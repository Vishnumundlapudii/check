# DeepSeek-OCR: Is an Image the Best Way to Compress Text?
Every so often, a research paper comes out that seems to be about one thing, but is secretly and much more excitingly about something else entirely. The new [DeepSeek-OCR paper](https://arxiv.org/html/2510.18234v1) is a perfect example.
On the surface, it’s a powerful new model for Optical Character Recognition (OCR). But hidden inside this paper is a brilliant experiment that tackles one of the biggest challenges for Large Language Models (LLMs): processing long documents.
Here’s the core problem: Large Language Models (LLMs) face a significant computational challenge when processing long textual content. This is because the processing cost doesn't just grow linearly with the length of the document—it often scales quadratically. In simple terms, this means a 10x longer document isn't just 10x harder to process, but potentially 100x harder. This quadratic scaling makes feeding long documents, like a 50-page report, incredibly slow and expensive.

**The DeepSeek team asked a radical question:** *What if the best way to "feed" a long document to an AI isn't as text at all? What if a 2D image of a page could serve as a highly efficient "compressed" file for the 1D text it contains?* This idea is what the paper calls **"optical compression”**. 

Even Andrej Karpathy noted, the DeepSeek-OCR paper raises a deeper question: **are pixels a better input for LLMs than text?** He suggests that our current text tokens might be "inherently wasteful" and just "historical baggage" that could eventually be replaced by visual inputs for greater efficiency.


![](DeepSeek-OCR%20Is%20an%20Image%20the%20Best%20Way%20to%20Compress%20Text/image%204.png)<!-- {"width":496} -->

But how could you even test such a thing? You would need a model that can take the "compressed file" (the image) and "decompress" it (spit out the original text) with perfect accuracy.

This makes **OCR the natural, perfect test bed for the idea**. The task *is* the experiment. Can a model look at a picture of a page and reconstruct all 1,000 words from it? If it can, how "small" can we make the visual data and still have it work?

This is what DeepSeek-OCR is really all about. It's an architecture designed from the ground up to test this hypothesis. It’s less of a simple OCR tool and more of a proof-of-concept for a new way of thinking about context. To do it, they had to build a special **"smart compressor"** to turn the image into a tiny, information-rich package for the language model to read.
And in the process of proving this hypothesis, they just so happened to create a state-of-the-art OCR model. As the paper shows, on the [OmniDocBench](https://github.com/opendatalab/OmniDocBench) benchmark, DeepSeek-OCR surpasses strong competitors like [GOT-OCR 2.0](https://arxiv.org/abs/2409.01704) while using only **100 vision tokens** (compared to 256 for GOT-OCR2.0). It also outperforms massive models like [MinerU2.0,](https://github.com/opendatalab/MinerU) which requires over **6,000 tokens per page** on average to do the same job.
In this article, we will dissect the architecture behind this simple but brilliant idea and understand how it works under the hood. In the end, we will also learn how you can run the model on [E2E Networks AI Platform](https://www.e2enetworks.com/).

---
# The Problem with Previous Approaches
Before we dive into DeepSeek's solution, it's helpful to know what everyone else was doing and why it wasn't good enough for this "optical compression" idea.
Most modern vision models (VLMs) use one of three main strategies to "see" a document, all of which have some problems.

![](DeepSeek-OCR%20Is%20an%20Image%20the%20Best%20Way%20to%20Compress%20Text/image.png)

1. **The Dual-Tower Approach (like [Vary](https://arxiv.org/abs/2312.06109)):** This method uses two different vision encoders *in parallel*. One encoder looks at a low-resolution version of the whole page (for layout), and a separate encoder looks at high-resolution patches (for detail). While this captures both views, the model then has to figure out how to combine these two separate outputs. This process is complex, requires two pre-processing steps, and is difficult to deploy and train efficiently.
2. **The Tiling Approach (like InternVL):** This model "cuts up" a single high-resolution image into many small tiles (e.g., 384x384 pixels) and processes them one by one. The problem is two-fold: it creates a massive number of vision tokens (one set for *each* tile), and it struggles with context. The model can read the text in Tile A and Tile B, but it has no easy way of knowing how they are positioned relative to each other on the full page.
3. **The Adaptive Approach (like Qwen2.5-VL):** This method takes the *entire* high-resolution image and processes it all in one go, without tiling. While flexible, this approach generates a massive number of vision tokens based on the image's size. A large, high-resolution document can create a sequence of tokens so long that it leads to extreme memory usage and can easily cause a GPU to run out of memory.

The common theme here? **All these methods generate a *massive amount of vision tokens*.** This is the central bottleneck. Because the attention mechanism in a Transformer scales quadratically, doubling the number of tokens doesn't just double the computation - it can square it. This leads to high GPU memory usage and much slower processing times, defeating the purpose of compression. And in OCR applications we require very fast processing times.

This is shown perfectly in the benchmark chart below.

![](DeepSeek-OCR%20Is%20an%20Image%20the%20Best%20Way%20to%20Compress%20Text/image%202.png)

Look at the X-axis, "Average Vision Tokens per Image." You'll see models like MinerU2.0 and InternVL clustered on the far left, using an average of **6,000 to 7,000 vision tokens** per page. This is the problem DeepSeek set out to solve.
Now, look at the far right of that same chart. You'll see the **DeepSeek-OCR models**. They are achieving *better* performance (a lower edit distance) while using dramatically fewer tokens. Some versions use **fewer than 800 tokens** on average.
This chart tells the whole story. The older methods are computationally heavy. The DeepSeek-OCR architecture, which we are about to explore, is designed for efficiency.

---
# The Architecture: A Deep Dive into "Optical Compression"
At its heart, the DeepSeek-OCR model is an elegant solution. Imagine trying to read an entire, full-sized newspaper page laid out on a table. If you're too far away, you can see the *layout* (the headlines, the columns, the advertisements) but the text is just a blurry line. If you press your face against the paper, you can read a single word, but you have no idea where you are on the page.

![](DeepSeek-OCR%20Is%20an%20Image%20the%20Best%20Way%20to%20Compress%20Text/image%203.png)

Standard vision models face a similar challenge. They either shrink the high-resolution image, losing all the fine detail (the "blurry newspaper" problem), or they try to process every pixel, creating a massive number of "vision tokens" that is computationally expensive and slow.

DeepSeek-OCR is engineered to solve this. Its inspiration is not just to build a better OCR, but to test a fundamental hypothesis: **can a 2D image act as a highly efficient "compressed" format for 1D text?** 

To achieve this, the architecture is split into two main components: a highly specialized Encoder and an efficient Decoder.

## The DeepEncoder: The "Smart Compressor"

The real magic happens in the encoder, which the paper calls **DeepEncoder**. This isn't one single model but a specialized, three-stage assembly line, with each stage passing its results to the next.

![](DeepSeek-OCR%20Is%20an%20Image%20the%20Best%20Way%20to%20Compress%20Text/image%205.png)

Let's trace the journey of a single $1024 \times 1024$ image to see how this works.
### **Stage 1: The Perceiver (SAM Encoder)**

* **What it is:** The image first enters a **pretrained [SAM \(Segment Anything Model\)](https://segment-anything.com/) image encoder**. SAM was introduced by Meta in April 2023 as a "foundation model for image segmentation." Its purpose was to segment *any* object in *any* image with zero-shot generalization, for which it was trained on a massive dataset of over 1 billion segmentation masks.
* **Why this is perfect:** For this architecture, we aren't using SAM's segmentation *output*. We are using its powerful **ViT (Vision Transformer) encoder**. Because SAM was trained to be a master of segmentation, its encoder backbone became incredibly good at understanding visual "perception" - things like boundaries, object relationships, and layout. This is the exact skill set needed to perceive the structure of a document.
* **How it works:** Like all Vision Transformers, it first "sees" the image by dividing it into a grid of $16 \times 16$ pixel patches. For our $1024 \times 1024$ image, this creates $(1024 / 16) \times (1024 / 16) = 64 \times 64 = \textbf{4096}$ patch tokens. This is a *massive* number of tokens. This first-stage SAM encoder is a relatively small 80M parameter model that uses **window attention**. This means it processes the 4096 tokens in small, local groups or "windows" rather than trying to compare every token to every other token. This design choice dramatically reduces the computational load and keeps activation memory low, making it possible to handle the high-resolution input with lower latencies and memory usage. Its job is to act as the initial "perceiver," analyzing the local shapes and layouts of the document.

### **Stage 2: The Compressor (Convolutional)**

* **What it is:** The 4096 feature tokens from SAM, now encoded with rich perceptual information, are immediately fed into a **16x convolutional compressor**. This "neck" is part of the SAM encoder's architecture, and it's the core of the compression.
* **How it works:** It's a series of 2D convolutional layers that downsample the *feature tokens* (not the image). It takes the 4096 tokens and downsample them to 256 tokens doing a 16x compression ($4096 / 16 = 256$).

We now have a tiny, 256-token summary of the original image, but it's a "smart" summary, rich with the perceptual features extracted by SAM. This is the crucial step that makes the next stage possible.

### **Stage 3: The Knower (CLIP Encoder)**

* **What it is:** This compact set of 256 tokens is now passed to the final stage: a **pretrained [CLIP \(Contrastive Language-Image Pre-Training\)](https://openai.com/index/clip/) image encoder**. CLIP was introduced by OpenAI in January 2021. Its goal was to connect images and text in a shared "embedding space." It was trained on 400 million image-text pairs from the internet, learning to associate visual concepts (like a picture of a dog) with language concepts (like the words "a photo of a dog").
* **Why this is perfect:** While SAM is a master of *perception* (where are the boundaries?), CLIP is a master of *knowledge* and *meaning* (what *is* this object?). By using CLIP's pretrained image encoder (specifically a 300M parameter ViT-L model), this architecture gains a deep, semantic understanding of the document's content.
* **How it works:** This is where the *type* of attention flips. Because we are now dealing with only 256 tokens (thanks to the compressor), this larger, more powerful model can afford to use **dense global attention**. It compares every single token to every *other* token, building a holistic, global understanding of the page. The global attention can now analyze the *relationships* between the compressed tokens. It understands that a cluster of tokens from SAM isn't just a "box shape" but represents a "table," and another cluster of wavy lines isn't just "scribbles" but a "handwritten signature." This fusion of local perception and global knowledge is what gives the final 256 tokens the richness to represent the entire document.

The entire DeepEncoder flow is a brilliant serial design: **Perceive Locally (SAM)** $\rightarrow$ **Squeeze (Compressor)** $\rightarrow$ **Understand Globally (CLIP)**.

### **Handling Any Document: The "Gundam" Strategy**

The process above describes encoding one $1024 \times 1024$ image. But what about our "blurry newspaper" problem? A single, shrunken-down $1024 \times 1024$ view might capture the layout but will blur tiny text into unreadability.

This is where the **"Gundam" mode** comes in, which is the model's advanced multi-view strategy for handling real-world, high-resolution documents. This introduces a **second level of "patching"** that is crucial to understand.

1. **Level 1: Gundam Tiling (The Pre-processing Step)**
   This step happens before the encoder. It's designed to create two sets of "views" from the single, giant original image:
   * **The Global View:** The *entire* document is shrunk down to a "base" resolution (e.g., $1024 \times 1024$). This is the "zoomed-out" view that gives the model the complete page layout.
   * **The Local Views:** The *original, high-resolution* image is sliced into multiple large "tiles" (e.g., $640 \times 640$). These are *not* the 16x16 patches. They are large, high-fidelity close-ups that allow the model to "zoom in" and read the fine-grained text.
2. **Level 2: ViT Patching (The Encoder's First Step)**
   This is the critical part. The DeepEncoder is now fed all of these images (e.g., 1 Global View + 4 Local Views). It processes each one independently. The very first thing the encoder's SAM component does to every single image it receives is divide it into $16 \times 16$ pixel patches.
   * **For the Global View (**$1024 \times 1024$**):** It is divided into $(1024/16)^2 = \textbf{4096}$ patches. These 4096 tokens go through the SAM $\rightarrow$ Compressor $\rightarrow$ CLIP pipeline.
   * **For *each* Local View (**$640 \times 640$**):** *Each tile* is divided into $(640/16)^2 = \textbf{1600}$ patches. These 1600 tokens go through the *same* SAM $\rightarrow$ Compressor $\rightarrow$ CLIP pipeline.

So, to be absolutely clear: the "Gundam" strategy is just a clever way of feeding the encoder *multiple* images (the global view + the local tiles). The encoder then, in turn, applies its *own* internal 16x16 patching logic to *all* of those images to process them.

### **The Final Token Sequence**
This multi-view strategy produces multiple sets of final tokens, which are then combined into one master sequence for the decoder. Let's use a concrete example:
* **1 Global View** ($1024 \times 1024$): Is divided into 4096 patches, which are processed by the full encoder pipeline and compressed by $16 \times$ to $\textbf{256}$ final tokens.
* **4 Local Views** (e.g., 4 tiles at $640 \times 640$): *Each* tile is divided into 1600 patches, processed by the full encoder pipeline, and compressed by $16 \times$ to $100$ tokens *each*.
  * This gives us a total of $4 \times 100 = \textbf{400}$ local tokens.

The model flattens all tokens from the local views first, then concatenates all tokens from the global view, and finally appends a single, special \[VIEW\_SEPARATOR\_TOKEN\] at the very end.

The final sequence fed to the language model looks like this:

\[All\_Local\_Tokens\_Stitched\] \[All\_Global\_Tokens\_Stitched\] \[SEPARATOR\_TOKEN\]

In our example, this would be a single sequence of ($400 \text{ local} + 256 \text{ global} + 1 \text{ separator}) = \textbf{657}$ tokens. This is the final package, containing the zoomed-in details to read the text and the zoomed-out context to understand the layout, all in one hyper-efficient package.

## The Decoder: The "Efficient Brain"

Once the DeepEncoder has meticulously crafted its compact sequence of vision tokens (like the 657 tokens in our example), this sequence is ready for the second main component: the Decoder. This is the language model that actually reads the visual information and your text prompt, and then writes the final output.

#### **What it is:**
* The decoder is a **DeepSeek-3B-MoE model**. The "3B" indicates it has the *potential capacity* of a 3-billion-parameter model, but the "MoE" (Mixture of Experts) part is the key to its efficiency.
#### **Why it's perfect for this task:**
* OCR is a demanding task. Unlike simple image captioning ("a cat sitting on a mat"), OCR often requires generating *thousands* of text tokens to reproduce the full content of a document page.
* Running a dense, multi-billion parameter model to generate that much text can be slow and computationally costly.
* The MoE architecture provides a way to get the *performance* of a larger model while keeping the *inference cost* (the computation needed to generate text) significantly lower. This makes it ideal for the high-throughput demands of OCR.

#### **How it works:**
1. **Mixture of Experts (MoE) Explained:** Think of a standard large language model (LLM) as one giant brain trying to know everything. An MoE model is different. It's like having a **team of specialists (the "experts")** and a smart **dispatcher (the "router" or "gating network")**.
   * **The Experts:** In the DeepSeek-3B-MoE model used here, there are **64 distinct "expert" networks** available within certain layers of the model. Each expert is like a smaller neural network (often just a specific part like the Feed-Forward Network layer in a Transformer block).
   * **The Router:** When the model needs to process a token (whether it's part of your text prompt or one of the visual tokens from the encoder), the router looks at that token and intelligently decides which experts are best suited to handle it.
   * **Sparse Activation:** Instead of activating *all* 64 experts, the router selects only a small number—in this case, just **6 out of the 64**—to process that specific token.
   * **Shared Experts:** Additionally, the DeepSeekMoE architecture includes **2 "shared" experts** that are *always* activated for every token. These shared experts likely handle common, fundamental language processing tasks, ensuring a baseline level of coherence and knowledge integration, while the 6 routed experts provide specialized insights based on the token's context.
   * **Efficiency:** Because only a small fraction of the model (2 shared + 6 routed experts) is activated for each token, the total computation is drastically reduced compared to activating the entire 3-billion-parameter equivalent. This model activates roughly 570 million parameters per token.
2. **Input Processing:** The decoder receives a single, combined sequence. It starts with your text prompt (e.g., \<image\>\n\<|grounding|\>Convert the document to markdown.), but the special \<image\> token has been replaced by the entire sequence of visual tokens generated by the DeepEncoder (e.g., our 657 vision tokens).
3. **Generating Text:** The MoE decoder then processes this combined sequence, using its router to selectively engage experts for each token. It generates the final output text (like the Markdown version of the document) one token at a time, predicting the next most likely word based on both the visual information and the text generated so far.

By pairing the highly efficient DeepEncoder with the computationally efficient MoE Decoder, the DeepSeek-OCR architecture achieves a remarkable balance: it can process high-resolution images to capture fine details while generating extensive text output with impressive speed and resource efficiency.

# Training Details: Crafting the Compressor
Building a model like DeepSeek-OCR requires a massive and carefully curated dataset. The core was **30 million PDF pages** covering around 100 languages, giving it a broad understanding of typical documents. But to handle complex content, they added specialized "OCR 2.0" data: millions of synthetic images of **charts, chemical formulas, and geometric figures**. This crucial step teaches the model to parse structure, not just characters. Finally, to ensure it remained a capable vision-language model, they mixed in 20% general vision data (specifically **100 million samples from the LAION dataset**) and 10% pure text data. The final blend was roughly 70% OCR data, 20% general vision, and 10% text.

The training itself happened in two stages. First, the **DeepEncoder** (the "smart compressor" part of the architecture) was trained independently using a next-token prediction framework. The goal here was to make it exceptionally good at one thing: taking any document image and creating that compact, information-rich visual summary. It learned this skill on the vast OCR and the 100M LAION image dataset.

Once the DeepEncoder was an expert compressor, it was connected to the **DeepSeek-3B-MoE decoder** (the "efficient brain"). The system was then trained together on the full data mix, but with a crucial detail: the first parts of the encoder (the **SAM component and the convolutional compressor**) were **frozen**. They acted like a fixed "vision tokenizer." Only the **CLIP component** of the encoder and the **entire MoE decoder** remained trainable. This second stage focused specifically on teaching the decoder how to read and interpret the highly compressed visual tokens coming from the now-fixed initial stages of the encoder. This large-scale effort used a cluster of **20 nodes (each with 8 NVIDIA A100 GPUs)** and techniques like pipeline parallelism to train efficiently.

# The Results: How Good is the Compression?
After training this carefully designed model on a massive dataset, the crucial question remains: did the "optical compression" idea actually work? The results, tested on the Fox benchmark using real English documents, are quite remarkable.

![](DeepSeek-OCR%20Is%20an%20Image%20the%20Best%20Way%20to%20Compress%20Text/image%206.png)

This table shows the model's performance (Precision) when trying to reconstruct text from images, using either 64 vision tokens (Tiny mode) or 100 vision tokens (Small mode). The "Text Tokens" column shows the original length of the document (how many standard text tokens it would take), and "Compression" shows the ratio achieved (Text Tokens / Vision Tokens).
The key takeaway is in the top few rows. For documents up to about 1,000 text tokens, using just **100 vision tokens** (Small mode) achieves around **97% precision** at compression ratios between **7x and 10x**. This is incredibly close to lossless decompression! Even with only **64 vision tokens** (Tiny mode), the model maintains over **93% precision** up to an **11x compression** ratio.
However, the table also shows the limits. As the original documents get longer (1100+ text tokens) and the compression ratio pushes towards 20x, the precision starts to drop more significantly, especially in the ultra-compact 64-token mode. This suggests there's a sweet spot around 10x compression where the visual representation holds almost all the information, but pushing much beyond that starts to introduce information loss, like a "blurry" image making text hard to read.

The actual results are incredibly good for complex tasks involving complex document layouts, shapes, etc. Here are some examples from the paper:

![](DeepSeek-OCR%20Is%20an%20Image%20the%20Best%20Way%20to%20Compress%20Text/image%2013.png)


![](DeepSeek-OCR%20Is%20an%20Image%20the%20Best%20Way%20to%20Compress%20Text/image%2014.png)

![](DeepSeek-OCR%20Is%20an%20Image%20the%20Best%20Way%20to%20Compress%20Text/image%2015.png)

As you can see from the results, the model can not just be used for OCR but a variety of different tasks.

---

# Running DeepSeek-OCR on E2E Cloud
Since the DeepSeek-OCR model is open-source (using a permissive MIT license), we can easily run it on the E2E Networks AI platform. While the creators provide examples using Hugging Face Transformers, they recommend using [vLLM](https://docs.vllm.ai/en/latest/) for production use cases, especially for faster inference speeds. We'll follow that recommendation and showcase how to set up and run the model using vLLM for offline batch processing of documents.

### 1. Setting Up Your GPU Instance
First, you'll need a GPU instance on the E2E Networks platform.
* Log in to your E2E Networks account and navigate to the **Instances (Nodes)** section under **Products** in the left sidebar.
* Click the **CREATE INSTANCE** button.
![](DeepSeek-OCR%20Is%20an%20Image%20the%20Best%20Way%20to%20Compress%20Text/image%207.png)

- You'll be asked to **Choose Image**. Select the **PyTorch** image under the **Pre-built** tab. This image comes pre-installed with NVIDIA drivers, CUDA, PyTorch, and other essentials, saving you setup time.
  ![](DeepSeek-OCR%20Is%20an%20Image%20the%20Best%20Way%20to%20Compress%20Text/image%208.png)<!-- {"width":794} -->

* Next, choose a **Plan**. Select a GPU instance suitable for running the model. Here we select a A100 instance.
* Choose your **Instance Pricing**. For cost savings, especially for batch jobs that don't need to run 24/7, select the **Spot** plan. Just be aware that spot instances can be interrupted.

![](DeepSeek-OCR%20Is%20an%20Image%20the%20Best%20Way%20to%20Compress%20Text/image%209.png)
- Configure **Storage** (the default 30GB is likely enough to start, but add more if you have large datasets), add your **SSH key** for secure access, and configure any necessary **Security Group** settings.
* Click **Launch Instance**.


### Connecting to Your Instance
Once your instance status shows as "Running," you can connect to it.

![](DeepSeek-OCR%20Is%20an%20Image%20the%20Best%20Way%20to%20Compress%20Text/image%2010.png)

You have two main options:
* **SSH:** Use the provided SSH command in your local terminal or configure your favorite IDE (like VS Code with the Remote - SSH extension) to connect directly to the instance's IP address. This is usually the preferred method for development.
* **Jupyter Lab:** Click the Jupyter link provided in the instance details page to open a Jupyter Lab interface directly in your web browser.

### Installing vLLM and running the model
DeepSeek-OCR requires the nightly build of vLLM as it is introduced recently. Open a terminal on your instance (either via SSH or within Jupyter Lab) and install it using pip:

```bash
pip install -U vllm --pre --extra-index-url https://wheels.vllm.ai/nightly
```

Once you are done with the installation, you can now run the model. Here's a concise code snippet provided in the official vLLM documentation for running DeepSeek-OCR for batch processing:

```python
from vllm import LLM, SamplingParams
from vllm.model_executor.models.deepseek_ocr import NGramPerReqLogitsProcessor
from PIL import Image

# Create model instance
llm = LLM(
    model="deepseek-ai/DeepSeek-OCR",
    enable_prefix_caching=False,
    mm_processor_cache_gb=0,
    logits_processors=[NGramPerReqLogitsProcessor]
)

# Prepare batched input with your image file
image_1 = Image.open("path/to/your/image_1.png").convert("RGB")
image_2 = Image.open("path/to/your/image_2.png").convert("RGB")
prompt = "<image>\nFree OCR."

model_input = [
    {
        "prompt": prompt,
        "multi_modal_data": {"image": image_1}
    },
    {
        "prompt": prompt,
        "multi_modal_data": {"image": image_2}
    }
]

sampling_param = SamplingParams(
            temperature=0.0,
            max_tokens=8192,
            # ngram logit processor args
            extra_args=dict(
                ngram_size=30,
                window_size=90,
                whitelist_token_ids={128821, 128822},  # whitelist: <td>, </td>
            ),
            skip_special_tokens=False,
        )
# Generate output
model_outputs = llm.generate(model_input, sampling_param)

# Print output
for output in model_outputs:
    print(output.outputs[0].text)
```

**Understanding the Prompts and Output Format:**
DeepSeek-OCR works better with simple, direct prompts.
* "<image>\nFree OCR.": Use this for plain text extraction without detailed layout information.
* "<image>\n<|grounding|>Convert the document to markdown.": Use this prompt when you want the model to preserve the document structure (headings, lists, tables) and output Markdown. Crucially, this prompt also instructs the model to include **bounding box** information for detected text elements.

When using the Markdown prompt, the output interleaves the recognized text with special tags like this:
Recognized text segment goes here... <|ref|>text<|/ref|><|det|>[[x1, y1, x2, y2]]<|/det|> Another text segment... <|ref|>title<|/ref|><|det|>[[x1, y1, x2, y2]]<|/det|>
* <|ref|>type<|/ref|>: Indicates the *type* of the detected element (e.g., text, title, table, figure).
* <|det|>[[x1, y1, x2, y2]]<|/det|>: Provides the bounding box coordinates for that element. The coordinates (x1, y1, x2, y2) are normalized to a 1000x1000 grid, regardless of the original image size. (x1, y1) is the top-left corner, and (x2, y2) is the bottom-right corner.

![](DeepSeek-OCR%20Is%20an%20Image%20the%20Best%20Way%20to%20Compress%20Text/image%2011.png)

This bounding box information is incredibly useful as you can see in the above figure. You can parse these coordinates from the Markdown output and use a library like Pillow (PIL) in Python to draw rectangles directly onto the original image, visually highlighting the text segments, titles, tables, etc., that the model identified, as shown in the example image above.


Now, let’s understand some key configuration tips to run the model optimally in vLLM:
* **Custom Logits Processor:** `NGramPerReqLogitsProcessor` (provided by vLLM or potentially needing import from DeepSeek's repo) is recommended for optimal OCR/Markdown generation. OCR output can be very long and repetitive (think tables or formatted lists). This processor prevents the model from getting stuck repeating the same sequence of tokens (n-grams) within a certain window, leading to more stable and accurate layout generation.
* **Disable Caching:** For OCR batch jobs, prefix caching (enable_prefix_caching=False) and multi-modal processor caching often don't provide benefits (as each page is unique) and can add overhead. Disabling them is recommended.
* **Use Plain Prompts:** As mentioned above, stick to simple prompts. The [DeepSeek-OCR repository](https://github.com/deepseek-ai/DeepSeek-OCR/blob/2ac6d64a00656693b79c4f759a5e62c1b78bbeb1/DeepSeek-OCR-master/DeepSeek-OCR-vllm/config.py#L27-L37) offers more prompt examples for different tasks (e.g., parsing figures).
* **Adjust Batch Size/Tokens:** Depending on your GPU, tuning parameters like max_num_seqs (in LLM) or max_num_batched_tokens (if set explicitly) can improve throughput.

Once you have the sample code above running, you can now modify it or run the model for any of your tasks. 

For example here’s the result on a fairly difficult to read handwritten letter by Ramanujan to GH Hardy. It’s doing an incredible job of parsing all the equations and letters.

![](DeepSeek-OCR%20Is%20an%20Image%20the%20Best%20Way%20to%20Compress%20Text/image%2012.png)

The paper provides more such results and you are free to test out the model on your use-case specific documents.

### Testing throughput on different GPUs
We ran batch inference effectively using the default "Gundam" mode settings (which the processor typically uses for large images passed via `multi_modal_data={"image": image}`) on the OmniDocBench dataset to get a sense of its speed on various E2E Networks GPU instances. Here are the approximate pages-per-second (PPS) we observed:

| **GPU**     | **Pages/sec (PPS)** | **Pages/day (Approx.)** | **Speedup vs A100** |
|-------------|---------------------|-------------------------|---------------------|
| NVIDIA A100 | 3.13                | ~270k                   | 1.00x               |
| NVIDIA H100 | 4.65                | ~401k                   | 1.49x               |
| NVIDIA H200 | 5.26                | ~455k                   | 1.68x               |

As the table shows, the newer **H100 and H200 GPUs** offer significant speedups compared to the A100, achieving approximately 1.5x and 1.7x the throughput, respectively. This translates to processing an incredible number of pages per day **(over 400k-450k)**, potentially exceeding the speed of many proprietary OCR solutions for large-scale batch tasks. These numbers give you an idea of the throughput you can expect for large-scale document processing tasks on the platform. Remember that actual performance can vary based on document complexity, image resolution, batch size, and other factors.

---

# Conclusion

This exploration of DeepSeek-OCR reveals it's far more than just a new state-of-the-art document OCR model. The project is truly a proof-of-concept for a fascinating and powerful idea: using 2D images as a highly efficient compression format for 1D text. The central finding that the model can "decompress" a page of text with ~97% precision from visual data that is 10 times smaller is a significant breakthrough.

This "optical compression" concept offers a promising new direction for tackling one of the biggest challenges in AI: **managing long-term context**. The paper itself proposes intriguing applications, such as compressing a chatbot's dialogue history. Imagine a system where recent conversations are clear and high-fidelity, but older messages are progressively "forgotten" by being rendered into smaller, lower-resolution images. This would save massive amounts of computational resources, mimicking a human-like memory system. The model is open-source and ready for real-world tasks. As we walked through, it can be deployed for practical, high-throughput document processing applications.

---

# References
- [DeepSeek-OCR paper](https://arxiv.org/html/2510.18234v1)
- [DeepSeek-OCR: Contexts Optical Compression Github repository](https://arxiv.org/html/2510.18234v1)
---
title: Getting started | E2E Cloud
description: Auto-generated documentation from https://docs.e2enetworks.com/docs/tir/Nodes/GuideTIR/
slug: /getting-started-e2e-cloud
tags:
  - documentation
  - auto-generated
sidebar_position: 1
---

import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';


# Getting started | E2E Cloud

:::info Source
📄 **Original Documentation**: [https://docs.e2enetworks.com/docs/tir/Nodes/GuideTIR/](https://docs.e2enetworks.com/docs/tir/Nodes/GuideTIR/)  
🤖 **Generated on**: 2025-07-30 12:31:32  
⚡ **Enhanced with**: AI content restructuring and OCR image analysis
:::

---

TIR Nodes are fully collaborative environments that make AI development possible. They combine the power of containers, Jupyter Labs, and AI/ML frameworks to create a readily usable workspace for you and your entire team.

Some of the most common use cases are:

- Run a script or notebook to fine-tune a Large Language Model (LLM) on a single GPU using PyTorch or Hugging Face train.
- Run a script or notebook to tokenize and fine-tune LLMs or Diffusion models with multiple GPUs (single machine) using DeepSpeed and Accelerate.
- Open and run a Jupyter notebook (.ipynb) from platforms like GitHub, Kaggle, or Colab.
- Download and review datasets stored on TIR or other platforms like Hugging Face.
- Download and test models like Stable Diffusion or any LLM.

A TIR node is a fully functional coding environment.
If you prefer to work with the command line (shell) over Jupyter Labs, you can configure SSH on a notebook (node). This way, you can upload your data using SFTP or sync your code with Git tools and run the scripts as you would on your local system.

### Getting Started with Nodes on TIRâ

- 1. User needs to log in using myaccount credentials and select the TIR AI platform to use resources on TIR.
- 2. User will land on the TIR landing page and create a project using the "Create project" button.
- 3. NOTE: The project will be created in the user's private workspace.
- 4. Once you are in the newly created project, click on "Nodes" in the side panel to launch the resource.
- 5. User can select from the available images to create a node.

1. User needs to log in using myaccount credentials and select the TIR AI platform to use resources on TIR.

2. User will land on the TIR landing page and create a project using the "Create project" button.

3. NOTE: The project will be created in the user's private workspace.

4. Once you are in the newly created project, click on "Nodes" in the side panel to launch the resource.

5. User can select from the available images to create a node.

User can also filter the nodes based on the need using TIR pre-built, Container Registry, and Base OS.

- 1. Next, you can choose a CPU or GPU plan. Feel free to choose the Free Tier plan for this exercise.
- 2. User needs to select the GPU or CPU required plan. In the case of CPU, the user can always select the Free Tier Plan in the exploration stage. In the case of GPU, if the required plan is not available, the user can always request the plan, and we will notify the user once it is available via email.
- 3. Choose an appropriate name for your node and select the type of nodes as New Notebook or Import Notebook. If Import Notebook is selected, then the user needs to provide the URL for the node.

1. Next, you can choose a CPU or GPU plan. Feel free to choose the Free Tier plan for this exercise.

2. User needs to select the GPU or CPU required plan. In the case of CPU, the user can always select the Free Tier Plan in the exploration stage. In the case of GPU, if the required plan is not available, the user can always request the plan, and we will notify the user once it is available via email.

3. Choose an appropriate name for your node and select the type of nodes as New Notebook or Import Notebook. If Import Notebook is selected, then the user needs to provide the URL for the node.

Choosing New Notebook will open an empty JupyterLab, while Import Notebook will give the user the flexibility to seamlessly pull publicly available nodes from GitHub or Colab.

- 1. Select the workspace size you want to create. Please note, by default, 30 GB of free workspace is provided with each node.
- 2. (Optional) Set Enable SSH Access switch to enabled to add or select your SSH key.
- 3. When the node is ready, you will see both Jupyter Labs and SSH options (if configured). Choose any of these to access the node environment.

1. Select the workspace size you want to create. Please note, by default, 30 GB of free workspace is provided with each node.

2. (Optional) Set Enable SSH Access switch to enabled to add or select your SSH key.

3. When the node is ready, you will see both Jupyter Labs and SSH options (if configured). Choose any of these to access the node environment.

### Node Imagesâ

TIR environments use container images that act as blueprints, providing the libraries, tools, and dependencies required to run each node. TIR supports a variety of pre-built images equipped with popular machine learning and deep learning frameworks such as Jupyter, FramePack, and ComfyUI. These pre-built images are optimized for performance and compatibility, making them ideal for most use cases.

- Base OS Image: The Base image is a container environment with no pre-installed packages or tools. It offers maximum flexibility for users who prefer to set up their own dependencies and frameworks from scratch. This image is ideal for highly customized workflows that require specific package versions or configurations. It is light-weight and well-suited for building tailored environments from the ground up.
- Jupyter Image: The Jupyter image comes pre-installed with Jupyter Notebook, making it an excellent choice for interactive, notebook-based development. It allows users to write, test, and visualize code directly within the browser using .ipynb files. This image is particularly useful for data analysis, experimentation with machine learning models, and educational purposes.
- ComfyUI: The ComfyUI image is designed for users working on visual and generative AI workflows. It includes the ComfyUI interface pre-installed, enabling a graphical, drag-and-drop environment for building model pipelines and experimenting with creative tools. This image is ideal for tasks that benefit from visual feedback, such as image generation, flow-based programming, or UI-driven model orchestration. It provides a ready-to-use environment for rapid prototyping in visual domains.
- FramePack: The FramePack image comes pre-configured with the FramePack framework, catering to specialized use cases that depend on it. It is pre-tuned for seamless integration and is well-suited for users who need immediate access to FramePackâs features without additional setup. Whether for research, development, or deployment, this image streamlines workflows by offering a ready-made environment tailored to FramePack-based projects.

Base OS Image: The Base image is a container environment with no pre-installed packages or tools. It offers maximum flexibility for users who prefer to set up their own dependencies and frameworks from scratch. This image is ideal for highly customized workflows that require specific package versions or configurations. It is light-weight and well-suited for building tailored environments from the ground up.

Jupyter Image: The Jupyter image comes pre-installed with Jupyter Notebook, making it an excellent choice for interactive, notebook-based development. It allows users to write, test, and visualize code directly within the browser using .ipynb files. This image is particularly useful for data analysis, experimentation with machine learning models, and educational purposes.

```text
.ipynb
```

ComfyUI: The ComfyUI image is designed for users working on visual and generative AI workflows. It includes the ComfyUI interface pre-installed, enabling a graphical, drag-and-drop environment for building model pipelines and experimenting with creative tools. This image is ideal for tasks that benefit from visual feedback, such as image generation, flow-based programming, or UI-driven model orchestration. It provides a ready-to-use environment for rapid prototyping in visual domains.

FramePack: The FramePack image comes pre-configured with the FramePack framework, catering to specialized use cases that depend on it. It is pre-tuned for seamless integration and is well-suited for users who need immediate access to FramePackâs features without additional setup. Whether for research, development, or deployment, this image streamlines workflows by offering a ready-made environment tailored to FramePack-based projects.

### Node Optionsâ

TIR nodes are extremely powerful and flexible. While most configurations have a default to make the user's life easier, sometimes you may need to tweak the knobs. The following are the configurations that you can tweak in a node environment:

- Enable SSH: You can enable SSH access on the node using a public key or password (not recommended). If you decide to enable SSH after starting a node, you will have to first stop the node before making changes.
- Disk Size: Each TIR node can have a disk size of up to 5000GB. The default is 30GB. The selected disk will be mounted at /home/jovyan in your node environment. We recommend using this path as your workspace so in case of restarts, your content will be persistent. Since TIR is container-native, the changes that you make to any other paths on the node will not be persisted on restarts. You can extend the disk size after starting the container as well. This workspace will be deleted when the associated node is deleted.

Enable SSH: You can enable SSH access on the node using a public key or password (not recommended). If you decide to enable SSH after starting a node, you will have to first stop the node before making changes.

Disk Size: Each TIR node can have a disk size of up to 5000GB. The default is 30GB. The selected disk will be mounted at /home/jovyan in your node environment. We recommend using this path as your workspace so in case of restarts, your content will be persistent. Since TIR is container-native, the changes that you make to any other paths on the node will not be persisted on restarts. You can extend the disk size after starting the container as well. This workspace will be deleted when the associated node is deleted.

```text
/home/jovyan
```

Please raise a support ticket if you need more than 5TB of disk workspace.

- Local NVME Storage: Only available for H100 plans. This fast local storage will be available at /mnt/local and only for the duration of the run. We recommend using this path when you need faster writes (e.g., save model checkpoints) or reads. Be sure to move this data to the EOS bucket or under /home/jovyan before shutting down the node. This type of storage is fixed and cannot be expanded at any time during the node cycle.
- Plan (Pricing): You can choose between an hourly or committed plan. We recommend using committed plans as they offer discounts and may also offer access to local NVME storage (for H100 plans only).
- Node Image: TIR environments are container-native. You can use pre-built images with well-known frameworks like PyTorch, Transformers, or customize the pre-built images. You can make your own images TIR-compatible using the image builder utility. We recommend starting with pre-built images. In case you need to install packages from pip or apt-get, we recommend doing so from a jupyter notebook (.ipynb) or maintaining requirements.txt.
- Configuration: TIR offers a variety of CPU and GPU options. We recommend using A100 or H100 for the best performance.
- Update Node: You can upgrade or downgrade both the configuration (e.g., upgrade from CPU to GPU) and Plan (e.g., hourly to committed) of a node if desired. This is a useful option when restarting nodes and the original hardware plan (GPU) on the node is no longer available.
- Stop Node: If the plan and configuration allow, you can stop a node and restart it. In the case of an hourly plan, you will not be billed for the GPU or CPU when the node is in a stopped state. However, if your disk usage is beyond the free tier, you will be charged for it.
- Delete Node: When a node is deleted, all the resources associated with it will be deleted, including the workspace (disk).

Local NVME Storage: Only available for H100 plans. This fast local storage will be available at /mnt/local and only for the duration of the run. We recommend using this path when you need faster writes (e.g., save model checkpoints) or reads. Be sure to move this data to the EOS bucket or under /home/jovyan before shutting down the node. This type of storage is fixed and cannot be expanded at any time during the node cycle.

```text
/mnt/local
```

```text
/home/jovyan
```

Plan (Pricing): You can choose between an hourly or committed plan. We recommend using committed plans as they offer discounts and may also offer access to local NVME storage (for H100 plans only).

Node Image: TIR environments are container-native. You can use pre-built images with well-known frameworks like PyTorch, Transformers, or customize the pre-built images. You can make your own images TIR-compatible using the image builder utility. We recommend starting with pre-built images. In case you need to install packages from pip or apt-get, we recommend doing so from a jupyter notebook (.ipynb) or maintaining requirements.txt.

```text
jupyter notebook (.ipynb)
```

```text
requirements.txt
```

Configuration: TIR offers a variety of CPU and GPU options. We recommend using A100 or H100 for the best performance.

Update Node: You can upgrade or downgrade both the configuration (e.g., upgrade from CPU to GPU) and Plan (e.g., hourly to committed) of a node if desired. This is a useful option when restarting nodes and the original hardware plan (GPU) on the node is no longer available.

Stop Node: If the plan and configuration allow, you can stop a node and restart it. In the case of an hourly plan, you will not be billed for the GPU or CPU when the node is in a stopped state. However, if your disk usage is beyond the free tier, you will be charged for it.

Delete Node: When a node is deleted, all the resources associated with it will be deleted, including the workspace (disk).

### Node Statusâ

- Waiting: The node instance is being deployed on the hardware of your choice.
- Running: The node is active, and you can use either Jupyter Labs or SSH (if enabled) to access it.
- Stopped: The node is not assigned to any machine. However, the workspace (disk mounted at /home/jovyan) will continue to exist until you delete the node. Depending on the size of the disk, you will be charged for the usage.
- Pending: The node enters this state when the requested inventory is not currently available. It remains in the Pending state for 48 to 72 hours while waiting for resources to become free.
- Expired: If the inventory is still unavailable after 72 hours, the node transitions to the Expired state. This indicates that the resource request is no longer in the queue and will not be fulfilled.

```text
/home/jovyan
```

### How to Create Node?â

To create a Node, you have to click on Create Node, which is at the right corner of the page.

![Create Node](/img/image_f943c7064e.png)

:::tip Screenshot Explanation
This image appears to be a screenshot of a private workspace dashboard, likely from a cloud computing or data science platform. The dashboard is labeled as "Private Workspace" with a unique identifier ("pri-019011218434") and displays various navigation options and features.

The main sections of the dashboard include:

1. **Nodes**: A section for managing computing nodes, with options to launch a new node and view existing nodes. Currently, no nodes are available.
2. **Datasets**: A section for managing datasets, with options to view and manage data. The section is currently empty, with no datasets listed.
3. **Inference**, **Pipelines**, **Foundation Studio**, **Vector Database**, and **Integrations**: These sections appear to be related to data science and machine learning workflows, but are not actively being used in this screenshot.
4. **API Tokens**: A section for managing API tokens, which are used for authentication and authorization.
5. **Settings**: A section for configuring account settings.

The dashboard also includes a sidebar with options to collapse or expand the navigation menu, as well as links to legal information, contact details, and copyright information.

The image is likely relevant to documentation related to setting up and using a private workspace on this platform, particularly for creating and managing computing nodes and datasets. The image may be used to illustrate the initial state of a private workspace, with no nodes or datasets created, and to provide a visual reference for users navigating the dashboard.
:::

<details>
<summary>📝 Extracted Text Content</summary>

```text
GDTIR 0 To MyaccounT | © & DB — & Private Workspace ~ P
Prose Private Workspace » pri-019011218434 » Nodes
pyj-013011213434 ~ 3)
Manage Nodes @ (Bi oocuwenrarion fo crearenooe |
88 Dashboard
Node Name Image Plan Name Plan Type Updated On Status Lab URL SSH Access. Actions
No node available, Click here to launch a new node.
E)__ Datasets
Rows perpage: 5 +  0-0of0
@ Inference v er pag
30 Pipelines v
Foundation Studio v
€, Vector Database
Integrations v
@_ API Tokens
Settings
& COLLAPSE SIDEBAR
Legal © 2024 E2E Networks Limited ™ Baya @ Contact Us
```

</details>


After clicking on the Create Node button, a page will appear. Now select the Node image option from TIR PRE-BUILT, BASE OS, and CONTAINER REGISTRY. Additionally, you can also perform the search on the Node Images.

![Node Image Selection](/img/image_b270df24a2.png)

:::tip Screenshot Explanation
**Image Description: Node Image Selection**

This image depicts a screenshot of a user interface for selecting a node image in a cloud-based platform, specifically TIR (Tensor Infrastructure Runtime). The interface presents users with options to choose from pre-built images, including those with PyTorch and Transformers, or to deploy custom images from a container registry.

**Key Features:**

1. **Node Image Options:** The interface lists various pre-built images, including:
	* TIR PRE-BUILT BASE OS
	* CONTAINER REGISTRY
	* Diffusers v0.27.2 with Python 3.10 and NVIDIA Cuda 12.4
	* NVIDIA RAPIDS 23.06 with Python 3.10 and NVIDIA Cuda
	* Fast.AI v2.7.14 with Python 3.10 and NVIDIA Cuda 12.1
2. **Node Resources:** Users can select a plan with CPU and GPU options to suit their needs.
3. **Node Storage:** Users can specify the Notebook Type, Workspace Size (in GB), and select pre-installed datasets for seamless integration.
4. **Security and Flexibility:** An SSH option is available for added security and flexibility.

**Relevance to Documentation:**

This image is relevant to the documentation as it illustrates the process of selecting a node image in the TIR platform. The context provided notes that the Base OS node image does not come with JupyterLab pre-installed, which is important for users to consider when making their selection. This image provides a visual representation of the options available to users, making it easier for them to understand the documentation and make informed decisions when working with the TIR platform.
:::

<details>
<summary>📝 Extracted Text Content</summary>

```text
C2)TIR GO TO MYACCOUNT Explore GenAl API © a @ Private Workspace A 7:
Al PLATFORM .
Private Workspace » default-project » Nodes » Create Node
i) Create Node FE DOCUMENTATION
ol ; .
rs) Image Details Image Details ©
2 TIR provides pre-built images including PyTorch and
Transformers, or users can alternatively deploy their
own custom images from the container registry. TIR provides pre-built images including PyTorch and Transformers, or users can alternatively deploy their own custom images from the container registry. Select the option that aligns
&] Select the option that aligns with your requirements. with your requirements.
TIR PRE-BUILT BASE OS CONTAINER REGISTRY [eo] G
@) ————
ga e Node Resources
TIR offers plans with CPU and GPU options. Select a
fi plan that suits your needs. R p D S f: t e
LZ @ Node storage D Affusers AP) aSt.al
TIR provide specify the Notebook Type to suit their
aa computational needs. Additionally, they can allocate
the desired Workspace Size (in GB) and select Diffusers v0.27.2 with Python 3.10 and NVIDIA Cuda 12.4 NVIDIA RAPIDS 23.06 with Python 3.10 and NVIDIA Cuda Fast.Al v2.7.14 with Python 3.10 and NVIDIA Cuda 12.1
datasets for seamless integration. For added pre-installed on Ubuntu 22.04 12.1 pre-installed on Ubuntu 20.04 pre-installed on Ubuntu 22.04
flexibility and security, an SSH option is available.
S © Node Detail
TIR provide specify the Notebook Type to suit their SciPy v1.7.0 v Jupyter CUDA... v Python 3.10 CUDA... v
computational needs. Additionally, they can allocate
the desired Workspace Size (in GB) and select
datasets for seamless integration. For added flexibility
and security, an SSH option is available. e
—_ © NVIDIA
S y ~ CUDA
NEXT
Legal © 2024 E2E Networks Limited ™ fini fi A) @ Contact Us
```

</details>


The Base OS node image does not come with JupyterLab pre-installed.

![Base OS Node](/img/image_015ea900f2.png)

:::tip Screenshot Explanation
This image appears to be a screenshot of a graphical user interface (GUI) for creating a new node on a platform, likely a cloud-based service for machine learning or artificial intelligence development. The interface is part of the "Private Workspace" section of the platform, specifically the "Nodes" area where users can create and manage their computing resources.

The image shows a form with various options for configuring a new node, including:

1. **Node Type**: The option to select a pre-built image from the platform's container registry, which includes popular frameworks like PyTorch and Transformers. Alternatively, users can deploy their own custom images.
2. **Node Resources**: The selection of computing resources, including CPU and GPU options, with specific plans available. In this case, a Python 3.10 environment with CUDA support on an Ubuntu 22.04 base operating system is selected.
3. **Node Storage**: The allocation of storage space for the node, with options for different sizes.
4. **Datasets**: The selection of datasets for seamless integration with the node.
5. **SSH Option**: The availability of a secure shell (SSH) option for added flexibility and security.

The image also includes navigation elements, such as buttons to access documentation, create the node, and proceed to the next step. The screenshot is relevant to the documentation, as it illustrates the process of creating a new node on the platform, specifically when installing an image from the Container Registry. The image helps to clarify the options and configurations available to users during this process.
:::

<details>
<summary>📝 Extracted Text Content</summary>

```text
C2)TIR GO TO MYACCOUNT Explore GenAl API © a © Private Workspace wv A 5
Al PLATFORM
Private Workspace > default-project » Nodes » Create Node
E) Create Node Ey DOCUMENTATION
ol ; .
rs) Image Details Image Details ©
2 TIR provides pre-built images including PyTorch and
Transformers, or users can alternatively deploy their
own custom images from the container registry. TIR provides pre-built images including PyTorch and Transformers, or users can alternatively deploy their own custom images from the container registry. Select the option that aligns
&] Select the option that aligns with your requirements. with your requirements.
TIR PRE-BUILT BASE OS CONTAINER REGISTRY Q G
@) ———_
E @ Node Resources Python 3.10 CUDA... ¥ Ubuntu 22.04 ©
TIR offers plans with CPU and GPU options. Select a
fi plan that suits your needs.
cas © Node Storage | NVIDIA
TIR provide specify the Notebook Type to suit their
ty computational needs. Additionally, they can allocate CU DA
the desired Workspace Size (in GB) and select
datasets for seamless integration. For added
flexibility and security, an SSH option is available.
e © Node Detail
TIR provide specify the Notebook Type to suit their TT
computational needs. Additionally, they can allocate
the desired Workspace Size (in GB) and select
datasets for seamless integration. For added flexibility
and security, an SSH option is available.
NEXT
Legal © 2024 E2E Networks Limited ™ fini fi A) @ Contact Us
```

</details>


When installing an image from the Container Registry, the user must specify whether the selected image includes JupyterLab pre-installed or not.

![Container Registry Node](/img/image_817463d747.png)

:::tip Screenshot Explanation
**Image Description: Node Creation Interface for TIR Platform**

This image depicts a screenshot of the TIR (Tensor Instance Registry) platform's Node Creation interface, specifically the "Create Node" page within the "Private Workspace" section. The interface allows users to configure and deploy a new node, selecting from various options to suit their computational requirements.

**Key Features and Options:**

1. **Image Selection**: Users can choose from TIR's pre-built images, including PyTorch and Transformers, or deploy their own custom images from a container registry.
2. **Node Resources**: The interface offers plans with CPU and GPU options, enabling users to select a plan that aligns with their computational needs.
3. **Node Storage**: Users can choose an existing registry or create a new one, specifying the Notebook Type, Workspace Size (in GB), and select datasets for seamless integration.
4. **Additional Options**: An SSH option is available for added flexibility and security.

**Relevance to Documentation:**

This image is relevant to the documentation as it illustrates the Node Creation process within the TIR platform. The interface shown is a critical step in configuring and deploying a node, and understanding the various options and features available is essential for users to effectively utilize the platform. The image provides a visual representation of the process, supplementing the documentation and helping users navigate the interface with ease.
:::

<details>
<summary>📝 Extracted Text Content</summary>

```text
C2)TIR GO TO MYACCOUNT Explore GenAl API © a @ Private Workspace A 7:
Al PLATFORM
Private Workspace > default-project » Nodes » Create Node
i) Create Node FE DOCUMENTATION
ol ; .
rs) Image Details Image Details ©
2 TIR provides pre-built images including PyTorch and
Transformers, or users can alternatively deploy their
own custom images from the container registry. TIR provides pre-built images including PyTorch and Transformers, or users can alternatively deploy their own custom images from the container registry. Select the option that aligns
&] Select the option that aligns with your requirements. with your requirements.
TIR PRE-BUILT BASE OS CONTAINER REGISTRY
@) —_—
Select this if your image supports JupyterLab.
Ba e Node Resources O y g He #
TIR offers plans with CPU and GPU options. Select a Your image will support JupyterLab if you have used tir's image builder utlitlity. Check this list for JupyterLab support if you have used tir's prebuilt images as your base
fi plan that suits your needs. image.
q rs Node Storage Choose an existing registry or Click here to create a new one.
TIR provide specify the Notebook Type to suit their
> computational needs. Additionally, they can allocate Select Registry Vv
the desired Workspace Size (in GB) and select
datasets for seamless integration. For added
flexibility and security, an SSH option is available.
S © Node Detail
TIR provide specify the Notebook Type to suit their
computational needs. Additionally, they can allocate
the desired Workspace Size (in GB) and select
datasets for seamless integration. For added flexibility
and security, an SSH option is available.
NEXT
Legal © 2024 E2E Networks Limited ™ fini fi A) @ Contact Us
```

</details>


After selecting the machine, the Resource page will appear. At this stage, choose a plan based on either CPU or GPU requirements.

![Node Resource Selection](/img/image_10214282b7.png)

:::tip Screenshot Explanation
This image depicts a screenshot of a node resource selection interface, specifically within the "Private Workspace" section of a platform, likely a cloud computing or artificial intelligence (AI) environment. The interface appears to be part of a larger platform, E2E Networks Limited, and is labeled as "Create Node" with a subtitle "Node Resources."

The image shows various options for selecting and configuring node resources, including:

1. **Pre-built images**: The platform offers pre-built images, such as PyTorch and Transformers, which can be deployed directly.
2. **Custom images**: Users can also deploy their own custom images from a container registry.
3. **Resource filtering**: The interface allows users to filter resources based on CPU, RAM, and GPU requirements.
4. **Plan selection**: The platform offers different plans with varying levels of CPU, RAM, and GPU resources, along with corresponding prices.
5. **Workspace configuration**: Users can specify the notebook type, workspace size (in GB), and select datasets for integration.
6. **SSH option**: An SSH option is available for added flexibility and security.

The image highlights two specific plans: "A100_Free" and "GDC.1xH10080-26.250GB_SXM," with their respective resource allocations and prices. The interface also mentions hourly billing and committed machine plans, with a note that committed plans may not be available for certain machines.

In the context of the documentation, this image illustrates the process of selecting and configuring node resources within the platform. It provides a visual representation of the various options and configurations available to users, allowing them to tailor their selection to their specific requirements. The image is likely used to support the documentation's discussion of node resource selection and configuration, providing a clear and concise visual aid for users to understand the process.
:::

<details>
<summary>📝 Extracted Text Content</summary>

```text
C2)TIR GO TO MYACCOUNT Explore GenAl API © a @ Private Workspace A 7:
Al PLATFORM .
Private Workspace » default-project » Nodes » Create Node
E) Create Node Ey DOCUMENTATION
a :
@ Image Details Node Resources @
2 TIR provides pre-built images including PyTorch and
Transformers, or users can alternatively deploy their
own custom images from the container registry. GPU CPU
&] Select the option that aligns with your requirements.
© C2) Node Resources Filter by CPU Filter by RAM Filter by GPU Card
G TIR offers plans with CPU and GPU options. Select a All vCPU ~ All RAM ~ All ~ 6
)) plan that suits your needs.
Fr Plan Name RAM CPU GPU Price
ra v A100_Free 1GB 1 1 Free Tier Select
ra rs Node Storage
TIR provide specify the Notebook Type to suit their a GDC.1xH10080-26.250GB_SXM 250GB 26 1 %450/hr Selected
computational needs. Additionally, they can allocate
the desired Workspace Size (in GB) and select
datasets for seamless integration. For added Select PI
Q@ flexibility and security, an SSH option is available. rec Elo
E2E offers two plans for this configuration: hourly billing and committed machines. The hourly plan charges .
; peut me U7 Walling) Eure} C ns yp 9 Hourly Billed, €450/hr ¥
e Node Detail based on usage, while the committed plan saves costs by reserving the machine for specific days.
TIR provide specify the Notebook Type to suit their Committed plans aren't available for certain machines, opt for the hourly plan. Choose the plan that fits your
computational needs. Additionally, they can allocate needs. Learn more about committed plan.
the desired Workspace Size (in GB) and select
datasets for seamless integration. For added flexibility
and security, an SSH option is available.
Vv GDC.2xH10080-52.500GB_SXM 500GB 52 2 %816/hr Select
63 we ANAC Avuianenina AnaneR evn 4nanee 4nA A FAGAN hy Galant
BACK NEXT
Legal © 2024 E2E Networks Limited ™ fini fi A) @ Contact Us
```

</details>


Additionally, you can filter CPU and GPU resources based on your specific requirements for a more tailored selection.

![CPU Filter](/img/image_4bca0d5cc1.png)

:::tip Screenshot Explanation
This image appears to be a screenshot of a user interface for creating a node within a private workspace on the TIR (Tensor Instance Runtime) platform. The interface is divided into several sections, including "Node Resources," "Node Storage," and "Node Details."

In the "Node Resources" section, users can select from various pre-built images, including PyTorch and Transformers, or choose to deploy their own custom images from a container registry. They can also filter node options by CPU or RAM and select a plan that suits their needs, with options ranging from a free tier to paid plans with varying amounts of RAM and CPU.

The "Node Storage" section allows users to specify the notebook type, allocate workspace size (in GB), and select datasets for integration. Additionally, an SSH option is available for added flexibility and security.

The image is relevant to the documentation as it illustrates the process of creating a node within the TIR platform, including selecting node resources, configuring storage, and adding datasets. This step is crucial in setting up a computational environment, and the image provides a visual representation of the options and configurations available to users. The context of the image suggests that it is part of a larger tutorial or guide on using the TIR platform, likely in the section on creating nodes and configuring resources.
:::

<details>
<summary>📝 Extracted Text Content</summary>

```text
C2)TIR GO TO MYACCOUNT Explore GenAl API © a @ Private Workspace A 7:
Al PLATFORM
Private Workspace » default-project » Nodes » Create Node
i) Create Node FE DOCUMENTATION
a :
@ Image Details Node Resources ©)
2 TIR provides pre-built images including PyTorch and
Transformers, or users can alternatively deploy their
own custom images from the container registry.
&] Select the option that aligns with your requirements. GPU CPU
Cs @ Node Resources
Filter by CPU Filter by RAM
TIR offers plans with CPU and GPU options. Select a
@) plan that suits your needs. All vCPU v All RAM v (S
Fy Plan Name RAM CPU Price
ca v  C3.4_Free 1GB 1 Free Tier
ra rs Node Storage
TIR provide specify the Notebook Type to suit their v C3.4 1GB 1 z5/hr
computational needs. Additionally, they can allocate
the desired Workspace Size (in GB) and select
datasets for seamless integration. For added
Q@ flexibility and security, an SSH option is available. v C1.2GB 2GB 1 %20/hr
© Node Detail
Rows per page: Sy 1-3 of 3
TIR provide specify the Notebook Type to suit their
computational needs. Additionally, they can allocate
the desired Workspace Size (in GB) and select
datasets for seamless integration. For added flexibility
and security, an SSH option is available.
BACK NEXT
Legal © 2024 E2E Networks Limited ™ fini fi A) @ Contact Us
```

</details>


At this step, the user can also add the required dataset to the node being created.

![Node Storage](/img/image_e2ea7098b0.png)

:::tip Screenshot Explanation
This image appears to be a screenshot of a node creation interface, specifically the "Create Node" page within the "Private Workspace" section of a platform. The platform, referred to as TIR, provides users with options to customize and configure their node environment.

The image shows various sections and fields that require user input, including:

1. **Node Storage**: This section allows users to choose between pre-built images (e.g., PyTorch and Transformers) or deploy their custom images from a container registry.
2. **Node Resources**: Users can select a plan that suits their computational needs, with options for CPU and GPU.
3. **Datasets**: Users can choose from existing datasets to mount onto the node instance, with the option to create a new dataset if needed.
4. **Node Details**: This section enables users to specify their notebook type, allocate workspace size (in GB), select datasets for integration, and optionally enable SSH for added flexibility and security.

The image also includes navigation buttons ("BACK" and "NEXT") and a copyright notice at the bottom.

In the context of documentation, this image is likely used to illustrate the node creation process and provide a visual guide for users to follow when setting up their node environment. The image helps to clarify the various options and configurations available, making it easier for users to understand and complete the node creation process.
:::

<details>
<summary>📝 Extracted Text Content</summary>

```text
GDTIR  [cotowaccont) Eyes © & — @ Prvateworspace ~ =A
Al PLATFORM
Private Workspace » default-project » Nodes » Create Node
i) Create Node FE DOCUMENTATION
a :
@ Image Details Node Storage @
2 TIR provides pre-built images including PyTorch and
Transformers, or users can alternatively deploy their
own custom images from the container registry.
&] Select the option that aligns with your requirements.
e Datasets ~
Cs @ Node Resources
TIR offers plans with CPU and GPU options. Select a Make a selection of existing datasets to mount onto the node instance. Click here to create new one.
@) plan that suits your needs. The selected datasets will be mounted at /datasets in your node environment
ge © Node Storage -_
TIR provide specify the Notebook Type to suit their
iE] computational needs. Additionally, they can allocate
the desired Workspace Size (in GB) and select
ra datasets for seamless integration. For added
flexibility and security, an SSH option is available.
& Seer!
@ © Node Detail
TIR provide specify the Notebook Type to suit their
computational needs. Additionally, they can allocate
the desired Workspace Size (in GB) and select
datasets for seamless integration. For added flexibility
and security, an SSH option is available.
BACK NEXT
Legal © 2024 E2E Networks Limited ™ » Contact Us
```

</details>


The user is prompted to provide the essential details before the node is created.

![Node Details](/img/image_e7cbd65dab.png)

:::tip Screenshot Explanation
**Node Details Configuration Interface**

This image depicts a comprehensive configuration interface for setting up a node, specifically a workspace environment. The screenshot showcases the various options and settings available for customizing a node, including:

1. **Node Details**: Displays the node's name, resources, and storage information.
2. **Node Resources**: Allows users to select from various node types, including options with and without GPU support.
3. **Workspace Size**: Enables users to allocate storage space, with a default size of 20 GB and the option to increase up to 5000 GB. Additional storage beyond the default size incurs a monthly charge.
4. **Notebook Type**: Provides the option to import a new notebook or select from existing ones.
5. **Node Storage**: Offers the ability to allocate NVMe storage and integrate datasets.
6. **SSH Access**: Allows users to enable secure remote access via SSH.
7. **Start Scripts**: Enables users to select from a list of scripts or create a new one that will execute automatically when the node starts or restarts.
8. **Add-on Services**: Displays available add-ons, although the specifics are not visible in this screenshot.

The image is relevant to the documentation as it illustrates the final step in the node setup process, where users can review and configure their node's details before deployment. The Node Summary details displayed in this interface will be available in the node environment after completion. This screenshot provides a clear visual representation of the various configuration options and settings, making it easier for users to understand and navigate the node setup process.
:::

<details>
<summary>📝 Extracted Text Content</summary>

```text
GTR © | @ Prateworepace ~ A
Boeriivae Workspace » new002 » Nodes » Create Node
@ image details Node Detail
| a Siar wth TI's pre-but mages oF deploy your own
trom he regs to you neds
Q Node Namo
@ Node Resources node-122712382828,
a ‘IR provies plans with noth GPU and GPU options
Notebook Type :©  @ NewNotebook © import Notebook
@ Node storage
@ Select notevook Type, allocate NVMe storage, and
iterate datasets to meet computational needs ‘This wil be avaliable at momesjovyan in your node environment
Ed 88
© Node Detail
00 1000 1500 2000 2500 000 500 4000 4500 5000
® TI enabias users to customize Notebook Type, Workspace Size
Workspace Siz, ane dataset intagraton, wth secure (68):
é, remote access via SSH. AX Please note that the workspace size cannot be reduced in the future but it can be increased upto 5000 GB
o By default, your node comes wth 20 GB ot tre workspace size, Over this space, each additional GB willbe charged at tS per month
This wil be avaliable at momesjovyan in your node envirnment
Enable SSH BD
fat Start Scripts
“This wll ad sept that wil execute automaticly when the node stats or restarts. Select from the is of scripts Below or Create a new Sevpt
Select one or more scrpt(s) .
Add-on Services
Add-ons -
it)
Legal © 2024 EE Networks Limited ™ Biya @ Contact Us
```

</details>


After all steps are completed, the Node Summary details will be displayed.

![Node Summary](/img/image_0f3e4b6858.png)

:::tip Screenshot Explanation
**Image Description: Node Creation Summary in TIR Platform**

This image captures a screenshot of the Node Creation Summary page within the TIR (TensorFlow Inference Runtime) platform. The page displays the details of a newly created node, including its configuration, resources, and settings. The node is named "node-09301628022" and is equipped with a pre-built Transformers image (version v4.39.3) on a CPU-based plan with 1 GB of RAM, billed at an hourly rate of ¢5/hr.

The page provides an overview of the node's resources, including the allocation of 30 GB of disk space and the enablement of JupyterLab. Additionally, users can edit the node's configuration, resources, and details, and have the option to specify the Notebook Type, Workspace Size, and select datasets for seamless integration. An SSH option is also available for added flexibility and security.

**Relevance to Documentation:**

This image is relevant to the documentation as it illustrates the Node Creation Summary page, which is displayed after clicking the 'Create' button. The page provides users with a comprehensive overview of their newly created node, allowing them to review and edit its configuration, resources, and settings. This image can be used to support documentation on creating and managing nodes within the TIR platform, providing visual context for users to understand the node creation process and its associated settings.
:::

<details>
<summary>📝 Extracted Text Content</summary>

```text
C2)TIR GO TO MYACCOUNT Explore GenAl API © a @ Private Workspace A 7:
Al PLATFORM
Private Workspace » default-project » Nodes » Create Node
i) Create Node FE DOCUMENTATION
ol ; .
g Image Details Summary Preview
2 TIR provides pre-built images including PyTorch and
Transformers, or users can alternatively deploy their .
own custom images from the container registry. Image Details Z@ EDIT
&) Select the option that aligns with your requirements. —eeeeeeeeeeeeeeeeeee
© .
ry @ Node Resources Image Type : pre-built
Q) TIR offers plans with CPU and GPU options. Select a Image : Transformers
@ plan that suits your needs.
Image Version: v4.39.3
ge g Node Storage
TIR provide specify the Notebook Type to suit their JupyterLab Enabled : True
Gi computational needs. Additionally, they can allocate
the desired Workspace Size (in GB) and select
ra datasets for seamless integration. For added Resource Details Zz EDIT
flexibility and security, an SSH option is available. a
iv) Node Detail Plan Configuration : 1CPU, 1GB RAM
TIR provide specify the Notebook Type to suit their .
computational needs. Additionally, they can allocate Plan : Hourly Billed, ¢5/hr
the desired Workspace Size (in GB) and select
@ datasets for seamless integration. For added flexibility
A .
and security, an SSH option is available. Node Details Z@ EDIT
Node Name : node-09301628022
Notebook Typ : New Notebook
Disk Size : 30
BACK LAUNCH
Legal © 2024 E2E Networks Limited ™ fini fi A) @ Contact Us
```

</details>


After clicking on the 'Create' button, the page will redirect to the 'Manage Nodes' page and display all details there.

![Manage Nodes](/img/image_72b7f0cb9a.png)

:::tip Screenshot Explanation
This image appears to be a screenshot of a Private Workspace dashboard, specifically the "Manage Nodes" section. The dashboard is displaying information about a node named "node-042517544848" that is utilizing the PyTorch image with a plan type of "Hourly".

The image reveals various details about the node, including:

1. Node Name and Image: The node is identified as "node-042517544848" and is running the PyTorch image.
2. Status: The node's status is displayed as "Running".
3. Plan Details: The plan type is "Hourly", indicating that the node is being billed on an hourly basis.
4. Connection Details: Although not fully visible, the image suggests that connection details, such as SSH access, are available.
5. Overview Tab: The image shows that the "Overview" tab is currently selected, which provides a summary of the node's details, including associated datasets and metrics.

The relevance of this image to the documentation is to provide a visual representation of the "Manage Nodes" section within the Private Workspace dashboard. It highlights the key information that users can expect to see when managing their nodes, including node details, plan details, and connection information. This image can be used to support documentation that guides users through the process of managing nodes, configuring SSH access, and monitoring node performance.
:::

<details>
<summary>📝 Extracted Text Content</summary>

```text
CESTIR [coro wvaccounr } © & DB — & Private Workspace ~ P
Private Workspace » pri-019011213434 » Nodes
33 Manage Nodes © |B coouewranon | RES
Node Name Image Plan Name Plan Type Updated On Status Lab URL, ‘SSH Access. ‘Actions
a node-042517544848 PyTorch 3.868 Hourly 26 April, 2024 10:24 am @ Bunning SF pyter A Disabled i
& Rowsperpage: S ~ ttf
Pa Overview Events Disk Size Metrics_-—=—Associated Datasets Configure SSH
gS Node Details [o)
Node Name: nc ,
Node Image: PyTorch Cy ryrh
Status @ Running
Created By: °
Created At
a Plan Details fo}
Connection Details fo}
Legal © 2024 E2E Networks Limited ™ Baya @ Contact Us
```

</details>


### Node Detailsâ

#### Overviewâ

You can see the Node Details and Plan Details under the Overview tab.

![Node Overview](/img/image_ef39efa579.png)

:::tip Screenshot Explanation
The provided image appears to be a screenshot of a node management interface, specifically a "Node Overview" page. The image displays various details about a particular node, identified as "node-o1071446022", within a larger system or network.

The node details include:

1. **Node Name**: node-o1071446022
2. **Node Image**: Transformers (version 3)
3. **Image Version**: v4.45.2
4. **JupyterLab Status**: Installed and Running
5. **Creation and Update Information**: Created and last updated on January 7, 2025, at 02:49 pm

The image also shows a graphical representation of the node's performance, with three monitoring graphs:

1. **CPU Utilization**
2. **Memory Utilization**
3. **Interval** ( likely referring to a time-based metric)

These graphs provide a visual representation of the node's resource usage and performance over time.

In the context of documentation, this image is likely used to illustrate the node management interface and provide a clear understanding of the information available for each node within the system. The image helps to support the documentation by providing a visual representation of the node details and performance metrics, making it easier for users to understand and navigate the system.
:::

<details>
<summary>📝 Extracted Text Content</summary>

```text
CB recm-120517075252 + prit2t7iiostttt » Nodes
Manage Nodes @ Search nove 3) (@ | By oocumentarion
|B toanane image Pian Name Pian Type Created At 7S staus tab URL 6H Access Aetons
e = :
odeo107 448022 ace Gc. 11008026 2008. sx Hout 07 danuary, 2025 0249 pm © Funring 2a ‘A.Diabied i
of owsperpage: Sv ttelt <>
- [[eveien ] rset Monitoring Workspace Size Associated Datasets Associated FlesSyster?® Network & Securty
& Node Details fo)
a Node Name node-o1071446022
Node Image: Transformers (3)
Lo) Image Version: v4.45.2
fay JupyterLab: @ Installed
Status @ Running
Created By
Updated at 07 January, 2025 02:49 pm
Bo bn
@ Plan Details fo)
```

</details>


#### Node Eventsâ

![Node Events](/img/image_020d5d93d4.png)

:::tip Screenshot Explanation
This image appears to be a distorted or low-quality screenshot of a system monitoring graph. The text extracted from the image using OCR (Optical Character Recognition) is largely illegible and contains numerous errors.

However, based on the original alt text "Node Events" and the context provided, it is likely that the image is intended to display a graph showing CPU utilization, memory utilization, and interval metrics for a node or system.

A clearer image would likely show a graphical representation of these metrics, with lines or charts plotting the values over time. The graph would provide a visual representation of system performance, allowing users to quickly identify trends, spikes, or anomalies in CPU and memory usage.

In the context of documentation, this image is likely intended to illustrate system monitoring capabilities, possibly in a section discussing node performance, event tracking, or system analytics. A higher-quality image would be necessary to effectively convey this information and provide a clear understanding of the system's performance metrics.
:::

<details>
<summary>📝 Extracted Text Content</summary>

```text
Gee mom a ©
Beeesscsrrrsen - pprerrri + Nader
\> = = SSC
DO eestaritae Taner 0 yeas ct vat eam, U8 4p eben, foto’ acess
° =
a ompenme ila >
rR)
© | nent 0
oe so we s
a ey ——— et ee
Sunn ns a
|| [am vn oo
ba errr cy eam
bl Rae reer —— oo
```

</details>


#### Monitoringâ

You can see the monitor graph in CPU Utilization, Memory Utilization & Interval.

![Metrics Graph](/img/image_fbd064293c.png)

:::tip Screenshot Explanation
The provided image is a screenshot of a project dashboard, displaying key metrics and analytics. The dashboard appears to be from a platform that supports data science and machine learning projects, given the presence of PyTorch and model endpoints.

The top section of the image shows navigation options, including "STIR," "GOTO MYACCOUNT," and "Private Workspace." Below this, the dashboard displays information about a specific project, including the project name "tir-notebook-43" and the framework used, PyTorch.

The main section of the image is divided into several panels, each providing different insights into the project's activity and performance. The panels include:

*   Model Endpoints: This section displays a list of model endpoints, but the actual list is not visible in the provided image.
*   API Tokens Overview: This panel provides an overview of API tokens, including disk size and associated datasets.
*   Analytics: This section displays analytics data, including CPU utilization and memory utilization over time. The data is shown in a graphical format, with a line chart displaying the utilization over a period of time.
*   Disk Size: This panel shows the disk size associated with the project.
*   Associated Datasets: This section displays the datasets associated with the project.

The bottom section of the image displays a graph with CPU and memory utilization metrics over time. The graph shows the utilization over a period of one month, with the most recent data points at the right-hand side of the graph. The graph is annotated with timestamps, indicating the time at which each data point was recorded.

Overall, this image provides a snapshot of a project's activity and performance, including key metrics such as CPU and memory utilization. The dashboard appears to be designed to provide a quick overview of the project's status, allowing users to monitor and manage their projects more effectively.
:::

<details>
<summary>📝 Extracted Text Content</summary>

```text
= (STIR | GOTO MYACCOUNT | G B= & Private Workspace ~ N
Al PLATFORM OO ~
E g Datasets tir-notebook-43 PyTorch 2 C3.4 21 July, 2023 12:31 pm 21 July, 2023 12:31 pm @ Running eee
Q Models Rows perpage: 57 1-1 of 1
@) Model Endpoints
S) API Tokens Overview Disk Size Associated Datasets
. Interval
il, Analytics |
' y Last 5 minutes ~ Gq
8% Settings
HE CPU Utilization HEE Memory Utilization
1.08 % 237.18 MB
DELETE PROJECT 1.04 % 237.14 MB
1.00 % 237.10 MB
0.96 % 237.06 MB
SFT FT FP FP HF PF FV PF PF OY SPP HP FP FP FP FP FP PW
sf S SS SS SES SS SS SSS SS SS SS
PP PP PS MW Ww Ww Ww wo ow PP DP PP NY PY ow Ww ew
Vv Vv vv vv vy Vv Vv vv vv vy
```

</details>


You can see the one-month activity as per your requirement in days & hours.

![One Month Activity](/img/image_5166ffebde.png)

:::tip Screenshot Explanation
**Image Description: Node Overview and Resource Utilization**

The provided image appears to be a screenshot of a node management dashboard, displaying detailed information about a specific node's configuration, resource utilization, and associated datasets. The image is divided into several sections, each providing insight into different aspects of the node's performance and settings.

**Key Components:**

1. **Node Information**: The top section displays the node's name ("odeo107"), ID ("448022"), and type ("ace Gc. 11008026"). It also shows the creation date and time ("January 7, 2025, 02:49 pm") and the node's status ("Funring 2a ‘A.Diabied i").
2. **Overview**: This section provides a summary of the node's workspace, including its size, associated datasets, and file system. It also displays the node's network and security settings.
3. **Resource Utilization**: The image shows the node's resource usage over different time periods, including:
	* **Workspace Usage**: The percentage of used and available workspace size.
	* **Local Storage Usage**: The percentage of used and available local storage.
	* **Memory Usage**: The percentage of used and available memory.
	* **GPU Utilization**: The percentage of time during which one or more kernels were executing on the GPU, displayed for the last hour, 24 hours, and 7 days.
4. **Actions**: The image suggests that users can modify the node's disk size according to their requirements.

**Relevance to Documentation**:
This image is likely part of a larger documentation set, possibly a user guide or tutorial, that explains how to manage and configure nodes in a specific environment. The image provides a visual representation of the node management dashboard, helping users understand the various components and settings available to them. The context provided indicates that the image is intended to illustrate how to view and modify disk size settings, making it a relevant and useful addition to the documentation.
:::

<details>
<summary>📝 Extracted Text Content</summary>

```text
, °
CB recm-120517075252 » prit2r7io8tttt » Nodes
Manage Nodes @ Soaron nove 3) (@ | By oocumentarion
|B toanane image Pian Name Pian Type Created At 7S staus tab URL 8H Access Aetons
e = :
odeo107 448022 ace Gc. 11008026 2008. sx Hout 07 danuary, 2025 0249 pm © Funring 2a ‘A.Diabied i
a orp
fe Overview Node vent Werkspace Size Associated Datasets Associated File-Systen® Network & Secutly
Workspace Usage Local Storage Usage Memory Usage
4 HMI Used Workspace size Available Workspace size HE Used Local Storage Available Local Storage HEE Used Memory Available Memory
ras)
® Last hour
GPU Utilization GPU Menic
it) Last 24 hours
“This represents the percentage of time during which one or more kernels were executing on the GPU “This represents the percentage of time during whictll len to
@ ae pe tact 7 days
1.00% 4.00 me est monn
Legal © 2025 E2E Networks Limited ™ Baya 1 Contact Us
```

</details>


#### Workspace Sizeâ

You can see the details disk size and also You can change the Disk size as per your requirements.

![Disk Size](/img/image_1fc4809368.png)

:::tip Screenshot Explanation
This image appears to be a screenshot of a disk size update interface, likely from a virtual machine or disk management software. The image is not of high quality, and the text is partially distorted, making it difficult to read. However, based on the OCR text and original alt text, it can be inferred that the image is showing a field or input box where the user can enter a new disk size.

The image seems to be relevant to a documentation or instructional guide that explains the process of updating the disk size. The context provided suggests that the user needs to modify the disk size value and then click an "update" button to apply the changes. The image is likely intended to illustrate this step in the process, providing a visual reference for the user to follow along with the instructions.

Overall, the image is a functional screenshot intended to support the documentation, rather than a decorative or illustrative image.
:::

<details>
<summary>📝 Extracted Text Content</summary>

```text
PEE Same) acm gt TTI
Brserrsse «terri «Ne
caren wo © eee
i = = = =o = So ss os 5
© secon enter 206 eneee nos wer fr amony escea ene mone Aone i
a fompeome 8+ at
© | santana tn stint tate a
Se [S o
F  oneunnn intent eee me ot =
```

</details>


For updating the disk size you have to change the disk size and then click on update button.

![Update Disk Size](/img/image_c8345f3998.png)

:::tip Screenshot Explanation
This image appears to be a screenshot of a system management or configuration interface, specifically showing a section related to disk management. The text "Update Disk Size" is visible, suggesting that the image is highlighting an option or feature to modify or update the size of a disk.

The surrounding text and elements, although partially distorted due to OCR errors, seem to be related to disk management and storage. The mention of "Mounted" and "Unmounted" datasets, as well as the option to "Unmount", further supports this interpretation.

In the context of the documentation, this image is likely used to illustrate the process of managing disk storage, specifically updating disk sizes, and navigating associated datasets. The image may be used to support instructions or explanations for system administrators or users who need to perform disk management tasks.
:::

<details>
<summary>📝 Extracted Text Content</summary>

```text
FU (oem) ED Sd
Bee srrorsese «perro «nee
© tome oo eo ED
om 5 = ve es wet
ever coenenen 00e verre 29098 wer fr amony escea ene Smee Aone i
é fompeome 8+ at
© | antennae tn minted tate _
es, Es)
fo | OMerniseceete nats nne Lote no =
```

</details>


#### Associated Datasetsâ

You can also see the Associated Datasets with two different datasets- Mounted & Unmounted. You can also Unmount.

![Associated Datasets](/img/image_d325454622.png)

:::tip Screenshot Explanation
The provided image appears to be a screenshot of a Node Overview page within a cloud or data management platform. The screenshot displays various sections and tabs related to node configuration and monitoring.

The main sections visible in the image include:

1. **Node Details**: This section shows information about the node, such as its name, type, creation date, and last update time.
2. **Overview**: This tab provides a high-level view of the node's status, including its monitoring workspace size and associated datasets.
3. **Associated Datasets**: This section is currently empty, indicating that no datasets are available or linked to the node.
4. **Network & Security**: This tab allows users to configure security settings, including SSH keys, as mentioned in the context.

The image seems to be part of a larger documentation set, likely related to node management, monitoring, and security configuration within a cloud or data management platform. The screenshot is intended to illustrate the layout and organization of the Node Overview page, providing visual context for users to understand how to navigate and configure their nodes.

The relevance of this image to the documentation is to provide a visual aid for users to understand the layout and organization of the Node Overview page, specifically highlighting the location of the Network & Security tab where SSH keys can be configured.
:::

<details>
<summary>📝 Extracted Text Content</summary>

```text
© manage Nodes @ Search nove =) @ |B vocumentarion
og ‘Node Mame cx Pan Name Pian Type crated at suas Lap un an Acces conn
TM) | reecterssone — CEST cry CEI orm = pyr AE :
fowsperpage: 8 ttl <>
fry
@ Overview Node Events Monitoring Workspace Size | Associated Datasets | Associated File-Systen® Network & Security
B (o)
reer ene storage Type Encryption Encryption Type state
a No dataset avaialable
eran
it) + (Rae
```

</details>


#### Associated File Systemâ

![Associated File System](/img/image_0b234ce27b.png)

:::tip Screenshot Explanation
The image appears to be a screenshot of a configuration settings page, specifically related to network and security options. The text extracted from the image using OCR (Optical Character Recognition) is somewhat distorted, but it suggests that the image is showing a section where users can manage nodes and configure SSH keys.

The original alt text "Associated File System" does not seem directly related to the content of the image. However, the context provided indicates that the image is relevant to configuring SSH keys under the Network and Security tab.

A clearer description of the image could be:

"This image shows a configuration settings page, specifically the Network and Security tab, where users can configure SSH keys. The screenshot displays various options and fields related to node management and SSH key configuration."

This description provides a more accurate representation of the image's content and its relevance to the documentation.
:::

<details>
<summary>📝 Extracted Text Content</summary>

```text
GREY (emer) on 0 a ©
Bee srrorsese «perro «nee
© Manage nodes a Peon Sy
a = ~ a pee eat
ever eter 00e verre 29098 toot eae sen om) ene Sve “a Oot 1
é femmes 55 tat
+ | orm maser Minny wont ae seas one [acanersynt J on se
0 | enregen onset rt thee me nae ee rn eee
‘|e — a 7 no
—_—_—_—_—_—_—_—_—_—_—_—_—_——
```

</details>


#### Network & securityâ

You can configure ssh key under Network and security tab.

![Launch Node](/img/image_91b1985b46.png)

:::tip Screenshot Explanation
The provided image appears to be a screenshot of a node management interface, likely from a cloud computing or virtual machine platform. The image displays a table with several columns, including "Node Name," "Image Plan Name," "Plan Type," "Created At," and "Status." The table lists a single node, "node-040915365151," which is running a PyTorch image plan.

The interface also features various buttons and links, including "Manage Nodes," "Search node," and "Configure SSH." The "Configure SSH" section allows users to enable SSH access to the node, either by uploading an existing SSH key or creating a new one. Additionally, the interface displays a notification informing the user that they will receive an email when the IP address is assigned to the node and SSH is activated.

The image seems to be relevant to documentation related to node management, SSH configuration, and virtual machine setup. It may be used to illustrate the process of launching and managing nodes, configuring SSH access, and monitoring node activity. The context provided suggests that the image is part of a larger guide or tutorial that explains how to use the platform's features, including searching for nodes and configuring SSH access.
:::

<details>
<summary>📝 Extracted Text Content</summary>

```text
CB eeam-osoo11365059 + detaut-poject » Nodes
a oo
Manage Nodes @ Search node =) © [|B oocumenrarion |
a Node Name Image Plan Name Plan Type Created At 4 Status Lab URL SSH Access Actions
@ =
node-040915365151 PyTorch ca.8cB wemty (09 April, 2025 03:37 pm O emir = jupyter o :
8 Rows perpage: 5 ~  1-tolt <>
w Tn
ie Overview Node Events Monitoring Workspace Size Associated Datasets Associated File-System | Network & Security Images
Configure SSH (o)
@ _Youwill also receive an email when IP address is assigned to this node and SSH is activated.
iQ Enable SSH Access @I@®
aS Choose a pre-existing SSH key for seamless access by uploading the key fl. Click here to create new one.
Bearch label x +
Label SSH Key ‘Action
e2e fo)
{ewes =
B EEE
Legal © 2025 E2E Networks Limited ™ BAXA @ Contact Us
```

</details>


You can Attach/Detach the Reserve IP under Network and security tab.

![Launch Node](/img/image_ed4177e7c5.png)

:::tip Screenshot Explanation
This image appears to be a screenshot of a node management interface, specifically the "Nodes" page within a project titled "default-project." The page displays a table listing various details about a node, including its name ("node-040915365151"), image plan ("PyTorch c3.8cB"), plan type ("Hourly"), creation date and time ("09 April, 2025 03:37 pm"), and status ("Running").

The table also provides links to additional information, such as the node's Lab URL and SSH access details. Furthermore, the page offers various actions that can be taken on the node, including configuration options for SSH, IP reservation, and application ports.

The image also shows several tabs at the top, including "Overview," "Node Events," "Monitoring," "Workspace Size," "Associated Datasets," "Associated File-System," "Images," and "Network & Security." This suggests that the node management interface provides a comprehensive set of tools for managing and monitoring nodes.

In the context of documentation, this image is likely relevant to a section on node management or deployment, and may be used to illustrate the process of launching or configuring a node. The image may also be used to support instructions on how to access a node's details, configure SSH access, or expose application ports.
:::

<details>
<summary>📝 Extracted Text Content</summary>

```text
default-project » Nodes
[3 Manage Nodes @ Search node =) © [|B oocumenrarion |
Node Name Image Plan Name Plan Type Created At 4 Status Lab URL, SSH Access Actions
Q node-040915365151 PyTorch c3.8cB Hourly (09 April, 2025 03:37 pm @ Running SF supyter o A
Rows perpage: 5 + ttoft <>
w —§<—<——$<—
# Overview Node Events Monitoring Workspace Size Associated Datasets Associated File-System [Network & Security] Images
Z Configure SSH fo)
Reserve IP (o)
Attach ReservelP  I@®
g Choose a pre-existing Reserve IP. Click here to create new one
Application Ports (o)
B You have not exposed any ports
Legal © 2025 E2E Networks Limited ™ BAXA @ Contact Us
```

</details>


You can Add Port under Network and security tab.

![Launch Node](/img/image_9a73cadd26.png)

:::tip Screenshot Explanation
This image appears to be a screenshot of a cloud computing or node management platform, specifically a node details page. The page displays various information and configuration options for a node identified as "node-040915365151" running PyTorch on a c3.8 instance.

The page is divided into several sections, including:

1. Overview: Providing a brief summary of the node, including its name, instance type, and running status.
2. Node Events: Likely a log or history of events related to the node, such as startup, shutdown, or errors.
3. Monitoring: Possibly displaying real-time monitoring data, such as resource utilization or performance metrics.
4. Workspace Size: Showing the allocated storage space for the node.
5. Associated Datasets and File-System: Listing the datasets and file systems connected to or accessible by the node.
6. Network & Security: Providing options for configuring network and security settings, such as SSH access and IP reservation.

The page also includes various action buttons and links, including:

* Launch Node
* Configure SSH
* Reserve IP
* Application Ports
* Start Scripts

The image is relevant to documentation that focuses on node management, cloud computing, or deep learning using PyTorch. It may be used to illustrate the process of setting up and configuring a node, or to provide a visual reference for users navigating the platform.
:::

<details>
<summary>📝 Extracted Text Content</summary>

```text
» —
8 manage Nodes @ Search node 2) @ [Booneno | OES
=} node-040915365151 PyTorch c3.8cB Hourly (09 April, 2025 03:37 pm @ Running SF supyter o A
@ Overview Node Events Monitoring Workspace Size Associated Datasets Associated File-System [Network & Security| Images
B Configure SSH fo)
4 Reserve IP fo)
a Nn ns
Application Ports (o)
Q a
[ay
oP ~| fa =] 0
_msser Ler]
i) Start Scripts (o)
ee —_ .
Legal © 2025 E2E Networks Limited ™ BAXA @ Contact Us
```

</details>


#### Start scriptâ

In this section, users can select the desired script to attach to the Node. The attached script enables seamless execution on the Node, ensuring that all necessary dependencies are installed and configured for optimal performance.

![Node Details](/img/image_83b301631d.png)

:::tip Screenshot Explanation
This image displays a screenshot of a node details page, specifically "node-040915965151," within a project management platform. The page provides an overview of the node's configuration, including its name, image, plan name, plan type, creation date, status, and lab URL. 

The top section of the page presents a table with the node's details, while the bottom section offers various options for node management, such as configuring SSH access, reserving an IP, setting application ports, and adding start scripts. A "Click here to create a new script" button allows users to generate a new script, which can be added to the node.

This image is relevant to the documentation as it illustrates the node details page and its various components, providing a visual reference for users navigating the platform. It also highlights the option to create a new script, which is an essential feature for customizing node configurations. The image can be used to support documentation on node management, script creation, and platform navigation.
:::

<details>
<summary>📝 Extracted Text Content</summary>

```text
_ ————__ °
> default-project » Nodes
a eo
Manage Nodes @ Search node =) @ [|B vocumenrarion |
a Node Name Image Plan Name Plan Type Created At 4 Status Lab URL SSH Access Actions
a _
node-040915965151 PyTorch ca.ece Hourly 09 April, 2025 09:97 pm © Running  pyter o i
8 Rows perpage: 5 ~  1-tolt <>
w Tn
ie Overview Node Events Monitoring Workspace Size Associated Datasets Associated File-System _| Network & Security Images
4 Configure SSH fo}
Reserve IP fo)
@ Application Ports fo)
a Start Scripts (o}
| Ei vocumentarion |
Select scripts to add from the list below or Click here to create a new script
node-seripto4o9160188s5 € [Search script name x
[caves IL rome]
ite)
Legal © 2025 E2E Networks Limited ™ BAXA @ Contact Us
```

</details>


Users can create a new script by clicking on the Click Here button.

![Node Details](/img/image_cb6c041c87.png)

:::tip Screenshot Explanation
This image, titled "Node Details," appears to be a screenshot of a web-based interface displaying information about a specific node, likely in a cloud computing or virtual machine environment. The node in question, named "node-040915965151," is running PyTorch and has a plan type of "ca.scs" with a hourly billing cycle.

The image shows various details about the node, including:

1. Node Name and Image Plan Name
2. Plan Type and Creation Date (April 9, 2025, at 09:57 pm)
3. Status (Running)
4. Lab URL and SSH Access information
5. Actions available for the node, such as configuring SSH, reserving an IP, and managing application ports

The image also features navigation links to other sections, including:

1. Overview
2. Node Events
3. Monitoring
4. Workspace Size
5. Associated Datasets
6. Associated File-System Images

Additionally, there is a section for Start Scripts, which currently indicates that no scripts are attached, with the option to attach a new script.

In the context of documentation, this image is likely used to illustrate the node management interface, highlighting the various features and options available to users for managing and configuring their nodes. It may be used to support tutorials, guides, or reference materials for users working with this platform.
:::

<details>
<summary>📝 Extracted Text Content</summary>

```text
+ defaul-project » Nodes
oo ——
Manage Nodes Q Search node 3) @ | Bi cocumentation Ip crearenove ]
a Node Name Image Plan Name Plan Type Created At 4 Status Lab URL SSH Access Actions
a =
node-040915965151 PyToreh ca.scs Hourly (09 Apri, 2025 09:97 pm @ Running  jupyter o i
a >
fer] Rows perpage: 5 > t-toft <>
¢] ee
ie Overview Node Events Monitoring Workspace Size Associated Datasets Associated File-System Images
4 Configure SSH fo}
Reserve IP fo)
@ Application Ports fo)
a Start Scripts (o}
{i vocumentarion |
No scripts attached. attach a new script
ite)
Legal © 2025 E2E Networks Limited ™ BaXaA @ Contact Us
```

</details>


Users have the flexibility to either upload a script file directly from their local machine or manually write/copy the script code within the interface. Before saving and utilizing the script, users are required to provide a name for the script file.

![Node Details](/img/image_1206067f53.png)

:::tip Screenshot Explanation
This image, titled "Node Details," displays a list view of available scripts within a project, specifically showing the "Start Scripts" section. The screenshot highlights a particular script, "node-script-040916102626," and provides an "Enter Script" option. The image illustrates a key functionality of the system, which allows users to select, update, or delete scripts as needed. The purpose of this image is to support documentation by visually demonstrating the script management feature, enabling users to effectively navigate and manage their project's scripts.
:::

<details>
<summary>📝 Extracted Text Content</summary>

```text
Start Scripts
node-script-040916102626
Enter Script
```

</details>


Users can select a script from the list of available scripts across the project. Additionally, users have the ability to update an existing script or delete any script as needed.

Any changes made to the script will only take effect once the Node, to which the script is attached, is restarted.

Users can only delete a script if it is not currently attached to any Node.

![Node Details](/img/image_b646881ad8.png)

:::tip Screenshot Explanation
This image is a screenshot of a "Node Details" page within a Private Workspace, displaying various configuration options and information related to a specific node. The node, identified as "node-script-121918111515" and "node-script-121817573636", appears to be part of a larger network or system.

The screenshot shows several key features and functionalities, including:

1. **Node Overview**: A summary of the node's details, including its name and associated datasets.
2. **Node Events**: A log of events related to the node, such as script additions or removals.
3. **Monitoring**: Options for monitoring the node's performance and activity.
4. **Workspace Size**: Information about the node's storage capacity and usage.
5. **Network & Security**: Configuration options for the node's network and security settings.
6. **SSH Access**: A section for enabling and configuring Secure Shell (SSH) access to the node, including a notification that an email will be sent when IP address is assigned and SSH is activated.

The image is relevant to the documentation as it illustrates the confirmation dialog box that appears when a script is added to or removed from the Node. The dialog box is not visible in this screenshot, but the context suggests that it would appear in response to user actions on this page, such as adding or removing a script. The image provides a clear visual representation of the node's configuration options and settings, which can help users understand the context and functionality of the confirmation dialog box.
:::

<details>
<summary>📝 Extracted Text Content</summary>

```text
CEYTIR _{cotomvaccount | © & — @ Private Workspace ~ A
Rows perpage: 5 > 1-50f6 >
fi} Oe
Overview Node Events Monitoring Workspace Size Associated Datasets Network & Security
o Configure SSH [O}
- @ _Youwill also receive an email when IP address is assigned to this node and SSH is activated.
Enable SSH Access
@ {cance |
edi ooo —
oa =
node-script-121918111515 ooo
a lanchainuni oo io)
senddataoo7 oo
e node-script-121817573636 @ oa
3} 7
newqutes oo o}
new! ooo
ry 47 ot
newm-jncike ooo
B foancer | (Tareas
Legal © 2024 E2E Networks Limited ™ Biv”? @ Contact Us
```

</details>


When a script is added to or removed from the Node, a confirmation dialog box appears to verify the action.

![Node Details](/img/image_e4987d4b97.png)

:::tip Screenshot Explanation
This image appears to be a screenshot of a node management interface, specifically the "Node Details" section. The screenshot displays a confirmation prompt titled "Confirm Attached Scripts." The prompt informs the user that selecting scripts will attach them to the node, but they will only be executed after the node is restarted.

In the context of the surrounding actions, which include "Launch Notebook," "Stop Node," "Restart Node," "Update Image," "Update Plan," and "Delete," this image is likely relevant to a documentation section that explains how to manage and configure nodes within a larger system or platform. The image may be used to illustrate the process of attaching scripts to a node and the associated considerations, such as the need for a restart to enable script execution.

Overall, this image provides a visual representation of a key node management feature and can help users understand the workflow and dependencies involved in attaching and running scripts on a node.
:::

<details>
<summary>📝 Extracted Text Content</summary>

```text
Confirm Attached Scripts
Selected scripts will be attached to the node, but scripts will run only after the Node is
restarted.
```

</details>


### Node Actionsâ

You can see the actions like Launch Notebook, Stop Node,Restart Node,Update Image,Update Plan, Delete.

![Node Actions](/img/image_6ac894b5bb.png)

:::tip Screenshot Explanation
This image appears to be a screenshot of a node management interface, specifically the "Manage Nodes" section. The screenshot displays a table with several columns, including "Node Name", "Image", "Plan Name", "Plan Type", "Created At", "Status", "Lab URL", and "SSH Access". The table lists a single node, "node-011515361313", which was created on January 16, 2025, at 03:57 pm.

Below the node information, a series of action buttons are visible, including "Launch Notebook", "Stop Node", "Restart Node", "Update Plan", and "Delete". The "Launch Notebook" button is highlighted, indicating that it has been clicked, and a tooltip or confirmation message "Node will be launched and it should be visible like this" is displayed.

This image is likely part of a documentation or tutorial that guides users through the process of managing nodes in a cloud or virtual environment. The screenshot provides visual context for the steps involved in launching a node and accessing its associated actions and settings. The image helps to illustrate the user interface and workflow, making it easier for users to follow along and understand the documentation.
:::

<details>
<summary>📝 Extracted Text Content</summary>

```text
Manage Nodes Q Search node 3) © B oocumentarion
8 Node Name Image Plan Name Plan Type. Created At 4 Status ‘Lab URL ‘SSH Access Actions
BH _ noseortstes61s18 TER cs.ac8 Hourly 16 Janvary, 2025 03:57 pm © Punning = supyrer ‘A Disabied :
° @Z_ Launch Notebook
cs ows per pag >
a © stop Node
b ——— «Restart Node
1 Update Plan
4 B Delete
a Node Name: node-011515361313
ras)
& Created By:
Plan Netaile oO
```

</details>


#### Launch Notebookâ

After clicking on Launch Node, Node will be launched and it should be visible like this.

![Node Launched 1](/img/image_8b55bf2922.png)

:::tip Screenshot Explanation
This image appears to be a screenshot of a node management dashboard, specifically a page for managing and monitoring a node named "node-011515361313" within a project titled "prj 121711041111". The node is utilizing the TensorFlow pi image, version v2.15.0, and has JupyterLab installed.

The dashboard provides various details about the node, including its status (currently "Running"), creation date, and last updated date. It also offers several actions that can be performed on the node, such as launching a notebook, stopping the node, restarting the node, and updating the image or plan.

The image seems to be part of a larger documentation set, likely related to managing and using nodes within a project or workspace. The context provided suggests that the image is being used to illustrate the process of stopping a notebook, specifically highlighting the need to click the "Stop" button to halt the node.

Overall, this image serves as a visual aid for users to understand how to manage and interact with nodes within the platform, and provides a clear representation of the node management dashboard and its various features.
:::

<details>
<summary>📝 Extracted Text Content</summary>

```text
team-120517075252 » prj 121711041111 » Nodes
Manage Nodes Search node HG B oocumentation
8 Node Name Image Plan Name Plan Type Created At 4 ‘Status Lab URL ‘SSH Access. ‘Actions
Brose ortsisg6t913 TensorFiow casos Howry 15 January, 2026 03:87 pm @ Funning  swoner ‘A Disabled i
° [Z_Launch Notebook
ce Rows por pal >
o © Stop Node
-. Restart Node
Overview Node Events Monitoring Workspace Size Associated Datasets Associated File-Systen® Network & Security 2 Update Image
1 Update Pian
4 DB Delete
Node Details )
oS ————
a Node Name: node-011515361313 #
@ Node Image: TensorFlow pi
Image Version v2.15.0
fay
JupyterLab © installed
Status: @ Running
& Created By:
B Updated At 18 January, 2025 05:06 pm
Plan Netaile oO
```

</details>


![Node Launched 2](/img/image_97aec2264e.png)

:::tip Screenshot Explanation
This image appears to be a screenshot of a graphical user interface, specifically a Jupyter Notebook or a similar interactive development environment (IDE). The interface displays various menu options, including "File", "Edit", "View", "Run", "Kernel", "Git", "Tabs", "Settings", and "Help".

In the main window, two consoles are visible: "Call Notebook" and "Console". Both consoles are running Python 3 with the iPython kernel. The presence of the "(ipykernel)" label indicates that the consoles are connected to an iPython kernel, which allows for interactive execution of Python code.

The image is likely relevant to documentation that explains how to stop a Jupyter Notebook or a similar interactive environment. The original alt text "Node Launched 2" and the context "For Stopping the Notebook you have to click on Stop button and the Node will be stopped" suggest that the image is intended to illustrate the process of stopping a running notebook or node.

However, it's worth noting that the image does not actually show a "Stop" button, which might be a limitation of the documentation. Nevertheless, the image provides context for the environment in which the stopping process takes place, and it may be useful for readers who need to understand the layout and features of the interface.
:::

<details>
<summary>📝 Extracted Text Content</summary>

```text
© Launcher
File Edit View Run Kernel Git Tabs Settings Help
] *e
Call Notebook
oO &
Python 3
= (ipykernel)
bY Console
Python 3
(ipykernel)
Other
```

</details>


#### Stop Nodeâ

For Stopping the Notebook you have to click on Stop button and the Node will be stopped.

![Stop Node](/img/image_61d10c925d.png)

:::tip Screenshot Explanation
This image appears to be a screenshot of a web-based interface for managing nodes in a cloud computing or data science environment. The interface is likely part of a larger platform or service that allows users to create, manage, and deploy nodes for various tasks such as machine learning, data analysis, or scientific computing.

The image shows a table with several columns, including Node Name, Image, Plan Name, Plan Type, Created At, Status, and Actions. The table lists a single node, "node-011515361313", which is running a TensorFlow image (version 2.15.0) and has JupyterLab installed. The node's status is "Running", and it was created on January 15, 2023, and last updated on January 18, 2025.

Below the table, there is a section with more detailed information about the node, including its name, image, image version, and status. There are also several buttons and links that allow the user to manage the node, such as stopping, restarting, or deleting it.

The image also includes a tooltip or alt text that provides additional context for restarting a notebook. It instructs the user to click on the restart button to restart the notebook.

In the context of documentation, this image is likely used to illustrate how to manage nodes and notebooks in a cloud-based environment. It may be used to support tutorials, guides, or user manuals that provide step-by-step instructions for creating, managing, and deploying nodes for various tasks. The image provides a visual representation of the interface and its various components, making it easier for users to understand and follow the instructions.
:::

<details>
<summary>📝 Extracted Text Content</summary>

```text
team-120517075252 » prj 121711041111 » Nodes
Manage Nodes Search node HG B oocumentation
8 Node Name Image Plan Name Plan Type Created At 4 ‘Status Lab URL ‘SSH Access. ‘Actions
Brose ortsisg6t913 TensorFiow casos Howry 15 January, 2026 03:87 pm @ Funning  swoner ‘A Disabled i
° @ _ Launch Notebook
ce Rows por pot >
o © _ Stop Node
-. Restart Node
Overview Node Events Monitoring Workspace Size Associated Datasets Associated File-Systen® Network & Security 2 Update Image
1 Update Pian
4 DB Delete
Node Details )
oS ————
a Node Name: node-011515361313 #
@ Node Image: TensorFlow pi
Image Version v2.15.0
fay
JupyterLab © installed
Status: @ Running
& Created By:
B Updated At 18 January, 2025 05:06 pm
Plan Netaile oO
```

</details>


#### Restart Nodeâ

For Restarting Notebook you have to click on restart button and notebook will be restarted.

![Restart Node](/img/image_47befafdb7.png)

:::tip Screenshot Explanation
This image appears to be a screenshot of a node management interface, likely from a cloud-based platform or a data science environment. The interface displays information about a specific node, including its name, image, plan type, creation date, and status.

The node in question, "node-011515361313", is running a TensorFlow image (version v2.15.0) with JupyterLab installed. The node's status is currently "Running", indicating that it is active and operational. The interface also provides information about the node's creation and update dates, as well as the user who created it.

The image highlights various actions that can be taken on the node, including restarting, stopping, and deleting it. Additionally, there is an option to update the node's image, which is accompanied by a brief instruction to click on "Update image" to initiate the process.

The relevance of this image to the documentation is likely to illustrate the process of managing nodes in a cloud-based environment, specifically updating the image of a node. The image provides a visual representation of the interface and the steps involved in updating a node's image, which can be useful for users who need to perform this task. The documentation may use this image to support instructions or tutorials on node management, providing a clear and concise visual aid to help users understand the process.
:::

<details>
<summary>📝 Extracted Text Content</summary>

```text
team-120517075252 » prj 121711041111 » Nodes
Manage Nodes Search node HG B oocumentation
8 Node Name Image Plan Name Plan Type Created At 4 ‘Status Lab URL ‘SSH Access. ‘Actions
Brose ortsisg6t913 TensorFiow casos Howry 15 January, 2026 03:87 pm @ Funning  swoner ‘A Disabled i
° @ _ Launch Notebook
ce Rows por pat >
o © _ stop Node
-. Restart Node
Overview Node Events Monitoring Workspace Size Associated Datasets Associated File-Systen® Network & Security F Update image
1 Update Pian
4 DB Delete
Node Details )
oS ————
a Node Name: node-011515361313 #
@ Node Image: TensorFlow pi
Image Version v2.15.0
fay
JupyterLab © installed
Status: @ Running
& Created By:
B Updated At 18 January, 2025 05:06 pm
Plan Netaile oO
```

</details>


#### Update Imageâ

You can update notebook image, For updating image you have to click on update image.

![Update Node](/img/image_1eb7a2eb59.png)

:::tip Screenshot Explanation
This image appears to be a screenshot of a node management interface, specifically the "Nodes" section of a cloud-based platform. The platform allows users to create, manage, and monitor nodes, which are likely virtual machines or containers used for computing tasks.

The image displays a table with a list of nodes, including their names, images, plan names, plan types, creation dates, and statuses. Each node has a set of actions available, such as stopping or restarting the node. The table also shows pagination options, allowing users to navigate through multiple pages of nodes.

Below the table, there are several tabs and options for managing nodes, including updating images, deleting nodes, and accessing node details. The node details section displays information about a specific node, including its name, image version, status, and creation date.

The image also shows a JupyterLab status, indicating whether JupyterLab is installed on the node. JupyterLab is an interactive development environment commonly used for data science and machine learning tasks.

The context of the image suggests that it is part of a documentation or tutorial that guides users on how to update a node's image. The original alt text "Update Node" and the context "Select image and click on update button" support this interpretation.

Overall, this image is relevant to documentation that focuses on node management, cloud computing, and data science or machine learning workflows. It provides a visual representation of the node management interface and illustrates the steps involved in updating a node's image.
:::

<details>
<summary>📝 Extracted Text Content</summary>

```text
team-111816235953 > defaul-project » Nodes
Manage Nodes Search node 3) © B oocumentarion
8 Node Name Image Plan Name Plan Type Created At ‘Status Lab URL SSH Access. Actions
fq nxorensoeoaca bunts cas Houry 14 January, 2025 03:09pm © Running Disabled o i
° _ ‘Stop Node
CS nodeott4t2982121 PyTorch c34 Hourly 14 January, 2025 12:36 pm @ Funning = supyter ve © SP
© Restart Node
o 2
e Rows perpage: [ 7 Update image J, >
CC Ts 2 Update Plan =
es —_
° DB Delete
Z Overview Node Events Monitoring Workspace Sie Associated Datasets Associated File-Systen® Network & Securly Images
ic) Node Details fo}
Node Name: node-011415082323
° Node Image vountu
Image Version 22.08
& JupyterLab: @ Not installed
8 Status: @ Running
Created By: preeti.awatsthorprepaidinr@eZenetworks.com
@ Updated At: 15 January, 2025 02:30 pm
Legal © 2025 EE Networks Limited ™ OaxXs @ contact Us
```

</details>


Select image and click on update button.

![Update Node](/img/image_9d6607cac6.png)

:::tip Screenshot Explanation
**Image Description: Update Node Confirmation Dialog**

The image depicts a confirmation dialog box with the title "Update Node Image". The dialog box contains a warning message that alerts the user of the consequences of updating the node image, specifically that the node will restart and any manually installed packages will need to be re-installed after the restart. The message prompts the user to confirm their intention to update the image, with the question "Are you sure you want to update image ?".

**Relevance to Documentation:**

This image is relevant to the documentation as it illustrates the confirmation step required to update a node. The image provides visual context to the documentation, allowing users to understand the process and potential consequences of updating a node. The image is likely used in a section of the documentation that explains how to update a node, and serves as a visual aid to support the written instructions.
:::

<details>
<summary>📝 Extracted Text Content</summary>

```text
Update Node Image
Updating the image will cause the nade to restart. Any packages you manually installed on
this node will need to be re-installed ater the restart.
‘Are you sure you want to update image ?
```

</details>


#### Update Planâ

You can update Node, For updating the Node You have to click on Update button.

![Update Node](/img/image_4ebbb1b373.png)

:::tip Screenshot Explanation
This image appears to be a screenshot of a node management interface, likely from a cloud-based platform or a data science workspace. The interface is displaying a specific node, identified as "node-011515361313," which is running a TensorFlow image (version v2.15.0) with JupyterLab installed.

The image shows various details about the node, including its name, image, plan type, creation date, and status. The status is currently "Running," indicating that the node is active and operational. The interface also provides options for managing the node, such as stopping, restarting, and deleting it.

Notably, the image highlights a crucial aspect of node management: the requirement for a node to be in a "Stop" state before updating it. This is indicated by a contextual message below the "Update Node" button, which reads, "NoteNode must be in Stop state before updating the Node."

In the context of documentation, this image is likely used to illustrate the process of managing nodes in a data science or machine learning workflow. It may be used to support tutorials, guides, or troubleshooting articles related to node management, TensorFlow, JupyterLab, or cloud-based data science platforms. The image provides a clear visual representation of the node management interface and its associated features, making it easier for users to understand and follow along with the documentation.
:::

<details>
<summary>📝 Extracted Text Content</summary>

```text
team-120517075252 » prj 121711041111 » Nodes
Manage Nodes Search node HG B oocumentation
8 Node Name Image Plan Name Plan Type Created At 4 ‘Status Lab URL ‘SSH Access. ‘Actions
Brose ortsisg6t913 TensorFiow casos Howry 15 January, 2026 03:87 pm @ Funning  swoner ‘A Disabled i
° @ _ Launch Notebook
ce Rows por pat >
o © stop Node
-. Restart Node
Overview Node Events Monitoring Workspace Size Associated Datasets Associated File-Systen® Network & Security 2 Update Image
1 Update Plan
4 DB Delete
Node Details )
oS ————
a Node Name: node-011515361313 #
@ Node Image: TensorFlow pi
Image Version v2.15.0
fay
JupyterLab © installed
Status: @ Running
& Created By:
B Updated At 18 January, 2025 05:06 pm
Plan Netaile oO
```

</details>


Node must be in Stop state before updating the Node.

#### Convert to Committedâ

After creating a node, it can be converted to a committed node if the committed SKU is available by selecting the "Convert to Committed" option.

Nodes on an hourly plan without an associated SKU will display a grayed-out "Convert to Committed" button.

Nodes on the Private Cluster or already Committed does not show this option.

This feature allows a node to be converted to a committed node without the need to stop or restart it, ensuring seamless operation.

![Convert to Committed Option](/img/image_95fc93fe09.png)

:::tip Screenshot Explanation
This image appears to be a screenshot of a node management dashboard within a private workspace, specifically the "default-project" environment. The dashboard, titled "Manage Nodes," displays a table listing available nodes, including their names, images, plan names, plan types, creation dates, statuses, and associated actions.

The nodes listed are primarily related to Transformers, a type of artificial intelligence model, with varying plan types (e.g., "C3.8GB_Free Hourly" and "C3.8GB Hourly"). The statuses indicate that these nodes are currently running, but with JupyterLab access disabled.

The dashboard provides various options for managing these nodes, including the ability to stop, restart, or delete them. Additionally, users can launch notebooks, access pipelines, update images, and convert nodes to committed versions.

The image also shows several navigation menus and links, such as "Datasets," "Pipelines," "Project Settings," "Billing and Usage," and "Contact Us." The footer displays copyright information and a contact link.

In the context of documentation, this image is likely used to illustrate the node management capabilities within a private workspace. It may be used to support tutorials or guides on how to create, manage, and deploy AI models, such as Transformers, within this specific environment. The image may also serve as a reference point for understanding the various features and options available within the node management dashboard.
:::

<details>
<summary>📝 Extracted Text Content</summary>

```text
Al PLATFORM
Private Workspace > default-project » Nodes
Manage Nodes Q Search node at CG | EY pocumentartion
O= Dashboard
B Nodes a Node Name Image Plan Name Plan Type Created At 7S Status Lab URL SSH Access Actions
| @ Nodes _—
Transformers C3.8GB_Free Hourly @ Running — Jupyter A Disabled :
& RAG Vv Transformers C3.8GB Hourly @ Running - Jupyter Disabled :
[—] Datasets [A Launch Notebook
Rows per pac
Stop Node
Cg Training Cluster = iO) r
——— © Restart Node
@) Inference v . — ; : ; ; e
Overview Node Events Monitoring Workspace Size Associated Datasets Associated File-System Z Update Image
= Pipelines v
t — Update Plan
[H} Foundation Studio v -O- Convert to Committed
Node Details
<, Vector Database 0 Delete
£3 ~~ Data Syncer v Node Name:
1 Intearations v Node Image: Transformers Se
68 Project Settings Image Version: v4.45.2
JupyterLab: G Installed
{@ Billing and Usage
Status: > Paenine
@ IAM Panel Created By:
Legal © 2025 E2E Networks Limited ™ HB aX Aj @ Contact Us
```

</details>


![Convert to Committed Option](/img/image_40b2620033.png)

:::tip Screenshot Explanation
**Image Description:**

This image displays a "Convert to Committed Plan" option, which allows users to reserve a node by converting it into a committed service at a discounted price. The image presents a selection of committed node plans with varying durations and corresponding prices:

* 90 Days Committed: ¥6,026
* 183 Days Committed: ¥11,573
* 365 Days Committed: ¥21,725
* 1095 Days Committed: ¥48,880.8

**Relevance to Documentation:**

This image is likely part of a documentation or user guide for a cloud computing or infrastructure management platform. The image illustrates the process of converting a node to a committed service, which can provide cost savings for users who commit to a specific duration. The documentation may use this image to explain the benefits and options available for committed plans, helping users make informed decisions about their resource allocation and cost management.
:::

<details>
<summary>📝 Extracted Text Content</summary>

```text
Convert to Committed Plan
You can reserve this node by converting it into a committed service at a discounted price.
Please select a committed node plan below, which will be applicable from the date of the
actual conversion.
Select a suitable committed plan a
90 Days Committed, ¥6026
183 Days Committed, §11573
365 Days Committed, ¥21725
1095 Days Committed, 748880.8 i
```

</details>


![Convert to Committed Option](/img/image_af446f3144.png)

:::tip Screenshot Explanation
**Image Description:**

This image depicts a dialog box or menu option labeled "Convert to Committed Plan." It appears to be a user interface element within a cloud computing or virtual machine management platform. The image presents the user with options to reserve a node by converting it into a committed service at a discounted price.

**Key Elements:**

1. **Committed Plan Selection:** A dropdown menu or selection field labeled "Committed Plan" allows the user to choose a plan, with the option "90 Days Committed, ¥6026" visible in the image.
2. **Auto Renewal:** A checkbox or toggle labeled "Auto Renewal" enables the user to set up automatic renewal of the committed plan.
3. **Alternative Options:** Two additional options are presented:
	* "Convert to Hourly Plan": This option allows the user to switch to hourly billing, charged at ¥3.1 per hour.
	* "Auto Delete": This option enables automatic deletion of the committed machine.

**Relevance to Documentation:**

This image is likely relevant to documentation related to cloud computing, virtual machine management, or infrastructure-as-a-service (IaaS) platforms. The image may be used to illustrate the process of converting a node to a committed service, highlighting the benefits of discounted pricing and automatic renewal options. It may also serve as a visual aid for explaining the differences between committed and hourly billing plans, as well as the auto-deletion feature.
:::

<details>
<summary>📝 Extracted Text Content</summary>

```text
Convert to Committed Plan
You can reserve this node by converting it into a committed service at a discounted price.
Please select a committed node plan below, which will be applicable from the date of the
actual conversion.
Committed Plan *
90 Days Committed, ¥6026 v
Auto Renewal
Auto renewal of this committed plan
Convert to Hourly Plan a
Auto start hourly billing for this machine, charged at %3.1/hr
Auto Delete
Auto deletion of this committed machine
```

</details>


#### Save Imageâ

When the node is restarted, any packages you manually installed will need to be re-installed. By saving an image, you can preserve all dependencies, allowing you to restore them later or create new nodes from the saved image.

##### Create Imageâ

To save an image, click the 'Save Image' button, enter a valid name, and select the container registry where the image should be saved. The saved image will then also appear in the chosen container registry.

![Create Saved Image](/img/image_5f3b296597.png)

:::tip Screenshot Explanation
**Image Description: Node Details and Management Interface**

The provided image appears to be a screenshot of a node management interface, likely from a cloud computing or data science platform. The interface displays detailed information about a specific node, including its name, image plan, plan type, creation date, and status.

The top section of the image shows the node's name, "node-012818132929," and its associated image plan, "Transformers GDC.1xH200-30.375GB_SXM." The plan type is listed as "Hourly," indicating that the node is billed on an hourly basis. The creation date and time are also displayed, showing that the node was created on January 28, 2025, at 6:13 pm.

Below the node information, the image shows a series of actions that can be performed on the node, including launching a notebook, stopping the node, restarting the node, and updating the image or plan. There are also links to view node events, monitoring, workspace size, associated datasets, file systems, network and security settings, and an option to save the image.

The image also displays a button to "Restore Image" under the context of storing saved dependencies and packages. This suggests that the image is relevant to documentation related to node management, image creation, and package management in a cloud computing or data science environment.

**Relevance to Documentation:**

This image is likely relevant to documentation related to:

1. Node management: The image provides a clear example of a node management interface, including the types of information displayed and actions that can be performed on a node.
2. Image creation and management: The image shows how to create and manage images, including saving and restoring images, and updating image plans.
3. Package management: The context of storing saved dependencies and packages suggests that the image is relevant to documentation related to package management in a cloud computing or data science environment.

Overall, the image provides a clear and concise visual representation of a node management interface and is likely to be useful in documentation related to cloud computing, data science, and node management.
:::

<details>
<summary>📝 Extracted Text Content</summary>

```text
Node Name Image Plan Name Plan Type Created At 7S Status Lab URL SSH Access Actions
node-012818132929 Transformers GDC.1xH200-30.375GB_SXM Hourly 28 January, 2025 06:13 pm @ Running S jupyter A Disabled :
{4 Launch Notebook
Rows per pac
@® Stop Node
— © Restart Node
Overview Node Events Monitoring Workspace Size Associated Datasets Associated File-Systen® Network & Security wy Save Image
@ Update Image
Tt — Update Plan
Node Details
-O- Convert to Committed
Node Name: node-012818132929 7 Bi sDelete
Node Image: Transformers py
```

</details>


![Create Saved Image](/img/image_f31904b391.png)

:::tip Screenshot Explanation
The image depicts a graphical user interface (GUI) for creating and storing a saved image in a container registry. The interface includes three primary fields:

1. **Image Name**: A text field where the user can enter a suitable name for the image, with "node-image" provided as a placeholder.
2. **Image Tag (Optional)**: A text field for adding an optional tag to the image.
3. **Container Registry**: A dropdown menu that allows the user to select a container registry from a list of existing options. The selected registry is "gygygggg7543u2b v". There is also an option to create a new registry.

The context of the image suggests that it is part of a documentation or tutorial that guides users on how to store dependencies and packages. The image is relevant to the section that explains how to create and store saved images, which can be restored later using the "Restore Image" icon under the "Images" tab.
:::

<details>
<summary>📝 Extracted Text Content</summary>

```text
Image Name*
Please enter a suitable name for the image
node-image
Image Tag (Optional)
Please enter a suitable tag for the image
Container Registry*
This save image will be stored in your container registry. Select a registry from the list below or Click here to create a new registry
gygygggg7543u2b v
```

</details>


To store all saved dependencies and packages, click Restore Image icon under Images tab.

![Restore Image](/img/image_9a1303c8f9.png)

:::tip Screenshot Explanation
The image appears to be a screenshot of a monitoring or management interface, specifically displaying information about a node image. The interface is organized into various sections, including:

1. Overview: Providing a brief summary of the node image.
2. Node Events: Displaying a log of events related to the node.
3. Monitoring: Offering real-time monitoring data for the node.
4. Workspace: Possibly showing the node's allocated resources or configuration.
5. Associated Datasets: Listing datasets linked to the node.
6. Associated File-System: Displaying file system information related to the node.
7. Network & Security: Providing network and security settings for the node.
8. Images: Listing available images for the node.

The main content area of the image shows a table with the following columns:

* Image Name
* Registry
* Namespace
* Created At
* Status

The table contains a single row with information about a node image named "node-image:latest", which was created on January 28, 2025, at 06:26 pm, and has a status of "Succeeded".

In the context of the documentation, this image is relevant to the process of deleting a node. The original alt text "Restore Image" suggests that the image is also related to restoring or managing node images. The image is likely used to illustrate the steps involved in deleting a node, which requires clicking on the "Delete" button. Overall, the image provides a visual representation of the node image management interface and is used to support the documentation's instructions on node deletion.
:::

<details>
<summary>📝 Extracted Text Content</summary>

```text
Overview Node Events Monitoring Workspace Size Associated Datasets Associated File-System Network & Security Images
Image Name Registry Namespace Created At Status
node-image:latest gygygggg7543u2b 28 January, 2025 06:26 pm @ Succeeded ial
Rows per page: Sy 1-1 of 1
```

</details>


#### Delete Nodeâ

For Deleting the Node you have to click on Delete button.

![Delete Node](/img/image_e3cb7d9cea.png)

:::tip Screenshot Explanation
This image appears to be a screenshot of a node management interface, likely from a cloud computing or virtual machine platform. The interface displays a table with several columns, including:

1. Node Name: A unique identifier for each node.
2. Image: The image or template used to create the node.
3. Plan Name: The name of the plan or configuration associated with the node.
4. Plan Type: The type of plan, in this case, "Hourly".
5. Created At: The date and time the node was created.
6. Status: The current status of the node, which is "Disabled" in this case.
7. Lab URL: A link to access the node's lab environment.
8. SSH Access: Information about SSH access to the node.

The table contains a single row with a node named "node-011515361313". The node was created on January 16, 2025, at 03:37 pm, and is currently disabled.

Below the table, there are several action buttons:

1. Launch Notebook: A button to launch a notebook from the node.
2. Stop Node: A button to stop the node.
3. Restart Node: A button to restart the node.
4. Update Plan: A button to update the node's plan.
5. Delete Node: A button to delete the node.

The image is relevant to the documentation as it illustrates the node management interface and the various actions that can be performed on a node. The context note suggests that the node can be launched from the left side of the Node name, indicating that there may be additional functionality or options available when interacting with the node. Overall, this image provides a visual representation of the node management interface and its features, which can be useful for users and administrators working with this platform.
:::

<details>
<summary>📝 Extracted Text Content</summary>

```text
Manage Nodes Q Search node 3) © B oocumentarion
8 Node Name Image Plan Name Plan Type. Created At 4 Status ‘Lab URL ‘SSH Access Actions
BH _ noseortstes61s18 TER cs.ac8 Hourly 16 January, 2025 03:37 pm © Punning supper ‘A Disabied :
° @Z_ Launch Notebook
cs ows per pag >
a © stop Node
b ——— «Restart Node
1 Update Plan
: a
a Node Name: node-011515361313
ray
& Created By:
Plan Netaile oO
```

</details>


### Launch Node from Sidebarâ

You can launch the node from the left side of the Node name.

![Launch from Sidebar](/img/image_91b1985b46.png)

:::tip Screenshot Explanation
The provided image appears to be a screenshot of a node management interface, likely from a cloud computing or virtual machine platform. The image displays a table with several columns, including "Node Name," "Image Plan Name," "Plan Type," "Created At," and "Status." The table lists a single node, "node-040915365151," which is running a PyTorch image plan.

The interface also features various buttons and links, including "Manage Nodes," "Search node," and "Configure SSH." The "Configure SSH" section allows users to enable SSH access to the node, either by uploading an existing SSH key or creating a new one. Additionally, the interface displays a notification informing the user that they will receive an email when the IP address is assigned to the node and SSH is activated.

The image seems to be relevant to documentation related to node management, SSH configuration, and virtual machine setup. It may be used to illustrate the process of launching and managing nodes, configuring SSH access, and monitoring node activity. The context provided suggests that the image is part of a larger guide or tutorial that explains how to use the platform's features, including searching for nodes and configuring SSH access.
:::

<details>
<summary>📝 Extracted Text Content</summary>

```text
CB eeam-osoo11365059 + detaut-poject » Nodes
a oo
Manage Nodes @ Search node =) © [|B oocumenrarion |
a Node Name Image Plan Name Plan Type Created At 4 Status Lab URL SSH Access Actions
@ =
node-040915365151 PyTorch ca.8cB wemty (09 April, 2025 03:37 pm O emir = jupyter o :
8 Rows perpage: 5 ~  1-tolt <>
w Tn
ie Overview Node Events Monitoring Workspace Size Associated Datasets Associated File-System | Network & Security Images
Configure SSH (o)
@ _Youwill also receive an email when IP address is assigned to this node and SSH is activated.
iQ Enable SSH Access @I@®
aS Choose a pre-existing SSH key for seamless access by uploading the key fl. Click here to create new one.
Bearch label x +
Label SSH Key ‘Action
e2e fo)
{ewes =
B EEE
Legal © 2025 E2E Networks Limited ™ BAXA @ Contact Us
```

</details>


#### Advance Filter on Nodeâ

You can locate the node by entering its name in the search bar.

![Node Search](/img/image_7ac56c23fe.png)

:::tip Screenshot Explanation
This image appears to be a screenshot of a user interface for a machine learning or artificial intelligence platform, specifically a node management dashboard. The dashboard is titled "Nodes" and is part of a project named "default-project" within the "Priest Private Workspace".

The interface displays various information and options related to node management, including:

1. Node details: The node name, image (Transformers), and status (Running) are displayed.
2. Associated datasets and models: The dashboard shows the number of datasets and models associated with the node, as well as options to configure and manage them.
3. Node events and monitoring: The interface provides options to monitor node events, disk size, and associated file systems.
4. Model endpoints and custom tokens: The dashboard displays options to manage model endpoints and custom tokens.
5. Pipelines and JupyterLab: The interface shows the number of pipelines and indicates that JupyterLab is installed.
6. Node configuration and management: Options to configure SSH, associated file systems, and node details are available.

The image also includes a sidebar with various options, such as accessing advanced filter options, template gallery, and add-ons. The footer of the image displays copyright information and contact details for E2E Networks Limited.

The original alt text "Node Search" suggests that the image is relevant to a documentation section that explains how to search for nodes within the platform. The context provided indicates that the image is used to illustrate how to access advanced filter options by clicking on a specific button. Overall, this image is likely used to support documentation on node management and configuration within the platform.
:::

<details>
<summary>📝 Extracted Text Content</summary>

```text
GTR (sence) oc: i ©
Priest Private Workspace » default-project » Nodes
default-project ~ io
93 Dashboard
[sais oe = —— a recue can nom came pee)
Datasets =
a Transformers ca.868 Hourly @ unning  supyter ‘A, Disabled :
3 Multi-Node Training
Rows perpage: 5 + t-tof1
@ Inference a
© Model Repositor
Postiony Overview Node Events Monitoring Disk Size Associated Datasets Configure SSH Associated File-Systen®
© Model Endpoints
© Custom Tokens Node Detatle ©
© Playground
Node Name:
3 Pipelines a Node Image: Transformers (3)
© Pipeline JupyterLab Installed: True
Status: @ Running
© Run
Created By:
© Scheduled Run Created At
© Template Gallery QED
Plan Details
@ Foundation Studio -« ©
© Fine Tune Models Connection Details °
© GenAl AP ‘Add-ons ©
{& COLLAPSE SIDEBAR
Legal (© 2024 E2E Networks Limited ™ BAYA @ Contact Us
```

</details>


You can access advanced filter options by clicking on this button.

![Search Button](/img/image_f42e5b45f3.png)

:::tip Screenshot Explanation
The provided image appears to be a screenshot of a web-based interface, specifically a node management dashboard, likely from a cloud computing or data science platform. The interface displays a table with various columns, including "Node Name", "Image Plan Name", "Plan Type", "Updated On", "Status", and "Actions".

The table shows a single node, named "Transformers", with a status of "Running" and an image plan name of "c3.8xlarge". The node is associated with a JupyterLab environment, as indicated by the "JupyterLab Installed: True" label.

Below the table, there are several tabs and buttons, including "Overview", "Node Events", "Monitoring", "Disk Size", "Associated Datasets", and "Configure SSH". These tabs suggest that the interface provides detailed information about the node, its performance, and its configuration.

In the context of the documentation, the image is relevant to a section that discusses applying advanced filter configurations and searching for nodes. The "Search Button" alt text suggests that the image is intended to illustrate the step of clicking the search button after configuring filters.

Overall, the image appears to be a visual aid for a tutorial or documentation on managing nodes and using advanced filter configurations in a cloud-based platform.
:::

<details>
<summary>📝 Extracted Text Content</summary>

```text
GTR (sence) oc: i ©
TF _private Workspace » defaultiproject » Nodes
83 Manage Nodes Q Search node © [|B vocumenrarion |
LEB) Node Name Image Plan Name Plan Type Updated On Status Lab URL SSH Access Actions
cs = :
Transformers c3.8c8 Hourly @ unning  supyter ‘A, Disabled :
Rowsperpage: § § ~ =— I-toft <>
Ss °
Overview Node Events Monitoring Disk Size Associated Datasets Configure SSH__—_Associated File-Systent
Node Details (o)
& Node Name:
Node Image: Transformers. &
JupyterLab Installed: True
Status: @ Running
Created By:
Created At
Plan Details fo)
Connection Details fo)
ia ‘Add-ons (0)
Legal (© 2024 E2E Networks Limited ™ BAYA @ Contact Us
```

</details>


You can apply the advanced filter configurations and then click the search button.

![Advanced Search](/img/image_616c5f8f33.png)

:::tip Screenshot Explanation
This image appears to be a screenshot of a user interface from a cloud computing or data science platform, likely a node management dashboard. The primary focus of the image is the "Node Details" section, which displays information about a specific node named "Transformers."

The node details include the following key information:

* Node Name: Transformers
* Node Image: Transformers
* JupyterLab Installed: True, indicating that JupyterLab is installed on this node
* Status: Running, indicating that the node is currently active

The image also shows various other sections and features, including:

* A search bar with the placeholder text "Search node"
* A table listing nodes, including their name, plan name, plan type, SSH access, and status
* A dropdown menu for selecting the number of rows to display per page
* Links to access various features, such as node events, monitoring, disk size, associated datasets, and SSH configuration
* A section for adding add-ons and accessing legal information

The relevance of this image to the documentation is likely to illustrate the process of managing nodes on this platform, including creating, configuring, and monitoring nodes. The image may be used to support documentation on topics such as:

* Creating and managing nodes
* Configuring node settings and add-ons
* Monitoring node performance and events
* Using JupyterLab on nodes

Overall, the image provides a visual representation of the node management dashboard and can be used to help users understand the layout and features of the platform.
:::

<details>
<summary>📝 Extracted Text Content</summary>

```text
GTR (sence) oc: i ©
TF _private Workspace » defaultiproject » Nodes
83 Manage Nodes Q Search node 3) © | By vocumentarion |
| Name
LEB) Node Name Image Plan Name Plan Type SSH Access Actions
° Status ~ +
ce OO ,
Transformers c3.8c8 Hourly A Disabled 8
@ Image Type ~ &§
Rowsperpage: § § ~ =— I-toft <>
Image
Ss °
Overview Node Events Monitoring Disk Size Associated Datasets Configure SSH__—_Associated File-Systent ‘Sku Series ~
a ‘Sku Type ~
Node Details (o)
° <= al
& Node Name:
Node Image: Transformers. &
JupyterLab Installed: True
Status: @ Running
Created By:
Created At
Plan Details fo)
Connection Details fo)
ia ‘Add-ons (0)
Legal (© 2024 E2E Networks Limited ™ BAYA @ Contact Us
```

</details>


- Getting Started with Nodes on TIR
- Node Images
- Node Options
- Node Status
- How to Create Node?
- Node DetailsOverviewNode EventsMonitoringWorkspace SizeAssociated DatasetsAssociated File SystemNetwork & securityStart script
- Overview
- Node Events
- Monitoring
- Workspace Size
- Associated Datasets
- Associated File System
- Network & security
- Start script
- Node ActionsLaunch NotebookStop NodeRestart NodeUpdate ImageUpdate PlanConvert to CommittedSave ImageDelete Node
- Launch Notebook
- Stop Node
- Restart Node
- Update Image
- Update Plan
- Convert to Committed
- Save Image
- Delete Node
- Launch Node from SidebarAdvance Filter on Node
- Advance Filter on Node

- Overview
- Node Events
- Monitoring
- Workspace Size
- Associated Datasets
- Associated File System
- Network & security
- Start script

- Launch Notebook
- Stop Node
- Restart Node
- Update Image
- Update Plan
- Convert to Committed
- Save Image
- Delete Node

- Advance Filter on Node

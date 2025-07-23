# TIR Nodes

TIR Nodes are fully collaborative environments that make AI development possible by combining the power of containers, Jupyter Labs, and AI/ML frameworks. These versatile development environments support a wide range of use cases:

- **Fine-tuning Large Language Models**: Optimize and customize LLMs for specific applications with dedicated GPU resources
- **Running Jupyter notebooks**: Interactive development environment with pre-installed data science and AI libraries  
- **Downloading and testing datasets and models**: Efficient data management with high-performance storage options
- **Command-line and SSH configuration options**: Complete terminal access for advanced development workflows

> **Note**: All TIR Nodes include full command-line and SSH access capabilities, enabling both interactive notebook development and traditional server-based workflows.

---

## Getting Started with Nodes on TIR

Creating and accessing TIR Nodes follows a straightforward process designed for both individual developers and enterprise teams:

1. **Account Access**: Log into your E2E Networks account and navigate to the TIR platform section
2. **Project Setup**: Create or select an existing project within your workspace environment  
3. **Node Access**: Navigate to the Nodes section from the left navigation panel
4. **Configuration**: Configure your node specifications including image type, hardware resources, and storage requirements
5. **Review and Deploy**: Review configuration summary and deploy your node
6. **Access Environment**: Access your running node through Jupyter interface or SSH connection

This comprehensive workflow typically takes 2-5 minutes from initiation to fully operational development environment, depending on resource availability and configuration complexity.

---

## Node Images

TIR provides several pre-configured image options designed to match different development workflows and AI/ML requirements.

![TIR Pre-built Image Selection](https://docs.e2enetworks.com/assets/images/node_create_tirprebuilt-6fe32f7a774c2d3dadb7f5d167ca1392.png)

The node image selection interface displays E2E Networks' comprehensive collection of AI-optimized development environments. Each image tile shows detailed information about the included software stack, optimization features, and recommended use cases. The interface enables easy browsing and selection of the most appropriate environment for your specific AI development needs.

### Base OS Image

![Base OS Selection Interface](https://docs.e2enetworks.com/assets/images/node_create_baseos-7822960dbeed2c236e77da807fe1c30e.png)

The Base OS selection interface presents various Linux distribution options with detailed version information and compatibility specifications. This screenshot shows the operating system selection panel where users can choose from different Ubuntu versions, CentOS distributions, and other Linux variants, each with clear version numbers and recommendation indicators.

**Available Distributions**:
- **Ubuntu LTS Versions**: 20.04, 22.04 with long-term support and stability
- **CentOS Options**: Enterprise-focused distributions for organizational requirements
- **Debian Variants**: Lightweight options for specialized configurations
- **Custom Distributions**: Specialized Linux builds for specific AI/ML requirements

The Base OS approach provides maximum customization flexibility, allowing users to build their development environment from the ground up according to specific organizational standards or unique technical requirements.

### Jupyter Image

![Jupyter Development Environment](https://docs.e2enetworks.com/assets/images/note_book_overview3-ea56bda8301e383531e7162eaf778941.png)

The Jupyter environment interface showcases a fully configured development workspace with JupyterLab running in a professional layout. This screenshot demonstrates the integrated development experience with file browser, notebook editor, terminal access, and extension panels all within a single, cohesive interface.

**Pre-configured Development Stack**:
- **JupyterLab Interface**: Modern, extensible web-based IDE with customizable layouts
- **Python Data Science Libraries**: pandas, numpy, scipy, matplotlib, seaborn pre-installed
- **Machine Learning Frameworks**: TensorFlow, PyTorch, scikit-learn with GPU acceleration
- **Visualization Tools**: plotly, bokeh, altair for interactive data visualization
- **Development Tools**: Git integration, debugger, variable inspector, and code formatting

The environment provides immediate productivity without configuration overhead, enabling data scientists and AI researchers to begin development work immediately upon node creation.

### ComfyUI

ComfyUI offers a revolutionary visual interface for AI workflow design, transforming complex AI operations into intuitive, node-based visual programming.

**Visual Workflow Features**:
- **Node-Based Design**: Drag-and-drop interface for building complex AI pipelines
- **Pre-built Components**: Extensive library of nodes for common AI operations
- **Generative AI Support**: Native integration with Stable Diffusion and other generative models
- **Real-time Preview**: Immediate visual feedback during workflow development
- **Custom Node Development**: Extensible architecture for specialized requirements

This environment particularly excels for creative professionals, digital artists, and research teams who prefer visual workflow design over traditional code-based approaches.

### FramePack

FramePack images provide comprehensive multi-framework environments designed for users who require access to multiple AI/ML frameworks within a single, optimized development environment.

**Integrated Framework Ecosystem**:
- **TensorFlow Stack**: Complete TensorFlow ecosystem with Keras, TensorBoard, and TensorFlow Extended
- **PyTorch Environment**: PyTorch, torchvision, torchaudio with distributed training support
- **Hugging Face Integration**: Transformers library with model hub access and pipeline tools
- **Computer Vision Suite**: OpenCV, PIL, scikit-image for comprehensive image processing
- **Traditional ML Tools**: scikit-learn, XGBoost, LightGBM for classical machine learning
- **Research Frameworks**: JAX, Flax for cutting-edge machine learning research

**Performance Optimizations**:
- Memory usage optimization for large model training and inference
- GPU utilization enhancements for maximum computational throughput
- Library compatibility verification across all framework versions  
- Pre-configured environment variables for optimal cross-framework performance
- Automated dependency management to prevent version conflicts

FramePack environments eliminate the complexity of managing multiple framework installations while providing enterprise-grade performance optimization for production AI development workflows.
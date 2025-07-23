# TIR Nodes

TIR Nodes are fully collaborative environments that make AI development possible by combining the power of containers, Jupyter Labs, and AI/ML frameworks. These versatile development environments support a wide range of use cases:

- **Fine-tuning Large Language Models**: Optimize and customize LLMs for specific applications with dedicated GPU resources
- **Running Jupyter notebooks**: Interactive development environment with pre-installed data science and AI libraries  
- **Downloading and testing datasets and models**: Efficient data management with high-performance storage options
- **Command-line and SSH configuration options**: Complete terminal access for advanced development workflows

> **Note**: All TIR Nodes include full command-line and SSH access capabilities, enabling both interactive notebook development and traditional server-based workflows.

---

## Getting Started with Nodes on TIR

Creating and accessing TIR Nodes follows a straightforward process designed for both individual developers and enterprise teams. The process begins with accessing the node creation interface through the TIR dashboard.

![Create Node Interface](https://docs.e2enetworks.com/assets/images/click_create_node-5cdfde38a5974bab42107967b1db8214.png)

The TIR dashboard provides a clean, intuitive interface with the "Create Node" button prominently displayed for immediate access. This screenshot shows the main navigation area where users can initiate the node creation process. The interface design ensures that creating new development environments is always just one click away.

**Complete Workflow Process**:

1. **Account Access**: Log into your E2E Networks account and navigate to the TIR platform section
2. **Project Setup**: Create or select an existing project within your workspace environment  
3. **Node Initiation**: Click the "Create Node" button shown in the interface above
4. **Configuration**: Configure your node specifications including image type, hardware resources, and storage requirements
5. **Review and Deploy**: Review configuration summary and deploy your node
6. **Access Environment**: Access your running node through Jupyter interface or SSH connection

This comprehensive workflow typically takes 2-5 minutes from initiation to fully operational development environment, depending on resource availability and configuration complexity. The "Create Node" button serves as the entry point for this entire process.

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

---

## Node Options

TIR Nodes offer extensive configuration options to customize your development environment according to specific requirements and use cases.

### Enable SSH

SSH access provides complete command-line control over your development environment with enterprise-grade security features.

**SSH Configuration Benefits**:
- **Secure Authentication**: RSA and Ed25519 key support with encrypted key storage
- **Flexible Access**: Configurable SSH port settings and IP filtering capabilities
- **Multi-user Support**: Team-based SSH access with individual authentication credentials
- **Advanced Security**: Network access restrictions and comprehensive audit logging

SSH enables advanced system administration tasks, custom software installation, and seamless integration with external development tools and CI/CD pipelines. This is particularly valuable for teams requiring full system access or organizations with specific security requirements.

### Disk Size

![Storage Configuration Interface](https://docs.e2enetworks.com/assets/images/node_create_node_storage-078d77740cb90960b457a6b3581d607c.png)

The storage configuration interface provides comprehensive options for managing node storage requirements. This interface displays various storage tiers, capacity options, and performance characteristics available for TIR Nodes.

**Available Storage Options**:
- **30GB Free Workspace**: Automatically included with every node at no additional cost for immediate development needs
- **Standard Persistent Storage**: Scalable up to 5,000GB with complete data persistence across node lifecycle
- **High-Performance SSD**: Enhanced read/write speeds for frequently accessed datasets and active development work
- **Network Storage**: Shared storage capabilities enabling seamless collaboration across team members

The interface clearly displays pricing information for different storage configurations, enabling users to optimize costs based on their specific data access patterns and performance requirements. Storage selection should consider factors like dataset size, access frequency, and collaborative requirements.

### Local NVME Storage

High-speed local NVME storage delivers exceptional performance for data-intensive operations requiring maximum throughput and minimal latency.

**Performance Advantages**:
- **Ultra-fast Operations**: Exceptional read/write speeds for large dataset processing and model training
- **Minimal Latency**: Optimal for real-time inference applications and interactive development
- **High Throughput**: Perfect for model checkpoints, training state management, and temporary processing
- **Cache Optimization**: Ideal for frequently accessed data requiring immediate availability

**Critical Consideration**: Local NVME storage is ephemeral and will be permanently lost during node recreation or termination. This makes it suitable exclusively for temporary, high-performance operations rather than long-term data storage.

### Plan (Pricing)

TIR Nodes support flexible billing models designed to optimize costs across different usage patterns and organizational requirements.

**Hourly Billing Model**:
- **Pay-per-use Structure**: Billing begins immediately when nodes become active and stops when nodes are terminated
- **Cost Optimization**: Automatic savings when nodes are stopped during idle periods
- **Development Friendly**: Perfect for experimentation, testing, and variable development workloads
- **No Commitments**: Complete flexibility without long-term contracts or minimum usage requirements

**Committed Plan Benefits**:
- **Substantial Discounts**: Significant cost reductions for predictable, long-term usage patterns
- **Resource Guarantee**: Fixed monthly pricing with guaranteed resource availability during peak demand
- **Budget Predictability**: Stable costs enabling accurate financial planning and budget allocation
- **Production Optimization**: Ideal for continuous training operations, production workloads, and enterprise deployments

---

## Node Status

TIR Nodes operate through distinct status states that reflect their current operational condition and resource allocation status. Understanding these states is crucial for effective resource management and troubleshooting.

**Waiting**: Node is queued for available resources in the selected geographic region. This status typically occurs during high-demand periods or when requesting specialized hardware configurations that may have limited availability. The waiting period ensures optimal resource allocation and fair distribution across users.

**Running**: Node is fully operational and accessible for all development activities. All requested compute resources are allocated, services are active and responsive, and billing charges are in effect. Users can access both Jupyter interfaces and SSH connections with full functionality.

**Stopped**: Node is gracefully shut down with all configurations and data preserved intact. Persistent storage maintains complete data integrity, billing charges are immediately paused, and the node can be quickly restarted without any data loss or configuration changes.

**Pending**: Node is actively transitioning between operational states - either starting up from stopped condition, shutting down from running state, or applying configuration changes. This temporary status indicates ongoing system operations and typically resolves within minutes.

**Expired**: Node has reached its maximum configured runtime limit, encountered a critical system error, or requires manual user intervention to resolve operational issues. This status demands immediate user attention and may indicate resource constraints, configuration problems, or system maintenance requirements.

Understanding these status states enables effective resource utilization optimization, proactive troubleshooting of operational issues, and strategic cost management across development projects.

---

## How to Create Node?

The comprehensive node creation process guides users through detailed configuration while maintaining operational simplicity for rapid deployment of AI development environments.

### Step 1: Initiate Node Creation

![Create Node Interface](https://docs.e2enetworks.com/assets/images/click_create_node-5cdfde38a5974bab42107967b1db8214.png)

The TIR dashboard presents a clean, professional interface with the "Create Node" button strategically positioned for immediate access. This centralized design ensures that creating new development environments is always accessible within one click from the main dashboard.

Click the prominently displayed "Create Node" button to launch the comprehensive configuration wizard that will guide you through selecting optimal settings for your specific AI development requirements.

### Step 2: Container Registry Integration

![Container Registry Configuration](https://docs.e2enetworks.com/assets/images/node_create_container_reg-7187dc5671d9cda2c7bbf059aa6e7fce.png)

The container registry configuration interface enables seamless integration with external container repositories for organizations using custom container images. This interface provides secure authentication management and version control capabilities.

**Registry Integration Features**:
- **Docker Hub Integration**: Direct access to public Docker Hub repositories with automated image pulling
- **Private Registry Support**: Secure connections to organizational container registries with encrypted authentication
- **Authentication Management**: Secure credential storage and automated authentication handling
- **Version Control**: Specific image tag selection ensuring reproducible deployments across team members

For development teams utilizing custom container images, this integration provides seamless access to organizational repositories while maintaining enterprise security standards and deployment consistency.

### Step 3: Advanced Hardware Filtering

![Hardware Filter Interface](https://docs.e2enetworks.com/assets/images/node_create_CPU_filter-aa71d9fe294d2dbf7cd6a3c100c2f7e4.png)

The advanced filtering system enables precise specification of hardware requirements through multiple comprehensive criteria. This interface allows users to narrow down available options based on technical specifications and budget constraints.

**Filtering Capabilities**:
- **CPU Architecture**: Filter by Intel or AMD processor families with specific performance characteristics
- **Memory Requirements**: Set minimum and maximum memory thresholds based on workload demands
- **GPU Specifications**: Define GPU memory requirements and performance levels for AI/ML workloads
- **Budget Constraints**: Apply price range filters to identify cost-effective configurations
- **Geographic Preferences**: Select preferred availability zones for optimal network performance

This granular filtering capability accelerates the selection process by quickly identifying configurations that meet both technical requirements and budgetary constraints.

### Step 4: Startup Script Configuration

![Script Configuration Interface](https://docs.e2enetworks.com/assets/images/nodescript01-d505d96b46b19d431e6cf08608444f5f.png)

The comprehensive script configuration interface provides advanced automation capabilities for environment setup and service initialization. This feature enables complete customization of the development environment during node creation.

**Automation Capabilities**:
- **Environment Preparation**: Automated installation of packages, libraries, and development dependencies
- **Data Pipeline Setup**: Scripted download and preprocessing of datasets, models, and research materials
- **Service Configuration**: Automatic startup of required background services and development applications
- **Custom Initialization**: Implementation of organization-specific configurations, security policies, and development standards

**Example Automation Script**:
```bash
#!/bin/bash
# Install additional Python packages for AI development
pip install transformers datasets accelerate wandb optuna

# Download and configure pre-trained models
huggingface-cli download microsoft/DialoGPT-medium
huggingface-cli download sentence-transformers/all-MiniLM-L6-v2

# Configure environment variables for optimization
export TRANSFORMERS_CACHE=/data/model_cache
export WANDB_PROJECT=tir-ai-development
export CUDA_VISIBLE_DEVICES=0

# Initialize Jupyter with custom extensions and configuration
jupyter lab --generate-config
jupyter labextension install @jupyter-widgets/jupyterlab-manager

# Start services with optimized configurations
jupyter lab --ip=0.0.0.0 --allow-root --no-browser --port=8888
```

Scripts execute automatically during node initialization, creating fully configured, immediately usable development environments without any manual intervention required.

### Step 5: Configuration Summary and Deployment

![Configuration Summary Interface](https://docs.e2enetworks.com/assets/images/node_create_summary_page-1797d59a189b44f565d84063ed62c368.png)

The comprehensive summary interface displays complete configuration details for final review before node deployment. This detailed overview serves both as a verification checkpoint and as documentation for future reference.

**Summary Information Components**:
- **Image Configuration**: Selected base image with version details and optimization specifications
- **Hardware Allocation**: Complete CPU, GPU, and memory specifications with performance expectations
- **Storage Configuration**: Persistent and local storage allocations with capacity and performance details
- **Network Setup**: Access configurations, security group settings, and connectivity specifications
- **Cost Analysis**: Detailed pricing breakdown with hourly and monthly estimates for budget planning
- **Automation Scripts**: Summary of configured startup scripts and initialization procedures

**Deployment Process**: Upon final confirmation, the node creation process initiates with automated resource provisioning, base image deployment, and script execution. The complete deployment process typically requires 3-5 minutes depending on image complexity, script requirements, and current system load.

This final review stage ensures configuration accuracy, provides cost transparency, and creates comprehensive documentation for team reference and organizational compliance requirements.
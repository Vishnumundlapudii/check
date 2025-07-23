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

**Step 1**: Log into your E2E Networks account and navigate to the TIR platform section

**Step 2**: Create or select an existing project within your workspace environment

**Step 3**: Access the Nodes section from the left navigation panel

**Step 4**: Configure your node specifications including image type, hardware resources, and storage requirements

**Step 5**: Review configuration summary and deploy your node

**Step 6**: Access your running node through Jupyter interface or SSH connection

This process typically takes 2-5 minutes from initiation to fully operational node, depending on resource availability and configuration complexity.

---

## Node Images

TIR provides several pre-configured image options to match different development workflows and requirements.

### Base OS Image

![Base OS Selection](https://docs.e2enetworks.com/assets/images/node_create_baseos-7822960dbeed2c236e77da807fe1c30e.png)

The Base OS image provides a minimal foundation with various Linux distributions available. This screenshot shows the operating system selection interface where users can choose from different Ubuntu versions, CentOS, and other distributions. Each option displays the OS version, compatibility information, and recommended use cases.

**Key Features**:
- Multiple Linux distribution options (Ubuntu, CentOS, Debian)
- Latest LTS versions for stability and long-term support
- Minimal installation with essential system packages
- Full customization capability for specialized requirements

This option is ideal for users who need complete control over their environment setup or have specific framework requirements not available in pre-built images.

### Jupyter Image

![Jupyter Environment](https://docs.e2enetworks.com/assets/images/note_book_overview3-ea56bda8301e383531e7162eaf778941.png)

The Jupyter image interface shows a fully configured development environment with JupyterLab running. The screenshot displays the familiar Jupyter interface with file browser, notebook editor, and terminal access all integrated into a single workspace.

**Pre-installed Components**:
- JupyterLab with latest extensions and widgets
- Python data science stack (pandas, numpy, matplotlib, seaborn)
- Machine learning frameworks (TensorFlow, PyTorch, scikit-learn)
- CUDA libraries for GPU acceleration
- Popular visualization libraries (plotly, bokeh)

The interface provides immediate access to a professional data science environment without any setup requirements.

### ComfyUI

ComfyUI offers a visual, node-based interface specifically designed for AI workflow creation and management, particularly useful for generative AI applications.

**Workflow Features**:
- Drag-and-drop node interface for building AI pipelines
- Pre-built nodes for common AI operations (image processing, model inference)
- Support for Stable Diffusion and other generative models
- Real-time preview capabilities
- Custom node creation for specialized workflows

This environment excels for creative professionals and researchers working with generative AI models who prefer visual workflow design over code-based approaches.

### FramePack

FramePack images contain optimized configurations of multiple AI/ML frameworks in a single environment, designed for users who work across different frameworks.

**Integrated Frameworks**:
- TensorFlow with performance optimizations
- PyTorch with CUDA acceleration
- Hugging Face Transformers library
- OpenCV for computer vision tasks
- scikit-learn for traditional ML algorithms

FramePack reduces environment management overhead by providing a comprehensive toolkit ready for diverse AI development tasks.

---

## Node Options

TIR Nodes offer extensive configuration options to customize your development environment according to specific requirements.

### Enable SSH

SSH access provides complete command-line control over your development environment with enterprise-grade security features.

**SSH Configuration**:
- RSA and Ed25519 key support for secure authentication
- Configurable SSH port settings for enhanced security
- Multi-user access capabilities for team environments
- IP filtering and network access restrictions
- Encrypted connections with audit logging

SSH enables advanced system administration tasks, custom software installation, and integration with external development tools and CI/CD pipelines.

### Disk Size

![Storage Configuration](https://docs.e2enetworks.com/assets/images/node_create_node_storage-078d77740cb90960b457a6b3581d607c.png)

The storage configuration interface shows comprehensive options for managing node storage requirements. The screenshot displays different storage tiers, capacity options, and performance characteristics available for TIR Nodes.

**Storage Tiers Available**:
- **Standard Persistent Storage**: Up to 5,000GB with data persistence across node lifecycle
- **High-Performance SSD**: Enhanced performance for frequently accessed datasets and active development
- **30GB Free Workspace**: Automatically included with every node at no additional cost
- **Network Storage**: Shared storage capabilities enabling collaboration across team members

The interface clearly shows pricing for different storage options, allowing users to optimize costs based on their specific data access patterns and performance requirements.

### Local NVME Storage

High-speed local NVME storage provides exceptional performance for data-intensive operations that require maximum throughput and minimal latency.

**Performance Benefits**:
- Ultra-fast read/write speeds for large dataset processing
- Minimal latency for real-time inference applications
- Ideal for model checkpoints and training state management
- Perfect for temporary processing and cache storage

**Important Note**: Local NVME storage is ephemeral and will be lost during node recreation, making it suitable only for temporary, high-performance operations.

### Plan (Pricing)

TIR Nodes support flexible billing models designed to optimize costs across different usage patterns and project requirements.

**Hourly Billing**:
- Immediate billing start when nodes become active
- Automatic cost savings when nodes are stopped
- Perfect for development, experimentation, and variable workloads
- No long-term commitments or minimum usage requirements

**Committed Plans**:
- Substantial discounts for predictable, long-term usage
- Fixed monthly pricing with guaranteed resource availability
- Optimal for production workloads and continuous training operations
- Reserved capacity ensuring availability during peak demand periods

### Node Image Selection

![TIR Pre-built Images](https://docs.e2enetworks.com/assets/images/node_create_tirprebuilt-6fe32f7a774c2d3dadb7f5d167ca1392.png)

The image selection interface displays E2E Networks' curated collection of AI-optimized environments. Each image tile shows the environment name, included frameworks, and optimization details. The screenshot shows various specialized images for different AI/ML workflows including deep learning, data science, and computer vision applications.

**Available Image Categories**:
- **Data Science Images**: Pre-configured with popular data analysis tools
- **Deep Learning Images**: Optimized for neural network training and inference
- **Computer Vision Images**: Specialized for image processing and computer vision tasks
- **NLP Images**: Configured for natural language processing workflows
- **Custom Images**: User-created and shared environments

Each image includes detailed descriptions of pre-installed software, optimization features, and recommended use cases.

### Configuration

![Node Resources Configuration](https://docs.e2enetworks.com/assets/images/node_create_noderesources-2d7398716d0e804ed64f0f5b77bde94f.png)

The hardware configuration interface provides comprehensive control over compute resources with real-time pricing information. The screenshot shows detailed hardware options including CPU specifications, memory configurations, GPU options, and associated costs.

**Hardware Selection Options**:

**CPU Configurations**:
- Standard multi-core processors for general development tasks
- High-performance CPUs with 16+ cores for data processing
- Memory options ranging from 16GB to 256GB based on workload requirements

**GPU Options**:
- **NVIDIA A100**: Premium performance for large model training and fine-tuning
- **NVIDIA V100**: Balanced performance suitable for most AI/ML workloads
- **NVIDIA T4**: Cost-effective option for inference and development environments
- **Multi-GPU configurations**: Scale across multiple GPUs for massive computational requirements

The interface displays real-time pricing for each configuration, enabling informed decisions about performance versus cost trade-offs.

### Advanced Hardware Filtering

![CPU Filter Options](https://docs.e2enetworks.com/assets/images/node_create_CPU_filter-aa71d9fe294d2dbf7cd6a3c100c2f7e4.png)

The advanced filtering interface allows precise specification of hardware requirements through multiple criteria. This screenshot shows the filtering options including CPU architecture preferences, memory ranges, GPU specifications, and budget constraints.

**Filter Categories**:
- **CPU Architecture**: Filter by Intel or AMD processors
- **Memory Range**: Set minimum and maximum memory requirements
- **GPU Memory**: Specify GPU memory requirements for specific workloads
- **Price Range**: Apply budget constraints to narrow options
- **Availability Zone**: Select preferred geographic regions

This granular filtering capability helps users quickly identify optimal configurations that meet both technical and budget requirements.

### Update Node

Node update functionality enables modification of existing configurations without data loss or complete environment rebuilding.

**Update Capabilities**:
- **Resource Scaling**: Dynamically adjust CPU, GPU, and memory allocations
- **Image Updates**: Upgrade to newer framework versions while preserving custom configurations
- **Storage Expansion**: Increase persistent storage capacity as data requirements grow
- **Network Reconfiguration**: Modify security settings and access controls

Updates typically complete within minutes while maintaining all user data, installed packages, and custom configurations.

### Stop Node

Node stopping provides immediate cost control while preserving all configurations and data for future use.

**Stop Process Benefits**:
- **Graceful Shutdown**: Proper shutdown sequence that preserves all work and system state
- **Complete Data Persistence**: All persistent storage and configurations remain intact
- **Immediate Billing Cessation**: Resource charges stop immediately upon shutdown
- **Rapid Restart Capability**: Nodes can be restarted quickly when development resumes

Stopping nodes during idle periods provides significant cost savings while maintaining complete development environment preservation.

### Delete Node

Permanent node removal with complete resource cleanup requires careful consideration of data backup and recovery requirements.

**Deletion Considerations**:
- **Data Backup Verification**: Ensure all critical data is properly backed up before deletion
- **Complete Resource Cleanup**: Removal of all associated compute, storage, and network resources
- **Immediate Cost Cessation**: All billing charges terminate immediately upon deletion
- **Irreversible Action**: Deleted nodes cannot be recovered, making backup essential

---

## Node Status

TIR Nodes operate through distinct status states that reflect their current operational condition and resource allocation status:

**Waiting**: Node is queued for available resources in the selected region. This status typically occurs during high-demand periods or when requesting specialized hardware configurations that may have limited availability.

**Running**: Node is fully operational and accessible for development work. All requested resources are allocated, services are active, and billing is in effect. Users can access both Jupyter interfaces and SSH connections.

**Stopped**: Node is gracefully shut down with all configurations preserved. Persistent storage remains intact, billing is paused, and the node can be quickly restarted without data loss or configuration changes.

**Pending**: Node is transitioning between operational states - either starting up, shutting down, or applying configuration changes. This is a temporary status during operational transitions.

**Expired**: Node has reached its maximum runtime limit, encountered a critical error, or requires manual intervention. This status requires user action to resolve and may indicate resource constraints or configuration issues.

Understanding these status states helps optimize resource utilization, troubleshoot operational issues, and manage costs effectively across development projects.

---

## How to Create Node?

The node creation process provides a comprehensive wizard that guides users through configuration while maintaining simplicity for rapid deployment.

### Step 1: Initiate Node Creation

![Create Node Button](https://docs.e2enetworks.com/assets/images/click_create_node-5cdfde38a5974bab42107967b1db8214.png)

The TIR dashboard displays a clean, organized interface with the "Create Node" button prominently positioned for immediate access. This screenshot shows the main dashboard layout with navigation elements and the primary action button that launches the node creation workflow.

Click the "Create Node" button to access the comprehensive configuration wizard that will guide you through selecting optimal settings for your AI development requirements.

### Step 2: Container Registry Integration

![Container Registry Setup](https://docs.e2enetworks.com/assets/images/node_create_container_reg-7187dc5671d9cda2c7bbf059aa6e7fce.png)

The container registry configuration interface enables integration with external container repositories. This screenshot shows the registry setup form with fields for registry URL, authentication credentials, and image selection options.

**Registry Integration Features**:
- **Docker Hub Integration**: Direct access to public Docker Hub repositories
- **Private Registry Support**: Secure connection to organizational container registries
- **Authentication Management**: Secure credential storage and management
- **Image Version Control**: Specific tag selection for reproducible deployments

For teams using custom container images, this integration provides seamless access to organizational container repositories while maintaining security and version control standards.

### Step 3: Startup Script Configuration

![Startup Scripts](https://docs.e2enetworks.com/assets/images/nodescript01-d505d96b46b19d431e6cf08608444f5f.png)

The script configuration interface provides a comprehensive editor for defining custom initialization automation. This screenshot shows the script editor with syntax highlighting, validation features, and template options for common setup scenarios.

**Script Configuration Capabilities**:
- **Environment Automation**: Automatic installation of packages, libraries, and dependencies
- **Data Pipeline Setup**: Automated download and preparation of datasets and models
- **Service Configuration**: Startup of required background services and applications
- **Custom Initialization**: Implementation of organization-specific configurations and standards

**Example Automation Scripts**:
```bash
#!/bin/bash
# Install additional Python packages
pip install transformers datasets accelerate wandb

# Download pre-trained models
huggingface-cli download microsoft/DialoGPT-medium

# Configure environment variables
export TRANSFORMERS_CACHE=/data/model_cache
export WANDB_PROJECT=my-ai-project

# Start Jupyter with custom configuration
jupyter lab --ip=0.0.0.0 --allow-root --no-browser
```

Scripts execute automatically during node initialization, creating fully configured development environments without manual intervention.

### Step 4: Final Configuration Review

![Configuration Summary](https://docs.e2enetworks.com/assets/images/node_create_summary_page-1797d59a189b44f565d84063ed62c368.png)

The comprehensive summary page displays complete configuration details for final review before node deployment. This screenshot shows the detailed breakdown including selected image, hardware allocation, storage configuration, network settings, and cost estimates.

**Summary Information Includes**:
- **Image Configuration**: Selected base image with version and optimization details
- **Hardware Allocation**: CPU, GPU, and memory specifications with performance expectations
- **Storage Setup**: Persistent and local storage allocation with capacity and performance characteristics
- **Network Configuration**: Access settings, security groups, and connectivity options
- **Cost Analysis**: Detailed pricing breakdown with hourly and monthly estimates
- **Automation Scripts**: Summary of configured startup scripts and initialization procedures

This final review serves both as a configuration verification checkpoint and as documentation for future reference. The detailed cost breakdown enables informed decisions about resource allocation and budget management.

**Deployment Process**: Upon confirmation, the node creation process begins with resource provisioning, image deployment, and script execution. The entire process typically completes within 3-5 minutes, depending on image size and script complexity.

---

**[Document continues with sections 7-9 in the next part...]**
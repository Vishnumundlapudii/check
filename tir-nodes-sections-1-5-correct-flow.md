# TIR Nodes

TIR Nodes are fully collaborative environments that make AI development possible by combining the power of containers, Jupyter Labs, and AI/ML frameworks. These versatile development environments support a wide range of use cases:

- **Fine-tuning Large Language Models**: Optimize and customize LLMs for specific applications with dedicated GPU resources
- **Running Jupyter notebooks**: Interactive development environment with pre-installed data science and AI libraries  
- **Downloading and testing datasets and models**: Efficient data management with high-performance storage options
- **Command-line and SSH configuration options**: Complete terminal access for advanced development workflows

> **Note**: All TIR Nodes include full command-line and SSH access capabilities, enabling both interactive notebook development and traditional server-based workflows.

---

## Getting Started with Nodes on TIR

Creating and accessing TIR Nodes follows a straightforward process designed for both individual developers and enterprise teams. The comprehensive workflow ensures optimal resource allocation while maintaining operational simplicity.

**Complete Development Workflow**:

1. **Account Access**: Log into your E2E Networks account and navigate to the TIR platform section
2. **Project Setup**: Create or select an existing project within your workspace environment  
3. **Node Initiation**: Access the node creation interface through the dashboard
4. **Configuration**: Configure your node specifications including image type, hardware resources, and storage requirements
5. **Review and Deploy**: Review configuration summary and deploy your node
6. **Access Environment**: Access your running node through Jupyter interface or SSH connection

This comprehensive workflow typically takes 2-5 minutes from initiation to fully operational development environment, depending on resource availability and configuration complexity. The streamlined process ensures that developers can focus on AI development rather than infrastructure management.

**Key Benefits**:
- **Rapid Deployment**: Complete environment setup within minutes
- **Enterprise Integration**: Seamless integration with organizational workflows and security policies
- **Cost Optimization**: Flexible billing models that scale with usage patterns
- **Collaborative Features**: Multi-user access and shared resource capabilities

---

## Node Images

TIR provides several pre-configured image options designed to match different development workflows and AI/ML requirements. Each image represents a carefully optimized environment with specific toolchains and frameworks.

### Base OS Image

The Base OS option provides a minimal, clean foundation for users requiring maximum customization flexibility. This approach enables complete control over the development environment setup.

**Customization Advantages**:
- **Complete Control**: Install specific versions of AI/ML frameworks not available in pre-built images
- **Organizational Standards**: Implement company-specific configurations and security requirements
- **Research Flexibility**: Create specialized setups for novel research applications and experimental workflows
- **Legacy Integration**: Support for older or specialized software requirements

**Available Distributions**:
- **Ubuntu LTS Versions**: 20.04, 22.04 with long-term support and stability guarantees
- **CentOS Options**: Enterprise-focused distributions for organizational requirements
- **Debian Variants**: Lightweight options for specialized configurations and minimal resource usage
- **Custom Distributions**: Specialized Linux builds optimized for specific AI/ML requirements

The Base OS approach is ideal for advanced users, research teams, and organizations with specific compliance or customization requirements that cannot be met through pre-built images.

### Jupyter Image

Pre-configured Jupyter environments eliminate setup complexity and provide immediate productivity for data science and AI development workflows.

**Pre-installed Development Stack**:
- **JupyterLab Interface**: Modern, extensible web-based IDE with customizable layouts and advanced features
- **Python Data Science Libraries**: Comprehensive ecosystem including pandas, numpy, scipy, matplotlib, seaborn
- **Machine Learning Frameworks**: TensorFlow, PyTorch, scikit-learn with GPU acceleration and optimization
- **Visualization Tools**: Advanced plotting libraries including plotly, bokeh, altair for interactive data visualization
- **Development Tools**: Integrated Git support, debugger, variable inspector, and automated code formatting

**Environment Features**:
- **Collaborative Development**: Real-time sharing capabilities and integrated version control
- **GPU Acceleration**: CUDA libraries pre-configured for machine learning workloads
- **Extension Ecosystem**: Access to hundreds of JupyterLab extensions for enhanced functionality
- **Notebook Templates**: Pre-built templates for common AI/ML workflows and use cases

The Jupyter environment supports both individual research and team-based development with enterprise-grade collaboration features.

### ComfyUI

ComfyUI provides a revolutionary visual interface for AI workflow design, transforming complex AI operations into intuitive, node-based visual programming environments.

**Visual Workflow Capabilities**:
- **Node-Based Design**: Drag-and-drop interface for building complex AI pipelines without traditional coding
- **Pre-built Components**: Extensive library of nodes for common AI operations including image processing and model inference
- **Generative AI Support**: Native integration with Stable Diffusion, DALL-E, and other generative models
- **Real-time Preview**: Immediate visual feedback during workflow development and iteration
- **Custom Node Development**: Extensible architecture supporting specialized requirements and custom implementations

**Optimal Use Cases**:
- **Creative Professionals**: Digital artists and designers working with AI-generated content
- **Research Teams**: Visual workflow documentation and collaborative AI pipeline development
- **Educational Environments**: Teaching AI concepts through visual, intuitive interfaces
- **Rapid Prototyping**: Quick experimentation with different AI model combinations and parameters

ComfyUI particularly excels for users who prefer visual workflow design over traditional code-based approaches while maintaining professional-grade functionality.

### FramePack

FramePack images provide comprehensive multi-framework environments designed for users requiring access to multiple AI/ML frameworks within a single, optimized development environment.

**Integrated Framework Ecosystem**:
- **TensorFlow Stack**: Complete TensorFlow ecosystem with Keras, TensorBoard, TensorFlow Extended, and distributed training support
- **PyTorch Environment**: PyTorch, torchvision, torchaudio with Lightning integration and distributed training capabilities
- **Hugging Face Integration**: Transformers library with model hub access, pipeline tools, and tokenization utilities
- **Computer Vision Suite**: OpenCV, PIL, scikit-image for comprehensive image processing and computer vision workflows
- **Traditional ML Tools**: scikit-learn, XGBoost, LightGBM for classical machine learning and ensemble methods
- **Research Frameworks**: JAX, Flax for cutting-edge machine learning research and advanced optimization

**Performance Optimizations**:
- **Memory Management**: Advanced memory usage optimization for large model training and inference operations
- **GPU Utilization**: Enhanced GPU utilization algorithms for maximum computational throughput
- **Library Compatibility**: Comprehensive compatibility verification across all framework versions and dependencies
- **Environment Variables**: Pre-configured optimization settings for optimal cross-framework performance
- **Dependency Management**: Automated conflict resolution and version management across multiple frameworks

FramePack environments eliminate the complexity of managing multiple framework installations while providing enterprise-grade performance optimization for production AI development workflows.

---

## Node Options

TIR Nodes offer extensive configuration options to customize your development environment according to specific requirements, performance needs, and organizational standards.

### Enable SSH

SSH access provides complete command-line control over your development environment with enterprise-grade security features and administrative capabilities.

**SSH Configuration Benefits**:
- **Secure Authentication**: Support for RSA and Ed25519 key types with encrypted key storage and management
- **Flexible Access Control**: Configurable SSH port settings and comprehensive IP filtering capabilities
- **Multi-user Support**: Team-based SSH access with individual authentication credentials and permission management
- **Advanced Security**: Network access restrictions, comprehensive audit logging, and security policy enforcement

**Administrative Capabilities**:
- **System Administration**: Complete root access for advanced system configuration and software installation
- **Custom Software**: Installation of specialized tools, libraries, and frameworks not available in pre-built images
- **CI/CD Integration**: Seamless integration with external development tools, deployment pipelines, and automation systems
- **Performance Monitoring**: Access to system-level monitoring tools and performance optimization utilities

SSH access is particularly valuable for teams requiring full system control, organizations with specific security requirements, or advanced users implementing custom development workflows.

### Disk Size

![Storage Configuration Interface](https://docs.e2enetworks.com/assets/images/node_create_node_storage-078d77740cb90960b457a6b3581d607c.png)

The storage configuration interface provides comprehensive options for managing node storage requirements across different performance tiers and capacity options. This interface displays detailed information about storage types, pricing, and performance characteristics.

**Available Storage Tiers**:
- **30GB Free Workspace**: Automatically included with every node at no additional cost for immediate development needs and basic project storage
- **Standard Persistent Storage**: Scalable storage up to 5,000GB with complete data persistence across the entire node lifecycle
- **High-Performance SSD**: Enhanced read/write speeds optimized for frequently accessed datasets and active development workflows
- **Network Storage**: Shared storage capabilities enabling seamless collaboration across team members and projects

**Storage Selection Considerations**:
- **Dataset Size**: Evaluate total storage requirements including raw data, processed datasets, and model artifacts
- **Access Patterns**: Consider frequency of data access and performance requirements for different storage tiers
- **Collaboration Needs**: Assess requirements for shared storage and multi-user access capabilities
- **Cost Optimization**: Balance storage performance requirements with budget constraints and usage patterns

The interface provides transparent pricing information for each storage configuration, enabling informed decisions about storage allocation and cost optimization strategies.

### Local NVME Storage

High-speed local NVME storage delivers exceptional performance for data-intensive operations requiring maximum throughput and minimal latency characteristics.

**Performance Advantages**:
- **Ultra-fast Operations**: Exceptional read/write speeds optimized for large dataset processing and intensive model training workflows
- **Minimal Latency**: Optimal performance for real-time inference applications and interactive development environments
- **High Throughput**: Perfect for model checkpoints, training state management, and temporary high-performance processing
- **Cache Optimization**: Ideal for frequently accessed data requiring immediate availability and rapid processing

**Optimal Use Cases**:
- **Model Training**: High-speed checkpoint storage during intensive training operations
- **Data Preprocessing**: Temporary storage for large-scale data transformation and preprocessing workflows
- **Cache Storage**: Frequently accessed datasets and models requiring minimal access latency
- **Temporary Processing**: High-performance scratch space for computational operations and intermediate results

**Critical Consideration**: Local NVME storage is ephemeral and will be permanently lost during node recreation, shutdown, or termination. This storage type is designed exclusively for temporary, high-performance operations rather than long-term data persistence.

### Plan (Pricing)

TIR Nodes support flexible billing models designed to optimize costs across different usage patterns, project requirements, and organizational budget constraints.

**Hourly Billing Model**:
- **Pay-per-use Structure**: Billing begins immediately when nodes become active and stops when nodes are terminated or stopped
- **Cost Optimization**: Automatic cost savings when nodes are stopped during idle periods or non-working hours
- **Development Friendly**: Perfect for experimentation, testing, variable workloads, and intermittent development activities
- **No Commitments**: Complete flexibility without long-term contracts, minimum usage requirements, or cancellation penalties

**Committed Plan Benefits**:
- **Substantial Discounts**: Significant cost reductions for predictable, long-term usage patterns and continuous operations
- **Resource Guarantee**: Fixed monthly pricing with guaranteed resource availability during peak demand periods
- **Budget Predictability**: Stable, predictable costs enabling accurate financial planning and budget allocation
- **Production Optimization**: Ideal for continuous training operations, production workloads, and enterprise deployments

**Cost Optimization Strategies**:
- **Usage Pattern Analysis**: Monitor actual usage patterns to identify optimal billing model selection
- **Resource Right-sizing**: Match resource allocations to actual computational requirements
- **Scheduled Operations**: Leverage automatic start/stop scheduling for cost-effective resource utilization
- **Team Coordination**: Coordinate resource usage across team members to maximize efficiency and minimize costs

---

## Node Status

TIR Nodes operate through distinct status states that reflect their current operational condition, resource allocation status, and system health. Understanding these states is crucial for effective resource management, troubleshooting, and operational optimization.

**Waiting**: Node is queued for available resources in the selected geographic region and hardware configuration. This status typically occurs during high-demand periods, when requesting specialized hardware configurations with limited availability, or during system maintenance windows. The waiting period ensures optimal resource allocation and fair distribution across all users while maintaining system stability.

**Running**: Node is fully operational and accessible for all development activities. All requested compute resources are allocated and active, services are responsive and available, and billing charges are in effect. Users can access both Jupyter interfaces and SSH connections with complete functionality. This status indicates optimal operational conditions for development work.

**Stopped**: Node is gracefully shut down with all configurations, installed software, and persistent data preserved intact. Persistent storage maintains complete data integrity, billing charges are immediately paused, and the node can be quickly restarted without any data loss or configuration changes. This status provides cost optimization during idle periods while maintaining environment preservation.

**Pending**: Node is actively transitioning between operational states - either starting up from stopped condition, shutting down from running state, applying configuration changes, or processing system updates. This temporary status indicates ongoing system operations and typically resolves within a few minutes depending on the complexity of the transition.

**Expired**: Node has reached its maximum configured runtime limit, encountered a critical system error, or requires manual user intervention to resolve operational issues. This status demands immediate user attention and may indicate resource constraints, configuration problems, system maintenance requirements, or security policy violations requiring resolution.

**Status Management Best Practices**:
- **Proactive Monitoring**: Regularly check node status to identify potential issues before they impact development work
- **Resource Optimization**: Use stopped status during idle periods to optimize costs while preserving development environments
- **Troubleshooting**: Understand status transitions to effectively diagnose and resolve operational issues
- **Cost Management**: Leverage status information for informed decisions about resource allocation and billing optimization

Understanding these status states enables effective resource utilization optimization, proactive troubleshooting of operational issues, and strategic cost management across development projects and team workflows.
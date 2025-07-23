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

TIR Nodes support multiple base image types, each optimized for specific development workflows and use cases.

### Base OS Image

The Base OS option provides a minimal, clean foundation for users requiring maximum customization flexibility. This approach is ideal for:

- **Custom Framework Installation**: Install specific versions of AI/ML frameworks not available in pre-built images
- **Organizational Standards**: Implement company-specific configurations and security requirements
- **Research Environments**: Create specialized setups for novel research applications
- **Legacy System Integration**: Support for older or specialized software requirements

![Base OS Configuration](https://docs.e2enetworks.com/assets/images/node_create_baseos-7822960dbeed2c236e77da807fe1c30e.png)

The interface presents various Linux distributions with detailed version information. Ubuntu LTS versions are recommended for most AI/ML workloads due to their stability and comprehensive package ecosystem.

### Jupyter Image

Pre-configured Jupyter environments eliminate setup complexity and provide immediate productivity for data science workflows.

![Notebook Overview Interface](https://docs.e2enetworks.com/assets/images/note_book_overview3-ea56bda8301e383531e7162eaf778941.png)

**Pre-installed Components**:
- Latest Jupyter Notebook and JupyterLab interfaces
- Comprehensive data science stack (pandas, numpy, scipy, matplotlib)
- Machine learning frameworks (TensorFlow, PyTorch, scikit-learn)
- GPU acceleration libraries with CUDA support
- Visualization tools (plotly, seaborn, bokeh)

The Jupyter environment supports collaborative development with real-time sharing capabilities and integrated version control features.

### ComfyUI

ComfyUI provides a visual, node-based interface for AI workflow design, particularly valuable for creative AI applications and users preferring graphical workflow management.

**Key Features**:
- Drag-and-drop workflow designer
- Support for Stable Diffusion and custom models
- Real-time preview and iteration capabilities
- Export functionality for production deployment

This environment is particularly effective for creative professionals, researchers working with generative models, and teams requiring visual workflow documentation.

### FramePack

FramePack images contain multiple AI/ML frameworks in optimized, production-ready configurations. These environments are specifically tuned for high-performance computing workloads.

**Included Frameworks**:
- Multiple deep learning frameworks with optimized configurations
- High-performance computing libraries and tools
- Production deployment utilities
- Automated dependency management systems

FramePack images reduce setup time for complex multi-framework projects and ensure optimal performance across different AI/ML tools.

---

## Node Options

TIR Nodes provide comprehensive configuration options enabling precise customization for diverse development requirements.

### Enable SSH

SSH access provides complete command-line control over your development environment with enterprise-grade security.

**Configuration Options**:
- **SSH Key Management**: Support for RSA and Ed25519 key types with secure key storage
- **Port Configuration**: Customizable SSH port settings for enhanced security
- **Multi-user Access**: Team-based SSH access with individual authentication
- **Network Security**: Encrypted connections with configurable IP filtering

SSH access enables advanced system administration, custom software installation, and integration with external development tools.

### Disk Size

Storage configuration supports diverse data requirements with flexible capacity and performance options.

![Storage Configuration](https://docs.e2enetworks.com/assets/images/node_create_node_storage-078d77740cb90960b457a6b3581d607c.png)

**Storage Options**:
- **Standard Persistent Storage**: Up to 5,000GB with data persistence across node lifecycle
- **30GB Free Workspace**: Automatically included with every node for immediate development needs
- **High-Performance SSD**: Enhanced performance for frequently accessed datasets
- **Network Storage Integration**: Shared storage capabilities for team collaboration

Storage selection should consider data access patterns, performance requirements, and cost optimization strategies.

### Local NVME Storage

High-speed local storage provides exceptional performance for data-intensive operations requiring maximum throughput.

**Optimal Use Cases**:
- **Model Checkpoints**: Rapid access for training state management and recovery
- **Temporary Processing**: High-speed scratch space for data preprocessing operations
- **Cache Storage**: Frequently accessed data requiring minimal latency
- **Real-time Inference**: Low-latency storage for production inference serving

Local NVME storage is ephemeral and will be lost during node recreation, making it suitable only for temporary, high-performance operations.

### Plan (Pricing)

TIR Nodes offer flexible billing models designed to optimize costs across different usage patterns.

**Hourly Billing**:
- Pay-per-use model with billing starting when nodes are running
- Immediate cost savings when nodes are stopped
- Ideal for development, experimentation, and variable workloads
- No long-term commitments or minimum usage requirements

**Committed Plans**:
- Significant discounts for predictable, long-term usage patterns
- Fixed monthly pricing with guaranteed resource availability
- Optimal for production workloads and continuous training operations
- Reserved capacity ensuring resource availability during peak demand

### Node Image

Image selection determines the software environment and pre-installed tools available in your development environment.

![TIR Pre-built Image Selection](https://docs.e2enetworks.com/assets/images/node_create_tirprebuilt-6fe32f7a774c2d3dadb7f5d167ca1392.png)

The image selection interface displays E2E Networks' curated collection of AI-optimized environments, each configured with specific toolchains and frameworks for particular use cases.

### Configuration

Advanced configuration options enable fine-tuning of node behavior and integration with external systems.

![Node Resources Configuration](https://docs.e2enetworks.com/assets/images/node_create_noderesources-2d7398716d0e804ed64f0f5b77bde94f.png)

**Hardware Configuration**:
- **CPU Selection**: Range from standard multi-core to high-performance processors
- **Memory Allocation**: 16GB to 256GB based on workload requirements
- **GPU Options**: NVIDIA A100, V100, and T4 GPUs with various memory configurations
- **Network Settings**: Custom networking and security group configurations

### Update Node

Node updates enable modification of configurations without data loss or complete rebuilding.

**Update Capabilities**:
- **Resource Scaling**: Modify CPU, GPU, and memory allocations based on changing requirements
- **Image Updates**: Upgrade to newer image versions while preserving custom configurations
- **Storage Expansion**: Increase storage capacity to accommodate growing datasets
- **Network Reconfiguration**: Adjust security settings and access controls

Updates typically complete within minutes and maintain all user data and custom configurations.

### Stop Node

Node stopping provides cost control while preserving all configurations and data for future use.

**Stop Process**:
- **Graceful Shutdown**: Proper shutdown sequence preserving all work and configurations
- **Data Persistence**: All persistent storage and configurations remain intact
- **Immediate Billing Stop**: Resource charges cease immediately upon shutdown
- **Quick Restart**: Nodes can be restarted rapidly when needed

Stopping nodes during idle periods provides significant cost savings while maintaining complete development environment preservation.

### Delete Node

Node deletion permanently removes the node and associated resources, requiring careful consideration of data backup requirements.

**Deletion Process**:
- **Complete Resource Cleanup**: Removal of all associated compute and storage resources
- **Data Backup Verification**: Ensure critical data is backed up before deletion
- **Immediate Billing Cessation**: All charges stop immediately upon deletion
- **Irreversible Action**: Deleted nodes cannot be recovered

---

## Node Status

TIR Nodes operate through distinct status states reflecting their current operational condition:

**Waiting**: Node is queued for available resources in the selected region. This typically occurs during high-demand periods or when requesting specialized hardware configurations.

**Running**: Node is fully operational and accessible for development work. All resources are allocated, services are active, and billing is in effect.

**Stopped**: Node is gracefully shut down with all configurations preserved. Storage remains intact, billing is paused, and the node can be quickly restarted.

**Pending**: Node is transitioning between states - either starting up, shutting down, or applying configuration changes. This is a temporary status during operational transitions.

**Expired**: Node has reached its maximum runtime limit, encountered a critical error, or requires manual intervention. This status requires user action to resolve.

Understanding these states helps optimize resource utilization and troubleshoot operational issues effectively.

---

## How to Create Node?

The node creation process guides users through comprehensive configuration while maintaining simplicity for quick deployment.

### Step 1: Initiate Creation

![Create Node Button](https://docs.e2enetworks.com/assets/images/click_create_node-5cdfde38a5974bab42107967b1db8214.png)

Access the node creation interface through the prominently displayed "Create Node" button in the TIR dashboard. This centralized approach ensures immediate access to node provisioning capabilities.

### Step 2: Advanced Filtering

![CPU Filtering Interface](https://docs.e2enetworks.com/assets/images/node_create_CPU_filter-aa71d9fe294d2dbf7cd6a3c100c2f7e4.png)

The advanced filtering system enables precise specification of requirements through multiple criteria including CPU architecture, memory ranges, GPU specifications, and budget constraints. This granular control helps identify optimal configurations quickly.

### Step 3: Container Registry Integration

![Container Registry Configuration](https://docs.e2enetworks.com/assets/images/node_create_container_reg-7187dc5671d9cda2c7bbf059aa6e7fce.png)

For teams using custom container images, the registry integration supports Docker Hub, private registries, and organizational repositories with secure authentication and version management.

### Step 4: Script Configuration

![Startup Script Configuration](https://docs.e2enetworks.com/assets/images/nodescript01-d505d96b46b19d431e6cf08608444f5f.png)

Startup script configuration enables complete automation of environment setup, including package installation, data download, and service configuration. Scripts execute during node initialization, creating immediately usable development environments.

### Step 5: Configuration Review

![Node Creation Summary](https://docs.e2enetworks.com/assets/images/node_create_summary_page-1797d59a189b44f565d84063ed62c368.png)

The comprehensive summary page displays complete configuration details including cost estimates, resource allocations, and startup automation. This final review ensures accuracy before deployment and serves as configuration documentation.

---

## Node Details

The node details interface provides comprehensive oversight and management capabilities for active development environments.

### Overview

![Node Management Interface](https://docs.e2enetworks.com/assets/images/Manage_Node_details-01f7278114b48534eee10f6a5a9a5afa.png)

The overview section presents essential node information including current status, resource utilization, network configuration, and quick access to management functions. This centralized view enables efficient monitoring and control of development environments.

**Key Information Displayed**:
- Real-time node status and health indicators
- Current resource utilization metrics
- Network connectivity and access information
- Cost tracking and billing status
- Quick action buttons for common operations

### Node Events

![Notebook Events](https://docs.e2enetworks.com/assets/images/notebook_event-29d16446a072d817fbebd5ab52221b6d.png)

The event monitoring system provides detailed logging of all node activities including startup events, user actions, system messages, and resource utilization changes.

**Event Categories**:
- **System Events**: Node lifecycle operations and configuration changes
- **User Activities**: Access patterns, file operations, and development activities
- **Resource Events**: Utilization alerts and performance notifications
- **Security Events**: Authentication, access control, and security-related activities

Event logs enable troubleshooting, performance optimization, and security auditing for professional development environments.

### Monitoring

Comprehensive monitoring capabilities provide visibility into node performance and resource utilization patterns.

**Monitoring Features**:
- **Real-time Metrics**: CPU, GPU, memory, and storage utilization
- **Historical Analysis**: Performance trends and usage patterns over time
- **Alert Configuration**: Automated notifications for resource thresholds
- **Optimization Recommendations**: Suggestions for resource efficiency improvements

### Workspace Size

**Default Configuration**: Every TIR Node includes a 30GB free workspace providing immediate storage for development activities without additional cost.

**Workspace Utilization**:
- Code repositories and development files
- Sample datasets and experimental data
- Model checkpoints and training results
- Temporary processing files and development logs

The free workspace is automatically mounted and accessible from both Jupyter and SSH environments, providing immediate productivity without configuration overhead.

### Associated Datasets

Dataset integration capabilities enable efficient data management and sharing across development workflows.

**Dataset Features**:
- **Direct Integration**: Seamless access to datasets stored in E2E Networks object storage
- **Version Management**: Dataset versioning and change tracking capabilities
- **Team Sharing**: Shared dataset access across team members and projects
- **Access Control**: Granular permissions for dataset security and compliance

### Associated File System

File system integration provides flexible storage options and data management capabilities.

**File System Features**:
- **Network File System**: Shared storage across multiple nodes and users
- **Backup Integration**: Automated backup and recovery capabilities
- **Performance Optimization**: Intelligent caching and access optimization
- **Security Controls**: Encryption and access control for sensitive data

### Network & Security

Network and security configurations ensure secure, compliant development environments.

**Security Features**:
- **Encrypted Connections**: All data transfer uses encrypted protocols
- **Access Control**: IP filtering and network access restrictions
- **Audit Logging**: Comprehensive access and activity logging
- **Compliance Support**: Features supporting various regulatory requirements

### Start Script

![Advanced Notebook Features](https://docs.e2enetworks.com/assets/images/Notebook8-d51412332b0237121acbd3f984fed64a.png)

Start script functionality enables comprehensive automation of environment preparation and service initialization.

**Script Capabilities**:
- **Environment Setup**: Automated installation of packages and dependencies
- **Data Preparation**: Download and preprocessing of datasets and models
- **Service Configuration**: Startup of required services and applications
- **Custom Initialization**: Implementation of organization-specific configurations

Scripts support complex automation scenarios and enable reproducible environment creation across team members and projects.

---

## Node Actions

Node actions provide comprehensive lifecycle management and operational control over development environments.

### Launch Notebook

Direct access to Jupyter environments with automatic authentication and session management eliminates manual configuration overhead.

**Launch Features**:
- **One-click Access**: Immediate connection to pre-configured Jupyter environment
- **Automatic Authentication**: Seamless security integration without manual login
- **Session Management**: Persistent sessions with automatic recovery capabilities
- **Multi-tab Support**: Concurrent access to multiple notebooks and development resources

### Stop Node

Graceful node shutdown preserves all data and configurations while providing immediate cost savings.

**Stop Process Benefits**:
- **Data Preservation**: All persistent storage and configurations remain intact
- **Cost Control**: Resource billing stops immediately upon shutdown
- **Quick Recovery**: Rapid restart capabilities when development resumes
- **State Maintenance**: All installed packages and customizations preserved

### Restart Node

Node restart functionality enables quick recovery from issues while maintaining all configurations and data.

**Restart Capabilities**:
- **Configuration Preservation**: All settings and customizations maintained
- **Data Integrity**: No data loss during restart operations
- **Service Recovery**: Automatic restoration of all running services
- **Troubleshooting**: Effective resolution of temporary system issues

### Update Image

Image updates enable access to newer software versions while preserving custom configurations and development work.

**Update Features**:
- **Version Advancement**: Access to latest framework versions and security updates
- **Configuration Preservation**: Custom settings and installed packages maintained
- **Data Integrity**: All user data and projects preserved during updates
- **Rollback Capability**: Option to revert to previous versions if needed

### Update Plan

Plan updates enable dynamic resource adjustment based on changing requirements without data loss or configuration changes.

**Update Options**:
- **Resource Scaling**: Modify CPU, GPU, and memory allocations
- **Storage Expansion**: Increase persistent storage capacity
- **Billing Model Changes**: Switch between hourly and committed pricing
- **Performance Optimization**: Adjust resources based on utilization patterns

### Convert to Committed

Conversion to committed plans provides significant cost savings for predictable, long-term usage patterns.

**Conversion Benefits**:
- **Cost Reduction**: Substantial discounts compared to hourly billing
- **Resource Guarantee**: Reserved capacity ensuring availability
- **Budget Predictability**: Fixed monthly costs for financial planning
- **Priority Access**: Guaranteed resource allocation during high-demand periods

### Save Image

Custom image creation enables environment standardization and rapid deployment of configured development environments.

**Save Image Features**:
- **Environment Capture**: Complete snapshot of current system configuration
- **Team Sharing**: Distribution of standardized environments across team members
- **Version Control**: Multiple image versions for different project requirements
- **Rapid Deployment**: Quick provisioning of identical development environments

### Delete Node

Permanent node removal with complete resource cleanup requires careful consideration of data backup and recovery requirements.

**Deletion Considerations**:
- **Data Backup**: Verification of critical data preservation before deletion
- **Resource Cleanup**: Complete removal of all associated compute and storage resources
- **Cost Cessation**: Immediate termination of all billing charges
- **Irreversible Action**: Permanent removal with no recovery options

---

## Launch Node from Sidebar

The sidebar launch functionality provides streamlined access to node creation and management capabilities.

### Advance Filter on Node

Advanced filtering capabilities enable precise node selection and management across large-scale deployments.

**Filter Categories**:
- **Status Filtering**: Select nodes based on operational status
- **Resource Filtering**: Find nodes by CPU, GPU, or memory specifications
- **Cost Filtering**: Identify nodes based on billing models or cost thresholds
- **Usage Filtering**: Locate nodes by utilization patterns or team assignment
- **Custom Tags**: Organization-specific labeling and categorization

**Filter Applications**:
- **Resource Optimization**: Identify underutilized resources for cost reduction
- **Capacity Planning**: Analyze resource usage patterns for scaling decisions
- **Team Management**: Organize nodes by team, project, or department
- **Cost Management**: Track expenses and optimize resource allocation

Advanced filtering supports enterprise-scale node management and enables data-driven optimization of AI development infrastructure.

---

## Advanced Configuration Areas

The following sections require additional screenshots from the original documentation. Each represents a crucial aspect of TIR Node functionality:

### **[PLACEHOLDER: Additional Node Image Types]**
*Multiple screenshots showing specialized pre-built images for different AI frameworks*

The expanded image gallery includes specialized environments for computer vision, natural language processing, reinforcement learning, and domain-specific applications. Each image represents hundreds of hours of optimization work, providing instantly usable environments for specific AI domains.

### **[PLACEHOLDER: Detailed Hardware Configuration Options]**  
*Screenshots of advanced GPU selection interfaces, memory configuration panels, and CPU variants*

Hardware selection interfaces provide detailed specifications for each option, including benchmark performance data, power consumption characteristics, and optimal use case recommendations. This information enables data-driven hardware selection decisions.

### **[PLACEHOLDER: Advanced Storage Management]**
*Screenshots showing storage tier selection, backup configuration, and performance optimization*

Storage management interfaces provide granular control over data lifecycle, backup policies, and performance optimization strategies essential for large-scale AI development projects.

### **[PLACEHOLDER: Team Management and Collaboration]**
*Screenshots of user management interfaces, role-based access controls, and collaborative workspace features*

Multi-user environments require sophisticated permission management. The interface provides role-based access control, resource quota management, and collaborative workspace organization features essential for team-based AI development.

### **[PLACEHOLDER: Advanced Monitoring and Analytics]**
*Screenshots of detailed performance dashboards, usage analytics, and optimization recommendations*

Performance monitoring goes beyond basic resource utilization to include AI-specific metrics like training throughput, model inference performance, and data pipeline efficiency. These insights enable continuous optimization of development workflows.

---

## Best Practices and Optimization

### Resource Management Excellence

Effective TIR Node utilization requires systematic approaches to resource allocation, cost optimization, and performance management.

**Strategic Resource Planning**:
- **Workload Analysis**: Match resource specifications to actual computational requirements
- **Cost-Performance Optimization**: Balance performance needs with budget constraints
- **Scalability Planning**: Design node configurations for future growth and changing requirements
- **Team Coordination**: Coordinate resource usage across multiple team members and projects

### Security and Compliance Framework

Enterprise AI development requires comprehensive security measures supporting both productivity and regulatory compliance.

**Security Implementation**:
- **Access Control Strategy**: Implement principle of least privilege with role-based permissions
- **Data Protection**: Ensure encryption, backup, and secure data handling procedures
- **Audit and Monitoring**: Maintain detailed logs for compliance and security analysis
- **Network Security**: Configure appropriate firewall rules and network isolation

### Development Workflow Integration

**Environment Standardization**: Establish team standards for node configurations reducing setup complexity and ensuring consistency.

**Version Control Integration**: Implement proper code management through Git integration and automated backup procedures.

**Continuous Integration Support**: Enable automated testing and deployment pipeline integration for professional development workflows.

**Collaboration Optimization**: Leverage shared resources and collaborative features for enhanced team productivity.

---

## Conclusion

TIR Nodes provide comprehensive, enterprise-grade infrastructure for AI development that combines powerful hardware options, optimized software environments, and sophisticated management capabilities. This platform enables teams to focus on innovation and model development rather than infrastructure complexity.

The extensive configuration options, from basic development environments to high-performance training configurations, support diverse AI development requirements while maintaining cost efficiency and operational simplicity.

Professional features including advanced monitoring, security controls, collaborative capabilities, and enterprise integration make TIR Nodes suitable for both individual research and large-scale organizational AI development initiatives.

Whether conducting exploratory research, developing production applications, or training large-scale models, TIR Nodes provide the robust, flexible foundation necessary for success in today's competitive AI development landscape.
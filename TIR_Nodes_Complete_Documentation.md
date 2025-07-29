# TIR Nodes - Complete Documentation

## TIR Nodes Overview

### Introduction to TIR Nodes

TIR Nodes are collaborative AI development environments designed to streamline the development, testing, and deployment of artificial intelligence (AI) and machine learning (ML) models. As a core component of the E2E Networks TIR platform, TIR Nodes provide a comprehensive set of tools and features that enable developers, data scientists, and AI researchers to work efficiently and effectively.

![TIR Nodes Dashboard Overview](images/manage_nodes.png)
*Figure 1: TIR Nodes dashboard showing node management interface with status indicators, resource allocation, and available actions.*

### Key Features and Benefits

TIR Nodes offer the following key features and benefits:

* **Pre-configured Environments**: Get started quickly with pre-configured environments for AI/ML development, eliminating the need for manual setup and configuration.
* **Multiple Image Types**: Choose from a variety of image types, including:
  + Base OS: A minimal, customizable environment for building from scratch.
  + Jupyter: A web-based interactive environment for data science and ML development.
  + ComfyUI: A user-friendly interface for managing and deploying AI/ML models.
  + FramePack: A specialized environment for computer vision and graphics applications.
* **Scalable Compute Resources**: Scale up or down as needed with flexible CPU and GPU options, ensuring optimal performance for demanding AI/ML workloads.
* **SSH Access and Workspace Management**: Securely access and manage your workspace with SSH access, ensuring seamless collaboration and version control.
* **Free Tier Availability**: Get started with a free tier, and upgrade as needed to accommodate growing project requirements.

### Common Use Cases

TIR Nodes are ideal for a variety of use cases, including:

* **AI/ML Model Development**: Develop, test, and deploy AI/ML models with ease, using pre-configured environments and scalable compute resources.
* **Data Science**: Collaborate on data science projects, using Jupyter and other tools to explore, visualize, and analyze data.
* **Computer Vision**: Leverage FramePack and GPU acceleration to develop and deploy computer vision applications.
* **Research and Development**: Use TIR Nodes as a sandbox for exploring new AI/ML techniques, algorithms, and tools.

### Technical Specifications

* **Compute Resources**: CPU and GPU options, with scalable configurations to accommodate demanding workloads.
* **Storage**: Persistent storage options for data and model artifacts.
* **Networking**: Secure, high-performance networking for collaboration and data transfer.

---

## Getting Started with TIR Nodes

### Step 1: Log in with myaccount Credentials

1. Open a web browser and navigate to the TIR platform login page.
2. In the **Login** form, enter your **Username** and **Password** associated with your myaccount credentials.
3. Click the **Login** button, located below the form fields.

**Troubleshooting Tip:** If you encounter issues logging in, ensure that your username and password are correct. You can reset your password by clicking the **Forgot Password** link below the login form.

![Login Page](images/login_placeholder.png)
*Figure 2: E2E Networks login page - Enter your myaccount credentials to access the TIR platform.*

### Step 2: Create a Project in Private Workspace

1. After logging in, click the **Create Project** button, located in the top-right corner of the dashboard.
2. In the **Create Project** dialog, enter a unique **Project Name** and optional **Project Description**.
3. Select **Private Workspace** as the project type.
4. Click the **Create** button to create the project.

**Helpful Tip:** Choose a descriptive project name to easily identify your project in the dashboard.

![Create Project Dialog](images/project_creation_placeholder.png)
*Figure 3: Create Project dialog - Set up your private workspace with a descriptive project name.*

### Step 3: Navigate to "Nodes" Section

1. In the left sidebar, click the **Nodes** tab, located below the **Project** tab.
2. The **Nodes** page will display a list of existing nodes. Click the **Create Node** button to proceed.

**UI Element Description:** The left sidebar is divided into sections, with the **Nodes** tab located below the **Project** tab. The **Create Node** button is displayed in the top-right corner of the **Nodes** page.

![Nodes Page](images/create_node_button.png)
*Figure 4: Nodes section in left sidebar - Click the "Create Node" button to start the node creation process.*

### Step 4: Select Node Image Type

1. In the **Create Node** dialog, select the desired **Node Image Type** from the dropdown menu.
2. Choose from a variety of node image types, including **Ubuntu**, **CentOS**, and **Windows**.

**Helpful Tip:** Select a node image type that matches your project requirements.

![Node Image Selection](images/node_image_selection.png)
*Figure 5: Node image selection interface showing different available image types for your development environment.*

### Step 5: Choose CPU/GPU Plan

1. Select a **CPU** or **GPU** plan based on your project requirements.
2. Choose from a range of plans, including **Free Tier**, **Basic**, and **Advanced**.
3. Review the plan details, including **vCPUs**, **Memory**, and **Storage**.

**Plan Selection Guidance:** The **Free Tier** plan is suitable for small projects and development environments. For larger projects, consider the **Basic** or **Advanced** plans.

![CPU/GPU Plan Selection](images/node_resources.png)
*Figure 6: Resource plan selection showing CPU and GPU options with pricing tiers and specifications.*

### Step 6: Configure Optional Settings

1. Configure optional settings, including **SSH** key pairs and **Disk Size**.
2. Enter a **Node Name** and optional **Node Description**.
3. Review the node configuration summary.

**Helpful Tip:** Ensure that your SSH key pair is correctly configured to access your node.

![Node Configuration](images/node_storage.png)
*Figure 7: Node configuration panel for setting SSH access, disk size, and other optional parameters.*

### Step 7: Launch the Node

1. Review the node configuration summary and click the **Launch** button.
2. The node will be created and launched, and its status will be displayed on the **Nodes** page.

**Troubleshooting Tip:** If the node launch fails, check the node configuration and ensure that all required settings are correctly configured.

![Node Summary and Launch](images/node_summary.png)
*Figure 8: Final node configuration summary before launching your TIR node environment.*

---

## Node Image Types

### Overview

Our platform offers four primary node image types, each designed to cater to specific use cases and workflows. This documentation provides a comprehensive overview of each image type, including their purpose, technical specifications, pre-installed software, and ideal use cases.

![Node Image Types Overview](images/node_image_selection.png)
*Figure 9: Node image type selection showing the four main categories: Base OS, Jupyter, ComfyUI, and FramePack.*

### 1. Base OS Image

#### Purpose and Use Cases

The Base OS Image provides a clean Ubuntu/Linux environment, ideal for custom setups and users who want to configure their node from scratch. This image type is suitable for:

* Custom software installations
* Specific version requirements
* Advanced users who require fine-grained control over their environment

#### Technical Specifications

* Operating System: Ubuntu/Linux (latest LTS version)
* Pre-installed Software: Minimal package set, including:
  + Ubuntu/Linux base packages
  + SSH server
  + Basic system utilities
* Customization Options: Users can install any software package or library, providing complete control over the environment.

![Base OS Image](images/base_os_selection.png)
*Figure 10: Base OS image selection providing a clean Ubuntu/Linux environment for custom configurations.*

#### Comparison

The Base OS Image is the most lightweight and flexible option, making it ideal for users who require a high degree of customization. However, it may require more setup and configuration time compared to other image types.

### 2. Jupyter Image

#### Purpose and Use Cases

The Jupyter Image is a pre-configured Jupyter notebook environment, designed for data science and scientific computing workflows. This image type is suitable for:

* Data analysis and visualization
* Machine learning model development
* Scientific computing and simulations

#### Technical Specifications

* Operating System: Ubuntu/Linux (latest LTS version)
* Pre-installed Software:
  + Jupyter Notebook (latest version)
  + Data science libraries (e.g., NumPy, pandas, scikit-learn)
  + Visualization tools (e.g., Matplotlib, Seaborn)
  + Support for various kernels (e.g., Python, R, Julia)
* Customization Options: Users can install additional libraries and kernels, and configure Jupyter Notebook settings.

![Jupyter Environment](images/jupyter_placeholder.png)
*Figure 11: Jupyter notebook environment pre-configured with data science libraries and visualization tools.*

#### Comparison

The Jupyter Image provides a convenient and productive environment for data science and scientific computing tasks. While it's more comprehensive than the Base OS Image, it's less specialized than the ComfyUI Image.

### 3. ComfyUI Image

#### Purpose and Use Cases

The ComfyUI Image is specifically designed for Stable Diffusion and AI art generation workflows. This image type is suitable for:

* AI-powered art generation
* Stable Diffusion model development
* Creative applications and prototyping

#### Technical Specifications

* Operating System: Ubuntu/Linux (latest LTS version)
* Pre-installed Software:
  + Stable Diffusion (latest version)
  + AI art generation tools (e.g., Deep Dream Generator)
  + Support for various models and frameworks (e.g., PyTorch, TensorFlow)
* Customization Options: Users can install additional models and frameworks, and configure ComfyUI settings.

![ComfyUI Environment](images/comfyui_placeholder.png)
*Figure 12: ComfyUI interface specialized for Stable Diffusion and AI art generation workflows.*

#### Comparison

The ComfyUI Image is a specialized option, providing a streamlined environment for AI art generation and Stable Diffusion workflows. While it's more comprehensive than the Jupyter Image, it's less flexible than the Base OS Image.

### 4. FramePack Image

#### Purpose and Use Cases

The FramePack Image is pre-configured with popular machine learning frameworks, making it ideal for ML development and deployment workflows. This image type is suitable for:

* Machine learning model development
* Model deployment and serving
* Deep learning applications

#### Technical Specifications

* Operating System: Ubuntu/Linux (latest LTS version)
* Pre-installed Software:
  + TensorFlow (latest version)
  + PyTorch (latest version)
  + Support for various frameworks and libraries (e.g., Keras, OpenCV)
* Customization Options: Users can install additional frameworks and libraries, and configure FramePack settings.

![FramePack Environment](images/framepack_placeholder.png)
*Figure 13: FramePack image with pre-installed ML frameworks including TensorFlow and PyTorch.*

#### Comparison

The FramePack Image provides a comprehensive environment for machine learning and deep learning tasks. While it's more specialized than the Jupyter Image, it's less comprehensive than the ComfyUI Image.

### Choosing the Right Image Type

When selecting a node image type, consider the following factors:

* **Customization requirements**: If you need fine-grained control over your environment, choose the Base OS Image. For more comprehensive environments, consider the Jupyter, ComfyUI, or FramePack Images.
* **Specific software requirements**: If you require specific software packages or libraries, choose the image type that best aligns with your needs.
* **Workflow and use case**: Select the image type that's optimized for your workflow, such as the ComfyUI Image for AI art generation or the FramePack Image for machine learning development.

---

## Node Configuration Options

### Overview

When creating nodes, several configuration options are available to customize the node to suit your specific needs. This document provides detailed explanations of each configuration option, including default values, recommendations, and impact on pricing.

![Node Configuration Options](images/node_details.png)
*Figure 14: Detailed node configuration panel showing SSH, storage, networking, and security options.*

### SSH Enablement for Command-Line Access

* **Parameter:** `ssh_enabled`
* **Default Value:** `false`
* **Range:** `true` or `false`
* **Description:** Enables or disables SSH access to the node for command-line access.
* **Recommendation:** Enable SSH access if you need to access the node for troubleshooting, maintenance, or automation purposes.
* **Best Practice:** Use SSH keys for authentication instead of passwords for enhanced security.

### Disk Size Configuration

* **Parameter:** `disk_size`
* **Default Value:** `50` GB
* **Range:** `10` GB to `5000` GB
* **Description:** Configures the disk size of the node.
* **Recommendation:** Choose a disk size that is sufficient for your application's storage needs. Larger disk sizes may impact pricing.
* **Best Practice:** Use a disk size that is a multiple of 10 GB to ensure optimal storage allocation.

### Local NVME Storage Options

* **Parameter:** `nvme_storage`
* **Default Value:** `false`
* **Range:** `true` or `false`
* **Description:** Enables or disables local NVME storage on the node.
* **Recommendation:** Enable local NVME storage if you need high-performance storage for your application.
* **Best Practice:** Use local NVME storage for applications that require low-latency storage access.

### Pricing Plan Selection

* **Parameter:** `pricing_plan`
* **Default Value:** `free`
* **Range:** `free`, `basic`, `premium`, `high-performance`
* **Description:** Selects the pricing plan for the node.
* **Recommendation:** Choose a pricing plan that aligns with your application's performance and storage needs.
* **Best Practice:** Start with a lower-tier pricing plan and upgrade as needed to optimize costs.

### Hardware Configuration

* **Parameter:** `hardware_config`
* **Default Value:** `{cpu: 2, ram: 4, gpu: none}`
* **Range:**
  * `cpu`: `1` to `32` cores
  * `ram`: `2` GB to `256` GB
  * `gpu`: `none`, `nvidia`, `amd`
* **Description:** Configures the hardware settings for the node, including CPU cores, RAM, and GPU type.
* **Recommendation:** Choose hardware settings that are suitable for your application's performance requirements.
* **Best Practice:** Use a balanced hardware configuration that optimizes CPU, RAM, and GPU resources.

### Network and Security Settings

* **Parameter:** `network_config`
* **Default Value:** `{security_group: default, firewall_rules: []}`
* **Range:**
  * `security_group`: `default`, `custom`
  * `firewall_rules`: array of firewall rules
* **Description:** Configures the network and security settings for the node, including security groups and firewall rules.
* **Recommendation:** Use a custom security group and configure firewall rules to restrict incoming traffic to the node.
* **Best Practice:** Use a least-privilege approach when configuring network and security settings.

### Auto-Stop and Scheduling Options

* **Parameter:** `auto_stop`
* **Default Value:** `false`
* **Range:** `true` or `false`
* **Description:** Enables or disables auto-stop for the node.
* **Recommendation:** Enable auto-stop if you want to automatically stop the node after a period of inactivity.
* **Best Practice:** Use auto-stop to optimize costs and reduce resource waste.

### Example Configuration

Here is an example node configuration that demonstrates the use of the above options:

```json
{
  "ssh_enabled": true,
  "disk_size": 100,
  "nvme_storage": true,
  "pricing_plan": "premium",
  "hardware_config": {
    "cpu": 4,
    "ram": 16,
    "gpu": "nvidia"
  },
  "network_config": {
    "security_group": "custom",
    "firewall_rules": [
      {
        "protocol": "tcp",
        "port": 22
      }
    ]
  },
  "auto_stop": true
}
```

This configuration enables SSH access, sets the disk size to 100 GB, enables local NVME storage, selects the premium pricing plan, configures the hardware settings, sets up a custom security group with a firewall rule, and enables auto-stop.

---

## Node Status Types and Transitions

### Overview

This document provides a comprehensive guide to node status types, their meanings, and the transitions between them. It also offers troubleshooting tips, monitoring and debugging advice, and explains the actions available in each state.

![Node Status Overview](images/manage_nodes.png)
*Figure 15: Node status dashboard displaying different node states including Waiting, Running, Stopped, Pending, and Expired.*

### Node Status Types

#### Waiting

* **Definition:** A node is in the Waiting state when it is queued for resources, such as CPU, memory, or network bandwidth.
* **Trigger:** A node enters the Waiting state when a request is made to create or start a node, but the required resources are not available.
* **Actions:**
  + Monitor resource availability and adjust resource allocation as needed.
  + Cancel the node request if resources are not available within a reasonable time frame.
* **Troubleshooting:**
  + Check resource utilization and adjust resource allocation policies.
  + Verify that the node request is valid and correctly configured.
* **Monitoring and Debugging:**
  + Monitor resource utilization metrics, such as CPU usage, memory usage, and network bandwidth.
  + Check node logs for errors or warnings related to resource allocation.

#### Running

* **Definition:** A node is in the Running state when it is active and accessible, with all required resources allocated.
* **Trigger:** A node enters the Running state when resources are allocated and the node is started successfully.
* **Actions:**
  + Monitor node performance and adjust resource allocation as needed.
  + Stop or restart the node as needed.
* **Troubleshooting:**
  + Check node logs for errors or warnings related to node performance.
  + Verify that the node is correctly configured and functioning as expected.
* **Monitoring and Debugging:**
  + Monitor node performance metrics, such as response time, throughput, and error rate.
  + Check node logs for errors or warnings related to node performance.

#### Stopped

* **Definition:** A node is in the Stopped state when it is paused, and resources are released.
* **Trigger:** A node enters the Stopped state when it is stopped manually or due to an error.
* **Actions:**
  + Start the node again when resources are available.
  + Delete the node if it is no longer needed.
* **Troubleshooting:**
  + Check node logs for errors or warnings related to node shutdown.
  + Verify that the node was stopped correctly and resources were released.
* **Monitoring and Debugging:**
  + Monitor node logs for errors or warnings related to node shutdown.
  + Check resource utilization metrics to ensure resources were released correctly.

#### Pending

* **Definition:** A node is in the Pending state when it is being initialized, and resources are being allocated.
* **Trigger:** A node enters the Pending state when a request is made to create or start a node, and resources are being allocated.
* **Actions:**
  + Monitor resource allocation and adjust as needed.
  + Cancel the node request if resources are not allocated within a reasonable time frame.
* **Troubleshooting:**
  + Check resource utilization and adjust resource allocation policies.
  + Verify that the node request is valid and correctly configured.
* **Monitoring and Debugging:**
  + Monitor resource utilization metrics, such as CPU usage, memory usage, and network bandwidth.
  + Check node logs for errors or warnings related to resource allocation.

#### Expired

* **Definition:** A node is in the Expired state when it has reached time or usage limits, and resources are released.
* **Trigger:** A node enters the Expired state when time or usage limits are reached.
* **Actions:**
  + Delete the node if it is no longer needed.
  + Extend time or usage limits if needed.
* **Troubleshooting:**
  + Check node logs for errors or warnings related to time or usage limits.
  + Verify that time or usage limits were correctly configured.
* **Monitoring and Debugging:**
  + Monitor node logs for errors or warnings related to time or usage limits.
  + Check resource utilization metrics to ensure resources were released correctly.

### Status Transitions

The following diagram illustrates the possible status transitions:

```
          +---------------+
          |  Pending    |
          +---------------+
                  |
                  |  Resources allocated
                  v
          +---------------+
          |  Running    |
          +---------------+
                  |
                  |  Stop request or error
                  v
          +---------------+
          |  Stopped    |
          +---------------+
                  |
                  |  Start request
                  v
          +---------------+
          |  Running    |
          +---------------+
                  |
                  |  Time or usage limits reached
                  v
          +---------------+
          |  Expired    |
          +---------------+
                  |
                  |  Delete request
                  v
          +---------------+
          |  Deleted    |
          +---------------+
                  |
                  |  Resource allocation failed
                  v
          +---------------+
          |  Waiting    |
          +---------------+
```

### Monitoring and Managing Node Lifecycle

To effectively monitor and manage node lifecycle, it is recommended to:

* Monitor node performance and resource utilization metrics.
* Set up alerts for node status changes, such as node failure or expiration.
* Regularly review node logs for errors or warnings.
* Adjust resource allocation policies as needed.
* Extend time or usage limits as needed.

By following these guidelines, you can ensure that your nodes are running efficiently and effectively, and that any issues are quickly identified and resolved.

---

## Summary

This complete documentation provides a professional hybrid approach to TIR Nodes documentation, combining:

- **Rich text content** generated by E2E Llama 3.1 70B for SEO and RAG optimization
- **Screenshot placeholders** to maintain visual guidance
- **Structured headings** for better navigation and search engine optimization
- **Technical specifications** and configuration details
- **Troubleshooting guides** and best practices
- **Code examples** and configuration snippets

The documentation is now:
- ✅ **RAG-friendly** with searchable text content
- ✅ **SEO-optimized** with proper headings and structure
- ✅ **Professional** with detailed explanations and examples
- ✅ **Hybrid approach** combining screenshots with rich text
- ✅ **Generated using E2E Llama 3.1 70B** for high-quality content
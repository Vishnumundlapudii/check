# E2E Networks TIR Nodes - Complete User Guide

**Source:** [E2E Networks TIR Documentation](https://docs.e2enetworks.com/docs/tir/Nodes/GuideTIR/)  
**Generated:** July 30, 2025  
**Reading Time:** ~15 minutes  

---

## 📋 Table of Contents

1. [Overview](#overview)
2. [Getting Started](#getting-started)
3. [Node Images](#node-images)
4. [Node Configuration Options](#node-configuration-options)
5. [Creating a Node Step-by-Step](#creating-a-node-step-by-step)
6. [Node Management](#node-management)
7. [Node Actions](#node-actions)
8. [Advanced Features](#advanced-features)

---

## Overview

**TIR Nodes** are fully collaborative environments that make AI development possible. They combine the power of containers, Jupyter Labs, and AI/ML frameworks to create a readily usable workspace for you and your entire team.

### 🎯 Common Use Cases

- **Fine-tune Large Language Models (LLMs)** on single GPU using PyTorch or Hugging Face
- **Multi-GPU training** for LLMs or Diffusion models using DeepSpeed and Accelerate
- **Run Jupyter notebooks** from GitHub, Kaggle, or Colab
- **Download and review datasets** from TIR or Hugging Face
- **Test AI models** like Stable Diffusion or any LLM

> **💡 Pro Tip:** A TIR node is a fully functional coding environment. You can configure SSH access to work with command line tools, upload data via SFTP, or sync code with Git.

---

## Getting Started

### Step 1: Login and Project Setup

1. **Login** using your myaccount credentials
2. **Select TIR AI platform** to access resources
3. **Create a project** using the "Create project" button
4. **Access Nodes** from the side panel
5. **Select from available images** to create a node

### Step 2: Plan Selection

1. **Choose CPU or GPU plan** (Free Tier available for testing)
2. **Select appropriate plan** based on requirements
3. **Request plan if unavailable** (email notification when available)

### Step 3: Node Configuration

1. **Name your node** and choose type:
   - **New Notebook:** Empty JupyterLab environment
   - **Import Notebook:** Pull from GitHub or Colab
2. **Select workspace size** (30 GB free by default)
3. **Enable SSH Access** (optional)
4. **Choose access method** when ready (Jupyter Labs or SSH)

---

## Node Images

TIR supports various pre-built container images optimized for different workflows:

### 🖥️ Available Image Types

#### **Base OS Image**
- Clean container environment with no pre-installed packages
- Maximum flexibility for custom setups
- Lightweight and ideal for tailored environments

#### **Jupyter Image**
- Pre-installed Jupyter Notebook environment
- Perfect for interactive development
- Supports `.ipynb` files directly in browser

#### **ComfyUI Image**
- Visual and generative AI workflows
- Drag-and-drop interface for model pipelines
- Ideal for image generation and creative tools

#### **FramePack Image**
- Pre-configured FramePack framework
- Optimized for specialized use cases
- Ready-to-use environment for FramePack projects

---

## Node Configuration Options

### 🔧 Configuration Settings

#### **SSH Access**
- Enable using public key or password
- Must stop node before enabling SSH
- Provides command-line access to environment

#### **Storage Options**

**Standard Disk:**
- Up to 5,000 GB available
- Default: 30 GB free
- Mounted at `/home/jovyan`
- Persistent across restarts

**Local NVME Storage (H100 only):**
- High-speed local storage at `/mnt/local`
- Available only during runtime
- Perfect for model checkpoints

#### **Pricing Plans**
- **Hourly:** Pay-as-you-go flexibility
- **Committed:** Discounted rates with longer commitment

### 📊 Node Status Types

| Status | Description |
|--------|-------------|
| **Waiting** | Node being deployed on selected hardware |
| **Running** | Active node, accessible via Jupyter/SSH |
| **Stopped** | Node paused, workspace preserved |
| **Pending** | Waiting for resources (48-72 hours) |
| **Expired** | Resource request no longer in queue |

---

## Creating a Node Step-by-Step

### Step 1: Start Node Creation

To create a Node, click on **Create Node** at the right corner of the page.

![Create Node Button](images/image_5cdfde38a5.png)
*Click "Create Node" to begin the process*

### Step 2: Select Node Image

Choose your Node image from **TIR PRE-BUILT**, **BASE OS**, or **CONTAINER REGISTRY**. You can also search for specific images.

![Node Image Selection](images/image_6fe32f7a77.png)
*Select from TIR Pre-built images with various frameworks*

#### Base OS Selection
The Base OS node image does not come with JupyterLab pre-installed.

![Base OS Node](images/image_7822960dbe.png)
*Base OS selection for custom environments*

#### Container Registry
When using Container Registry, specify whether the image includes JupyterLab.

![Container Registry Node](images/image_7187dc5671.png)
*Container Registry selection with JupyterLab specification*

### Step 3: Resource Selection

Choose your plan based on CPU or GPU requirements.

![Node Resource Selection](images/image_2d7398716d.png)
*Select CPU or GPU resources based on your needs*

#### Resource Filtering
Filter CPU and GPU resources for more tailored selection.

![CPU Filter](images/image_aa71d9fe29.png)
*Filter resources by specific requirements*

### Step 4: Storage Configuration

Add required datasets to your node during creation.

![Node Storage](images/image_078d77740c.png)
*Configure storage and add datasets*

### Step 5: Node Details

Provide essential details before the node is created.

![Node Details Form](images/image_d505d96b46.png)
*Enter node configuration details*

### Step 6: Review Summary

Review all configuration details before creation.

![Node Summary](images/image_1797d59a18.png)
*Final summary before node creation*

### Step 7: Node Management

After creation, access your nodes from the management dashboard.

![Manage Nodes](images/image_01f7278114.png)
*Manage all your nodes from the dashboard*

---

## Node Management

### 📊 Overview Dashboard

View complete node details and plan information under the Overview tab.

![Node Overview](images/image_ea56bda830.png)
*Complete node overview with details and plan information*

### 📅 Node Events

Track all node events and activities.

![Node Events](images/image_29d16446a0.png)
*Monitor node events and status changes*

### 📈 Monitoring

#### Real-time Metrics
Monitor CPU utilization, memory usage, and custom intervals.

![Metrics Graph](images/image_d51412332b.png)
*Real-time CPU and memory utilization graphs*

#### Activity Tracking
View one-month activity breakdown by days and hours.

![Monthly Activity](images/image_74994e86a7.png)
*Detailed activity tracking over time*

### 💾 Storage Management

#### Disk Size Management
View and modify disk size as needed.

![Disk Management](images/image_1bfc800aa0.png)
*Current disk usage and management options*

#### Update Disk Size
Change disk size and apply updates.

![Update Disk Size](images/image_26dca5fb26.png)
*Update disk size interface*

### 📁 Dataset Management

Manage mounted and unmounted datasets.

![Associated Datasets](images/image_f5da9d5fbf.png)
*View and manage associated datasets*

### 🗂️ File System

View associated file systems.

![Associated File System](images/image_e4d692e08f.png)
*File system associations and management*

### 🔐 Network & Security

#### SSH Configuration
Configure SSH keys for secure access.

![SSH Setup](images/image_6d1d0164cd.png)
*SSH key configuration interface*

#### IP Management
Attach or detach reserved IP addresses.

![Reserve IP](images/image_b8ce57fc22.png)
*Reserved IP management*

#### Port Configuration
Add custom ports for your applications.

![Port Management](images/image_a7f11bd334.png)
*Custom port configuration*

### 📜 Start Scripts

#### Script Selection
Select scripts to attach to your Node for automated setup.

![Script Selection](images/image_28f079e5a4.png)
*Choose from available start scripts*

#### Create New Script
Create new scripts by clicking the "Click Here" button.

![Create Script](images/image_5837f5b492.png)
*Create new start script interface*

#### Script Editor
Upload files or write scripts directly in the interface.

![Script Editor](images/image_66bd60991357.png)
*Script editor with upload and write options*

#### Script Management
Manage, update, or delete existing scripts.

![Script Library](images/image_6bce8a854d.png)
*Script library management*

> **⚠️ Important:** Script changes take effect only after node restart. Scripts cannot be deleted if attached to active nodes.

#### Script Confirmation
Confirmation dialog appears when adding or removing scripts.

![Script Confirmation](images/image_59ff15d7cc.png)
*Script modification confirmation dialog*

---

## Node Actions

### 🎮 Available Actions

View all available actions: Launch Notebook, Stop Node, Restart Node, Update Image, Update Plan, Delete.

![Node Actions](images/image_23542c37b0.png)
*Complete list of available node actions*

### 🚀 Launch Notebook

#### Launch Process
After clicking Launch Node, the node will be launched.

![Launch Process](images/image_62549632d3.png)
*Node launching in progress*

#### Active Node
Successfully launched node with access options.

![Active Node](images/image_7fde4a93e6.png)
*Active node with Jupyter and SSH access*

### ⏹️ Stop Node

Stop the notebook by clicking the Stop button.

![Stop Node](images/image_1e1a73910586.png)
*Stop node interface*

### 🔄 Restart Node

Restart the notebook using the restart button.

![Restart Node](images/image_39a468ced8.png)
*Node restart confirmation*

### 🔄 Update Image

#### Update Process
Click "Update Image" to change the node image.

![Update Image](images/image_d7c2b9a7e4.png)
*Update image selection*

#### Image Selection
Select new image and click update.

![Update Image Selection](images/image_fff33efd99.png)
*Choose new image for update*

### ⚙️ Update Plan

Update node configuration and plan.

![Update Plan](images/image_2814d5dab0.png)
*Node plan update interface*

> **⚠️ Important:** Node must be in Stop state before updating.

### 💰 Convert to Committed

Convert hourly nodes to committed plans for discounts.

![Convert Option 1](images/image_574aee8b59.png)
*Convert to committed plan option*

![Convert Option 2](images/image_4eaa91451a.png)
*Committed plan selection*

![Convert Option 3](images/image_c9de6974153.png)
*Conversion confirmation*

> **💡 Note:** This feature allows conversion without stopping or restarting the node.

### 💾 Save Image

#### Create Custom Image
Save your configured environment as a custom image.

![Save Image](images/image_b815917f37.png)
*Save custom image interface*

![Create Image](images/image_a37327925c.png)
*Image creation with registry selection*

#### Restore Image
Restore saved images with all dependencies.

![Restore Image](images/image_f6be24b406.png)
*Restore saved image interface*

### 🗑️ Delete Node

Delete the node permanently.

![Delete Node](images/image_0595fb7af8.png)
*Node deletion confirmation*

---

## Advanced Features

### 🔍 Node Search & Filtering

#### Basic Search
Search nodes by entering the name in the search bar.

![Node Search](images/image_e201798885.png)
*Basic node search functionality*

#### Advanced Filter Access
Access advanced filtering options.

![Advanced Filter Button](images/image_49b2737165.png)
*Advanced filter access button*

#### Advanced Search Configuration
Configure detailed search parameters.

![Advanced Search](images/image_6ffaaca01c.png)
*Advanced search configuration options*

### 🚀 Quick Launch

Launch nodes directly from the sidebar.

![Sidebar Launch](images/image_6d1d0164cd.png)
*Quick launch from sidebar*

---

## 🎯 Best Practices

### **Resource Selection**
- Use **Free Tier** for exploration and testing
- Choose **A100 or H100** for production workloads
- Consider **committed plans** for cost savings

### **Storage Strategy**
- Use `/home/jovyan` for persistent data
- Leverage `/mnt/local` (H100) for temporary high-speed storage
- Regular backups to EOS buckets recommended

### **Image Management**
- Start with pre-built images
- Save custom configurations as images
- Use `requirements.txt` for package management

### **Security**
- Prefer SSH keys over passwords
- Configure appropriate network access
- Regular security updates

---

## 📞 Support

For additional assistance:
- **Storage > 5TB:** Raise support ticket
- **Technical Issues:** Contact E2E Networks support
- **Documentation:** Visit [E2E Networks Docs](https://docs.e2enetworks.com/)

---

*This comprehensive guide was created from the original E2E Networks TIR documentation, enhanced with proper image placement, professional formatting, and step-by-step instructions for optimal user experience.*

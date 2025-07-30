# Getting started  E2E Cloud

**Source:** [https://docs.e2enetworks.com/docs/tir/Nodes/GuideTIR/](https://docs.e2enetworks.com/docs/tir/Nodes/GuideTIR/)
**Generated:** July 30, 2025 at 04:44 PM
**Reading Time:** ~10 minutes

## Table of Contents

- [Introduction](#introduction)
  - [Getting Started with Nodes on TIRâ](#getting-started-with-nodes-on-tirâ)
  - [Node Imagesâ](#node-imagesâ)
  - [Node Optionsâ](#node-optionsâ)
  - [How to Create Node?â](#how-to-create-nodeâ)
  - [Node Detailsâ](#node-detailsâ)
  - [Node Actionsâ](#node-actionsâ)
  - [Launch Node from Sidebarâ](#launch-node-from-sidebarâ)

## Introduction

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

After clicking on the Create Node button, a page will appear. Now select the Node image option from TIR PRE-BUILT, BASE OS, and CONTAINER REGISTRY. Additionally, you can also perform the search on the Node Images.

The Base OS node image does not come with JupyterLab pre-installed.

When installing an image from the Container Registry, the user must specify whether the selected image includes JupyterLab pre-installed or not.

After selecting the machine, the Resource page will appear. At this stage, choose a plan based on either CPU or GPU requirements.

Additionally, you can filter CPU and GPU resources based on your specific requirements for a more tailored selection.

At this step, the user can also add the required dataset to the node being created.

The user is prompted to provide the essential details before the node is created.

After all steps are completed, the Node Summary details will be displayed.

After clicking on the 'Create' button, the page will redirect to the 'Manage Nodes' page and display all details there.


### Node Detailsâ

#### Overviewâ

You can see the Node Details and Plan Details under the Overview tab.

#### Node Eventsâ

#### Monitoringâ

You can see the monitor graph in CPU Utilization, Memory Utilization & Interval.

You can see the one-month activity as per your requirement in days & hours.

#### Workspace Sizeâ

You can see the details disk size and also You can change the Disk size as per your requirements.

For updating the disk size you have to change the disk size and then click on update button.

#### Associated Datasetsâ

You can also see the Associated Datasets with two different datasets- Mounted & Unmounted. You can also Unmount.

#### Associated File Systemâ

#### Network & securityâ

You can configure ssh key under Network and security tab.

You can Attach/Detach the Reserve IP under Network and security tab.

You can Add Port under Network and security tab.

#### Start scriptâ

In this section, users can select the desired script to attach to the Node. The attached script enables seamless execution on the Node, ensuring that all necessary dependencies are installed and configured for optimal performance.

Users can create a new script by clicking on the Click Here button.

Users have the flexibility to either upload a script file directly from their local machine or manually write/copy the script code within the interface. Before saving and utilizing the script, users are required to provide a name for the script file.

Users can select a script from the list of available scripts across the project. Additionally, users have the ability to update an existing script or delete any script as needed.

Any changes made to the script will only take effect once the Node, to which the script is attached, is restarted.

Users can only delete a script if it is not currently attached to any Node.

When a script is added to or removed from the Node, a confirmation dialog box appears to verify the action.


### Node Actionsâ

You can see the actions like Launch Notebook, Stop Node,Restart Node,Update Image,Update Plan, Delete.

#### Launch Notebookâ

After clicking on Launch Node, Node will be launched and it should be visible like this.

#### Stop Nodeâ

For Stopping the Notebook you have to click on Stop button and the Node will be stopped.

#### Restart Nodeâ

For Restarting Notebook you have to click on restart button and notebook will be restarted.

#### Update Imageâ

You can update notebook image, For updating image you have to click on update image.

Select image and click on update button.

#### Update Planâ

You can update Node, For updating the Node You have to click on Update button.

Node must be in Stop state before updating the Node.

#### Convert to Committedâ

After creating a node, it can be converted to a committed node if the committed SKU is available by selecting the "Convert to Committed" option.

Nodes on an hourly plan without an associated SKU will display a grayed-out "Convert to Committed" button.

Nodes on the Private Cluster or already Committed does not show this option.

This feature allows a node to be converted to a committed node without the need to stop or restart it, ensuring seamless operation.

#### Save Imageâ

When the node is restarted, any packages you manually installed will need to be re-installed. By saving an image, you can preserve all dependencies, allowing you to restore them later or create new nodes from the saved image.

##### Create Imageâ

To save an image, click the 'Save Image' button, enter a valid name, and select the container registry where the image should be saved. The saved image will then also appear in the chosen container registry.

To store all saved dependencies and packages, click Restore Image icon under Images tab.

#### Delete Nodeâ

For Deleting the Node you have to click on Delete button.


### Launch Node from Sidebarâ

You can launch the node from the left side of the Node name.

#### Advance Filter on Nodeâ

You can locate the node by entering its name in the search bar.

You can access advanced filter options by clicking on this button.

You can apply the advanced filter configurations and then click the search button.

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


---

*This documentation was automatically generated from [https://docs.e2enetworks.com/docs/tir/Nodes/GuideTIR/](https://docs.e2enetworks.com/docs/tir/Nodes/GuideTIR/) using Professional Documentation Generator.*

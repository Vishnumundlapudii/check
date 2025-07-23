# TIR Nodes: A Comprehensive Guide to AI Development Environments
====================================================================

TIR Nodes are fully collaborative environments that make AI development possible by combining the power of containers, Jupyter Labs, and AI/ML frameworks. This guide provides a detailed overview of TIR Nodes, including their features, use cases, and configuration options.

## Getting Started with TIR Nodes
-------------------------------

To get started with TIR Nodes, follow these steps:

### Step 1: Log in and Select TIR AI Platform

![Create Node](https://docs.e2enetworks.com/assets/images/click_create_node-5cdfde38a5974bab42107967b1db8214.png)

**Interface Analysis:** The login page allows users to access the TIR AI platform using their myaccount credentials.

**Technical Context:** The TIR AI platform provides a secure and collaborative environment for AI development.

**User Action:** Enter your myaccount credentials and select the TIR AI platform.

**Expected Result:** You will be redirected to the TIR landing page.

**Professional Tips:** Make sure to use a secure password and keep your account credentials confidential.

### Step 2: Create a Project

![Node Image Selection](https://docs.e2enetworks.com/assets/images/node_create_tirprebuilt-6fe32f7a774c2d3dadb7f5d167ca1392.png)

**Interface Analysis:** The project creation page allows users to create a new project using the "Create project" button.

**Technical Context:** The project will be created in the user's private workspace.

**User Action:** Click on the "Create project" button and enter the project details.

**Expected Result:** The project will be created, and you will be redirected to the project dashboard.

**Professional Tips:** Use a descriptive project name and description to help you identify your projects.

### Step 3: Launch TIR Node

![Node Resource Selection](https://docs.e2enetworks.com/assets/images/node_create_noderesources-2d7398716d0e804ed64f0f5b77bde94f.png)

**Interface Analysis:** The node launch page allows users to select the node resources, including CPU, GPU, and disk size.

**Technical Context:** The node resources will determine the performance and capabilities of the TIR Node.

**User Action:** Select the desired node resources and click on the "Launch" button.

**Expected Result:** The TIR Node will be launched, and you will be redirected to the node dashboard.

**Professional Tips:** Choose the right node resources for your project needs to ensure optimal performance.

## Node Images
-------------

TIR environments use container images that act as blueprints, providing the libraries, tools, and dependencies required to run each node. TIR supports a variety of pre-built images equipped with popular machine learning and deep learning frameworks.

### Base OS Image

![Base OS Node](https://docs.e2enetworks.com/assets/images/node_create_baseos-7822960dbeed2c236e77da807fe1c30e.png)

**Interface Analysis:** The Base OS image is a container environment with no pre-installed packages or tools.

**Technical Context:** The Base OS image offers maximum flexibility for users who prefer to set up their own dependencies and frameworks from scratch.

**User Action:** Select the Base OS image and configure the node resources.

**Expected Result:** The TIR Node will be launched with the Base OS image.

**Professional Tips:** Use the Base OS image for highly customized workflows that require specific package versions or configurations.

### Jupyter Image

![Jupyter Image](https://docs.e2enetworks.com/assets/images/node_create_jupyter-6fe32f7a774c2d3dadb7f5d167ca1392.png)

**Interface Analysis:** The Jupyter image comes pre-installed with Jupyter Notebook, making it an excellent choice for interactive, notebook-based development.

**Technical Context:** The Jupyter image is particularly useful for data analysis, experimentation with machine learning models, and educational purposes.

**User Action:** Select the Jupyter image and configure the node resources.

**Expected Result:** The TIR Node will be launched with the Jupyter image.

**Professional Tips:** Use the Jupyter image for interactive, notebook-based development and data analysis.

### ComfyUI Image

![ComfyUI Image](https://docs.e2enetworks.com/assets/images/node_create_comfyui-7187dc5671d9cda2c7bbf059aa6e7fce.png)

**Interface Analysis:** The ComfyUI image is designed for users working on visual and generative AI workflows.

**Technical Context:** The ComfyUI image includes the ComfyUI interface pre-installed, enabling a graphical, drag-and-drop environment for building model pipelines and experimenting with creative tools.

**User Action:** Select the ComfyUI image and configure the node resources.

**Expected Result:** The TIR Node will be launched with the ComfyUI image.

**Professional Tips:** Use the ComfyUI image for visual and generative AI workflows that require a graphical interface.

### FramePack Image

![FramePack Image](https://docs.e2enetworks.com/assets/images/node_create_framepack-7822960dbeed2c236e77da807fe1c30e.png)

**Interface Analysis:** The FramePack image comes pre-configured with the FramePack framework, catering to specialized use cases that depend on it.

**Technical Context:** The FramePack image is pre-tuned for seamless integration and is well-suited for users who need immediate access to FramePack’s features without additional setup.

**User Action:** Select the FramePack image and configure the node resources.

**Expected Result:** The TIR Node will be launched with the FramePack image.

**Professional Tips:** Use the FramePack image for specialized use cases that depend on the FramePack framework.

## Node Options
--------------

TIR nodes are extremely powerful and flexible. While most configurations have a default to make the user's life easier, sometimes you may need to tweak the knobs. The following are the configurations that you can tweak in a node environment:

### Enable SSH

![Enable SSH](https://docs.e2enetworks.com/assets/images/node_create_ssh-078d77740cb90960b457a6b3581d607c.png)

**Interface Analysis:** The SSH option allows users to enable SSH access on the node using a public key or password (not recommended).

**Technical Context:** Enabling SSH access allows users to access the node remotely using SSH clients.

**User Action:** Enable SSH access using a public key or password (not recommended).

**Expected Result:** SSH access will be enabled on the node.

**Professional Tips:** Use a public key for SSH access instead of a password for added security.

### Disk Size

![Disk Size](https://docs.e2enetworks.com/assets/images/Notebook6-1bfc800aa05cfdc53bff133752dda2fb.png)

**Interface Analysis:** The disk size option allows users to select the disk size for the node, up to 5000GB.

**Technical Context:** The selected disk will be mounted at /home/jovyan in your node environment.

**User Action:** Select the desired disk size for the node.

**Expected Result:** The selected disk size will be allocated to the node.

**Professional Tips:** Choose a disk size that meets your project needs to ensure optimal performance.

## Troubleshooting
--------------

### Common Issues

* Node not launching: Check if the node resources are sufficient for the project needs.
* SSH access not working: Check if SSH access is enabled and if the public key or password is correct.
* Disk size not sufficient: Check if the selected disk size meets the project needs.

### Solutions

* Node not launching: Increase the node resources or try launching a different node.
* SSH access not working: Check the SSH logs for errors or try using a different SSH client.
* Disk size not sufficient: Increase the disk size or try using a different disk configuration.

## Conclusion
----------

TIR Nodes provide a powerful and flexible environment for AI development. By understanding the features, use cases, and configuration options of TIR Nodes, users can optimize their workflow and achieve better results. Remember to follow best practices and troubleshooting tips to ensure optimal performance and minimize errors.
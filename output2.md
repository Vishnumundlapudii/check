## Creating a New Node
=====================================

### Before You Begin
--------------------

Before creating a new node, ensure you have:

* An active MyAccount login credentials
* A project set up in TIR
* A SSH key added to your MyAccount (if you plan to enable SSH access)

### Step-by-Step Instructions
---------------------------

### Step 1: Log in to MyAccount
------------------------------

1. Open a web browser and navigate to the MyAccount login page.
2. Enter your login credentials to access your account.

### Step 2: Select a Project
-------------------------

1. Navigate to **Projects** → **TIR**.
2. Choose a project from the list of available projects.

### Step 3: Create a New Node
---------------------------

1. Click on the **Nodes** tab.
2. Click the **+ Create Node** button.

### Step 4: Choose an Image
-------------------------

* Select one of the following image options:
	+ **Prebuilt**: Use a pre-configured image.
	+ **Base OS**: Use a base operating system image.
	+ **From Container Registry**: Use a custom image from a container registry.

### Step 5: Select a Compute Plan
------------------------------

* Choose a compute plan that suits your needs:
	+ **CPU**: Suitable for general-purpose computing.
	+ **GPU**: Suitable for graphics-intensive computing.

### Step 6: Configure the Notebook
---------------------------------

* Choose one of the following notebook options:
	+ **New**: Create a new notebook from scratch.
	+ **Import**: Import an existing notebook.

### Step 7: Set Disk Size
----------------------

* Set the disk size for your node. The default size is 30GB.

### Step 8: Enable SSH (Optional)
------------------------------

* If required, enable SSH access to your node.
* Ensure you have a SSH key added to your MyAccount.

### Step 9: Create the Node
-------------------------

* Click the **Create** button to create the new node.

### After Creation
-----------------

* The node status will move to **Running** when it is ready for use.
* You can access your node via:
	+ Jupyter: For web-based notebook access.
	+ SSH: For command-line access (if enabled).
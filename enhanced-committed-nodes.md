```html
<div style="display: flex; gap: 2rem;">
  <div style="flex: 1; max-width: calc(100% - 280px);">
    # Model Endpoints
    TIR provides two methods for deploying containers that serve model API endpoints for AI inference services:
    Deploy Using Pre-built Containers (Provided by TIR)
    Before launching a service with TIR's pre-built containers, you need to create a TIR Model and upload the necessary model files. These containers are configured to automatically download model files from an EOS (E2E Object Storage) Bucket and start the API server. Once the endpoint is ready, you can make synchronous requests to the endpoint for inference. Learn more in this tutorial.

    Deploy using your own container
    You can launch an inference service using your own Docker image, either public or private. Once the endpoint is ready, you can make synchronous requests for inference. Optionally, you can attach a TIR model to automate the download of model files from an EOS bucket to the container. Learn more in this tutorial.

    ## Create Model Endpoints

    To create a model endpoint:

    ### Step 1: Navigate to Inference
    ![Model Endpoints](https://docs.e2enetworks.com/assets/images/model_endpoint1-3d26d1bb83f8851e0f7ddc503c584d46.png)
    **UI Elements Description:** The screenshot shows the "Model Endpoints" page with a list of existing endpoints and a "CREATE ENDPOINT" button.
    **User Actions Required:** Click on the "CREATE ENDPOINT" button.
    **Expected Results:** The "Create Model Endpoint" page will be displayed.
    **Technical Context:** This step is important to create a new model endpoint.
    **Troubleshooting:** If the "CREATE ENDPOINT" button is not visible, ensure that you have the necessary permissions.

    ### Step 2: Create an Endpoint
    ![Create Model Endpoint](https://docs.e2enetworks.com/assets/images/create_modelendpoint-257c920a02c0b790d66235208c93786e.png)
    **UI Elements Description:** The screenshot shows the "Create Model Endpoint" page with a form to fill in the endpoint details.
    **User Actions Required:** Fill in the form with the required information and click on the "CREATE ENDPOINT" button.
    **Expected Results:** The endpoint will be created and displayed on the "Model Endpoints" page.
    **Technical Context:** This step is important to create a new model endpoint.
    **Troubleshooting:** If the endpoint is not created, ensure that the form is filled in correctly and that there are no errors.

    ### Step 3: Choose a Framework
    ![Choose Framework](https://docs.e2enetworks.com/assets/images/inference_create_new_framework-f2abec2c4e8ab9bef4dcea94222db643.png)
    **UI Elements Description:** The screenshot shows the "Choose Framework" page with a list of available frameworks.
    **User Actions Required:** Select a framework from the list.
    **Expected Results:** The framework will be selected and displayed on the "Create Model Endpoint" page.
    **Technical Context:** This step is important to choose a framework for the model endpoint.
    **Troubleshooting:** If the framework is not selected, ensure that the list is populated and that there are no errors.

    ### Step 4: Link with Model Repository
    ![Link with Model Repository](https://docs.e2enetworks.com/assets/images/inference_create_new_link_model_repo-b2244b5c7865fbfda217c8332cf73ed0.png)
    **UI Elements Description:** The screenshot shows the "Link with Model Repository" page with a form to fill in the repository details.
    **User Actions Required:** Fill in the form with the required information and click on the "LINK" button.
    **Expected Results:** The repository will be linked to the model endpoint.
    **Technical Context:** This step is important to link a model repository to the model endpoint.
    **Troubleshooting:** If the repository is not linked, ensure that the form is filled in correctly and that there are no errors.

    ### Step 5: Download from Huggingface
    ![Download from Huggingface](https://docs.e2enetworks.com/assets/images/inference_create_new_from_huggingface-6153261681f1c0fdc7cd0e064d223d59.png)
    **UI Elements Description:** The screenshot shows the "Download from Huggingface" page with a form to fill in the Huggingface details.
    **User Actions Required:** Fill in the form with the required information and click on the "DOWNLOAD" button.
    **Expected Results:** The model will be downloaded from Huggingface.
    **Technical Context:** This step is important to download a model from Huggingface.
    **Troubleshooting:** If the model is not downloaded, ensure that the form is filled in correctly and that there are no errors.

    ## Plan Details

    ### Machine

    ![Machine Selection](https://docs.e2enetworks.com/assets/images/inference_create_new_plan_gpu-4a0b6e902b5318ebc22a517d10a10af8.png)
    **UI Elements Description:** The screenshot shows the "Machine Selection" page with a list of available machines.
    **User Actions Required:** Select a machine from the list.
    **Expected Results:** The machine will be selected and displayed on the "Plan Details" page.
    **Technical Context:** This step is important to select a machine for the model endpoint.
    **Troubleshooting:** If the machine is not selected, ensure that the list is populated and that there are no errors.

    ### LLM Settings (Optional)

    ![LLM Setting](https://docs.e2enetworks.com/assets/images/llm_setting_img-217d177523ba2a926477583e5ec68406.png)
    **UI Elements Description:** The screenshot shows the "LLM Setting" page with a form to fill in the LLM details.
    **User Actions Required:** Fill in the form with the required information and click on the "SAVE" button.
    **Expected Results:** The LLM settings will be saved and displayed on the "Plan Details" page.
    **Technical Context:** This step is important to configure LLM settings for the model endpoint.
    **Troubleshooting:** If the LLM settings are not saved, ensure that the form is filled in correctly and that there are no errors.

    ## Environment Variables

    ![Add Variable](https://docs.e2enetworks.com/assets/images/inference_hourly_env-ebb7ef3a76005c811b67deb6ec6793d1.png)
    **UI Elements Description:** The screenshot shows the "Add Variable" page with a form to fill in the variable details.
    **User Actions Required:** Fill in the form with the required information and click on the "ADD" button.
    **Expected Results:** The variable will be added and displayed on the "Environment Variables" page.
    **Technical Context:** This step is important to add environment variables for the model endpoint.
    **Troubleshooting:** If the variable is not added, ensure that the form is filled in correctly and that there are no errors.

  </div>
  <div style="width: 280px; position: sticky; top: 20px;">
    ## 📋 On This Page
    * [Create Model Endpoints](#create-model-endpoints)
      + [Step 1: Navigate to Inference](#step-1-navigate-to-inference)
      + [Step 2: Create an Endpoint](#step-2-create-an-endpoint)
      + [Step 3: Choose a Framework](#step-3-choose-a-framework)
      + [Step 4: Link with Model Repository](#step-4-link-with-model-repository)
      + [Step 5: Download from Huggingface](#step-5-download-from-huggingface)
    * [Plan Details](#plan-details)
      + [Machine](#machine)
      + [LLM Settings (Optional)](#llm-settings-optional)
    * [Environment Variables](#environment-variables)
  </div>
</div>

<script>
  // Add event listener to scroll event
  window.addEventListener('scroll', () => {
    // Get current scroll position
    const scrollPosition = window.scrollY;

    // Get all headings
    const headings = document.querySelectorAll('h1, h2, h3, h4, h5, h6');

    // Loop through headings
    headings.forEach((heading) => {
      // Get heading offset top
      const headingOffsetTop = heading.offsetTop;

      // Check if heading is within scroll position
      if (scrollPosition >= headingOffsetTop - 100) {
        // Get heading id
        const headingId = heading.id;

        // Get all navigation links
        const navigationLinks = document.querySelectorAll('.nav-link');

        // Loop through navigation links
        navigationLinks.forEach((link) => {
          // Get link href
          const linkHref = link.href;

          // Check if link href matches heading id
          if (linkHref === `#${headingId}`) {
            // Add active class to link
            link.classList.add('active');
          } else {
            // Remove active class from link
            link.classList.remove('active');
          }
        });
      }
    });
  });
</script>

<style>
  /* Add styles for navigation */
  .nav-link {
    display: block;
    padding: 10px;
    border-bottom: 1px solid #ccc;
  }

  .nav-link.active {
    background-color: #f0f0f0;
  }

  /* Add styles for progress bar */
  .progress-bar {
    width: 100%;
    height: 10px;
    background-color: #ccc;
  }

  .progress-bar-fill {
    width: 0;
    height: 100%;
    background-color: #333;
  }
</style>

<!-- Add progress bar -->
<div class="progress-bar">
  <div class="progress-bar-fill"></div>
</div>

<script>
  // Add event listener to scroll event
  window.addEventListener('scroll', () => {
    // Get current scroll position
    const scrollPosition = window.scrollY;

    // Get document height
    const documentHeight = document.body.offsetHeight;

    // Calculate progress bar width
    const progressBarWidth = (scrollPosition / documentHeight) * 100;

    // Update progress bar fill width
    document.querySelector('.progress-bar-fill').style.width = `${progressBarWidth}%`;
  });
</script>
```

This code creates a right-side navigation menu with links to different sections of the page. It also adds a progress bar at the top of the page that fills up as you scroll down. The navigation links are highlighted as you scroll to their corresponding sections.

Note that this code assumes that you have already created the HTML structure for your page, including the sections and headings. You will need to modify the code to match your specific HTML structure.

Also, this code uses JavaScript and CSS to create the navigation menu and progress bar. If you are not familiar with these technologies, you may need to modify the code or seek additional help.

I hope this helps! Let me know if you have any questions or need further assistance.
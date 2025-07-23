# Table of Contents
- [Model Endpoints](#model-endpoints)
  - [Create Model Endpoints](#create-model-endpoints)
  - [Plan Details](#plan-details)
    - [Machine](#machine)
    - [LLM Settings(Optional)](#llm-settingsoptional)
      - [LLM Settings](#llm-settings)
      - [Tokenizer Settings](#tokenizer-settings)
      - [System Settings](#system-settings)
    - [Serverless Configuration](#serverless-configuration)
  - [Environment Variables](#environment-variables)
  - [Summary](#summary)
  - [Model Endpoint Dashboard](#model-endpoint-dashboard)
    - [Overview](#overview)
    - [Async Invocations](#async-invocations)
    - [Logs](#logs)
    - [Deployment Events](#deployment-events)
    - [Request Logs](#request-logs)
    - [Monitoring](#monitoring)
    - [Serverless Configuration](#serverless-configuration-1)
    - [Search Model Endpoint](#search-model-endpoint)
  - [Actions](#actions)

## Model Endpoints
TIR provides two methods for deploying containers that serve model API endpoints for AI inference services:
Deploy Using Pre-built Containers (Provided by TIR)
Before launching a service with TIR's pre-built containers, you need to create a TIR Model and upload the necessary model files. These containers are configured to automatically download model files from an EOS (E2E Object Storage) Bucket and start the API server. Once the endpoint is ready, you can make synchronous requests to the endpoint for inference. Learn more in this tutorial.

Deploy using your own container
You can launch an inference service using your own Docker image, either public or private. Once the endpoint is ready, you can make synchronous requests for inference. Optionally, you can attach a TIR model to automate the download of model files from an EOS bucket to the container. Learn more in this tutorial.

## Create Model Endpoints
To create a model endpoint:

### Navigate to Inference: Click on "Model Endpoints."
![Model Endpoints](https://docs.e2enetworks.com/assets/images/model_endpoint1-3d26d1bb83f8851e0f7ddc503c584d46.png)

**UI Elements:**

*   Navigation menu
*   "Model Endpoints" button

**User Actions:**

1.  Click on "Model Endpoints" button

**Expected Results:**

*   The "Model Endpoints" page will be displayed

**Technical Context:**

*   This step is important to access the model endpoints

**Troubleshooting:**

*   If the "Model Endpoints" button is not visible, check if you have the necessary permissions

### Create an Endpoint: Click on the "CREATE ENDPOINT" button.
![Create Model Endpoint](https://docs.e2enetworks.com/assets/images/create_modelendpoint-257c920a02c0b790d66235208c93786e.png)

**UI Elements:**

*   "CREATE ENDPOINT" button

**User Actions:**

1.  Click on the "CREATE ENDPOINT" button

**Expected Results:**

*   The "Create Endpoint" page will be displayed

**Technical Context:**

*   This step is important to create a new endpoint

**Troubleshooting:**

*   If the "CREATE ENDPOINT" button is not visible, check if you have the necessary permissions

### Choose a Framework:
You can use the search bar to explore the available frameworks.
![Choose Framework](https://docs.e2enetworks.com/assets/images/inference_create_new_framework-f2abec2c4e8ab9bef4dcea94222db643.png)

**UI Elements:**

*   Search bar
*   Framework list

**User Actions:**

1.  Type in the search bar to find a framework
2.  Select a framework from the list

**Expected Results:**

*   The selected framework will be displayed

**Technical Context:**

*   This step is important to choose a framework for the endpoint

**Troubleshooting:**

*   If the search bar is not visible, check if you have the necessary permissions

### Link with Model Repository and select from Model Repository.
![Link with Model Repository](https://docs.e2enetworks.com/assets/images/inference_create_new_link_model_repo-b2244b5c7865fbfda217c8332cf73ed0.png)

**UI Elements:**

*   "Link with Model Repository" button
*   Model repository list

**User Actions:**

1.  Click on the "Link with Model Repository" button
2.  Select a model repository from the list

**Expected Results:**

*   The selected model repository will be linked to the endpoint

**Technical Context:**

*   This step is important to link a model repository to the endpoint

**Troubleshooting:**

*   If the "Link with Model Repository" button is not visible, check if you have the necessary permissions

### Download from Huggingface and select token from HF Token Integration.
![Download from Huggingface](https://docs.e2enetworks.com/assets/images/inference_create_new_from_huggingface-6153261681f1c0fdc7cd0e064d223d59.png)

**UI Elements:**

*   "Download from Huggingface" button
*   HF Token Integration list

**User Actions:**

1.  Click on the "Download from Huggingface" button
2.  Select a token from the HF Token Integration list

**Expected Results:**

*   The selected token will be used to download from Huggingface

**Technical Context:**

*   This step is important to download from Huggingface

**Troubleshooting:**

*   If the "Download from Huggingface" button is not visible, check if you have the necessary permissions

## Plan Details
### Machine
Here you can select a machine type, either GPU or CPU. While selecting the plan, you can choose the plan for the inference from Committed or Hourly Billed.
You can apply filters to the available machines to refine your search results.
![Machine Selection](https://docs.e2enetworks.com/assets/images/inference_create_new_plan_gpu-4a0b6e902b5318ebc22a517d10a10af8.png)

**UI Elements:**

*   Machine type selection
*   Plan selection
*   Filter options

**User Actions:**

1.  Select a machine type
2.  Select a plan
3.  Apply filters to refine search results

**Expected Results:**

*   The selected machine type and plan will be displayed

**Technical Context:**

*   This step is important to select a machine type and plan for the endpoint

**Troubleshooting:**

*   If the machine type selection is not visible, check if you have the necessary permissions

### LLM Settings(Optional)
LLM settings encompass various configurations that define the model's behavior, efficiency, and performance during inference. These settings are categorized into three key areas: LLM Settings, Tokenizer Settings, and System Settings, each playing a crucial role in optimizing the model's output and deployment.

#### LLM Settings
LLM settings define the behavior, accuracy, and efficiency of a large language model during inference. Key parameters include Load Format (auto, pt, safetensors, etc.), Data Type (auto, float16, etc.), KV Cache Data Type, Quantization, and many more. Optimizing these settings ensures precise and contextually relevant outputs.
![LLM Setting](https://docs.e2enetworks.com/assets/images/llm_setting_img-217d177523ba2a926477583e5ec68406.png)

**UI Elements:**

*   LLM settings configuration

**User Actions:**

1.  Configure LLM settings

**Expected Results:**

*   The configured LLM settings will be displayed

**Technical Context:**

*   This step is important to configure LLM settings for the endpoint

**Troubleshooting:**

*   If the LLM settings configuration is not visible, check if you have the necessary permissions

#### Tokenizer Settings
Tokenizer settings determine how text is split into tokens, impacting model efficiency and comprehension. Parameters such as Tokenizer, Tokenizer Revision, and Custom Chat Template influence how input text is processed and interpreted before inference.
![Tokenizer Setting](https://docs.e2enetworks.com/assets/images/token_setting-9e73027630a70681b71b768cf2be77ae.png)

**UI Elements:**

*   Tokenizer settings configuration

**User Actions:**

1.  Configure tokenizer settings

**Expected Results:**

*   The configured tokenizer settings will be displayed

**Technical Context:**

*   This step is important to configure tokenizer settings for the endpoint

**Troubleshooting:**

*   If the tokenizer settings configuration is not visible, check if you have the necessary permissions

#### System Settings
System settings manage the hardware and computational aspects of LLM deployment. These include GPU utilization, Max Parallel Loading Workers, Block Size, and Swap Space to maximize performance and cost efficiency.
![System Setting](https://docs.e2enetworks.com/assets/images/system_setting_img-dd4f5b70178026a715803cfaac1dfbfe.png)

**UI Elements:**

*   System settings configuration

**User Actions:**

1.  Configure system settings

**Expected Results:**

*   The configured system settings will be displayed

**Technical Context:**

*   This step is important to configure system settings for the endpoint

**Troubleshooting:**

*   If the system settings configuration is not visible, check if you have the necessary permissions

### Serverless Configuration
For Hourly Billed Inference, it's possible to set the Active Workers to 0. You can set the number of Active Workers to any value from 0 up to the max workers. When there are no incoming requests, the number of active workers automatically reduces to 0, ensuring that no billing is incurred for that period.
For Committed Inference, the Active Workers cannot be set to 0, and the number of active workers must always remain greater than 0, ensuring the committed nature of Inference. You can set the number of Active Workers to any value from 1 up to the max workers.
All additional inferences, which are added automatically due to the autoscaling feature, will be charged at an hourly billing rate. Similarly, if the Active Worker count is increased from a serverless configuration after the inference is created, those additional inferences will also be billed at the hourly rate.
![Hourly Billed Serverless Configuration](https://docs.e2enetworks.com/assets/images/inference_hourly_serverless_config-5a51bd0bf23a39f02ac232aafcb8a90f.png)

**UI Elements:**

*   Serverless configuration options

**User Actions:**

1.  Configure serverless configuration options

**Expected Results:**

*   The configured serverless configuration options will be displayed

**Technical Context:**

*   This step is important to configure serverless configuration options for the endpoint

**Troubleshooting:**

*   If the serverless configuration options are not visible, check if you have the necessary permissions

## Environment Variables
### Add Variable
You can add a variable by clicking the ADD VARIABLE button.
![Add Variable](https://docs.e2enetworks.com/assets/images/inference_hourly_env-ebb7ef3a76005c811b67deb6ec6793d1.png)

**UI Elements:**

*   ADD VARIABLE button
*   Variable input field

**User Actions:**

1.  Click on the ADD VARIABLE button
2.  Enter a variable name and value in the input field

**Expected Results:**

*   The added variable will be displayed in the list of environment variables

**Technical Context:**

*   This step is important to add environment variables for the endpoint

**Troubleshooting:**

*   If the ADD VARIABLE button is not visible, check if you have the necessary permissions

## Summary
You can view the endpoint summary on the summary page, and if needed, modify any section of the inference creation process by clicking the edit button.
In the case of Hourly Billed Inference with Active Worker not equal to Max Worker, the billing is shown as:
In the case of Committed Inference with Active Worker not equal to Max Worker, the billing is shown as:
If the committed inference option is selected, a dialog box will appear asking for your preference regarding the next cycle.
You can change the serving model for the inference at any stage of the inference creation process.
![Hourly Billed Summary](https://docs.e2enetworks.com/assets/images/inference_hourly_summary-dcb8c28feb137efe4a6e6ac7979176bd.png)

**UI Elements:**

*   Summary page
*   Edit button
*   Billing information
*   Dialog box (for committed inference)

**User Actions:**

1.  View summary page
2.  Click on edit button to modify any section of inference creation process
3.  Review billing information
4.  Respond to dialog box (for committed inference)

**Expected Results:**

*   The summary page will be displayed with all relevant information
*   Any modifications made to inference creation process will be saved
*   Billing information will be accurate and up-to-date
*   Dialog box will appear for committed inference (if applicable)

**Technical Context:**

*   This step is important to review and finalize endpoint configuration before deployment

**Troubleshooting:**

*   If summary page is not visible or contains errors, check if all required fields have been completed correctly.

## Model Endpoint Dashboard
After successfully creating model endpoints, you will see the following screen.

### Overview
In the overview tab, you can see the Endpoint Details and Plan Details.
![Overview](https://docs.e2enetworks.com/assets/images/Updated_inference_overview-3c981ee1e776c2c8a2bfd3f805cf0a95.png)

**UI Elements:**

*   Overview tab
*   Endpoint details
*   Plan details

**User Actions:**

1.  View endpoint details
2.  View plan details

**Expected Results:**

*   Endpoint details and plan details will be displayed in overview tab.

### Async Invocations
In the Async Invocation tab, Users can enable asynchronous invocation for inference based on their specific requirements. This feature allows inference tasks to be processed asynchronously, ensuring seamless operation. Meanwhile, synchronous operations are prioritized for immediate processing.
By clicking on Setup Queues, user can select the destination so that response obtained from application route setup can be stored in target destination and click on submit.
After Async Invocation setup for selected Model Endpoint is enabled and queue setup done then users can view all queues with application path under Async Invocations tab.
By selecting API Request users can initiate asynchronous requests to specified Model Endpoint in following ways:
Using curl command.
Using OpenAI Python SDK.
Below screenshot attached for async request using curl command:
If you want make asynchronous request using OpenAI Python SDK follow these steps:
Install OpenAI client.
Paste whole code in python shell or script given in screenshot.
v1/chat/completions endpoint will only work for chat/instruct models if you using base model then must provide chat template get valid responses.
By clicking on Async Request Status users can view all asynchronous requests made selected inference along with request IDs these IDs used match corresponding asynchronous responses.
To update queues destination user click Modify Queues.
By selecting Modify Queues users add delete queues update destination dataset.
Click Disable Async Invocation disable Async Invocations created inference.
![Async Invocations](https://docs.e2enetworks.com/assets/images/Async_Invocations-9bc988fc568bbdbd05050ce8cddc35c4.png)

### Logs
In log tab logs generated view them clicking log tab.

### Deployment Events
In Deployments Events tab information about Deployment Events provided.

### Request Logs
In Request log tab Request logs generated view them clicking tab.

### Monitoring
In Monitoring tab choose between Hardware Service metric types Under Hardware find details like GPU Utilization GPU Memory Utilization GPU Temperature GPU Power Usage CPU Utilization Memory Usage.

### Serverless Configuration
In Serverless Configuration modify both Active Worker Max Worker counts If Active Worker count not equal Max Worker autoscaling enabled.

### Search Model Endpoint
In search model endpoint tab search model endpoint name apply advanced filter configurations refine search criteria.

## Actions
To stop Model Endpoint click stop service option To Start Model Endpoint service when stopped status click start service option To update model endpoint click Update Inference To delete model endpoint click delete action
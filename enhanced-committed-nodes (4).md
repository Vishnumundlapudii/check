# Model Endpoints
=====================================================

## Introduction
---------------

This document provides a step-by-step guide on creating model endpoints using TIR's pre-built containers and deploying containers that serve model API endpoints for AI inference services.

## Deploying Model Endpoints
---------------------------

TIR provides two methods for deploying containers that serve model API endpoints for AI inference services:

*   Deploy Using Pre-built Containers (Provided by TIR)
*   Deploy using your own container

### Deploy Using Pre-built Containers (Provided by TIR)

Before launching a service with TIR's pre-built containers, you need to create a TIR Model and upload the necessary model files. These containers are configured to automatically download model files from an EOS (E2E Object Storage) Bucket and start the API server. Once the endpoint is ready, you can make synchronous requests to the endpoint for inference.

### Deploy using your own container

You can launch an inference service using your own Docker image, either public or private. Once the endpoint is ready, you can make synchronous requests for inference. Optionally, you can attach a TIR model to automate the download of model files from an EOS bucket to the container.

## Create Model Endpoints
-------------------------

### Step 1: Navigate to Inference

Navigate to Inference: Click on "Model Endpoints."

![Model Endpoints](https://docs.e2enetworks.com/assets/images/model_endpoint1-3d26d1bb83f8851e0f7ddc503c584d46.png)

### Step 2: Create an Endpoint

Create an Endpoint: Click on the "CREATE ENDPOINT" button.

![Create Model Endpoint](https://docs.e2enetworks.com/assets/images/create_modelendpoint-257c920a02c0b790d66235208c93786e.png)

### Step 3: Choose a Framework

Choose a Framework:

You can use the search bar to explore the available frameworks.

![Choose Framework](https://docs.e2enetworks.com/assets/images/inference_create_new_framework-f2abec2c4e8ab9bef4dcea94222db643.png)

### Step 4: Link with Model Repository

Link with Model Repository and select from Model Repository.

![Link with Model Repository](https://docs.e2enetworks.com/assets/images/inference_create_new_link_model_repo-b2244b5c7865fbfda217c8332cf73ed0.png)

### Step 5: Download from Huggingface

Download from Huggingface and select token from HF Token Integration.

![Download from Huggingface](https://docs.e2enetworks.com/assets/images/inference_create_new_from_huggingface-6153261681f1c0fdc7cd0e064d223d59.png)

### Step 6: Create New Integration

In case any HF Token is not integrated, then click on Click Here to create a new Integration.

![Create New Integration](https://docs.e2enetworks.com/assets/images/inference_create_new_click_new-de612d584778a4bd52cf66747deaad9e.png)

Add Integration Name and Hugging Face Token and then click on create.

![Add Integration](https://docs.e2enetworks.com/assets/images/inference_create_new_integration-f5c54d9f32c60ac613c9ce313433a555.png)

## Plan Details
--------------

### Machine

Here you can select a machine type, either GPU or CPU. While selecting the plan, you can choose the plan for the inference from Committed or Hourly Billed.

You can apply filters to the available machines to refine your search results.

![Machine Selection](https://docs.e2enetworks.com/assets/images/inference_create_new_plan_gpu-4a0b6e902b5318ebc22a517d10a10af8.png)

### LLM Settings (Optional)

LLM settings encompass various configurations that define the model's behavior, efficiency, and performance during inference. These settings are categorized into three key areas: LLM Settings, Tokenizer Settings, and System Settings, each playing a crucial role in optimizing the model's output and deployment.

#### LLM Settings

LLM settings define the behavior, accuracy, and efficiency of a large language model during inference. Key parameters include Load Format (auto, pt, safetensors, etc.), Data Type (auto, float16, etc.), KV Cache Data Type, Quantization, and many more. Optimizing these settings ensures precise and contextually relevant outputs.

![LLM Setting](https://docs.e2enetworks.com/assets/images/llm_setting_img-217d177523ba2a926477583e5ec68406.png)

#### Tokenizer Settings

Tokenizer settings determine how text is split into tokens, impacting model efficiency and comprehension. Parameters such as Tokenizer, Tokenizer Revision, and Custom Chat Template influence how input text is processed and interpreted before inference.

![Tokenizer Setting](https://docs.e2enetworks.com/assets/images/token_setting-9e73027630a70681b71b768cf2be77ae.png)

#### System Settings

System settings manage the hardware and computational aspects of LLM deployment. These include GPU utilization, Max Parallel Loading Workers, Block Size, and Swap Space to maximize performance and cost efficiency.

![System Setting](https://docs.e2enetworks.com/assets/images/system_setting_img-dd4f5b70178026a715803cfaac1dfbfe.png)

### Serverless Configuration

For Hourly Billed Inference, it's possible to set the Active Workers to 0. You can set the number of Active Workers to any value from 0 up to the max workers. When there are no incoming requests, the number of active workers automatically reduces to 0, ensuring that no billing is incurred for that period.

For Committed Inference, the Active Workers cannot be set to 0, and the number of active workers must always remain greater than 0, ensuring the committed nature of Inference. You can set the number of Active Workers to any value from 1 up to the max workers.

All additional inferences, which are added automatically due to the autoscaling feature, will be charged at an hourly billing rate. Similarly, if the Active Worker count is increased from a serverless configuration after the inference is created, those additional inferences will also be billed at the hourly rate.

![Hourly Billed Serverless Configuration](https://docs.e2enetworks.com/assets/images/inference_hourly_serverless_config-5a51bd0bf23a39f02ac232aafcb8a90f.png)

## Environment Variables
----------------------

### Add Variable

You can add a variable by clicking the ADD VARIABLE button.

## Summary
----------

You can view the endpoint summary on the summary page, and if needed, modify any section of the inference creation process by clicking the edit button.

## Model Endpoint Dashboard
---------------------------

After successfully creating model endpoints, you will see the following screen.

### Overview

In the overview tab, you can see the Endpoint Details and Plan Details.

![Overview](https://docs.e2enetworks.com/assets/images/Updated_inference_overview-3c981ee1e776c2c8a2bfd3f805cf0a95.png)

### Async Invocations

In the Async Invocation tab, Users can enable asynchronous invocation for inference based on their specific requirements. This feature allows inference tasks to be processed asynchronously, ensuring seamless operation. Meanwhile, synchronous operations are prioritized for immediate processing.

By clicking on Setup Queues, user can select the destination so that response obtained from application route setup can be stored in the target destination and click on submit.

After the Async Invocation to the selected Model Endpoint is enabled and queue is set up, then the users can view all the queues with application path under the Async Invocations tab.

By selecting API Request, users can initiate asynchronous requests to the specified Model Endpoint in the following ways:

*   Using a curl command
*   Using the OpenAI Python SDK

Below is the screenshot attached for async request using curl command:

![API Request using curl](https://docs.e2enetworks.com/assets/images/curl_req-9181a44fd1636b83438c9e9e94ecef0a.png)

If you want to make an asynchronous request using the OpenAI Python SDK, follow these steps:

*   Install the OpenAI client
*   Paste the whole code in python shell or script given in screenshot

v1/chat/completions endpoint will only work for chat/instruct models, if you are using base model then you must provide a chat template to get valid responses.

By clicking on Async Request Status, users can view all asynchronous requests made to the selected inference, along with the request IDs. These IDs can be used to match the corresponding asynchronous responses.

To update queues and destination, user can click on Modify Queues.

By selecting Modify Queues, users can add or delete queues and update the destination dataset.

Click on Disable Async Invocation to disable Async Invocations for the created inference.

### Logs

In the log tab, logs are generated, and you can view them by clicking on the log tab.

![Logs](https://docs.e2enetworks.com/assets/images/Updated_inference_logs-c2c77f5582d5b31ae2f3fd2c38b5a6b8.png)

### Deployment Events

In the Deployments Events tab, information about Deployment Events is provided.

![Deployment Events](https://docs.e2enetworks.com/assets/images/Updated_inference_deploymentevent-b959f2e01b6bcc42192fe8be1d6288d4.png)

### Request Logs

In the Request log tab, Request logs are generated, and you can view them by clicking on the tab.

![Request Logs](https://docs.e2enetworks.com/assets/images/Updated_inference_accesslogs-2137b8376fd868f8e81999357be33291.png)

### Monitoring

In the Monitoring tab, you can choose between Hardware and Service as metric types. Under Hardware, you'll find details like GPU Utilization, GPU Memory Utilization, GPU Temperature, GPU Power Usage, CPU Utilization, and Memory Usage.

![Monitoring](https://docs.e2enetworks.com/assets/images/Updated_inference_monitoring-ac797ce90c693caa9550114149467c11.png)

### Serverless Configuration

In the Serverless Configuration, you can modify both the Active Worker and Max Worker counts. If the Active Worker count is not equal to the Max Worker, autoscaling will be enabled.

![Serverless Configuration](https://docs.e2enetworks.com/assets/images/inference_update_serverless_config-6f6ce6de7dbed4ef73579079e82dc80d.png)

### Search Model Endpoint

In the search model endpoint tab, you can search for the model endpoint by name and apply advanced filter configurations to refine your search criteria.

![Search Model Endpoint](https://docs.e2enetworks.com/assets/images/inference_search-bfc744d3193e72d3e79d5ea66d451d1c.png)

## Actions
----------

To stop a Model Endpoint, you have to click on the stop service option.

To Start Model Endpoint service when it is in stopped status, you have to click on start service option.

To update model endpoint, click on Update Inference

To delete model endpoint, click on delete action.
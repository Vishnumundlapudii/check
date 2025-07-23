```markdown
---
title: "Model Endpoints"
description: "TIR provides two methods for deploying containers that serve model API endpoints for AI inference services."
sidebar_position: 1
slug: /model-endpoints
tags: [model-endpoints, tir, ai-inference]
---

# Model Endpoints

TIR provides two methods for deploying containers that serve model API endpoints for AI inference services: Deploy Using Pre-built Containers (Provided by TIR) and Deploy using your own container.

## Create Model Endpoints

To create a model endpoint:

### Navigate to Inference

Click on "Model Endpoints."

![Model Endpoints](https://docs.e2enetworks.com/assets/images/model_endpoint1-3d26d1bb83f8851e0f7ddc503c584d46.png)

*   Key UI elements visible: Model Endpoints button
*   Essential user actions required: Click on the Model Endpoints button
*   Expected results: The Model Endpoints page will be displayed

### Create an Endpoint

Click on the "CREATE ENDPOINT" button.

![Create Model Endpoint](https://docs.e2enetworks.com/assets/images/create_modelendpoint-257c920a02c0b790d66235208c93786e.png)

*   Key UI elements visible: CREATE ENDPOINT button
*   Essential user actions required: Click on the CREATE ENDPOINT button
*   Expected results: The Create Endpoint page will be displayed

### Choose a Framework

You can use the search bar to explore the available frameworks.

![Choose Framework](https://docs.e2enetworks.com/assets/images/inference_create_new_framework-f2abec2c4e8ab9bef4dcea94222db643.png)

*   Key UI elements visible: Search bar, framework list
*   Essential user actions required: Select a framework from the list or search for a specific framework
*   Expected results: The selected framework will be displayed

### Link with Model Repository

Click on Link with Model Repository and select from Model Repository.

![Link with Model Repository](https://docs.e2enetworks.com/assets/images/inference_create_new_link_model_repo-b2244b5c7865fbfda217c8332cf73ed0.png)

*   Key UI elements visible: Link with Model Repository button, Model Repository list
*   Essential user actions required: Click on the Link with Model Repository button and select a repository from the list
*   Expected results: The selected repository will be linked to the model endpoint

### Download from Huggingface

Click on Download from Huggingface and select token from HF Token Integration.

![Download from Huggingface](https://docs.e2enetworks.com/assets/images/inference_create_new_from_huggingface-6153261681f1c0fdc7cd0e064d223d59.png)

*   Key UI elements visible: Download from Huggingface button, HF Token Integration list
*   Essential user actions required: Click on the Download from Huggingface button and select a token from the list
*   Expected results: The selected token will be used to download the model from Huggingface

## Plan Details

### Machine

Here you can select a machine type, either GPU or CPU. While selecting the plan, you can choose the plan for the inference from Committed or Hourly Billed.

![Machine Selection](https://docs.e2enetworks.com/assets/images/inference_create_new_plan_gpu-4a0b6e902b5318ebc22a517d10a10af8.png)

*   Key UI elements visible: Machine type selection, plan selection
*   Essential user actions required: Select a machine type and plan
*   Expected results: The selected machine type and plan will be applied to the model endpoint

### LLM Settings (Optional)

LLM settings encompass various configurations that define the model's behavior, efficiency, and performance during inference.

![LLM Setting](https://docs.e2enetworks.com/assets/images/llm_setting_img-217d177523ba2a926477583e5ec68406.png)

*   Key UI elements visible: LLM settings configuration
*   Essential user actions required: Configure LLM settings as desired
*   Expected results: The configured LLM settings will be applied to the model endpoint

### Tokenizer Settings

Tokenizer settings determine how text is split into tokens, impacting model efficiency and comprehension.

![Tokenizer Setting](https://docs.e2enetworks.com/assets/images/token_setting-9e73027630a70681b71b768cf2be77ae.png)

*   Key UI elements visible: Tokenizer settings configuration
*   Essential user actions required: Configure tokenizer settings as desired
*   Expected results: The configured tokenizer settings will be applied to the model endpoint

### System Settings

System settings manage the hardware and computational aspects of LLM deployment.

![System Setting](https://docs.e2enetworks.com/assets/images/system_setting_img-dd4f5b70178026a715803cfaac1dfbfe.png)

*   Key UI elements visible: System settings configuration
*   Essential user actions required: Configure system settings as desired
*   Expected results: The configured system settings will be applied to the model endpoint

### Serverless Configuration

For Hourly Billed Inference, it's possible to set the Active Workers to 0.

![Hourly Billed Serverless Configuration](https://docs.e2enetworks.com/assets/images/inference_hourly_serverless_config-5a51bd0bf23a39f02ac232aafcb8a90f.png)

*   Key UI elements visible: Serverless configuration settings
*   Essential user actions required: Configure serverless settings as desired
*   Expected results: The configured serverless settings will be applied to the model endpoint

## Environment Variables

You can add a variable by clicking the ADD VARIABLE button.

![Add Variable](https://docs.e2enetworks.com/assets/images/inference_hourly_env-ebb7ef3a76005c811b67deb6ec6793d1.png)

*   Key UI elements visible: ADD VARIABLE button
*   Essential user actions required: Click on the ADD VARIABLE button and add a variable
*   Expected results: The added variable will be applied to the model endpoint

## Summary

You can view the endpoint summary on the summary page, and if needed, modify any section of the inference creation process by clicking the edit button.

## Model Endpoint Dashboard

After successfully creating model endpoints, you will see the following screen.

### Overview

In the overview tab, you can see the Endpoint Details and Plan Details.

![Overview](https://docs.e2enetworks.com/assets/images/Updated_inference_overview-3c981ee1e776c2c8a2bfd3f805cf0a95.png)

*   Key UI elements visible: Endpoint Details, Plan Details
*   Essential user actions required: View endpoint details and plan details
*   Expected results: The endpoint details and plan details will be displayed

### Async Invocations

In the Async Invocation tab, Users can enable asynchronous invocation for inference based on their specific requirements.

![Async Invocations](https://docs.e2enetworks.com/assets/images/Async_Invocations-9bc988fc568bbdbd05050ce8cddc35c4.png)

*   Key UI elements visible: Async Invocation settings
*   Essential user actions required: Configure async invocation settings as desired
*   Expected results: The configured async invocation settings will be applied to the model endpoint

### Logs

In the log tab, logs are generated, and you can view them by clicking on the log tab.

![Logs](https://docs.e2enetworks.com/assets/images/Updated_inference_logs-c2c77f5582d5b31ae2f3fd2c38b5a6b8.png)

*   Key UI elements visible: Logs
*   Essential user actions required: View logs
*   Expected results: The logs will be displayed

### Deployment Events

In the Deployments Events tab, information about Deployment Events is provided.

![Deployment Events](https://docs.e2enetworks.com/assets/images/Updated_inference_deploymentevent-b959f2e01b6bcc42192fe8be1d6288d4.png)

*   Key UI elements visible: Deployment Events information
*   Essential user actions required: View deployment events information
*   Expected results: The deployment events information will be displayed

### Request Logs

In the Request log tab, Request logs are generated, and you can view them by clicking on the tab.

![Request Logs](https://docs.e2enetworks.com/assets/images/Updated_inference_accesslogs-2137b8376fd868f8e81999357be33291.png)

*   Key UI elements visible: Request logs
*   Essential user actions required: View request logs
*   Expected results: The request logs will be displayed

### Monitoring

In the Monitoring tab, you can choose between Hardware and Service as metric types.

![Monitoring](https://docs.e2enetworks.com/assets/images/Updated_inference_monitoring-ac797ce90c693caa9550114149467c11.png)

*   Key UI elements visible: Monitoring settings
*   Essential user actions required: Configure monitoring settings as desired
*   Expected results: The configured monitoring settings will be applied to the model endpoint

### Serverless Configuration

In the Serverless Configuration, you can modify both the Active Worker and Max Worker counts.

![Serverless Configuration](https://docs.e2enetworks.com/assets/images/inference_update_serverless_config-6f6ce6de7dbed4ef73579079e82dc80d.png)

*   Key UI elements visible: Serverless configuration settings
*   Essential user actions required: Configure serverless settings as desired
*   Expected results: The configured serverless settings will be applied to the model endpoint

### Search Model Endpoint

In the search model endpoint tab, you can search for the model endpoint by name and apply advanced filter configurations to refine your search criteria.

![Search Model Endpoint](https://docs.e2enetworks.com/assets/images/inference_search-bfc744d3193e72d3e79d5ea66d451d1c.png)

*   Key UI elements visible: Search bar, filter configurations
*   Essential user actions required: Search for a model endpoint by name and apply filter configurations as desired
*   Expected results: The search results will be displayed

## Actions

To stop a Model Endpoint, you have to click on the stop service option.

![Stop Model Endpoint](https://docs.e2enetworks.com/assets/images/Stop_model_endpoint-a8ea166bce796650092c690a07b389b9.png)

*   Key UI elements visible: Stop service option
*   Essential user actions required: Click on the stop service option
*   Expected results: The model endpoint will be stopped

To Start Model Endpoint service when it is in stopped status, you have to click on start service option.

![Start Model Endpoint](https://docs.e2enetworks.com/assets/images/Start_model_endpoint-a3c8daea120a25b05e65ac07e5a7f9a5.png)

*   Key UI elements visible: Start service option
*   Essential user actions required: Click on the start service option
*   Expected results: The model endpoint will be started

To update model endpoint, click on Update Inference.

![Update Model Endpoint](https://docs.e2enetworks.com/assets/images/Update_model_endpoint-4034238c9164fa871c868f3fd00b8eec.png)

*   Key UI elements visible: Update Inference option
*   Essential user actions required: Click on the Update Inference option
*   Expected results: The model endpoint will be updated

To delete model endpoint, click on delete action.

![Delete Model Endpoint](https://docs.e2enetworks.com/assets/images/Delete_model_endpoint-4078e984932700fa926973c4537274c5.png)

*   Key UI elements visible: Delete option
*   Essential user actions required: Click on the delete option
*   Expected results: The model endpoint will be deleted
<div style="display: flex; gap: 2rem;">

<div style="flex: 1; max-width: calc(100% - 280px);">

# Model Endpoints - TIR Inference Platform

> **Enhanced Documentation with Right-Side Navigation**  
> Platform: E2E Networks TIR AI Platform | Section: Inference | Last Updated: January 2024

## Introduction

Model Endpoints on the TIR Inference Platform provide scalable, production-ready deployment solutions for machine learning models with support for both pre-built containers and custom Docker environments. The platform offers flexible billing options, comprehensive monitoring, and enterprise-grade performance optimization.

### Key Features

- **🚀 Multiple Deployment Options:** Pre-built TIR containers or custom Docker containers
- **⚡ Flexible Scaling:** Serverless autoscaling with min/max instance configuration
- **🖥️ Hardware Flexibility:** CPU and GPU instances with various configurations
- **📊 Comprehensive Monitoring:** Built-in dashboards and performance metrics
- **💰 Cost Optimization:** Both committed and hourly billing models
- **🔧 Advanced Configuration:** LLM settings, quantization, and tokenizer customization

### Deployment Methods Comparison

| Method | Best For | Configuration Complexity | Time to Deploy |
|--------|----------|-------------------------|----------------|
| **Pre-built TIR Containers** | Standard ML models, quick deployment | Low | 5-10 minutes |
| **Custom Docker Containers** | Specialized models, custom environments | Medium-High | 15-30 minutes |

---

## Create Model Endpoints

### Prerequisites

Before creating a model endpoint, ensure you have:

- [ ] Active E2E Networks TIR account with inference permissions
- [ ] Model artifacts ready (weights, configuration files)
- [ ] Understanding of your model's resource requirements
- [ ] Decision on deployment method (pre-built vs custom container)
- [ ] Knowledge of expected traffic patterns for scaling configuration

### Step-by-Step Creation Process

#### Step 1: Access Model Endpoints Interface

**Navigation Path:**
```
TIR Dashboard → Inference → Model Endpoints → Create Endpoint
```

**Interface Elements:**
- **Header Navigation:** "Inference" section highlighted
- **Sidebar Menu:** "Model Endpoints" option selected
- **Main Action:** "Create Endpoint" button prominently displayed
- **Overview Panel:** Existing endpoints listed (if any)

**What to Expect:**
- Clean interface with clear deployment options
- Summary of current resource usage
- Quick access to documentation and examples

---

#### Step 2: Select Deployment Method

**Method 1: Pre-built TIR Containers**

| Framework | Supported Versions | Pre-installed Libraries | Use Cases |
|-----------|-------------------|------------------------|-----------|
| **PyTorch** | 1.x, 2.x | transformers, torch-serve, fastapi | Deep learning models, NLP |
| **TensorFlow** | 2.x | tf-serving, keras, tensorflow-hub | Computer vision, structured data |
| **ONNX** | Latest | onnxruntime, optimum | Cross-platform inference |
| **Custom** | User-defined | User-specified | Specialized frameworks |

**Method 2: Custom Docker Containers**

**Container Requirements:**
- **Base Image:** Any Linux-based image (Ubuntu, Alpine, etc.)
- **Exposed Port:** Must expose port 8000 for inference requests
- **Health Check:** Implement `/health` endpoint for monitoring
- **Model Loading:** Handle model initialization and memory management
- **API Interface:** REST API for inference requests

**Selection Criteria:**
- **Pre-built:** Choose for standard models with common frameworks
- **Custom:** Select for proprietary models, special preprocessing, or unique dependencies

---

#### Step 3: Configure Model Repository

### Model Source Options

| Source Type | Configuration | Authentication | Best For |
|-------------|---------------|----------------|----------|
| **Hugging Face Hub** | Model ID (e.g., `microsoft/DialoGPT-medium`) | HF token (optional) | Public models, quick deployment |
| **Git Repository** | Git URL + branch/tag | SSH keys or access tokens | Version-controlled models |
| **Cloud Storage** | S3/GCS bucket path | Cloud credentials | Large model files |
| **TIR Model Registry** | Model name + version | TIR authentication | Internal model management |

**Repository Configuration Steps:**
1. **Select Source Type** from dropdown menu
2. **Enter Repository Details** (URL, model ID, or path)
3. **Configure Authentication** if required (tokens, keys, credentials)
4. **Specify Model Path** within repository (if not in root)
5. **Set Version/Branch** for version control
6. **Validate Connection** using "Test Connection" button

**Model Structure Requirements:**
```
model_repository/
├── model.py                 # Model class definition
├── requirements.txt         # Python dependencies
├── config.json             # Model configuration
├── weights/                # Model weights directory
│   ├── pytorch_model.bin
│   └── config.json
└── tokenizer/              # Tokenizer files (for NLP)
    ├── tokenizer.json
    └── vocab.txt
```

---

#### Step 4: Machine and GPU Selection

### Available Instance Types

#### CPU-Optimized Instances

| Instance Type | vCPUs | Memory | Network | Hourly Cost | Best For |
|---------------|-------|--------|---------|-------------|----------|
| **c6i.large** | 2 | 4 GB | Up to 12.5 Gbps | ₹3.2 | Light inference, testing |
| **c6i.xlarge** | 4 | 8 GB | Up to 12.5 Gbps | ₹6.4 | Medium throughput models |
| **c6i.2xlarge** | 8 | 16 GB | Up to 12.5 Gbps | ₹12.8 | High-throughput CPU inference |
| **c6i.4xlarge** | 16 | 32 GB | 25 Gbps | ₹25.6 | Large models, batch processing |

#### GPU-Accelerated Instances

| Instance Type | GPU | GPU Memory | vCPUs | System Memory | Hourly Cost | Best For |
|---------------|-----|------------|-------|---------------|-------------|----------|
| **g4dn.xlarge** | NVIDIA T4 | 16 GB | 4 | 16 GB | ₹15.8 | Small to medium models |
| **g4dn.2xlarge** | NVIDIA T4 | 16 GB | 8 | 32 GB | ₹28.4 | Medium models, higher throughput |
| **p3.2xlarge** | NVIDIA V100 | 16 GB | 8 | 61 GB | ₹52.7 | Large models, training |
| **p4d.xlarge** | NVIDIA A100 | 40 GB | 8 | 96 GB | ₹89.3 | Largest models, high performance |

**Selection Guidelines:**
- **Model Size:** Ensure GPU memory > model size + inference overhead
- **Batch Size:** Larger batches require more memory but improve throughput
- **Latency Requirements:** V100/A100 for low-latency applications
- **Cost Optimization:** Start small and scale based on actual usage

**Performance Considerations:**
```python
# Memory estimation formula
required_memory = (model_size_gb * precision_multiplier) + batch_size * sequence_length * hidden_size * 4
```

Where:
- `precision_multiplier`: 4 for FP32, 2 for FP16, 1 for INT8
- Additional 20-30% overhead for inference framework

---

#### Step 5: LLM Settings Configuration

### Load Format Options

| Format | Description | Memory Usage | Speed | Quality | Use Case |
|--------|-------------|--------------|-------|---------|----------|
| **Auto** | Automatic optimal format selection | Variable | Good | High | General purpose, recommended |
| **FP32** | 32-bit floating point | Highest | Slower | Best | Research, maximum accuracy |
| **FP16** | 16-bit floating point | Medium | Faster | Good | Production, balanced performance |
| **INT8** | 8-bit integer quantization | Lowest | Fastest | Reduced | High-throughput, cost-optimized |

### Data Type Configuration

**Available Data Types:**
- **float32:** Standard precision, maximum compatibility
- **float16:** Half precision, 2x memory reduction, modern GPU optimized
- **bfloat16:** Brain float, better numerical stability than FP16
- **int8:** Quantized inference, significant memory and compute savings

### Quantization Settings

| Quantization Method | Memory Reduction | Speed Improvement | Quality Impact | Supported Models |
|--------------------|------------------|-------------------|----------------|------------------|
| **Dynamic Quantization** | 50-75% | 1.5-2x | Minimal | Most PyTorch models |
| **Static Quantization** | 75% | 2-3x | Small | Post-training calibration |
| **QAT (Quantization Aware)** | 75% | 2-3x | Minimal | Specially trained models |

**Quantization Configuration:**
```json
{
  "quantization": {
    "method": "dynamic",
    "data_type": "int8",
    "calibration_dataset": "optional_dataset_path",
    "accuracy_threshold": 0.95
  }
}
```

### Tokenizer Settings

**Configuration Options:**
- **Tokenizer Type:** BPE, WordPiece, SentencePiece
- **Vocabulary Size:** Model-specific, typically 32k-50k tokens
- **Special Tokens:** Handling for padding, unknown, start/end tokens
- **Truncation Strategy:** How to handle sequences exceeding max length
- **Padding Strategy:** Left, right, or no padding

### System Settings

| Setting | Options | Default | Description |
|---------|---------|---------|-------------|
| **Max Sequence Length** | 128-8192 tokens | 2048 | Maximum input/output sequence length |
| **Batch Size** | 1-64 | 1 | Number of requests processed together |
| **Temperature** | 0.1-2.0 | 1.0 | Randomness in text generation |
| **Top-k Sampling** | 1-100 | 50 | Consider top-k tokens for sampling |
| **Top-p Sampling** | 0.1-1.0 | 0.9 | Nucleus sampling probability threshold |

---

#### Step 6: Serverless Configuration

### Auto-scaling Settings

| Parameter | Range | Default | Description |
|-----------|-------|---------|-------------|
| **Min Instances** | 0-10 | 1 | Minimum number of running instances |
| **Max Instances** | 1-100 | 10 | Maximum number of instances for scaling |
| **Target Concurrency** | 1-1000 | 10 | Requests per instance before scaling |
| **Scale-up Threshold** | 50-95% | 80% | CPU/memory utilization trigger |
| **Scale-down Delay** | 60-3600s | 300s | Wait time before scaling down |

### Cold Start Optimization

**Cold Start Mitigation Strategies:**
1. **Warm Pool:** Maintain minimum instances to reduce cold starts
2. **Model Caching:** Pre-load models in memory for faster initialization
3. **Container Optimization:** Use smaller, optimized base images
4. **Health Check Tuning:** Optimize health check intervals

**Cold Start Performance:**
| Instance Type | Model Size | Cold Start Time | Warm Start Time |
|---------------|------------|-----------------|-----------------|
| **CPU (small model)** | <1GB | 30-60s | 1-3s |
| **GPU (medium model)** | 1-5GB | 60-120s | 2-5s |
| **GPU (large model)** | >5GB | 120-300s | 5-15s |

### Cost Optimization

**Billing Models:**
- **Per Request:** Pay only for actual inference requests
- **Per Hour:** Fixed hourly rate regardless of usage
- **Committed:** Discounted rates for guaranteed usage periods

**Cost Calculation Example:**
```
# Serverless costs
Per request: ₹0.001 per request + ₹15.8/hour for active instances
Monthly estimate: (requests_per_month * ₹0.001) + (active_hours * hourly_rate)

# Committed costs
60-day commitment: 25% discount on hourly rates
90-day commitment: 30% discount on hourly rates
```

---

#### Step 7: Environment Variables

### Standard Environment Variables

| Variable | Purpose | Example Value | Required |
|----------|---------|---------------|----------|
| **MODEL_PATH** | Path to model files | `/opt/model` | Yes |
| **MAX_WORKERS** | Number of worker processes | `4` | No |
| **LOG_LEVEL** | Logging verbosity | `INFO` | No |
| **CUDA_VISIBLE_DEVICES** | GPU device selection | `0,1` | No (GPU only) |
| **TRANSFORMERS_CACHE** | HuggingFace cache directory | `/tmp/transformers` | No |

### Custom Environment Variables

**Configuration Format:**
```json
{
  "environment_variables": {
    "CUSTOM_CONFIG_PATH": "/opt/config/model.json",
    "API_TIMEOUT": "30",
    "BATCH_SIZE": "8",
    "USE_TENSORRT": "true"
  }
}
```

**Best Practices:**
- **Security:** Never store secrets in environment variables (use TIR Secrets Manager)
- **Validation:** Validate environment variables in application startup
- **Documentation:** Document all custom variables for team members
- **Defaults:** Provide sensible defaults for optional variables

### Secrets Management

**Using TIR Secrets Manager:**
```python
import os
from tir_secrets import get_secret

# Instead of: api_key = os.getenv('API_KEY')
api_key = get_secret('model-api-key')
database_url = get_secret('database-connection-string')
```

---

#### Step 8: Summary and Deployment

### Pre-Deployment Checklist

- [ ] **Model Configuration:** Verified model path and access permissions
- [ ] **Resource Allocation:** Confirmed instance type meets model requirements
- [ ] **Scaling Configuration:** Set appropriate min/max instances
- [ ] **Environment Variables:** All required variables configured
- [ ] **Health Checks:** Endpoint and timeout configured
- [ ] **Monitoring:** Alerts and dashboards enabled
- [ ] **Cost Estimation:** Reviewed projected costs and budget alignment

### Deployment Timeline

| Phase | Duration | Activities | Status Indicators |
|-------|----------|------------|-------------------|
| **Validation** | 30-60s | Configuration validation, resource checking | "Validating configuration..." |
| **Container Build** | 2-5 minutes | Custom container builds (if applicable) | "Building container..." |
| **Resource Allocation** | 1-3 minutes | GPU/CPU provisioning, network setup | "Allocating resources..." |
| **Model Loading** | 1-10 minutes | Model download and initialization | "Loading model..." with progress |
| **Health Check** | 30-60s | Endpoint availability verification | "Running health checks..." |
| **Ready** | 5-20 minutes total | Endpoint available for inference | Green "Active" status |

### Post-Deployment Verification

**Immediate Checks:**
```bash
# Health check
curl -X GET https://your-endpoint.tir.e2enetworks.com/health

# Sample inference
curl -X POST https://your-endpoint.tir.e2enetworks.com/v1/chat/completions \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer YOUR_API_KEY" \
  -d '{
    "model": "your-model-name",
    "messages": [{"role": "user", "content": "Hello, world!"}],
    "max_tokens": 100
  }'
```

**Performance Validation:**
- **Response Time:** < 5s for first request (cold start), < 1s for subsequent requests
- **Throughput:** Verify requests/second meets requirements
- **Resource Utilization:** Monitor CPU/GPU usage during load testing
- **Error Rates:** Should be < 1% for properly configured endpoints

---

## Model Endpoint Dashboard

### Overview Metrics

The Model Endpoint Dashboard provides comprehensive monitoring and management capabilities for deployed models.

#### Key Performance Indicators

| Metric | Description | Healthy Range | Alert Thresholds |
|--------|-------------|---------------|------------------|
| **Request Latency** | Average response time | < 1000ms | > 5000ms (critical) |
| **Requests/Second** | Throughput rate | Varies by model | > 80% of capacity |
| **Error Rate** | Failed requests percentage | < 1% | > 5% (warning), > 10% (critical) |
| **GPU Utilization** | GPU usage percentage | 60-80% | < 20% (underutilized), > 95% (overloaded) |
| **Memory Usage** | RAM/GPU memory consumption | < 80% | > 90% (warning), > 95% (critical) |

#### Real-time Monitoring

**Dashboard Sections:**
1. **Performance Overview:** Request volume, latency trends, error rates
2. **Resource Utilization:** CPU, memory, GPU usage graphs
3. **Scaling Activity:** Instance count, scaling events, cold starts
4. **Cost Analysis:** Real-time cost tracking and projections
5. **Health Status:** Service availability and endpoint health

**Alert Configuration:**
```json
{
  "alerts": {
    "high_latency": {
      "threshold": "5000ms",
      "duration": "5m",
      "notification": ["email", "slack"]
    },
    "error_rate": {
      "threshold": "5%",
      "duration": "2m",
      "notification": ["email", "pager"]
    },
    "gpu_memory": {
      "threshold": "90%",
      "duration": "10m",
      "notification": ["email"]
    }
  }
}
```

### Traffic Analytics

#### Request Patterns

| Time Period | Typical Patterns | Optimization Strategy |
|-------------|------------------|----------------------|
| **Peak Hours** | 2-5x average traffic | Pre-scale instances, enable aggressive scaling |
| **Off-Peak** | 10-50% of peak | Reduce min instances, longer scale-down delays |
| **Weekend** | 20-70% of weekday | Adjust scaling policies, consider scheduling |

#### Usage Statistics

**Weekly Report Example:**
- **Total Requests:** 1,250,000
- **Average Latency:** 847ms
- **Peak RPS:** 456 requests/second
- **Error Rate:** 0.3%
- **Top Error Types:** Timeout (45%), Model Error (30%), Rate Limit (25%)

### Cost Monitoring

#### Real-time Cost Tracking

**Cost Breakdown:**
- **Compute Costs:** Instance hours × hourly rate
- **Request Costs:** Number of requests × per-request rate (serverless)
- **Storage Costs:** Model storage and logs
- **Network Costs:** Data transfer and bandwidth

**Cost Optimization Insights:**
- **Underutilized Instances:** Instances running below 30% utilization
- **Scaling Efficiency:** Ratio of productive vs. idle instance time
- **Request Batching:** Opportunities to batch requests for cost savings

---

## Actions and Management

### Endpoint Management Actions

#### Scaling Operations

| Action | Purpose | Downtime | Considerations |
|--------|---------|----------|----------------|
| **Manual Scale Up** | Increase instance count | None | Immediate cost increase |
| **Manual Scale Down** | Decrease instance count | None | May affect performance |
| **Update Scaling Config** | Modify auto-scaling rules | None | Takes effect on next scaling event |
| **Emergency Scale** | Rapid scaling for traffic spikes | None | Higher costs for rapid provisioning |

**Scaling Commands:**
```bash
# Scale up immediately
tir endpoint scale --name my-model --instances 10

# Update scaling configuration
tir endpoint update-scaling --name my-model \
  --min-instances 2 --max-instances 20 --target-concurrency 15
```

#### Configuration Updates

**Hot Updates (No Downtime):**
- Environment variables
- Scaling parameters
- Monitoring settings
- Alert configurations

**Cold Updates (Requires Restart):**
- Model version changes
- Instance type changes
- Framework updates
- Major configuration changes

**Update Process:**
1. **Prepare Update:** Validate new configuration
2. **Rolling Deployment:** Gradually replace instances
3. **Health Verification:** Ensure new instances pass health checks
4. **Traffic Migration:** Shift traffic to updated instances
5. **Cleanup:** Remove old instances after verification

#### Monitoring and Debugging

**Log Management:**
- **Application Logs:** Model inference logs and errors
- **System Logs:** Container and infrastructure logs
- **Access Logs:** Request/response logging with privacy controls
- **Performance Logs:** Detailed timing and resource usage

**Log Access:**
```bash
# Stream real-time logs
tir endpoint logs --name my-model --follow

# Search historical logs
tir endpoint logs --name my-model --since="2024-01-15" --filter="ERROR"

# Download log archive
tir endpoint logs --name my-model --download --format=json
```

#### Troubleshooting Common Issues

| Issue | Symptoms | Potential Causes | Resolution |
|-------|----------|------------------|------------|
| **High Latency** | Slow response times | Model complexity, insufficient resources | Scale up instances, optimize model |
| **Memory Errors** | OOM exceptions, crashes | Large models, memory leaks | Increase instance size, fix memory leaks |
| **Cold Start Issues** | Slow first requests | Large models, complex initialization | Increase min instances, optimize startup |
| **Authentication Errors** | 401/403 responses | Invalid tokens, expired credentials | Refresh tokens, check permissions |

**Debugging Tools:**
- **Performance Profiler:** Identify bottlenecks in inference pipeline
- **Memory Analyzer:** Track memory usage and detect leaks
- **Request Tracer:** Follow request flow through system
- **Load Tester:** Simulate traffic patterns for testing

---

## API Reference

### Endpoint URLs and Authentication

**Base URL Structure:**
```
https://{endpoint-name}.{region}.tir.e2enetworks.com
```

**Authentication Methods:**
1. **API Key:** Header-based authentication for programmatic access
2. **JWT Token:** Short-lived tokens for web applications
3. **Service Account:** Long-lived credentials for service-to-service

### Inference API

#### Chat Completions API

**Endpoint:** `POST /v1/chat/completions`

**OpenAI Compatible API:**
```bash
curl -X POST https://your-endpoint.tir.e2enetworks.com/v1/chat/completions \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer YOUR_API_KEY" \
  -d '{
    "model": "your-model-name",
    "messages": [
      {"role": "system", "content": "You are a helpful assistant."},
      {"role": "user", "content": "Explain quantum computing"}
    ],
    "max_tokens": 150,
    "temperature": 0.7,
    "top_p": 0.9,
    "frequency_penalty": 0,
    "presence_penalty": 0,
    "stream": false
  }'
```

**Response Format:**
```json
{
  "id": "chatcmpl-123",
  "object": "chat.completion",
  "created": 1677652288,
  "model": "your-model-name",
  "choices": [
    {
      "index": 0,
      "message": {
        "role": "assistant",
        "content": "Quantum computing is a revolutionary computing paradigm..."
      },
      "finish_reason": "stop"
    }
  ],
  "usage": {
    "prompt_tokens": 25,
    "completion_tokens": 150,
    "total_tokens": 175
  }
}
```

#### Streaming Responses

**Enable Streaming:**
```javascript
const response = await fetch('https://your-endpoint.tir.e2enetworks.com/v1/chat/completions', {
  method: 'POST',
  headers: {
    'Content-Type': 'application/json',
    'Authorization': 'Bearer YOUR_API_KEY'
  },
  body: JSON.stringify({
    model: 'your-model-name',
    messages: [{role: 'user', content: 'Tell me a story'}],
    stream: true
  })
});

const reader = response.body.getReader();
while (true) {
  const { done, value } = await reader.read();
  if (done) break;
  
  const chunk = new TextDecoder().decode(value);
  const lines = chunk.split('\n').filter(line => line.trim() !== '');
  
  for (const line of lines) {
    if (line.startsWith('data: ')) {
      const data = line.slice(6);
      if (data !== '[DONE]') {
        const parsed = JSON.parse(data);
        console.log(parsed.choices[0].delta.content);
      }
    }
  }
}
```

### Async Invocation API

#### Submit Async Request

**Endpoint:** `POST /v1/async/chat/completions`

```bash
curl -X POST https://your-endpoint.tir.e2enetworks.com/v1/async/chat/completions \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer YOUR_API_KEY" \
  -d '{
    "model": "your-model-name",
    "messages": [{"role": "user", "content": "Analyze this large document..."}],
    "max_tokens": 2000,
    "webhook_url": "https://your-app.com/webhook/completion"
  }'
```

**Response:**
```json
{
  "request_id": "async-req-123456",
  "status": "queued",
  "estimated_completion_time": "2024-01-15T10:35:00Z"
}
```

#### Check Async Status

**Endpoint:** `GET /v1/async/status/{request_id}`

```bash
curl -X GET https://your-endpoint.tir.e2enetworks.com/v1/async/status/async-req-123456 \
  -H "Authorization: Bearer YOUR_API_KEY"
```

### SDK Integration

#### Python SDK

```python
import openai

# Configure client
client = openai.OpenAI(
    api_key="your-tir-api-key",
    base_url="https://your-endpoint.tir.e2enetworks.com/v1"
)

# Chat completion
response = client.chat.completions.create(
    model="your-model-name",
    messages=[
        {"role": "system", "content": "You are a helpful assistant."},
        {"role": "user", "content": "What is machine learning?"}
    ],
    max_tokens=150,
    temperature=0.7
)

print(response.choices[0].message.content)

# Streaming
stream = client.chat.completions.create(
    model="your-model-name",
    messages=[{"role": "user", "content": "Tell me a joke"}],
    stream=True
)

for chunk in stream:
    if chunk.choices[0].delta.content is not None:
        print(chunk.choices[0].delta.content, end="")
```

#### Node.js SDK

```javascript
const OpenAI = require('openai');

const openai = new OpenAI({
  apiKey: 'your-tir-api-key',
  baseURL: 'https://your-endpoint.tir.e2enetworks.com/v1'
});

async function chatCompletion() {
  const completion = await openai.chat.completions.create({
    messages: [{ role: 'user', content: 'Hello world' }],
    model: 'your-model-name',
    max_tokens: 100
  });

  console.log(completion.choices[0].message.content);
}

chatCompletion();
```

---

## Troubleshooting & Support

### Common Issues and Solutions

#### Deployment Issues

| Issue | Symptoms | Root Cause | Solution |
|-------|----------|------------|----------|
| **Model Loading Timeout** | Deployment stuck at "Loading model" | Large model, slow download | Increase timeout, use faster storage |
| **Container Build Failed** | Build errors in logs | Dockerfile issues, missing dependencies | Review Dockerfile, check base image |
| **Resource Allocation Failed** | "Insufficient resources" error | No available GPU/CPU | Try different region, adjust requirements |
| **Authentication Failed** | "Access denied" errors | Invalid credentials, expired tokens | Verify API keys, refresh tokens |

#### Runtime Issues

| Issue | Symptoms | Diagnosis | Resolution |
|-------|----------|-----------|------------|
| **High Error Rate** | 500 errors, model crashes | Check logs for stack traces | Review model code, increase resources |
| **Slow Response Times** | Latency > 10s | Monitor resource usage | Scale up instances, optimize model |
| **Memory Issues** | OOM kills, crashes | Memory usage graphs | Increase instance size, optimize code |
| **Cold Start Problems** | First requests very slow | Monitor cold start metrics | Increase min instances, optimize startup |

#### Performance Optimization

**Latency Optimization:**
1. **Model Optimization:** Use quantization, pruning, distillation
2. **Caching:** Implement response caching for common queries
3. **Batching:** Process multiple requests together
4. **Hardware:** Use faster GPUs, optimize memory allocation

**Throughput Optimization:**
1. **Scaling:** Increase max instances and target concurrency
2. **Load Balancing:** Distribute requests evenly across instances
3. **Request Queuing:** Implement smart request queueing
4. **Async Processing:** Use async APIs for non-realtime requests

**Cost Optimization:**
1. **Right-sizing:** Choose appropriate instance types
2. **Scaling Policies:** Optimize min/max instances
3. **Spot Instances:** Use spot instances for batch workloads
4. **Reserved Capacity:** Commit to longer terms for discounts

### Monitoring and Alerting

#### Key Metrics to Monitor

**Performance Metrics:**
- Request latency (p50, p95, p99)
- Requests per second
- Error rate and error types
- Queue depth and wait time

**Resource Metrics:**
- CPU and GPU utilization
- Memory usage (system and GPU)
- Disk I/O and network bandwidth
- Container health and restarts

**Business Metrics:**
- Cost per request
- User satisfaction scores
- Feature usage patterns
- Revenue attribution

#### Alert Configuration

**Critical Alerts:**
```yaml
alerts:
  - name: high_error_rate
    condition: error_rate > 10%
    duration: 2m
    severity: critical
    
  - name: extreme_latency
    condition: p95_latency > 30s
    duration: 5m
    severity: critical
    
  - name: endpoint_down
    condition: health_check_failures > 3
    duration: 1m
    severity: critical
```

**Warning Alerts:**
```yaml
  - name: elevated_latency
    condition: p95_latency > 5s
    duration: 10m
    severity: warning
    
  - name: high_gpu_usage
    condition: gpu_utilization > 85%
    duration: 15m
    severity: warning
    
  - name: cost_anomaly
    condition: hourly_cost > baseline * 1.5
    duration: 30m
    severity: warning
```

### Support Resources

#### Contact Information

| Support Type | Availability | Contact Method | Response Time | Best For |
|--------------|--------------|----------------|---------------|----------|
| **Technical Support** | 24/7 | support@e2enetworks.com | 1-4 hours | Deployment issues, performance problems |
| **Developer Support** | Business hours | developers@e2enetworks.com | 2-8 hours | API questions, integration help |
| **Account Support** | Business hours | accounts@e2enetworks.com | 4-24 hours | Billing, quota increases |
| **Emergency Support** | 24/7 | +91-11-4084-0700 | 15-30 minutes | Production outages |

#### Self-Service Resources

| Resource | URL | Content | Update Frequency |
|----------|-----|---------|------------------|
| **Documentation** | docs.e2enetworks.com/tir/inference | API docs, tutorials, examples | Weekly |
| **Status Page** | status.tir.e2enetworks.com | Service health, planned maintenance | Real-time |
| **Community Forum** | community.e2enetworks.com | User discussions, solutions | Daily |
| **GitHub Examples** | github.com/e2enetworks/tir-examples | Code samples, templates | Monthly |

#### Best Practices Documentation

**Model Deployment:**
- Security best practices for API keys and secrets
- Performance optimization guidelines
- Cost management strategies
- Monitoring and observability setup

**Production Readiness:**
- Health check implementation
- Error handling and retry logic
- Load testing methodology
- Disaster recovery planning

---

## Conclusion

The TIR Model Endpoints platform provides a comprehensive solution for deploying and managing machine learning models at scale. With support for multiple frameworks, flexible scaling options, and enterprise-grade monitoring, it enables teams to move from development to production quickly and efficiently.

### Key Takeaways

- **Flexible Deployment:** Choose between pre-built containers and custom Docker environments
- **Cost Optimization:** Leverage serverless scaling and committed pricing for optimal costs
- **Enterprise Ready:** Comprehensive monitoring, alerting, and support resources
- **Developer Friendly:** OpenAI-compatible APIs and comprehensive SDK support

### Next Steps

1. **Start Small:** Begin with a simple model deployment using pre-built containers
2. **Monitor Performance:** Set up alerting and monitoring from day one
3. **Optimize Iteratively:** Use performance data to optimize costs and latency
4. **Scale Confidently:** Leverage auto-scaling and load testing for production readiness

For additional support or questions about Model Endpoints, contact TIR support at support@e2enetworks.com or visit the comprehensive documentation at docs.e2enetworks.com/tir/inference.

</div>

<div style="width: 280px; position: sticky; top: 20px; height: fit-content; background: #f8fafc; border: 1px solid #e2e8f0; border-radius: 8px; padding: 1.5rem; margin-left: 2rem;">

## 📋 On This Page

### [Introduction](#introduction)
- [Key Features](#key-features)
- [Deployment Methods](#deployment-methods-comparison)

### [Create Model Endpoints](#create-model-endpoints)
- [Prerequisites](#prerequisites)
- [Step 1: Access Interface](#step-1-access-model-endpoints-interface)
- [Step 2: Select Method](#step-2-select-deployment-method)
- [Step 3: Configure Repository](#step-3-configure-model-repository)
- [Step 4: Machine Selection](#step-4-machine-and-gpu-selection)
- [Step 5: LLM Settings](#step-5-llm-settings-configuration)
- [Step 6: Serverless Config](#step-6-serverless-configuration)
- [Step 7: Environment Variables](#step-7-environment-variables)
- [Step 8: Deploy](#step-8-summary-and-deployment)

### [Model Endpoint Dashboard](#model-endpoint-dashboard)
- [Overview Metrics](#overview-metrics)
- [Traffic Analytics](#traffic-analytics)
- [Cost Monitoring](#cost-monitoring)

### [Actions and Management](#actions-and-management)
- [Scaling Operations](#scaling-operations)
- [Configuration Updates](#configuration-updates)
- [Monitoring & Debugging](#monitoring-and-debugging)

### [API Reference](#api-reference)
- [Endpoint URLs](#endpoint-urls-and-authentication)
- [Inference API](#inference-api)
- [Async Invocation](#async-invocation-api)
- [SDK Integration](#sdk-integration)

### [Troubleshooting & Support](#troubleshooting--support)
- [Common Issues](#common-issues-and-solutions)
- [Performance Optimization](#performance-optimization)
- [Support Resources](#support-resources)

### [Conclusion](#conclusion)
- [Key Takeaways](#key-takeaways)
- [Next Steps](#next-steps)

---

**🔗 Quick Links:**
- [TIR Platform](https://tir.e2enetworks.com)
- [API Documentation](https://docs.e2enetworks.com/api)
- [GitHub Examples](https://github.com/e2enetworks/tir-examples)
- [Status Page](https://status.tir.e2enetworks.com)
- [Support Portal](https://support.e2enetworks.com)

**📊 Resource Calculators:**
- [Cost Estimator](https://tir.e2enetworks.com/calculator)
- [Performance Planner](https://tir.e2enetworks.com/planner)

</div>

</div>
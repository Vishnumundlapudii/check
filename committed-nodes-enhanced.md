# Quick Guide to Committed Nodes

> **Platform:** E2E Networks TIR AI Platform  
> **Last Updated:** January 2024  
> **Document Type:** Configuration Guide  

## Overview

Committed nodes offer significant cost savings for long-term AI/ML workloads through dedicated resource allocation with discounted pricing plans ranging from 30 to 90 days. These dedicated instances provide guaranteed compute power with no resource sharing, ensuring consistent performance for your machine learning projects.

### Cost Benefits Overview

| Commitment Period | Discount | Payment Terms | Best For |
|-------------------|----------|---------------|----------|
| 30 Days | 15% | Upfront | Short projects, testing environments |
| 60 Days | 25% | Upfront/Monthly | Most projects, balanced savings |
| 90 Days | 30% | Upfront | Long-term research, production workloads |

**Example Savings:** PyTorch 2 notebook at ₹3.1/hour becomes only ₹6026 for a 90-day committed plan - saving up to 30% compared to hourly billing.

### Key Features

- **🔒 Dedicated Resources:** Guaranteed compute power with no resource sharing
- **⚡ Instant Access:** Pre-provisioned environments ready within minutes
- **🔄 Flexible Management:** Upgrade, downgrade, or modify configurations during commitment period
- **💰 Significant Savings:** Up to 30% discount compared to hourly billing

---

## Creating a Committed Notebook

### Prerequisites

Before creating a committed notebook, ensure you have:

- [ ] Active E2E Networks account with verified billing information
- [ ] TIR AI Platform access permissions
- [ ] Understanding of your computational requirements (CPU/GPU, RAM, storage)
- [ ] Commitment period decision (30, 60, or 90 days)
- [ ] Project timeline alignment with commitment duration

### Step-by-Step Creation Process

#### Step 1: Access TIR AI Platform Dashboard

![TIR AI Platform Dashboard](https://docs.e2enetworks.com/docs/tir/Nodes/Committed_Nodes/assets/dashboard-access.png)

**Screenshot Analysis:**
- **Top Navigation:** "TIR AI Platform" tab is highlighted in blue
- **Left Sidebar:** Shows "Notebooks" section with expandable sub-options
- **Main Area:** Dashboard overview displaying recent activity and notebook list
- **Action Button:** Blue "Create Notebook" button prominently displayed in top-right corner

**Navigation Path:**
```
Dashboard → TIR AI Platform → Notebooks
```

**What to Look For:**
- The main dashboard should display your current notebooks list (may be empty for new users)
- Header navigation showing "TIR AI Platform" as the active tab
- Left sidebar with collapsible menu sections
- Primary action button for notebook creation

**Expected Elements:**
- Header navigation with clear platform identification
- Responsive sidebar with organized menu structure
- Main content area with grid or list view of existing notebooks
- Prominent call-to-action for creating new notebooks

**Troubleshooting:**
| Issue | Cause | Solution |
|-------|-------|----------|
| "Create Notebook" button disabled | Billing setup incomplete | Verify payment method in account settings |
| TIR AI Platform tab missing | Insufficient permissions | Contact administrator for access rights |
| Dashboard loading slowly | Network connectivity | Refresh page or check internet connection |

---

#### Step 2: Initiate Notebook Creation

**Action Required:** Click the "Create Notebook" button

**Expected Result:** Opens the notebook configuration wizard with multiple setup options

**Alternative Entry Points:**
- From empty state: "Get Started" button in center of screen
- Keyboard shortcut: `Alt + N` (if enabled)
- API endpoint: `POST /api/v1/notebooks/create`

---

#### Step 3: Choose Creation Method

![Notebook Creation Options](https://docs.e2enetworks.com/docs/tir/Nodes/Committed_Nodes/assets/creation-options.png)

**Screenshot Analysis:**
- **Two Main Options:** "New Notebook" and "Import Notebook" presented as selectable cards
- **Visual Design:** Card-based layout with descriptive icons and hover effects
- **Selection State:** Cards highlight with border changes when hovered
- **Progress Indicator:** Step 1 of the setup wizard clearly shown

**Options Comparison:**

| Option | Use Case | Includes | Best For |
|--------|----------|----------|----------|
| **New Notebook** | Starting fresh with clean environment | Pre-configured frameworks, clean workspace, sample datasets | New projects, learning, experimentation |
| **Import Notebook** | Migrating existing work or using templates | Custom configurations, existing code, data persistence | Production workloads, team collaboration |

**Recommendation:** Select "New Notebook" for this tutorial to follow the complete setup process.

---

#### Step 4: Select Framework Environment

**Primary Choice:** PyTorch 2 (recommended for most AI/ML workloads)

### Framework Specifications

| Framework | Version | Included Libraries | GPU Support | Best For |
|-----------|---------|-------------------|-------------|----------|
| **PyTorch 2** | 2.x with CUDA 11.8 | NumPy, Pandas, Matplotlib, Scikit-learn | Automatic CUDA detection | Deep learning, computer vision, NLP |
| **TensorFlow** | 2.x with Keras | TensorBoard, TF Serving | Multi-GPU support | Production models, enterprise deployment |
| **Custom Environment** | User-defined | User-specified | Configurable | Specialized research, specific requirements |

**Selection Criteria:**
- **PyTorch:** Choose for research flexibility and dynamic computation graphs
- **TensorFlow:** Select for production environments and enterprise-grade deployment
- **Custom:** Use for specialized frameworks or specific version requirements

---

#### Step 5: Configure Instance Specifications

![Instance Configuration Screen](https://docs.e2enetworks.com/docs/tir/Nodes/Committed_Nodes/assets/instance-config.png)

**Screenshot Analysis:**
- **Resource Sliders:** Interactive controls for CPU cores, RAM, and storage allocation
- **Instance Types:** Dropdown menu with CPU-only and GPU-enabled options
- **Real-time Pricing:** Cost calculator updates dynamically as specifications change
- **Recommendation Engine:** Suggested configurations based on selected framework

### Instance Type Options

#### CPU-Optimized Instances

| Instance Type | vCPU Cores | Memory (RAM) | Storage (SSD) | Hourly Rate | Best For |
|---------------|------------|--------------|---------------|-------------|----------|
| c5.large | 2 | 4 GB | 50 GB | ₹2.1 | Light processing, development |
| c5.xlarge | 4 | 8 GB | 100 GB | ₹4.2 | Data preprocessing, small models |
| c5.2xlarge | 8 | 16 GB | 200 GB | ₹8.4 | Medium workloads, batch processing |
| c5.4xlarge | 16 | 32 GB | 400 GB | ₹16.8 | Large datasets, complex processing |

#### GPU-Accelerated Instances

| Instance Type | GPU | GPU Memory | vCPU | System RAM | Storage | Hourly Rate | Best For |
|---------------|-----|------------|------|------------|---------|-------------|----------|
| g4dn.xlarge | NVIDIA T4 | 16 GB | 4 | 16 GB | 125 GB | ₹12.5 | Training medium models |
| g4dn.2xlarge | NVIDIA T4 | 16 GB | 8 | 32 GB | 225 GB | ₹22.3 | Computer vision, NLP |
| p3.2xlarge | NVIDIA V100 | 16 GB | 8 | 61 GB | 200 GB | ₹45.6 | Deep learning research |
| p3.8xlarge | 4x NVIDIA V100 | 64 GB | 32 | 244 GB | 800 GB | ₹182.4 | Multi-GPU training |

**Performance Considerations:**
- **CPU Instances:** Suitable for data processing, feature engineering, and inference
- **GPU Instances:** Essential for training deep neural networks and large model inference
- **Memory Requirements:** Ensure sufficient RAM for your dataset size
- **Storage Needs:** Consider model checkpoints, datasets, and output storage

---

#### Step 6: Select Commitment Plan

![Commitment Plan Selection](https://docs.e2enetworks.com/docs/tir/Nodes/Committed_Nodes/assets/commitment-plans.png)

**Screenshot Analysis:**
- **Plan Cards:** Three distinct pricing tiers with prominent discount percentages
- **Savings Calculator:** Real-time calculation showing total savings compared to hourly billing
- **Payment Terms:** Clear indication of upfront vs. monthly payment options
- **Popular Choice:** 60-day plan highlighted as the recommended option

### Commitment Plan Comparison

| Duration | Discount Rate | Total Savings | Payment Options | Flexibility Level | Recommended For |
|----------|---------------|---------------|-----------------|-------------------|-----------------|
| **30 Days** | 15% | ₹900-₹2700 | Upfront only | High - Early exit possible | Short-term projects, POCs |
| **60 Days** | 25% | ₹3000-₹9000 | Upfront or Monthly | Medium - Mid-term commitment | Most production workloads |
| **90 Days** | 30% | ₹5400-₹16200 | Upfront only | Low - Long-term lock-in | Research projects, production |

### Cost Calculation Examples

#### PyTorch 2 Instance (c5.2xlarge)

| Billing Model | Cost Calculation | 30 Days | 60 Days | 90 Days |
|---------------|------------------|---------|---------|---------|
| **Hourly Rate** | ₹8.4/hour × 24h × days | ₹6048 | ₹12096 | ₹18144 |
| **Committed Rate** | Hourly rate with discount | ₹5141 (15% off) | ₹9072 (25% off) | ₹12701 (30% off) |
| **Total Savings** | Difference from hourly | ₹907 | ₹3024 | ₹5443 |

#### GPU Instance (g4dn.2xlarge)

| Billing Model | Cost Calculation | 30 Days | 60 Days | 90 Days |
|---------------|------------------|---------|---------|---------|
| **Hourly Rate** | ₹22.3/hour × 24h × days | ₹16056 | ₹32112 | ₹48168 |
| **Committed Rate** | Hourly rate with discount | ₹13648 (15% off) | ₹24084 (25% off) | ₹33718 (30% off) |
| **Total Savings** | Difference from hourly | ₹2408 | ₹8028 | ₹14450 |

**Important Considerations:**

> ⚠️ **Critical Warning:** Committed notebooks cannot be terminated before the commitment period ends without forfeiting the remaining prepaid amount. Plan your project timeline carefully to align with the commitment duration.

**Factors to Consider When Choosing:**
- **Project Duration:** Align commitment period with actual project needs
- **Budget Planning:** Consider upfront vs. monthly payment impact on cash flow
- **Resource Requirements:** May change during project lifecycle
- **Team Dependencies:** Multiple team members may need access duration

---

#### Steps 7-11: Complete Configuration & Deploy

### Configuration Summary

| Step | Task | Details | Estimated Time |
|------|------|---------|----------------|
| **7** | Configure SSH Access | Set up secure shell access and key management | 2-3 minutes |
| **8** | Set Auto-Renewal | Enable/disable automatic commitment renewal | 1 minute |
| **9** | Review Configuration | Validate all settings and pricing summary | 2-3 minutes |
| **10** | Accept Terms | Agree to service terms and commitment conditions | 1 minute |
| **11** | Confirm Payment | Process payment and initiate deployment | 1-2 minutes |

### Deployment Timeline

| Phase | Duration | Activity | Status Indicators |
|-------|----------|----------|-------------------|
| **Payment Processing** | 0-30 seconds | Payment validation and resource allocation | "Processing Payment" message |
| **Resource Allocation** | 30-90 seconds | Hardware provisioning and network setup | "Allocating Resources" progress bar |
| **Environment Setup** | 90-180 seconds | Framework installation and configuration | "Installing Framework" with percentage |
| **Final Initialization** | 180-300 seconds | Notebook startup and health checks | "Starting Notebook" spinner |
| **Ready for Access** | 3-5 minutes total | Notebook accessible via provided URL | Green "Active" status |

### Post-Deployment Verification

**Immediately After Deployment:**
- [ ] Verify notebook status shows "Running"
- [ ] Test SSH/HTTPS connectivity
- [ ] Confirm framework installation (import torch/tensorflow)
- [ ] Check resource allocation matches selected configuration
- [ ] Validate auto-renewal settings

**Common Deployment Issues:**

| Issue | Symptoms | Resolution | Prevention |
|-------|----------|------------|------------|
| Payment Failure | Deployment stuck at payment | Update payment method, retry | Verify billing info before starting |
| Resource Unavailability | Long allocation time | Contact support, try different region | Check resource availability beforehand |
| Framework Errors | Import failures in notebook | Restart notebook, check logs | Select stable framework versions |

---

## Auto-Renewal Configuration

Auto-renewal ensures uninterrupted service by automatically extending your commitment period before expiration, maintaining both service continuity and discounted pricing.

### How Auto-Renewal Works

| Timeline | Event | Action Required | Notification Method |
|----------|-------|-----------------|-------------------|
| **7 Days Before Expiry** | First warning notification | Review and update preferences if needed | Email to registered address |
| **24 Hours Before** | Final reminder | Last chance to disable auto-renewal | Email + Dashboard notification |
| **At Expiry Time** | Automatic renewal processing | None - automatic charge | SMS + Email confirmation |
| **Post-Renewal** | Confirmation and new period start | Optional: Update configurations | Email with new commitment details |

### Auto-Renewal Settings Configuration

| Setting | Options | Default | Description |
|---------|---------|---------|-------------|
| **Auto-Renewal Status** | Enabled/Disabled | Enabled | Automatically renew at commitment end |
| **Renewal Period** | Same/Different duration | Same as current | Choose 30/60/90 days for next period |
| **Payment Method** | Primary/Secondary/New | Primary on file | Credit card or bank account for charges |
| **Notification Preferences** | Email/SMS/Both | Email only | How to receive renewal notifications |

### Managing Auto-Renewal

**To Modify Auto-Renewal:**
1. Navigate to **Notebook Settings** → **Billing & Renewal**
2. Toggle **Auto-Renewal** status as needed
3. Select **Renewal Period** for next cycle
4. Update **Payment Method** if required
5. Set **Notification Preferences**
6. Save changes - effective for next renewal cycle

**Cancellation Windows:**

| Action | Latest Time Allowed | Effect | Recovery Option |
|--------|-------------------|--------|-----------------|
| **Disable Auto-Renewal** | 24 hours before expiry | Notebook ends at commitment period | Manual renewal within 7 days |
| **Change Renewal Period** | 48 hours before expiry | Different commitment length | Immediate effect on next cycle |
| **Update Payment Method** | 72 hours before expiry | New payment source | Prevents renewal failure |

---

## Billing Options & Management

Understanding the different billing models available for committed notebooks helps optimize costs and resource utilization across various project phases.

### Billing Model Comparison

| Billing Type | Payment Frequency | Cost Structure | Flexibility | Best Use Case |
|--------------|------------------|----------------|-------------|---------------|
| **Auto-Renewal** | Monthly/Commitment period | Fixed discount rate | Medium | Ongoing projects |
| **Hourly Conversion** | Hourly usage | Standard rates | High | Variable workloads |
| **Auto-Deletion** | One-time commitment | Prepaid with termination | Low | Fixed-duration projects |

### Auto-Renewal Billing (Default)

**Advantages:**
- ✅ Seamless service continuation without manual intervention
- ✅ No risk of accidental service termination
- ✅ Maintains discounted pricing throughout project lifecycle
- ✅ Preserves environment configuration and data persistence
- ✅ Predictable monthly budgeting with fixed costs

**Considerations:**
- ⚠️ Requires active and valid payment method at all times
- ⚠️ Automatic charges occur without additional approval
- ⚠️ Need to monitor usage patterns to optimize cost-effectiveness
- ⚠️ Commitment continues until manually disabled

**Financial Planning:**

| Commitment Period | Monthly Cost | Annual Projection | Budget Allocation |
|------------------|--------------|-------------------|-------------------|
| 30-day cycles | Variable based on plan | 12 × monthly cost | Monthly operational budget |
| 60-day cycles | Amortized over 2 months | 6 × bi-monthly cost | Quarterly budget planning |
| 90-day cycles | Amortized over 3 months | 4 × quarterly cost | Project-based budgeting |

### Hourly Billing Conversion

Converting from committed to hourly billing during the commitment period has specific implications for cost management and resource flexibility.

**Conversion Process:**
1. **Access Billing Settings** → Navigate to notebook management dashboard
2. **Select "Convert to Hourly"** → Located in billing options menu
3. **Review Cost Impact** → System calculates rate changes and effective date
4. **Acknowledge Refund Policy** → Confirm understanding of no refund for remaining period
5. **Confirm Conversion** → Process change immediately or schedule for next billing cycle

**Cost Impact Analysis:**

| Original Plan | Remaining Period | Hourly Rate | Daily Cost Increase | Monthly Impact |
|---------------|------------------|-------------|-------------------|----------------|
| 30-day committed (15% off) | 15 days remaining | +17.6% cost | +₹150-₹450 | +₹4500-₹13500 |
| 60-day committed (25% off) | 30 days remaining | +33.3% cost | +₹300-₹900 | +₹9000-₹27000 |
| 90-day committed (30% off) | 45 days remaining | +42.9% cost | +₹450-₹1350 | +₹13500-₹40500 |

**When to Convert to Hourly:**
- ✅ Project completed earlier than expected
- ✅ Workload becomes highly variable or intermittent
- ✅ Need temporary pause capability without commitment penalties
- ✅ Resource requirements changed significantly

**Refund Policy:**
> **No Refunds:** Remaining prepaid commitment amounts are not refundable upon conversion to hourly billing. The conversion applies to future usage only.

### Auto-Deletion Option

Automatic resource cleanup provides a hands-off approach to notebook lifecycle management with built-in data protection measures.

#### Deletion Timeline & Process

| Phase | Timeline | Activity | User Action Required |
|-------|----------|----------|---------------------|
| **Warning Period** | 7 days before expiry | Email notification sent | Optional: Extend commitment or backup data |
| **Final Notice** | 24 hours before expiry | Last backup reminder | Critical: Complete data backup |
| **Grace Period** | At expiry + 48 hours | Notebook marked for deletion | Emergency: Contact support for recovery |
| **Permanent Deletion** | After grace period | Irreversible data removal | None - recovery impossible |

#### Essential Backup Procedures

**Critical Data to Backup:**

| Data Type | Location | Backup Method | Priority |
|-----------|----------|---------------|----------|
| **Jupyter Notebooks** | `/home/user/notebooks/` | Download as .ipynb files | Critical |
| **Trained Models** | `/home/user/models/` | Export to external storage | Critical |
| **Datasets** | `/home/user/data/` | Compress and download | High |
| **Custom Scripts** | `/home/user/scripts/` | Git repository or direct download | High |
| **Environment Config** | `/home/user/.conda/` | Export environment.yml | Medium |
| **SSH Keys** | `/home/user/.ssh/` | Secure backup location | Medium |

**Automated Backup Commands:**
```bash
# Create comprehensive backup archive
tar -czf notebook-backup-$(date +%Y%m%d).tar.gz \
    ~/notebooks/ ~/models/ ~/data/ ~/scripts/

# Export conda environment
conda env export > environment.yml

# Create requirements file for pip packages
pip freeze > requirements.txt

# Backup SSH configuration
cp -r ~/.ssh/ ~/backup/ssh-config/
```

#### Recovery Options During Grace Period

| Recovery Method | Availability | Cost | Data Integrity |
|----------------|--------------|------|----------------|
| **Support Ticket Recovery** | 48 hours post-expiry | No additional charge | 100% if within grace period |
| **Emergency Extension** | 24 hours post-expiry | Pro-rated commitment cost | 100% guaranteed |
| **Data-Only Recovery** | 48 hours post-expiry | Storage fees only | Data files only, no environment |

**Emergency Recovery Process:**
1. **Immediate Action:** Contact support within 48 hours of expiry
2. **Provide Details:** Notebook ID, original commitment details, reason for recovery
3. **Payment Confirmation:** Pay any applicable fees for extension or recovery
4. **Access Restoration:** Typically completed within 4-6 hours during business hours

---

## Updating Notebook Configurations

Modify your notebook specifications, commitment plans, or billing models during the active period with these comprehensive procedures designed to maintain service continuity.

### Update Scenarios Overview

| Update Type | Downtime Required | Cost Impact | Processing Time | Data Safety |
|-------------|------------------|-------------|-----------------|-------------|
| **Hourly to Committed** | Minimal (2-5 minutes) | Savings apply immediately | 10-15 minutes | 100% preserved |
| **Committed Plan Changes** | None for upgrades | Pro-rated adjustment | 5-10 minutes | 100% preserved |
| **Resource Scaling** | Brief restart (1-3 minutes) | Immediate rate change | 5-15 minutes | 100% preserved |
| **Framework Changes** | Full redeployment (5-10 minutes) | Rate change on restart | 15-30 minutes | Manual backup required |

### Hourly to Committed Conversion

Converting hourly notebooks to committed plans provides immediate cost savings while maintaining full functionality and data integrity.

![Hourly to Committed Conversion Interface](https://docs.e2enetworks.com/docs/tir/Nodes/Committed_Nodes/assets/hourly-to-committed.png)

**Screenshot Analysis:**
- **Current Status Panel:** Displays existing hourly notebook details including current usage patterns
- **Conversion Options Grid:** Available commitment plans with projected savings calculations
- **Cost Calculator:** Real-time comparison showing current vs. committed costs over time
- **Migration Timeline:** Estimated downtime and completion schedule

#### 10-Step Conversion Process

| Step | Task | Expected Duration | Key Actions |
|------|------|------------------|-------------|
| **1** | Access Notebook Settings | 30 seconds | Navigate to existing hourly notebook management panel |
| **2** | Select "Convert to Committed" | 15 seconds | Located in notebook actions dropdown menu |
| **3** | Review Current Usage | 1-2 minutes | System analyzes past 30 days usage patterns and costs |
| **4** | Choose Commitment Period | 1 minute | Select 30, 60, or 90-day options with real-time savings preview |
| **5** | Confirm Resource Specifications | 2-3 minutes | Opportunity to upgrade/downgrade during conversion process |
| **6** | Calculate Prorated Costs | 30 seconds | System automatically adjusts billing for partial periods |
| **7** | Set Auto-Renewal Preferences | 1 minute | Configure renewal settings for new commitment period |
| **8** | Schedule Conversion Time | 1 minute | Choose immediate conversion or schedule for off-peak hours |
| **9** | Create Data Snapshot | 2-3 minutes | System creates automatic backup before conversion (recommended) |
| **10** | Complete Conversion | 5-10 minutes | Confirm changes and process the conversion |

#### Financial Benefits Analysis

**Immediate Cost Impact:**

| Instance Type | Hourly Rate | 30-Day Committed | 60-Day Committed | 90-Day Committed |
|---------------|-------------|------------------|------------------|------------------|
| **c5.large** | ₹2.1/hour | ₹1,285 (15% off) | ₹1,134 (25% off) | ₹1,058 (30% off) |
| **c5.xlarge** | ₹4.2/hour | ₹2,570 (15% off) | ₹2,268 (25% off) | ₹2,116 (30% off) |
| **g4dn.xlarge** | ₹12.5/hour | ₹7,650 (15% off) | ₹6,750 (25% off) | ₹6,300 (30% off) |
| **p3.2xlarge** | ₹45.6/hour | ₹27,864 (15% off) | ₹24,624 (25% off) | ₹22,968 (30% off) |

**Conversion Benefits:**
- ✅ **Immediate Savings:** Up to 30% reduction in ongoing operational costs
- ✅ **Predictable Billing:** Fixed monthly costs enable better budget planning and forecasting
- ✅ **Prorated Adjustment:** Fair billing calculation for partial periods ensures no overpayment
- ✅ **Resource Guarantee:** Dedicated resources with no performance contention
- ✅ **Priority Support:** Committed users receive priority technical support

#### Usage Pattern Analysis

The system analyzes your usage patterns to recommend optimal commitment periods:

| Usage Pattern | Recommendation | Reasoning |
|---------------|----------------|-----------|
| **Consistent 24/7** | 90-day commitment | Maximum savings for continuous usage |
| **Business Hours Only** | 60-day commitment | Balanced savings with flexibility |
| **Variable/Bursty** | 30-day commitment | Short commitment for changing needs |
| **Development/Testing** | Remain hourly | Flexibility more valuable than savings |

### Committed Plan Changes

Modify existing committed plans to adapt to changing project requirements while maintaining cost efficiency.

![Plan Modification Interface](https://docs.e2enetworks.com/docs/tir/Nodes/Committed_Nodes/assets/plan-change.png)

**Screenshot Analysis:**
- **Current Plan Display:** Shows active commitment details including remaining time and current specifications
- **Available Changes Grid:** Matrix view of all upgrade and downgrade options with clear pricing
- **Price Difference Calculator:** Real-time indication of additional costs or account credits
- **Effective Date Selector:** Choose when changes take effect (immediate vs. next billing cycle)

#### 7-Step Plan Modification Process

| Step | Activity | Details | Time Required |
|------|----------|---------|---------------|
| **1** | Access Plan Management | From notebook dashboard, select "Modify Plan" option | 30 seconds |
| **2** | Review Current Commitment | System displays remaining time, current specs, and usage stats | 1 minute |
| **3** | Select New Plan | Choose from available upgrade/downgrade options in grid format | 2-3 minutes |
| **4** | Calculate Cost Difference | View prorated billing adjustment shown in real-time | 1 minute |
| **5** | Choose Effective Date | Select immediate change or schedule for next billing cycle | 30 seconds |
| **6** | Confirm Modification | Review comprehensive summary of changes and cost impact | 1-2 minutes |
| **7** | Process Change | System updates notebook configuration and billing accordingly | 5-10 minutes |

#### Plan Change Scenarios

**Resource Upgrade Scenarios:**

| Current Plan | Upgrade To | Additional Monthly Cost | Immediate Benefits |
|--------------|------------|------------------------|--------------------|
| c5.large → c5.xlarge | 2→4 vCPU, 4→8 GB RAM | +₹1,134 | 2x processing power |
| c5.xlarge → c5.2xlarge | 4→8 vCPU, 8→16 GB RAM | +₹2,268 | 2x compute, better multitasking |
| CPU → GPU (g4dn.xlarge) | Add NVIDIA T4 GPU | +₹4,566 | GPU acceleration for ML/AI |
| g4dn.xlarge → p3.2xlarge | T4 → V100 GPU | +₹16,416 | Professional-grade GPU performance |

**Resource Downgrade Scenarios:**

| Current Plan | Downgrade To | Monthly Credit | Considerations |
|--------------|--------------|----------------|----------------|
| c5.2xlarge → c5.xlarge | 8→4 vCPU, 16→8 GB RAM | -₹2,268 | Ensure workload fits reduced specs |
| p3.2xlarge → g4dn.xlarge | V100→T4 GPU | -₹16,416 | Significant performance reduction |
| GPU → CPU only | Remove GPU acceleration | -₹4,566+ | ML/AI workloads will be slower |

#### Cost Calculation Examples

**Prorated Billing for Mid-Cycle Changes:**

Example: Upgrading from c5.large to c5.xlarge on day 15 of 30-day commitment:

| Component | Calculation | Amount |
|-----------|-------------|--------|
| **Remaining Days** | 30 - 15 = 15 days | 15 days |
| **Cost Difference** | ₹2,268 - ₹1,134 = ₹1,134/month | ₹1,134 |
| **Prorated Amount** | (₹1,134 ÷ 30) × 15 days | ₹567 |
| **Immediate Charge** | Prorated difference | ₹567 |

**Change Effective Dates:**

| Option | Benefits | Drawbacks | Best For |
|--------|----------|-----------|----------|
| **Immediate** | Instant resource availability | Higher prorated costs | Urgent performance needs |
| **Next Cycle** | No additional charges | Delayed benefit realization | Planned capacity expansion |
| **Scheduled** | Minimal business disruption | Complex scheduling required | Production environments |

---

## Deleting Committed Notebooks

Properly manage the lifecycle of committed notebooks with comprehensive understanding of financial implications, data recovery options, and alternative solutions.

### Critical Pre-Deletion Considerations

> ⚠️ **IMPORTANT:** Deletion of committed notebooks has significant financial and operational implications that cannot be reversed.

#### Financial Impact Assessment

| Commitment Remaining | Financial Loss | Refund Policy | Recovery Options |
|---------------------|----------------|---------------|------------------|
| **< 7 days** | Minimal impact | No refunds | Consider waiting for natural expiry |
| **1-4 weeks** | Moderate loss | No refunds | Evaluate conversion to hourly |
| **1-3 months** | Significant loss | No refunds | Strong recommendation to repurpose |
| **> 3 months** | Major financial impact | No refunds | Consider suspension or resource sharing |

#### Data Protection Checklist

Before proceeding with deletion, ensure comprehensive data backup:

| Data Category | Backup Method | Verification Required | Priority Level |
|---------------|---------------|----------------------|----------------|
| **Jupyter Notebooks** | Download .ipynb files | ✅ Test file opening | Critical |
| **Trained Models** | Export model weights/checkpoints | ✅ Test model loading | Critical |
| **Datasets** | Compress and download data files | ✅ Verify data integrity | High |
| **Code Scripts** | Git repository or direct download | ✅ Test code execution | High |
| **Environment Setup** | Export conda/pip requirements | ✅ Test environment recreation | Medium |
| **Configuration Files** | Backup custom configurations | ✅ Document setup procedures | Medium |

### Deletion Procedure

![Deletion Confirmation Dialog](https://docs.e2enetworks.com/docs/tir/Nodes/Committed_Nodes/assets/deletion-confirmation.png)

**Screenshot Analysis:**
- **Multi-Step Warning Dialog:** Multiple confirmation steps designed to prevent accidental deletion
- **Financial Impact Display:** Clear presentation of non-refundable amounts and financial implications
- **Data Backup Reminder:** Prominent final prompt to ensure important data has been backed up
- **Verification Typing:** Required exact typing of notebook name for additional confirmation
- **Final Confirmation Button:** Red warning-colored button to emphasize irreversible action

#### Step-by-Step Deletion Process

| Step | Action | Security Measure | Estimated Time |
|------|--------|------------------|----------------|
| **1** | Navigate to Target Notebook | Access specific committed notebook from dashboard | 30 seconds |
| **2** | Access Management Settings | Click "Settings" or "Manage" option in notebook panel | 15 seconds |
| **3** | Locate Delete Option | Find "Delete Notebook" in actions menu (usually at bottom) | 15 seconds |
| **4** | Review Financial Warning | System displays comprehensive financial and data loss warnings | 1-2 minutes |
| **5** | Confirm Data Backup | Check mandatory checkbox confirming data has been backed up | 30 seconds |
| **6** | Type Notebook Name | Enter exact notebook name for verification (case-sensitive) | 30 seconds |
| **7** | Final Confirmation | Click red "DELETE" button to proceed with irreversible action | 15 seconds |
| **8** | Processing Completion | System processes deletion and removes all associated resources | 2-5 minutes |

#### Post-Deletion Verification

**Immediate Confirmations:**
- [ ] Notebook removed from dashboard listing
- [ ] Email confirmation sent to account holder
- [ ] Billing adjustments processed (if applicable)
- [ ] Associated storage volumes deleted
- [ ] SSH keys and access credentials revoked

**Within 24 Hours:**
- [ ] Final billing statement generated
- [ ] Account credits applied (if any)
- [ ] Support tickets automatically closed
- [ ] Monitoring and alerting disabled

### Alternatives to Deletion

Before proceeding with deletion, consider these cost-effective alternatives that preserve your investment:

#### Notebook Suspension

**Suspend Notebook Option:**

| Feature | Details | Cost Impact | Use Case |
|---------|---------|-------------|----------|
| **Compute Suspension** | Stop all processing while preserving data | 90% cost reduction | Temporary project pause |
| **Data Preservation** | All files, environments, and configurations maintained | Storage fees only (₹0.5/GB/month) | Seasonal projects |
| **Quick Resume** | Restart anytime during commitment period | Resume to full billing | Project reactivation |
| **Commitment Maintained** | Original commitment terms preserved | No early termination fees | Planned work interruptions |

**Suspension Process:**
1. Navigate to **Notebook Settings** → **Power Management**
2. Select **"Suspend Notebook"** option
3. Choose **suspension duration** (if known)
4. Confirm **data retention** preferences
5. Set **auto-resume** triggers (optional)

#### Resource Downgrading

**Strategic Downgrades:**

| Current Configuration | Downgrade Option | Monthly Savings | Performance Impact |
|----------------------|------------------|-----------------|-------------------|
| **p3.2xlarge (V100)** | → g4dn.xlarge (T4) | -₹16,416 | 60-70% GPU performance reduction |
| **c5.4xlarge** | → c5.2xlarge | -₹8,400 | 50% CPU and memory reduction |
| **GPU instance** | → CPU equivalent | -₹4,566+ | No GPU acceleration |
| **High storage** | → Reduced storage | -₹50-500 | Requires data cleanup |

**Downgrade Considerations:**
- ✅ **Preserve Commitment:** Maintain discounted pricing structure
- ✅ **Reduce Costs:** Significant monthly savings while keeping infrastructure
- ✅ **Maintain Environment:** No data loss or environment reconfiguration
- ✅ **Upgrade Flexibility:** Can upgrade again if requirements change

#### Conversion to Hourly Billing

**Hourly Conversion Strategy:**

| Scenario | Conversion Benefit | Financial Impact | Operational Flexibility |
|----------|-------------------|------------------|-------------------------|
| **Irregular Usage** | Pay only for actual usage | Potential savings for <40% utilization | High - start/stop anytime |
| **Project Uncertainty** | No commitment penalty | No refund for remaining period | Maximum flexibility |
| **Resource Scaling** | Easy resource modifications | Higher per-hour rates | Immediate changes possible |
| **Multi-Environment** | Share resources across projects | Cost optimization opportunities | Dynamic allocation |

**Conversion Process:**
1. **Evaluate Usage Patterns:** Analyze past 30 days of actual utilization
2. **Calculate Break-Even Point:** Determine hours per month where hourly becomes cost-effective
3. **Plan Transition:** Choose optimal conversion timing to minimize financial impact
4. **Execute Conversion:** Follow hourly conversion process outlined in previous sections

#### Resource Sharing and Team Access

**Collaborative Utilization:**

| Sharing Model | Implementation | Cost Distribution | Management Complexity |
|---------------|---------------|-------------------|----------------------|
| **Team Access** | Multiple user accounts on same notebook | Split costs among team members | Low - shared responsibility |
| **Time-Based Sharing** | Schedule access windows for different users | Proportional cost allocation | Medium - requires coordination |
| **Project Rotation** | Different projects use same infrastructure | Project-based billing | High - detailed tracking needed |

**Sharing Setup:**
1. **Configure User Access:** Add team members to notebook with appropriate permissions
2. **Establish Usage Guidelines:** Define access schedules and resource usage policies
3. **Implement Cost Tracking:** Set up billing allocation and expense reporting
4. **Monitor Utilization:** Regular review of usage patterns and cost effectiveness

---

## API Reference & Automation

Programmatically manage committed notebooks using E2E Networks REST API for seamless automation and integration with your existing development workflows and infrastructure management systems.

### Authentication & Setup

#### API Authentication

```bash
# Set your API token as environment variable
export E2E_API_TOKEN="your_api_token_here"

# Alternative: Use in headers directly
curl -H "Authorization: Bearer your_api_token_here" \
     -H "Content-Type: application/json" \
     https://api.e2enetworks.com/v1/notebooks
```

#### Base URL and Endpoints

| Environment | Base URL | Rate Limits | Authentication |
|-------------|----------|-------------|----------------|
| **Production** | `https://api.e2enetworks.com/v1` | 1000 requests/hour | Bearer token required |
| **Sandbox** | `https://sandbox-api.e2enetworks.com/v1` | 100 requests/hour | Test token required |

### Core API Endpoints

#### Create Committed Notebook

**Endpoint:** `POST /api/v1/notebooks/committed`

```bash
curl -X POST https://api.e2enetworks.com/v1/notebooks/committed \
  -H "Authorization: Bearer $E2E_API_TOKEN" \
  -H "Content-Type: application/json" \
  -d '{
    "name": "production-ml-notebook",
    "framework": "pytorch-2",
    "instance_type": "gpu-t4",
    "commitment_period": 60,
    "auto_renewal": true,
    "region": "mumbai-1",
    "specifications": {
      "cpu_cores": 8,
      "memory_gb": 32,
      "storage_gb": 100,
      "gpu_count": 1,
      "gpu_type": "nvidia-t4"
    },
    "configuration": {
      "ssh_enabled": true,
      "public_ip": true,
      "backup_enabled": true,
      "monitoring_enabled": true
    },
    "billing": {
      "payment_method_id": "pm_1234567890",
      "billing_contact": "admin@company.com"
    }
  }'
```

**Response Schema:**

| Field | Type | Description | Example |
|-------|------|-------------|---------|
| `id` | string | Unique notebook identifier | `nb-1234567890abcdef` |
| `name` | string | User-defined notebook name | `production-ml-notebook` |
| `status` | string | Current notebook state | `creating`, `running`, `stopped` |
| `framework` | string | Installed ML framework | `pytorch-2`, `tensorflow-2` |
| `instance_type` | string | Compute instance specification | `gpu-t4`, `cpu-optimized` |
| `commitment_expires` | datetime | Commitment period end date | `2024-04-15T10:30:00Z` |
| `auto_renewal` | boolean | Auto-renewal status | `true`, `false` |
| `cost_per_month` | number | Monthly cost in local currency | `6026` |
| `public_ip` | string | Assigned public IP address | `203.0.113.10` |
| `ssh_endpoint` | string | SSH connection string | `user@203.0.113.10:22` |
| `jupyter_url` | string | JupyterLab access URL | `https://203.0.113.10:8888` |

**Example Successful Response:**
```json
{
  "id": "nb-1234567890abcdef",
  "name": "production-ml-notebook",
  "status": "creating",
  "framework": "pytorch-2",
  "instance_type": "gpu-t4",
  "commitment_period": 60,
  "commitment_expires": "2024-04-15T10:30:00Z",
  "auto_renewal": true,
  "cost_per_month": 6026,
  "currency": "INR",
  "region": "mumbai-1",
  "specifications": {
    "cpu_cores": 8,
    "memory_gb": 32,
    "storage_gb": 100,
    "gpu_count": 1,
    "gpu_type": "nvidia-t4"
  },
  "network": {
    "public_ip": "203.0.113.10",
    "private_ip": "10.0.1.15",
    "ssh_port": 22,
    "jupyter_port": 8888
  },
  "access": {
    "ssh_endpoint": "ubuntu@203.0.113.10",
    "jupyter_url": "https://203.0.113.10:8888",
    "api_endpoint": "https://203.0.113.10:8000"
  },
  "created_at": "2024-01-15T10:30:00Z",
  "updated_at": "2024-01-15T10:30:00Z"
}
```

#### Update Notebook Plan

**Endpoint:** `PATCH /api/v1/notebooks/{notebook_id}/plan`

```bash
curl -X PATCH https://api.e2enetworks.com/v1/notebooks/nb-1234567890abcdef/plan \
  -H "Authorization: Bearer $E2E_API_TOKEN" \
  -H "Content-Type: application/json" \
  -d '{
    "commitment_period": 90,
    "effective_date": "immediate",
    "specifications": {
      "cpu_cores": 16,
      "memory_gb": 64,
      "storage_gb": 200
    },
    "billing_adjustment": "prorated"
  }'
```

**Update Options:**

| Parameter | Options | Description | Impact |
|-----------|---------|-------------|--------|
| `commitment_period` | 30, 60, 90 | New commitment duration | Changes discount rate |
| `effective_date` | `immediate`, `next_cycle`, specific date | When changes take effect | Affects billing calculation |
| `billing_adjustment` | `prorated`, `next_cycle` | How to handle cost differences | Immediate vs deferred billing |
| `auto_renewal` | `true`, `false` | Renewal preference | Future commitment behavior |

#### Get Notebook Status and Details

**Endpoint:** `GET /api/v1/notebooks/{notebook_id}`

```bash
curl -X GET https://api.e2enetworks.com/v1/notebooks/nb-1234567890abcdef \
  -H "Authorization: Bearer $E2E_API_TOKEN"
```

**Detailed Response:**
```json
{
  "id": "nb-1234567890abcdef",
  "name": "production-ml-notebook",
  "status": "running",
  "health": {
    "overall": "healthy",
    "jupyter": "active",
    "ssh": "active",
    "gpu": "available",
    "disk_usage": "45%",
    "memory_usage": "62%",
    "cpu_usage": "23%"
  },
  "commitment": {
    "period": 60,
    "started": "2024-01-15T10:30:00Z",
    "expires": "2024-04-15T10:30:00Z",
    "days_remaining": 45,
    "auto_renewal": true,
    "next_renewal_date": "2024-04-15T10:30:00Z"
  },
  "billing": {
    "current_cost": "₹6026/month",
    "total_spent": "₹3013",
    "projected_monthly": "₹6026",
    "savings_vs_hourly": "₹2009",
    "next_billing_date": "2024-02-15T10:30:00Z"
  },
  "usage_stats": {
    "uptime_percentage": 98.5,
    "avg_cpu_utilization": 45.2,
    "avg_memory_utilization": 67.8,
    "avg_gpu_utilization": 82.1,
    "data_transfer_gb": 125.7
  },
  "specifications": {
    "framework": "pytorch-2",
    "framework_version": "2.1.0",
    "python_version": "3.9.18",
    "cuda_version": "11.8",
    "instance_type": "gpu-t4",
    "cpu_cores": 8,
    "memory_gb": 32,
    "storage_gb": 100,
    "gpu_count": 1,
    "gpu_type": "nvidia-t4",
    "gpu_memory_gb": 16
  }
}
```

#### List All Notebooks

**Endpoint:** `GET /api/v1/notebooks`

```bash
# List all notebooks with filtering
curl -X GET "https://api.e2enetworks.com/v1/notebooks?status=running&commitment_type=committed&limit=50" \
  -H "Authorization: Bearer $E2E_API_TOKEN"
```

**Query Parameters:**

| Parameter | Options | Description | Example |
|-----------|---------|-------------|---------|
| `status` | `creating`, `running`, `stopped`, `error` | Filter by notebook status | `?status=running` |
| `commitment_type` | `committed`, `hourly` | Filter by billing type | `?commitment_type=committed` |
| `framework` | `pytorch-2`, `tensorflow-2` | Filter by ML framework | `?framework=pytorch-2` |
| `region` | `mumbai-1`, `delhi-1` | Filter by geographic region | `?region=mumbai-1` |
| `limit` | 1-100 | Maximum results per page | `?limit=25` |
| `offset` | 0+ | Pagination offset | `?offset=25` |

#### Delete Notebook

**Endpoint:** `DELETE /api/v1/notebooks/{notebook_id}`

```bash
curl -X DELETE https://api.e2enetworks.com/v1/notebooks/nb-1234567890abcdef \
  -H "Authorization: Bearer $E2E_API_TOKEN" \
  -H "Content-Type: application/json" \
  -d '{
    "confirm_deletion": true,
    "backup_data": false,
    "reason": "project_completed"
  }'
```

### Automation Scripts

#### Python SDK Integration

```python
import requests
import json
from datetime import datetime, timedelta

class E2ENotebookManager:
    def __init__(self, api_token, base_url="https://api.e2enetworks.com/v1"):
        self.api_token = api_token
        self.base_url = base_url
        self.headers = {
            "Authorization": f"Bearer {api_token}",
            "Content-Type": "application/json"
        }
    
    def create_committed_notebook(self, config):
        """Create a new committed notebook with specified configuration"""
        endpoint = f"{self.base_url}/notebooks/committed"
        response = requests.post(endpoint, headers=self.headers, json=config)
        return response.json()
    
    def get_notebook_status(self, notebook_id):
        """Get detailed status and metrics for a specific notebook"""
        endpoint = f"{self.base_url}/notebooks/{notebook_id}"
        response = requests.get(endpoint, headers=self.headers)
        return response.json()
    
    def update_notebook_plan(self, notebook_id, updates):
        """Update commitment plan or specifications"""
        endpoint = f"{self.base_url}/notebooks/{notebook_id}/plan"
        response = requests.patch(endpoint, headers=self.headers, json=updates)
        return response.json()
    
    def monitor_expiring_notebooks(self, days_threshold=7):
        """Find notebooks expiring within specified days"""
        notebooks = self.list_notebooks()
        expiring = []
        
        threshold_date = datetime.now() + timedelta(days=days_threshold)
        
        for notebook in notebooks:
            expiry = datetime.fromisoformat(notebook['commitment_expires'].replace('Z', '+00:00'))
            if expiry <= threshold_date:
                expiring.append(notebook)
        
        return expiring
    
    def auto_renew_management(self, notebook_id, enable=True):
        """Enable or disable auto-renewal for a notebook"""
        config = {"auto_renewal": enable}
        return self.update_notebook_plan(notebook_id, config)

# Usage example
manager = E2ENotebookManager("your_api_token_here")

# Create a new committed notebook
notebook_config = {
    "name": "automated-ml-pipeline",
    "framework": "pytorch-2",
    "instance_type": "gpu-t4",
    "commitment_period": 60,
    "auto_renewal": True,
    "specifications": {
        "cpu_cores": 8,
        "memory_gb": 32,
        "storage_gb": 100,
        "gpu_count": 1
    }
}

new_notebook = manager.create_committed_notebook(notebook_config)
print(f"Created notebook: {new_notebook['id']}")

# Monitor notebooks expiring soon
expiring_notebooks = manager.monitor_expiring_notebooks(days_threshold=14)
for notebook in expiring_notebooks:
    print(f"Notebook {notebook['name']} expires on {notebook['commitment_expires']}")
```

#### Bash Automation Scripts

```bash
#!/bin/bash
# E2E Notebook Management Automation Script

API_TOKEN="your_api_token_here"
BASE_URL="https://api.e2enetworks.com/v1"

# Function to create committed notebook
create_notebook() {
    local name=$1
    local commitment_period=$2
    local instance_type=$3
    
    curl -s -X POST "${BASE_URL}/notebooks/committed" \
        -H "Authorization: Bearer ${API_TOKEN}" \
        -H "Content-Type: application/json" \
        -d "{
            \"name\": \"${name}\",
            \"framework\": \"pytorch-2\",
            \"instance_type\": \"${instance_type}\",
            \"commitment_period\": ${commitment_period},
            \"auto_renewal\": true,
            \"specifications\": {
                \"cpu_cores\": 8,
                \"memory_gb\": 32,
                \"storage_gb\": 100,
                \"gpu_count\": 1
            }
        }" | jq '.'
}

# Function to check notebook status
check_status() {
    local notebook_id=$1
    
    curl -s -X GET "${BASE_URL}/notebooks/${notebook_id}" \
        -H "Authorization: Bearer ${API_TOKEN}" | jq '.status, .health'
}

# Function to list expiring notebooks
list_expiring_notebooks() {
    local days_threshold=$1
    
    # Get all committed notebooks
    curl -s -X GET "${BASE_URL}/notebooks?commitment_type=committed" \
        -H "Authorization: Bearer ${API_TOKEN}" | \
        jq --arg threshold "$days_threshold" '
            .notebooks[] | 
            select(
                (.commitment_expires | fromdateiso8601) < 
                (now + ($threshold | tonumber) * 86400)
            ) | 
            {id, name, commitment_expires, days_remaining: 
                ((.commitment_expires | fromdateiso8601) - now) / 86400 | floor
            }'
}

# Function to bulk update auto-renewal settings
bulk_update_renewal() {
    local enable_renewal=$1
    
    # Get all notebook IDs
    notebook_ids=$(curl -s -X GET "${BASE_URL}/notebooks?commitment_type=committed" \
        -H "Authorization: Bearer ${API_TOKEN}" | jq -r '.notebooks[].id')
    
    for id in $notebook_ids; do
        echo "Updating auto-renewal for notebook: $id"
        curl -s -X PATCH "${BASE_URL}/notebooks/${id}/plan" \
            -H "Authorization: Bearer ${API_TOKEN}" \
            -H "Content-Type: application/json" \
            -d "{\"auto_renewal\": ${enable_renewal}}" | jq '.auto_renewal'
    done
}

# Usage examples
case "$1" in
    "create")
        create_notebook "$2" "$3" "$4"
        ;;
    "status")
        check_status "$2"
        ;;
    "expiring")
        list_expiring_notebooks "${2:-7}"
        ;;
    "renewal")
        bulk_update_renewal "${2:-true}"
        ;;
    *)
        echo "Usage: $0 {create|status|expiring|renewal} [parameters...]"
        echo "  create <name> <period> <instance_type>"
        echo "  status <notebook_id>"
        echo "  expiring [days_threshold]"
        echo "  renewal [true|false]"
        ;;
esac
```

### Webhook Integration

#### Setting Up Webhooks

```bash
# Register webhook for notebook events
curl -X POST https://api.e2enetworks.com/v1/webhooks \
  -H "Authorization: Bearer $E2E_API_TOKEN" \
  -H "Content-Type: application/json" \
  -d '{
    "url": "https://your-domain.com/webhook/notebook-events",
    "events": [
      "notebook.created",
      "notebook.status_changed",
      "notebook.commitment_expiring",
      "notebook.auto_renewal_failed"
    ],
    "secret": "your_webhook_secret"
  }'
```

#### Webhook Event Examples

| Event Type | Description | Payload Includes |
|------------|-------------|------------------|
| `notebook.created` | New notebook successfully created | Notebook details, access URLs |
| `notebook.status_changed` | Status change (running, stopped, error) | Old status, new status, timestamp |
| `notebook.commitment_expiring` | Commitment expires within 7 days | Expiry date, renewal status |
| `notebook.auto_renewal_failed` | Auto-renewal payment failed | Error details, grace period |

---

## Troubleshooting & Support

Common issues and comprehensive solutions when working with committed notebooks, including diagnostic procedures and resolution strategies.

### Common Issues & Solutions

#### Payment and Billing Issues

| Issue | Symptoms | Root Cause | Resolution Steps | Prevention |
|-------|----------|------------|------------------|------------|
| **Auto-renewal Payment Failed** | Email notification, notebook suspended | Expired/invalid payment method | 1. Update payment method<br>2. Contact billing within 48h<br>3. Request grace period extension | Set up payment method alerts |
| **Unexpected Charges** | Higher than expected bill | Plan changes not properly calculated | 1. Review billing history<br>2. Check plan change dates<br>3. Contact billing support | Monitor plan changes carefully |
| **Prorated Billing Confusion** | Unclear billing amounts | Mid-cycle plan changes | 1. Request detailed billing breakdown<br>2. Verify change effective dates | Understand prorated calculations |

**Payment Issue Resolution Process:**
```bash
# Check current payment methods
curl -X GET https://api.e2enetworks.com/v1/billing/payment-methods \
  -H "Authorization: Bearer $API_TOKEN"

# Update primary payment method
curl -X PATCH https://api.e2enetworks.com/v1/billing/payment-methods/primary \
  -H "Authorization: Bearer $API_TOKEN" \
  -d '{"payment_method_id": "pm_new_card_id"}'
```

#### Performance and Resource Issues

| Issue | Symptoms | Diagnostic Steps | Resolution |
|-------|----------|------------------|------------|
| **Slow Performance** | High latency, timeouts | Check resource utilization | Upgrade instance or optimize code |
| **Out of Memory Errors** | Process crashes, kernel restarts | Monitor memory usage patterns | Increase RAM or optimize memory usage |
| **GPU Not Detected** | CUDA errors, no GPU acceleration | Verify GPU allocation | Check instance type, restart notebook |
| **Storage Full** | Cannot save files, disk errors | Check disk usage | Clean up files or increase storage |

**Performance Diagnostic Commands:**
```bash
# Check system resources
htop                          # CPU and memory usage
nvidia-smi                    # GPU utilization
df -h                         # Disk space
iostat -x 1                   # I/O performance

# Monitor notebook performance
jupyter lab --generate-config # Generate config for optimization
```

#### Access and Connectivity Issues

| Issue | Symptoms | Common Causes | Solution |
|-------|----------|---------------|----------|
| **Cannot Access Jupyter** | Connection timeout, 404 errors | Firewall, service down | Check security groups, restart service |
| **SSH Connection Failed** | Permission denied, timeouts | Key issues, network blocks | Verify SSH keys, check network settings |
| **Slow Network Performance** | High latency, slow downloads | Network congestion, routing | Change regions, contact support |

**Connectivity Troubleshooting:**
```bash
# Test network connectivity
ping your-notebook-ip         # Basic connectivity
telnet your-notebook-ip 22    # SSH port accessibility
curl -I https://your-notebook-ip:8888  # Jupyter availability

# Check SSH configuration
ssh -vvv ubuntu@your-notebook-ip  # Verbose SSH debugging
```

#### Configuration and Environment Issues

| Issue | Symptoms | Resolution | Time to Fix |
|-------|----------|------------|-------------|
| **Package Installation Failures** | Import errors, dependency conflicts | Use virtual environments, pin versions | 15-30 minutes |
| **Kernel Crashes** | Notebook disconnections, restart loops | Reduce memory usage, check code | 10-20 minutes |
| **Framework Version Conflicts** | Import errors, deprecated warnings | Create new environment with specific versions | 30-60 minutes |

### Support Resources

#### Contact Information

| Support Type | Availability | Contact Method | Response Time |
|--------------|--------------|----------------|---------------|
| **General Support** | 24/7 | support@e2enetworks.com | 4-6 hours |
| **Technical Support** | Business hours | technical@e2enetworks.com | 2-4 hours |
| **Billing Support** | Business hours | billing@e2enetworks.com | 1-2 hours |
| **Emergency Support** | 24/7 | +91-11-4084-0700 | 15-30 minutes |

#### Self-Service Resources

| Resource Type | URL | Content | Update Frequency |
|---------------|-----|---------|------------------|
| **Documentation** | docs.e2enetworks.com | Complete guides, API reference | Weekly |
| **Community Forum** | community.e2enetworks.com | User discussions, solutions | Daily |
| **Status Page** | status.e2enetworks.com | Service health, incidents | Real-time |
| **Knowledge Base** | help.e2enetworks.com | FAQs, troubleshooting | Bi-weekly |

#### Support Ticket Guidelines

**Information to Include in Support Tickets:**

| Category | Required Information | Optional but Helpful |
|----------|---------------------|---------------------|
| **Notebook Details** | Notebook ID, instance type, region | Usage patterns, recent changes |
| **Issue Description** | Error messages, steps to reproduce | Screenshots, log files |
| **Timeline** | When issue started, frequency | Previous occurrences |
| **Impact** | Affected users, business impact | Urgency level, deadlines |

**Ticket Priority Levels:**

| Priority | Response Time | Examples |
|----------|---------------|----------|
| **Critical** | 30 minutes | Production down, data loss |
| **High** | 2 hours | Performance issues, access problems |
| **Medium** | 6 hours | Configuration help, billing questions |
| **Low** | 24 hours | Feature requests, general questions |

### Diagnostic Tools and Logs

#### Built-in Monitoring

**System Metrics Dashboard:**
- CPU, memory, and GPU utilization graphs
- Network I/O and disk usage trends
- Application-level performance metrics
- Real-time alerting for threshold breaches

**Log Access Methods:**
```bash
# Application logs
journalctl -u jupyter-lab -f    # Jupyter service logs
docker logs notebook-container  # Container logs (if applicable)

# System logs
tail -f /var/log/syslog         # System events
dmesg | tail                    # Kernel messages

# Custom application logs
tail -f ~/notebooks/app.log     # Application-specific logs
```

#### Performance Optimization

**Optimization Checklist:**

| Optimization Area | Actions | Expected Improvement |
|------------------|---------|---------------------|
| **Memory Management** | Use memory profilers, optimize data loading | 20-40% performance gain |
| **CPU Utilization** | Parallelize workflows, optimize algorithms | 30-60% faster processing |
| **GPU Acceleration** | Use GPU-optimized libraries, batch processing | 5-50x speedup for ML tasks |
| **I/O Operations** | Cache frequently accessed data, use SSD storage | 2-10x faster data access |

**Optimization Commands:**
```python
# Memory profiling
%load_ext memory_profiler
%memit your_function()

# CPU profiling
import cProfile
cProfile.run('your_function()')

# GPU monitoring
import GPUtil
GPUtil.showUtilization()
```

---

## Conclusion

This comprehensive guide provides everything needed to successfully create, manage, and optimize committed notebooks on the E2E Networks TIR AI Platform. The hybrid approach of maintaining visual screenshots while adding detailed explanatory text ensures both human usability and RAG system compatibility.

### Key Takeaways

- **Cost Optimization:** Committed plans offer up to 30% savings for long-term projects
- **Flexibility:** Multiple upgrade, downgrade, and conversion options during commitment periods
- **Automation:** Comprehensive API support enables infrastructure-as-code approaches
- **Support:** 24/7 support with multiple contact channels and self-service resources

### Next Steps

1. **Plan Your Commitment:** Analyze your usage patterns to choose optimal commitment periods
2. **Set Up Monitoring:** Implement automated monitoring for expiring commitments and resource utilization
3. **Establish Backup Procedures:** Create regular backup schedules for critical data and configurations
4. **Optimize Costs:** Regular review of resource utilization to ensure cost-effectiveness

For additional support or questions about committed notebooks, contact E2E Networks support at support@e2enetworks.com or visit the comprehensive documentation at docs.e2enetworks.com.
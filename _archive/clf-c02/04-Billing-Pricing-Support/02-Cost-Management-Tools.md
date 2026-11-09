---
tags:
  - aws
  - cloud-practitioner
  - billing
  - cost-management
domain: Billing, Pricing, and Support
aliases:
  - "Cost Explorer"
  - "AWS Budgets"
  - "Cost Management"
  - "Cost Allocation"
  - "CUR"
status: not-started
date: 2026-07-01
---

# Cost Management Tools

## AWS Organizations & Consolidated Billing

- **Consolidated Billing**: one payment method for all accounts in an organization
- Benefits:
  - **Volume pricing discounts** — combined usage across all accounts (S3, EC2)
  - **Pooled EC2 Reserved Instances** — unused RIs in one account can be used by others
  - Single invoice for all accounts

---

## Cost Allocation Tags

- **Tags** used to track AWS costs at a detailed level
- Two types:
  - **AWS-generated tags**: automatically applied; prefix `aws:` (e.g., `aws:createdBy`)
  - **User-defined tags**: created by you; prefix `user:` (e.g., `user:Team`, `user:Environment`)
- Tags appear in the **Cost and Usage Report**
- Common tags: `Name`, `Environment`, `Team`, `Project`

### Resource Groups
- Group AWS resources by tag to view/manage them together
- Example: all resources tagged `Environment=Production`

---

## AWS Cost and Usage Reports (CUR)

- **Most comprehensive** cost and usage data available
- Contains detailed line items for every AWS service
- Includes: pricing, usage, tags, resource IDs, metadata
- Delivered to an **S3 bucket**
- Can integrate with: Athena, Redshift, QuickSight for analysis

---

## AWS Cost Explorer

- **Visualize, understand, and manage** AWS costs over time
- Create custom reports analyzing cost and usage data
- Analyze at any granularity: account, service, resource
- **Forecast usage** up to 12 months
- **Identify Savings Plans** opportunities
- View: monthly, hourly, resource-level granularity

> [!tip]
> Cost Explorer is the go-to tool for analyzing historical spending and forecasting future costs.

---

## Billing Alarms in CloudWatch

- Billing metric stored in **CloudWatch us-east-1** (worldwide totals)
- Set alarms for **actual cost** (not projected)
- Simple notification when billing exceeds threshold
- Less powerful than AWS Budgets

---

## AWS Budgets

- Set **custom budgets** and get **alerted** when costs or usage exceed thresholds
- 4 budget types:
  1. **Cost budget** — track spending ($)
  2. **Usage budget** — track usage (hours, requests)
  3. **Reservation budget** — track RI utilization
  4. **Savings Plans budget** — track Savings Plans coverage
- Can send alerts: before, when, or forecasted to exceed budget
- First 2 budgets are free; $0.02/day per additional budget
- Can trigger SNS notifications or actions (e.g., apply IAM policy to restrict usage)

---

## AWS Cost Anomaly Detection

- Uses **ML to detect unusual spending patterns**
- Monitors your cost and usage data
- Sends alerts when unexpected spending spikes occur
- Can create monitors for specific services, accounts, or cost categories

---

## AWS Service Quotas

- View and manage your **service limits** (quotas)
- Set **CloudWatch alarms** when approaching a quota
- Request quota increases through Service Quotas console
- Example: "Alert when EC2 instances in us-east-1 reach 450 of 500 limit"

---

## Cost Tools Comparison

| Tool | Purpose | Key Feature |
|---|---|---|
| **Pricing Calculator** | Estimate BEFORE deploying | Plan architecture costs |
| **Billing Dashboard** | View current bill | Month-to-date; forecasted |
| **Cost & Usage Reports** | Most detailed data | Line-item per resource; goes to S3 |
| **Cost Explorer** | Visualize trends | Forecasts; custom reports |
| **Billing Alarms** | Simple cost alerts | CloudWatch; actual cost |
| **AWS Budgets** | Proactive budget management | 4 types; threshold alerts; actions |
| **Cost Anomaly Detection** | ML anomaly alerts | Detects unusual spend patterns |

---

## Exam Tips

> [!tip]
> - Consolidated Billing = single bill for all org accounts + volume discounts
> - Cost Explorer = historical analysis + 12-month forecast
> - AWS Budgets = set alert thresholds for spend/usage (proactive)
> - CloudWatch Billing Alarm = reactive; actual cost only
> - Cost & Usage Report = most detailed; goes to S3
> - Cost Anomaly Detection = ML-based unusual spend detection

> [!warning]
> CloudWatch Billing Alarms are based on **actual** cost, NOT projected. AWS Budgets can alert on **forecasted** costs too — more powerful.

## Related Notes
- [[01-Pricing-Models]]
- [[03-Support-Plans]]

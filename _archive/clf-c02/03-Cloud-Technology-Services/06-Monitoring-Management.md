---
tags:
  - aws
  - cloud-practitioner
  - technology
  - cloudwatch
  - cloudtrail
  - monitoring
domain: Cloud Technology and Services
aliases:
  - "CloudWatch"
  - "X-Ray"
  - "SSM"
  - "Monitoring"
  - "Observability"
  - "Compute Optimizer"
status: not-started
date: 2026-07-01
---

# Monitoring & Management

## Amazon CloudWatch

### CloudWatch Metrics
- Monitor AWS services and custom metrics
- Examples: EC2 CPUUtilization, NetworkIn, S3 BucketSizeBytes
- Default metrics available for free; some detailed metrics cost extra
- Metrics have a **namespace** and **dimensions**

### CloudWatch Alarms
- Trigger notifications when a metric crosses a threshold
- Actions: send SNS notification, auto-scale EC2, stop/terminate/recover EC2 instance
- States: OK, ALARM, INSUFFICIENT_DATA
- Billing alarm example: alert when bill exceeds $X (stored in CloudWatch us-east-1)

### CloudWatch Logs
- Collect, monitor, and store **log files**
- Sources: EC2 (via CloudWatch agent), Lambda, ECS, CloudTrail, Route 53
- EC2 instances need the **CloudWatch agent** to send logs
- Adjustable **log retention** (1 day to 10 years)
- Real-time monitoring

### Amazon EventBridge (CloudWatch Events)
- **Serverless event bus** — schedule tasks or react to events
- Create rules based on:
  - **Schedule** (cron jobs): "Run every Monday at 10am"
  - **Event pattern**: "When an EC2 instance changes state to stopped → trigger Lambda"
- Integrates with many AWS services and SaaS partners

---

## AWS CloudTrail

- **Record and audit all API calls** made in your AWS account
- Records: who made the call, what was called, when, from where
- Default retention: **90 days** in CloudTrail console
- Export to **S3** for longer retention
- Export to **CloudWatch Logs** for real-time monitoring
- Applies to: Console, CLI, SDK, AWS services

### CloudTrail Insights
- Detects **unusual API activity** patterns
- Examples: sudden spike in IAM role creation, unusual number of terminated instances

> [!tip]
> "Who deleted my EC2 instance?" → CloudTrail. It records every API call.

---

## AWS X-Ray

- **Distributed tracing** for debugging and profiling
- Provides a **visual service map** of your application
- Helps identify bottlenecks, errors, latency issues
- Works with: EC2, Lambda, ECS, API Gateway
- Great for microservices architectures

---

## Amazon CodeGuru

- **ML-powered code review and application performance recommendations**
- **CodeGuru Reviewer**: automated code reviews (finds bugs, security issues) — for pull requests
- **CodeGuru Profiler**: performance recommendations in production
- Supports: Java and Python
- Finds expensive code lines, identifies performance bottlenecks

---

## AWS Health Dashboard

- **Service Health Dashboard**: real-time status of all AWS services in all regions
  - Previously "AWS Service Health Dashboard"
  - Publishes historical info on service availability
  
- **AWS Personal Health Dashboard** (now "AWS Health"):
  - **Proactive notifications** for events affecting YOUR AWS resources
  - "Your RDS instance in us-east-1 may be affected by the ongoing issue"
  - Alerts for scheduled maintenance, deprecated services

---

## AWS Systems Manager (SSM)

- Manage **EC2 and on-premises** servers at scale
- **Hybrid service** — works for both AWS and non-AWS infrastructure
- Provides: patch management, run commands, state manager
- **No SSH required** — uses SSM agent (pre-installed on Amazon Linux 2 and some Windows)
- **Free to use**

### SSM Session Manager
- **Secure shell access** to EC2 instances without SSH
- No need to open port 22
- Full audit trail in CloudTrail
- Works on EC2 and on-premises machines

---

## AWS Trusted Advisor

- Real-time recommendations across **5 categories**:

| Category | Examples |
|---|---|
| **Cost Optimization** | Idle EC2, underutilized RDS, unassociated Elastic IPs |
| **Performance** | Overutilized EC2 instances, CloudFront delivery optimization |
| **Security** | Open security groups, MFA on root, public S3 buckets |
| **Fault Tolerance** | EC2 without backups, single AZ deployments |
| **Service Limits** | Approaching EC2 or IAM service quotas |

| Plan | Access |
|---|---|
| Basic / Developer | 7 core security checks |
| Business / Enterprise | 125+ checks + programmatic API access |

---

## Exam Tips

> [!tip]
> - CloudWatch = metrics, alarms, logs (monitoring)
> - CloudTrail = API call history (auditing who did what)
> - X-Ray = distributed tracing for debugging microservices
> - EventBridge = event-driven automation (cron + event patterns)
> - SSM = manage EC2 without SSH; hybrid (on-premises + cloud)
> - Trusted Advisor = recommendations for cost, performance, security, fault tolerance, service limits

> [!warning]
> CloudWatch ≠ CloudTrail. CloudWatch monitors performance metrics and logs. CloudTrail records API calls for audit/governance. They're often confused on the exam.

## Related Notes
- [[05-Compliance-Governance]]
- [[07-Application-Integration]]

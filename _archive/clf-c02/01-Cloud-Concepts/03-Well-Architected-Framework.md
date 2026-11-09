---
tags:
  - aws
  - cloud-practitioner
  - cloud-concepts
  - well-architected
domain: Cloud Concepts
aliases:
  - "Well Architected"
  - "6 Pillars"
  - "WAF"
  - "WAP"
status: not-started
date: 2026-07-01
---

# Well-Architected Framework

## Overview

The AWS Well-Architected Framework helps cloud architects build secure, high-performing, resilient, and efficient infrastructure. It consists of **6 pillars**.

---

## The 6 Pillars

### 1. Operational Excellence
Run and monitor systems to deliver business value and continually improve processes.
- Perform operations as code (IaC)
- Annotate documentation
- Make frequent, small, reversible changes
- Refine operations procedures frequently
- Anticipate failure

### 2. Security
Protect information, systems, and assets while delivering business value.
- Implement a strong identity foundation (least privilege, MFA)
- Enable traceability (CloudTrail, logs)
- Apply security at all layers
- Automate security best practices
- Protect data in transit and at rest
- Prepare for security events

### 3. Reliability
Ensure a workload performs its intended function correctly and consistently.
- Automatically recover from failure
- Test recovery procedures
- Scale horizontally (increase aggregate availability)
- Stop guessing capacity
- Manage change through automation

### 4. Performance Efficiency
Use computing resources efficiently to meet system requirements and maintain efficiency as demand changes.
- Democratize advanced technologies
- Go global in minutes
- Use serverless architectures
- Experiment more often
- Consider mechanical sympathy (use the right resource type)

### 5. Cost Optimization
Avoid unnecessary costs.
- Adopt a consumption model (pay for what you use)
- Measure overall efficiency
- Stop spending money on undifferentiated heavy lifting
- Analyze and attribute expenditure
- Use managed and application-level services

### 6. Sustainability
Minimize environmental impact of running cloud workloads.
- Understand your impact
- Establish sustainability goals
- Maximize utilization
- Anticipate and adopt new efficient offerings
- Use managed services (more efficient)
- Reduce downstream impact

---

## AWS Well-Architected Tool

- Free tool in the AWS Console
- Review your architecture against the 6 pillars
- Get recommendations for improvement

---

## Exam Tips

> [!tip]
> - Memorize all **6 pillars** and their key themes
> - "Cost Optimization pillar" = right-sizing, on-demand/reserved, eliminating waste
> - "Reliability pillar" = fault tolerance, backups, multi-AZ, auto-recovery
> - "Security pillar" = least privilege, MFA, encryption, traceability
> - The Well-Architected Tool is **free**

> [!warning]
> Common trick: "Which pillar focuses on using the right resource type for the workload?" → **Performance Efficiency**

## Related Notes
- [[01-Cloud-Computing-Fundamentals]]
- [[04-Cloud-Adoption-Migration]]

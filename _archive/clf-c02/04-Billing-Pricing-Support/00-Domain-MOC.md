---
tags:
  - aws
  - cloud-practitioner
  - billing
  - moc
domain: Billing, Pricing, and Support
aliases:
  - "Billing MOC"
  - "Domain 4"
  - "D4"
status: not-started
date: 2026-07-01
---

# Domain 4: Billing, Pricing & Support — Map of Content

**Exam Weight: 12%** (~8 questions)

---

## Notes in This Domain

1. [[01-Pricing-Models]] — EC2 purchasing options, S3 pricing, AWS Free Tier, Savings Plans, Pricing Calculator, TCO
2. [[02-Cost-Management-Tools]] — Consolidated Billing, Cost Allocation Tags, CUR, Cost Explorer, Billing Alarms, AWS Budgets, Cost Anomaly Detection
3. [[03-Support-Plans]] — Basic, Developer, Business, Enterprise On-Ramp, Enterprise; response times; TAMs; Trusted Advisor; AWS Marketplace; APN

---

## Key Exam Themes

- EC2 pricing models and when to use each
- AWS Free Tier (always-free vs 12-month vs trial)
- Consolidated Billing and volume discounts
- Cost Explorer (historical + forecast) vs Budgets (alerts)
- Support plan response times and features
- Trusted Advisor checks by support plan

---

## Quick Reference

### EC2 Pricing Options Summary

| Option | Discount | Best For |
|---|---|---|
| On-Demand | 0% | Short-term, unpredictable |
| Savings Plans | Up to 72% | Flexible long-term commitment |
| Reserved (Standard) | Up to 72% | Predictable workloads, specific type |
| Reserved (Convertible) | Up to 66% | Predictable but flexible workloads |
| Spot | Up to 90% | Fault-tolerant, batch workloads |
| Dedicated Host | Varies | BYOL, compliance |
| Capacity Reservations | 0% | Guaranteed capacity, no discount |

### Support Plans Summary

| Plan | Cost | 24/7 Support | TAM | Prod Down Response |
|---|---|---|---|---|
| Basic | Free | ✗ | ✗ | N/A |
| Developer | $29+/mo | ✗ (email only) | ✗ | N/A |
| Business | $100+/mo | ✓ | ✗ | < 1 hour |
| Enterprise On-Ramp | $5,500+/mo | ✓ | Pool | < 30 min |
| Enterprise | $15,000+/mo | ✓ | Dedicated | < 15 min |

### Cost Management Tools

| Tool | Use When |
|---|---|
| Pricing Calculator | Planning architecture costs before deployment |
| Cost & Usage Reports | Need most detailed, line-item cost data |
| Cost Explorer | Visualizing trends and forecasting |
| AWS Budgets | Proactive alerts when costs exceed threshold |
| CloudWatch Billing Alarm | Simple alert for actual cost |
| Cost Anomaly Detection | ML-based unusual spending alerts |

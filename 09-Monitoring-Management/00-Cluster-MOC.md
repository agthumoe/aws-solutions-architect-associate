---
tags: [aws, saa-c03, moc, monitoring]
domain: Monitoring-Management
exam-domains: [1, 2, 3]
aliases:
  - "Monitoring & Management MOC"
status: not-started
date: 2026-07-21
---

# Monitoring & Management — Cluster MOC

## Key Concepts

This cluster covers how AWS Solutions Architects observe, audit, and govern resources across an account: performance monitoring and alerting (CloudWatch), API call auditing (CloudTrail), and configuration/compliance tracking (AWS Config), tied together via EventBridge event routing.

## Notes in This Cluster

- [[01-Monitoring-Audit-Performance]] — CloudWatch (metrics, logs, alarms, EventBridge, Insights family) vs. CloudTrail (API audit) vs. AWS Config (compliance/configuration history), including a direct comparison table and an Elastic Load Balancer worked example.

## AWS Services / Features

```mermaid
graph TD
    MOC[Monitoring & Management] --> M1[01: Monitoring, Audit & Performance]
    M1 --> CW[CloudWatch<br>Metrics, Logs, Alarms, EventBridge]
    M1 --> CT[CloudTrail<br>API Call Audit]
    M1 --> CFG[AWS Config<br>Compliance & Config History]
```

## Exam Tips
> [!TIP]
> When a question mixes up CloudWatch, CloudTrail, and Config, anchor on the one-line distinction in [[01-Monitoring-Audit-Performance]]: performance vs. audit vs. compliance.

## Related Notes
- [[01-Monitoring-Audit-Performance]]

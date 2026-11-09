---
tags: [aws, saa-c03, architecture-patterns, moc]
domain: Architecture Patterns
exam-domains: [1, 2, 3, 4]
status: not-started
date: 2026-07-21
---

# Architecture Patterns — Cluster MOC

## Key Concepts
This cluster covers the source's capstone architecture material (pages 227–858): the classic and advanced solutions-architecture case studies, disaster recovery & migration strategies, the "Other Services" grab-bag, and the Well-Architected / Trusted Advisor whitepaper material.

## Notes in This Cluster

| Note | Covers |
|---|---|
| [[01-Classic-Solutions-Architecture]] | WhatIsTheTime.com (stateless), MyClothes.com (stateful, sessions, RDS/ElastiCache), MyWordPress.com (EBS vs EFS), instantiating apps quickly, 3-tier reference architecture, Elastic Beanstalk |
| [[02-More-Solutions-Architecture]] | Lambda/SNS/SQS reliability patterns, fan-out, S3 event notifications (native & via EventBridge), API Gateway service integration, caching strategies, blocking an IP (NACL/ALB/NLB/WAF/CloudFront), HPC on AWS, single-instance HA patterns |
| [[03-Disaster-Recovery-Migrations]] | RPO/RTO, the 4 DR strategies (Backup & Restore, Pilot Light, Warm Standby, Multi-Site Active-Active) with a comparison table, AWS Elastic DR, DMS, SCT, Aurora migrations, AWS Backup, AWS Backup Vault Lock, MGN, Application Discovery Service, large data transfer math |
| [[04-Other-Services]] | CloudFormation, SES, Pinpoint, Systems Manager (Session Manager/Run Command/Patch Manager/Automation), Cost Explorer, Cost Anomaly Detection, Outposts, AWS Batch, AppFlow, Amplify, Instance Scheduler |
| [[05-White-Papers-Architectures]] | Well-Architected Framework guiding principles & 6 pillars, Well-Architected Tool, Trusted Advisor, reference architecture resources |

## Exam Tips
> [!TIP]
> If studying for **Domain 2 (Security and Compliance / Design Resilient Architectures)**, prioritize [[03-Disaster-Recovery-Migrations]] — the 4 DR strategies comparison table is one of the most heavily tested patterns on the exam.

> [!TIP]
> [[01-Classic-Solutions-Architecture]] and [[02-More-Solutions-Architecture]] are best studied by tracing the **progression diagrams** (single instance → HA/multi-AZ) rather than memorizing isolated facts — the exam favors scenario questions that test *why* each architectural step is needed.

## Related Notes
- [[01-Classic-Solutions-Architecture]]
- [[02-More-Solutions-Architecture]]
- [[03-Disaster-Recovery-Migrations]]
- [[04-Other-Services]]
- [[05-White-Papers-Architectures]]

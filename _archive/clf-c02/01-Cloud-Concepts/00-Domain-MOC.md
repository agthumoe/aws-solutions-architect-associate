---
tags:
  - aws
  - cloud-practitioner
  - cloud-concepts
  - moc
domain: Cloud Concepts
aliases:
  - "Cloud Concepts MOC"
  - "Domain 1"
  - "D1"
status: not-started
date: 2026-07-01
---

# Domain 1: Cloud Concepts — Map of Content

**Exam Weight: 24%** (~16 questions)

---

## Notes in This Domain

1. [[01-Cloud-Computing-Fundamentals]] — What is cloud, 5 characteristics, 6 advantages, deployment models, IaaS/PaaS/SaaS, pricing
2. [[02-AWS-Global-Infrastructure]] — Regions, AZs, Edge Locations, how to choose a region
3. [[03-Well-Architected-Framework]] — 6 pillars: Operational Excellence, Security, Reliability, Performance Efficiency, Cost Optimization, Sustainability
4. [[04-Cloud-Adoption-Migration]] — AWS CAF (6 perspectives), 7 Rs of migration, migration services, AWS ecosystem

---

## Key Exam Themes

- **5 Characteristics** of cloud computing (on-demand, broad access, multi-tenancy, elasticity, measured)
- **6 Advantages** of cloud (CAPEX→OPEX, economies of scale, stop guessing capacity, speed/agility, stop spending on data centers, go global)
- **Deployment models**: Public, Private, Hybrid
- **Service models**: IaaS (EC2), PaaS (Elastic Beanstalk), SaaS (Rekognition, Gmail, Zoom)
- **Region selection factors**: Compliance, Proximity, Available services, Pricing
- **AZs**: isolated data centers within a region; connected with high bandwidth
- **Edge Locations**: 400+; used by CloudFront and Route 53
- **Well-Architected**: 6 pillars — know each one's focus area
- **CAF**: 6 perspectives — Business, People, Governance, Platform, Security, Operations
- **7 Rs**: Retire, Retain, Relocate, Rehost, Replatform, Repurchase, Refactor

---

## Quick Reference

| Concept | Key Fact |
|---|---|
| Cloud computing | On-demand delivery with pay-as-you-go |
| CAPEX | Upfront purchase of hardware (traditional IT) |
| OPEX | Ongoing operational costs (cloud model) |
| Region | Cluster of data centers; most services are region-scoped |
| AZ | 1+ discrete data centers in a region; 3 minimum per region |
| Edge Location | 400+ worldwide; used for content delivery |
| IAM scope | Global — not region-specific |
| Data transfer IN | Free |
| Data transfer OUT | Charged |
| IaaS example | Amazon EC2 |
| PaaS example | Elastic Beanstalk |
| SaaS example | Amazon Rekognition |

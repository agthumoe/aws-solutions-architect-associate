---
tags:
  - aws
  - cloud-practitioner
  - cloud-concepts
  - caf
  - migration
domain: Cloud Concepts
aliases:
  - "CAF"
  - "Cloud Adoption Framework"
  - "7 Rs"
  - "Migration Strategies"
status: not-started
date: 2026-07-01
---

# Cloud Adoption Framework & Migration Strategies

## AWS Cloud Adoption Framework (CAF)

The CAF helps organizations understand how to move to the cloud and what capabilities they need. It has **6 perspectives** grouped into **Business** and **Technical** capabilities.

### The 6 CAF Perspectives

| Perspective | Focus | Who |
|---|---|---|
| **Business** | Ensure cloud investments accelerate digital transformation | Business managers, Finance, Strategy |
| **People** | Change management, roles, capabilities | HR, People managers |
| **Governance** | Maximize business value and minimize risk | CIO, Program managers |
| **Platform** | Build the right cloud platform | CTO, Architects, Engineers |
| **Security** | Achieve security objectives | CISO, Security engineers |
| **Operations** | Deliver and optimize cloud services | IT operations managers |

### CAF Transformation Domains
- Technology
- Process
- Organization
- Product

### CAF Transformation Phases
1. **Envision** — demonstrate how cloud will accelerate business outcomes
2. **Align** — identify capability gaps across the 6 perspectives
3. **Launch** — deliver pilot initiatives and demonstrate incremental value
4. **Scale** — expand pilots and business value to desired scale

---

## Migration Strategies (7 Rs)

When migrating applications to AWS, there are 7 common strategies:

| Strategy | Also Called | Description | Effort |
|---|---|---|---|
| **Retire** | — | Sunset/remove applications no longer needed | None |
| **Retain** | Revisit | Keep on-premises for now (not ready to migrate) | None |
| **Relocate** | — | Move to cloud without changes (e.g., VMware on AWS) | Low |
| **Rehost** | Lift and Shift | Move to AWS without code changes | Low |
| **Replatform** | Lift, Tinker & Shift | Move with minor optimizations (e.g., RDS instead of self-managed DB) | Medium |
| **Repurchase** | Drop and Shop | Move to a different product, often SaaS | Medium |
| **Refactor / Re-architect** | — | Reimagine using cloud-native features; most expensive but biggest gains | High |

> [!tip]
> For the exam: "A company wants to move to AWS with minimal changes" → **Rehost (Lift and Shift)**
> "A company wants to use managed services instead of self-managing" → **Replatform**
> "A company wants to move to a SaaS CRM" → **Repurchase**

---

## AWS Migration Services

| Service | Purpose |
|---|---|
| **AWS Migration Hub** | Central hub to track migration projects |
| **AWS Application Migration Service** | Lift-and-shift (rehost) migration to AWS |
| **Application Discovery Service** | Collect data about on-premises servers to plan migration |
| **AWS Database Migration Service (DMS)** | Migrate databases to AWS; source stays available during migration |
| **AWS DataSync** | Move large amounts of data from on-premises to AWS; scheduled, automated |
| **AWS Transfer Family** | Managed FTP/SFTP/FTPS to/from S3 and EFS |
| **AWS Snow Family** | Physical devices for offline data transfer (Snowcone, Snowball Edge, Snowmobile) |

---

## AWS Ecosystem

| Resource | Description |
|---|---|
| **AWS Marketplace** | Digital catalog of 3rd-party software to run on AWS; pay per use or BYOL |
| **AWS Partner Network (APN)** | Technology Partners (software) and Consulting Partners (professional services) |
| **AWS Professional Services** | Global team to help with cloud adoption |
| **AWS IQ** | Connect with AWS-certified experts for paid project-based help |
| **AWS re:Post** | Q&A community; managed forum for AWS questions (replaced AWS Forums) |

---

## Exam Tips

> [!tip]
> - Know all **7 Rs** of migration — they're frequently tested
> - **Rehost = no code changes**, just move the VM/server
> - **Refactor = biggest investment, biggest payoff**, uses cloud-native services
> - CAF has **6 perspectives**: Business, People, Governance, Platform, Security, Operations

## Related Notes
- [[01-Cloud-Computing-Fundamentals]]
- [[03-Well-Architected-Framework]]

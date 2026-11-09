---
tags:
  - aws
  - saa-c03
  - index
aliases:
  - "Index"
  - "Start Here"
  - "Home"
status: not-started
date: 2026-07-21
---

# AWS Certified Solutions Architect – Associate (SAA-C03) — Study Vault

Target: sit the exam in **1.5–2 months** of intensive study. CLF-C02 (already passed) is archived at `_archive/clf-c02/`.

## Sources
- **AWS Certified Solutions Architect Slides v48.pdf** (Stéphane Maarek, 876 pages)
- **Official SAA-C03 Exam Guide** (AWS Documentation)
- **Official In-Scope / Out-of-Scope Services Lists** (AWS Documentation)

## Quick Links
- [[Online-Resources]] — Official docs, Skill Builder courses
- [[Domain-Overview]] — Visual canvas map of all 4 domains
- [[Study-Progress]] — Obsidian Bases view: all notes with status and domain
- `memory/progress_tracking.md` — 8-week study schedule and checklist

## Exam Info
- **Exam Code**: SAA-C03
- **Questions**: 65 (50 scored + 15 unscored)
- **Duration**: 130 minutes
- **Passing Score**: 720/1000 (scaled 100–1000)
- **Cost**: $150 USD · **Validity**: 3 years

---

## How this vault is organized

Content lives in **topic clusters** (AWS service/topic groupings, matching the course's own structure) since the 4 exam domains are cross-cutting design concerns that touch nearly every service. The **domain pages** below cross-reference official task statements to the cluster notes that cover them — use those for exam-weighted review.

## Exam Domains (official weights)

| Domain | Weight | MOC |
|---|---|---|
| Domain 1: Design Secure Architectures | 30% | [[00-Index/Exam-Domains/01-Design-Secure-Architectures]] |
| Domain 2: Design Resilient Architectures | 26% | [[00-Index/Exam-Domains/02-Design-Resilient-Architectures]] |
| Domain 3: Design High-Performing Architectures | 24% | [[00-Index/Exam-Domains/03-Design-High-Performing-Architectures]] |
| Domain 4: Design Cost-Optimized Architectures | 20% | [[00-Index/Exam-Domains/04-Design-Cost-Optimized-Architectures]] |

---

## Topic Clusters

- [[01-Foundations/00-Cluster-MOC|01 — Foundations]] — Getting Started with AWS, IAM Basics
- [[02-Compute-EC2/00-Cluster-MOC|02 — Compute (EC2)]] — EC2 Basics/Associate/Instance Storage, HA & Scalability (ELB, ASG)
- [[03-Storage/00-Cluster-MOC|03 — Storage]] — S3, S3 Advanced, S3 Security, Storage Extras (FSx, Storage Gateway, Snow, DataSync)
- [[04-Databases/00-Cluster-MOC|04 — Databases]] — RDS/Aurora/ElastiCache, Databases Overview, Data & Analytics
- [[05-Networking-Content-Delivery/00-Cluster-MOC|05 — Networking & Content Delivery]] — Route 53, VPC, CloudFront/Global Accelerator
- [[06-Containers-Serverless/00-Cluster-MOC|06 — Containers & Serverless]] — Containers (ECS/EKS), Serverless Overview & Architectures (Lambda, API Gateway, DynamoDB)
- [[07-Integration-Messaging/00-Cluster-MOC|07 — Integration & Messaging]] — SQS, SNS, Kinesis
- [[08-Security-Identity/00-Cluster-MOC|08 — Security & Identity]] — Advanced Identity (Organizations, SCPs, IAM Identity Center), Security & Encryption (KMS, Shield, WAF, GuardDuty)
- [[09-Monitoring-Management/00-Cluster-MOC|09 — Monitoring & Management]] — CloudWatch, CloudTrail, Config, EventBridge
- [[10-Machine-Learning/00-Cluster-MOC|10 — Machine Learning]] — ML services overview
- [[11-Architecture-Patterns/00-Cluster-MOC|11 — Architecture Patterns]] — Classic & More Solutions Architecture, Disaster Recovery & Migrations, Other Services, White Papers
- [[12-Exam-Prep/00-Cluster-MOC|12 — Exam Prep]] — Exam-day tips and strategy

---

## Practice

- `05-Practice/` — Practice questions and flashcards *(create notes here with `/quiz`)*
- `06-Cheatsheets/` — Quick reference cheatsheets *(create notes here with `/notes`)*
- `exams/` — Full mock exams *(create with `/fullexam` or `/simulate-exam`)*

---

## Commands

| Command | Action |
|---|---|
| `/teach <topic>` | Start a teaching session |
| `/quiz <topic>` | Generate practice questions |
| `/fullexam` | Full 65-question practice exam |
| `/readiness` | Check exam readiness % |
| `/progress` | View study dashboard |
| `/flashcards <topic>` | Generate flashcards |
| `/gap-analysis` | Find coverage gaps |
| `/study-plan` | Create personalized study plan |

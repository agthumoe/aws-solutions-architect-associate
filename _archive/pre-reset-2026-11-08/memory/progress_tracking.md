# Progress Tracking — SAA-C03

Target: sit the exam in **1.5–2 months** (intensive prep). Started: 2026-07-21.

## Domain Status (official weights)

| Domain | Topic | Status | Last Studied | Notes |
|--------|-------|--------|--------------|-------|
| D1 | Design Secure Architectures (30%) | 🔵 Not Started | — | |
| D2 | Design Resilient Architectures (26%) | 🔵 Not Started | — | |
| D3 | Design High-Performing Architectures (24%) | 🔵 Not Started | — | |
| D4 | Design Cost-Optimized Architectures (20%) | 🔵 Not Started | — | |

Status key: 🔵 Not Started | 🟡 In Progress | 🟠 Needs Review | 🟢 Reviewed

---

## Quiz Score Log

| Date | Topic | Score | Notes |
|------|-------|-------|-------|
| — | — | — | — |

---

## Weak Areas

*(none yet — take some quizzes to identify weak areas)*

---

## 8-Week Study Schedule (flexible — adjust via `/schedule` or `/study-plan`)

Sequenced in the course's own dependency order (each topic builds on the last), with the final 2 weeks switching to domain-weighted review via `00-Index/Exam-Domains/`.

| Week | Focus (topic clusters) | Primary domains touched |
|------|------------------------|--------------------------|
| 1 | Foundations, Compute-EC2 (EC2 Basics/Associate/Instance Storage, HA & Scalability) | D2, D3, D4 |
| 2 | Databases pt.1 (RDS/Aurora/ElastiCache), Networking pt.1 (Route 53), Architecture-Patterns (Classic SA), Storage (S3/S3 Advanced/S3 Security) | D1, D2, D3, D4 |
| 3 | Networking pt.2 (CloudFront/Global Accelerator), Storage Extras, Integration-Messaging (SQS/SNS/Kinesis) | D2, D3, D4 |
| 4 | Containers-Serverless (Containers, Serverless Overview/Architectures), Databases pt.2 (Databases Overview, Data & Analytics) | D2, D3, D4 |
| 5 | Machine-Learning, Monitoring-Management, Security-Identity (Advanced Identity, Security & Encryption) | D1, D2, D3 |
| 6 | Networking pt.3 (VPC), Architecture-Patterns (DR & Migrations, More SA, Other Services, White Papers) | D1, D2, D4 |
| 7 | Domain-weighted review — walk `00-Index/Exam-Domains/01-04` in order, `/weakness` drilling, first `/fullexam` | All (weighted) |
| 8 | 2–3 more `/fullexam` simulations, `/finalreview`, `/strategy`, close remaining gaps | All (weighted) |

---

## Topics Covered Checklist

### Domain 1 — Design Secure Architectures (30%)
- [ ] Task 1.1: Secure access to AWS resources (IAM users/roles/policies, MFA, cross-account access, STS, SCPs, Control Tower, federation)
- [ ] Task 1.2: Secure workloads and applications (VPC security components, network segmentation, Shield, WAF, Secrets Manager, Cognito, GuardDuty, Macie, VPN/Direct Connect)
- [ ] Task 1.3: Data security controls (KMS, ACM/TLS, encryption at rest/in transit, backups/replication, key rotation, certificate renewal)

### Domain 2 — Design Resilient Architectures (26%)
- [ ] Task 2.1: Scalable and loosely coupled architectures (API Gateway, SQS/SNS, caching, microservices, event-driven, horizontal/vertical scaling, CDN, containers, ELB, multi-tier, Step Functions, read replicas)
- [ ] Task 2.2: Highly available and/or fault-tolerant architectures (Multi-AZ/Multi-Region, Route 53, DR strategies — backup/restore, pilot light, warm standby, active-active, RPO/RTO, failover, RDS Proxy, X-Ray)

### Domain 3 — Design High-Performing Architectures (24%)
- [ ] Task 3.1: High-performing/scalable storage (S3, EFS, EBS, hybrid storage)
- [ ] Task 3.2: High-performing/elastic compute (EC2 Auto Scaling, Batch, EMR, Fargate, Lambda sizing, ECS/EKS)
- [ ] Task 3.3: High-performing databases (ElastiCache, read replicas, proxies, capacity planning, engine selection)
- [ ] Task 3.4: High-performing/scalable networking (CloudFront, Global Accelerator, subnet/routing design, load balancing, VPN/Direct Connect/PrivateLink)
- [ ] Task 3.5: High-performing data ingestion/transformation (Kinesis, Glue, Athena, Lake Formation, DataSync, Storage Gateway, EMR)

### Domain 4 — Design Cost-Optimized Architectures (20%)
- [ ] Task 4.1: Cost-optimized storage (S3 storage classes/lifecycle, EBS volume types, FSx, EFS, backup/archival, Requester Pays)
- [ ] Task 4.2: Cost-optimized compute (Spot/Reserved/Savings Plans, instance family/size selection, Outposts, hibernation, ALB vs NLB vs GWLB cost)
- [ ] Task 4.3: Cost-optimized databases (engine selection, capacity planning, retention/backup policy, DynamoDB vs RDS cost)
- [ ] Task 4.4: Cost-optimized networking (NAT gateway strategy, Direct Connect vs VPN vs internet, Transit Gateway/peering, throttling, CDN/edge caching)

### Topic Clusters (source coverage — the actual notes)
- [ ] 01-Foundations (Getting Started, IAM Basics)
- [ ] 02-Compute-EC2 (EC2 Basics, Associate, Instance Storage, HA & Scalability)
- [ ] 03-Storage (S3, S3 Advanced, S3 Security, Storage Extras)
- [ ] 04-Databases (RDS/Aurora/ElastiCache, Databases Overview, Data & Analytics)
- [ ] 05-Networking-Content-Delivery (Route 53, VPC, CloudFront/Global Accelerator)
- [ ] 06-Containers-Serverless (Containers, Serverless Overview, Serverless Architectures)
- [ ] 07-Integration-Messaging (SQS/SNS/Kinesis)
- [ ] 08-Security-Identity (Advanced Identity, Security & Encryption)
- [ ] 09-Monitoring-Management (CloudWatch/CloudTrail/Config)
- [ ] 10-Machine-Learning (ML Services)
- [ ] 11-Architecture-Patterns (Classic SA, More SA, DR & Migrations, Other Services, White Papers)
- [ ] 12-Exam-Prep (Exam Tips)

---

## Session Log

| Date | Duration | Topics Covered | Next Action |
|------|----------|----------------|-------------|
| 2026-07-21 | — | Migrated project from CLF-C02 (passed) to SAA-C03. Archived old vault to `_archive/clf-c02/`. Scaffolded new topic-cluster structure + 4 domain cross-reference MOCs from the official exam guide. Populated all cluster notes from the v48 slide deck (876 pages). Set an 8-week study schedule. | Start Week 1: `/teach getting-started` or `/teach iam` |
| 2026-07-28 | — | Merged 15 XMind mind maps (`AWS-Solutions-Architect-Associate/xmind/`) into the vault as a second source alongside the slide deck. Media Services and End User Computing skipped (low SAA-C03 relevance, per decision). Added many previously-missing services (AWS SMS, Migration Hub, Cognito, RAM, Network Firewall, Security Hub/Detective/Artifact/Audit Manager, Device Farm, API Gateway, Step Functions, EventBridge, CloudSearch, Data Pipeline, Data Exchange, Trusted Advisor, Compute Optimizer, Managed Grafana/Prometheus, Elastic Beanstalk, ECS/EKS Anywhere, Kinesis Video Streams/Data Analytics, Forecast, Fraud Detector, and more) and expanded dozens of thin sections. Found 14 factual conflicts between the two sources; researched each against current official AWS docs and resolved all of them in-note with citations (most conflicts turned out to be the mind map being a stale/outdated source — e.g. pre-2017 EC2 billing, pre-2024 Lambda Go runtime, pre-Aug-2025 SQS message size; one genuine correction: Aurora's max storage is version-dependent, not a flat number). Compute Optimizer (cost) and AppSync remain open gaps — not covered in any available source. | Continue Week 1: `/teach getting-started` or `/teach iam`. Vault content is now current as of 2026-07. |

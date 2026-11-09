# Progress Tracking — CLF-C02

## Domain Status

| Domain | Topic | Status | Last Studied | Notes |
|--------|-------|--------|--------------|-------|
| D1 | Cloud Concepts (24%) | 🟡 In Progress | 2026-07-01 | Covered: Global Infra (Region/AZ/Edge), pricing principles |
| D2 | Security & Compliance (30%) | 🔵 Not Started | — | |
| D3 | Cloud Technology & Services (34%) | 🔵 Not Started | — | |
| D4 | Billing, Pricing & Support (12%) | 🟡 In Progress | 2026-07-01 | Covered: pricing principles, On-Demand, Reserved, Savings Plans (partial) |

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

## Topics Covered Checklist

### Domain 1 — Cloud Concepts
- [ ] Cloud computing definition and 5 characteristics
- [ ] 6 advantages of cloud computing
- [ ] Deployment models (public, private, hybrid)
- [ ] Service models (IaaS, PaaS, SaaS) with examples
- [x] AWS Global Infrastructure (Regions, AZs, Edge Locations) — 2026-07-01
- [ ] How to choose a region
- [ ] Well-Architected Framework (6 pillars)
- [ ] AWS Cloud Adoption Framework (6 perspectives)
- [ ] Migration strategies (7 Rs) and migration services
- [ ] Economics of cloud (CAPEX vs OPEX, fixed vs variable costs)
- [ ] Rightsizing concept and tools (Compute Optimizer, Cost Explorer)
- [ ] SCT and Migration Evaluator (migration planning)
- [ ] AWS Partner Network (APN) ecosystem

### Domain 2 — Security & Compliance
- [ ] Shared Responsibility Model
- [ ] IAM: users, groups, policies, roles
- [ ] IAM: password policy, MFA, access keys
- [ ] AWS Shield (Standard & Advanced) and WAF
- [ ] AWS Firewall Manager
- [ ] VPC, subnets, security groups, NACLs
- [ ] VPC Peering, VPC Endpoints (Gateway + Interface/PrivateLink), VPN, Direct Connect
- [ ] KMS and CloudHSM
- [ ] GuardDuty, Inspector, Macie, Security Hub, Detective
- [ ] CloudTrail, AWS Config, AWS Audit Manager
- [ ] AWS Artifact and compliance frameworks
- [ ] IAM Identity Center (SSO) and Cognito
- [ ] AWS Resource Access Manager (RAM)
- [ ] AWS Directory Service

### Domain 3 — Cloud Technology & Services
- [ ] EC2 instance types and purchasing options
- [ ] EBS, EFS, AMI, EC2 Image Builder
- [ ] S3: buckets, storage classes, versioning, replication
- [ ] S3: security, lifecycle, transfer acceleration
- [ ] AWS Snow family and Storage Gateway
- [ ] AWS Backup and Elastic Disaster Recovery
- [ ] RDS, Aurora, ElastiCache
- [ ] DynamoDB (+ DAX + Global Tables), Redshift, Athena, Glue, DMS, SCT
- [ ] Amazon OpenSearch Service
- [ ] ELB (ALB, NLB, GWLB) and ASG
- [ ] Lambda, ECS, Fargate, ECR, EKS, API Gateway
- [ ] CloudFormation, CDK, Elastic Beanstalk
- [ ] Route 53, CloudFront, Global Accelerator
- [ ] AWS Transit Gateway and PrivateLink
- [ ] CloudWatch, CloudTrail, X-Ray, EventBridge
- [ ] AWS Compute Optimizer
- [ ] SQS, SNS, Kinesis, Step Functions
- [ ] Amazon Q (Q Business + Q Developer)
- [ ] AWS ML services (Rekognition, Transcribe, Polly, Translate, Lex, Comprehend, SageMaker, Kendra, Personalize, Textract, Forecast)
- [ ] End User Computing (WorkSpaces, AppStream 2.0, WorkSpaces Secure Browser)
- [ ] Frontend/Mobile (Amplify, AppSync)
- [ ] Business apps (SES, Connect)
- [ ] IoT (AWS IoT Core)
- [ ] AWS Service Catalog, License Manager

### Domain 4 — Billing, Pricing & Support (~8 questions)
- [x] EC2 pricing models (On-Demand, Reserved Standard/Convertible, Spot, Savings Plans, Dedicated Host/Instance, Capacity Reservations) — 2026-07-01 (partial: On-Demand ✅ Reserved ✅ Savings Plans ✅ — Spot/Dedicated/Capacity pending)
- [ ] S3 and other service pricing factors
- [ ] AWS Free Tier (always-free vs 12-month vs trial)
- [ ] Pricing Calculator and TCO Calculator
- [ ] Cost & Usage Reports (most comprehensive)
- [ ] Cost Explorer (historical + 12-month forecast)
- [ ] AWS Budgets (4 types: cost/usage/reservation/savings plans)
- [ ] CloudWatch Billing Alarms vs AWS Budgets (difference)
- [ ] Cost Anomaly Detection (ML-based)
- [ ] Cost Allocation Tags (aws: vs user: prefix)
- [ ] AWS Organizations and Consolidated Billing (volume discounts, pooled RIs)
- [ ] Support plans (Basic free / Developer $29+ / Business $100+ / Enterprise On-Ramp $5500+ / Enterprise $15000+)
- [ ] Support response times by plan
- [ ] Trusted Advisor (7 checks free vs 125+ Business+)
- [ ] AWS Marketplace and APN

---

## Session Log

| Date | Duration | Topics Covered | Next Action |
|------|----------|----------------|-------------|
| 2026-07-01 | ~3h | Full vault created from Maarek slides v44 (D1–D4, 9 D3 notes); domain weights corrected (D3=34%, D4=12%); missing services added (09-Additional-Services); fullexam/quiz updated for multiple-response questions | Start teaching from Domain 1 or run /readiness |
| 2026-07-01 | ~1h | Teaching session: Global Infra hierarchy (Region/AZ/Edge); D4 Pricing — principles, On-Demand, Reserved, Savings Plans | Continue pricing: Spot, Dedicated, Capacity, S3, Free Tier |

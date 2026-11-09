# AWS Certified Solutions Architect – Associate (SAA-C03)

> A free-first study guide and Codex-ready learning plan, assembled from the resources and recommendations discussed in this conversation (November 2026).
>
> **Important:** Verify current exam version, prices, course availability, and AWS features against official sources before booking. Community notes and practice questions can become outdated. Hands-on AWS labs can incur cloud charges.

## 1. Study goal and approach

**Goal:** Prepare for AWS Certified Solutions Architect – Associate (SAA-C03) using free resources first, hands-on architecture exercises, and scenario-based practice.

**Assumed background:** Experienced software engineer already familiar with AWS EKS, Lambda, SQS, CloudWatch, API Gateway, and distributed applications.

**Strategy:**

1. Use the **official AWS SAA-C03 exam guide** as the authoritative syllabus.
2. Follow **AWS Skill Builder** and the free **freeCodeCamp / Andrew Brown** video course for coverage.
3. Supplement with **Adrian Cantrill's SAA-C03 GitHub materials** and **AWS Well-Architected Labs**.
4. Concentrate on architecture trade-offs: networking, storage, databases, resilience, security, and cost.
5. Use legitimate practice exams to locate weak areas; review why each wrong option is wrong.
6. Book the exam only after consistently scoring **80–85% on fresh, reputable timed mock exams** (a study heuristic, not an AWS passing requirement).

## 2. Official resources

| Resource | Link | Why use it | Cost / caveat |
|---|---|---|---|
| AWS Certification catalog | https://aws.amazon.com/certification/ | Confirm current exam details and registration | Exam fee applies |
| SAA-C03 official exam guide | https://docs.aws.amazon.com/pdfs/aws-certification/latest/solutions-architect-associate-03/solutions-architect-associate-03.pdf | Primary syllabus, in-scope services, domain objectives | Free |
| AWS SAA-C03 Skill Builder exam prep | https://skillbuilder.aws/category/exam-prep/solutions-architect-associate-SAA-C03 | AWS-authored preparation content | Some free, some paid |
| AWS certification preparation | https://aws.amazon.com/certification/certification-prep/ | Official preparation options and practice materials | Free sampler; other offerings may cost |
| AWS Well-Architected Framework | https://docs.aws.amazon.com/wellarchitected/latest/framework/welcome.html | Six pillars and architecture decision principles | Free |
| AWS documentation | https://docs.aws.amazon.com/ | Validate up-to-date service behavior | Free |
| AWS Builder Center Sandbox information | https://aws.amazon.com/about-aws/whats-new/2026/07/aws-builder-center-sandbox/ | Check supported temporary hands-on environments | Availability and eligibility vary |

**Exam overview discussed:** SAA-C03; approximately 65 questions, 130 minutes, and $150 USD exam fee. Verify these details before scheduling.

### Exam domains (official SAA-C03 weighting)

- **Design Secure Architectures:** 30%
- **Design Resilient Architectures:** 26%
- **Design High-Performing Architectures:** 24%
- **Design Cost-Optimized Architectures:** 20%

## 3. Free courses and video learning

### freeCodeCamp / Andrew Brown — AWS Solutions Architect Associate

- Video: https://www.youtube.com/watch?v=c3Cn4xYfxJY
- Comprehensive long-form course (approximately 50 hours, as previously described).
- Covers VPC, IAM, EC2, Auto Scaling, S3, databases, networking, serverless, security, and additional exam topics.
- **Caution:** Published in 2024; cross-check details that AWS may have updated.

### AWS Skill Builder

- Learning plan: https://skillbuilder.aws/category/exam-prep/solutions-architect-associate-SAA-C03
- Use for targeted review of any missed domain objectives.
- Check which modules and assessments are free before enrolling.

## 4. Open-source / GitHub repositories

| Repository | Link | Use | Caveat |
|---|---|---|---|
| Adrian Cantril — SAA-C03 resources | https://github.com/acantril/aws-sa-associate-saac03 | Diagrams, supporting files, architectural study aids | Not the complete course for free |
| AWS Well-Architected Labs | https://github.com/awslabs/aws-well-architected-labs | Practical labs in security, reliability, operations, and costs | AWS usage may incur charges; check repo status |
| AWS Certifications Wiki | https://github.com/AWSCertifications/AWSCertificationsWiki | Community-curated notes, prep references, and links | Check update dates |
| apgosar/aws_exam_prep | https://github.com/apgosar/aws_exam_prep | Additional SAA notes, comparisons, and mock prep | Newer/smaller repository; independently validate |

**Recommended pairing:** Cantril resources for concepts and diagrams; AWS Well-Architected Labs for architecture practice; AWS official guide to decide what to study.

## 5. Free practice questions

| Source | Link | Previously identified free offer | Notes |
|---|---|---|---|
| AWS official practice | https://aws.amazon.com/certification/certification-prep/ | 20-question set | Highest-priority official calibration |
| Tutorials Dojo free sampler | https://portal.tutorialsdojo.com/courses/free-aws-certified-solutions-architect-associate-practice-exams-sampler/ | 30 questions | Review explanations and distractors |
| Training Camp practice test | https://trainingcamp.com/aws-solutions-architect-practice-test/ | 50 questions | Supplement only; check freshness |
| SAA Practice Dojo | https://app.boochi-engineer.net/service/aws-saa-siken?bsc_lang=en | Advertised 1,000 questions | Community questions: verify accuracy |

**Optional paid resource:** Tutorials Dojo full practice tests, if you need additional high-quality mock exams. Previously estimated at roughly $15–$25; verify live pricing.

**Avoid exam dumps or purported leaked real exam questions.** They may violate exam rules and are often inaccurate or outdated.

## 6. Topic priorities

| Topic | Priority | Essential distinctions |
|---|---|---|
| VPC / networking | Very high | Public/private subnets, route tables, IGW vs NAT, VPC endpoints, peering vs Transit Gateway, VPN vs Direct Connect, security groups vs NACLs |
| Storage | Very high | S3 classes and lifecycle, EBS vs EFS vs FSx, encryption, replication and access patterns |
| Databases | Very high | RDS Multi-AZ vs read replica, Aurora vs RDS, DynamoDB, backups, caching and scaling |
| Availability / DR | Very high | ALB vs NLB, Auto Scaling, Route 53 routing, multi-AZ vs multi-Region, RTO/RPO, failover choices |
| Security / governance | High | IAM policies, roles, KMS, AWS Organizations, SCPs, least privilege |
| Cost optimization | High | On-Demand vs Spot vs Reserved Instances vs Savings Plans, storage tiers, data transfer costs |
| Serverless / messaging | Medium (familiar territory) | Lambda, API Gateway, SQS vs SNS vs EventBridge, Step Functions, idempotency |
| Containers | Medium (familiar territory) | ECS vs EKS vs Fargate, trade-offs, networking and cost |

**Priority for an experienced AWS application engineer:** Pay disproportionate attention to networking, database trade-offs, storage options, hybrid architecture, cost, and disaster recovery—not general code implementation.

## 7. Six-week preparation plan

**Suggested schedule:** 1–1.5 hours per weekday and 2–3 hours per weekend day. Adapt based on diagnostic practice scores.

### Week 1 — Networking and security
- [ ] Read relevant official exam guide sections.
- [ ] Study VPC, subnets, route tables, IGW, NAT, endpoints, peering, Transit Gateway, Direct Connect.
- [ ] Review IAM, KMS, SGs vs NACLs, Organizations and SCPs.
- [ ] **Lab:** Design a VPC with public and private subnets; explain secure outbound connectivity and private AWS-service access.
- [ ] Record scenario-based architectural trade-offs.

### Week 2 — Compute, availability, and resilience
- [ ] Study EC2 purchase options, Auto Scaling, ALB vs NLB, Route 53, CloudFront.
- [ ] Learn backup, failover, RTO/RPO, multi-AZ and multi-Region decisions.
- [ ] **Lab:** Draw a resilient multi-AZ three-tier architecture with failover.
- [ ] Practice relevant exam questions.

### Week 3 — Storage and databases
- [ ] Compare S3 storage classes, lifecycle, replication, encryption.
- [ ] Compare EBS, EFS, and FSx workloads.
- [ ] Review RDS Multi-AZ, read replicas, Aurora, DynamoDB, ElastiCache.
- [ ] **Lab:** Choose and justify storage/database services for three different workloads.
- [ ] Practice relevant exam questions.

### Week 4 — Integration, serverless, and costs
- [ ] Review Lambda, API Gateway, SQS, SNS, EventBridge, Step Functions.
- [ ] Study data transfer billing, Reserved Instances, Spot, and Savings Plans.
- [ ] Review the Well-Architected cost and performance pillars.
- [ ] **Lab:** Design a cost-optimized, event-driven order-processing architecture.
- [ ] Take a domain-based quiz.

### Week 5 — Practice questions and gap analysis
- [ ] Complete the AWS official free practice set.
- [ ] Complete the Tutorials Dojo free sampler.
- [ ] Use any suitable supplementary practice resources.
- [ ] For **every incorrect or guessed answer**, record the concept, why the correct answer wins, and why the alternatives lose.
- [ ] Revisit weak topics using official documentation.

### Week 6 — Exam readiness
- [ ] Take fresh, timed, reputable full-length mocks if available.
- [ ] Target consistently **80–85%+** in unseen mocks (study target, not official passing threshold).
- [ ] Revisit wrong answers and repeated weak areas.
- [ ] Review AWS service-comparison notes, DR strategies and pricing trade-offs.
- [ ] Check current official exam requirements and schedule when ready.

## 8. Hands-on project ideas

1. **Public/private three-tier deployment:** VPC, ALB, Auto Scaling/EC2, private database and secure management.
2. **Serverless order workflow:** API Gateway, Lambda, SQS, SNS/EventBridge, DynamoDB and idempotent consumers.
3. **Highly available database architecture:** RDS/Aurora Multi-AZ, read scaling, backup and recovery planning.
4. **Hybrid connectivity design:** Compare site-to-site VPN and Direct Connect; sketch routing and resilience.
5. **Storage design challenge:** Pick S3/EBS/EFS/FSx and lifecycle strategies for different access patterns.
6. **Cost optimization exercise:** Explain the right EC2 purchase models, data transfer routes and managed-service trade-offs.

**Cost safety:** Check each lab's pricing before deployment, set AWS Budgets alerts, use sandbox/free-tier eligibility when available, and tear down all resources afterward. A budget alert does not automatically stop charges.

## 9. Codex instructions (use this file as study context)

When operating as my SAA-C03 study assistant:

1. Treat the **latest AWS official SAA-C03 exam guide** as the source of truth.
2. Begin with a diagnostic quiz of 15–20 original scenario-based multiple-choice questions, balanced across domains.
3. Ask **one question at a time**, allow me to answer before revealing the solution, and then explain each option.
4. Prefer real architectural scenarios over service-definition memorization.
5. Focus additional questions on weak domains; maintain a progress record in `study-progress.md`.
6. Make original practice questions: **do not reproduce proprietary exam questions or dumps**.
7. When providing Terraform or CloudFormation labs, include prerequisites, cost warnings, validation, and cleanup steps.
8. Explain architectural trade-offs through **security, resilience, performance and cost**.
9. When facts could change, consult up-to-date official AWS documentation; identify uncertainty if live browsing is unavailable.
10. Avoid giving only an answer key—provide the reasoning, including why incorrect options are less suitable.

### Suggested progress-file schema

Create `study-progress.md` containing:

- Start date and target exam date
- Completed weekly checklist items
- Questions attempted, correct and incorrect by exam domain
- Concepts missed and links to official explanations
- Completed labs and cleanup confirmation
- Practice exam date, source, score and weak topics
- Next three recommended study tasks

### Paste into Codex to begin

```text
Use aws-saa-c03-codex-study-guide.md as my study plan for AWS Certified
Solutions Architect – Associate (SAA-C03). Create study-progress.md with
checklists for the six weeks. Then administer a 20-question original
architecture-focused diagnostic test, one question at a time. Don't reveal
answers before I respond. After each response, explain the correct answer
and why each distractor is less suitable. Track domain-level scores and
adapt the study plan based on my weak areas. Prefer current official AWS
documentation and flag any service details that need verification.
```

## 10. Budget

- **Free-first preparation:** $0 course/repository budget, excluding any AWS lab usage.
- **SAA exam fee:** previously discussed as $150 USD; verify the current price.
- **Optional practice exams:** approximately $15–$25, subject to current pricing.
- **Estimated exam + optional practice questions:** approximately $165–$175, excluding lab usage, taxes and retakes.

## 11. Exam-readiness checklist

- [ ] I can explain the architectural differences between common competing AWS services.
- [ ] I can identify and justify the most secure option in a scenario.
- [ ] I can design a failure-tolerant multi-AZ architecture.
- [ ] I understand RTO, RPO, backups, replication and cross-Region recovery.
- [ ] I can identify cost-efficient solutions without compromising requirements.
- [ ] I score consistently 80–85%+ on fresh reputable mocks.
- [ ] I can explain why wrong options are wrong, not just remember answers.
- [ ] I have verified the current exam version and registration requirements.

---

**Maintainer note:** Update URLs, exam policies, and content as AWS evolves; this file is a study plan, not a replacement for AWS's official exam guide.

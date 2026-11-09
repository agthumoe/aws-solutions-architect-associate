# Gap Analysis

Analyze the vault coverage against the official SAA-C03 exam guide and report missing topics.

**Usage:** `/gap-analysis`

## Instructions

1. Scan all `.md` files in the vault (all topic-cluster folders + `00-Index/Exam-Domains/`)
2. Cross-reference against the SAA-C03 exam domain breakdown (official exam guide task statements):

   **Domain 1 (30%) — Design Secure Architectures:** Secure access to AWS resources (IAM, federation, SCPs, Control Tower), secure workloads/applications (VPC security, Shield, WAF, Secrets Manager, Cognito, GuardDuty, Macie), data security controls (KMS, ACM, encryption at rest/in transit)
   **Domain 2 (26%) — Design Resilient Architectures:** Scalable/loosely coupled architectures (API Gateway, SQS/SNS, caching, microservices, event-driven, containers, ELB, Step Functions), highly available/fault-tolerant architectures (Multi-AZ/Multi-Region, Route 53, DR strategies, RPO/RTO)
   **Domain 3 (24%) — Design High-Performing Architectures:** High-performing storage (S3/EFS/EBS), elastic compute (Auto Scaling, Fargate, Lambda, ECS/EKS), high-performing databases (ElastiCache, read replicas), scalable networking (CloudFront, Global Accelerator, load balancing), data ingestion/transformation (Kinesis, Glue, Athena)
   **Domain 4 (20%) — Design Cost-Optimized Architectures:** Cost-optimized storage (S3 tiers/lifecycle), cost-optimized compute (Spot/Reserved/Savings Plans), cost-optimized databases, cost-optimized networking (NAT strategy, Direct Connect vs VPN)

3. Report in the chat (do NOT write a file):
   - **Covered** — topics with notes
   - **Partial** — topics with thin coverage
   - **Missing** — topics not yet in the vault
   - **Priority list** — top 5 notes to create next, ordered by exam weight impact

4. Suggest specific filenames and folders for missing notes.

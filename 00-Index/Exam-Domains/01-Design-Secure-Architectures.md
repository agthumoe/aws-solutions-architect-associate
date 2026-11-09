---
tags:
  - aws
  - saa-c03
  - exam-domain
aliases:
  - "Domain 1"
  - "Secure Architectures"
status: not-started
date: 2026-07-21
---

# Domain 1: Design Secure Architectures (30%)

Highest-weighted domain on the exam. Source: official AWS SAA-C03 exam guide.

## Task 1.1: Design secure access to AWS resources

**Knowledge of:** Access controls and management across multiple accounts; AWS federated access and identity services (IAM, IAM Identity Center); AWS global infrastructure (AZs, Regions); AWS security best practices (least privilege); shared responsibility model.

**Skills in:** Applying IAM security best practices (MFA); designing a flexible authorization model (users, groups, roles, policies); designing a role-based access control strategy (STS, role switching, cross-account access); designing a security strategy for multiple accounts (Control Tower, SCPs); determining appropriate use of resource policies; determining when to federate a directory service with IAM roles.

**Covered by:** [[01-Foundations/02-IAM-Basics]] · [[08-Security-Identity/01-Advanced-Identity]]

## Task 1.2: Design secure workloads and applications

**Knowledge of:** Application configuration/credentials security; AWS service endpoints; controlling ports/protocols/network traffic; secure application access; security services (Cognito, GuardDuty, Macie); external threat vectors (DDoS, SQL injection).

**Skills in:** Designing VPC architectures with security components (security groups, route tables, NACLs, NAT gateways); network segmentation (public/private subnets); integrating AWS services to secure applications (Shield, WAF, IAM Identity Center, Secrets Manager); securing external connections (VPN, Direct Connect).

**Covered by:** [[05-Networking-Content-Delivery/02-VPC]] · [[08-Security-Identity/02-Security-Encryption]]

## Task 1.3: Determine appropriate data security controls

**Skills in:** Aligning AWS technologies to compliance requirements; encrypting data at rest (KMS); encrypting data in transit (ACM/TLS); implementing access policies for encryption keys; implementing data backups/replications; implementing policies for data access/lifecycle/protection; rotating encryption keys and renewing certificates.

**Covered by:** [[03-Storage/03-S3-Security]] · [[08-Security-Identity/02-Security-Encryption]]

## Related
- [[00-Index/Home]]

## Current verification path

See [[00-Index/Exam-Scope]] for the 2026-11-09 task/reference audit and [official domain details](https://docs.aws.amazon.com/aws-certification/latest/solutions-architect-associate-03/solutions-architect-associate-03-domain1.html). This page is a course-derived summary; note presence is not learner mastery.

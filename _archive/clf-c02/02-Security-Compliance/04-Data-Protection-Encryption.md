---
tags:
  - aws
  - cloud-practitioner
  - security
  - encryption
  - kms
domain: Security and Compliance
aliases:
  - "KMS"
  - "CloudHSM"
  - "GuardDuty"
  - "Inspector"
  - "Macie"
  - "Encryption"
  - "Secrets Manager"
status: not-started
date: 2026-07-01
---

# Data Protection & Encryption

## Encryption Concepts

- **Encryption at rest** — data is encrypted when stored (AES-256 common standard)
- **Encryption in transit** — data is encrypted when moving between systems (SSL/TLS)

Both are the customer's responsibility for configuring on their data.

---

## AWS Key Management Service (KMS)

- **Managed service** for creating and controlling encryption keys
- AWS manages the keys on behalf of the customer
- Integrated with most AWS services (S3, EBS, RDS, etc.)
- Keys never leave AWS KMS unencrypted

---

## AWS CloudHSM (Hardware Security Module)

- **Dedicated hardware** for key storage and cryptographic operations
- Customer manages their own keys (AWS does NOT have access)
- FIPS 140-2 Level 3 compliant
- Use when regulations require customer-managed keys on dedicated hardware

| Feature | AWS KMS | AWS CloudHSM |
|---|---|---|
| Key management | AWS manages | Customer manages |
| Hardware | Shared | Dedicated |
| Access | AWS can access metadata | AWS has NO access to keys |
| Compliance | General purpose | Strict regulatory requirements |

---

## AWS Certificate Manager (ACM)

- Provision, manage, and deploy **SSL/TLS certificates**
- Public certificates are **free**
- Integrates with: ELB, CloudFront, API Gateway
- Handles certificate renewal automatically

---

## AWS Secrets Manager

- Securely store and manage **secrets** (database passwords, API keys)
- Supports **automatic rotation** of secrets (e.g., RDS password rotation)
- Integrates with RDS, Redshift, DocumentDB
- Encrypted using KMS

---

## Amazon GuardDuty

- **Intelligent threat detection** service using machine learning
- Continuously monitors for malicious activity
- Analyzes: CloudTrail logs, VPC Flow Logs, DNS logs
- **No agent needed** — works out of the box
- Findings include: cryptocurrency mining, credential compromise, unauthorized access
- Can trigger EventBridge events → Lambda → SNS

---

## Amazon Inspector

- **Automated security assessments** for:
  - EC2 instances (OS vulnerabilities, network reachability)
  - Container images in ECR
  - Lambda functions
- Reports findings to **AWS Security Hub**
- Risk score for prioritization

---

## Amazon Macie

- Uses **ML to discover and protect sensitive data** stored in S3
- Identifies **Personally Identifiable Information (PII)**
- Alerts when PII is detected in S3 buckets
- Helps with data privacy regulations (GDPR, HIPAA)

---

## AWS Security Hub

- **Central security dashboard** across AWS accounts and services
- Automates security checks
- Aggregates findings from GuardDuty, Inspector, Macie, Config, etc.
- Provides compliance dashboards

---

## Amazon Detective

- **Investigate security issues** after the fact
- Uses ML to analyze CloudTrail, VPC Flow Logs, GuardDuty findings
- Builds a graph of relationships between resources
- Helps answer "what happened?" after a security incident

---

## Penetration Testing on AWS

**8 services you can pen-test without prior AWS approval:**
1. Amazon EC2 instances, NAT Gateways, Elastic Load Balancers
2. Amazon RDS
3. Amazon CloudFront
4. Amazon Aurora
5. Amazon API Gateway
6. AWS Lambda and Lambda Edge
7. Amazon Lightsail
8. Amazon Elastic Beanstalk environments

**Prohibited** (regardless of approval): DDoS simulation, DNS zone walking, port/protocol/request flooding

---

## Exam Tips

> [!tip]
> - KMS = AWS manages keys; CloudHSM = YOU manage keys on dedicated hardware
> - GuardDuty = threat detection (no agent; uses logs)
> - Inspector = security assessment of EC2/containers/Lambda
> - Macie = sensitive data (PII) discovery in S3
> - ACM = free SSL/TLS certs for ALB, CloudFront, API Gateway
> - Secrets Manager = store + rotate secrets (especially DB passwords)

> [!warning]
> GuardDuty ≠ Inspector. GuardDuty detects THREATS to your AWS account. Inspector checks for VULNERABILITIES in your resources.

## Related Notes
- [[01-IAM]]
- [[02-Shared-Responsibility-Model]]
- [[05-Compliance-Governance]]

---
tags:
  - aws
  - cloud-practitioner
  - security
  - moc
domain: Security and Compliance
aliases:
  - "Security MOC"
  - "Domain 2"
  - "D2"
status: not-started
date: 2026-07-01
---

# Domain 2: Security & Compliance — Map of Content

**Exam Weight: 30%** (~19 questions) — **Highest weight domain**

---

## Notes in This Domain

1. [[01-IAM]] — Users, groups, policies, roles, MFA, access keys, CLI, SDK, best practices
2. [[02-Shared-Responsibility-Model]] — AWS vs customer responsibilities; examples for EC2, RDS, S3
3. [[03-Network-Security]] — VPC, subnets, Security Groups, NACLs, VPC Peering, Endpoints, VPN, Direct Connect, Shield, WAF
4. [[04-Data-Protection-Encryption]] — KMS, CloudHSM, ACM, Secrets Manager, GuardDuty, Inspector, Macie, Security Hub, Detective
5. [[05-Compliance-Governance]] — AWS Artifact, Config, CloudTrail, Organizations, SCPs, Control Tower, Trusted Advisor, IAM Identity Center, Cognito

---

## Key Exam Themes

- **Shared Responsibility Model** — understand exactly what AWS manages vs the customer
- **IAM** — least privilege, MFA, roles for services, access keys for CLI
- **Security Groups vs NACLs** — stateful vs stateless; instance vs subnet
- **KMS vs CloudHSM** — AWS manages vs customer manages keys
- **GuardDuty vs Inspector vs Macie** — threat detection vs vulnerability assessment vs PII discovery
- **CloudTrail vs Config** — who did what (API calls) vs what changed (configuration history)
- **Organizations** — consolidated billing, SCPs
- **Shield vs WAF** — DDoS (L3/L4) vs web exploits (L7)

---

## Quick Reference

| Service | Purpose |
|---|---|
| IAM | Manage AWS account access |
| MFA | Additional login security |
| AWS Shield Standard | Free DDoS protection (Layer 3/4) |
| AWS Shield Advanced | Premium DDoS ($3,000/month) |
| AWS WAF | Web app firewall (Layer 7; SQL injection, XSS) |
| AWS KMS | AWS manages encryption keys |
| AWS CloudHSM | Customer manages keys on dedicated hardware |
| ACM | Free SSL/TLS certificates |
| Secrets Manager | Store & rotate secrets (DB passwords) |
| GuardDuty | Threat detection (ML; no agent) |
| Inspector | Vulnerability assessment (EC2/containers/Lambda) |
| Macie | PII discovery in S3 |
| CloudTrail | API call history (who did what) |
| AWS Config | Configuration change history (what changed) |
| AWS Artifact | Compliance reports (SOC, PCI, ISO) |
| AWS Organizations | Multi-account management; consolidated billing |
| SCPs | Restrict actions in member accounts |
| Control Tower | Automated multi-account governance |
| IAM Identity Center | SSO across all accounts |
| Cognito | User management for your apps |
| VPC | Isolated network in AWS |
| Security Group | EC2-level firewall (stateful; allow only) |
| NACL | Subnet-level firewall (stateless; allow + deny) |
| VPC Endpoint | Private access to AWS services |
| Direct Connect | Private dedicated line to AWS |

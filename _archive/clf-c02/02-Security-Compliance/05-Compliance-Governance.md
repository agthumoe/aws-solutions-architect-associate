---
tags:
  - aws
  - cloud-practitioner
  - security
  - compliance
  - governance
domain: Security and Compliance
aliases:
  - "CloudTrail"
  - "AWS Config"
  - "Organizations"
  - "SSO"
  - "Cognito"
  - "Control Tower"
  - "Governance"
status: not-started
date: 2026-07-01
---

# Compliance & Governance

## AWS Artifact

- **On-demand access** to AWS compliance reports and agreements
- Examples: SOC reports, PCI DSS, ISO certifications
- Free self-service portal
- Use to demonstrate AWS compliance to auditors

> [!tip]
> "Where can a company access AWS ISO certifications and SOC reports?" → **AWS Artifact**

---

## AWS Config

- **Audit and record the configuration** of your AWS resources over time
- Answers: "Has anything changed?", "Is this compliant?"
- Can set **Config Rules** — e.g., "EBS volumes must be encrypted"
- Sends notifications to **SNS** when non-compliant
- Historical view of resource configurations
- Region-specific (but can aggregate across regions/accounts)
- **Does NOT prevent** non-compliant changes — only records and alerts

---

## AWS CloudTrail

- **Records all API calls** made in your AWS account
- Tracks: who made a call, from where, what was changed
- Default: 90-day history in CloudTrail console
- Can export to S3 or CloudWatch for longer retention
- Use cases: governance, compliance, operational auditing

### CloudTrail Insights
- Detects **unusual activity** in your account (e.g., sudden spike in API calls)

> [!tip]
> "How do I know who deleted an S3 bucket?" → CloudTrail
> "How do I check if security groups were changed?" → CloudTrail + Config

---

## AWS Organizations

- **Global service** to manage **multiple AWS accounts**
- One management account (formerly master) + member accounts
- Organized into **Organizational Units (OUs)**

### Benefits
- **Consolidated billing** — one payment method, combined usage for volume discounts
- **Pooled EC2 Reserved Instances** — unused RIs shared across accounts
- **Isolation** — separate accounts for dev/prod/audit
- **Service Control Policies (SCPs)** — restrict what member accounts can do

### Service Control Policies (SCPs)
- Restrict actions at **OU or account level**
- Apply to **all users and roles** in affected accounts (including account's own admins)
- **Do NOT apply to the management account**
- Cannot grant permissions — only restrict

---

## AWS Control Tower

- Easy way to **set up and govern a multi-account AWS environment**
- Sits on top of AWS Organizations
- Automates setup of landing zone (best practice multi-account environment)
- **Guardrails**:
  - **Preventive guardrails** — use SCPs to prevent non-compliant actions
  - **Detective guardrails** — use AWS Config to detect non-compliant resources

---

## AWS Trusted Advisor

- **Real-time recommendations** across 5 pillars:
  1. Cost Optimization
  2. Performance
  3. Security
  4. Fault Tolerance
  5. Service Limits

| Support Plan | Trusted Advisor Access |
|---|---|
| Basic / Developer | 7 core security checks only |
| Business / Enterprise On-Ramp / Enterprise | Full checks (125+) + API access |

> [!tip]
> "Which service gives recommendations to reduce costs and improve security?" → **Trusted Advisor**

---

## IAM Identity Center (SSO)

- Formerly AWS Single Sign-On (SSO)
- **One login for all AWS accounts** in an Organization
- Supports SAML 2.0 and identity federation
- Can use built-in identity store or connect to **Active Directory**, Okta, etc.
- Free to use

---

## Amazon Cognito

- **User identity management for web and mobile apps**
- Not for AWS account access — for **your application's users**
- Supports millions of users
- Social identity federation (Google, Facebook, Apple, enterprise IdPs via SAML 2.0 / OAuth 2.0)
- Handles sign-up, sign-in, access control

### Cognito: User Pools vs Identity Pools

| | **User Pools** | **Identity Pools** |
|---|---|---|
| Purpose | Authentication — sign-up, sign-in, user directory | Authorization — grant temporary AWS credentials to users |
| What it returns | JWT tokens | AWS IAM temporary credentials (via STS) |
| Use case | "Log in with username/password or Google" | "Let authenticated users access S3 / DynamoDB directly" |
| AWS access | ✗ (not for AWS) | ✓ (gives users scoped AWS access) |

> [!tip]
> User Pools = who you are (authentication). Identity Pools = what AWS resources you can access (authorization via temporary STS credentials).

---

## AWS Directory Services

| Service | Description |
|---|---|
| **AWS Managed Microsoft AD** | Full AD domain in cloud; MFA support; trust with on-premises AD |
| **AD Connector** | Proxy to redirect to existing on-premises AD |
| **Simple AD** | Standalone AD-compatible; no on-premises connection needed |

---

## Root User Privileges

Some actions require the **root user** (cannot be delegated to IAM users):
- Change AWS account settings (account name, email, root password)
- Change AWS Support plan
- Close the AWS account
- Change billing currency
- Restore IAM user permissions

> [!warning]
> Never use root for day-to-day operations. Enable MFA on root immediately after account creation.

---

## IAM Access Analyzer

- Identifies resources in your account shared with **external entities**
- Generates findings for S3 buckets, IAM roles, KMS keys, Lambda functions, SQS queues shared outside the account/organization

---

## Exam Tips

> [!tip]
> - AWS Artifact = compliance reports (SOC, PCI, ISO)
> - CloudTrail = WHO did WHAT and WHEN (API call history)
> - Config = WHAT changed in my resource configuration over time
> - Organizations = manage multiple accounts; consolidated billing; SCPs
> - Control Tower = automated multi-account setup with guardrails
> - IAM Identity Center = SSO for all accounts in an organization
> - Cognito = user management for YOUR apps (not AWS account access)

## Related Notes
- [[01-IAM]]
- [[02-Shared-Responsibility-Model]]
- [[04-Data-Protection-Encryption]]

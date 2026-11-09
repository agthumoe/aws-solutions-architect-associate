---
tags:
  - aws
  - cloud-practitioner
  - security
  - iam
domain: Security and Compliance
aliases:
  - "IAM"
  - "Identity Access Management"
  - "Users Groups Roles"
  - "Policies"
status: not-started
date: 2026-07-01
---

# IAM — Identity and Access Management

## What is IAM?

IAM = Identity and Access Management — a **global service** (not region-specific).

Used to manage who can access AWS and what they can do.

---

## Core Components

### Users
- Represent **people** within your organization
- Have a **password** for the AWS Console
- Each physical person should have exactly **one AWS user**
- Root account = created by default; **never use or share the root account**

### Groups
- Contain users only (groups **cannot** contain other groups)
- Users can belong to **multiple groups** or **no group**
- Assign permissions at the group level

### Policies
- JSON documents that define permissions
- Applied to users, groups, or roles
- Follow the **principle of least privilege**: give only what's needed

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Action": "ec2:Describe*",
      "Resource": "*"
    }
  ]
}
```

#### Policy Structure
| Field | Description |
|---|---|
| Version | Always `"2012-10-17"` |
| Id | Optional identifier |
| Statement | One or more statements (required) |
| Sid | Optional statement identifier |
| Effect | `Allow` or `Deny` |
| Principal | Account/user/role the policy applies to |
| Action | List of allowed/denied actions |
| Resource | Resources the actions apply to |
| Condition | Optional conditions (e.g., IP range, time, MFA) |

#### Policy Types
| Type | Description |
|---|---|
| **AWS Managed Policy** | Pre-built by AWS for common use cases (e.g., `AmazonS3ReadOnlyAccess`) |
| **Customer Managed Policy** | Custom policies you create and manage; reusable |
| **Inline Policy** | Policy directly embedded in a single user/group/role; not reusable |
| **Identity-based Policy** | Attached to IAM identities (users, groups, roles) — controls what the identity can do |
| **Resource-based Policy** | Attached directly to a resource (S3 bucket, SQS queue, SNS topic) — controls who can access it |

> [!tip]
> Two ways to allow EC2 to access S3: (1) give EC2 an IAM **role** (identity-based) or (2) write a **bucket policy** on S3 (resource-based).

### Roles
- Assigned to **AWS services** (not humans) to perform actions on your behalf
- Common roles: EC2 Instance Role, Lambda Function Role, CloudFormation Role
- Roles use **temporary credentials** — no access keys stored

#### AWS STS (Security Token Service)
- The underlying mechanism that issues **temporary security credentials** when a role is assumed
- Temporary credentials = access key ID + secret access key + **session token** + expiration
- AWS services automatically call `AssumeRole` → STS returns tokens → tokens are auto-rotated
- Duration: minimum 15 minutes; most cases 12 hours

| | IAM User | IAM Role |
|---|---|---|
| Assigned to | A person | A service or federated user |
| Credentials | Permanent (access keys) | Temporary via STS |
| Best for | Individual access | Services, cross-account, federation |

---

## Security Mechanisms

### Password Policy
Set requirements: minimum length, uppercase, lowercase, numbers, special characters, expiration, prevent reuse.

### Multi-Factor Authentication (MFA)
- MFA = something you know (password) + something you own (device)
- **If password is compromised, account is still protected**

#### MFA Device Options
| Type | Example |
|---|---|
| Virtual MFA | Google Authenticator, Authy (phone) |
| Universal 2nd Factor (U2F) | YubiKey (supports multiple users on single key) |
| Hardware Key Fob | Gemalto (3rd party) |
| Hardware Key Fob (GovCloud) | SurePassID (3rd party) |

---

## How to Access AWS

| Method | Protected By |
|---|---|
| AWS Management Console | Password + MFA |
| AWS CLI | Access Keys |
| AWS SDK | Access Keys |

### Access Keys
- Generated through the AWS Console
- Each user manages their own access keys
- **Never share access keys** — treat like a password
- Access Key ID ≈ username; Secret Access Key ≈ password

### AWS CLI
- Open-source tool for interacting with AWS via command line
- Built on AWS SDK for Python
- Direct access to public APIs of AWS services

### AWS SDK
- Language-specific libraries (JavaScript, Python, PHP, .NET, Ruby, Java, Go, Node.js, C++)
- Embedded within your application

---

## IAM Security Tools

| Tool | Scope | Purpose |
|---|---|---|
| **IAM Credentials Report** | Account-level | Lists all users and status of their credentials |
| **IAM Access Advisor** | User-level | Shows service permissions and last access time; helps revise policies |

---

## IAM Best Practices

- Don't use the root account except for AWS account setup
- One physical user = one AWS user
- Assign users to groups; assign permissions to groups
- Create a strong password policy
- Use and enforce MFA
- Create and use Roles for AWS services
- Use Access Keys for programmatic access (CLI/SDK)
- Audit with IAM Credentials Report & IAM Access Advisor
- **Never share IAM users or access keys**

---

## Shared Responsibility for IAM

| AWS Responsibility | Customer Responsibility |
|---|---|
| Global network security infrastructure | Users, groups, roles, policies management |
| Configuration and vulnerability analysis | Enable MFA on all accounts |
| Compliance validation | Rotate all keys often |
| | Use IAM tools to apply appropriate permissions |
| | Analyze access patterns; review permissions |

---

## Exam Tips

> [!tip]
> - Root account = most powerful; must be protected with MFA; **never** used day-to-day
> - Groups contain **only users**, not other groups
> - Roles are for **services** (not humans); EC2 instance needs a role to access S3
> - **Least privilege principle** — always give minimum permissions required
> - IAM is **global** — users/groups/roles are not region-specific

> [!warning]
> - A user can belong to multiple groups (no limit)
> - A user does NOT need to belong to a group
> - Policies attached directly to a user = **inline policies**

## Related Notes
- [[02-Shared-Responsibility-Model]]
- [[03-Network-Security]]
- [[05-Compliance-Governance]]

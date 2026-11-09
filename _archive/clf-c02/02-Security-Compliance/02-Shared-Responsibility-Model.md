---
tags:
  - aws
  - cloud-practitioner
  - security
  - shared-responsibility
domain: Security and Compliance
aliases:
  - "Shared Responsibility"
  - "AWS vs Customer"
status: not-started
date: 2026-07-01
---

# Shared Responsibility Model

## Core Principle

- **AWS** = Responsibility for the **security OF the cloud** (the infrastructure)
- **Customer** = Responsibility for the **security IN the cloud** (what you put in it)

---

## What AWS Is Responsible For

- Physical infrastructure (hardware, software, facilities, networking)
- Global network security
- Hypervisor and virtualization layer
- Managed services (S3, DynamoDB, RDS underlying hardware/software)
- Configuration and vulnerability analysis of infrastructure
- Compliance validation for infrastructure

---

## What the Customer Is Responsible For

- **EC2**: Guest OS (patches and updates), firewall & network configuration, IAM
- **Applications**: encrypting application data
- **Databases (self-managed)**: port/IP/SG rules, user creation, encryption settings
- **S3**: bucket configuration, bucket policy, public access settings, IAM users/roles, enabling encryption
- All data placed in AWS services

---

## Shared Controls

Both AWS and the customer share responsibility for:
- **Patch Management** (AWS patches infrastructure; customer patches guest OS/apps)
- **Configuration Management** (AWS configures its infrastructure; customer configures their apps)
- **Awareness & Training** (AWS trains its employees; customer trains theirs)

---

## Examples by Service

### For EC2
| AWS | Customer |
|---|---|
| Physical host, hypervisor, network | Guest OS patches and updates |
| Hardware replacement | Software installed on the instance |
| | Security groups and firewall rules |
| | IAM roles assigned to EC2 |
| | Data security on the instance |

### For RDS
| AWS | Customer |
|---|---|
| Underlying EC2, disks, networking | Port/IP/SG inbound rules |
| SSH access (disabled — customers can't SSH) | In-database user creation and permissions |
| Automated DB and OS patching | Public access setting |
| Underlying instance auditing | SSL configuration |
| | Database encryption setting |

### For S3
| AWS | Customer |
|---|---|
| Unlimited storage guarantee | Bucket configuration |
| Encryption infrastructure | Bucket policy / public access setting |
| Data separation between customers | IAM users and roles |
| Employees cannot access your data | Enabling encryption |

---

## Acceptable Use Policy (AUP)

https://aws.amazon.com/aup/

Prohibited:
- Illegal, Harmful, or Offensive Use or Content
- Security Violations
- Network Abuse
- E-Mail or Other Message Abuse

---

## Exam Tips

> [!tip]
> - "AWS is responsible for the security OF the cloud" = hardware, facilities, infrastructure
> - "Customer is responsible for security IN the cloud" = data, OS, apps, IAM
> - For managed services (S3, DynamoDB): customer responsible for **data and access config**, AWS handles everything else
> - For IaaS (EC2): customer responsible for **OS patches, apps, security groups, IAM**

> [!warning]
> Common trick: "Who is responsible for patching the RDS operating system?" → **AWS** (managed service). "Who is responsible for patching the OS on an EC2 instance?" → **Customer**.

## Related Notes
- [[01-IAM]]
- [[03-Network-Security]]

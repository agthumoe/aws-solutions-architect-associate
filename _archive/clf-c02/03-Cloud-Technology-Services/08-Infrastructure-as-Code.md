---
tags:
  - aws
  - cloud-practitioner
  - technology
  - cloudformation
  - iac
  - devops
domain: Cloud Technology and Services
aliases:
  - "CloudFormation"
  - "CDK"
  - "Elastic Beanstalk"
  - "IaC"
  - "CodePipeline"
  - "CI/CD"
status: not-started
date: 2026-07-01
---

# Infrastructure as Code & Developer Tools

## AWS CloudFormation

- **Infrastructure as Code (IaC)** — define AWS resources using YAML or JSON templates
- Declarative: describe WHAT you want; CloudFormation figures out HOW
- Creates a **stack** of resources from a template
- Resources within a stack are tagged automatically (cost visibility)
- Supports **almost every AWS resource** (and custom resources via Lambda)

### Benefits
- No manual resource creation — infrastructure is code
- Resources are created in the **right order** automatically
- Changes can be reviewed in code (version controlled)
- Destroy and recreate stacks easily (dev/staging/prod)

### Key CloudFormation Concepts
| Concept | Description |
|---|---|
| **Template** | YAML or JSON file describing the desired resources and their properties |
| **Stack** | A collection of AWS resources managed as a single unit via a template |
| **Change Set** | A preview of how proposed changes to a stack will impact running resources — review before applying |
| **StackSets** | Deploy stacks across multiple accounts and regions in one operation |

> [!tip]
> Change Sets = "preview before you apply" for CloudFormation. Safe way to review infra changes before they go live.

---

## AWS Cloud Development Kit (CDK)

- Define cloud infrastructure using **familiar programming languages**:  Python, TypeScript, Java, .NET
- Code is **compiled to CloudFormation** templates
- Allows reuse of infrastructure patterns via software constructs
- Write tests for your infrastructure

---

## AWS Elastic Beanstalk

- **Platform as a Service (PaaS)** — deploy applications without managing infrastructure
- You provide your code; Beanstalk handles: EC2, ASG, ELB, RDS configuration
- Free service — you pay only for underlying resources
- Supports: Java, Python, PHP, Ruby, Go, Docker, Node.js, .NET

### Beanstalk Environments
| Environment | Use |
|---|---|
| **Web Server Tier** | HTTP web application |
| **Worker Tier** | Background processing (SQS-backed) |

| Deployment | Use |
|---|---|
| Single instance | Development |
| High availability (with ALB) | Production |

---

## AWS CodePipeline (CI/CD)

- **Continuous Integration / Continuous Delivery** orchestration
- Automates: Source → Build → Test → Deploy
- Fully managed; free to use

### CI/CD Services

| Service | Role | Notes |
|---|---|---|
| **CodeCommit** | Source control (Git) | Being retired; use GitHub instead |
| **CodeBuild** | Build and test | Serverless; pay per build minute |
| **CodeDeploy** | Deploy to EC2/on-premises | Rolling upgrades; hybrid |
| **CodePipeline** | Orchestrate the pipeline | Connects all stages |
| **CodeArtifact** | Package/artifact management | npm, Maven, pip, etc. |

---

## AWS Systems Manager (SSM) — Infrastructure Management

- Manage EC2 and **on-premises** servers at scale (**hybrid**)
- **Patch Manager**: automate OS patches across fleet
- **Session Manager**: secure shell without SSH (no port 22)
- **Parameter Store**: store configuration data and secrets
- Works on: Amazon Linux, Ubuntu, Windows, on-premises Linux/Windows
- **Free to use**

---

## AWS OpsWorks

- Managed **Chef and Puppet** on AWS
- For organizations that already use Chef/Puppet for configuration management
- Alternative to SSM for existing Chef/Puppet users

---

## Deployment Summary

| Service | Category | Key Characteristic |
|---|---|---|
| CloudFormation | IaC | YAML/JSON templates; any resource |
| CDK | IaC | Programming languages → CloudFormation |
| Elastic Beanstalk | PaaS | Upload code; AWS manages the rest |
| CodePipeline | CI/CD | Source→Build→Test→Deploy orchestration |
| CodeBuild | CI | Serverless build and test |
| CodeDeploy | CD | Deploy to EC2/on-premises |
| Systems Manager | Management | Patch + run commands across fleet |
| OpsWorks | Config management | Chef/Puppet |

---

## Exam Tips

> [!tip]
> - CloudFormation = IaC; YAML/JSON; all AWS resources; version controlled
> - CDK = programming languages compile to CloudFormation
> - Elastic Beanstalk = PaaS; upload code; free (pay for underlying)
> - CodePipeline = full CI/CD pipeline orchestration
> - SSM = manage EC2 + on-premises; no SSH needed; free
> - "A company wants to deploy the same infrastructure in dev and prod automatically" → CloudFormation

> [!warning]
> Beanstalk is PaaS (like Heroku). CloudFormation is IaC. Beanstalk uses CloudFormation under the hood but abstracts it away.

## Related Notes
- [[01-EC2-Compute]]
- [[05-Serverless-Containers]]
- [[06-Monitoring-Management]]

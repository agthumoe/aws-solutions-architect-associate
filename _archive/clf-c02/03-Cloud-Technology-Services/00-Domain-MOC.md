---
tags:
  - aws
  - cloud-practitioner
  - technology
  - moc
domain: Cloud Technology and Services
aliases:
  - "Technology MOC"
  - "Domain 3"
  - "D3"
status: not-started
date: 2026-07-01
---

# Domain 3: Cloud Technology & Services — Map of Content

**Exam Weight: 34%** (~22 questions) — **Largest domain**

---

## Notes in This Domain

1. [[01-EC2-Compute]] — EC2 instance types, purchasing options, security groups, AMI, ELB, ASG
2. [[02-Storage-S3-EBS-EFS]] — EBS, EFS, Instance Store, FSx, S3 (buckets, storage classes, replication, encryption), Snow family, Storage Gateway
3. [[03-Databases]] — RDS, Aurora, DynamoDB (+ DAX), ElastiCache, Redshift, Athena, QuickSight, DocumentDB, Neptune, QLDB, Glue, DMS
4. [[04-Networking]] — Route 53, CloudFront, Global Accelerator, Outposts, WaveLength, Local Zones
5. [[05-Serverless-Containers]] — Lambda, ECS, Fargate, ECR, EKS, API Gateway, Batch, Lightsail
6. [[06-Monitoring-Management]] — CloudWatch, CloudTrail, X-Ray, EventBridge, CodeGuru, AWS Health Dashboard, SSM, Trusted Advisor
7. [[07-Application-Integration]] — SQS, SNS, Kinesis, Amazon MQ, Step Functions, ML Services overview
8. [[08-Infrastructure-as-Code]] — CloudFormation, CDK, Elastic Beanstalk, CodePipeline, CodeBuild, CodeDeploy, SSM
9. [[09-Additional-Services]] — Amazon Q, AppStream 2.0, WorkSpaces, Amplify, AppSync, SES, Connect, IoT Core, OpenSearch, Transit Gateway, PrivateLink, AWS Backup, Elastic Disaster Recovery, Compute Optimizer, Firewall Manager, RAM, SCT, Migration Evaluator

---

## Service Quick Reference

### Compute
| Service | Type | Key Fact |
|---|---|---|
| EC2 | Virtual machines | IaaS; many instance types; purchasing options |
| Lambda | Serverless functions | Max 15 min; event-driven; pay per call+duration |
| ECS | Containers | You manage EC2; Docker |
| Fargate | Serverless containers | AWS manages infrastructure |
| EKS | Kubernetes | Managed K8s |
| Batch | Batch processing | No time limit; uses EC2/Spot |
| Lightsail | Simple apps | Beginner-friendly; low cost |
| Elastic Beanstalk | PaaS | Upload code; AWS manages rest |

### Storage
| Service | Type | Key Fact |
|---|---|---|
| S3 | Object storage | Unlimited; globally unique bucket names |
| EBS | Block storage | One EC2; one AZ; network drive |
| EFS | File system | 100s of EC2; multi-AZ; Linux only |
| Instance Store | Physical disk | Ephemeral; highest IOPS |
| FSx | 3rd-party FS | Windows File Server or Lustre |
| Snow family | Physical devices | Offline data migration |

### Databases
| Service | Type | Use Case |
|---|---|---|
| RDS | Relational SQL | General purpose managed DB |
| Aurora | Relational SQL | Fastest; 5× MySQL; auto-grows |
| DynamoDB | NoSQL | Serverless; millisecond latency |
| ElastiCache | In-memory | Redis/Memcached; reduce DB load |
| Redshift | Data warehouse | OLAP; analytics; BI |
| Athena | Serverless SQL | Query S3 data; pay per query |

### Integration
| Service | Purpose |
|---|---|
| SQS | Queue; decouple; 1 consumer per message |
| SNS | Pub/sub; broadcast to many subscribers |
| EventBridge | Event bus; cron + event patterns |
| Step Functions | Visual workflows; orchestrate Lambda |
| Kinesis | Real-time streaming data |
| Amazon MQ | ActiveMQ/RabbitMQ (migration) |

---
tags: [aws, saa-c03, comparisons, recall]
status: reference
reviewed_on: 2026-11-09
---
# Architecture decisions — explain the closest alternative

Use this after trying recall without notes. This sheet consolidates checked distinctions; it is not a record of learning. Ask one prompt at a time during practice and save actual outcomes in [[memory/progress_tracking]].

| Requirement | Likely fit / distinction | Why the closest alternative can lose |
|---|---|---|
| Relational HA within one Region, single standby not serving reads | RDS Multi-AZ **DB instance** deployment | Ordinary read replicas primarily scale reads and normally require explicit promotion |
| RDS HA plus two readable standbys across three AZs | RDS Multi-AZ **DB cluster**, where supported | Do not apply the instance-deployment no-readable-standby rule to the cluster |
| Aurora shared storage and replica failover | Aurora cluster | It is not an ordinary RDS database with a customer-selected gp3/io2 volume; failover still interrupts connections |
| Microsecond eventually consistent DynamoDB reads | DAX; both item and Query/Scan caches | ElastiCache requires application-managed cache behavior and is not DynamoDB-specific |
| Cross-Region DynamoDB replication | Global tables; identify **MREC versus MRSC** | Streams replication is an MREC detail, not a universal global-table prerequisite |
| Strong reads after S3 overwrite/delete | S3 already provides strong object consistency | Cross-Region replication is a separate asynchronous process |
| Avoid clobbering a changed S3 object | Conditional write with `If-Match`/ETag | Strong consistency alone does not coordinate concurrent writers |
| Prevent deletion of retained S3 versions | Object Lock; compliance versus governance | Versioning alone permits privileged deletion of versions |
| Prevent root from removing protected backups | Backup Vault Lock **compliance mode after grace time** | Governance mode can be removed by authorized principals |
| General-purpose EBS with separately configured performance | gp3; check current size/IOPS/throughput and instance limits | Provisioned-IOPS storage is not automatically required above the old 16k gp3 ceiling |
| Change placement of an existing supported EC2 instance | Stop, modify placement, start | The old never-move-existing-instances rule is false |
| Flexible compute discount across eligible families/Regions | Compute Savings Plans | EC2 Instance Savings Plans bind to a family in one Region; discounts do not reserve capacity |
| Cheap interruptible batch work | Spot with checkpointing and capacity diversity | A higher maximum price does not guarantee uninterrupted capacity |
| HTTP(S) edge content caching | CloudFront | Global Accelerator routes traffic; it does not cache/copy the app |
| Static entry IPs and TCP/UDP routing to regional endpoints | Global Accelerator | CloudFront's primary fit is HTTP(S) content delivery |
| Private regional S3 access without NAT processing | S3 gateway endpoint where topology supports it | Gateway endpoints have no added endpoint processing fee; interface endpoints have different connectivity/pricing |
| Resource/ENI traffic filtering | Security groups | NACLs apply to subnets; security groups do not attach to the VPC edge |
| Replayed stream, destination delivery, or stream computation | Kinesis Data Streams / Data Firehose / Managed Service for Apache Flink | These serve different roles; retired Kinesis Data Analytics SQL is not a current shortcut |
| Lower recovery time after a Region failure | Match DR strategy to RTO/RPO, cost and tested failover | Multi-AZ within one Region alone does not solve a full Region outage |

## Recall and application prompts

1. Explain why “Multi-AZ standbys never serve reads” is an incomplete statement.
2. A cached read is stale: how does a DAX question differ from S3 object consistency?
3. A writer must update an object only if nobody changed it since the last read: which condition matters?
4. Why can a cheaper single-AZ design fail a scenario before you calculate cost?
5. Name one requirement that favors CloudFront and one that favors Global Accelerator.
6. Why does a Vault Lock question need its mode and grace-period details?

## Checked references

- [[04-Databases/01-RDS-Aurora-ElastiCache]] — [RDS deployment types](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Concepts.MultiAZ.html).
- [[06-Containers-Serverless/02-Serverless-Overview]] — [DAX caches](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/DAX.consistency.html), [global tables](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/V2globaltables_HowItWorks.html).
- [[03-Storage/01-S3]] and [[03-Storage/03-S3-Security]] — [conditional writes](https://docs.aws.amazon.com/AmazonS3/latest/userguide/conditional-writes.html), [Object Lock](https://docs.aws.amazon.com/AmazonS3/latest/userguide/object-lock-configure.html).
- [[02-Compute-EC2/01-EC2-Basics]] and [[02-Compute-EC2/03-EC2-Instance-Storage]] — [Savings Plans](https://docs.aws.amazon.com/savingsplans/latest/userguide/plan-types.html), [gp3](https://docs.aws.amazon.com/ebs/latest/userguide/general-purpose.html).
- [[05-Networking-Content-Delivery/02-VPC]] and [[05-Networking-Content-Delivery/03-CloudFront-Global-Accelerator]] — [S3 gateway endpoints](https://docs.aws.amazon.com/vpc/latest/privatelink/vpc-endpoints-s3.html), [Global Accelerator](https://aws.amazon.com/global-accelerator/faqs/).
- [[11-Architecture-Patterns/03-Disaster-Recovery-Migrations]] — [Vault Lock](https://docs.aws.amazon.com/aws-backup/latest/devguide/vault-lock.html), [DR options](https://docs.aws.amazon.com/whitepapers/latest/disaster-recovery-workloads-on-aws/disaster-recovery-options-in-the-cloud.html).

---
tags: [aws, saa-c03, architecture, exercises]
status: unattempted
---
# Architecture exercises — design before deploying

These are original practice briefs informed by the checked course/lab resources and official docs, not copied vendor questions. **All are unattempted.** No AWS deployment is authorized just because an exercise exists. Begin with a diagram/explanation; record work only after the learner actually performs it. For a deployed version, agree cost/prerequisites first, validate it, then verify cleanup.

For every design: list requirements, choose components, trace traffic/data, identify a failure, explain security/resilience/performance/cost, and reject the closest alternative. Answers belong in a later attempt record rather than in the question prompt.

## 1. Private three-tier application

A public web application must keep application servers and a relational database off public inbound routes. It must survive one AZ failing and access S3 without NAT processing for S3 traffic.

Draw two AZs, routing, load balancing, database topology and access rules. Explain outbound connectivity and why a public IP is not required on each server. Distinguish security groups from NACLs and justify the database deployment. Use [[05-Networking-Content-Delivery/02-VPC]], [[04-Databases/01-RDS-Aurora-ElastiCache]], [Cantrill VPC assets](https://github.com/acantril/aws-sa-associate-saac03/tree/main/0800-VIRTUAL_PRIVATE_CLOUD%28VPC%29) and the [official S3 endpoint guide](https://docs.aws.amazon.com/vpc/latest/privatelink/vpc-endpoints-s3.html).

## 2. Storage and concurrent updates

Choose storage for a Linux shared-file application, a single-instance low-latency block workload, and an object archive. A separate object-writing application must prevent overwriting a version it did not read.

Compare EBS/EFS/FSx/S3, failure scope, access pattern and current performance configuration. Explain how strong consistency differs from conditional writes and retained version protection. Use [[03-Storage/01-S3]], [[03-Storage/04-Storage-Extras]], [[02-Compute-EC2/03-EC2-Instance-Storage]], [S3 conditional writes](https://docs.aws.amazon.com/AmazonS3/latest/userguide/conditional-writes.html), and the relevant freeCodeCamp storage sections through [[00-Index/Online-Resources]].

## 3. Read scaling versus recovery

A relational workload needs to tolerate an AZ outage and offload reporting reads. Compare a Multi-AZ DB instance plus replicas, a supported Multi-AZ DB cluster, and Aurora. Then explain what additional design is needed for a Region outage.

Show which nodes serve reads, where writes go, how the application reconnects, and why replicas are not backups. Use [[04-Databases/01-RDS-Aurora-ElastiCache]], [RDS Multi-AZ documentation](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Concepts.MultiAZ.html) and the [Well-Architected Labs site](https://www.wellarchitectedlabs.com/) to select a current reliability exercise.

## 4. Burst-tolerant order processing

An API receives bursts of orders. Processing can be asynchronous, messages can be retried, and duplicate business actions must be avoided. Design the request path, queue/event routing, workers, data store and failure handling.

Explain queue versus pub/sub, scaling, retry/poison-message handling, idempotency and operational overhead. Compare Lambda and container workers without assuming previous expertise. Use [[07-Integration-Messaging/01-SQS-SNS-Kinesis]], [[06-Containers-Serverless/03-Serverless-Architectures]], and relevant official Skill Builder/freeCodeCamp sections. Do not copy external practice questions into an answer file.

## 5. RTO/RPO and protected backups

A company defines two workload classes: one can recover over hours with limited budget; the other requires much faster recovery with very little data loss. Propose and justify different DR strategies from the actual objectives.

Distinguish backup/restore, pilot light, warm standby and active-active. Include restoration testing and protection against privileged deletion; specify Vault Lock mode and grace-period implications. Use [[11-Architecture-Patterns/03-Disaster-Recovery-Migrations]], the [DR whitepaper](https://docs.aws.amazon.com/whitepapers/latest/disaster-recovery-workloads-on-aws/disaster-recovery-options-in-the-cloud.html), and the [Well-Architected Framework](https://docs.aws.amazon.com/wellarchitected/latest/framework/welcome.html).

## 6. Cost and access review

Review one earlier design for unnecessary NAT processing, cross-AZ/Region traffic, public IPv4, oversized compute/storage and unsafe commitments. Compare On-Demand, Spot, Compute Savings Plans and EC2 Instance Savings Plans against the actual interruption/flexibility requirements.

Use current [Pricing Calculator](https://calculator.aws/) inputs, not the old slides' fixed example rates. Treat a cost estimate as a scenario estimate, not a price guarantee. Compare against [[06-Cheatsheets/Architecture-Decisions]] and use Tutorials Dojo comparisons as question prompts only after checking AWS sources.

## External question calibration

After relevant study, take the official free question set and Tutorials Dojo sampler through [[00-Index/Online-Resources]]. Record source, date, fresh/repeated status, domain counts, mistakes and guesses in [[memory/progress_tracking]]. Full timed mocks follow `workflows/assessment.md`; optional community/short-form tests are supplemental. No score or readiness is implied by adding this page.

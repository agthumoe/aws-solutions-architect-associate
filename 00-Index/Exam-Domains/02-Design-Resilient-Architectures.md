---
tags:
  - aws
  - saa-c03
  - exam-domain
aliases:
  - "Domain 2"
  - "Resilient Architectures"
status: not-started
date: 2026-07-21
---

# Domain 2: Design Resilient Architectures (26%)

Source: official AWS SAA-C03 exam guide.

## Task 2.1: Design scalable and loosely coupled architectures

**Knowledge of:** API creation/management (API Gateway, REST API); AWS managed services (Transfer Family, SQS, Secrets Manager); caching strategies; microservice design principles (stateless vs stateful); event-driven architectures; horizontal vs vertical scaling; edge accelerators (CDN); migrating applications into containers; load balancing (ALB); multi-tier architectures; queuing/messaging (pub/sub); serverless technologies (Fargate, Lambda); storage types (object/file/block); container orchestration (ECS, EKS); when to use read replicas; workflow orchestration (Step Functions).

**Skills in:** Designing event-driven/microservice/multi-tier architectures; determining scaling strategies; determining services for loose coupling; determining when to use containers/serverless; recommending compute/storage/networking/database technologies; using purpose-built AWS services.

**Covered by:** [[02-Compute-EC2/04-High-Availability-Scalability]] · [[06-Containers-Serverless/01-Containers]] · [[06-Containers-Serverless/02-Serverless-Overview]] · [[06-Containers-Serverless/03-Serverless-Architectures]] · [[07-Integration-Messaging/01-SQS-SNS-Kinesis]]

## Task 2.2: Design highly available and/or fault-tolerant architectures

**Knowledge of:** AWS global infrastructure (AZs, Regions, Route 53); AWS Managed Services use cases; basic networking (route tables); DR strategies (backup and restore, pilot light, warm standby, active-active failover, RPO/RTO); distributed design patterns; failover strategies; immutable infrastructure; load balancing; proxy concepts (RDS Proxy); service quotas/throttling; storage durability/replication; workload visibility (X-Ray).

**Skills in:** Determining automation strategies for infrastructure integrity; determining services for HA/fault tolerance across Regions/AZs; identifying metrics for HA; implementing designs to mitigate single points of failure; implementing durability/availability strategies (backups); selecting DR strategy to meet business requirements; using AWS services to improve reliability of legacy applications.

**Covered by:** [[04-Databases/01-RDS-Aurora-ElastiCache]] · [[05-Networking-Content-Delivery/01-Route53]] · [[09-Monitoring-Management/01-Monitoring-Audit-Performance]] · [[11-Architecture-Patterns/03-Disaster-Recovery-Migrations]]

## Related
- [[00-Index/Home]]

## Current verification path

See [[00-Index/Exam-Scope]] for the 2026-11-09 task/reference audit and [official domain details](https://docs.aws.amazon.com/aws-certification/latest/solutions-architect-associate-03/solutions-architect-associate-03-domain2.html). This page is a course-derived summary; note presence is not learner mastery.

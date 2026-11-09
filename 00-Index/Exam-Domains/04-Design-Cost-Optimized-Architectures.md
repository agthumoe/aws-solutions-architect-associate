---
tags:
  - aws
  - saa-c03
  - exam-domain
aliases:
  - "Domain 4"
  - "Cost-Optimized Architectures"
status: not-started
date: 2026-07-21
---

# Domain 4: Design Cost-Optimized Architectures (20%)

Source: official AWS SAA-C03 exam guide.

## Task 4.1: Design cost-optimized storage solutions

**Knowledge of:** Access options (Requester Pays); AWS cost management features (cost allocation tags, multi-account billing); AWS cost management tools (Cost Explorer, Budgets, Cost and Usage Report); storage services (FSx, EFS, S3, EBS); backup strategies; block storage options (HDD vs SSD volume types); data lifecycles; hybrid storage options (DataSync, Transfer Family, Storage Gateway); storage access patterns; storage tiering; storage types.

**Skills in:** Designing appropriate storage strategies (batch vs individual uploads); determining correct storage size; determining lowest-cost data transfer method; determining when storage auto scaling is required; managing S3 object lifecycles; selecting backup/archival solution; selecting service for data migration; selecting storage tier; selecting data lifecycle; selecting most cost-effective storage service.

**Covered by:** [[03-Storage/01-S3]] · [[03-Storage/02-S3-Advanced]] · [[02-Compute-EC2/03-EC2-Instance-Storage]] · [[03-Storage/04-Storage-Extras]]

## Task 4.2: Design cost-optimized compute solutions

**Knowledge of:** AWS cost management features/tools; AWS global infrastructure; purchasing options (Spot, Reserved, Savings Plans); distributed compute strategies (edge processing); hybrid compute (Outposts); instance types/families/sizes; optimization of compute utilization (containers, serverless, microservices); scaling strategies (auto scaling, hibernation).

**Skills in:** Determining load balancing strategy (ALB vs NLB vs GWLB); determining scaling methods (horizontal vs vertical, hibernation); determining cost-effective compute services (Lambda, EC2, Fargate); determining required availability for workload classes; selecting instance family/size.

**Covered by:** [[02-Compute-EC2/01-EC2-Basics]] · [[02-Compute-EC2/02-EC2-Associate]] · [[02-Compute-EC2/04-High-Availability-Scalability]]

## Task 4.3: Design cost-optimized database solutions

**Knowledge of:** AWS cost management features/tools; caching strategies; data retention policies; database capacity planning; database connections/proxies; database engines; database replication; database types (relational vs non-relational, Aurora, DynamoDB).

**Skills in:** Designing backup/retention policies (snapshot frequency); determining appropriate database engine; determining cost-effective database services/types (DynamoDB vs RDS, serverless); migrating database schemas/data.

**Covered by:** [[04-Databases/01-RDS-Aurora-ElastiCache]] · [[04-Databases/02-Databases-Overview]]

## Task 4.4: Design cost-optimized network architectures

**Knowledge of:** AWS cost management features/tools; load balancing concepts; NAT gateways (instance vs gateway cost); network connectivity (private/dedicated lines, VPNs); network routing/topology/peering (Transit Gateway, VPC peering); network services (DNS).

**Skills in:** Configuring appropriate NAT gateway types; configuring appropriate network connections (Direct Connect vs VPN vs internet); configuring routes to minimize transfer costs; determining CDN/edge caching needs; reviewing workloads for network optimizations; selecting throttling strategy; selecting bandwidth allocation.

**Covered by:** [[05-Networking-Content-Delivery/02-VPC]] · [[05-Networking-Content-Delivery/03-CloudFront-Global-Accelerator]]

## Related
- [[00-Index/Home]]

## Current verification path

See [[00-Index/Exam-Scope]] for the 2026-11-09 task/reference audit and [official domain details](https://docs.aws.amazon.com/aws-certification/latest/solutions-architect-associate-03/solutions-architect-associate-03-domain4.html). This page is a course-derived summary; note presence is not learner mastery.

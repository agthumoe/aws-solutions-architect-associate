---
tags: [aws, saa-c03, scope, moc]
checked_on: 2026-11-09
status: reference
---
# Exam scope and reference coverage

Checked against the official **SAA-C03** guide on 2026-11-09. Four domains: secure 30%, resilient 26%, high-performing 24%, cost-optimized 20%. The 14 rows below are local summaries, not verbatim replacements for the official task details. These links identify references; **every learner task remains unassessed**.

Official task details: [D1](https://docs.aws.amazon.com/aws-certification/latest/solutions-architect-associate-03/solutions-architect-associate-03-domain1.html), [D2](https://docs.aws.amazon.com/aws-certification/latest/solutions-architect-associate-03/solutions-architect-associate-03-domain2.html), [D3](https://docs.aws.amazon.com/aws-certification/latest/solutions-architect-associate-03/solutions-architect-associate-03-domain3.html), [D4](https://docs.aws.amazon.com/aws-certification/latest/solutions-architect-associate-03/solutions-architect-associate-03-domain4.html).

| Task | Decision area | Local reference notes | Application evidence still needed |
|---|---|---|---|
| 1.1 | Secure access | [[01-Foundations/02-IAM-Basics]] · [[08-Security-Identity/01-Advanced-Identity]] | Cross-account role/resource policies; least privilege and account guardrails |
| 1.2 | Secure workloads | [[05-Networking-Content-Delivery/02-VPC]] · [[08-Security-Identity/02-Security-Encryption]] | Trace a request through network and application controls |
| 1.3 | Data security | [[03-Storage/03-S3-Security]] · [[08-Security-Identity/02-Security-Encryption]] | Choose keys, transport protection, retention and rotation |
| 2.1 | Scalable and loosely coupled | [[06-Containers-Serverless/03-Serverless-Architectures]] · [[07-Integration-Messaging/01-SQS-SNS-Kinesis]] | Decouple components, handle retry/duplicates and scaling |
| 2.2 | HA and fault tolerance | [[02-Compute-EC2/04-High-Availability-Scalability]] · [[11-Architecture-Patterns/03-Disaster-Recovery-Migrations]] | Remove single points of failure; test recovery against RTO/RPO |
| 3.1 | Performing storage | [[02-Compute-EC2/03-EC2-Instance-Storage]] · [[03-Storage/04-Storage-Extras]] | Match block/file/object and access/performance constraints |
| 3.2 | Elastic compute | [[02-Compute-EC2/04-High-Availability-Scalability]] · [[06-Containers-Serverless/01-Containers]] | Choose compute and independent scaling metrics |
| 3.3 | Performing databases | [[04-Databases/01-RDS-Aurora-ElastiCache]] · [[06-Containers-Serverless/02-Serverless-Overview]] | Choose engine, read scaling, cache, capacity and connections |
| 3.4 | Performing networks | [[05-Networking-Content-Delivery/02-VPC]] · [[05-Networking-Content-Delivery/03-CloudFront-Global-Accelerator]] | Choose edge/hybrid/endpoint/routing topology |
| 3.5 | Ingestion and transformation | [[04-Databases/03-Data-Analytics]] · [[07-Integration-Messaging/01-SQS-SNS-Kinesis]] | Separate streams, delivery, processing and analytics |
| 4.1 | Cost-efficient storage | [[03-Storage/01-S3]] · [[03-Storage/04-Storage-Extras]] | Use access patterns, lifecycle and migration constraints |
| 4.2 | Cost-efficient compute | [[02-Compute-EC2/01-EC2-Basics]] · [[06-Containers-Serverless/01-Containers]] | Compare commitments, interrupts, sizing and overhead |
| 4.3 | Cost-efficient databases | [[04-Databases/01-RDS-Aurora-ElastiCache]] · [[04-Databases/02-Databases-Overview]] | Compare capacity/engine choices and backup retention |
| 4.4 | Cost-efficient networking | [[05-Networking-Content-Delivery/02-VPC]] · [[05-Networking-Content-Delivery/03-CloudFront-Global-Accelerator]] | Identify processing, endpoint and transfer cost drivers |

## Service mention audit

The [official in-scope list](https://docs.aws.amazon.com/aws-certification/latest/solutions-architect-associate-03/saa-03-in-scope-services.html) is **non-exhaustive and subject to change**. The rows below list the 119 entries observed in that page and a matching local note. A textual mention is not full topic coverage, current accuracy, lab completion or mastery. Review each service's role and task relevance during study; secondary services need less depth than common architecture decisions.

Two missing names were added to [[11-Architecture-Patterns/04-Other-Services]]: Serverless Application Repository and Wavelength. Media is not categorically out of scope: the current list includes Kinesis Video Streams. Do not restore all old media/end-user course material simply because it exists.

| Official listed service / feature | Example local mention (not proof of coverage) |
|---|---|
| Amazon Athena | [[03-Storage/01-S3]] |
| AWS Data Exchange | [[04-Databases/03-Data-Analytics]] |
| AWS Data Pipeline | [[04-Databases/03-Data-Analytics]] |
| Amazon EMR | [[03-Storage/01-S3]] |
| AWS Glue | [[03-Storage/01-S3]] |
| Amazon Kinesis | [[00-Index/Resource-Audit]] |
| AWS Lake Formation | [[04-Databases/03-Data-Analytics]] |
| Amazon Managed Streaming for Apache Kafka (Amazon MSK) | [[04-Databases/02-Databases-Overview]] |
| Amazon OpenSearch Service | [[04-Databases/03-Data-Analytics]] |
| Amazon Quick | [[01-Foundations/02-IAM-Basics]] |
| Amazon Redshift | [[04-Databases/01-RDS-Aurora-ElastiCache]] |
| Amazon AppFlow | [[11-Architecture-Patterns/04-Other-Services]] |
| Amazon EventBridge | [[03-Storage/02-S3-Advanced]] |
| Amazon MQ | [[05-Networking-Content-Delivery/03-CloudFront-Global-Accelerator]] |
| Amazon SNS | [[03-Storage/02-S3-Advanced]] |
| Amazon SQS | [[01-Foundations/01-Getting-Started-AWS]] |
| AWS Step Functions | [[03-Storage/02-S3-Advanced]] |
| AWS Budgets | [[07-Integration-Messaging/01-SQS-SNS-Kinesis]] |
| AWS Cost and Usage Report | [[11-Architecture-Patterns/04-Other-Services]] |
| AWS Cost Explorer | [[07-Integration-Messaging/01-SQS-SNS-Kinesis]] |
| Savings Plans | [[02-Compute-EC2/01-EC2-Basics]] |
| AWS Batch | [[02-Compute-EC2/01-EC2-Basics]] |
| Amazon EC2 | [[00-Index/Home]] |
| Amazon EC2 Auto Scaling | [[02-Compute-EC2/04-High-Availability-Scalability]] |
| AWS Elastic Beanstalk | [[01-Foundations/01-Getting-Started-AWS]] |
| AWS Outposts | [[02-Compute-EC2/03-EC2-Instance-Storage]] |
| AWS Serverless Application Repository | [[11-Architecture-Patterns/04-Other-Services]] |
| VMware Cloud on AWS | [[03-Storage/04-Storage-Extras]] |
| AWS Wavelength | [[11-Architecture-Patterns/04-Other-Services]] |
| Amazon ECR | [[01-Foundations/01-Getting-Started-AWS]] |
| Amazon ECS | [[02-Compute-EC2/04-High-Availability-Scalability]] |
| Amazon ECS Anywhere | [[06-Containers-Serverless/01-Containers]] |
| Amazon EKS | [[00-Index/Home]] |
| Amazon EKS Anywhere | [[06-Containers-Serverless/01-Containers]] |
| Amazon EKS Distro | [[06-Containers-Serverless/01-Containers]] |
| Amazon Aurora | [[02-Compute-EC2/04-High-Availability-Scalability]] |
| Amazon Aurora Serverless | [[04-Databases/01-RDS-Aurora-ElastiCache]] |
| Amazon DocumentDB | [[04-Databases/02-Databases-Overview]] |
| Amazon DynamoDB | [[02-Compute-EC2/04-High-Availability-Scalability]] |
| Amazon ElastiCache | [[02-Compute-EC2/04-High-Availability-Scalability]] |
| Amazon Keyspaces | [[04-Databases/02-Databases-Overview]] |
| Amazon Neptune | [[04-Databases/02-Databases-Overview]] |
| Amazon RDS | [[01-Foundations/02-IAM-Basics]] |
| Amazon Redshift | [[04-Databases/01-RDS-Aurora-ElastiCache]] |
| AWS X-Ray | [[09-Monitoring-Management/01-Monitoring-Audit-Performance]] |
| AWS Amplify | [[11-Architecture-Patterns/04-Other-Services]] |
| Amazon API Gateway | [[05-Networking-Content-Delivery/01-Route53]] |
| AWS Device Farm | [[11-Architecture-Patterns/04-Other-Services]] |
| Amazon Comprehend | [[04-Databases/01-RDS-Aurora-ElastiCache]] |
| Amazon Lex | [[02-Compute-EC2/01-EC2-Basics]] |
| Amazon Polly | [[10-Machine-Learning/01-ML-Services]] |
| Amazon Rekognition | [[01-Foundations/01-Getting-Started-AWS]] |
| Amazon SageMaker AI | [[02-Compute-EC2/01-EC2-Basics]] |
| Amazon Textract | [[10-Machine-Learning/01-ML-Services]] |
| Amazon Transcribe | [[10-Machine-Learning/01-ML-Services]] |
| Amazon Translate | [[02-Compute-EC2/04-High-Availability-Scalability]] |
| AWS Auto Scaling | [[02-Compute-EC2/01-EC2-Basics]] |
| AWS CLI | [[01-Foundations/02-IAM-Basics]] |
| AWS CloudFormation | [[01-Foundations/02-IAM-Basics]] |
| AWS CloudTrail | [[03-Storage/03-S3-Security]] |
| Amazon CloudWatch | [[01-Foundations/02-IAM-Basics]] |
| AWS Compute Optimizer | [[09-Monitoring-Management/01-Monitoring-Audit-Performance]] |
| AWS Config | [[01-Foundations/02-IAM-Basics]] |
| AWS Control Tower | [[08-Security-Identity/01-Advanced-Identity]] |
| AWS Health Dashboard | [[09-Monitoring-Management/01-Monitoring-Audit-Performance]] |
| AWS License Manager | [[11-Architecture-Patterns/04-Other-Services]] |
| Amazon Managed Grafana | [[09-Monitoring-Management/01-Monitoring-Audit-Performance]] |
| Amazon Managed Service for Prometheus | [[09-Monitoring-Management/01-Monitoring-Audit-Performance]] |
| AWS Management Console | [[01-Foundations/02-IAM-Basics]] |
| AWS Organizations | [[04-Databases/03-Data-Analytics]] |
| AWS Proton | [[11-Architecture-Patterns/04-Other-Services]] |
| AWS Service Catalog | [[11-Architecture-Patterns/04-Other-Services]] |
| AWS Systems Manager | [[08-Security-Identity/01-Advanced-Identity]] |
| AWS Well-Architected Tool | [[11-Architecture-Patterns/04-Other-Services]] |
| Amazon Kinesis Video Streams | [[00-Index/Resource-Audit]] |
| AWS Application Discovery Service | [[11-Architecture-Patterns/03-Disaster-Recovery-Migrations]] |
| AWS Application Migration Service | [[11-Architecture-Patterns/03-Disaster-Recovery-Migrations]] |
| AWS DataSync | [[03-Storage/04-Storage-Extras]] |
| AWS DMS | [[04-Databases/01-RDS-Aurora-ElastiCache]] |
| AWS Snow Family | [[03-Storage/04-Storage-Extras]] |
| AWS Transfer Family | [[03-Storage/04-Storage-Extras]] |
| AWS Client VPN | [[05-Networking-Content-Delivery/02-VPC]] |
| Amazon CloudFront | [[01-Foundations/01-Getting-Started-AWS]] |
| AWS Direct Connect | [[03-Storage/02-S3-Advanced]] |
| Elastic Load Balancing (ELB) | [[06-Containers-Serverless/03-Serverless-Architectures]] |
| AWS Global Accelerator | [[02-Compute-EC2/04-High-Availability-Scalability]] |
| AWS PrivateLink | [[05-Networking-Content-Delivery/02-VPC]] |
| Amazon Route 53 | [[01-Foundations/01-Getting-Started-AWS]] |
| AWS Site-to-Site VPN | [[05-Networking-Content-Delivery/02-VPC]] |
| AWS Transit Gateway | [[05-Networking-Content-Delivery/02-VPC]] |
| Amazon VPC | [[00-Index/Online-Resources]] |
| AWS Artifact | [[08-Security-Identity/02-Security-Encryption]] |
| AWS Certificate Manager (ACM) | [[02-Compute-EC2/04-High-Availability-Scalability]] |
| AWS CloudHSM | [[08-Security-Identity/02-Security-Encryption]] |
| Amazon Cognito | [[03-Storage/04-Storage-Extras]] |
| Amazon Detective | [[08-Security-Identity/01-Advanced-Identity]] |
| AWS Directory Service | [[02-Compute-EC2/01-EC2-Basics]] |
| AWS Firewall Manager | [[05-Networking-Content-Delivery/02-VPC]] |
| Amazon GuardDuty | [[08-Security-Identity/02-Security-Encryption]] |
| AWS IAM Identity Center | [[08-Security-Identity/01-Advanced-Identity]] |
| Amazon Inspector | [[08-Security-Identity/02-Security-Encryption]] |
| AWS KMS | [[02-Compute-EC2/03-EC2-Instance-Storage]] |
| Amazon Macie | [[08-Security-Identity/02-Security-Encryption]] |
| AWS Network Firewall | [[05-Networking-Content-Delivery/02-VPC]] |
| AWS Resource Access Manager (AWS RAM) | [[05-Networking-Content-Delivery/02-VPC]] |
| AWS Secrets Manager | [[04-Databases/01-RDS-Aurora-ElastiCache]] |
| AWS Security Hub | [[08-Security-Identity/02-Security-Encryption]] |
| AWS Shield | [[05-Networking-Content-Delivery/02-VPC]] |
| AWS WAF | [[01-Foundations/01-Getting-Started-AWS]] |
| IAM | [[01-Foundations/01-Getting-Started-AWS]] |
| AWS Fargate | [[02-Compute-EC2/01-EC2-Basics]] |
| AWS Lambda | [[01-Foundations/01-Getting-Started-AWS]] |
| AWS Backup | [[00-Index/Online-Resources]] |
| Amazon EBS | [[01-Foundations/01-Getting-Started-AWS]] |
| Amazon EFS | [[02-Compute-EC2/01-EC2-Basics]] |
| Amazon FSx (for all types) | [[03-Storage/04-Storage-Extras]] |
| Amazon S3 | [[01-Foundations/01-Getting-Started-AWS]] |
| Amazon S3 Glacier | [[03-Storage/01-S3]] |
| AWS Storage Gateway | [[03-Storage/01-S3]] |

## Exclusions and lifecycle

Use the [official out-of-scope list](https://docs.aws.amazon.com/aws-certification/latest/solutions-architect-associate-03/saa-03-out-of-scope-services.html) and [technology concepts](https://docs.aws.amazon.com/aws-certification/latest/solutions-architect-associate-03/saa-technologies-concepts.html). Absence from a non-exhaustive in-scope list does not alone prove exclusion. Explicit examples outside scope include Personalize and developer tools such as CDK/CloudShell; they can still be useful optional lab tools.

Distinguish **exam references** from **live service availability**. Old course notes include QLDB, Kinesis Data Analytics SQL, Snowmobile and legacy migration tools. Retired services are not new deployment recommendations. Check [AWS service lifecycle](https://docs.aws.amazon.com/general/latest/gr/full_shutdown_services.html) and service-specific docs when they conflict; never delete an official task from the curriculum solely because a named example is old.

Next study step: diagnose understanding and prioritize the task decisions above. Progress stays in [[memory/progress_tracking]], not in this reference index.

---
tags:
  - aws
  - cloud-practitioner
  - mock-exam
aliases:
  - "Mock Exam 3"
status: completed
date: 2026-07-12
---

# Mock Exam 3 — 65 Questions

No answers included in this file. See `mock-exam-3-results.md` for your answers vs. correct answers.

---

### Q1
An IT company has a hybrid cloud architecture and it wants to centralize the server logs for its Amazon Elastic Compute Cloud (Amazon EC2) instances and on-premises servers. Which of the following is the MOST effective for this use-case?

A) Use AWS CloudTrail for the Amazon Elastic Compute Cloud (Amazon EC2) instance and Amazon CloudWatch Logs for the on-premises servers
B) Use Amazon CloudWatch Logs for the Amazon Elastic Compute Cloud (Amazon EC2) instance and AWS CloudTrail for the on-premises servers
C) Use Amazon CloudWatch Logs for both the Amazon Elastic Compute Cloud (Amazon EC2) instance and the on-premises servers
D) Use AWS Lambda to send log data from Amazon Elastic Compute Cloud (Amazon EC2) instance as well as on-premises servers to Amazon CloudWatch Logs

---

### Q2 (Select TWO)
Which of the following AWS services offer block-level storage?

A) Amazon Elastic File System (Amazon EFS)
B) Amazon Elastic Container Service (Amazon ECS)
C) Amazon Elastic Block Store (Amazon EBS)
D) Instance Store
E) Amazon Simple Storage Service (Amazon S3)

---

### Q3
Which of the following is correct regarding the AWS Shield Advanced pricing?

A) AWS Shield Advanced offers protection against higher fees that could result from a DDoS attack
B) AWS Shield Advanced is a free service for AWS Enterprise Support plan
C) AWS Shield Advanced is a free service for AWS Business Support plan
D) AWS Shield Advanced is a free service for all AWS Support plans

---

### Q4 (Select TWO)
Which of the following are recommended best practices for AWS Identity and Access Management (AWS IAM) service?

A) Grant maximum privileges to avoid assigning privileges again
B) Share AWS account root user access keys with other administrators
C) Enable multi-factor authentication (MFA) for all users
D) Rotate credentials regularly
E) Create a minimum number of accounts and share these account credentials among employees

---

### Q5
Under the AWS Shared Responsibility Model, which of the following is the responsibility of a customer regarding AWS Lambda?

A) Configure networking infrastructure for the AWS Lambda functions
B) Patch underlying OS for the AWS Lambda function infrastructure
C) Maintain all runtime environments for AWS Lambda functions
D) Maintain versions of an AWS Lambda function

---

### Q6
Which AWS service will you use to privately connect your virtual private cloud (VPC) to Amazon Simple Storage Service (Amazon S3)?

A) VPC Endpoint
B) AWS Transit Gateway
C) Amazon API Gateway
D) AWS Direct Connect

---

### Q7
A company has a static website hosted on an Amazon Simple Storage Service (Amazon S3) bucket in an AWS Region in Asia. Although most of its users are in Asia, now it wants to drive growth globally. How can it improve the global performance of its static website?

A) Use Amazon S3 Transfer Acceleration (Amazon S3TA) to improve the performance of your website
B) Use Amazon CloudFront to improve the performance of your website
C) Use Amazon CloudFormation to improve the performance of your website
D) Use AWS Web Application Firewall (AWS WAF) to improve the performance of your website

---

### Q8
Which feature of AWS Cloud offers the ability to innovate faster and rapidly develop, test and launch software applications?

A) Agility
B) Cost savings
C) Elasticity
D) Ability to deploy globally in minutes

---

### Q9
A financial services company must meet compliance requirements that mandate storing multiple copies of data in geographically distant locations. As the company uses Amazon Simple Storage Service (Amazon S3) as its main storage service, which of the following represents the MOST resource-efficient solution for this use-case?

A) Use S3 cross-region replication (S3 CRR) to replicate data between distant AWS Regions
B) Use S3 same-region replication (S3 SRR) to replicate data between distant AWS Regions
C) For every new object, trigger an AWS Lambda function to write data into a bucket in another AWS Region
D) Run a daily job on an Amazon Elastic Compute Cloud (Amazon EC2) instance to copy objects into another Region

---

### Q10
Which of the following statements is correct regarding the Amazon Elastic File System (Amazon EFS) storage service?

A) EC2 instances can access files on an Amazon Elastic File System (Amazon EFS) file system across many Availability Zones (AZ) and VPCs but not across Regions
B) EC2 instances can access files on an Amazon Elastic File System (Amazon EFS) file system across many Availability Zones (AZ) but not across VPCs and Regions
C) EC2 instances can access files on an Amazon Elastic File System (Amazon EFS) file system across many Availability Zones (AZ), Regions and VPCs
D) EC2 instances can access files on an Amazon Elastic File System (Amazon EFS) file system only in one Availability Zone (AZ)

---

### Q11
Which AWS service can be used for online analytical processing?

A) Amazon Redshift
B) Amazon Relational Database Service (Amazon RDS)
C) Amazon DynamoDB
D) Amazon ElastiCache

---

### Q12
Which of the following is a part of the AWS Global Infrastructure?

A) Virtual Private Cloud (VPC)
B) AWS Region
C) Virtual Private Network (VPN)
D) Subnet

---

### Q13
A startup has just moved its IT infrastructure to AWS Cloud. The CTO would like to receive detailed reports that break down the startup's AWS costs by the hour in an Amazon Simple Storage Service (Amazon S3) bucket. As a Cloud Practitioner, which AWS service would you recommend for this use-case?

A) AWS Pricing Calculator
B) AWS Cost & Usage Report (AWS CUR)
C) AWS Cost Explorer
D) AWS Budgets

---

### Q14
Which of the following improves the availability for a fleet of Amazon Elastic Compute Cloud (Amazon EC2) instances?

A) Deploy the Amazon Elastic Compute Cloud (Amazon EC2) instances in the same Availability Zone (AZ) across two different AWS Regions
B) Deploy the Amazon Elastic Compute Cloud (Amazon EC2) instances in the same Availability Zone (AZ) of an AWS Region
C) Deploy the Amazon Elastic Compute Cloud (Amazon EC2) instances across different Availability Zones (AZ) in the same AWS Region
D) Deploy the Amazon Elastic Compute Cloud (Amazon EC2) instances across different AWS Regions of the same Availability Zone (AZ)

---

### Q15 (Select TWO)
A customer is running a comparative study of pricing models of Amazon EFS and Amazon Elastic Block Store (Amazon EBS) that are used with the Amazon EC2 instances that host the application. Which of the following statements are correct regarding this use-case?

A) Amazon Elastic Block Store (Amazon EBS) Snapshots are stored incrementally, which means you are billed only for the changed blocks stored
B) You will pay a fee each time you read from or write data stored on the Amazon Elastic File System (Amazon EFS) - Infrequent Access storage class
C) Amazon Elastic Block Store (Amazon EBS) Snapshot storage pricing is based on the amount of space your data consumes in Amazon Elastic Block Store (Amazon EBS)
D) Amazon Elastic Compute Cloud (Amazon EC2) data transfer charges will apply for all Amazon Elastic Block Store (Amazon EBS) direct APIs for Snapshots
E) With AWS Backup, you pay only for the amount of Amazon Elastic File System (Amazon EFS) backup storage you use in a month, you need not pay for restoring this data

---

### Q16 (Select THREE)
Which budget types can be created under AWS Budgets?

A) Software budget
B) Resource budget
C) Usage budget
D) Cost budget
E) Reservation budget
F) Hardware budget

---

### Q17
Which of the following AWS entities provides the information required to launch an Amazon Elastic Compute Cloud (Amazon EC2) instance?

A) Amazon Elastic File System (Amazon EFS)
B) Amazon Elastic Block Store (Amazon EBS)
C) AWS Lambda
D) Amazon Machine Image (AMI)

---

### Q18 (Select TWO)
Which of the following statements are CORRECT regarding security groups and network access control lists (network ACL)?

A) A network access control list (network ACL) is stateful, that is, it automatically allows the return traffic
B) A security group contains a numbered list of rules and evaluates these rules in the increasing order while deciding whether to allow the traffic
C) A network access control list (network ACL) contains a numbered list of rules and evaluates these rules in the increasing order while deciding whether to allow the traffic
D) A security group is stateless, that is, the return traffic must be explicitly allowed
E) A security group is stateful, that is, it automatically allows the return traffic

---

### Q19
Which AWS service can be used to automate code deployment to Amazon Elastic Compute Cloud (Amazon EC2) instances as well as on-premises instances?

A) AWS CodeCommit
B) AWS CodePipeline
C) AWS CloudFormation
D) AWS CodeDeploy

---

### Q20 (Select TWO)
AWS Trusted Advisor analyzes your AWS environment and provides best practice recommendations for which of the following categories?

A) Service Limits
B) Cost Optimization
C) Change Management
D) Documentation
E) Elasticity

---

### Q21
An IT company has deployed a static website on Amazon Simple Storage Service (Amazon S3), but the website is still inaccessible. As a Cloud Practioner, which of the following solutions would you suggest to address this issue?

A) Disable Amazon S3 encryption
B) Enable Amazon S3 replication
C) Enable Amazon S3 versioning
D) Fix the Amazon S3 bucket policy

---

### Q22
A research lab wants to optimize the caching capabilities for its scientific computations application running on Amazon Elastic Compute Cloud (Amazon EC2) instances. Which Amazon Elastic Compute Cloud (Amazon EC2) storage option is best suited for this use-case?

A) Amazon Elastic File System (Amazon EFS)
B) Amazon Elastic Block Store (Amazon EBS)
C) Amazon Simple Storage Service (Amazon S3)
D) Instance Store

---

### Q23
Which AWS service can be used as an in-memory database with high-performance and low latency?

A) Amazon Relational Database Service (Amazon RDS)
B) Amazon ElastiCache
C) Amazon DynamoDB
D) Amazon Athena

---

### Q24 (Select TWO)
Which of the following are components of an AWS Site-to-Site VPN?

A) AWS storage gateway
B) Network Address Translation gateway (NAT gateway)
C) Customer gateway
D) Internet gateway
E) Virtual private gateway (VGW)

---

### Q25
A research group wants to provision an Amazon Elastic Compute Cloud (Amazon EC2) instance for a flexible application that can be interrupted. As a Cloud Practitioner, which of the following would you recommend as the MOST cost-optimal option?

A) Spot Instance
B) Dedicated Host
C) Reserved Instance (RI)
D) On-Demand Instance

---

### Q26
A development team is looking for a forum where the most frequent questions and requests from AWS customers are listed along with AWS provided solutions.

Which AWS forum/service can be used for troubleshooting an issue or checking for a solution?

A) AWS Knowledge Center
B) AWS Marketplace
C) AWS Health Dashboard - service health
D) AWS Support Center

---

### Q27 (Select TWO)
AWS Lambda pricing is based on which of the following criteria?

A) Number of requests for the AWS Lambda function
B) The number of lines of code for the AWS Lambda function
C) The size of the deployment package for the AWS Lambda function
D) The time it takes for the AWS Lambda function to execute
E) The language runtime of the AWS Lambda function

---

### Q28 (Select TWO)
Which of the following statements are true about Cost Allocation Tags in AWS Billing?

A) For each resource, each tag key must be unique, but can have multiple values
B) Tags help in organizing resources and are a mandatory configuration item to run reports
C) For each resource, each tag key must be unique, and each tag key can have only one value
D) You must activate both AWS generated tags and user-defined tags separately before they can appear in Cost Explorer or on a cost allocation report
E) Only user-defined tags need to be activated before they can appear in Cost Explorer or on a cost allocation report

---

### Q29
A medical device company is looking for a durable and cost-effective way of storing their historic data. Due to compliance requirements, the data must be stored for 10 years. Which AWS Storage solution will you suggest?

A) Amazon S3 Glacier Flexible Retrieval
B) Amazon Elastic File System (Amazon EFS)
C) AWS Storage Gateway
D) Amazon S3 Glacier Deep Archive

---

### Q30
Which AWS service protects your AWS account by monitoring malicious activity and detecting threats?

A) AWS CloudTrail
B) AWS Trusted Advisor
C) Amazon CloudWatch
D) Amazon GuardDuty

---

### Q31
A multi-national company has its business-critical data stored on a fleet of Amazon Elastic Compute Cloud (Amazon EC2) instances, in various countries, configured in region-specific compliance rules. To demonstrate compliance, the company needs to submit historical configurations on a regular basis. Which AWS service is best suited for this requirement?

A) Amazon Macie
B) AWS CloudTrail
C) AWS Config
D) Amazon GuardDuty

---

### Q32
A cyber-security agency uses AWS Cloud and wants to carry out security assessments on its own AWS infrastructure without any prior approval from AWS. Which of the following describes/facilitates this practice?

A) Network Stress Testing
B) Penetration Testing
C) Amazon Inspector
D) AWS Secrets Manager

---

### Q33
As a Cloud Practitioner, which Amazon Simple Storage Service (Amazon S3) storage class would you recommend for data archival?

A) Amazon S3 Intelligent-Tiering
B) Amazon S3 Glacier Flexible Retrieval
C) Amazon S3 One Zone-Infrequent Access (S3 One Zone-IA)
D) Amazon S3 Standard

---

### Q34
An enterprise is developing a roadmap for its cloud adoption journey and wants to ensure its IT investments align with business objectives and deliver measurable value. Which perspective of the AWS Cloud Adoption Framework (CAF) addresses the strategy management capability?

A) Platform Perspective
B) Operations Perspective
C) Governance Perspective
D) Business Perspective

---

### Q35
Which Amazon Simple Storage Service (Amazon S3) storage class offers the lowest availability?

A) Amazon S3 One Zone-Infrequent Access (S3 One Zone-IA)
B) Amazon S3 Standard
C) Amazon S3 Glacier Flexible Retrieval
D) Amazon S3 Intelligent-Tiering

---

### Q36 (Select TWO)
Which AWS services/features support High Availability by default?

A) Instance Store
B) Subnet
C) Amazon Elastic Block Store (Amazon EBS)
D) Amazon Elastic File System (Amazon EFS)
E) Amazon DynamoDB

---

### Q37
A financial services enterprise plans to enable Multi-Factor Authentication (MFA) for its employees. For ease of travel, they prefer not to use any physical devices to implement Multi-Factor Authentication (MFA). Which of the below options is best suited for this use case?

A) Soft Token Multi-Factor Authentication (MFA) device
B) Virtual Multi-Factor Authentication (MFA) device
C) Hardware Multi-Factor Authentication (MFA) device
D) U2F security key

---

### Q38
A startup runs its proprietary application on docker containers. As a Cloud Practitioner, which AWS service would you recommend so that the startup can run containers and still have access to the underlying servers?

A) AWS Fargate
B) AWS Lambda
C) Amazon Elastic Container Registry (Amazon ECR)
D) Amazon Elastic Container Service (Amazon ECS)

---

### Q39 (Select TWO)
Which of the following AWS services specialize in data migration from on-premises to AWS Cloud?

A) AWS Snowball
B) AWS Direct Connect
C) AWS Database Migration Service (AWS DMS)
D) AWS Site-to-Site VPN
E) AWS Transit Gateway

---

### Q40
A global e-commerce platform wants to restrict access to its website from specific countries to comply with regional regulations. Which AWS service is best suited to implement this restriction?

A) AWS Shield
B) Amazon WAF
C) Amazon Pinpoint
D) Amazon Fraud Detector

---

### Q41 (Select TWO)
Which of the following are correct statements regarding the AWS Shared Responsibility Model?

A) AWS is responsible for Security 'of' the Cloud
B) For abstracted services like Amazon S3, AWS operates the infrastructure layer, the operating system, and platforms
C) AWS is responsible for training AWS and customer employees on AWS products and services
D) For a service like Amazon EC2, that falls under Infrastructure as a Service (IaaS), AWS is responsible for maintaining guest operating system
E) Configuration Management is the responsibility of the customer

---

### Q42
An AWS hardware failure has impacted one of your Amazon Elastic Block Store (Amazon EBS) volumes. Which AWS service will alert you of the affected resources and provide a remedial action?

A) AWS Config
B) Amazon GuardDuty
C) AWS Trusted Advisor
D) AWS Health Dashboard – Your account health

---

### Q43
Which pillar of the AWS Well-Architected Framework recommends maintaining infrastructure as code (IaC)?

A) Performance Efficiency
B) Operational Excellence
C) Cost Optimization
D) Security

---

### Q44 (Select TWO)
Which of the following AWS services have data encryption automatically enabled?

A) Amazon Elastic File System (Amazon EFS)
B) Amazon Elastic Block Store (Amazon EBS)
C) Amazon Simple Storage Service (Amazon S3)
D) Amazon Redshift
E) AWS Storage Gateway

---

### Q45
As per the AWS Shared Responsibility Model, Security and Compliance is a shared responsibility between AWS and the customer. Which of the following security services/utilities falls under the purview of AWS under the AWS Shared Responsibility Model?

A) AWS Shield Standard
B) AWS Web Application Firewall (AWS WAF)
C) Security group
D) AWS Shield Advanced

---

### Q46
Compared to the on-demand instance prices, what is the highest possible discount offered for reserved instances (RI)?

A) 90
B) 72
C) 40
D) 50

---

### Q47 (Select TWO)
According to the AWS Shared Responsibility Model, which of the following are the responsibilities of the customer?

A) Managing IAM users and roles
B) Compliance validation of Cloud infrastructure
C) Ensuring AWS employees cannot access customer data
D) AWS Global Network Security
E) Operating system patches and updates of an Amazon Elastic Compute Cloud (Amazon EC2) instance

---

### Q48
Which of the following use cases is best suited for Amazon EFS Standard-Infrequent Access (EFS Standard-IA) storage class?

A) Object storage for workloads that need sub-second latency speeds for accessing the data
B) Storing data in a single AWS Availability Zone (AZ)
C) Use as boot volume for highly available Amazon Elastic Compute Cloud (Amazon EC2) instances
D) Storing files in an accessible location to satisfy audit requirements

---

### Q49
What is the primary benefit of deploying an Amazon Relational Database Service (Amazon RDS) database in a Read Replica configuration?

A) Read Replica reduces database usage costs
B) Read Replica improves database scalability
C) Read Replica protects the database from a regional failure
D) Read Replica enhances database availability

---

### Q50
Which of the following capabilities does Amazon Rekognition provide as a ready-to-use feature?

A) Identify objects in a photo
B) Human pose detection
C) Convert images into greyscale
D) Resize images quickly

---

### Q51
AWS Identity and Access Management (AWS IAM) policies are written as JSON documents. Which of the following are mandatory elements of an IAM policy?

A) Action, Condition
B) Effect, Action
C) Sid, Principal
D) Effect, Sid

---

### Q52
An IT company would like to move its IT resources (including any data and applications) from an AWS Region in the US to another AWS Region in Europe. Which of the following represents the correct solution for this use-case?

A) The company should raise a ticket with AWS Support for this resource migration
B) The company should just start creating new resources in the destination AWS Region and then migrate the relevant data and applications into this new AWS Region
C) The company should use AWS Database Migration Service (AWS DMS) to move the resources (including any data and applications) from source AWS Region to destination AWS Region
D) The company should use AWS CloudFormation to move the resources (including any data and applications) from source AWS Region to destination AWS Region

---

### Q53
Which of the following Cloud Computing models does the 'gmail' service represent?

A) Software as a service (SaaS)
B) Function as a service (FaaS)
C) Infrastructure as a service (IaaS)
D) Platform as a service (PaaS)

---

### Q54
Which AWS service can be used to execute code triggered by new files being uploaded to Amazon Simple Storage Service (Amazon S3)?

A) Amazon Elastic Compute Cloud (Amazon EC2)
B) AWS Lambda
C) Amazon Simple Queue Service (Amazon SQS)
D) Amazon Elastic Container Service (Amazon ECS)

---

### Q55
A leading research firm needs to access information available in old patents and documents (such as PDFs, Text Files, Word documents, etc) present in its huge knowledge base. The firm is looking for a powerful search tool that can dig into these knowledge resources and return the most relevant files/documents. Which of the following is the correct service to address this requirement?

A) Amazon Kendra
B) Amazon Comprehend
C) Amazon Personalize
D) Amazon Lex

---

### Q56 (Select TWO)
Which of the following statements are CORRECT about the AWS Auto Scaling group?

A) Auto Scaling group scales out and adds more number of Amazon EC2 instances to match an increase in demand
B) Auto Scaling group scales in and reduces the number of Amazon EC2 instances to match a decrease in demand
C) Auto Scaling group scales down and reduces the number of Amazon EC2 instances to match a decrease in demand
D) Auto Scaling group scales up and upgrades to a more powerful Amazon EC2 instance to match an increase in demand
E) Auto Scaling group scales down and downgrades to a less powerful Amazon EC2 instance to match a decrease in demand

---

### Q57
Amazon CloudWatch billing metric data is stored in which AWS Region?

A) US West (N. California) - us-west-1
B) US East (N. Virginia) - us-east-1
C) In the AWS Region where the AWS account is created
D) In the AWS Region where the AWS resource is provisioned

---

### Q58
An e-commerce company uses AWS Cloud and would like to receive separate invoices for development and production environments. As a Cloud Practioner, which of the following solutions would you recommend for this use-case?

A) Create separate AWS accounts for development and production environments to receive separate invoices
B) Use AWS Cost Explorer to create separate invoices for development and production environments
C) Tag all resources in the AWS account as either development or production. Then use the tags to create separate invoices
D) Use AWS Organizations to create separate invoices for development and production environments

---

### Q59 (Select TWO)
An IT company is on a cost-optimization spree and wants to identify all Amazon Elastic Compute Cloud (Amazon EC2) instances that are under-utilized. Which AWS services can be used off-the-shelf to address this use-case without needing any manual configurations?

A) AWS Cost Explorer
B) AWS Budgets
C) AWS Trusted Advisor
D) Amazon CloudWatch
E) AWS Cost & Usage Report (AWS CUR)

---

### Q60
Which Amazon Route 53 routing policy would you use when you want to route your traffic in an active-passive configuration?

A) Latency-based routing
B) Failover routing
C) Weighted routing
D) Simple routing

---

### Q61
An organization maintains separate Amazon Virtual Private Clouds (Amazon VPC) for each of its departments. With expanding business, the organization now wants to connect all Amazon Virtual Private Clouds (Amazon VPC) for better departmental collaboration. Which AWS service will help the organization tackle the issue effectively?

A) AWS Transit Gateway
B) AWS Site-to-Site VPN
C) VPC peering connection
D) AWS Direct Connect

---

### Q62
An AWS user is trying to launch an Amazon Elastic Compute Cloud (Amazon EC2) instance in a given region. What is the region-specific constraint that the Amazon Machine Image (AMI) must meet so that it can be used for this Amazon Elastic Compute Cloud (Amazon EC2) instance?

A) An Amazon Machine Image (AMI) is a global entity, so the region is not applicable
B) You must use an Amazon Machine Image (AMI) from the same region as that of the Amazon EC2 instance. The region of the Amazon Machine Image (AMI) has no bearing on the performance of the Amazon EC2 instance
C) You should use an Amazon Machine Image (AMI) from the same region, as it improves the performance of the Amazon EC2 instance
D) You can use an Amazon Machine Image (AMI) from a different region, but it degrades the performance of the Amazon EC2 instance

---

### Q63
Which AWS service will you use if you have to move large volumes of on-premises data to AWS Cloud from a remote location with limited bandwidth?

A) AWS Transit Gateway
B) AWS Direct Connect
C) AWS Snowball
D) AWS Virtual Private Network (VPN)

---

### Q64 (Select TWO)
Which of the following AWS services are regional in scope?

A) Amazon Rekognition
B) AWS Identity and Access Management (AWS IAM)
C) Amazon CloudFront
D) AWS Web Application Firewall (AWS WAF)
E) AWS Lambda

---

### Q65
Which of the following is the best way to protect your data from accidental deletion on Amazon S3?

A) Amazon S3 Versioning
B) Amazon S3 lifecycle configuration
C) Amazon S3 storage classes
D) Amazon S3 Transfer Acceleration (Amazon S3TA)

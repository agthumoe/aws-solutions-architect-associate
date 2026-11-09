---
tags:
  - aws
  - cloud-practitioner
  - mock-exam
aliases:
  - "Mock Exam 1"
status: completed
date: 2026-07-12
---

# Mock Exam 1 — 65 Questions

No answers included in this file. See `mock-exam-1-results.md` for your answers vs. correct answers.

---

### Q1
A cyber forensics team has detected that AWS owned IP-addresses are being used to carry out malicious attacks. As this constitutes prohibited use of AWS services, which of the following is the correct solution to address this issue?

A) Contact AWS Support
B) Contact AWS Developer Forum moderators
C) Write an email to Jeff Bezos, the founder of Amazon, with the details of the incident
D) Contact AWS Abuse Team

---

### Q2
Which security service of AWS is enabled for all AWS customers, by default, at no additional cost?

A) AWS Shield Advanced
B) AWS Shield Standard
C) AWS Secrets Manager
D) AWS Web Application Firewall (AWS WAF)

---

### Q3
Which of the following Amazon S3 storage classes takes the most time to retrieve data (also known as first byte latency)?

A) Amazon S3 Standard
B) Amazon S3 Glacier Flexible Retrieval
C) Amazon S3 Intelligent-Tiering
D) Amazon S3 Glacier Deep Archive

---

### Q4
A silicon valley based healthcare startup stores anonymized patient health data on Amazon S3. The CTO further wants to ensure that any sensitive data on S3 is discovered and identified to prevent any sensitive data leaks. As a Cloud Practitioner, which AWS service would you recommend addressing this use-case?

A) AWS Glue
B) AWS Secrets Manager
C) Amazon Macie
D) Amazon Polly

---

### Q5
Which of the following is CORRECT regarding removing an AWS account from AWS Organizations?

A) Raise a support ticket with AWS Support to remove the account
B) The AWS account must not have any Service Control Policies (SCPs) attached to it. Only then it can be removed from AWS organizations
C) The AWS account must be able to operate as a standalone account. Only then it can be removed from AWS organizations
D) The AWS account can be removed from AWS Systems Manager

---

### Q6 (Select THREE)
Which of the following AWS services support reservations to optimize costs?

A) Amazon DocumentDB
B) AWS Lambda
C) Amazon Simple Storage Service (Amazon S3)
D) Amazon Relational Database Service (Amazon RDS)
E) Amazon Elastic Compute Cloud (Amazon EC2)
F) Amazon DynamoDB

---

### Q7 (Select TWO)
According to the AWS Shared Responsibility Model, which of the following are responsibilities of AWS?

A) Replacing faulty hardware of Amazon EC2 instances
B) Creating S3 bucket policies for appropriate user access
C) Operating the infrastructure layer, the operating system and the platform for the Amazon S3 service
D) Enabling Multi Factor Authentication on AWS accounts in your organization
E) Creating IAM role for accessing Amazon EC2 instances

---

### Q8
A company needs a storage solution for a project wherein the data is accessed less frequently but needs rapid access when required. Which S3 storage class is the MOST cost-effective for the given use-case?

A) Amazon S3 Glacier (S3 Glacier)
B) Amazon S3 Standard-Infrequent Access (S3 Standard-IA)
C) Amazon S3 Standard
D) Amazon S3 Intelligent-Tiering (S3 Intelligent-Tiering)

---

### Q9 (Select TWO)
AWS Shield Advanced provides expanded DDoS attack protection for web applications running on which of the following resources?

A) AWS CloudFormation
B) Amazon Route 53
C) AWS Global Accelerator
D) AWS Elastic Beanstalk
E) Amazon API Gateway

---

### Q10
Which AWS Support plan provides architectural guidance contextual to your specific use-cases?

A) AWS Developer Support
B) AWS Enterprise On-Ramp Support
C) AWS Business Support
D) AWS Enterprise Support

---

### Q11 (Select TWO)
Which option is a common stakeholder role for the AWS Cloud Adoption Framework (AWS CAF) platform perspective?

A) Chief Product Officer (CPO)
B) Chief Data Officer (CDO)
C) Chief Information Officer (CIO)
D) Chief Technology Officer (CTO)
E) Engineer

---

### Q12
Which of the following is the MOST cost-effective option to purchase an EC2 Reserved Instance (RI)?

A) No upfront payment option with standard 3-years term
B) No upfront payment option with standard 1-year term
C) All upfront payment option with the standard 1-year term
D) Partial upfront payment option with standard 3-years term

---

### Q13
Which AWS service will help you receive alerts when the reservation utilization falls below the defined threshold?

A) AWS Pricing Calculator
B) AWS CloudTrail
C) AWS Trusted Advisor
D) AWS Budgets

---

### Q14 (Select TWO)
Which of the following AWS services support VPC Gateway Endpoint for a private connection from a VPC?

A) Amazon Simple Notification Service (SNS)
B) Amazon DynamoDB
C) Amazon Simple Queue Service (SQS)
D) Amazon Simple Storage Service (Amazon S3)
E) Amazon Elastic Compute Cloud (Amazon EC2)

---

### Q15
Which of the following AWS services can be used to connect a company's on-premises environment to a VPC without using the public internet?

A) AWS Direct Connect
B) AWS Site-to-Site VPN
C) Internet Gateway
D) VPC Endpoint

---

### Q16
Which of the following AWS services should be used to automatically distribute incoming traffic across multiple targets?

A) AWS Elastic Load Balancing (ELB)
B) Amazon OpenSearch Service
C) AWS Auto Scaling
D) AWS Elastic Beanstalk

---

### Q17 (Select TWO)
Which AWS services can be used to decouple components of a microservices based application on AWS Cloud?

A) AWS Step Functions
B) Amazon Simple Queue Service (SQS)
C) AWS Lambda
D) Amazon Elastic Compute Cloud (Amazon EC2)
E) Amazon Simple Notification Service (SNS)

---

### Q18
Which type of cloud computing does Amazon Elastic Compute Cloud (EC2) represent?

A) Software as a Service (SaaS)
B) Infrastructure as a Service (IaaS)
C) Network as a Service (NaaS)
D) Platform as a Service (PaaS)

---

### Q19
Which of the following is an AWS database service?

A) AWS Glue
B) AWS Storage Gateway
C) Amazon Redshift
D) AWS Database Migration Service (AWS DMS)

---

### Q20 (Select TWO)
Which of the following statements are CORRECT regarding the AWS VPC service?

A) A Security Group can have allow rules only
B) A network access control list (network ACL) can have allow rules only
C) A Network Address Translation gateway (NAT gateway) is managed by AWS
D) A Security Group can have both allow and deny rules
E) A Network Address Translation instance (NAT instance) is managed by AWS

---

### Q21
A medical research startup wants to understand the compliance of AWS services concerning HIPAA guidelines. Which AWS service can be used to review the HIPAA compliance and governance-related documents on AWS?

A) AWS Trusted Advisor
B) AWS Systems Manager
C) AWS Artifact
D) AWS Secrets Manager

---

### Q22
Which of the following entities applies patches to the underlying OS for Amazon Aurora?

A) The AWS Product Team automatically
B) The AWS Support after receiving a request from the customer
C) The AWS customer by using AWS Systems Manager
D) The AWS customer by SSHing on the instances

---

### Q23
Which of the following is a serverless AWS service?

A) Amazon Elastic Compute Cloud (Amazon EC2)
B) AWS Lambda
C) AWS Elastic Beanstalk
D) Amazon EMR

---

### Q24 (Select TWO)
A Project Manager, working on AWS for the first time, is confused about how credits are used in AWS. There are two credits available in the manager's account. Credit one is for $100, expires July 2022, and can be used for either Amazon S3 or Amazon EC2. Credit two is for $50, expires December 2022, and can be used only for Amazon EC2. The manager's AWS account has incurred two charges: $1000 for Amazon EC2 and $500 for Amazon S3.

What will be the outcome on the overall bill once the credits are used?

A) Then, credit two is applied to the remaining $900 of Amazon EC2 usage
B) Then, credit two is applied to $500 for Amazon S3 usage
C) Credit one is applied, which expires in July, to Amazon S3 usage which leaves you with a $1000 Amazon EC2 charge and a $400 Amazon S3 charge
D) Credit one is applied, which expires in July, to the Amazon EC2 charge which leaves you with a $900 Amazon EC2 charge and a $500 Amazon S3 charge
E) Only one credit can be used in one billing cycle and the customer has a choice to choose from the available ones

---

### Q25
The DevOps team at an IT company is moving 500 GB of data from an EC2 instance to an S3 bucket in the same region. Which of the following scenario captures the correct charges for this data transfer?

A) The company would only be charged for the outbound data transfer from EC2 instance
B) The company would be charged for both the outbound data transfer from EC2 instance as well as the inbound data transfer into the S3 bucket
C) The company would not be charged for this data transfer
D) The company would only be charged for the inbound data transfer into the S3 bucket

---

### Q26
Which AWS Route 53 routing policy would you use to route traffic to multiple resources and also choose how much traffic is routed to each resource?

A) Simple routing
B) Weighted routing
C) latency-based routing
D) Failover routing

---

### Q27
Which of the following is a recommended way to provide programmatic access to AWS resources?

A) Use Access Key ID and Secret Access Key to access AWS resources programmatically
B) Create a new IAM user and share the username and password
C) Use IAM user group to access AWS resources programmatically
D) Use AWS Multi-Factor Authentication (AWS MFA) to access AWS resources programmatically

---

### Q28
A company wants to move to AWS cloud and release new features with quick iterations by utilizing relevant AWS services whenever required. Which of the following characteristics of AWS Cloud does it want to leverage?

A) Reliability
B) Scalability
C) Agility
D) Elasticity

---

### Q29
AWS Web Application Firewall (WAF) offers protection from common web exploits at which layer?

A) Layer 3
B) Layer 7
C) Layer 4 and 7
D) Layer 4

---

### Q30 (Select TWO)
According to the AWS Cloud Adoption Framework (AWS CAF), what are two tasks that a company should perform when planning to migrate to the AWS Cloud and aiming to become more responsive to customer inquiries and feedback as part of their organizational transformation?

A) Organize your teams around products and value streams
B) Leverage agile methods to rapidly iterate and evolve
C) Organize your teams around bureaucratic design principles
D) Leverage legacy infrastructure for cost efficiencies
E) Create new analytical insights with existing products and services

---

### Q31
The DevOps team at an e-commerce company is trying to debug performance issues for its serverless application built using a microservices architecture. As a Cloud Practitioner, which AWS service would you recommend to address this use-case?

A) AWS Trusted Advisor
B) AWS X-Ray
C) Amazon Pinpoint
D) AWS CloudFormation

---

### Q32
A company wants to identify the optimal AWS resource configuration for its workloads so that the company can reduce costs and increase workload performance. Which of the following services can be used to meet this requirement?

A) AWS Systems Manager
B) AWS Budgets
C) AWS Compute Optimizer
D) AWS Cost Explorer

---

### Q33
A company wants to improve the resiliency of its flagship application so it wants to move from its traditional database system to a managed AWS NoSQL database service to support active-active configuration in both the East and West US AWS regions. The active-active configuration with cross-region support is the prime criteria for any database solution that the company considers.

Which AWS database service is the right fit for this requirement?

A) Amazon Relational Database Service (Amazon RDS) for MYSQL
B) Amazon DynamoDB with DynamoDB Accelerator
C) Amazon DynamoDB with global tables
D) Amazon Aurora with multi-master clusters

---

### Q34
A web application stores all of its data on Amazon S3 buckets. A client has mandated that data be encrypted before sending it to Amazon S3.

Which of the following is the right technique for encrypting data as needed by the customer?

A) Enable server-side encryption with AWS Key Management Service (AWS KMS) keys (SSE-KMS)
B) Enable server-side encryption with Amazon S3 Managed Keys (SSE-S3)
C) Encryption is enabled by default for all the objects written to Amazon S3. Additional configuration is not required
D) Enable client-side encryption using AWS encryption SDK

---

### Q35
Which of the following statements are CORRECT regarding the Availability Zone (AZ) specific characteristics of Amazon Elastic Block Store (EBS) and Amazon Elastic File System (Amazon EFS) storage types?

A) EBS volume can be attached to one or more instances in multiple Availability Zones (AZ) and EFS file system can be mounted on instances in the same Availability Zone (AZ)
B) EBS volume can be attached to a single instance in the same Availability Zone (AZ) whereas EFS file system can be mounted on instances across multiple Availability Zones (AZ)
C) EBS volume can be attached to a single instance in the same Availability Zone (AZ) and EFS file system can only be mounted on instances in the same Availability Zone (AZ)
D) EBS volume can be attached to one or more instances in multiple Availability Zones (AZ) and EFS file system can be mounted on instances across multiple Availability Zones (AZ)

---

### Q36
A startup wants to provision an EC2 instance for the lowest possible cost for a long-term duration but needs to make sure that the instance would never be interrupted. As a Cloud Practitioner, which of the following options would you recommend?

A) EC2 On-Demand Instance
B) EC2 Spot Instance
C) EC2 Reserved Instance (RI)
D) EC2 Dedicated Host

---

### Q37
A multi-national company has just moved its infrastructure from its on-premises data center to AWS Cloud. As part of the shared responsibility model, AWS is responsible for which of the following?

A) Service and Communications Protection or Zone Security
B) Physical and Environmental controls
C) Patching guest OS
D) Configuring customer applications

---

### Q38 (Select TWO)
An IT company is planning to migrate from an on-premises environment to AWS Cloud. Which of the following expense areas would result in cost savings when the company moves to AWS Cloud?

A) Data center physical security expenditure
B) Project manager salary
C) SaaS application license fee
D) Developer salary
E) Data center hardware infrastructure expenditure

---

### Q39
A startup wants to set up its IT infrastructure on AWS Cloud. The CTO would like to get an estimate of the monthly AWS bill based on the AWS services that the startup wants to use. As a Cloud Practitioner, which AWS service would you suggest for this use-case?

A) AWS Pricing Calculator
B) AWS Budgets
C) AWS Cost & Usage Report (AWS CUR)
D) AWS Cost Explorer

---

### Q40 (Select TWO)
Which of the following are correct statements regarding the AWS Global Infrastructure?

A) Each AWS Region consists of a minimum of three Availability Zones (AZ)
B) Each Availability Zone (AZ) consists of two or more discrete data centers
C) Each AWS Region consists of two or more Edge Locations
D) Each AWS Region consists of a minimum of two Availability Zones (AZ)
E) Each Availability Zone (AZ) consists of one or more discrete data centers

---

### Q41
A unicorn startup is building an analytics application with support for a speech-based interface. The application will accept speech-based input from users and then convey results via speech. As a Cloud Practitioner, which solution would you recommend for the given use-case?

A) Use Amazon Translate to convert speech to text for downstream analysis. Then use Amazon Polly to convey the text results via speech
B) Use Amazon Transcribe to convert speech to text for downstream analysis. Then use Amazon Polly to convey the text results via speech
C) Use Amazon Polly to convert speech to text for downstream analysis. Then use Amazon Transcribe to convey the text results via speech
D) Use Amazon Polly to convert speech to text for downstream analysis. Then use Amazon Translate to convey the text results via speech

---

### Q42
Compared to the on-demand instance prices, what is the highest possible discount offered for spot instances?

A) 50
B) 90
C) 10
D) 75

---

### Q43
A big data analytics company is moving its IT infrastructure from an on-premises data center to AWS Cloud. The company has some server-bound software licenses that it wants to use on AWS. As a Cloud Practitioner, which of the following EC2 instance types would you recommend to the company?

A) Reserved Instance (RI)
B) Dedicated Host
C) On-Demand Instance
D) Dedicated Instance

---

### Q44
Which of the following AWS services has encryption enabled by default?

A) Amazon Elastic Block Store (Amazon EBS)
B) Amazon Relational Database Service (Amazon RDS)
C) AWS CloudTrail Logs
D) Amazon Elastic File System (Amazon EFS)

---

### Q45 (Select THREE)
Which of the following are the advantages of cloud computing?

A) Allocate a few months of planning for your infrastructure capacity needs
B) Trade variable expense for capital expense
C) Trade capital expense for variable expense
D) Benefit from massive economies of scale
E) Spend money on building and maintaining data centers
F) Go global in minutes and deploy applications in multiple regions around the world with just a few clicks

---

### Q46 (Select TWO)
A startup wants to migrate its data and applications from the on-premises data center to AWS Cloud. Which of the following options can be used by the startup to help with this migration?

A) Consult moderators on AWS Developer Forums
B) Leverage AWS Professional Services to accelerate the infrastructure migration
C) Utilize AWS Partner Network (APN) to build a custom solution for this infrastructure migration
D) Use AWS Trusted Advisor to automate the infrastructure migration
E) Raise a support ticket with AWS Support for further assistance

---

### Q47
Under the AWS Shared Responsibility Model, which of the following is a shared responsibility of both AWS and the customer?

A) Infrastructure maintenance of Amazon Simple Storage Service (Amazon S3) storage servers
B) Configuration Management
C) Availability Zone (AZ) infrastructure maintenance
D) Guarantee data separation among various AWS customers

---

### Q48
An e-commerce company has deployed an RDS database in a single Availability Zone (AZ). The engineering team wants to ensure that in case of an AZ outage, the database should continue working on the same endpoint without any manual administrative intervention. Which of the following solutions can address this use-case?

A) Deploy the database via AWS Elastic Beanstalk
B) Provision the database via AWS CloudFormation
C) Configure the database in RDS read replica mode with automatic failover to the standby
D) Configure the database in RDS Multi-AZ deployment with automatic failover to the standby

---

### Q49
A multi-national corporation wants to get expert professional advice on migrating to AWS and managing their applications on AWS Cloud. Which of the following entities would you recommend for this engagement?

A) APN Technology Partner
B) AWS Trusted Advisor
C) APN Consulting Partner
D) Concierge Support Team

---

### Q50 (Select TWO)
An organization needs to securely access AWS services and establish private connectivity between its Virtual Private Clouds (VPCs) and supported AWS services without using the public internet. Which AWS services can meet this requirement?

A) Amazon Connect
B) AWS Transit Gateway
C) Amazon Inspector
D) AWS PrivateLink
E) AWS Internet Gateway

---

### Q51
A financial services company wants to ensure that its AWS account activity meets the governance, compliance and auditing norms. As a Cloud Practitioner, which AWS service would you recommend for this use-case?

A) AWS Config
B) AWS CloudTrail
C) Amazon CloudWatch
D) AWS Trusted Advisor

---

### Q52
A company uses reserved EC2 instances across multiple units with each unit having its own AWS account. However, some of the units under-utilize their reserved instances while other units need more reserved instances. As a Cloud Practitioner, which of the following would you recommend as the most cost-optimal solution?

A) Use AWS Trusted Advisor to manage AWS accounts of all units and then share the reserved EC2 instances amongst all units
B) Use AWS Systems Manager to manage AWS accounts of all units and then share the reserved EC2 instances amongst all units
C) Use AWS Organizations to manage AWS accounts of all units and then share the reserved EC2 instances amongst all units
D) Use AWS Cost Explorer to manage AWS accounts of all units and then share the reserved EC2 instances amongst all units

---

### Q53
A company wants to have control over creating and using its own keys for encryption on AWS services. Which of the following can be used for this use-case?

A) AWS managed key
B) AWS Secrets Manager
C) customer managed key (CMK)
D) AWS owned key

---

### Q54
A data analytics company is running a proprietary batch analytics application on AWS and wants to use a storage service which would be accessed by hundreds of EC2 instances simultaneously to append data to existing files. As a Cloud Practitioner, which AWS service would you suggest for this use-case?

A) Amazon Simple Storage Service (Amazon S3)
B) Amazon Elastic Block Store (Amazon EBS)
C) Instance Store
D) Amazon Elastic File System (Amazon EFS)

---

### Q55 (Select TWO)
Which of the following AWS Support plans provide access to only core checks from the AWS Trusted Advisor Best Practice Checks?

A) AWS Enterprise Support
B) AWS Enterprise On-Ramp Support
C) AWS Basic Support
D) AWS Business Support
E) AWS Developer Support

---

### Q56 (Select TWO)
Which of the following are the storage services offered by the AWS Cloud?

A) Amazon Simple Notification Service (SNS)
B) Amazon Elastic Compute Cloud (Amazon EC2)
C) Amazon Elastic File System (Amazon EFS)
D) Amazon Simple Queue Service (SQS)
E) Amazon Simple Storage Service (Amazon S3)

---

### Q57
Which of the following is an INCORRECT statement about Scaling, a design principle of Reliability pillar of the AWS Well-Architected Framework?

A) A scale up operation implies you scale by adding more power (CPU, RAM) to your existing machine/node
B) Fault tolerance is achieved by a scale up operation
C) A scale out operation implies you scale by adding more instances to your existing pool of resources
D) Fault tolerance is achieved by a scale out operation

---

### Q58
A company runs an application on a fleet of EC2 instances. The company wants to automate the traditional maintenance job of running timely assessments and checking for OS vulnerabilities. As a Cloud Practitioner, which service will you suggest for this use case?

A) Amazon Macie
B) Amazon Inspector
C) AWS Shield
D) Amazon GuardDuty

---

### Q59
An organization is currently operating MySQL databases on its own on-premises servers. To reduce the operational burden of database maintenance and management, the organization wants to move to a fully managed AWS database offering.

Which migration strategy best aligns with this goal?

A) Repurchase
B) Replatform
C) Rehost
D) Refactor

---

### Q60
An intern at an IT company provisioned a Linux based On-demand EC2 instance with per-second billing but terminated it within 30 seconds as he wanted to provision another instance type. What is the duration for which the instance would be charged?

A) 300 seconds
B) 30 seconds
C) 600 seconds
D) 60 seconds

---

### Q61 (Select TWO)
What are the advantages that AWS Cloud offers over a traditional on-premises IT infrastructure?

A) Trade capital expense for variable expense
B) Eliminate guessing on your infrastructure capacity needs
C) Make a capacity decision before deploying an application, to reduce costs
D) Increase speed and agility by keeping servers and other required resources ready before time in your data centers
E) Provide lower latency to applications by maintaining servers on-premises

---

### Q62
Which tool/service will help you access AWS services using programming language-specific APIs?

A) AWS Management Console
B) Integrated Development Environments (IDE)
C) AWS Software Developer Kit (SDK)
D) AWS Command Line Interface (CLI)

---

### Q63
A research group wants to use EC2 instances to run a scientific computation application that already has a fault tolerant architecture. The application needs high-performance hardware disks that provide fast I/O performance. As a Cloud Practitioner, which of the following storage options would you recommend as the MOST cost-effective solution?

A) Amazon Elastic File System (Amazon EFS)
B) Amazon Simple Storage Service (Amazon S3)
C) Instance Store
D) Amazon Elastic Block Store (EBS)

---

### Q64 (Select TWO)
Which of the following AWS Support plans provide access to guidance, configuration, and troubleshooting of AWS interoperability with third-party software?

A) AWS Basic Support
B) AWS Enterprise Support
C) AWS Developer Support
D) AWS Corporate Support
E) AWS Business Support

---

### Q65
Which AWS Service can be used to mitigate a Distributed Denial of Service (DDoS) attack?

A) AWS Shield
B) AWS Systems Manager
C) Amazon CloudWatch
D) AWS Key Management Service (AWS KMS)

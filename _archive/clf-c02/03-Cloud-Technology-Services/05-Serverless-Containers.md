---
tags:
  - aws
  - cloud-practitioner
  - technology
  - lambda
  - serverless
  - containers
domain: Cloud Technology and Services
aliases:
  - "Lambda"
  - "ECS"
  - "Fargate"
  - "Serverless"
  - "Containers"
  - "API Gateway"
  - "EKS"
status: not-started
date: 2026-07-01
---

# Serverless & Container Services

## Docker & Containers

- Docker = standardized way to package applications into containers
- Containers are isolated; run the same way on any machine
- AWS container services: ECS, EKS, Fargate, ECR

---

## Amazon ECS (Elastic Container Service)

- Run **Docker containers** on AWS
- You provision and maintain the **EC2 infrastructure** (your responsibility)
- AWS manages container scheduling and placement
- Integrates with ALB for load balancing

---

## AWS Fargate

- Run Docker containers **without managing servers**
- **Serverless** — no EC2 instances to manage
- AWS runs containers based on required CPU/RAM
- Fargate automatically scales with your containers

| Feature | ECS | Fargate |
|---|---|---|
| Infrastructure | You manage EC2 | AWS manages (serverless) |
| Control | More control | Less control, simpler |
| Cost | Pay for EC2 | Pay per container resource usage |

---

## Amazon ECR (Elastic Container Registry)

- **Private Docker image registry** on AWS
- Store, manage, and deploy container images
- Integrated with ECS and EKS

---

## Amazon EKS (Elastic Kubernetes Service)

- Managed **Kubernetes** on AWS
- For organizations already using Kubernetes
- Kubernetes is cloud-agnostic (can migrate between clouds)

---

## AWS Lambda

- **Serverless functions** — run code without provisioning servers
- **Event-driven** — executes in response to triggers
- Pay per call and per duration of execution

### Lambda Characteristics

| Property | Limit/Detail |
|---|---|
| Max execution time | **15 minutes** |
| Max RAM | 10 GB |
| Languages | Python, Node.js, Java, C#, Go, Ruby, PowerShell, custom runtime |
| Scaling | Automatic; unlimited concurrent executions |

### Lambda Pricing
- **Requests**: $0.20 per 1 million requests (first 1M free)
- **Duration**: $0.0000166667 per GB-second (400,000 GB-seconds free per month)

### Lambda Event Triggers
- API Gateway, S3, DynamoDB, Kinesis, SNS, SQS, EventBridge, CloudWatch, Cognito, and more

> [!tip]
> Lambda is ideal for: short tasks (< 15 min), event-driven processing, sporadic workloads, microservices. It's the definition of serverless on AWS.

---

## Amazon API Gateway

- **Managed serverless REST/WebSocket API** creation service
- Expose Lambda functions as REST APIs to the web
- Scales automatically; no infrastructure to manage
- Supports: REST APIs, HTTP APIs, WebSocket APIs
- Use with: Lambda, EC2, any HTTP endpoint

---

## AWS Batch

- **Managed batch processing** at any scale
- Dynamically provisions EC2 or Spot instances to run batch jobs
- Runs **Docker images** on ECS
- No time limit (unlike Lambda's 15 min)
- Scheduled or event-triggered

| Service | Duration | Infrastructure |
|---|---|---|
| Lambda | Max 15 min | Serverless |
| Batch | Unlimited | EC2/Spot (managed) |

---

## Amazon Lightsail

- **Virtual servers, storage, databases, and networking** for beginners
- Simplified interface with low, predictable prices
- Ideal for: simple web apps, WordPress, small databases, development environments
- Less flexibility than EC2 but much easier to use
- Limited AWS integrations

---

## Compute Services Comparison

| Service | Use Case | Notes |
|---|---|---|
| EC2 | General-purpose VMs | Full control; any workload |
| Lambda | Short serverless functions | < 15 min; event-driven |
| ECS | Docker on EC2 | You manage EC2 |
| Fargate | Serverless Docker | AWS manages infrastructure |
| Batch | Long-running batch jobs | No time limit; Docker |
| Lightsail | Beginner simple apps | Low cost; limited features |
| LightSail | WordPress/simple web | Predictable pricing |

---

## Exam Tips

> [!tip]
> - Lambda = serverless functions; event-driven; max 15 min; pay per call + duration
> - Fargate = serverless containers (no EC2 to manage)
> - ECS = Docker on EC2 (you manage EC2)
> - Batch = long-running batch jobs (not limited to 15 min like Lambda)
> - Lightsail = beginner/simple apps; low price; not for complex architectures

> [!warning]
> Lambda max duration is **15 minutes**. If a task needs longer → use Batch, ECS, or EC2.

## Related Notes
- [[06-Monitoring-Management]]
- [[07-Application-Integration]]
- [[08-Infrastructure-as-Code]]

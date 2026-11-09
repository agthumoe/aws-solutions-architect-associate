---
tags:
  - aws
  - cloud-practitioner
  - billing
  - pricing
domain: Billing, Pricing, and Support
aliases:
  - "EC2 Pricing"
  - "On-Demand"
  - "Reserved Instances"
  - "Spot Instances"
  - "Savings Plans"
  - "Free Tier"
status: not-started
date: 2026-07-01
---

# AWS Pricing Models

## AWS Pricing Fundamentals

AWS has 4 pricing principles:

1. **Pay as you go** — no upfront cost; no long-term commitment
2. **Save when you reserve** — reserved capacity = discounts
3. **Pay less by using more** — volume discounts (S3, data transfer)
4. **Pay less as AWS grows** — economies of scale passed to customers

---

## EC2 Pricing Options

### On-Demand
- Pay per second (Linux/Windows) or per hour (other OS)
- No long-term commitment; highest cost
- Best for: short-term, unpredictable workloads

### Reserved Instances (1 or 3 years)
- Up to **72% discount** vs On-Demand
- **Standard**: fixed instance type (higher discount)
- **Convertible**: can change type, family, OS (up to 66% discount)
- Payment options: No Upfront | Partial Upfront | All Upfront (more upfront = more discount)
- **3 years** > **1 year** in terms of discount

### EC2 Savings Plans (1 or 3 years)
- Commit to a **specific $ amount per hour** (e.g., $10/hour)
- Locked to **instance family and region** (e.g., M5 in us-east-1)
- Flexible across: instance size, OS, tenancy
- Usage beyond the commitment billed at On-Demand rates

### Spot Instances
- Up to **90% discount** — bid on unused EC2 capacity
- Can be **terminated with 2-minute notice** if AWS needs the capacity back
- Best for: batch jobs, data analysis, image processing, flexible workloads
- **NOT suitable** for critical or time-sensitive workloads

### Dedicated Hosts
- Physical server dedicated to you
- Required for BYOL or strict compliance
- Most expensive option
- On-Demand or Reserved pricing

### Capacity Reservations
- Reserve capacity in a specific AZ; no time commitment
- No discount — billed at On-Demand rate
- Guarantees capacity is available when needed

---

## Compute Savings Plans vs EC2 Reserved Instances

| Feature | EC2 Reserved Instances | EC2 Savings Plans | Compute Savings Plans |
|---|---|---|---|
| Commitment | Specific instance type + region + OS | Specific instance family + region | Any EC2, Lambda, Fargate |
| Flexibility | Low | Medium | Highest |
| Discount | Up to 72% | Up to 72% | Up to 66% |

---

## S3 Pricing Factors

1. **Storage** — how many GB stored (depends on storage class)
2. **Requests** — GET, PUT, COPY, POST, LIST
3. **Data Transfer OUT** — data going out of S3 to the internet
4. **Data Transfer IN** — **FREE**
5. **Transfer Acceleration** — additional fee
6. **Replication** — additional storage and data transfer fees

---

## AWS Free Tier

Three types of free offerings:

| Type | Duration | Examples |
|---|---|---|
| **Always Free** | Forever | Lambda (1M requests/month), DynamoDB (25 GB), CloudWatch (10 metrics) |
| **12-Month Free** | First 12 months after sign-up | EC2 t2.micro (750h/month), S3 (5 GB Standard), RDS (750h/month) |
| **Trials** | Short-term | SageMaker (2 months), Comprehend Medical, etc. |

> [!tip]
> EC2 Free Tier = t2.micro (or t3.micro in regions without t2.micro), 750 hours/month for 12 months.

---

## Savings Plans

Three types:

| Type | Applies To | Discount |
|---|---|---|
| **EC2 Instance Savings Plan** | Specific instance family + region | Up to 72% |
| **Compute Savings Plan** | Any EC2, Lambda, Fargate; any region | Up to 66% |
| **SageMaker Savings Plan** | SageMaker | Up to 64% |

---

## Pricing Calculator

- **AWS Pricing Calculator**: estimate the cost of your AWS architecture BEFORE deploying
  - URL: calculator.aws
  - Create estimates; share via URL
  - Use to plan budgets and compare options

---

## Total Cost of Ownership (TCO)

- Compare on-premises vs AWS costs
- AWS TCO advantages: no hardware, no data center, pay for what you use
- **AWS Pricing Calculator** can model TCO comparison

---

## Exam Tips

> [!tip]
> - Spot = cheapest (90% off); can be interrupted — for tolerant workloads
> - Reserved = long-term predictable (databases); 1 or 3 years
> - Savings Plans = commit to $/hour; more flexible than Reserved
> - On-Demand = highest cost; most flexible
> - Data transfer IN = FREE; transfer OUT = charged
> - AWS Free Tier has 3 types: always-free, 12-month, trial

> [!warning]
> Reserved Instances vs Savings Plans: Reserved locks you to a specific instance type+region. Savings Plans commit you to a $/hour spend — more flexible.

## Related Notes
- [[02-Cost-Management-Tools]]
- [[03-Support-Plans]]

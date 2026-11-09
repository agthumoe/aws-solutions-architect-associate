---
tags:
  - aws
  - cloud-practitioner
  - technology
  - ec2
  - compute
domain: Cloud Technology and Services
aliases:
  - "EC2"
  - "Elastic Compute Cloud"
  - "Instance Types"
  - "ELB"
  - "ASG"
  - "Load Balancer"
  - "Auto Scaling"
status: not-started
date: 2026-07-01
---

# Amazon EC2

## What is EC2?

**EC2 = Elastic Compute Cloud** = Infrastructure as a Service (IaaS)

Capabilities:
- Rent virtual machines (EC2 instances)
- Store data on virtual drives (EBS)
- Distribute load across machines (ELB)
- Scale services using auto-scaling (ASG)

---

## EC2 Configuration Options

| Option | Details |
|---|---|
| Operating System | Linux, Windows, Mac OS |
| CPU | Number of cores |
| RAM | Memory |
| Storage | Network-attached (EBS/EFS) or hardware (Instance Store) |
| Network | Speed, public IP |
| Firewall | Security groups |
| Bootstrap script | EC2 User Data |

### EC2 User Data
- Script that runs **once at first start** of the instance
- Used to: install updates, install software, download files
- Runs with **root user** privileges

---

## EC2 IP Addressing

| IP Type | Description | Cost |
|---|---|---|
| **Private IP** | Assigned from subnet; used for internal communication; stays the same across restarts | Free |
| **Public IP** | Optional; required to communicate with the internet; **changes on restart** | Free |
| **Elastic IP** | Static, fixed public IPv4 address you own; persists across restarts | $0.005/hour (~$4/month); free only while associated with a running instance |

- Max **5 Elastic IPs per region** (can request increase)
- Attach Elastic IP to one instance at a time
- Use Elastic IP when you need a fixed IP that survives instance stops/restarts

---

## EC2 Instance Types

Naming convention: `m5.2xlarge` = m (class) + 5 (generation) + 2xlarge (size)

| Type | Optimized For | Use Cases |
|---|---|---|
| **General Purpose** (t, m) | Balanced CPU/Memory/Networking | Web servers, code repos; t2.micro |
| **Compute Optimized** (c) | High-performance processors | Batch, media transcoding, HPC, ML, gaming |
| **Memory Optimized** (r, x, z) | Large data sets in memory | High-perf DB, in-memory cache, real-time BI |
| **Storage Optimized** (i, d, h) | High sequential read/write | OLTP, NoSQL DB, data warehousing, Redis cache |

---

## Security Groups

- Fundamental network security for EC2 — acts as a **firewall**
- **Stateful** — return traffic automatically allowed
- **Allow rules only** (no deny rules)
- All **inbound blocked** by default; all **outbound allowed** by default
- Locked to a **region/VPC combination**
- Lives "outside" EC2 — blocked traffic never reaches the instance

> [!warning]
> "Application timeout" = Security Group issue. "Connection refused" = application error (traffic reached the instance but app rejected it).

---

## EC2 Purchasing Options

### On-Demand
- Pay per second (Linux/Windows) or per hour (other OS)
- **Highest cost**, no upfront, no commitment
- Best for: short-term, unpredictable workloads

### Reserved Instances (1 or 3 years)
- Up to **72% discount** vs On-Demand
- Reserve specific: instance type, region, OS, tenancy
- Payment options: No Upfront (+), Partial Upfront (++), All Upfront (+++)
- 3 years = more discount than 1 year
- **Standard**: fixed instance type
- **Convertible**: can change instance type, family, OS, scope (up to 66% discount)
- Can buy/sell in Reserved Instance Marketplace

### Savings Plans (1 or 3 years)
- Up to **72% discount** — commit to a **dollar amount per hour**
- Locked to instance family and AWS Region
- Flexible across: instance size, OS, tenancy

### Spot Instances
- Up to **90% discount** — most cost-efficient
- Can be **terminated** at any time if spot price exceeds your max price
- Best for: batch jobs, data analysis, image processing, flexible workloads
- **NOT suitable** for critical jobs or databases

### Dedicated Host
- Physical server **fully dedicated** to your use
- Supports: compliance requirements, BYOL (Bring Your Own License)
- Purchasing: On-Demand or Reserved (1/3 years)
- **Most expensive option**

### Dedicated Instance
- Hardware dedicated to your account
- May share hardware with other instances in **same account**
- No control over instance placement

### Capacity Reservations
- Reserve capacity in a **specific AZ** for any duration
- No time commitment (create/cancel anytime)
- **No billing discount** — billed at On-Demand rate whether you use it or not

---

## Purchasing Option Summary (Hotel Analogy)

| Option | Analogy |
|---|---|
| On-Demand | Walk-in rate — pay full price anytime |
| Reserved | Book in advance — great discount for long stay |
| Savings Plans | Pay a certain amount per night for any room type |
| Spot | Bid on empty rooms — can be kicked out anytime |
| Dedicated Host | Book the entire building |
| Capacity Reservation | Book a room but pay even if you don't stay |

---

## Price Comparison (m4.large, us-east-1)

| Purchase Type | Price/Hour |
|---|---|
| On-Demand | $0.10 |
| Reserved Instance (1yr, All Upfront) | $0.058 |
| Reserved Instance (3yr, All Upfront) | $0.037 |
| Spot Instance | $0.038–$0.039 (up to 61% off) |
| Dedicated Host Reservation | Up to 70% off |
| Capacity Reservations | On-Demand price |

---

## AMI (Amazon Machine Image)

- A **customization of an EC2 instance** — includes OS, software, configuration
- Built for a **specific region** (can be copied across regions)
- Types: Public AMI (AWS provided), Your own AMI, AWS Marketplace AMI
- AMI process: Launch instance → Customize → Stop → Create AMI → Launch from AMI

### EC2 Image Builder
- Automate creation, maintenance, validation, and testing of EC2 AMIs
- Can run on a schedule
- **Free service** (only pay for underlying resources)

---

## ELB & ASG (Elastic Load Balancing & Auto Scaling)

### Elastic Load Balancer (ELB)
Distribute incoming traffic across multiple EC2 instances.

| Load Balancer | Protocol | Layer | Use Case |
|---|---|---|---|
| **ALB** (Application) | HTTP/HTTPS/gRPC | 7 | Web apps; URL-based routing; static DNS |
| **NLB** (Network) | TCP/UDP | 4 | Extreme performance; static IP |
| **GWLB** (Gateway) | GENEVE | 3 | Security appliances (firewall, IDS/IPS) |
| **CLB** (Classic) | HTTP/TCP | 4/7 | Old; deprecated |

### Auto Scaling Group (ASG)
- Automatically **scale out** (add EC2) or **scale in** (remove EC2) based on load
- Ensures min/max/desired number of instances
- Automatically replaces unhealthy instances
- **Free service** (pay only for EC2 instances created)

#### ASG Scaling Policies
| Policy | Description |
|---|---|
| **Target Tracking** | Maintain a CloudWatch metric at a target value (e.g., keep CPU at 50%) |
| **Step Scaling** | Custom scaling rules based on metric thresholds; more fine-grained control |
| **Scheduled Scaling** | Scale based on date/time (e.g., add capacity every weekday at 9 AM) |
| **Predictive Scaling** | ML-powered; analyzes 2 weeks of historical data to forecast the next 48 hours |

> [!tip]
> Target Tracking = simplest ("keep CPU at 60%"). Predictive = ML-based ("forecast next 2 days from 2 weeks of data").

---

## Exam Tips

> [!tip]
> - On-Demand = highest cost, most flexible
> - Spot = cheapest (90% off), can be interrupted — use for batch/tolerant workloads
> - Reserved = long-term predictable workloads (databases)
> - Dedicated Host = BYOL compliance; most expensive
> - Savings Plans = commit to $/hour amount; flexible across instance sizes
> - ALB = Layer 7 (HTTP); NLB = Layer 4 (TCP/UDP, highest performance)

## Related Notes
- [[02-Storage-S3-EBS-EFS]]
- [[05-Serverless-Containers]]

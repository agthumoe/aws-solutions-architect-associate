---
tags:
  - aws
  - cloud-practitioner
  - security
  - vpc
  - networking
domain: Security and Compliance
aliases:
  - "VPC"
  - "Security Groups"
  - "NACLs"
  - "Network Security"
  - "Shield"
  - "WAF"
status: not-started
date: 2026-07-01
---

# Network Security — VPC, Security Groups, NACLs

## Amazon VPC (Virtual Private Cloud)

A **VPC** is a logically isolated section of the AWS cloud where you launch resources in a virtual network you define.
- VPC is **region-scoped**
- You control IP address range, subnets, route tables, and gateways

---

## Subnets

| Subnet Type | Access | Use Case |
|---|---|---|
| **Public Subnet** | Accessible from the internet | Web servers, load balancers |
| **Private Subnet** | No direct internet access | Databases, application servers |

### Private CIDR Ranges (Reserved for Private Networks)
| CIDR Block | IP Range | # Hosts |
|---|---|---|
| `10.0.0.0/8` | 10.0.0.0 – 10.255.255.255 | 16,777,216 |
| `172.16.0.0/12` | 172.16.0.0 – 172.31.255.255 | 1,048,576 |
| `192.168.0.0/16` | 192.168.0.0 – 192.168.255.255 | 65,536 |

VPCs use these private IP ranges. Traffic within these ranges stays inside the private network.

---

## Route Tables

- Define rules (routes) that determine where **network traffic is directed**
- Each subnet must be associated with exactly **one route table**
- Common routes: local (VPC-internal), internet-bound (via IGW), private (via VPC peering or TGW)
- Default route table allows all local VPC traffic; add a `0.0.0.0/0 → IGW` route to make a subnet public

---

## Internet Gateway (IGW)

- Connects a **public subnet** to the internet
- Attached to the VPC
- Required for public instances to send/receive traffic from the internet

---

## NAT Gateway / NAT Instance

Allow instances in **private subnets** to access the internet (for updates) without being publicly accessible:
- **NAT Gateway** — AWS managed; highly available; preferred
- **NAT Instance** — Self-managed; older approach

---

## Security Controls

### Security Groups (Stateful)
- Acts as a **firewall at the EC2 instance level**
- **Stateful** — return traffic is automatically allowed
- **Allow rules only** (no deny rules)
- All inbound traffic **blocked by default**; all outbound traffic **allowed by default**
- Can be attached to multiple instances
- Locked to a region/VPC combination

### Network ACLs / NACLs (Stateless)
- Firewall at the **subnet level**
- **Stateless** — must explicitly allow both inbound AND outbound
- Supports both **Allow and Deny** rules
- Rules are evaluated in order (lowest number first)
- Default NACL: allows all traffic

| Feature | Security Group | NACL |
|---|---|---|
| Level | Instance | Subnet |
| Stateful/Stateless | Stateful | Stateless |
| Rules | Allow only | Allow and Deny |
| Default | Block inbound, allow outbound | Allow all |

> [!warning]
> Security Groups = stateful (response automatically allowed). NACLs = stateless (must set both inbound and outbound rules). This is a very common exam gotcha.

---

## VPC Connectivity

### VPC Peering
- Connect two VPCs privately (same or different accounts/regions)
- Must have **non-overlapping CIDR ranges**
- **Not transitive** — if A↔B and B↔C, A cannot reach C automatically

### VPC Endpoints
Allow private connection to AWS services **without going through the internet**:
- **Gateway Endpoint** — for S3 and DynamoDB (free)
- **Interface Endpoint (PrivateLink)** — for other AWS services (uses ENI with private IP)

### VPC Flow Logs
- Capture IP traffic information going in and out of network interfaces
- Stored in S3 or CloudWatch Logs
- Used for troubleshooting connectivity issues

---

## AWS Site-to-Site VPN

- Connect on-premises network to VPC over the **public internet** using **IPsec** encryption
- Set up in minutes; encrypted; goes over public internet

## AWS Direct Connect

- **Private, dedicated, physical** connection between on-premises and AWS
- More consistent bandwidth; no internet variability
- Takes longer to set up (weeks to months); more expensive

| Feature | Site-to-Site VPN | Direct Connect |
|---|---|---|
| Connection | Over internet (encrypted) | Private dedicated line |
| Speed | Variable | Consistent |
| Setup time | Minutes | Weeks/months |
| Cost | Lower | Higher |

---

## DDoS Protection

### AWS Shield
| Tier | Cost | Protection |
|---|---|---|
| **Shield Standard** | Free; automatic | SYN/UDP floods, reflection attacks; Layer 3/4 |
| **Shield Advanced** | $3,000/month | Premium DDoS protection; 24/7 DDoS response team; EC2, ELB, CloudFront, Route 53 |

### AWS WAF (Web Application Firewall)
- Protect web applications from common web exploits
- Operates at **Layer 7 (HTTP)**
- Filter by: IP addresses, HTTP headers, HTTP body, URI strings
- Protects against: SQL injection, Cross-Site Scripting (XSS)
- Deploy on: ALB, API Gateway, CloudFront

> [!tip]
> DDoS protection = Shield. Web exploit protection (SQL injection, XSS) = WAF.

---

## Classic Ports to Know

| Port | Protocol | Use |
|---|---|---|
| 22 | SSH | Log into Linux instance |
| 21 | FTP | Upload files to file share |
| 22 | SFTP | Upload files using SSH |
| 80 | HTTP | Unsecured websites |
| 443 | HTTPS | Secured websites |
| 3389 | RDP | Log into Windows instance |

---

## Exam Tips

> [!tip]
> - Security Groups = EC2 level, stateful, allow only
> - NACLs = subnet level, stateless, allow + deny
> - VPC Endpoints = private access to AWS services without internet
> - Direct Connect = private dedicated line (consistent bandwidth)
> - Shield Standard = free, automatic DDoS protection
> - WAF = Layer 7; blocks SQL injection, XSS

## Related Notes
- [[01-IAM]]
- [[04-Data-Protection-Encryption]]
- [[05-Compliance-Governance]]

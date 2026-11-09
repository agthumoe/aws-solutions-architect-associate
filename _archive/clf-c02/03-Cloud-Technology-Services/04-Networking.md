---
tags:
  - aws
  - cloud-practitioner
  - technology
  - networking
  - route53
  - cloudfront
domain: Cloud Technology and Services
aliases:
  - "Route 53"
  - "CloudFront"
  - "CDN"
  - "Global Accelerator"
  - "Transit Gateway"
  - "DNS"
status: not-started
date: 2026-07-01
---

# Networking — Route 53, CloudFront, and Global Services

## Amazon Route 53

- **Managed DNS** (Domain Name System) service
- DNS translates human-readable domain names into IP addresses

### Common DNS Record Types

| Record | Maps | Example |
|---|---|---|
| **A** | hostname → IPv4 | www.example.com → 12.34.56.78 |
| **AAAA** | hostname → IPv6 | www.example.com → 2001:db8::1 |
| **CNAME** | hostname → hostname | search.example.com → www.example.com |
| **Alias** | hostname → AWS resource | app.example.com → ALB DNS name |

### Route 53 Routing Policies

| Policy | Description |
|---|---|
| **Simple** | Single resource; no health checks |
| **Weighted** | Split traffic by percentage (e.g., 70%/20%/10%) |
| **Latency** | Route to lowest latency region |
| **Failover** | Primary/failover with health checks; disaster recovery |

> [!tip]
> Route 53 is a **Global** service (like IAM). Supports domain registration, DNS routing, and health checking.

---

## Amazon CloudFront

- **Content Delivery Network (CDN)**
- Caches content at **Edge Locations** worldwide (400+)
- Improves read performance and user experience
- Built-in **DDoS protection** via integration with Shield and WAF

### CloudFront Origins

| Origin Type | Examples |
|---|---|
| **S3 Bucket** | Static files; use OAC (Origin Access Control) for security |
| **VPC Origin** | Private ALB/NLB/EC2 in VPC private subnets |
| **Custom HTTP Origin** | Any public HTTP endpoint; EC2, ALB, S3 static website |

---

## AWS Global Accelerator

- Improves performance using the **AWS global private network**
- Creates **2 static Anycast IP addresses** for your application
- Routes traffic through Edge Locations → private AWS backbone → application
- ~60% improvement in performance

### CloudFront vs Global Accelerator

| Feature | CloudFront | Global Accelerator |
|---|---|---|
| Protocol | HTTP/HTTPS (cacheable) | TCP/UDP (any) |
| Caching | Yes — at the edge | No — proxying packets |
| Use case | Static content, images, videos | Dynamic content, gaming, IoT |
| IPs | Dynamic per edge location | 2 static Anycast IPs |
| DDoS | Yes (Shield) | Yes (Shield) |

---

## AWS Outposts

- **AWS rack in your on-premises data center**
- AWS delivers and installs hardware
- Same AWS services, APIs, and tools on-premises
- Lower latency for on-premises applications
- **Customer is physically responsible** for the Outpost hardware
- Good for: data residency requirements, low-latency local processing

---

## AWS WaveLength

- Extends AWS infrastructure to **5G networks**
- Deploy AWS compute and storage at the edge of 5G carrier networks
- Ultra-low latency to mobile devices (milliseconds)
- Use for: connected vehicles, smart cities, AR/VR, real-time gaming

---

## AWS Local Zones

- **Extension of an AWS Region** to specific geographic locations (closer to end users)
- Run latency-sensitive applications closer to large population centers
- Example: Los Angeles Local Zone attached to us-west-2 region

---

## S3 Transfer Acceleration

- Increase S3 transfer speed by uploading to an **Edge Location** first
- Edge Location forwards to S3 bucket via fast AWS private network
- Compatible with multi-part upload

---

## Exam Tips

> [!tip]
> - Route 53 = DNS service; global; supports health checks and failover
> - CloudFront = CDN; caches at edge locations; integrates with S3 and ALB
> - Global Accelerator = 2 static IPs; private AWS backbone; TCP/UDP; no caching
> - CloudFront: cacheable content (images, videos). Global Accelerator: dynamic content (APIs, gaming)
> - Outposts = AWS hardware IN your data center
> - Local Zones = closer AWS services for low-latency apps

> [!warning]
> CloudFront ≠ Global Accelerator. CloudFront caches and serves content. Global Accelerator just routes traffic faster without caching.

## Related Notes
- [[01-EC2-Compute]]
- [[06-Monitoring-Management]]

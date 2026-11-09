---
tags: [aws, saa-c03, moc, networking]
domain: Networking & Content Delivery
exam-domains: [1, 2, 3, 4]
aliases:
  - "Networking & Content Delivery MOC"
status: not-started
date: 2026-07-21
---

# Networking & Content Delivery — Cluster MOC

## Key Concepts
This cluster covers DNS, the core AWS networking building block (VPC), and the two AWS global-network acceleration services (CloudFront and Global Accelerator). Together these topics span every exam domain — from foundational connectivity (Domain 1/3) to network security (Domain 2) to cost-optimized data transfer (Domain 4).

## Notes in This Cluster

- [[01-Route53]] — DNS fundamentals, hosted zones, record types, Alias vs CNAME, all Route 53 routing policies (simple, weighted, latency-based, failover, geolocation, geoproximity, IP-based, multi-value), health checks, and hybrid DNS resolver endpoints.
- [[02-VPC]] — The core AWS networking service: CIDR/subnetting, Internet Gateway, NAT Gateway vs NAT Instance, Security Groups vs NACLs, VPC Peering, VPC Endpoints/PrivateLink, VPC Flow Logs, Site-to-Site VPN, Direct Connect, Transit Gateway, IPv6, networking costs, and AWS Network Firewall. The single most heavily tested topic on the SAA-C03.
- [[03-CloudFront-Global-Accelerator]] — CDN fundamentals, CloudFront origins (S3/VPC/custom), cache invalidation, geo restriction, and how CloudFront compares to Global Accelerator's Anycast-IP TCP/UDP acceleration model.

## AWS Services / Features
| Service | One-Line Role |
|---|---|
| Route 53 | Authoritative DNS + domain registration + health checks |
| VPC | Isolated private network foundation for all AWS resources |
| CloudFront | Global CDN — caches content at edge locations |
| Global Accelerator | Anycast-IP proxying over the AWS backbone for TCP/UDP apps |

## Exam Tips
> [!TIP]
> Cross-note connections to watch for in scenario questions: Route 53 **Alias records** can target CloudFront distributions and ALBs (but not raw EC2 DNS names); CloudFront can use **VPC Origins** to reach private ALB/NLB/EC2 resources without exposing them publicly; Global Accelerator's static Anycast IPs are often paired with Route 53 when DNS-level failover isn't fast enough.

> [!WARNING]
> Don't confuse **DNS routing** (Route 53 — responds to queries, doesn't move packets) with **traffic routing** (VPC Route Tables, Global Accelerator — actually directs packets).

## Related Notes
- [[01-Route53]]
- [[02-VPC]]
- [[03-CloudFront-Global-Accelerator]]

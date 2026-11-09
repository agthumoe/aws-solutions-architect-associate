---
tags:
  - aws
  - cloud-practitioner
  - billing
  - support
domain: Billing, Pricing, and Support
aliases:
  - "Support Plans"
  - "TAM"
  - "Trusted Advisor"
  - "Developer Business Enterprise"
  - "Basic Support"
status: not-started
date: 2026-07-01
---

# AWS Support Plans

## Overview

AWS offers 5 support plan tiers:

| Plan | Cost | Who |
|---|---|---|
| **Basic** | Free | All customers |
| **Developer** | $29/month or 3% of monthly AWS charges | Early development/testing |
| **Business** | $100/month or 10%/7%/5% tiered | Production workloads |
| **Enterprise On-Ramp** | $5,500/month or 10% of monthly charges | Business-critical production |
| **Enterprise** | $15,000/month or 10%/7%/5%/3% tiered | Mission-critical production |

---

## Basic Support (Free)

Included with every AWS account:
- **Customer Service**: account questions 24/7
- **Documentation**, whitepapers, support forums
- **AWS Health Dashboard** — service status alerts
- **Trusted Advisor**: 7 core security checks
- No technical support

---

## Developer Support ($29/month or 3%)

Everything in Basic, plus:
- **Email support** during business hours
- 1 primary contact allowed
- Response times:
  - General guidance: < 24 hours
  - System impaired: < 12 hours

---

## Business Support ($100/month or 10%/7%/5%)

Everything in Developer, plus:
- **24/7 phone, email, and chat** support
- **Unlimited contacts**
- **Full Trusted Advisor** checks (125+) + API access
- **Infrastructure Event Management** (for additional fee)
- Response times:
  - General guidance: < 24 hours
  - System impaired: < 12 hours
  - Production system impaired: < 4 hours
  - Production system down: **< 1 hour**

---

## Enterprise On-Ramp Support ($5,500/month or 10%)

Everything in Business, plus:
- Access to a **pool of Technical Account Managers (TAMs)**
- **Concierge Support Team** for billing/account
- **Infrastructure Event Management**, Well-Architected, Operations Reviews
- Response times:
  - Business-critical system down: **< 30 minutes**

---

## Enterprise Support ($15,000/month or 10%/7%/5%/3%)

Everything in Enterprise On-Ramp, plus:
- **Designated Technical Account Manager (TAM)**
- **Concierge Support Team**
- Response times:
  - Business-critical system down: **< 15 minutes**

---

## Response Time Summary

| Severity | Developer | Business | Enterprise On-Ramp | Enterprise |
|---|---|---|---|---|
| General guidance | < 24h | < 24h | < 24h | < 24h |
| System impaired | < 12h | < 12h | < 12h | < 12h |
| Prod system impaired | — | < 4h | < 4h | < 4h |
| Prod system DOWN | — | **< 1h** | **< 1h** | **< 1h** |
| Business-critical down | — | — | **< 30 min** | **< 15 min** |

---

## AWS Trusted Advisor by Plan

| Feature | Basic | Developer | Business | Enterprise |
|---|---|---|---|---|
| Core checks | 7 | 7 | 125+ | 125+ |
| Full checks | ✗ | ✗ | ✓ | ✓ |
| API access | ✗ | ✗ | ✓ | ✓ |
| TAM | ✗ | ✗ | ✗ | ✓ |

---

## AWS Marketplace

- **Digital catalog** of 3rd-party software, services, and data
- Products: AMIs, SaaS products, containers, data products, professional services
- Purchase and deploy directly through AWS Console
- Billing integrated with AWS bill
- Categories: security, networking, storage, ML, IoT, etc.

---

## AWS Partner Network (APN)

| Partner Type | Description |
|---|---|
| **Technology Partners** | Software products (ISVs) that build on or integrate with AWS |
| **Consulting Partners** | Professional services firms that help customers build on AWS |

---

## Exam Tips

> [!tip]
> - Basic = free; 7 Trusted Advisor checks; no technical support
> - Developer = email only; business hours; 1 contact
> - Business = 24/7 phone/chat/email; full Trusted Advisor; < 1h for prod down
> - Enterprise On-Ramp = pool of TAMs; < 30 min for business-critical
> - Enterprise = designated TAM; < 15 min for business-critical
> - "Which plan includes a TAM?" → Enterprise On-Ramp (pool) or Enterprise (dedicated)

> [!warning]
> Developer support has ONLY email (no phone/chat). Business support is first plan with 24/7 phone/chat support.

## Related Notes
- [[01-Pricing-Models]]
- [[02-Cost-Management-Tools]]

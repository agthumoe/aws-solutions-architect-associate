---
tags:
  - aws
  - cloud-practitioner
  - mock-exam
  - results
aliases:
  - "Mock Exam 1 Results"
status: completed
date: 2026-07-12
---

# Mock Exam 1 — Results

Companion answer key to `mock-exam-1.md`. Letters (A/B/C/D/E/F) match the option order in the questions file.

## Score

**49 / 65 correct (75.4%)** — passing score for CLF-C02 is 700/1000 (~72%), so this is right around the line. 16 missed questions below are your highest-value review targets before the exam.

## Answer Key

| Q# | Domain | Your Answer(s) | Correct Answer(s) | Result |
|---|---|---|---|---|
| 1 | Security & Compliance | D | D | ✓ |
| 2 | Security & Compliance | D | B | ✗ |
| 3 | Technology | D | D | ✓ |
| 4 | Technology | C | C | ✓ |
| 5 | Cloud Concepts | C | C | ✓ |
| 6 | Billing & Pricing | A, D, E | D, E, F | ✗ |
| 7 | Security & Compliance | A, C | A, C | ✓ |
| 8 | Technology | B | B | ✓ |
| 9 | Security & Compliance | A, B | B, C | ✗ |
| 10 | Billing & Pricing | D | C | ✗ |
| 11 | Cloud Concepts | C, D | D, E | ✗ |
| 12 | Billing & Pricing | D | D | ✓ |
| 13 | Billing & Pricing | D | D | ✓ |
| 14 | Security & Compliance | D, E | B, D | ✗ |
| 15 | Cloud Concepts | A | A | ✓ |
| 16 | Technology | A | A | ✓ |
| 17 | Technology | B, C | B, E | ✗ |
| 18 | Cloud Concepts | B | B | ✓ |
| 19 | Technology | C | C | ✓ |
| 20 | Cloud Concepts | A, C | A, C | ✓ |
| 21 | Security & Compliance | C | C | ✓ |
| 22 | Technology | A | A | ✓ |
| 23 | Technology | B | B | ✓ |
| 24 | Billing & Pricing | A, D | A, D | ✓ |
| 25 | Billing & Pricing | C | C | ✓ |
| 26 | Technology | B | B | ✓ |
| 27 | Security & Compliance | A | A | ✓ |
| 28 | Cloud Concepts | D | C | ✗ |
| 29 | Security & Compliance | B | B | ✓ |
| 30 | Cloud Concepts | A, E | A, B | ✗ |
| 31 | Technology | B | B | ✓ |
| 32 | Technology | C | C | ✓ |
| 33 | Technology | B | C | ✗ |
| 34 | Security & Compliance | D | D | ✓ |
| 35 | Technology | B | B | ✓ |
| 36 | Billing & Pricing | C | C | ✓ |
| 37 | Cloud Concepts | B | B | ✓ |
| 38 | Cloud Concepts | A, E | A, E | ✓ |
| 39 | Billing & Pricing | A | A | ✓ |
| 40 | Technology | A, E | A, E | ✓ |
| 41 | Technology | C | B | ✗ |
| 42 | Technology | B | B | ✓ |
| 43 | Technology | B | B | ✓ |
| 44 | Security & Compliance | A | C | ✗ |
| 45 | Cloud Concepts | C, D, F | C, D, F | ✓ |
| 46 | Cloud Concepts | B, C | B, C | ✓ |
| 47 | Security & Compliance | B | B | ✓ |
| 48 | Cloud Concepts | D | D | ✓ |
| 49 | Cloud Concepts | D | C | ✗ |
| 50 | Technology | B, D | B, D | ✓ |
| 51 | Cloud Concepts | A | B | ✗ |
| 52 | Security & Compliance | C | C | ✓ |
| 53 | Security & Compliance | B | C | ✗ |
| 54 | Technology | D | D | ✓ |
| 55 | Cloud Concepts | D, E | C, E | ✗ |
| 56 | Technology | C, E | C, E | ✓ |
| 57 | Cloud Concepts | B | B | ✓ |
| 58 | Security & Compliance | B | B | ✓ |
| 59 | Cloud Concepts | B | B | ✓ |
| 60 | Billing & Pricing | D | D | ✓ |
| 61 | Cloud Concepts | A, B | A, B | ✓ |
| 62 | Technology | C | C | ✓ |
| 63 | Technology | C | C | ✓ |
| 64 | Billing & Pricing | B, E | B, E | ✓ |
| 65 | Security & Compliance | A | A | ✓ |

## Missed Questions — Quick Reference (16)

| Q# | Topic | One-line takeaway |
|---|---|---|
| 2 | Shield Standard vs WAF vs Secrets Manager | Free-by-default DDoS protection = **Shield Standard**, not WAF |
| 6 | Reservable AWS services | EC2, RDS, **DynamoDB** support reservations — not DocumentDB |
| 9 | Shield Advanced coverage | Covers **Route 53 + Global Accelerator** (not CloudFormation) |
| 10 | Support plan w/ contextual architectural guidance | **Business**, not Enterprise |
| 11 | CAF platform perspective stakeholders | **CTO + Engineer**, not CIO |
| 14 | VPC Gateway Endpoint services | Only **S3 + DynamoDB** — not EC2 |
| 17 | Decoupling microservices | **SQS + SNS**, not Lambda |
| 28 | Quick iteration / fast feature releases | **Agility**, not Elasticity |
| 30 | CAF responsiveness tasks | Organize around products/value streams + **leverage agile methods** |
| 33 | NoSQL active-active cross-region | DynamoDB **Global Tables**, not DAX |
| 41 | Speech-to-text vs text-to-speech | **Transcribe** = speech→text; Polly = text→speech (you had it backwards) |
| 44 | Encrypted by default | **CloudTrail Logs** are encrypted by default; EBS/RDS/EFS are opt-in |
| 49 | Migration/management consulting | **APN Consulting Partner**, not Concierge Support Team |
| 51 | Governance/compliance/audit of account activity | **CloudTrail** (who did what), not Config |
| 53 | Full control of your own encryption keys | **Customer Managed Key (CMK)**, not Secrets Manager |
| 55 | Support plans with ONLY core Trusted Advisor checks | **Basic + Developer**, not Business |

**Pattern in your misses:** A cluster around **support plan tiers** (Q10, 49, 55), **select-two/three questions where you found one correct answer but missed the second** (Q6, 9, 11, 14, 17, 30, 55 — 7 of your 16 misses), and a few **service mix-ups** (Transcribe/Polly, CloudTrail/Config, Shield coverage list). Worth a fast targeted drill on support plans and re-reading each select-two/three question twice before answering, since you're consistently finding one right answer but stopping short of the second.

---
tags:
  - aws
  - cloud-practitioner
  - mock-exam
  - results
aliases:
  - "Mock Exam 2 Results"
status: completed
date: 2026-07-12
---

# Mock Exam 2 — Results

Companion answer key to `mock-exam-2.md`. Letters (A/B/C/D/E/F) match the option order in the questions file.

## Score

**54 / 65 correct (83.1%)** — passing score for CLF-C02 is 700/1000 (~72%), so this is your strongest result of the three mock exams. 11 missed questions below are your highest-value review targets before the exam.

## Answer Key

| Q# | Domain | Your Answer(s) | Correct Answer(s) | Result |
|---|---|---|---|---|
| 1 | Cloud Concepts | C | C | ✓ |
| 2 | Billing & Pricing | B | B | ✓ |
| 3 | Technology | A, C | A, C | ✓ |
| 4 | Cloud Concepts | C | B | ✗ |
| 5 | Cloud Concepts | D | B | ✗ |
| 6 | Cloud Concepts | C | C | ✓ |
| 7 | Cloud Concepts | A | A | ✓ |
| 8 | Technology | C | C | ✓ |
| 9 | Technology | A, D | A, D | ✓ |
| 10 | Technology | B, C | B, C | ✓ |
| 11 | Technology | C | C | ✓ |
| 12 | Security & Compliance | A | A | ✓ |
| 13 | Technology | A | B | ✗ |
| 14 | Security & Compliance | C | D | ✗ |
| 15 | Technology | A | A | ✓ |
| 16 | Security & Compliance | A | A | ✓ |
| 17 | Technology | C | C | ✓ |
| 18 | Cloud Concepts | B, E | B, E | ✓ |
| 19 | Security & Compliance | C, D | C, D | ✓ |
| 20 | Security & Compliance | D | D | ✓ |
| 21 | Technology | A | A | ✓ |
| 22 | Technology | B | B | ✓ |
| 23 | Cloud Concepts | B | B | ✓ |
| 24 | Technology | B | B | ✓ |
| 25 | Technology | C | C | ✓ |
| 26 | Technology | D | D | ✓ |
| 27 | Cloud Concepts | A | A | ✓ |
| 28 | Technology | C, E | B, C | ✗ |
| 29 | Technology | A | A | ✓ |
| 30 | Cloud Concepts | A | A | ✓ |
| 31 | Security & Compliance | A, F | A, B, F | ✗ |
| 32 | Cloud Concepts | B | B | ✓ |
| 33 | Technology | D | D | ✓ |
| 34 | Technology | B, D, F | B, D, F | ✓ |
| 35 | Billing & Pricing | C | C | ✓ |
| 36 | Technology | A | B | ✗ |
| 37 | Technology | B | B | ✓ |
| 38 | Security & Compliance | C | C | ✓ |
| 39 | Technology | D | D | ✓ |
| 40 | Cloud Concepts | B, C | B, C | ✓ |
| 41 | Technology | A | A | ✓ |
| 42 | Technology | A | A | ✓ |
| 43 | Technology | B | B | ✓ |
| 44 | Security & Compliance | C | C | ✓ |
| 45 | Billing & Pricing | A | A | ✓ |
| 46 | Billing & Pricing | D | D | ✓ |
| 47 | Cloud Concepts | B | B | ✓ |
| 48 | Cloud Concepts | A | A | ✓ |
| 49 | Technology | C, E | C, E | ✓ |
| 50 | Cloud Concepts | B, D | B, E | ✗ |
| 51 | Technology | C | C | ✓ |
| 52 | Security & Compliance | A, B | A, B | ✓ |
| 53 | Security & Compliance | C | C | ✓ |
| 54 | Technology | A | A | ✓ |
| 55 | Technology | C | D | ✗ |
| 56 | Technology | A | A | ✓ |
| 57 | Technology | D | D | ✓ |
| 58 | Technology | A | A | ✓ |
| 59 | Billing & Pricing | D | D | ✓ |
| 60 | Security & Compliance | D | D | ✓ |
| 61 | Technology | A | B | ✗ |
| 62 | Technology | A, D | A, D | ✓ |
| 63 | Technology | C | B | ✗ |
| 64 | Security & Compliance | C | C | ✓ |
| 65 | Billing & Pricing | C | C | ✓ |

## Missed Questions — Quick Reference (11)

| Q# | Topic | One-line takeaway |
|---|---|---|
| 4 | Acceptable Use Policy naming | Correct name is **AWS Acceptable Use Policy** — "Applicable Use" and "Fair Use" are made-up distractors |
| 5 | CAF transformation phase | **Envision** = demonstrating how cloud accelerates business outcomes; Scale = expanding pilots to full value |
| 13 | Low-latency access for local end-users | **AWS Local Zones**, not Edge Locations — Edge Locations only cache CloudFront content, they don't run compute |
| 14 | Blocking SQL injection / XSS | **AWS WAF** blocks exploits at the HTTP layer; Inspector only assesses/reports vulnerabilities, it doesn't block traffic |
| 28 | Compute Optimizer scope (select two) | Covers **EC2 + ASG + EBS + Lambda** — you correctly had EC2/ASG but missed **EBS+Lambda** and wrongly added EFS |
| 31 | DDoS prevention (select three) | Missed **AWS WAF** — full trio is CloudFront+Route 53, WAF, and Shield |
| 36 | RDS Multi-AZ primary benefit | Multi-AZ = **availability** (automatic failover); protecting from a **regional** failure needs Multi-Region, not Multi-AZ |
| 50 | Well-Architected Framework pillars (select two) | **Reliability** is a real pillar — Scalability, Availability, Elasticity are NOT among the 6 named pillars |
| 55 | Storage Gateway types | Correct trio is **Tape, File, Volume** Gateway — "Block Gateway" is a made-up option |
| 61 | Easiest way to get resizable compute + per-second billing + OS access | **EC2**, not Lightsail — Lightsail runs on fixed monthly plans, no per-second billing |
| 63 | VPC vs subnet AZ span | **VPC spans all AZs in a Region; a subnet lives in exactly one AZ** — you had both spanning all AZs |

**Pattern in your misses:** Two clear clusters emerge. First, **made-up/distractor option traps** (Q4, Q55 — confidently-worded but fictional AWS terms like "Fair Use Policy" or "Block Gateway") caught you twice — worth building a habit of asking "have I actually seen this named service/policy in the source material?" before selecting it. Second, **service-capability boundary confusion** (Q13 Local Zones vs Edge Locations, Q14 WAF vs Inspector, Q36 Multi-AZ vs Multi-Region, Q61 EC2 vs Lightsail, Q63 VPC vs subnet AZ scope) — five misses where two similar-sounding AWS concepts got swapped. A smaller pattern is **select-two/three questions where one correct answer was found but the second was missed** (Q28, Q31, Q50 — 3 of 11 misses), consistent with the same habit seen in mocks 1 and 3. This is your strongest exam of the three (83.1%), with no Shared Responsibility Model misses this time — a good sign that concept has solidified.

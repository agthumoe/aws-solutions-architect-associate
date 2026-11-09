---
tags:
  - aws
  - cloud-practitioner
  - mock-exam
  - results
aliases:
  - "Mock Exam 3 Results"
status: completed
date: 2026-07-12
---

# Mock Exam 3 — Results

Companion answer key to `mock-exam-3.md`. Letters (A/B/C/D/E/F) match the option order in the questions file.

## Score

**49 / 65 correct (75.4%)** — passing score for CLF-C02 is 700/1000 (~72%), so this is a comfortable pass margin. 16 missed questions below are your highest-value review targets before the exam.

## Answer Key

| Q# | Domain | Your Answer(s) | Correct Answer(s) | Result |
|---|---|---|---|---|
| 1 | Security & Compliance | C | C | ✓ |
| 2 | Technology | C, D | C, D | ✓ |
| 3 | Billing & Pricing | A | A | ✓ |
| 4 | Security & Compliance | C, D | C, D | ✓ |
| 5 | Security & Compliance | C | D | ✗ |
| 6 | Security & Compliance | A | A | ✓ |
| 7 | Technology | B | B | ✓ |
| 8 | Cloud Concepts | A | A | ✓ |
| 9 | Technology | A | A | ✓ |
| 10 | Technology | B | C | ✗ |
| 11 | Technology | A | A | ✓ |
| 12 | Cloud Concepts | B | B | ✓ |
| 13 | Billing & Pricing | B | B | ✓ |
| 14 | Technology | C | C | ✓ |
| 15 | Billing & Pricing | A, E | A, B | ✗ |
| 16 | Billing & Pricing | C, D, E | C, D, E | ✓ |
| 17 | Technology | D | D | ✓ |
| 18 | Technology | C, E | C, E | ✓ |
| 19 | Technology | D | D | ✓ |
| 20 | Security & Compliance | A, B | A, B | ✓ |
| 21 | Technology | D | D | ✓ |
| 22 | Technology | D | D | ✓ |
| 23 | Technology | B | B | ✓ |
| 24 | Technology | A, B | C, E | ✗ |
| 25 | Billing & Pricing | A | A | ✓ |
| 26 | Cloud Concepts | A | A | ✓ |
| 27 | Technology | A, D | A, D | ✓ |
| 28 | Billing & Pricing | C, D | C, D | ✓ |
| 29 | Technology | D | D | ✓ |
| 30 | Security & Compliance | D | D | ✓ |
| 31 | Security & Compliance | C | C | ✓ |
| 32 | Security & Compliance | C | B | ✗ |
| 33 | Technology | B | B | ✓ |
| 34 | Cloud Concepts | C | D | ✗ |
| 35 | Technology | A | A | ✓ |
| 36 | Technology | D, E | D, E | ✓ |
| 37 | Security & Compliance | B | B | ✓ |
| 38 | Technology | D | D | ✓ |
| 39 | Security & Compliance | A, C | A, C | ✓ |
| 40 | Cloud Concepts | B | B | ✓ |
| 41 | Security & Compliance | A, E | A, B | ✗ |
| 42 | Security & Compliance | D | D | ✓ |
| 43 | Cloud Concepts | B | B | ✓ |
| 44 | Security & Compliance | C, E | C, E | ✓ |
| 45 | Security & Compliance | C | A | ✗ |
| 46 | Billing & Pricing | B | B | ✓ |
| 47 | Security & Compliance | A, B | A, E | ✗ |
| 48 | Technology | A | D | ✗ |
| 49 | Technology | D | B | ✗ |
| 50 | Technology | A | A | ✓ |
| 51 | Technology | C | B | ✗ |
| 52 | Technology | C | B | ✗ |
| 53 | Cloud Concepts | A | A | ✓ |
| 54 | Technology | B | B | ✓ |
| 55 | Technology | A | A | ✓ |
| 56 | Technology | A, B | A, B | ✓ |
| 57 | Billing & Pricing | D | B | ✗ |
| 58 | Billing & Pricing | C | A | ✗ |
| 59 | Cloud Concepts | B, E | A, C | ✗ |
| 60 | Technology | B | B | ✓ |
| 61 | Cloud Concepts | A | A | ✓ |
| 62 | Technology | B | B | ✓ |
| 63 | Technology | C | C | ✓ |
| 64 | Technology | A, E | A, E | ✓ |
| 65 | Technology | A | A | ✓ |

## Missed Questions — Quick Reference (16)

| Q# | Topic | One-line takeaway |
|---|---|---|
| 5 | Lambda customer responsibility | Customer maintains **function versions**; runtime environment is AWS's job |
| 10 | EFS access scope | EFS reaches across **AZs, Regions, AND VPCs** — you undersold its reach |
| 15 | EFS-IA vs EBS snapshot pricing | **EFS-IA charges per read/write**; AWS Backup restore is NOT free (you had that backwards) |
| 24 | Site-to-Site VPN components | **Customer Gateway + Virtual Private Gateway** — not Storage Gateway/NAT Gateway |
| 32 | Security self-assessment terminology | The practice itself is called **Penetration Testing**; Inspector is just one tool used for it |
| 34 | CAF perspective for strategy alignment | **Business Perspective** owns aligning cloud investment with business objectives, not Governance |
| 41 | Shared Responsibility Model (select two) | Config management is **shared, not customer-only**; missed "AWS operates infra/OS/platform for abstracted services" |
| 45 | What falls under AWS's purview | **Shield Standard** is AWS-managed (free, automatic); Security Groups are always customer-configured |
| 47 | Customer responsibilities (select two) | **OS patching of EC2** is customer's job — you picked "compliance validation" which is AWS's |
| 48 | EFS Standard-IA best use case | Best fit is **audit-accessible archival**, not sub-second latency object storage (that's S3/EBS territory) |
| 49 | Read Replica primary benefit | Read Replicas exist for **scalability** (read throughput), not availability — that's Multi-AZ's job |
| 51 | Mandatory IAM policy JSON elements | Only **Effect + Action** are mandatory; Sid and Principal are optional/conditional |
| 52 | Cross-region resource migration | No migration tool moves "everything" — you **manually rebuild in the destination Region** |
| 57 | CloudWatch billing metric Region | Always stored in **us-east-1 (N. Virginia)**, regardless of where your resources live |
| 58 | Separate invoices per environment | Only **separate AWS accounts** produce separate invoices — tags and Organizations don't |
| 59 | Off-the-shelf under-utilized EC2 detection | **Cost Explorer + Trusted Advisor** do this natively; Budgets/CUR/CloudWatch need manual setup first |

**Pattern in your misses:** The dominant cluster is **AWS Shared Responsibility Model** (Q5, 41, 45, 47 — 4 of 16 misses), where you're consistently unsure which granular task sits on which side of the line (runtime vs. version, Shield Standard vs. Security Groups, OS patching vs. compliance validation). Close behind is **select-two/three questions where you found one correct answer but the second was wrong or missing** (Q15, 24, 41, 47, 59 — 5 of 16 misses), suggesting a habit of stopping the search once one option feels right instead of validating all five before finalizing. A smaller cluster sits around **billing/cost-management tool boundaries** (Q57, 58, 59) and **storage-service edge cases** (Q10, 15, 48). Worth a focused re-read of the Shared Responsibility Model note and a deliberate "check every option" habit on multi-select questions before the next mock exam.

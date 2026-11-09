# Current Lesson State

## Status
**In Progress** — first teaching session underway.

## Last Session
- Date: 2026-07-01
- Action: Created all vault notes (D1–D4), corrected domain weights, added 09-Additional-Services for missing in-scope services, updated fullexam/quiz for multiple-response questions, created online resources index
- Progress: Vault complete. No teaching or quiz sessions yet.

## Vault Contents Summary
- Domain 1 (24%): 4 notes — Cloud fundamentals, Global Infra, Well-Architected, CAF + Migration
- Domain 2 (30%): 5 notes — IAM, Shared Responsibility, Network Security, Data Protection, Compliance/Governance
- Domain 3 (34%): 9 notes — Compute, Storage, DBs, Networking, Serverless, Monitoring, App Integration, IaC, Additional Services
- Domain 4 (12%): 3 notes — Pricing Models, Cost Management, Support Plans

## Last Session — 2026-07-01
**Topic: AWS Pricing Models (Domain 4)**

Sections taught so far:
- [x] Section 1: 4 AWS pricing principles (Pay as you go, Save when you reserve, Pay less by using more, Pay less as AWS grows)
- [x] Section 2: On-Demand — highest cost, most flexible, for unpredictable/short-term workloads
- [x] Section 3: Reserved Instances — Standard (72% off, locked) vs Convertible (66% off, flexible); payment: No/Partial/All Upfront; 1 or 3 years
- [x] Section 4: Savings Plans — commit to $/hour; EC2 Instance SP (72%) vs Compute SP (66%, most flexible) vs SageMaker SP (64%)

Sections remaining:
- [ ] Section 5: Spot Instances
- [ ] Section 6: Dedicated Host & Dedicated Instance
- [ ] Section 7: Capacity Reservations
- [ ] Section 8: S3 Pricing & Free Tier
- [ ] Section 9: Full comparison table + knowledge check

Also covered (D1): Region / AZ / Edge Location hierarchy and relationships.

## Teaching Preferences (confirmed this session)
- Ask "Any questions?" after each section, NOT a check question
- Save all questions for end-of-topic knowledge check
- Questions should be obvious and confidence-building, not tricky
- Same content/structure when revisiting the same topic

## Next Action
Resume pricing models at **Section 5: Spot Instances**.

## Pending Check Questions
None mid-section. Full knowledge check at end of all 9 sections.

---

## PARALLEL TRACK: Mock Exam Weak-Point Revision

**Status: In Progress — TIME-BOXED MODE (user has ~1 hour, started 2026-07-12).** Separate activity from the Pricing Models lesson above. Resume with "continue". Format is condensed (corrected fact + 1-line rule per miss, no long analogies) to fit the time budget — keep this condensed style until user signals more time is available.

Source: 43 total misses combined from `exams/mock-exam-1-results.md` (16), `exams/mock-exam-2-results.md` (11), `exams/mock-exam-3-results.md` (16), grouped into 18 thematic clusters, ordered by miss-frequency (highest first). One cluster per turn; user says "continue" to advance.

### Cluster order (18 total, re-ranked after mock exam 2 added)
1. [x] **Shared Responsibility Model** — mock3 Q5, 41, 45, 47 (4) — **TAUGHT (full depth, session 1)**
2. [ ] Storage services edge cases (EFS/EBS/Storage Gateway types) — mock3 Q10, 15, 48; mock2 Q55 (4) — **NEXT**
3. [ ] CAF (Perspectives + Transformation Phases) — mock1 Q11, 30; mock3 Q34; mock2 Q5 (4)
4. [ ] Database nuances (reservations, Global Tables/DAX, Read Replica vs Multi-AZ) — mock1 Q6, 33; mock3 Q49; mock2 Q36 (4)
5. [ ] DDoS/Security service boundaries (Shield/WAF/Inspector/GuardDuty) — mock1 Q2, 9; mock2 Q14, 31 (4)
6. [ ] Support Plans & Trusted Advisor — mock1 Q10, 55; mock3 Q59 (3)
7. [ ] Billing/cost tool boundaries + cross-region migration — mock3 Q52, 57, 58 (3)
8. [ ] VPC Networking (Gateway Endpoints/VPN gateways/VPC-subnet AZ span) — mock1 Q14; mock3 Q24; mock2 Q63 (3)
9. [ ] Messaging/Compute service choice + cloud characteristic terms (SQS/SNS/Lambda, Agility, EC2 vs Lightsail) — mock1 Q17, 28; mock2 Q61 (3)
10. [ ] Encryption defaults & key management (CMK, encrypted-by-default services) — mock1 Q44, 53 (2)
11. [ ] Governance/Audit + IAM policy elements (CloudTrail vs Config) — mock1 Q51; mock3 Q51 (2)
12. [ ] AI/ML services (Transcribe vs Polly) — mock1 Q41 (1)
13. [ ] Partners/Ecosystem (APN) — mock1 Q49 (1)
14. [ ] Security assessment terminology (Penetration Testing vs Inspector) — mock3 Q32 (1)
15. [ ] Global infra edge options (Local Zones vs Wavelength vs Edge Locations vs Direct Connect) — mock2 Q13 (1)
16. [ ] AWS Compute Optimizer scope (EC2/ASG/EBS/Lambda — not S3/EFS) — mock2 Q28 (1)
17. [ ] Well-Architected Framework pillar naming (Reliability/Cost Optimization — not Elasticity/Availability/Scalability) — mock2 Q50 (1)
18. [ ] AWS Acceptable Use Policy naming (vs made-up "Fair Use"/"Applicable Use") — mock2 Q4 (1)

### Standing meta-note (applies across all clusters)
Select-two/three questions where the student found one correct answer but missed/got the second wrong are a recurring pattern across all 3 mocks — mention periodically, not every cluster.

### Next Action
Resume at **Cluster 2: Storage services edge cases (EFS/EBS/Storage Gateway)** when user says "continue". Given the 1-hour budget and 17 remaining clusters, consider batching 2+ small (1-miss) clusters together in later turns to finish in time — use judgment based on time remaining.

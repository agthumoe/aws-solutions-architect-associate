# AWS Solutions Architect Associate — checked study guide

Updated **2026-11-09** after resource verification. The original downloaded guide is preserved under `_archive/pre-resource-audit-2026-11-09/`. This active guide replaces unchecked recommendations and prior-background assumptions. Full evidence/limits: [[00-Index/Resource-Audit]].

## Goal and starting point

Cloud Practitioner is passed. Prepare for **SAA-C03** in about six weeks if evidence supports it, with a maximum of two calendar months from the first actual study session. Daily availability, engineering background, current strengths and the exam booking are unconfirmed. No diagnostic or teaching has begun in this reset.

Memory support: short lessons, stable outlines, comparisons, retrieval, one question at a time, and explicit review dates at roughly 1/3/7/14/30 days. Do not promise perfect retention or a guaranteed pass. Use [[memory/progress_tracking]] as the single ledger; [[study-progress]] is only a pointer.

## Exam facts and scope

The [official guide](https://docs.aws.amazon.com/aws-certification/latest/solutions-architect-associate-03/solutions-architect-associate-03.html) defines four domains: secure 30%, resilient 26%, high-performing 24%, cost-optimized 20%. It describes 50 scored plus 15 unidentified unscored questions and a scaled 100–1000 score with a 720 passing standard. Do not convert a local practice percentage into that scaled score.

The [official overview](https://aws.amazon.com/certification/certified-solutions-architect-associate/) lists 65 questions, 130 minutes and a $150 USD base fee. Taxes, local currency, vouchers and booking rules can vary. Recheck at scheduling. [[00-Index/Exam-Scope]] links the 14 task statements and current service references; service lists are non-exhaustive and can change.

## Resources to use

1. Official guide, AWS docs, Skill Builder and Well-Architected material establish scope and correct service behavior.
2. Use selected [freeCodeCamp / Andrew Brown sections](https://www.freecodecamp.org/news/pass-the-aws-certified-solutions-architect-associate-certification/) for explanations; the linked 2024 course is about 50 hours, not a required watch-everything assignment.
3. Use [Cantrill supporting assets](https://github.com/acantril/aws-sa-associate-saac03) and [Well-Architected Labs](https://www.wellarchitectedlabs.com/) for diagrams and selected exercises; public supporting assets do not make the full Cantrill course free.
4. Use AWS's [free 20-question sets](https://aws.amazon.com/certification/certification-prep/) and the [Tutorials Dojo 30-question sampler](https://portal.tutorialsdojo.com/courses/free-aws-certified-solutions-architect-associate-practice-exams-sampler/) for external checks. Neither is a free full 65-question mock; official full practice exams are a separate subscription offering.
5. Treat the AWS Certifications Wiki and Tutorials Dojo comparisons as supplementary discovery/comparison aids. Training Camp's 25/50-question form-gated test and SAA Practice Dojo's advertised 1,000-question community bank are optional supplements whose full banks were not audited.

All links, access restrictions and rejected resources are in [[00-Index/Resource-Audit]]. The checked apgosar README has wrong fee/weights and missing files; do not use it as curriculum. The checked Jayendra page makes uncorroborated SAA-C04 claims; do not import them. Old SAA-C02 course/instructor routes are not the current syllabus. Paid prices and gated content are not asserted as verified.

## Six-week plan with buffer

| Week | Study focus | Evidence |
|---|---|---|
| 1 | Diagnostic, IAM/KMS/security, VPC routing/endpoints/hybrid | Explain access decisions and packet paths |
| 2 | EC2, load balancing/scaling, DNS, availability and DR | Justify multi-AZ and recovery choices |
| 3 | Storage, lifecycle, relational/NoSQL databases and caching | Explain competing service choices |
| 4 | Messaging, serverless, containers, analytics, migration, monitoring and costs | Design decoupled systems and identify charges |
| 5 | Complete task/scope review, missed and guessed questions, mixed practice | New scenario reasoning and delayed recall |
| 6 | Fresh reputable timed mocks and targeted remediation | Evidence-based readiness assessment |
| 7–8 | Buffer only as needed within the original two-month maximum | Close observed gaps without restarting the clock |

The maintained schedule is [[memory/progress_tracking]]; change it there. Use [[05-Practice/Architecture-Exercises]] and [[06-Cheatsheets/Architecture-Decisions]] after diagnostic identifies needs. Do not mark those activities complete because this guide exists.

## Assistant workflow

Read [[AGENTS]] and its required state. When the learner starts studying, confirm available time, set actual start/target/deadline, then administer 20 original scenario questions one at a time using `workflows/assessment.md`. Explain every choice only after an answer. Record incorrect answers AND correct guesses; schedule delayed recall. Keep initial topic recall supportive, then increase scenario difficulty. Preserve actual pending question/answers across sessions.

Readiness is not an arbitrary progress percentage. A provisional coaching target is at least two fresh reputable timed full mocks around 80–85%+, coverage of all tasks, no persistent major gaps and delayed explanations of key decisions. It is not an AWS passing threshold or pass guarantee; generated quizzes and repeats alone are insufficient calibration.

## Hands-on and budget

Prefer paper designs first. Deployed labs require separate learner authorization, current pricing, prerequisites, validation and cleanup. Builder Center sandboxes are only for eligible workshops and have time/request limits; they are not universal free AWS access. Free Tier terms depend on account/plan eligibility. Budget alerts do not cap charges. Check actual pricing before any optional practice subscription or paid course purchase.

No exam dumps, copied proprietary question banks, invented study results, or public sharing of supplied course PDFs. This repository must stay **private**. The learner authorized the resource-audit commit/push on 2026-11-09; normal teaching does not grant future publication permission.

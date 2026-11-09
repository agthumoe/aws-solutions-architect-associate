---
tags: [aws, saa-c03, exam-prep]
exam-domains: [1, 2, 3, 4]
status: reference
checked_on: 2026-11-09
---
# Exam strategy and logistics

## What to know

The [official SAA overview](https://aws.amazon.com/certification/certified-solutions-architect-associate/) lists 65 multiple-choice/multiple-response questions, 130 minutes and a $150 USD base exam fee. Testing can be at a Pearson VUE center or online; verify available languages, regional prices, vouchers, taxes and booking conditions at registration.

The [official guide](https://docs.aws.amazon.com/aws-certification/latest/solutions-architect-associate-03/solutions-architect-associate-03.html) says 50 questions are scored and 15 are unidentified unscored questions. Answer all questions; unanswered questions count as incorrect and there is no guessing penalty. AWS reports a scaled 100–1000 result with a 720 passing standard. Local quiz percentage is not directly convertible to that score.

## Solve the requirement, then compare

Identify the hard requirements: security, failure scope, latency/throughput, recovery objectives, cost and operational effort. Eliminate options that fail a requirement before comparing costs or simplicity. A complicated answer is not automatically wrong; the best answer meets all stated constraints with the appropriate trade-offs.

For multiple-response questions, select exactly the requested number. Budget roughly two minutes per question on average, reserving time to revisit flagged items. A 50-question/90-minute third-party test is a shorter, faster drill, not an exact exam simulation. Use a real timer for full mocks; all local mock questions are scored for practice.

## Prepare with evidence

Use [[00-Index/Exam-Scope]] for task/reference coverage, [[06-Cheatsheets/Architecture-Decisions]] for comparisons and `workflows/assessment.md` for readiness. Practice new architecture decisions, explain why distractors fail, log correct guesses and revisit errors after a delay. Reading a whole course again is not the default remedy for every gap.

Free official question sets and free vendor samplers are useful small samples, not full mocks or a pass prediction. Fresh reputable timed mock performance, delayed recall and task-level understanding together support a readiness judgment. The 80–85% study target is a coaching heuristic, not AWS's required raw percentage.

## Verify registration policies

Read [Before Testing](https://aws.amazon.com/certification/policies/before-testing/) for accepted ID, name matching, testing environment and accommodation rules, and [After Testing](https://aws.amazon.com/certification/policies/after-testing/) for results and retake policies. Do not memorize an old slide's universal “one ID” or “no pen” rule; requirements vary by delivery mode and location. Current AWS policy specifies a 14-calendar-day wait after a failed attempt; recheck before a retake.

## Further reading

Use the [Well-Architected Framework](https://docs.aws.amazon.com/wellarchitected/latest/framework/welcome.html) and [DR strategy whitepaper](https://docs.aws.amazon.com/whitepapers/latest/disaster-recovery-workloads-on-aws/disaster-recovery-workloads-on-aws.html). The general AWS disaster-recovery marketing URL is an Elastic Disaster Recovery product page, not the full four-strategy paper. FAQs can clarify service behavior; do not claim their exact wording is guaranteed to appear on an exam.

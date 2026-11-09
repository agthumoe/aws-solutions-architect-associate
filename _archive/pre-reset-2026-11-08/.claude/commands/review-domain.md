# Review Domain

Summarize and review all notes for an exam domain to reinforce study.

**Usage:** `/review-domain <domain-number>`

## Instructions

Given `$ARGUMENTS` as a domain number (1–4):

1. Read the relevant domain MOC from `00-Index/Exam-Domains/` to get the task statements and linked cluster notes, then read those cluster notes (SAA-C03 domains are cross-cutting — content lives in topic-cluster folders, not one folder per domain):
   - 1 → `00-Index/Exam-Domains/01-Design-Secure-Architectures.md` (30%) — notes tagged `exam-domains: [1]`
   - 2 → `00-Index/Exam-Domains/02-Design-Resilient-Architectures.md` (26%) — notes tagged `exam-domains: [2]`
   - 3 → `00-Index/Exam-Domains/03-Design-High-Performing-Architectures.md` (24%) — notes tagged `exam-domains: [3]`
   - 4 → `00-Index/Exam-Domains/04-Design-Cost-Optimized-Architectures.md` (20%) — notes tagged `exam-domains: [4]`

3. Produce a review summary in the chat (do NOT write a file) covering:
   - **Key concepts** from all notes in that domain
   - **AWS services** that map to that domain
   - **Likely exam question themes** based on domain weight
   - **Gaps** — topics the vault doesn't yet cover well
   - **Suggested next notes** to create

4. End with a checklist:
```markdown
## Domain <N> Review Checklist
- [ ] Can explain <concept 1>
- [ ] Know difference between <service A> and <service B>
- [ ] Remember exam tip: <tip>
```

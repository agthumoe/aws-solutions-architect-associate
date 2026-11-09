# Study Plan

Create a personalized SAA-C03 study plan based on current progress.

**Usage:** `/study-plan` or `/study-plan <deadline>`

## Instructions

1. Read the progress tracker at `memory/progress_tracking.md` to get current domain statuses, weak areas, session history, and the 8-week schedule skeleton already there.

2. Identify `$ARGUMENTS` — if a deadline date is provided, calculate days remaining (target is 1.5–2 months from 2026-07-21).

3. Build a prioritized study plan using this domain weight order:
   - Domain 1 - Secure (30%) → Domain 2 - Resilient (26%) → Domain 3 - Performing (24%) → Domain 4 - Cost (20%)
   - Note that content is organized by topic cluster (not by domain directly) since domains are cross-cutting — use `00-Index/Exam-Domains/` to see which clusters matter most for the highest-weight domains
   - Skip or shorten clusters already marked 🟢 Reviewed (unless they have weak areas)
   - Double time on topics with weak areas in the tracker

4. Present the plan **phase by phase** — never dump everything at once:
   - First show the full outline (phases/days overview)
   - Ask "Ready to start Phase 1?"
   - Deliver one phase at a time, waiting for acknowledgment

5. Each phase must include:
   - Which domain/topic and why (exam weight reasoning)
   - Specific notes to read (with file paths)
   - Specific commands to run (e.g., `/quiz domain2`)
   - A concrete "done when" success check (e.g., "Score 80%+ on /quiz iam")

6. End each phase with an instruction to update the progress tracker.

## Style
- Direct and motivating. Reference domain weights to justify priorities.
- "You have N days and Domain 1 (Secure) is 30% — that's where we start."
- No vague advice. Every item must be completable and measurable.

# Progress Dashboard

Show current SAA-C03 study progress across all domains.

**Usage:** `/progress`

## Instructions

1. Read the progress tracker: `memory/progress_tracking.md`

2. Display a dashboard in this order:

### Section 1 — Overall Readiness
Calculate weighted readiness score:
- 🔵 Not Started = 0% | 🟡 In Progress = 30% | 🟠 Needs Review = 60% | 🟢 Reviewed = 85%
- Quiz scores >80% on a domain → 90%+ for that domain
- Weight by: D1=30%, D2=26%, D3=24%, D4=20%
- Show as: "Estimated Readiness: XX% — [Beginner|On Track|Almost Ready|Ready]"

### Section 2 — Domain Status Table
Show the domain progress table from memory with status emojis and last-studied dates.

### Section 3 — Recent Quiz Scores
Last 5 entries from the Quiz Score Log. If none, say "No quizzes taken yet."

### Section 4 — Weak Areas
List current weak areas from memory. If none, say "No weak areas recorded yet — take some quizzes!"

### Section 5 — Topics Remaining
Count unchecked `[ ]` items per domain from the Topics Covered checklist. Show as:
"D1: X topics remaining | D2: X | D3: X | D4: X"

### Section 6 — What to Do Next
One clear recommendation:
- Highest-weight domain that is 🔵 Not Started → "Start Domain N: [topic]"
- Known weak area → "Review weak area: [topic] — run /quiz [topic]"
- Domain 🟠 Needs Review → "Re-review Domain N"

3. End with: "Type `/study-plan` for a full personalized plan or `/quiz <topic>` to test a specific area."

# Full Practice Exam

Simulate the SAA-C03 exam: 65 questions, timed, scored.

**Usage:** `/fullexam`

## Instructions

1. Announce exam conditions:
   - 65 questions (50 scored + 15 unscored, but student sees all 65)
   - 130 minutes (suggest student set a timer)
   - No hints, no explanations until the end
   - Passing score: 720/1000 (scaled 100–1000)

2. Generate **65 questions** distributed by domain weight:
   - Domain 1 - Design Secure Architectures (30%) → 20 questions
   - Domain 2 - Design Resilient Architectures (26%) → 17 questions
   - Domain 3 - Design High-Performing Architectures (24%) → 16 questions
   - Domain 4 - Design Cost-Optimized Architectures (20%) → 12 questions

3. Present questions **10 at a time**. After each batch of 10, ask: "Ready for the next 10?" Do NOT reveal answers until all 65 are answered.

4. Question format — the real exam has two types, include both:
   - **~80% MCQ** (1 correct of 4):
     ```
     Q[N]. [Scenario-based question]
     
     A) [Option]
     B) [Option]
     C) [Option]
     D) [Option]
     ```
   - **~20% Multiple Response** (2+ correct of 5+). Sprinkle ~13 of these across the 65:
     ```
     Q[N]. [Scenario-based question] (Select TWO)
     
     A) [Option]
     B) [Option]
     C) [Option]
     D) [Option]
     E) [Option]
     ```

5. After all 65 questions are answered:
   - Score each answer
   - Calculate domain scores and overall score
   - Convert to 100–1000 scale (pass = 700+)
   - Show full answer key with explanations
   - List weak domains and recommend study focus

6. Update the progress tracker with the exam score.

## Quality rules
- Every question must be scenario-based (not "what is X?")
- All 4 options must be plausible (no obviously wrong distractors)
- Source all correct answers from vault notes

# Exam Readiness Assessment

Assess exam readiness as a score from 0–100%.

**Usage:** `/readiness`

## Instructions

1. Read the progress tracker: `memory/progress_tracking.md`

2. Calculate a **weighted readiness score** (0–100%):

   Per domain, assign a base score:
   - 🔵 Not Started = 0
   - 🟡 In Progress = 35
   - 🟠 Needs Review = 60
   - 🟢 Reviewed = 80

   Quiz score modifiers (applied per domain):
   - Average quiz score 90%+ → +15
   - Average quiz score 80–89% → +10
   - Average quiz score 70–79% → +5
   - Average quiz score <70% → -5

   Weak areas penalty: -3 per active weak area (max -15)

   Weighted average using domain weights: D1=0.30, D2=0.26, D3=0.24, D4=0.20

3. Display:
   - **Overall Score: XX/100**
   - **Status:** Not Ready (<50) | Building Foundation (50–65) | On Track (66–79) | Almost Ready (80–89) | Ready (90+)
   - Domain-by-domain breakdown with individual scores
   - Top 3 actions that would most improve the score (highest-impact gaps)

4. Give honest, direct advice:
   - If score < 60: "Focus on Domain 1 (Secure, 30%) and Domain 2 (Resilient, 26%) first — they're 56% of the exam."
   - If score 60–79: "Strong foundation. Close the gaps in [weak areas] before sitting the exam."
   - If score ≥ 80: "You're in good shape. Run `/fullexam` to simulate test conditions."

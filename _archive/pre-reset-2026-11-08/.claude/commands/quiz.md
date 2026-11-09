# Generate Practice Quiz

Generate AWS Certified Solutions Architect Associate (SAA-C03) practice questions for a domain or topic.

**Usage:** `/quiz [domain-number|topic] [count]`

## Instructions

Given `$ARGUMENTS`:
- Parse domain number (1–4) or topic keyword
- Default count: 10 questions
- Generate questions in SAA-C03 exam style (scenario-based, mostly 4-option single-answer, with some multiple-response) — delegate to the `quiz-master` agent for question quality

Output format — append to `05-Practice/Practice-Questions-Domain-<N>.md` or create a new file if topic-based:

```markdown
## Question Set — <Topic> — <Date>

### Q1. <Question text>

A) Option A  
B) Option B  
C) Option C  
D) Option D  

<details>
<summary>Answer</summary>

**Correct: B**

**Explanation:** Why B is correct and why others are wrong.

</details>
```

Rules:
- Questions must reflect real SAA-C03 exam style (scenario-based architecture design decisions, not simple recall)
- Cover both easy recall and tricky application questions
- Reference actual AWS services by correct name
- After appending, report how many questions were added and to which file

# Quick Reference Notes

Retrieve a quick reference summary for any topic or service.

**Usage:** `/notes <topic>`  
**Examples:** `/notes bedrock`, `/notes rag`, `/notes domain5`, `/notes sagemaker-clarify`

## Instructions

Given `$ARGUMENTS` as the topic/service:

1. Find and read the relevant vault note(s).

2. Produce a **concise quick-reference card** — NOT a full explanation. Format:

   ```
   ## [Topic Name]
   
   **What it is:** One sentence.
   
   **Key facts:**
   - Fact 1
   - Fact 2
   - Fact 3
   
   **Exam scenarios:**
   - "Question pattern" → Answer
   - "Question pattern" → Answer
   
   **Don't confuse with:** [similar service/concept and the key difference]
   ```

3. Keep it to one screen — this is a quick lookup, not a lesson.

4. If the topic spans multiple notes, combine into a single reference card.

## Source constraint
All facts from vault notes only.

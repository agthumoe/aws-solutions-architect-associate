# Fact Tree

Generate a visual fact tree for a topic, domain, or all domains.

**Usage:** `/facts <topic|domain-number|all>`  
**Examples:** `/facts bedrock`, `/facts domain3`, `/facts all`

## Instructions

Given `$ARGUMENTS`:

1. Read the relevant vault notes for the topic/domain.

2. Generate a **Mermaid mindmap or flowchart** showing the key facts as a tree structure.

3. Below the diagram, provide a **numbered fact list** — exam-critical facts only, formatted as:
   ```
   1. [FACT] — [why it matters on the exam]
   2. [FACT] — [why it matters on the exam]
   ```

4. End with **3 most-likely exam scenarios** for this topic, formatted as:
   ```
   🎯 "A company needs to..." → [answer]
   🎯 "Which service..." → [answer]
   🎯 "What is the difference between..." → [answer]
   ```

## Scope rules
- Single topic → facts for that specific service/concept
- Domain number (1–5) → top 15–20 facts for that domain
- "all" → master fact summary across all 5 domains (top 10 per domain)

## Source constraint
Facts must come from vault notes only. No external knowledge.

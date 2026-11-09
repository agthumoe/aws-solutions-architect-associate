# New Study Note

Create a new study note for the AWS Certified Solutions Architect Associate (SAA-C03) vault.

**Usage:** `/new-note <title> [cluster] [exam-domains]`

## Instructions

Given the arguments `$ARGUMENTS`, parse:
- `title` — the note title (required)
- `cluster` — target folder: `01-Foundations`, `02-Compute-EC2`, `03-Storage`, `04-Databases`, `05-Networking-Content-Delivery`, `06-Containers-Serverless`, `07-Integration-Messaging`, `08-Security-Identity`, `09-Monitoring-Management`, `10-Machine-Learning`, `11-Architecture-Patterns`, `12-Exam-Prep`, `05-Practice`, `06-Cheatsheets` (default: infer from topic)
- `exam-domains` — which of the 4 official exam domains (1–4) this note is relevant to (infer if not given; a note can map to multiple)

Create a new `.md` file using the standard vault template:

```markdown
---
tags: [aws, saa-c03, <topic-tag>]
domain: <cluster-name>
exam-domains: [N, ...]
status: not-started
date: <today's date>
---

# <Title>

## Key Concepts

## AWS Services / Features

## Exam Tips
> [!TIP]
> Key things to remember for the exam

## Related Notes
- [[Related Note]]
```

Rules:
- Use Obsidian wiki-links `[[Note Title]]` for cross-references
- Use Mermaid for any diagrams — never ASCII art
- Place the file in the correct cluster folder based on topic
- After creating, remind the user to add a link in the cluster's `00-Cluster-MOC.md` and the relevant `00-Index/Exam-Domains/0N-*.md` file(s)

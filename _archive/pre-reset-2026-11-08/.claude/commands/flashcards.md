# Generate Flashcards

Generate flashcard-style Q&A pairs for a topic or domain and save to `04-Practice/`.

**Usage:** `/flashcards <topic-or-domain>`

## Instructions

Given `$ARGUMENTS`, generate 15–20 flashcard pairs covering the topic.

Create or append to `05-Practice/Flashcards-<Topic>.md`:

```markdown
---
tags: [aws, cloud-practitioner, flashcards, <topic-tag>]
domain: <domain>
---

# Flashcards — <Topic>

## Card 1
**Q:** What is <term>?  
**A:** <concise answer, 1–2 sentences>

---

## Card 2
**Q:** What is the difference between <A> and <B>?  
**A:** <A> does X while <B> does Y.

---
```

Rules:
- Cover service names, definitions, use cases, and differentiators
- Include "trick" cards that address common misconceptions
- Keep answers concise — exam recall, not essays
- Add `[[Flashcards-<Topic>]]` link to the relevant domain MOC after creating

# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

> [!NOTE]
> The configuration in `.claude/` is shared between Antigravity CLI and Claude Code.

## Local Memory (Git-Tracked)

Study progress and lesson state are stored in `memory/` inside this repo — git-committed and portable across any Claude session.

**At the start of every session, read ALL files in `memory/`:**
- `memory/progress_tracking.md` — domain status, quiz scores, session log
- `memory/current_lesson_state.md` — exact section, pending check question, resume instructions
- `memory/feedback_teaching_flow.md` — how to pace teaching sessions
- `memory/feedback_teaching_consistency.md` — follow canonical outline strictly
- `memory/feedback_terminal_diagrams.md` — plain text diagrams in chat, Mermaid only in vault files
- `memory/feedback_diagrams.md` — Mermaid rules for vault files
- `memory/project_purpose.md` — project context and output rules

**After every session, update** `progress_tracking.md` and `current_lesson_state.md` to reflect what was covered, questions answered, and what's next.

---

## Project Overview

This repository is a **study environment** for the **AWS Certified Solutions Architect – Associate (SAA-C03)** exam preparation. The goal is to study material from uploaded course sources and pass the certification exam within a 1.5–2 month intensive timeline.

The AWS Certified Cloud Practitioner (CLF-C02) material has been archived to `_archive/clf-c02/` — that certification was already passed.

**Exam Domains (official AWS exam guide weights):**
- Domain 1: Design Secure Architectures (30%)
- Domain 2: Design Resilient Architectures (26%)
- Domain 3: Design High-Performing Architectures (24%)
- Domain 4: Design Cost-Optimized Architectures (20%)

**Exam format:** 65 questions (50 scored + 15 unscored), 130 minutes, scaled score 100–1000, passing score 720, $150 USD, valid 3 years.

---

## Slash Commands

Skills are invoked by typing a `/command` prefix. Available commands:

### Teaching Commands
- `/teach <topic>` — Professor explains a topic section by section
- `/clarify <concept>` — Clarify a confused concept
- `/analogy <topic>` — Get an analogy for a hard concept
- `/domain <number>` — Deep dive into specific domain (1-4)
- `/moc <domain>` — Map of Content for domain

### Coding/Lab Commands
- `/code <task>` — Engineer helps you write AWS SDK / CLI code
- `/review <code>` — Engineer reviews your code
- `/debug <problem>` — Debug an AWS service issue
- `/example <concept>` — Show a real-world AWS example

### Quiz Commands
- `/quiz <topic>` — 5-10 questions (medium difficulty)
- `/hardquiz <topic>` — Hard questions for mastery
- `/easyquiz <topic>` — Easy questions for practice
- `/practice <topic>` — Practice with hints
- `/check <answer>` — Grade your answer
- `/weakness` — Quiz on weak areas
- `/progress` — Show your progress

### Exam Commands
- `/fullexam` — Full practice exam (65 questions, like the real exam)
- `/timedquiz <mins> <topic>` — Timed quiz
- `/strategy` — Exam-day strategy
- `/readiness` — Assess readiness (0-100%)
- `/finalreview` — Last-minute summary
- `/simulate-exam` — Full exam under test conditions

### Study Planning Commands
- `/study-plan` — Create personalized study plan
- `/today` — What to study today
- `/gaps` — Identify knowledge gaps
- `/strongareas` — Show your strong topics
- `/weakareas` — Show weak areas
- `/schedule <deadline>` — Plan to deadline

### Reference Commands
- `/notes <topic>` — Quick reference on a topic
- `/key-terms <domain>` — Key terminology for a domain
- `/compare <service1> <service2>` — Compare two AWS services
- `/summary <topic>` — Topic summary
- `/definitions` — All key definitions
- `/services` — AWS services quick reference

### Exam Facts Commands
- `/facts <topic>` — Visual fact tree for a topic
- `/facts <domain>` — All key facts for an entire domain
- `/facts all` — Master fact tree across all four domains

### Understanding Commands
- `/visualize <concept>` — ASCII diagram of any architecture or service flow
- `/diagram <concept>` — Alias for `/visualize`
- `/flowchart <process>` — Step-by-step process with state shown at each step
- `/misconceptions <topic>` — Top misconceptions, with corrections and self-test drills
- `/gotchas <topic>` — Alias for `/misconceptions`

**Examples:**
```
/teach ec2                      <- Learn from Professor
/quiz s3                        <- Quiz on S3
/compare ec2 lambda             <- Compare two AWS services
/readiness                      <- Check exam readiness
/fullexam                       <- Take full practice exam
```

---

## Repository Structure

The repository follows a **Map of Content (MOC)** organizational pattern, but unlike a typical single-domain-per-folder layout, SAA-C03's 4 domains are cross-cutting design concerns (secure/resilient/performing/cost-optimized) that every AWS service touches. So structure splits into two layers:

- **Topic clusters** (`01-Foundations/`, `02-Compute-EC2/`, `03-Storage/`, `04-Databases/`, `05-Networking-Content-Delivery/`, `06-Containers-Serverless/`, `07-Integration-Messaging/`, `08-Security-Identity/`, `09-Monitoring-Management/`, `10-Machine-Learning/`, `11-Architecture-Patterns/`, `12-Exam-Prep/`) — the source of truth for content, organized by AWS service/topic to match the course structure. Each cluster has:
  - `00-Cluster-MOC.md` — index of the cluster's notes
  - `01-xxx.md`, `02-xxx.md`, etc. — detailed notes on subtopics

- **Domain cross-reference MOCs** (`00-Index/Exam-Domains/01-Design-Secure-Architectures.md` etc.) — list the official task statements per domain and link out to the cluster notes that cover them. Used for exam-weighted review (`/readiness`, `/study-plan`, `/fullexam`, `/review-domain`) without duplicating content 4 times.

- `/slides` — Study source PDFs and documents (upload here). Primary source: `AWS Certified Solutions Architect Slides v48.pdf`

- `_archive/clf-c02/` — Archived CLF-C02 vault (passed exam, kept for reference)

- `.claude/` — Skills, rules, and settings

---

## Key Constraint: Source-Only Principle

All content must adhere to the **source-only principle**:
> Every fact comes from the uploaded study sources. Nothing has been added from outside reading, textbooks, or general knowledge.

**Enforcement:**
- ALLOWED: "According to Domain 1 slides, cloud computing is..."
- NOT ALLOWED: External sources or unsourced claims

---

## CRITICAL: Never Guess Rule

**If a fact or service detail is not explicitly in the study sources — STOP.**

Do NOT answer from general knowledge. Instead say:
> "This is not in the study sources. Want me to look it up in official AWS docs (only after you approve), or skip it?"

**Never use words like:** "probably", "typically", "I believe", "should be", "generally" — these mean you are guessing.

**Only consult official documentation after the student explicitly approves.**

This rule applies to ALL agents and skills — teach, quiz, facts, study, everything.

---

## Mermaid Diagram Rule

**CRITICAL: Never use `\n` inside Mermaid diagram code blocks. Always use `<br>` for line breaks.**

Obsidian renders Mermaid natively. `\n` is invalid in Mermaid node label syntax and will break the diagram. `<br>` is the correct line break.

```
❌ WRONG:  A["Amazon EC2\n(Compute)"]
✅ CORRECT: A["Amazon EC2<br>(Compute)"]

❌ WRONG:  B --> C[Data stored in\nS3 bucket]
✅ CORRECT: B --> C[Data stored in<br>S3 bucket]
```

This applies to **all** Mermaid node labels `[...]`, edge labels `|...|`, and quoted strings `"..."` inside any ` ```mermaid ` block.

Full rule documented in: `.claude/rules/content-rules.md` — Rule 7a

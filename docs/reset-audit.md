# Reset audit — 2026-11-08

The repository already contained a partial SAA migration, 12 topic clusters, four domain MOCs, course PDFs, XMind files, and archived CLF notes/exams. The imported guide was untracked and is preserved unchanged.

Problems found: July start dates and stale migration state; slide-only rules blocking authorized external sources; conflicting per-section teaching checks; commands that implied unsupported aliases; a flashcard command with a CLF tag and wrong path; five-domain wording; arbitrary readiness points; mock scoring that mixed 720 with 700 and claimed a percentage-to-scaled conversion.

Applied approach: preserve reference content and archives, snapshot pre-reset configuration/state, replace active tracking, and centralize assistant instructions/workflows. This avoids destructive deletion and avoids copying stale mastery into a new track. Vendor adapters delegate to shared rules; a portable study skill can be read directly by any assistant. Existing generic Obsidian skills remain intact.

Not done: diagnostic, teaching, paid enrollment, AWS deployment, source-by-source fact audit, commits or pushes. Notes retain historical metadata/provenance; they need verification when used. Resource availability beyond the official guide and certification overview is not asserted. The study guide's engineering-background assumption is unconfirmed.

Dates: actual study start and booking are unset. Plan aims for six weeks with an eight-week buffer bounded by two calendar months from first study. Readiness is an evidence-based coaching judgment, never a pass guarantee.

Repository handling: create a private empty GitHub destination; do not overwrite origin, commit, or push. Without an authorized future commit/push the new remote cannot contain this working tree. Existing local git history stays intact; a truly history-free local repository can be prepared separately when requested.

This document records the **2026-11-08 reset only**. The learner subsequently authorized the resource audit, corrections and private initial publication on 2026-11-09; see [[docs/content-audit]] and [[docs/publication]].

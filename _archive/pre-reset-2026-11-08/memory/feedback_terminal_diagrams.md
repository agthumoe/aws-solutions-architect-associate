# Feedback: Terminal Diagrams

## Rule: Plain Text Diagrams in Chat, Mermaid Only in Vault Files

**In chat (teaching sessions, explanations):**
- Use plain ASCII/text diagrams — they render correctly in the terminal
- Example:
  ```
  Internet → [IGW] → [Public Subnet] → EC2
                              ↓
                      [NAT Gateway]
                              ↓
                      [Private Subnet] → EC2
  ```

**In vault Markdown files (.md):**
- Use Mermaid diagrams in ```mermaid blocks
- Never use ASCII art in .md files
- Never use `\n` inside Mermaid node labels — use `<br>` instead

## Why
- Terminal/chat: Mermaid is not rendered; ASCII is readable
- Obsidian: Mermaid renders natively; ASCII looks messy

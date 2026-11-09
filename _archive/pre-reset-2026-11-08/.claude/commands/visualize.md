# Visualize a Concept

Generate a Mermaid diagram for any AWS AI/ML concept, architecture, or service flow.

**Usage:** `/visualize <concept>` or `/diagram <concept>`  
**Examples:** `/visualize rag-pipeline`, `/visualize bedrock-agents`, `/visualize ml-lifecycle`

## Instructions

Given `$ARGUMENTS` as the concept:

1. Read the relevant vault notes to base the diagram on source content only.

2. Generate a **Mermaid diagram** (always use ```mermaid blocks — never ASCII art).

3. Choose the most appropriate diagram type:
   - `flowchart LR/TD` — for pipelines, workflows, decision flows
   - `sequenceDiagram` — for request/response flows between services
   - `graph TD` — for hierarchies and relationships
   - `classDiagram` — for comparing service capabilities

4. After the diagram, provide a **2–3 sentence explanation** of what the diagram shows and what the exam tests about this concept.

5. If the concept maps to a specific domain, note which domain and task statement it belongs to.

## Mermaid rules
- Always use `mermaid` code fences (Obsidian renders these natively)
- Keep node labels concise (max ~5 words per node)
- Use subgraphs to group related components
- Add a title comment at the top: `%% Title: <concept name>`

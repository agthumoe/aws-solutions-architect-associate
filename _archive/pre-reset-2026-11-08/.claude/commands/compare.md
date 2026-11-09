# Compare Two AWS Services

Side-by-side comparison of two AWS AI/ML services.

**Usage:** `/compare <service1> <service2>`  
**Examples:** `/compare bedrock sagemaker`, `/compare rekognition comprehend`, `/compare rag fine-tuning`

## Instructions

Given `$ARGUMENTS` as two service/concept names:

1. Read the vault notes for both services.

2. Produce a **comparison table** with these rows:
   - What it is (one-line definition)
   - Primary use case
   - Who uses it (persona)
   - Requires ML expertise?
   - Managed / serverless?
   - Key features
   - When to choose this over the other
   - Exam trap (common mistake students make)

3. Below the table, add a **decision flowchart** (Mermaid):
   ```
   A[Business need described] --> B{Which one?}
   B -- "condition" --> C[Service 1]
   B -- "condition" --> D[Service 2]
   ```

4. End with **3 exam scenario examples** — one question per service and one that tests the distinction:
   ```
   Q: "A company wants to [X]..." → [Service]
   Q: "A team needs to [Y]..." → [Service]
   Q: "Both services can [Z], but the key difference is..." → [explanation]
   ```

## Source constraint
Only use facts from vault notes. No external knowledge.

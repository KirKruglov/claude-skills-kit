# Starter Prompt Templates by Project Type

Loaded by the Starter Prompts module (step 6). Claude selects the section based on the project type, adapts it to the project context (name, terminology), and saves as separate .md files in resources/prompts/.

---

## Type: analytics

### File: analyze-data.md

```markdown
## Role
Data Analyst

## Task
Analyze the file from input/ following this plan:
1. Overall data structure: rows, columns, types, missing values
2. Key metrics and distributions
3. Anomalies and outliers
4. Findings and recommendations

## Input
File from the input/ folder — identify automatically from task context.

## Output Requirements
- Format: structured text with tables
- Each finding: fact → interpretation → recommendation
- Save result to output/
```

### File: compare-sources.md

```markdown
## Role
Research Analyst

## Task
Compare data from multiple files in input/:
1. Identify common and unique parameters
2. Find discrepancies and contradictions
3. Build a comparison table
4. Formulate findings

## Input
All relevant files from input/.

## Output Requirements
- Comparison table
- List of discrepancies with source references
- Summary: 3–5 sentences
- Save to output/
```

---

## Type: content

### File: write-post.md

```markdown
## Role
Content Strategist and Copywriter

## Task
Write a post on the topic: [topic]

## Requirements
- Platform: [LinkedIn / Telegram / X]
- Tone: expert, no motivational clichés
- Structure: hook → main point → examples/data → conclusion
- Length: 150–250 words for LinkedIn, 100–150 for Telegram

## Constraints
- No emojis (unless specified)
- No generic phrases or clichés
- Save draft to drafts/
```

### File: adapt-post.md

```markdown
## Role
Content Editor

## Task
Adapt the post from file [source] for platform [target platform].

## Adaptation Rules
- LinkedIn → Telegram: shorten, remove CTA, add directness
- LinkedIn → X: compress to 280 characters, preserve the key point
- Telegram → LinkedIn: expand, add context and professional tone

## Output
- Save to drafts/ with platform suffix
```

---

## Type: business

### File: research-topic.md

```markdown
## Role
Business Analyst / Researcher

## Task
Conduct structured research on the topic: [topic]

## Plan
1. Define key questions
2. Analyze available sources from input/
3. Matrix: facts / hypotheses / gaps
4. Findings and next steps

## Output Requirements
- Mark all hypotheses as [hypothesis]
- Reference the source for each fact
- Save to output/
```

### File: prepare-summary.md

```markdown
## Role
Analyst

## Task
Prepare a summary of materials from input/ on the topic: [topic]

## Format
- Executive summary: 3–5 sentences
- Key facts: table or list
- Open questions: what needs clarification
- Length: no more than 1 page

## Output
- Save to output/
```

---

## Type: personal

Starter prompts are not generated. Tasks are too varied — the user is better off creating prompts using the prompt-builder skill.

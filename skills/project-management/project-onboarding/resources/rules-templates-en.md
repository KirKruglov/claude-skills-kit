# Project Rule Templates by Type

Loaded by the Rules module (step 5). Claude selects the section based on the project type from answer 2, then appends the general rules.

---

## Type: analytics

```markdown
## Project Rules

### Data Handling
- Include data source references for all calculations
- Do not modify input files — work with copies
- If data anomalies are detected — report before proceeding

### Output Structure
- Format: fact → interpretation → recommendation
- Round numbers to 2 decimal places unless specified otherwise
- Format comparisons as tables

### Output Files
- Save analysis results to output/
- Intermediate calculations — in drafts/
```

---

## Type: content

```markdown
## Project Rules

### Content Creation
- Follow brand voice defined in context.md (if specified)
- Before finalizing, check: tone, length, structure
- Do not publish without explicit user confirmation

### Files
- Save drafts to drafts/
- Final versions — in output/
- Each post/article — a separate file with date in filename

### Adaptation
- When adapting across platforms — account for each platform's format and audience
- Do not copy text verbatim between platforms
```

---

## Type: business

```markdown
## Project Rules

### Research and Hypotheses
- Mark all hypotheses as [hypothesis] until validated
- Reference data and document sources
- Record decisions with date and rationale

### Documentation
- Record key decisions in the decisions-log section of context.md
- Meetings and discussions — in notes/
- Final documents — in output/

### Communication
- Stakeholder materials — avoid technical jargon
- Presentations — include executive summary on the first slide
```

---

## Type: personal

```markdown
## Project Rules

### General
- Priority — speed and practicality
- Minimal formality in formatting
- Save results to output/
```

---

## General Rules (appended to all types)

```markdown
## General Rules

### File Discovery
If a task references a file by description, topic, or type — rather than by exact name — run `ls` or `find` in the project folder and locate the file on your own. Do not ask for clarification if you can identify the file from context. If multiple files match — show a list and ask briefly.

### Language and Style
- Language: English
- Style: direct, structured, no filler
- Do not suggest next steps unless asked

### Safety
- Do not delete files without explicit confirmation
- Do not modify input data (input/) — read only
```

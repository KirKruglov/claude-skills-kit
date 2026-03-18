---
name: context-builder-cowork
description: "Activate this skill when the user wants to create a project context file for Cowork. Triggers: 'create project context', 'new project context', 'context-builder', 'generate context file', 'quick context'. Generates a ready-to-download project-context.md file for Claude Cowork based on user's answers."
version: 1.0
modes:
  - new: Full interview, complete context file
  - quick: Minimal interview (blocks 1-3 only), placeholders for the rest
---

# Skill: context-builder-cowork

Generates a ready-to-use `project-context.md` for Claude Cowork based on user answers.

---

## Launch Modes

| Mode | How to trigger | What it does |
|------|---------------|--------------|
| `new` | "create project context" / "new project" | Full interview, all blocks |
| `quick` | "quick context" | Blocks 1–3 only, rest → `[to clarify]` |

---

## Instructions for Claude

### Step 1 — Determine mode
If the user wrote "quick context" → use `quick` mode (questions 1–8).
Otherwise → use `new` mode (all 15 questions).

### Step 2 — Conduct the interview
Ask questions **in blocks**, not all at once.
Wait for the user's response after each block, then proceed to the next.

---

## Question Script

### Block 1 — Basics
```
1. Project name?
2. Type: business / analytics / personal / other?
3. Status: Active / On hold / Completed?
4. Start date? Deadline (if any)?
```

### Block 2 — Project essence
```
5. Describe the project in 2–4 sentences.
6. Vision — what outcome counts as project success?
```

### Block 3 — Current stage goal
```
7. What are we building / working on right now?
8. What is the specific deliverable for this stage?
```

*→ `quick` mode stops here. Remaining blocks are filled with `[to clarify]`.*

### Block 4 — Project structure
```
9. Describe the key elements, components, or layers of the project (freely, any format).
```

### Block 5 — Participants and dependencies
```
10. Who is involved in the project?
    List: stakeholders, partners, external dependencies — briefly for each.
```

### Block 6 — Constraints
```
11. Are there any constraints? Time, resources, risks — what matters?
```

### Block 7 — Data structure
```
12. Path to the input folder?
    List key files if any.
13. Path to the output folder?
    List already created files if any.
```

### Block 8 — Open questions
```
14. Are there known open questions or unresolved tasks?
    (List format, bullet points — any format works)
```

### Block 9 — Additional sections (optional)
```
15. Do you need additional sections?
    - Market context
    - Methodology
    - Stages / Roadmap
    Or none of the above?
```
If the user selects additional sections — ask 1–2 clarifying questions for each selected section.

---

## Step 3 — Generate the file

**Response processing rules:**
- Do not paste user answers verbatim
- Write each block as coherent structured text
- Preserve the user's terminology and phrasing
- Do not invent facts — only what the user stated
- Missing or unclear items → mark as `[to clarify]`
- Changelog: one entry with the file creation date

**Output filename:** `project-context.md`

---

## Output File Template
```markdown
# Project Context: [name]

## Basics

- **Type:** [value]
- **Status:** [value]
- **Start date:** [value]
- **Deadline:** [value or "Not defined"]

---

# Project Overview

[Coherent text based on answer 5]

# Vision

[Coherent text based on answer 6]

---

# Current Stage Goal

[Coherent text based on answers 7–8]

---

# Project Structure

[Coherent text based on answer 9]

---

# Participants and Dependencies

[Structured text based on answer 10]

---

# Constraints

[Text based on answer 11]

---

# Data Structure

Input: [input/ path]

Files:
[list from answer 12]

Output: [output/ path]

Files:
[list from answer 13]

---

# Open Questions

[List from answer 14, formatted as a tracker]

---

[Optional sections if selected]

---

# Changelog

| Date | Change |
|------|--------|
| [date] | Project context created |
```

---

## Step 4 — Deliver the file

After generation:
1. Create the file `project-context.md` with the generated content
2. Make it available for download
3. Briefly report: how many blocks are filled, how many are marked `[to clarify]`

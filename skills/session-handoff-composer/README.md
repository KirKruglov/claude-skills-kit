# Session Handoff Composer

Transfer your work context to a new session without losing a thing.

---

## Overview

Session Handoff Composer extracts the key elements of your current chat session — decisions made, tasks in progress, open questions, and next steps — and formats them into a structured, copy-paste-ready block. It solves the context loss problem that happens when a long session fills up and you have to start fresh. Use this skill when your Cowork session is approaching its context limit, when you want to pause and continue later, or when you need to switch focus areas mid-conversation.

---

## Requirements

- An active Cowork session with meaningful content (decisions, tasks, or ongoing work)
- No files or external tools required
- Works entirely from the current conversation context

**Recommended:** Use the skill when your session has at least 5–10 exchanges. Very short sessions produce minimal handoffs.

---

## How to Use

1. **Notice that your session is filling up (or decide to pause)**
   - You don't need to do anything to prepare — the skill reads the conversation automatically

2. **Trigger the skill by saying:**
   - "Compose handoff" or "Session handoff"
   - Or in Russian: "Составь хэндофф" or "Подготовь handoff-документ"

3. **Answer one clarifying question (if asked)**
   - The skill may ask one targeted question if something is ambiguous
   - You can also add any context it may have missed

4. **Copy the handoff block**
   - You receive a markdown code block ready to paste as the first message in your new session
   - An opener line is included: just copy it and paste below your handoff block

For detailed usage scenarios, see [docs/USER-GUIDE.md](docs/USER-GUIDE.md).

---

## Examples

### Example 1: Pausing a writing task mid-session

**Trigger:** "Compose handoff"

**Output:**
```markdown
## Session Handoff

**Topic:** Drafting Q2 product update email
**Date:** 2026-04-19
**Status:** in-progress

### Done
- Agreed on tone: concise, executive-friendly
- Drafted intro paragraph (approved)

### In Progress
- Body section: features list not yet finalized

### Open Questions
- Should we include pricing changes in this update?

### Files
- q2-update-draft.md — intro paragraph written, body incomplete

### Next Steps
1. Finalize the features list (3–4 bullets)
2. Add pricing section if decision is yes
3. Draft closing CTA

### Context for New Session
We're writing a Q2 product update for executive stakeholders. Tone is decided (concise, no jargon). Intro is done; body is stalled pending a pricing decision.
```

---

### Example 2: Context overflow on a research session

**Trigger:** "Session handoff — context is almost full"

**Output:**
```markdown
## Session Handoff

**Topic:** Competitive research — project management tools
**Date:** 2026-04-19
**Status:** paused

### Done
- Researched Asana and Notion (summaries written)
- Identified 3 key differentiators for each

### In Progress
- Linear: research started, not summarized yet

### Open Questions
- Should Monday.com be included? (not in original scope)

### Files
- competitive-research.md — Asana + Notion sections complete

### Next Steps
1. Summarize Linear research
2. Decide on Monday.com inclusion
3. Draft comparison table across all tools

### Context for New Session
Competitive research for PM tool selection. Asana and Notion are done. Linear is next. Comparison table to follow after all tools are researched.
```

---

## Triggers

Use any of these phrases to trigger the skill:

| English | Russian |
|---------|---------|
| Compose handoff | Составь хэндофф |
| Session handoff | Хэндофф сессии |
| Context is getting full, help me prepare | Контекст заполняется, помоги перенести |
| I need to continue this in a new session | Нужно продолжить в новой сессии |
| Prepare handoff document | Подготовь handoff-документ |

---

**Version:** 1.0.0
**Last updated:** 2026-04-19

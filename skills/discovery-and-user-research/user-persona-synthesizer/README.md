> [Версия на русском языке](README.ru.md)

# User Persona Synthesizer

Turn real interview transcripts into structured, evidence-backed user persona cards — no integrations, no templates to fill.

---

## Overview

User Persona Synthesizer extracts recurring user profiles from real CustDev interview transcripts and generates structured persona cards backed by verbatim quotes and respondent counts. Unlike synthetic persona generators, it only surfaces patterns that actually appear across multiple interviews. Use this skill when you've completed a batch of user interviews and need to synthesize findings into personas for product documents, roadmap discussions, or stakeholder presentations.

---

## Requirements

- Interview transcripts or notes (any format accepted: plain text, markdown, pasted content)
  - Works with raw interview notes, formatted transcripts, or mixed notes
  - Minimum 3 interviews recommended for meaningful patterns; works with fewer but adds a low-sample warning
- No additional tools or skills required

**Recommended:** Have at least 3–5 interviews ready. Very small samples (1–2 interviews) produce personas with a low-confidence warning.

---

## How to Use

1. **Gather your interview transcripts or notes**
   - Collect the files or notes from your CustDev sessions
   - Any format works: plain text, bullet notes, full transcripts

2. **Trigger the skill by saying:**
   - "Synthesize personas from my interviews"
   - "Create user personas from these transcripts"
   - Or in Russian: "Синтезируй персоны из интервью" or "Создай персоны из транскриптов"

3. **Provide the interview content**
   - Paste the transcripts or reference your files
   - Optionally specify focus: "focus on goals and frustrations" or "aim for 3 personas"

4. **Review your persona cards**
   - Receive a markdown document with a summary table, per-persona cards (with verbatim quotes), and synthesis notes
   - Copy into product documents, share with stakeholders, or use to drive roadmap decisions

---

## Examples

### Example 1: Synthesizing 5 SaaS Product Interviews

**Input:**
```
Interview 1 — Anna, Marketing Manager, B2B SaaS:
"I spend at least an hour every Monday pulling metrics from three different dashboards. I'd love to have one place where everything lives."
Goal: save reporting time. Frustration: tool fragmentation.

Interview 2 — Boris, Marketing Manager, E-commerce:
"I hate that every time I need to show leadership the results, I have to rebuild the same deck from scratch."
Goal: reusable reporting. Frustration: no templates.

Interview 3 — Carlos, Content Lead, Agency:
"Honestly, I just need to know what worked and what didn't. The tools give me too many numbers."
Goal: clear performance signal. Frustration: data overload.
...
```

**Output:**
```markdown
## User Persona Synthesis — 2026-05-18

**Source:** 5 interview transcripts
**Personas found:** 2
**Total respondents mapped:** 5 of 5

### Summary Table

| Persona | Respondents | Top Attributes |
|---------|-------------|----------------|
| The Overwhelmed Reporter | 3 of 5 | weekly reporting, tool fragmentation, time loss |
| The Clarity Seeker | 2 of 5 | data overload, needs signal not noise |

### Persona 1: The Overwhelmed Reporter
**Respondents:** 3 of 5
**Goals:** Save time on reporting; create reusable reports
**Frustrations:** Switching between tools; rebuilding decks every week
**Key quotes:**
> "I spend at least an hour every Monday pulling metrics from three different dashboards."

### Persona 2: The Clarity Seeker
**Goals:** Understand what worked and what didn't
**Frustrations:** Too many metrics, no clear signal
**Key quotes:**
> "The tools give me too many numbers."
```

---

### Example 2: 3 Interviews, Low Sample Warning

**Input:** 3 interviews with a product manager, a designer, and a developer

**Output:** Two persona cards are generated (PM + Designer as one cluster; developer as second), plus a warning: "Low sample size (3 interviews) — patterns may not be representative. Consider adding more interviews before sharing with stakeholders."

---

## Triggers

Use any of these phrases to trigger the skill:

| English | Russian |
|---------|---------|
| Synthesize personas from interviews | Синтезируй персоны из интервью |
| Create user personas | Создай пользовательские персоны |
| Extract personas from transcripts | Извлеки персоны из транскриптов |
| I have interview notes and need personas | У меня есть транскрипты — сделай персоны |

---

**Version:** 1.0.0
**Last updated:** 2026-05-18

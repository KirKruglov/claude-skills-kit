> [Версия на русском языке](README.ru.md)

# Research to Content Brief

Turn your research notes into a ready-to-use content brief — without the interview.

---

## Overview

Research to Content Brief reads a folder of raw research notes (audience observations, competitor signals, trend snippets) and synthesizes them into a structured content brief with six sections: Audience, Core Message, Content Angles, Competitive Differentiation, Trend Hooks, and Recommended Formats. Unlike dialogue-based brief generators that start from scratch, this skill works from your existing research files — the output is ready to hand off to a writer or use as a creation checklist. Use this skill when you have a folder of accumulated research and need to turn it into an actionable brief, when you want to consolidate audience and competitor notes before briefing a writer, or when you're starting content production after a research sprint.

---

## Requirements

- A folder with research notes in `.md` or `.txt` format, OR research content pasted directly into chat
  - Supported note types: audience observations, competitor signals, trend snippets, mixed notes
  - Minimum 1 file; optimal 3–10 files across categories
- Optional: target content format hint (blog post, landing page, social, email)
- No additional tools or skills required

---

## How to Use

1. **Gather your research files**
   - Collect your audience notes, competitor observations, and trend snippets into one folder
   - Files can be named anything; the skill categorizes them automatically

2. **Trigger the skill**
   - Say: "Research to content brief" and provide the folder path
   - Or: "Create content brief from my notes" and paste your research directly
   - In Russian: "Составь контент-бриф из заметок" or "Бриф из исследований"

3. **Optionally specify the target format**
   - Add: "for a blog post", "for a landing page", or "for social media"
   - The skill adjusts angle framing and format recommendations accordingly

4. **Review and use the brief**
   - Receive a `content-brief.md` with six sections
   - Sections with no source data are flagged — fill them manually before briefing a writer

---

## Examples

### Example 1: Brief from Three Research Files

**Input:**
```
Folder: /research/q2-campaign/
Files:
- audience-notes.md (pain points of mid-market PMs)
- competitor-signals.md (what Notion, Linear say about product planning)
- trends-june.md (AI-in-PM trends spotted this week)
```

**Action:** Skill reads all three files, categorizes them, extracts audience pain points, competitor gaps, and trend hooks, then synthesizes a brief.

**Output:**
```markdown
# Content Brief: AI-assisted product planning for mid-market PMs

**Generated:** 2026-06-05
**Source files:** audience-notes.md, competitor-signals.md, trends-june.md
**Target format:** unspecified

## Audience
- **Who they are:** Mid-market product managers (10–200 person orgs), managing 2–4 squads
- **Pain points:** Overwhelmed by manual status updates; no single source of truth for planning
- **Jobs to be done:** Communicate planning decisions to stakeholders without spending hours in docs

## Core Message
Mid-market PMs can reclaim 3+ hours per week by using AI to automate the synthesis layer — turning notes and updates into decisions and briefs without manual compilation.

## Content Angles
1. "The synthesis tax": why PMs spend 30% of their time formatting, not deciding — and how AI removes it
2. What Notion and Linear don't tell you about planning automation (gap spotted in competitor signals)

## Competitive Differentiation
- **What competitors say:** Planning is about structure and workflows
- **Gap:** Neither addresses the synthesis burden between raw notes and stakeholder-ready docs
- **Differentiation point:** Lead with synthesis as the real bottleneck, not structure

## Trend Hooks
- "AI copilots for PMs" growing fast in 2026 — frame as "what the next generation of PM tools gets right" (trends-june.md)

## Recommended Formats
- Long-form blog post: audiences engages with "real pain + concrete solution" narrative
- LinkedIn post: punchy "3 hours back per week" hook to drive top-of-funnel
```

---

### Example 2: Brief from a Single Mixed Notes File

**Input:**
```
Paste of mixed-notes.md containing: audience frustrations + one competitor mention + two trend observations
```

**Action:** Skill auto-categorizes the content, extracts what's available, flags the missing competitor and trend sections.

**Output:**
```markdown
# Content Brief: [derived from content]

## Audience
[Extracted from audience signals in the file]

## Competitive Differentiation
NEEDS MANUAL INPUT — no competitor source data

## Trend Hooks
[Two trends extracted from notes]

...

Source coverage:
- Audience notes: 1 file (mixed-notes.md)
- Competitor signals: none ⚠️ NEEDS MANUAL INPUT
- Trend snippets: 1 file (mixed-notes.md)
```

---

## Triggers

Use any of these phrases to trigger the skill:

| English | Russian |
|---------|---------|
| Research to content brief | Бриф из исследований |
| Create content brief from my notes | Составь контент-бриф из заметок |
| Turn my research notes into a brief | Преобразуй research-заметки в бриф |
| Write content brief from research folder | Создай контент-бриф из папки с исследованиями |

---

**Version:** 1.0.0
**User guide:** [docs/USER-GUIDE.md](docs/USER-GUIDE.md) | [docs/USER-GUIDE.ru.md](docs/USER-GUIDE.ru.md)

# Industry Trend Brief

Turn your weekly reading pile into a structured trend signals brief for your product team — in minutes, without leaving Cowork.

---

## Overview

Industry Trend Brief synthesizes a folder of saved articles, blog posts, and text fragments into a concise weekly brief with ranked trend themes and actionable product team takeaways. It works entirely from local files — no web access or API needed. Use this skill when you want to extract signal from your reading before a planning session, share a weekly trend brief with your team, or turn scattered clippings into a structured summary for roadmap discussions.

---

## Requirements

- A folder containing articles or text fragments in md or txt format
  - Content can be copy-pasted articles, saved blog posts, newsletter excerpts, or research notes
  - One file per article is recommended, but multi-topic files work too
- No external tools, APIs, or internet access required

**Recommended:** 3–10 files covering different topics work best. The skill handles 1 file (single-topic brief) and 15+ files (large brief) but optimal output comes from a focused weekly reading set.

---

## How to Use

1. **Collect your reading material**
   - Save articles, excerpts, or notes as md or txt files into a folder
   - Name files descriptively (e.g., `ai-tools-article.md`, `market-trends-notes.txt`)

2. **Trigger the skill**
   - Say: "Industry trend brief from [folder path]"
   - Or: "Trend signals from articles in [folder path]"
   - In Russian: "Тренд-бриф из статей в [путь к папке]"

3. **The skill processes your files**
   - It scans all md/txt files, extracts key signals, groups them by theme, and ranks by signal strength

4. **Review your brief**
   - Receive a markdown brief with executive summary, ranked theme sections, and a "What to Watch" list
   - Each theme includes key signals with source filenames and a one-sentence takeaway for your product team

---

## Examples

### Example 1: Weekly PM Reading Pile

**Input:** Folder with 5 files — 3 articles about AI tools in enterprise, 1 article about no-code platform growth, 1 article about developer tool adoption patterns.

**Action:** Skill extracts signals, groups into 2 themes (AI Tools Adoption, Low-Code/No-Code Growth), ranks both as High signal strength.

**Output:**
```
## Industry Trend Brief — 2026-05-29

Processed 5 files. Identified 2 themes.

**Summary:** Enterprise AI tool adoption is accelerating with concrete ROI data emerging, while no-code platforms are gaining traction with non-technical teams.

---

### Theme 1: Enterprise AI Tool Adoption
**Signal strength:** High
**Key signals:**
- 67% of enterprise teams report productivity gains from AI coding assistants *(Source: ai-tools-article.md)*
- Microsoft Copilot adoption up 3x in Q1 2026 *(Source: ai-tools-article.md)*
- Resistance shifting from "if" to "how fast" *(Source: enterprise-ai-notes.md)*
**Takeaway for product team:** Customers are past the evaluation stage — focus on integration depth and workflow fit, not AI feature announcements.

### Theme 2: No-Code / Low-Code Platform Growth
**Signal strength:** High
**Key signals:**
- No-code platform market grew 28% YoY *(Source: nocode-growth.md)*
- Non-technical users self-building internal tools in 40% of SMBs surveyed
**Takeaway for product team:** Consider how your product can serve non-technical users building their own workflows — this is a fast-growing segment.

---

### What to Watch
- Developer tool consolidation trend — vendors merging CLI and IDE tooling *(Source: devtools-adoption.md)*

---
*Brief generated from 5 files. 2 themes identified.*
```

---

### Example 2: Single-Topic Deep Dive

**Input:** Folder with 3 files all covering the same topic — product-led growth trends in B2B SaaS.

**Action:** Skill detects single-topic coverage, generates a deep-dive brief with detailed signal extraction.

**Output:**
```
## Industry Trend Brief — 2026-05-29

Processed 3 files. All content covers one theme — single-topic brief generated.

**Summary:** Product-led growth is maturing as a go-to-market strategy, with increasing emphasis on hybrid PLG+sales motions for mid-market expansion.

---

### Theme: Product-Led Growth in B2B SaaS
**Signal strength:** High
**Key signals:**
- 78% of new SaaS unicorns use PLG as primary acquisition channel *(Source: plg-trends-2026.md)*
- "PLG + sales" hybrid model becoming standard for $50K+ ACV deals *(Source: gtm-shifts.md)*
- Free tier conversion rates improving with in-product nudging vs. email nurture *(Source: conversion-notes.md)*
**Takeaway for product team:** If targeting mid-market expansion, design for a hand-off point from self-serve to sales — don't treat PLG as a pure replacement.

---

### What to Watch
- Community-led growth emerging as PLG complement in developer-focused tools *(Source: plg-trends-2026.md)*
```

---

## Triggers

Use any of these phrases to trigger the skill:

| English | Russian |
|---------|---------|
| Industry trend brief | Тренд-бриф из статей |
| Trend signals from articles | Сигналы трендов из папки |
| Summarize my industry reading | Создай brief по трендам |
| What trends matter this week | Что важно из моих статей на этой неделе |
| Weekly trend brief from [folder] | Еженедельный тренд-бриф из [папки] |

---

**Version:** 1.0.0
**Last updated:** 2026-05-29

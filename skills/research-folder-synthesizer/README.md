# Research Folder Synthesizer

Turn a folder of scattered research files into a structured thematic report — no manual sorting required.

---

## Overview

Research Folder Synthesizer reads a collection of local files (markdown notes, plain-text articles, research excerpts) and produces a single structured report with named themes, key findings, contradictions, and a source index. It clusters ideas across files, surfaces what different sources agree or disagree on, and delivers an executive summary ready to use as input for reports, PRDs, strategy documents, or presentations. Use this skill after a research sprint when you have 5–20 files and need to make sense of them before writing.

---

## Requirements

- A folder containing local research files (`.md`, `.txt`, plain text)
  - Works best with 3–20 files; larger folders are supported with reduced per-file depth
  - Supported formats: Markdown, plain text, pasted excerpts
- No API keys, external services, or internet connection required

**Optional:** A focus question (e.g., "What do users say about onboarding?") to guide thematic clustering.

---

## How to Use

1. **Gather your research folder**
   - Collect notes, article excerpts, and research files into one folder
   - Ensure files are in `.md` or `.txt` format (binary files will be skipped)

2. **Trigger the skill by saying:**
   - "Synthesize my research folder"
   - "Research synthesis — [folder name]"
   - In Russian: "Синтезируй папку с исследованиями" or "Сведи файлы в отчёт"

3. **Provide the folder path or file list**
   - Point to the folder, or paste file contents directly
   - Optionally add a focus question: "Focus on user pain points"

4. **Receive your synthesis report**
   - Get `research-synthesis.md` with: executive summary, themes, key findings, contradictions/gaps, and source index
   - Use it as the foundation for your next document

---

## Examples

### Example 1: Synthesizing competitor research notes

**Input:**
```
Folder: /research/competitor-analysis/
Files: competitor-a-notes.md, competitor-b-notes.md, market-overview.txt
Focus question: "Where are competitors weakest?"
```

**Output (`research-synthesis.md`):**
```markdown
# Research Synthesis: competitor-analysis
**Date:** 2026-04-30
**Files processed:** 3
**Focus question:** Where are competitors weakest?

## Executive Summary
The three sources converge on onboarding friction and limited mobile support as shared competitor weaknesses. Competitor A leads on analytics but lags in mobile UX; Competitor B is strong on integrations but lacks self-serve onboarding. No source addresses pricing transparency, suggesting a potential gap in available data.

## Themes

### Theme 1: Onboarding Friction
Both Competitor A and B require manual setup steps that slow activation. Users report 3–7 day time-to-value.
**Sources:** competitor-a-notes.md, competitor-b-notes.md

### Theme 2: Mobile Experience
Competitor A's mobile app has a 2.8 star rating; Competitor B has no native mobile app.
**Sources:** competitor-a-notes.md, market-overview.txt

## Key Findings
- Competitor A time-to-value: 5–7 days *(competitor-a-notes.md)*
- Competitor B has no mobile app as of Q1 2026 *(market-overview.txt)*

## Contradictions & Gaps
- **Contradiction:** competitor-a-notes.md rates support as "excellent"; market-overview.txt rates it "average."
- **Gap:** Pricing transparency not addressed in any source.

## Source Index
| File | Type | Main Topic | Language |
|------|------|------------|----------|
| competitor-a-notes.md | Markdown | Competitor A analysis | EN |
| competitor-b-notes.md | Markdown | Competitor B analysis | EN |
| market-overview.txt | Plain text | Market landscape | EN |
```

---

### Example 2: Consolidating UX research notes before writing a PRD

**Input:**
```
Folder: /research/ux-sprint-2026-04/
Files: interview-notes-1.md, interview-notes-2.md, survey-summary.txt, usability-test-findings.md
```

**Output excerpt:**
```markdown
## Executive Summary
Four sources from the April 2026 UX sprint consistently identify navigation complexity and slow search as primary pain points. Interview data reveals emotional friction ("I always get lost"); usability tests quantify it (avg. 4.2 clicks to reach core feature). Survey data confirms broad scope: 67% of respondents rated navigation as "confusing."

## Themes

### Theme 1: Navigation Complexity
Users struggle to find core features; average click depth is 4.2 (target: ≤2).
**Sources:** interview-notes-1.md, usability-test-findings.md

### Theme 2: Search Performance
Search results are slow (avg. 3.8s) and return irrelevant results.
**Sources:** interview-notes-2.md, survey-summary.txt

## Contradictions & Gaps
- **Contradiction:** interview-notes-1.md describes search as "broken"; survey-summary.txt shows 52% satisfaction with search.
- **Gap:** Mobile-specific pain points not addressed in any source.
```

---

## Triggers

Use any of these phrases to trigger the skill:

| English | Russian |
|---------|---------|
| Synthesize my research folder | Синтезируй папку с исследованиями |
| Research synthesis | Синтез ресёрча |
| Summarize all files in this folder | Сведи все файлы в отчёт |
| Turn my research notes into a report | Преобразуй мои заметки в структурированный отчёт |
| Consolidate my research files | Собери мои исследования в один отчёт |

---

**Version:** 1.0.0
**Last updated:** 2026-04-30

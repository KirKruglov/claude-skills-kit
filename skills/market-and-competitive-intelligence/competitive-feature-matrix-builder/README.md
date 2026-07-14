> [Версия на русском языке](README.ru.md)

# Competitive Feature Matrix Builder

Turn a folder of competitor notes into a structured feature comparison table and gap analysis — no web access, no API, fully offline.

---

## Overview

Competitive Feature Matrix Builder reads your local competitor research notes (md or txt files) and outputs a ready-to-share markdown matrix showing which features each competitor has, alongside a prioritized gap analysis. It works entirely from your files — no internet search or external API required. Use this skill when you need to consolidate scattered competitor notes before a roadmap session, run a quarterly competitive review, or identify which features to prioritize based on market coverage.

---

## Requirements

- A folder containing competitor research notes in `.md` or `.txt` format (one file per competitor recommended)
- Optional: a file named `your-product.md` or `own-product.md` in the same folder for self-comparison and gap analysis
- No additional tools, APIs, or web access required

**Recommended:** 2–6 competitor files, each with at least 5–10 feature-level notes per competitor. The more structured your notes (bullet lists, headings), the more accurate the extraction.

---

## How to Use

1. **Gather your competitor notes**
   - Save each competitor's research in a separate `.md` or `.txt` file (e.g., `salesforce.md`, `hubspot.md`)
   - Optionally add `your-product.md` with your own feature list for gap comparison

2. **Trigger the skill by saying:**
   - "Build a competitive feature matrix from my notes folder"
   - "Competitive feature matrix"
   - In Russian: "Составь feature matrix" or "Матрица фич конкурентов"

3. **Provide the folder path**
   - Share the path to your notes folder (or have it open in Cowork)
   - The skill will scan all md/txt files, extract features, and normalize them

4. **Review the output**
   - Get a Feature Matrix table, Gap Analysis section, and Recommendations
   - Copy the markdown to your roadmap doc, slide deck, or share with your team

---

## Examples

### Example 1: Three-Competitor SaaS Analysis

**Input:**
```
Folder: /competitive-research/
Files: hubspot.md, salesforce.md, pipedrive.md, your-product.md
```

**Action:** Skill scans 4 files, extracts competitor names from headings, normalizes 12 features across all files.

**Output (excerpt):**
```markdown
Processed 4 files: HubSpot, Salesforce, Pipedrive, Your Product. Matrix covers 12 features.

## Feature Matrix

| Feature | HubSpot | Salesforce | Pipedrive | Your Product |
|---------|:---:|:---:|:---:|:---:|
| Email Sequences | ✓ | ✓ | ✓ | ✗ |
| Mobile App | ✓ | ✓ | ✓ | ✓ |
| AI Lead Scoring | ✓ | ✓ | ✗ | ✗ |
| Pipeline Automation | ✓ | ✓ | ✓ | ✓ |

## Gap Analysis

| Feature | Competitors With It | Priority |
|---------|---------------------|---------|
| Email Sequences | HubSpot, Salesforce, Pipedrive | High |
| AI Lead Scoring | HubSpot, Salesforce | Medium |
```

---

### Example 2: Two-Competitor Review Without Self-Comparison

**Input:**
```
Folder: /research/q2-competitive/
Files: notion-notes.txt, coda-notes.txt
```

**Action:** Skill scans 2 files, extracts feature lists from bullet points and prose, builds a 2-column matrix.

**Output (excerpt):**
```markdown
Processed 2 files: Notion, Coda. Matrix covers 8 features.
Note: Add a file named `your-product.md` to enable self-comparison and gap analysis.

## Feature Matrix

| Feature | Notion | Coda |
|---------|:---:|:---:|
| Database Views | ✓ | ✓ |
| Automation / Workflows | ? | ✓ |
| AI Writing Assistant | ✓ | ✓ |
| Formula Language | ✗ | ✓ |

*Legend: ✓ = confirmed present, ✗ = confirmed absent, ? = not mentioned in notes*
```

---

## Triggers

Use any of these phrases to trigger the skill:

| English | Russian |
|---------|---------|
| Build feature matrix | Составь feature matrix |
| Competitive feature matrix | Матрица фич конкурентов |
| Compare competitors from notes | Сравни конкурентов по файлам |
| Analyze competitive notes | Построй конкурентную матрицу |
| Build a comparison table from my competitor files | Проанализируй мои конкурентные заметки |

---

**Version:** 1.0.0
**Last updated:** 2026-05-28

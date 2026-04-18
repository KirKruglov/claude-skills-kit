# OKR Progress Narrator

**Transform raw OKR data into a readable stakeholder update — automatically.**

[![Skills](https://img.shields.io/badge/claude--skills--kit-okr--progress--narrator-blue)](https://github.com/KirKruglov/claude-skills-kit)

---

## What it does

OKR Progress Narrator takes your raw OKR data — a table, a list, a CSV, or text pasted in chat — and converts it into a clean narrative update ready to share with stakeholders.

Instead of copying metrics into a manually written report, you get:
- An **executive summary** in 2–4 sentences
- A **per-objective narrative** explaining momentum and risks in plain language
- A **KR status table** with progress percentages and color-coded status
- A **key risks block** listing at-risk and off-track items
- An **optional next steps section** if your data includes planned actions

Output: `okr-update-YYYY-MM-DD.md`

---

## Trigger phrases

**English:**
> "okr update"  
> "narrate okr progress"  
> "stakeholder okr update"  
> "generate okr report"  
> "write okr status update"

**Russian:**
> «okr апдейт»  
> «нарратив по OKR»  
> «прогресс-апдейт для стейкхолдеров»  
> «оформи OKR»  
> «прогресс по целям»

---

## Input formats

The skill accepts OKR data in any of these formats:

| Format | Example |
|--------|---------|
| Markdown table | `\| Objective \| KR \| Current \| Target \|` |
| Indented list | `O1: Grow revenue` / `- KR1.1: ARR $500K` |
| CSV / TSV file | Any file with Objective, KR, Current, Target columns |
| Free-form text | Plain description of goals and progress |

**Optional parameters you can specify:**
- Period: `Q2 2026`, `April`, `Sprint 12`
- Audience: `CEO`, `board`, `team` (affects narrative depth)
- Focus: `at-risk only` or `highlights only`

---

## Example

**Input (pasted in chat):**
```
Q1 2026 OKRs

Objective 1: Grow MRR to $200K
- KR1: New MRR — current $42K, target $50K, notes: pipeline healthy
- KR2: Churn rate — current 3.2%, target <2.5%, notes: retention at risk

Objective 2: Launch mobile app
- KR1: App store release — done ✅
- KR2: 1000 DAU week 4 — current 680, target 1000
```

**Output excerpt:**
```markdown
# OKR Progress Update — Q1 2026
**Prepared:** 2026-04-18

## Executive Summary
1 of 2 objectives is on track. The mobile app has shipped and is building 
an active user base ahead of the DAU target. Revenue growth is progressing 
but churn risk requires immediate attention.

## Objectives

### Grow MRR to $200K — 🟡 At Risk
New MRR is tracking at 84% of the Q1 sub-target with strong pipeline 
signals. However, churn has exceeded the target threshold, which may 
offset acquisition gains if not addressed this quarter.
...
```

---

## Installation

1. Download `SKILL.md` from this folder
2. Place it in your Claude Cowork skills directory, or paste the contents into a Project instruction
3. Use any trigger phrase to activate

---

## License

MIT — [claude-skills-kit](https://github.com/KirKruglov/claude-skills-kit)

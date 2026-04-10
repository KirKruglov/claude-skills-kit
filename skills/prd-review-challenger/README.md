# PRD Review Challenger — AI Devil's Advocate for Product Documents

Find the gaps in your PRD before your team does.

---

## What It Does

`prd-review-challenger` is a Claude skill that critically reviews product requirements documents, feature specs, and product decisions. It plays devil's advocate — surfacing weak assumptions, missing requirements, implementation risks, and logical gaps before a document goes to the team or into development.

Unlike tools that summarize or rewrite PRDs, this skill challenges them. It asks the uncomfortable questions that engineers and designers will ask anyway — only earlier, when fixes cost less.

---

## How It Works

Paste your PRD or feature spec into a conversation with Claude. The skill runs a structured four-part critique:

**1. Weak spots and hidden assumptions** — statements treated as facts that haven't been validated or explained.

**2. Open questions** — what the document doesn't answer but developers and designers will definitely ask.

**3. Implementation and UX risks** — technical complexity, dependencies, and friction points users will encounter.

**4. Alternative approaches** — 2–3 other ways to solve the problem, so the chosen solution is a deliberate choice, not a default.

Plus a **completeness checklist** — whether the PRD covers user stories, acceptance criteria, edge cases, success metrics, rollback plan, and more.

---

## Quick Start

1. Install the skill (see `docs/INSTALL.md`)
2. Open a conversation with Claude
3. Type: `"Review my PRD"` and paste your document
4. Get a structured critique in seconds

---

## Example Triggers

```
Review my PRD
Challenge my spec
Devil's advocate for my product doc
Find holes in my PRD
Critique my feature spec
Stress-test my PRD
What's missing in my spec
```

---

## Who It's For

Product Managers who want to find holes in their own PRDs before peer review. Team leads validating a spec before development starts. Anyone reviewing another PM's document and wanting a structured critique framework.

---

## Requirements

- Claude account (free or paid)
- Claude.ai Projects, Claude Cowork, or Claude Code
- No additional connectors or integrations needed

---

## What It Doesn't Do

- Does not write or rewrite PRDs (see the product-management write-spec skill for that)
- Does not replace review with actual stakeholders, engineers, and designers
- Does not have domain knowledge about your specific product without context you provide

---

## Files in This Package

```
prd-review-challenger/
├── SKILL.md              — Skill instructions (bilingual EN/RU)
├── skill-spec-ru.md      — Source specification (RU)
├── README.md             — This file (EN)
├── README.ru.md          — Overview in Russian
├── evals.json            — Test cases for quality validation
└── docs/
    ├── INSTALL.md        — Installation guide (EN)
    ├── INSTALL.ru.md     — Installation guide (RU)
    ├── USER-GUIDE.md     — Usage guide (EN)
    └── USER-GUIDE.ru.md  — Usage guide (RU)
```

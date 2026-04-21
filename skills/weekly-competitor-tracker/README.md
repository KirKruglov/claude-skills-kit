# Weekly Competitor Tracker

Stay on top of what your competitors are doing — without spreadsheets, subscriptions, or code.

---

## Overview

Weekly Competitor Tracker generates a delta-report from your markdown competitor notes, showing exactly what changed since last week. You maintain a simple folder of `.md` files (one per competitor), and the skill diffs this week's notes against last week's snapshot to surface new pricing, product changes, and messaging shifts. Use this skill when preparing for Monday strategy reviews, planning roadmap sessions, or briefing your team on competitive landscape changes.

---

## Requirements

- A `competitors/` folder with one `.md` file per competitor
  - Each file can use any structure; H2 headers (`## Pricing`, `## Product`, etc.) improve diff quality
  - Supported format: plain markdown (`.md`)
- Optional: `competitors/snapshot/` subfolder with last week's versions of the same files
  - If no snapshot exists, the skill runs in baseline mode (first-run summary, no diff)
- No external tools, APIs, or installations required — runs entirely in Cowork/Claude

**Recommended file structure per competitor:**
```markdown
## Product
[key facts about product features]

## Pricing
[pricing tiers, plans, pricing changes]

## Messaging
[tagline, positioning, homepage copy]

## Recent News
[latest announcements, blog posts, news items]
```

---

## How to Use

1. **Prepare your competitor notes folder**
   - Create a `competitors/` folder with one `.md` file per competitor (e.g., `acme.md`, `rival.md`)
   - Update current-week notes in each file before running the skill

2. **Trigger the skill by saying:**
   - "Track competitor changes" or "Weekly competitor report"
   - In Russian: "Отследи изменения конкурентов" or "Дельта-отчёт по конкурентам"
   - Provide the path to your `competitors/` folder

3. **The skill reads and compares your files**
   - If `competitors/snapshot/` exists: performs section-by-section diff vs. last week
   - If no snapshot exists: generates a baseline summary (first run)

4. **Review the delta-report**
   - Receive `competitor-delta-YYYY-MM-DD.md` saved to your `competitors/` folder
   - High-significance changes (pricing, product) are flagged 🔴; minor changes 🟡; no changes 🟢

5. **Update your snapshot**
   - After reviewing the report, copy current files to `competitors/snapshot/` to set the new baseline for next week

---

## Examples

### Example 1: Weekly Monday Review (with snapshot)

**Setup:**
```
competitors/
├── acme.md          ← updated this week
├── rival.md         ← updated this week
└── snapshot/
    ├── acme.md      ← last week's version
    └── rival.md     ← last week's version
```

**Action:** Trigger "Weekly competitor report" with the `competitors/` folder path.

**Output (excerpt):**
```markdown
# Competitor Delta Report — 2026-04-21

**Period:** 2026-04-14 → 2026-04-21
**Competitors tracked:** 2
**Changes detected:** 2 (High: 1, Medium: 1, Low: 0)

## Acme

**Overall:** 🔴 Significant changes

### What Changed
| Section | Change | Significance |
|---------|--------|-------------|
| Pricing | New Starter plan added at $49/mo | High |

### Unchanged
- Product: no changes detected
```

---

### Example 2: First Run (no snapshot — baseline mode)

**Setup:**
```
competitors/
├── acme.md
└── rival.md
```
*(no snapshot/ folder)*

**Action:** Trigger "Track competitor changes".

**Output (excerpt):**
```markdown
# Competitor Delta Report — 2026-04-21

⚠️ First Run — No Snapshot Found
This is your baseline report. To enable delta tracking next week,
copy all files from `competitors/` to `competitors/snapshot/`.

## Acme

### Baseline Summary
**Product:** Team collaboration tool with real-time editing.
**Pricing:** Free tier + Pro at $12/user/mo + Enterprise custom.
**Messaging:** "Work better together."
```

---

## Triggers

Use any of these phrases to trigger the skill:

| English | Russian |
|---------|---------|
| Track competitor changes | Отследи изменения конкурентов |
| Weekly competitor report | Еженедельный отчёт по конкурентам |
| What changed with my competitors | Что изменилось у конкурентов |
| Competitor delta this week | Дельта-отчёт по конкурентам за неделю |
| Generate competitor delta report | Сформируй дельта-отчёт по конкурентам |

---

**Version:** 1.0.0
**Last updated:** 2026-04-21

> 📖 See [docs/USER-GUIDE.md](docs/USER-GUIDE.md) for detailed usage scenarios and tips.

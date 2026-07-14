> [Версия на русском языке](README.ru.md)

# Skill Usage Log Reviewer

Audit your installed Claude skill collection and get a deactivation checklist to keep your portfolio lean.

---

## Overview

Skill Usage Log Reviewer analyses your installed Claude skills, flags which are unused or redundant, and generates a structured audit report with a one-click deactivation checklist. As skill collections grow, each installed skill adds tokens to every session — even skills you never trigger. Use this skill when your list of installed skills has grown to 10 or more, your sessions feel slower or noisier, or you want a quarterly check-up of your skill portfolio.

---

## Requirements

- A list of your installed skill names (paste from settings, an `ls` output, or a description)
- Optional: brief usage notes per skill ("used daily", "tried once", "never used")
- No additional tools or file uploads required

---

## How to Use

1. **Prepare your skill list**
   - Open your Claude settings and look at the active skills, or paste the names of installed skills
   - Optionally add a quick note next to each: "used weekly", "installed but never used", etc.

2. **Trigger the skill**
   - Say: "Audit my skills" or "Skill usage review"
   - In Russian: "Аудит скилов" or "Обзор использования скилов"

3. **Answer usage questions (if asked)**
   - The skill will ask which skills you use daily / weekly / monthly / never
   - Questions are batched — answer for groups of 5–8 skills at once

4. **Review your audit report**
   - Get a table with Keep / Review / Deactivate verdicts per skill
   - Use the Deactivation Checklist to remove unused skills from your settings

---

## Examples

### Example 1: Cleaning up a 12-skill collection

**Input:**
```
morning-standup-brief-generator — used daily
session-handoff-composer — used weekly
weekly-competitor-tracker — installed 3 weeks ago, never used
meeting-prep-briefer — used occasionally
one-to-one-prep — used once
context-window-health-check — used weekly
retro-pattern-analyzer — never used
okr-progress-narrator — installed, tried once
team-update-aggregator — used monthly
weekly-ai-workflow-review — used weekly
delegation-brief — installed, not sure what it does
feature-guide — used a few times
```

**Action:** Skill classifies usage tiers, detects that meeting-prep-briefer and one-to-one-prep overlap in purpose, flags 4 skills as Deactivate.

**Output:**
```markdown
# Skill Audit Report
**Date:** 2026-05-05
**Total skills audited:** 12
**Keep:** 6 | **Review:** 2 | **Deactivate:** 4

## Summary
Collection is moderately bloated — 4 skills can be deactivated immediately, saving ~1,200 tokens per session.

## Audit Table

| Skill | Verdict | Reason |
|-------|---------|--------|
| weekly-competitor-tracker | ❌ Deactivate | Never used in 3 weeks since install |
| retro-pattern-analyzer | ❌ Deactivate | Never used; niche use case not matching workflow |
| okr-progress-narrator | ❌ Deactivate | Tried once; superseded by team-update-aggregator |
| delegation-brief | ❌ Deactivate | Never triggered; purpose unclear to user |
| one-to-one-prep | ⚠️ Review | Overlaps with meeting-prep-briefer; used once |
| feature-guide | ⚠️ Review | Used a few times; consider if still needed |
| morning-standup-brief-generator | ✅ Keep | Used daily |
...
```

---

### Example 2: Small collection health check

**Input:**
```
prompt-library-curator, session-handoff-composer, context-window-health-check, feature-guide, report-analyzer
```

**Action:** Skill runs audit on 5 skills, finds all are occasionally or actively used, no duplicates.

**Output:**
```markdown
# Skill Audit Report
**Date:** 2026-05-05
**Total skills audited:** 5
**Keep:** 4 | **Review:** 1 | **Deactivate:** 0

## Summary
Collection is healthy. No deactivations recommended.

## Deactivation Checklist
No skills recommended for deactivation.

## Notes
Your collection is small — deactivating is optional. Focus on keeping only what you actually trigger.
```

---

## Triggers

Use any of these phrases to trigger the skill:

| English | Russian |
|---------|---------|
| Audit my skills | Аудит скилов |
| Skill usage review | Обзор использования скилов |
| Which skills should I deactivate | Какие скилы деактивировать |
| Review my installed skills | Проверь мои установленные скилы |
| Clean up my skill collection | Почисти мою коллекцию скилов |

---

**Version:** 1.0.0
**Last updated:** 2026-05-05

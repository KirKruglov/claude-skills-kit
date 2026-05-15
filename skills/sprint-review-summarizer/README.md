# Sprint Review Summarizer

Turn your raw sprint notes into a structured stakeholder document in seconds — no Jira, no YAML, no integrations needed.

---

## Overview

Sprint Review Summarizer transforms plain-language sprint notes into a structured document with four sections: delivered items, deferred work, risks and issues, and next sprint focus. It reads any free-form text or markdown file and produces a ready-to-share stakeholder update with an executive summary and completion metric. Use this skill when preparing for a sprint review meeting, drafting a stakeholder update after each sprint, or converting rough PM notes into a structured report.

---

## Requirements

- Sprint notes as pasted text or a markdown file (any structure accepted)
  - Bullet lists, paragraphs, or mixed-format notes all work
  - No specific formatting required
- Optional: sprint number, team name, dates, sprint goal (used for metadata if provided)
- No external tools, plugins, or integrations required

---

## How to Use

1. **Gather your sprint notes**
   - Write a free-form summary of the sprint, or use existing notes
   - Notes can be bullet points, paragraphs, or a mix — any structure works

2. **Trigger the skill by saying:**
   - "Sprint review summary" or "Summarize sprint results"
   - In Russian: "Итоги спринта" or "Оформи итоги спринта"

3. **Provide the sprint notes**
   - Paste the notes directly into the chat
   - Or reference a local file path if working in Cowork

4. **Review your stakeholder document**
   - Receive a markdown document with all four sections plus an executive summary
   - Copy and paste directly into email, Slack, or your project wiki

---

## Examples

### Example 1: End-of-Sprint PM Notes

**Input:**
```
Sprint 24, May 5–19, Product team

Shipped the new onboarding flow — all 3 screens done and in production.
Fixed the login bug that was blocking mobile users.
The analytics dashboard got pushed to next sprint — design wasn't ready in time.
We're blocked on the payment integration because the vendor API docs are outdated.
Next sprint: focus on payment integration and start the A/B test setup.
Decision: we agreed to delay the v2 launch by one week to polish onboarding.
```

**Output:**
```markdown
## Sprint Review: Sprint 24

**Team:** Product team
**Sprint dates:** May 5–19
**Summary:** 2 of 3 items delivered; 1 deferred due to design delay; payment integration blocked by vendor.

---

### ✅ Delivered
- New onboarding flow — all 3 screens live in production
- Login bug fix — mobile users unblocked

### ⏩ Deferred
- Analytics dashboard — design not ready in time; moved to next sprint

### ⚠️ Risks & Issues
- Payment integration blocked: vendor API documentation is outdated

### 🎯 Next Sprint Focus
- Payment integration
- A/B test setup

### 📋 Key Decisions
- v2 launch delayed by one week to polish onboarding
```

---

### Example 2: Minimal Notes with No Structure

**Input:**
```
We finished the search feature. Notifications are still not done. Main risk is the third-party API rate limits. Next up: finish notifications and start on the settings page.
```

**Output:**
```markdown
## Sprint Review: Sprint 2026-05-15

**Team:** —
**Sprint dates:** —
**Summary:** Core sprint goal achieved; 1 item deferred; API rate limit risk flagged.

---

### ✅ Delivered
- Search feature

### ⏩ Deferred
- Notifications — not completed this sprint

### ⚠️ Risks & Issues
- Third-party API rate limits may impact upcoming work

### 🎯 Next Sprint Focus
- Finish notifications
- Start settings page

*(Source notes were minimal — document may be incomplete. Consider adding detail before sharing.)*
```

---

## Triggers

Use any of these phrases to trigger the skill:

| English | Russian |
|---------|---------|
| Sprint review summary | Итоги спринта |
| Summarize sprint results | Оформи итоги спринта |
| Create sprint stakeholder doc | Создай документ по итогам спринта |
| Turn my sprint notes into a report | Преобразуй заметки спринта в отчёт |

---

**Version:** 1.0.0
**Last updated:** 2026-05-15

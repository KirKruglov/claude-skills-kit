> [Версия на русском языке](README.ru.md)

# Weekly Status Report Generator

Turn your raw weekly notes into two polished status reports — ready to send to your manager and skip-level in minutes.

---

## Overview

Weekly Status Report Generator transforms unstructured weekly notes into two audience-tailored formats in a single pass: a detailed Manager Report and a concise 3-point Skip-Level Brief. It extracts completed tasks, in-progress work, blockers, and next-week plans from any note format — bullet lists, free text, or pasted Slack messages. Use this skill when you need to send your end-of-week update, prepare a manager recap, or write a quick skip-level summary without spending time reformatting.

---

## Requirements

- Your raw weekly notes (any format: bullet list, free text, pasted Slack messages, or a mix)
- No additional files, tools, or integrations required

**Works best with:** Notes covering 2–10 items across completed tasks, in-progress work, and upcoming plans. Very sparse notes (1–2 items) will produce short reports; the skill flags this automatically.

---

## How to Use

1. **Collect your weekly notes**
   - Gather anything from the week: tasks done, meetings attended, blockers encountered, plans for next week
   - Format doesn't matter — paste raw bullet points, free text, or copy from Slack

2. **Trigger the skill**
   - Say: "Write my weekly status report" or "Turn my notes into a status report"
   - In Russian: "Напиши мой еженедельный статус-отчёт" or "Преобразуй мои заметки в отчёт"

3. **Paste your notes**
   - The skill will parse your notes and extract structured items automatically

4. **Get two ready-to-send reports**
   - **Manager Report:** structured sections — Done, In Progress, Blockers, Next Week
   - **Skip-Level Brief:** 3 labeled bullets — Top result, Main challenge, Next week focus
   - Copy each section and paste directly into your message — no editing needed

---

## Examples

### Example 1: Bullet-style notes

**Input:**
```
- Shipped search feature to prod (no rollbacks)
- Reviewed 2 PRs from the backend team
- Still waiting on legal approval for the partner integration (blocked since Tuesday)
- Next week: kick off analytics instrumentation, 1:1 with eng lead
```

**Output:**
```markdown
## Status Report — Week of Jun 9

### Done
- Shipped search feature to production (no rollbacks)
- Reviewed 2 backend team PRs

### In Progress
- Partner integration — awaiting legal approval (blocked since Tuesday)

### Blockers
- Legal approval pending for partner integration

### Next Week
- Kick off analytics instrumentation
- 1:1 with eng lead

---

## Skip-Level Brief

1. **Top result:** Shipped the search feature to production with zero rollbacks.
2. **Main challenge:** Partner integration is blocked on legal approval since Tuesday.
3. **Next week focus:** Starting analytics instrumentation and syncing with the eng lead.
```

---

### Example 2: Free-form notes with metrics

**Input:**
```
Finalized the Q2 OKR doc and presented to the team on Wednesday. Conversion rate improved from 4.2% to 4.7% after the A/B test shipped. Still working on the dashboard redesign — design review scheduled for Friday but got pushed to next week. No hard blockers right now. Next week: finish dashboard redesign, review pricing proposal with finance.
```

**Output:**
```markdown
## Status Report — Week of Jun 9

### Done
- Finalized Q2 OKR document and presented to team
- A/B test shipped — conversion rate improved from 4.2% to 4.7%

### In Progress
- Dashboard redesign — design review rescheduled to next week

### Blockers
- No blockers this week

### Next Week
- Complete dashboard redesign
- Review pricing proposal with finance team

---

## Skip-Level Brief

1. **Top result:** A/B test shipped — conversion rate grew from 4.2% to 4.7%.
2. **Main challenge:** Dashboard design review was deferred to next week.
3. **Next week focus:** Completing the dashboard redesign and aligning with finance on pricing.
```

---

## Triggers

Use any of these phrases to trigger the skill:

| English | Russian |
|---------|---------|
| Write my weekly status report | Напиши мой еженедельный статус-отчёт |
| Weekly status report | Еженедельный статус-отчёт |
| Turn my notes into a status report | Преобразуй мои заметки в отчёт |
| I need to send my weekly update to my manager | Мне нужно отправить еженедельный апдейт менеджеру |

---

> See [docs/USER-GUIDE.md](docs/USER-GUIDE.md) for detailed usage scenarios and tips.

**Version:** 1.0.0

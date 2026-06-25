> [Версия на русском языке](README.ru.md)

# Fundraise Pipeline Tracker

Turn raw investor notes into a structured, tiered pipeline — with follow-up priorities — in seconds.

---

## Overview

Fundraise Pipeline Tracker assembles a structured investor pipeline from pasted meeting notes and round context, solving the problem of pipeline decay: by week 3 of a fundraise, tracking spreadsheets go stale and founders lose track of where each conversation stands. The skill classifies each investor into Tier 1/2/3, extracts per-investor detail (status, next step, why us, feedback), and generates a prioritised "Needs Action" list that separates overdue next steps from investors who've gone silent. No CRM or integrations required — works entirely from pasted text. Bilingual EN/RU.

Use this skill when you want to get a quick status snapshot of your fundraising pipeline, when you're about to make investor calls and need to know who to prioritise, or when your tracking spreadsheet is out of date and you want to rebuild it from notes fast.

---

## Requirements

- Investor notes in any format — free-form text, meeting summaries, email threads, bullet lists
  - Minimum: investor name + a status signal per investor
  - Optimal: name, firm, last meeting date, current status, any feedback given
- Optional: round context (stage, target raise, timeline)
- No external tools, integrations, or file uploads required

---

## How to Use

1. **Gather your investor notes**
   - Collect meeting notes, email summaries, or a list of investor names and statuses
   - Paste everything in one message — the skill handles any format

2. **Trigger the skill by saying:**
   - "Fundraise pipeline" or "Show me my investor pipeline status"
   - In Russian: "Pipeline инвесторов" or "Трекинг раунда"

3. **Optionally add round context**
   - Include your round stage (seed, Series A), target raise amount, and timeline if you have them
   - Without context, the skill still works — round header fields will show "—"

4. **Review the output**
   - Get a three-section markdown document: Pipeline Table → Per-Investor Detail → Needs Action
   - Use the Needs Action list to plan your day: who to email, who to send materials to, who has gone quiet

---

## Examples

### Example 1: Rebuilding a Stale Pipeline from Meeting Notes

**Input:**
```
Seed round, $1.5M target. Talking to 6 investors.

Jane Smith / Acme Ventures — had intro call Jun 5, follow-up Jun 12, she asked for cap table and financial model. Very interested, strong PMF signal. Didn't send the cap table yet.

Ivan Petrov — angel, met at demo day Jun 10. Liked the product. Sent follow-up email Jun 13, no reply since.

Startup Fund / Mark Lee — intro scheduled for Jun 25. Haven't met yet.

GreenLight VC — passed. Said too early stage.

Sarah Johnson / Builder Capital — had first meeting Jun 3. Said she needs to discuss internally. No update since Jun 3.

Alex / TechAngels — met Jun 8. Interested but ticket is $50k, below our minimum.
```

**Output:**
```markdown
# Investor Pipeline — Seed Round
**Report Date:** Jun 23, 2026
**Round:** Seed | **Target:** $1.5M | **Timeline:** —
**Investors tracked:** 6 | **Tier 1:** 1 | **Tier 2:** 2 | **Tier 3:** 3 | **Needs action:** 3

---

## Pipeline Table

| Investor | Firm | Type | Tier | Status | Next Step | Why Us | Feedback |
|----------|------|------|------|--------|-----------|--------|----------|
| Jane Smith | Acme Ventures | VC | 1 | Due diligence | Send cap table + financial model ⚠️ overdue | Strong PMF signal | — |
| Sarah Johnson | Builder Capital | VC | 2 | First meeting done | Follow up — no update since Jun 3 (20d) | — | — |
| Ivan Petrov | — | Angel | 2 | Intro sent | Follow up — no reply since Jun 13 (10d) | Product liked | Ticket size TBD |
| Mark Lee | Startup Fund | VC | 3 | Meeting Jun 25 | Attend intro | — | — |
| Alex | TechAngels | Angel | 3 | Met Jun 8 | — | Product interest | Ticket $50k (below min) |
| GreenLight VC | GreenLight VC | VC | 3 | Passed | — | — | Too early stage |

---

## Needs Action

### 🔴 Overdue Next Steps
1. **Jane Smith (Acme Ventures)** — Send cap table + financial model. Overdue (not sent after Jun 12 meeting).

### 🟡 Gone Silent
2. **Sarah Johnson (Builder Capital)** — No update in 20 days. Last contact: Jun 3. Send check-in.
3. **Ivan Petrov** — No reply in 10 days. Last contact: Jun 13. Send follow-up.
```

---

### Example 2: Quick Status Check Mid-Raise (Russian)

**Input:**
```
Series A, $3M. Декабрьский закрытие. 

Фонд «Рост» / Алексей Иванов — встречались 10 июня. Сильный интерес, запросили данные по юнит-экономике. Отправил данные 15 июня. Жду ответа.

Анна Соколова — бизнес-ангел. Познакомились на конференции 5 июня. Написал follow-up — не ответила.

NovaTech Ventures — прислали term sheet 20 июня. Сейчас на legal review.
```

**Output:**
```markdown
# Воронка инвесторов — Раунд Series A
**Дата отчёта:** 23 июня 2026
**Раунд:** Series A | **Цель:** $3M | **Таймлайн:** закрытие в декабре
**Инвесторов:** 3 | **Tier 1:** 2 | **Tier 2:** 1 | **Tier 3:** 0 | **Требует внимания:** 1

---

## Таблица пайплайна

| Инвестор | Фонд | Тип | Tier | Статус | Next Step | Что зашло | Фидбэк |
|----------|------|-----|------|--------|-----------|-----------|--------|
| NovaTech Ventures | NovaTech Ventures | VC | 1 | Term sheet | Legal review | — | — |
| Алексей Иванов | Фонд «Рост» | VC | 1 | Due diligence | Ждём ответа после данных (8д) | Сильный интерес | — |
| Анна Соколова | — | Ангел | 2 | Знакомство | Follow up — нет ответа (18д) | — | — |

---

## Требует внимания

### 🟡 Потерял ответ
1. **Анна Соколова** — Нет ответа 18 дней. Последний контакт: ~5 июня. Отправить follow-up.
```

---

## Triggers

Use any of these phrases to trigger the skill:

| English | Russian |
|---------|---------|
| Fundraise pipeline | Pipeline инвесторов |
| Track my investors | Трекинг раунда |
| Who should I follow up with | Кому пора следить по инвесторам |
| Show me my investor pipeline status | Покажи статус моей воронки инвесторов |
| Investor pipeline tracker | Статус воронки инвесторов |

See [docs/USER-GUIDE.md](docs/USER-GUIDE.md) for detailed usage scenarios and tips.

---

**Version:** 1.0.0
**Last updated:** 2026-06-23

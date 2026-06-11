> [Версия на русском языке](README.ru.md)

# Proposal and Quote Drafter

Turn raw discovery call notes or a client brief into a polished proposal — complete with scope, pricing packages, cover letter, and a human-review checklist.

---

## Overview

Proposal and Quote Drafter transforms your unstructured notes from a client call or brief into a complete, client-ready proposal document. It structures the scope, builds three pricing tiers (Basic / Standard / Premium), writes a cover letter, and appends a review checklist so you catch errors before sending. Use this skill when you need to send a proposal after a discovery call, prepare a quote for a new project, or convert scattered client notes into a professional document.

---

## Requirements

- Your raw notes from a discovery call or client brief (paste as text — any format, RU or EN)
  - Works with bullet points, free-form paragraphs, or even rough shorthand
  - No pre-formatted document required — the messier the notes, the better this skill shines
- No additional tools or skills required

**Recommended:** Include at least: client name, what they want to solve, and key deliverables. Pricing and timeline help but are optional — the skill uses placeholders if they're missing.

---

## How to Use

1. **Gather your discovery notes**
   - Copy your raw notes from the call (bullet points, paragraphs, shorthand — any format)
   - Or paste a rough brief the client sent you

2. **Trigger the skill by saying:**
   - "Write a client proposal" or "Draft proposal and quote"
   - In Russian: "Напиши предложение клиенту" or "Пропозал и смета"
   - Then paste your notes

3. **The skill will:**
   - Extract client name, project scope, deliverables, timeline, and budget signals
   - Build three pricing packages (or use `[PRICE]` placeholders if no budget was mentioned)
   - Generate the full proposal, cover letter, and review checklist

4. **Review before sending**
   - Work through the ⚠️ Human Review Checklist before sending
   - Fill in any `[FILL IN]` placeholders the skill flagged as missing
   - Adjust pricing if you used placeholder tiers

For detailed scenarios, see [docs/USER-GUIDE.md](docs/USER-GUIDE.md).

---

## Examples

### Example 1: Proposal from a Discovery Call (EN)

**Input:**
```
Client: Acme Digital, Sarah Chen (CMO)
Problem: their blog gets traffic but no leads — want to fix this with a content revamp
What they need: content audit, new content strategy, 4 blog posts per month
Timeline: ideally start Q3, soft deadline end of year
Budget: around $3–5k/month
```

**Output:**

```markdown
## Acme Digital — Proposal

**Client:** Acme Digital (Sarah Chen, CMO)
**Date:** 2026-06-11
**Project:** Content Strategy & Blog Revamp

---

### Executive Summary
Acme Digital is generating blog traffic but failing to convert readers into leads. We propose a content audit, a revised content strategy, and a 4-post/month publishing cadence to turn the blog into a reliable lead generation channel.

### Scope / Deliverables
- Full content audit of existing blog (gap analysis + SEO review)
- Content strategy document (audience personas, topic clusters, editorial calendar)
- 4 long-form blog posts per month (1,500–2,000 words each)
- Monthly performance report

### Timeline
- July: Audit + strategy delivery
- August onward: 4 posts/month

### Pricing Packages

| Package | Price | Includes |
|---------|-------|----------|
| Basic | $3,000/mo | Strategy doc + 2 posts/month |
| Standard | $4,000/mo | Strategy + 4 posts/month + monthly report |
| Premium | $5,000/mo | Standard + SEO optimization + quarterly strategy review |

### Next Steps
Review the packages and let us know which fits best. We'll send a contract and kick off with a 30-minute alignment call.

---

## Cover Letter

Hi Sarah, thank you for the call last week — it was great to learn about Acme's content goals. I've put together a proposal based on our discussion that addresses the gap between your traffic and lead conversion. The Standard package aligns most closely with what you described, and I'm happy to adjust the scope based on your feedback. I've also included two alternative tiers in case the budget needs to flex up or down. Let me know if you'd like to schedule 30 minutes this week to go through the details together.

---

## ⚠️ Human Review Checklist
- [ ] Verify all pricing figures are accurate and reflect your actual rates
- [ ] Verify client name (Sarah Chen, Acme Digital) is spelled correctly
- [ ] Confirm July start date is realistic given your current workload
- [ ] Check legal/contractual terms match your standard agreement
```

---

### Example 2: Proposal from Sparse Notes (RU)

**Input:**
```
Клиент — Иван Сидоров, стартап
Хочет сайт. Нужен лендинг и интеграция с CRM.
Бюджет не обсуждали.
```

**Output (excerpt):**

```markdown
⚠️ Заметки были краткими — заполните разделы [FILL IN] перед отправкой.

## Иван Сидоров — Предложение

**Клиент:** Иван Сидоров (стартап)
**Дата:** 2026-06-11
**Проект:** [FILL IN — уточните название проекта]

### Резюме
[FILL IN — опишите проблему клиента и предложенное решение в 2–3 предложениях]

### Объём работ / Deliverables
- Дизайн и разработка лендинга
- Интеграция с CRM
- [FILL IN — уточните дополнительные требования]

### Ценовые пакеты

| Пакет | Цена | Включает |
|-------|------|----------|
| Базовый | [PRICE] | Лендинг (без CRM) |
| Стандарт | [PRICE] | Лендинг + интеграция с CRM |
| Премиум | [PRICE] | Стандарт + поддержка 3 месяца |

💡 Совет: определите ставку на основе сложности задачи, затрат времени и вашего позиционирования на рынке.
```

---

## Triggers

Use any of these phrases to trigger the skill:

| English | Russian |
|---------|---------|
| Write a client proposal | Напиши предложение клиенту |
| Draft proposal and quote | Пропозал и смета |
| I need to send a quote to a client | Мне нужно отправить коммерческое предложение |
| Turn my discovery notes into a proposal | Преврати заметки звонка в пропозал |
| Write a quote from my notes | Составь КП из моих заметок |

---

**Version:** 1.0.0  
**Last updated:** 2026-06-11

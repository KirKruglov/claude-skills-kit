> [Версия на русском языке](README.ru.md)

# Monthly Close Checklist and Reconciliation Prep

Close the month in minutes — paste your bank export, get a checklist, a categorization draft, and a summary ready for your accountant.

---

## Overview

Monthly Close Checklist and Reconciliation Prep transforms a pasted transaction list or bank export (CSV or Markdown table) plus a brief business context into three ready-to-use artifacts: a locale-adapted monthly-close checklist, a categorization draft with auto-flagged disputed transactions, and a two-part summary for your accountant and investors. Use this skill when you need to close the books at month-end without an accounting platform, prepare data for your accountant in a structured format, or give investors a plain-language snapshot of the month's finances.

---

## Requirements

- A transaction list for the month: CSV rows or a Markdown table with at minimum date, counterparty/description, and amount columns
- 1–3 sentences of business context: entity type (sole-prop, LLC, ИП, ООО), primary currency, and a brief description of how you earn revenue
- No accounting software, integrations, or API access required

**Works best with:** 5–200 transactions per month. For lists >200 rows, all rows are categorized but the investor narrative uses aggregate totals only.

---

## How to Use

1. **Gather your bank export or transaction list**
   - Export or copy-paste the month's transactions (CSV from your bank, a spreadsheet range, or a plain Markdown table)
   - Have 1–3 sentences of business context ready (entity type, currency, revenue model)

2. **Trigger the skill**
   - Say: "Monthly close checklist" or "Reconcile my transactions"
   - Or in Russian: "Чек-лист месячного закрытия" or "Сверь мои транзакции"

3. **Paste the transaction list and context**
   - Provide the CSV/table and your business context in the same message
   - The skill maps columns automatically and notes any assumptions in the output preamble

4. **Review the three artifacts**
   - Work through the checklist before sending data to your accountant
   - Confirm or correct the categorization draft (mark any `⚠ DISPUTED` items)
   - Use the accountant snapshot as a cover note for your accountant handoff
   - Copy the investor narrative into your monthly update

---

## Examples

### Example 1: Freelance Consultant (Sole-Prop, USD)

**Input:**
```
Entity: Sole proprietor, USD, consulting services (monthly retainers + project fees)

Date,Counterparty,Amount
2026-05-02,Acme Corp,+5000
2026-05-05,Stripe Payout,+1200
2026-05-10,AWS,-89
2026-05-12,Notion Pro,-16
2026-05-15,Acme Corp,+5000
2026-05-20,Unknown Transfer,-500
2026-05-28,IRS EFTPS,-620
```

**Output:**
```
## Чек-лист месячного закрытия / Monthly-Close Checklist
**Period:** May 2026 | **Entity:** Sole-prop

- [ ] Verify bank balance matches internal records
- [ ] Confirm all transactions are categorized (1 DISPUTED item pending)
- [ ] Clarify 2026-05-20 "Unknown Transfer" –$500 before handoff
- [ ] Check outstanding receivables (any May invoices unpaid?)
- [ ] Confirm quarterly estimated tax payment scheduled (Q2 due Jun 15)

## Правила категоризации / Categorization Draft
| Date       | Counterparty      | Amount    | Category             | Status      |
|------------|-------------------|-----------|----------------------|-------------|
| 2026-05-02 | Acme Corp         | +5,000    | Revenue/Consulting   | ✅          |
| 2026-05-05 | Stripe Payout     | +1,200    | Revenue/Product      | ✅          |
| 2026-05-10 | AWS               | -89       | OPEX/Software        | ✅          |
| 2026-05-12 | Notion Pro        | -16       | OPEX/Software        | ✅          |
| 2026-05-15 | Acme Corp         | +5,000    | Revenue/Consulting   | ✅          |
| 2026-05-20 | Unknown Transfer  | -500      | Other/Unknown        | ⚠ DISPUTED |
| 2026-05-28 | IRS EFTPS         | -620      | Tax                  | ✅          |

> Disputed: 1. Review before handoff.

## Резюме для бухгалтера / Accountant Snapshot
Income: $11,200 | Expenses: $1,225 | Net: +$9,975

Disputed items:
- 2026-05-20 | Unknown Transfer | –$500 — counterparty unrecognized; confirm business vs. personal

## Резюме для инвестора / Investor Narrative
May revenue came in at $11,200 across two retainer payments from Acme Corp and a Stripe payout, with operating expenses of $1,225 leaving a net of $9,975. Cash position is healthy. One open item: a $500 outgoing transfer with an unidentified counterparty that needs clarification before books can be closed.
```

---

### Example 2: Russian ИП (УСН 6%, RUB)

**Input:**
```
Тип: ИП, УСН 6%, рубли, консалтинг и обучение

Дата,Контрагент,Сумма
2026-05-03,ООО «Альфа»,+120000
2026-05-07,Тинькофф Касса,+25000
2026-05-12,Яндекс 360,-1500
2026-05-15,ООО «Альфа»,+80000
2026-05-20,Иванов И.И.,-15000
2026-05-28,ФНС России,-36200
```

**Output:**
```
## Чек-лист месячного закрытия / Monthly-Close Checklist
**Период:** май 2026 | **Тип субъекта:** ИП (УСН 6%)

- [ ] Сверить остаток по банку с данными из личного кабинета
- [ ] Подтвердить категоризацию (1 спорная позиция)
- [ ] Уточнить платёж от 20.05 «Иванов И.И.» –15 000 ₽ (займ / услуга?)
- [ ] Обновить КУДиР записями за май (доходы: 225 000 ₽)
- [ ] Проверить акт сверки с ООО «Альфа» при наличии дебиторки
- [ ] Срок авансового платежа: 28 июля (Q2)

## Правила категоризации / Categorization Draft
| Дата       | Контрагент        | Сумма      | Категория            | Статус      |
|------------|-------------------|------------|----------------------|-------------|
| 2026-05-03 | ООО «Альфа»       | +120 000 ₽ | Доходы/Консалтинг    | ✅          |
| 2026-05-07 | Тинькофф Касса    | +25 000 ₽  | Доходы/Продукт       | ✅          |
| 2026-05-12 | Яндекс 360        | −1 500 ₽   | ОПEX/ПО              | ✅          |
| 2026-05-15 | ООО «Альфа»       | +80 000 ₽  | Доходы/Консалтинг    | ✅          |
| 2026-05-20 | Иванов И.И.       | −15 000 ₽  | Прочее/Неизвестно    | ⚠ DISPUTED |
| 2026-05-28 | ФНС России        | −36 200 ₽  | Налог/УСН            | ✅          |

> Спорных: 1. Отметьте перед передачей бухгалтеру.

## Резюме для бухгалтера / Accountant Snapshot
Доходы: 225 000 ₽ | Расходы: 52 700 ₽ | Нетто: +172 300 ₽

Спорная позиция: 20.05 | Иванов И.И. | −15 000 ₽ — не ясно: займ или оплата услуг? Требует пояснения для КУДиР.

## Резюме для инвестора / Investor Narrative
Май: выручка 225 000 ₽ по двум контрактам с ООО «Альфа» и через Тинькофф Кассу. Операционные расходы — 52 700 ₽ (ПО + налог УСН). Нетто — 172 300 ₽. Одна открытая позиция: платёж 15 000 ₽ Иванову И.И. нуждается в уточнении перед закрытием месяца.
```

---

## Triggers

Use any of these phrases to trigger the skill:

| English | Russian |
|---------|---------|
| Monthly close checklist | Чек-лист месячного закрытия |
| Reconcile my transactions | Сверь мои транзакции |
| Help me close the month | Помоги закрыть месяц |
| I have a bank export and need to close the month | У меня банковская выгрузка, нужно закрыть месяц |
| Categorize my transactions | Разбей транзакции по категориям |
| Prepare data for my accountant | Подготовь данные для бухгалтера |

---

> See [docs/USER-GUIDE.md](docs/USER-GUIDE.md) for step-by-step usage scenarios.

**Version:** 1.0.0

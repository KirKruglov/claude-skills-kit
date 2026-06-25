> [Версия на русском языке](README.ru.md)

# Invoice & Payment Tracker Summary

Turn a pasted invoice list into a clear aging summary, per-client reconciliation, and action list — no accounting software required.

---

## Overview

Invoice & Payment Tracker Summary classifies each invoice in your list by payment status (Paid, Partially Paid, Overdue, Current), calculates how many days each overdue invoice has been outstanding, and groups results into standard aging buckets (0–30 / 31–60 / 61–90 / 90+ days). It generates three ready-to-use sections: an aging summary table, a per-client reconciliation in the style of a statement of account, and a prioritised "needs action" list. Use this skill when you need a quick receivables snapshot before a cash flow conversation, a weekly payment status review, or data to bring to your accountant — without opening any external tool.

---

## Requirements

- A list of invoices or payments pasted directly into the conversation (any format: markdown table, CSV, plain text, or free-form list)
  - Minimum fields: client name, invoice amount, payment status or paid amount
  - Recommended fields: invoice number, invoice date, due date
- No accounting SaaS, no API access, no integrations required

**Note:** This skill works with invoice data, not bank statements. For bank transaction analysis, use [monthly-close-checklist-and-reconciliation-prep](../monthly-close-checklist-and-reconciliation-prep/). For drafting reminder messages, use [accounts-receivable-followup-writer](../accounts-receivable-followup-writer/).

---

## How to Use

1. **Prepare your invoice list**
   - Export or copy your invoice data (from a spreadsheet, accounting tool, or notes)
   - Include at minimum: client name, invoice amount, and paid/unpaid status

2. **Trigger the skill**
   - Say: "Invoice aging summary" or "Who owes me money?"
   - In Russian: "Aging-сводка по счетам" or "Кто из клиентов не заплатил?"

3. **Paste your invoice list**
   - Paste the data in any format — the skill will identify columns automatically
   - If headers are ambiguous, it will ask you to confirm the mapping before proceeding

4. **Receive your three-part report**
   - **Aging Summary Table** — all invoices with status, balance, days overdue, and bucket
   - **Per-Client Reconciliation** — statement-of-account view for each client
   - **Needs Action List** — prioritised by longest overdue and largest balance

---

## Examples

### Example 1: Freelancer Checking Outstanding Invoices

**Input:**
```
Invoice #  | Client       | Date       | Amount  | Paid
INV-001    | Studio Alpha | 2026-04-10 | $3,500  | $0
INV-002    | Studio Alpha | 2026-05-01 | $1,200  | $1,200
INV-003    | BrandCo      | 2026-05-15 | $4,800  | $2,000
INV-004    | NewClient    | 2026-06-15 | $900    | $0
```

**Action:** Skill classifies each invoice, calculates aging (report date: 2026-06-22, net 30 assumed for due dates), and assembles the three-part report.

**Output:**
```markdown
# Invoice & Payment Status Summary
**Report Date:** 2026-06-22
**Total Invoices:** 4 | **Total Outstanding:** $7,000

> Assumption: due date = invoice date + net 30 (no due dates provided).

---

## Aging Summary

| Invoice # | Client       | Invoice Date | Due Date   | Amount  | Paid    | Balance | Status          | Days Overdue | Bucket      |
|-----------|--------------|--------------|------------|---------|---------|---------|-----------------|--------------|-------------|
| INV-001   | Studio Alpha | 2026-04-10   | 2026-05-10 | $3,500  | $0      | $3,500  | Overdue         | 43           | 31–60 days  |
| INV-003   | BrandCo      | 2026-05-15   | 2026-06-14 | $4,800  | $2,000  | $2,800  | Partially Paid  | 8            | 0–30 days   |
| INV-004   | NewClient    | 2026-06-15   | 2026-07-15 | $900    | $0      | $900    | Current         | —            | —           |
| INV-002   | Studio Alpha | 2026-05-01   | 2026-05-31 | $1,200  | $1,200  | $0      | Paid            | —            | —           |

---

## Per-Client Reconciliation

### Studio Alpha
| Invoice # | Date       | Amount  | Paid    | Balance | Status         |
|-----------|------------|---------|---------|---------|----------------|
| INV-001   | 2026-04-10 | $3,500  | $0      | $3,500  | Overdue 43d    |
| INV-002   | 2026-05-01 | $1,200  | $1,200  | $0      | Paid           |

**Total outstanding: $3,500**

### BrandCo
| Invoice # | Date       | Amount  | Paid    | Balance | Status            |
|-----------|------------|---------|---------|---------|-------------------|
| INV-003   | 2026-05-15 | $4,800  | $2,000  | $2,800  | Partially Paid 8d |

**Total outstanding: $2,800**

### NewClient
| Invoice # | Date       | Amount  | Paid | Balance | Status  |
|-----------|------------|---------|------|---------|---------|
| INV-004   | 2026-06-15 | $900    | $0   | $900    | Current |

**Total outstanding: $900 (not yet due)**

---

## Needs Action

1. **Studio Alpha — $3,500 overdue 43 days** (Bucket: 31–60 days)
2. **BrandCo — $2,800 partially paid, 8 days overdue** (Bucket: 0–30 days)
```

---

### Example 2: Small Business, Multiple Currencies

**Input:**
```
Client: TechVentures — INV-010, €8,000, due 2026-05-20, paid €0
Client: LocalShop — INV-011, ₽120,000, due 2026-06-01, paid ₽120,000
Client: TechVentures — INV-012, €3,000, due 2026-06-30, paid €0
```

**Action:** Skill classifies invoices, calculates aging per invoice, groups by client, and notes that cross-currency totals cannot be combined.

**Output (excerpt):**
```markdown
# Invoice & Payment Status Summary
**Report Date:** 2026-06-22

> Note: Multiple currencies detected. Per-client totals are shown by currency; no cross-currency aggregate is calculated.

## Needs Action

1. **TechVentures — €8,000 overdue 33 days** (Bucket: 31–60 days)
```

---

## Triggers

Use any of these phrases to trigger the skill:

| English | Russian |
|---------|---------|
| Invoice aging summary | Aging-сводка по счетам |
| Who owes me money? | Кто из клиентов не заплатил? |
| Track my overdue invoices | Покажи статус моих счетов |
| I need to see which invoices are unpaid | Мне нужно понять, по каким счетам просрочка |
| Payment tracker summary | Сводка дебиторской задолженности |
| Accounts receivable status | Акт сверки по клиентам |

---

## User Guide

See [docs/USER-GUIDE.md](docs/USER-GUIDE.md) for step-by-step scenarios and tips.

---

**Version:** 1.0.0
**Last updated:** 2026-06-22

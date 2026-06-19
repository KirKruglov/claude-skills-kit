# Monthly Close Checklist and Reconciliation Prep — User Guide

Learn how to get the most out of the Monthly Close Checklist skill for your month-end routine.

---

## Quick Start

Here's the fastest way to close a month:

1. Export or copy-paste this month's transactions from your bank (CSV rows or a Markdown table)
2. Write: "Monthly close checklist" and paste the transactions plus one sentence of context (entity type + currency)
3. Get back three ready-to-use sections: a checklist, a categorization draft, and an accountant/investor summary

**Result:** A structured, copy-paste-ready close package you can send to your accountant or paste into your monthly update.

**Time:** ~3 minutes

---

## Scenarios

### Scenario 1: Solo Freelancer Closing the Month Before Sending to Accountant

**Situation:**
You are a freelance designer working as a sole proprietor. At the end of each month, you send your accountant a summary of transactions along with a note about anything unclear. Normally this takes you 30–45 minutes of copy-pasting and checking. You have a bank CSV export for May and a few transactions you're not sure how to classify.

**What to do:**

1. Export your bank statement for May as a CSV
   - Include all columns your bank provides (date, description/merchant, debit, credit)
   - Don't worry about cleaning it up — the skill handles messy column names

2. Trigger the skill by saying: "Monthly close checklist"
   - Paste the CSV rows directly in your message
   - Add one sentence of context: "Sole proprietor, USD, graphic design retainers and project fees"

3. Review the Categorization Draft
   - Look for any rows marked `⚠ DISPUTED`
   - Add a note for your accountant next to each disputed item (e.g., "this is a personal transfer — ignore")
   - Approve the category labels or correct them where needed

4. Use the Accountant Snapshot as your handoff note
   - Copy the snapshot section and paste it into your email to your accountant
   - Attach the original CSV; the snapshot gives them context before they open it

5. Work through the checklist
   - The checklist shows exactly what to verify before you can mark the month as closed
   - Tick off items as you go

**Expected result:**

You receive:
- **Checklist:** 8–10 items, including one or two custom items based on your disputed transactions
- **Categorization table:** every transaction with a proposed label and status
- **Accountant Snapshot:** income/expense totals by category, disputed items listed, and open questions for your accountant
- **Investor Narrative:** a 3-sentence plain-English paragraph you can reuse in client updates or investor emails

**Why this works:** Instead of manually sorting transactions and writing a note from scratch, you get a structured package in seconds. Your accountant receives exactly the information they need, and nothing ambiguous gets left in a pile for later.

---

### Scenario 2: Russian ИП Preparing КУДиР Data After Month-End

**Situation:**
You are an ИП on УСН 6% (simplified tax, income-only basis). At the end of each month, you need to update your КУДиР with the month's income, confirm the bank balance, and check whether an advance tax payment is due. You have your Тинькофф or Сбер bank statement in CSV format.

**What to do:**

1. Download the month's bank statement from your online banking as a CSV
   - Most Russian banks export in a format with: дата, контрагент, сумма прихода, сумма расхода

2. Trigger the skill by saying: "Чек-лист месячного закрытия"
   - Paste the CSV rows in your message
   - Add context: "ИП, УСН 6%, рубли, консалтинг и продажа курсов"

3. Review the output and update your КУДиР
   - The checklist includes a specific reminder to update the КУДиР income column
   - The Categorization Draft shows the total income amount for you to copy into КУДиР
   - The Accountant Snapshot lists any disputed items that need classification before the КУДиР entry

4. Handle the акт сверки reminder
   - If you have outstanding receivables, the checklist flags the акт сверки with your key counterparties
   - Note the counterparty names from the Categorization Draft and initiate reconciliation if needed

5. Check the advance payment deadline
   - The checklist shows the next quarterly deadline (Q1: 28 Apr, Q2: 28 Jul, Q3: 28 Oct)
   - If the month closes near a deadline, plan the payment before the checklist is done

**Expected result:**

You receive a fully Russian-language close package:
- **Чек-лист** with ИП-specific items: КУДиР update, акт сверки, advance payment deadline, bank reconciliation
- **Правила категоризации** table with Russian category names and `⚠ DISPUTED` flags for unclear payments
- **Резюме для бухгалтера** with ruble totals broken down by category and open questions for your accountant
- **Резюме для инвестора** — a 3-sentence summary in plain Russian you can paste into a monthly report

**Why this works:** The skill knows ИП-specific obligations on УСН and adds them automatically to the checklist. You don't need to remember every regulatory task — they're already in the output, adapted to your entity type.

---

### Scenario 3: Team Lead Preparing a Financial Snapshot for Investors

**Situation:**
You are a co-founder of a small LLC. You don't have a CFO. Each month, your investors expect a brief financial update via email. You have the month's transaction list, but turning raw numbers into a readable investor narrative takes you an hour each time.

**What to do:**

1. Export or copy-paste the month's bank transactions
   - Any format works: CSV, spreadsheet range, or a plain list with date, counterparty, and amount

2. Trigger the skill by saying: "Reconcile my transactions" or "Help me close the month"
   - Paste the transactions plus 2–3 sentences of context:
     "LLC, USD, SaaS subscription revenue + professional services. Monthly recurring revenue ~$15k. Main expenses: payroll, AWS, Stripe fees."

3. Review the Investor Narrative section first
   - The skill generates a 3–5 sentence plain-language paragraph covering revenue, cash position, and key risks
   - Edit it to add any context the skill doesn't have (e.g., a big deal that closed after month-end)

4. Check the Accountant Snapshot for accuracy
   - Verify the income and expense totals match your expectations
   - Confirm or correct any disputed items

5. Send the investor update
   - Paste the Investor Narrative into your investor email template
   - Attach the Accountant Snapshot as the supporting detail

**Expected result:**

You receive a complete investor-ready package with:
- A plain-language narrative paragraph (paste-ready for your investor email)
- Income/expense totals by category with disputed items flagged
- A close checklist to verify before you finalize the month

**Why this works:** The investor narrative section is designed for a non-accountant reader. It takes the categorized numbers and turns them into 3–5 sentences that tell the month's financial story — without jargon, without formulas, without you having to write it from scratch.

---

## Tips

### Tip 1: Include Business Context in Your First Message

The skill adapts its output (checklist items, category names, RU-specific reminders) based on the entity type you provide. If you don't include it, the output falls back to generic international defaults — which may be missing ИП-specific items like the КУДиР reminder or the advance payment deadline.

**Pro tip:** Keep a one-liner saved for your monthly message: "ИП, УСН 6%, рубли, консалтинг" — paste it every time with your CSV.

### Tip 2: Don't Clean Up Your CSV Before Pasting

Raw bank exports often have non-standard column names (e.g., "Дата операции", "Merchant ID", "Debit Amount"). The skill detects columns by heuristic and lists its mapping in the preamble. You can correct it there, rather than spending time reformatting the CSV manually.

**Pro tip:** If the skill maps columns incorrectly, add a note in your message: "Column 3 is the amount (positive = income, negative = expense)" — the skill will use that override.

### Tip 3: Use the Disputed Flag as Your Handoff Checklist

Every `⚠ DISPUTED` row becomes an open question for your accountant. Don't resolve them yourself before handoff — instead, send the categorization draft with the flags intact and let your accountant make the final call. This saves you time and puts the decision with the person who knows your accounting rules.

**Pro tip:** Copy just the "Disputed items" section from the Accountant Snapshot into a sticky note or your accountant Slack channel as a quick-to-action list.

---

**Version:** 1.0.0

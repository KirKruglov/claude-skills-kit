# Invoice & Payment Tracker Summary — User Guide

Learn how to get a complete aging summary, per-client reconciliation, and action list from your invoice data in minutes.

---

## Quick Start

Here's the fastest way to get a summary:

1. Copy your invoice list from a spreadsheet or notes (any format)
2. Say: "Invoice aging summary" and paste the data
3. Receive a three-part report: aging table, per-client reconciliation, and needs-action list

**Result:** A complete receivables snapshot you can share with your accountant or use in a cash flow conversation.

**Time:** ~2 minutes

---

## Scenarios

### Scenario 1: Monthly Receivables Review Before an Accountant Meeting

**Situation:**
You are a freelancer or small business owner preparing for a monthly check-in with your accountant. You have 10–15 invoices in various states — some paid, some partially paid, several overdue. Your accountant wants to know the current receivables position before the meeting. You have the data in a spreadsheet but no accounting software to generate a proper aging report.

**What to do:**

1. Open your invoice spreadsheet and copy the relevant rows
   - Include columns: invoice number, client name, date, amount, amount paid (or status)
   - If you have due dates, include them too — they make the aging calculation more precise

2. Trigger the skill by saying: "Invoice aging summary" or "Who owes me money?"
   - Paste the copied data
   - If column headers are unclear, the skill will ask you to confirm the mapping before proceeding

3. Review the three-part output
   - **Aging Summary Table:** Check which invoices fall into the 31–60 or 90+ day buckets — these need the most attention
   - **Per-Client Reconciliation:** Share this section with your accountant as the statement-of-account data
   - **Needs Action List:** Use this as your agenda for the meeting

4. Forward the report to your accountant
   - Copy the markdown output and paste it into your email or project folder
   - Your accountant has the exact data needed without having to decode a spreadsheet

**Expected result:**

You receive a clean report showing:
- Each invoice with status, outstanding balance, and days overdue
- A per-client breakdown (replaces manual "who owes what" tracking)
- A short list of overdue items sorted by urgency

**Why this works:** Instead of building a pivot table or manually summarising rows, the skill structures your raw data into a professional aging report in under two minutes.

---

### Scenario 2: Weekly Cash Flow Check for a Small Business

**Situation:**
You run a small agency with 5–8 active clients. Every Monday morning you want to know: who has paid this week, who is coming up for payment, and who has gone quiet past their due date. You track invoices in a simple text file or Notion table, not in accounting software.

**What to do:**

1. Copy this week's invoice data
   - Include all open invoices (current and overdue) plus any new payments received
   - Even a plain text list works: "Client A — INV-045 — $4,200 — due June 15 — unpaid"

2. Say: "Track my overdue invoices" and paste the data

3. Focus on the Needs Action List
   - The list is sorted by urgency (longest overdue first, then by amount)
   - Use it to decide who to follow up with today vs. who can wait until end of week

4. Use the Per-Client Reconciliation to check if partial payments arrived
   - If a client paid a portion last week, the reconciliation shows the remaining balance automatically

**Expected result:**

You receive a Monday morning snapshot:
- All overdue invoices ranked by urgency
- Clear balance per client (including partial payments)
- Current invoices flagged as "not yet due" so you don't chase prematurely

**Why this works:** The aging buckets give you a structured triage: 90+ days needs a call today, 31–60 days gets a follow-up email, 0–30 days goes on watch. No spreadsheet formulas needed.

---

### Scenario 3: Preparing an Accounts Receivable Summary for a Business Partner

**Situation:**
You are a project manager in a consulting firm. A potential business partner or investor has asked for a summary of your receivables position — who owes you money and how long it's been outstanding. You have the raw invoice data but need to present it in a clean, structured format rather than sharing a messy spreadsheet.

**What to do:**

1. Export or copy your invoice data (from any tool)
   - Include: client names, invoice amounts, due dates, and payment status

2. Say: "Payment tracker summary" and paste the data
   - The skill processes all invoices and builds the full report

3. Use the Per-Client Reconciliation section as your presentation artifact
   - Each client has a clean statement-of-account subsection
   - Copy this section into a slide, email, or document

4. Add the Aging Summary table as an appendix
   - It shows the full picture with buckets (0–30 / 31–60 / 61–90 / 90+) for a quick risk assessment

**Expected result:**

A professional receivables report that shows:
- Total outstanding and distribution across aging buckets
- Per-client statement view (equivalent to a formal statement of account)
- Needs-action list for internal use

**Why this works:** The output is formatted for external sharing — no raw spreadsheet data, no formulas, no pivot tables. You can copy it directly into any document.

---

## Tips

### Tip 1: Include Due Dates for Precise Aging

If your invoice list doesn't have due dates, the skill assumes net 30 (invoice date + 30 days) and notes this assumption at the top of the report. For more accurate aging, include the actual due date column — especially if your payment terms vary by client (net 15, net 45, net 60).

**Pro tip:** If some clients have different terms, note the term next to each client name: "Acme Corp (net 60)" — the skill will use this context.

### Tip 2: Paste Partial Payments Explicitly

If a client has made a partial payment, include a "Paid" or "Amount Received" column rather than just marking the invoice as "partially paid." The skill uses the actual paid amount to calculate the remaining balance and will show it clearly in the per-client reconciliation.

**Pro tip:** "INV-003 — $4,800 — paid $2,000" gives you a precise balance of $2,800, whereas "partially paid" alone doesn't let the skill calculate the exact outstanding amount.

### Tip 3: For Large Lists, Add a Report Date

When you paste 20+ invoices, add your report date at the top: "Report date: June 22, 2026." This ensures the aging calculation is anchored to a specific date rather than the current session date, which is important if you're generating a report for a past period or want consistent results across sessions.

**Pro tip:** You can also specify payment terms globally: "All invoices are net 30 unless noted" — the skill will apply this to any invoice without a due date.

---

**Version:** 1.0.0
**Last updated:** 2026-06-22

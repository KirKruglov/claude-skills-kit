> [Версия на русском языке](README.ru.md)

# Accounts Receivable Follow-up Writer

Stop chasing overdue invoices with awkward, one-size-fits-all emails. Get a professional, relationship-aware reminder sequence in seconds.

---

## Overview

Accounts Receivable Follow-up Writer drafts an escalating sequence of 4 invoice reminder messages — from a friendly nudge to a formal final notice — based on your invoice details and client relationship context. Each message is calibrated to the previous one, with explicit guidance on tone and send timing, so you collect payment without damaging the relationship. Use this skill when a client hasn't paid, you need to follow up professionally on an overdue invoice, or you want to prepare a full reminder sequence in advance.

---

## Requirements

- Invoice details: client name, amount and currency, due date (or days overdue)
- Relationship context: describe your relationship in a few words (new client, long-term partner, difficult history, etc.)
- Optional: prior contact history ("already sent one email"), formality preference

No accounting software or external tools required. Works entirely from the information you provide.

---

## How to Use

1. **Gather your invoice details**
   - Note the client name, invoice amount, and how many days overdue it is
   - Describe your relationship with the client in a few words

2. **Trigger the skill**
   - Say: "Write invoice reminder sequence for [Client], $[Amount], [X] days overdue, [relationship context]"
   - Or: "My client hasn't paid — help me write follow-up emails"
   - In Russian: "Клиент не платит — напиши напоминания об оплате счёта"

3. **Review the 4-message sequence**
   - Each message includes a subject line, body, send-date recommendation, and tone note
   - A relationship risk flag appears before Messages 3 and 4 if your context warrants it

4. **Personalize and send**
   - Add your invoice reference number, company name, and contact details
   - Adjust wording to match your voice before sending
   - For high-stakes relationships, have a colleague review Messages 3 and 4

---

## Examples

### Example 1: Freelancer Following Up on a Late Invoice

**Input:**
```
Client: Acme Design Studio
Amount: $3,200
Due: 18 days ago
Relationship: long-term client, usually pays on time
```

**Output (excerpt):**
```
## Invoice Reminder Sequence: Acme Design Studio — $3,200 USD overdue 18 days

Relationship context: long-term client, usually pays on time
Escalation starting level: Message 2 (Neutral)

---

### Message 2 — Neutral Follow-up
Subject: Following up: Invoice #___ — $3,200 due
Send: immediately
Tone note: Professional and factual; 18 days overdue warrants a direct follow-up while preserving the warm working relationship.

Hi [Name],

I wanted to follow up on Invoice #___ for $3,200, which was due on [Date]. I know things get busy — just checking in to make sure it didn't slip through the cracks.

If you have any questions about the invoice or need me to resend it, happy to do that right away. Otherwise, payment via [method] would be much appreciated.

Thanks as always for the great partnership!
[Your name]
```

---

### Example 2: Small Business Owner with an Unresponsive New Client

**Input:**
```
Client: TechVentures LLC
Amount: €8,500
Due: 45 days ago
Relationship: new client, signed contract, no prior history
Prior contact: sent one email 2 weeks ago, no response
```

**Output (excerpt):**
```
## Invoice Reminder Sequence: TechVentures LLC — €8,500 EUR overdue 45 days

Escalation starting level: Message 3 (Firm) — prior outreach unanswered + 45 days overdue

### Message 3 — Firm Notice
Subject: Action Required: Invoice #___ — €8,500 45 Days Overdue
Send: immediately
Tone note: Firm and professional; references prior unanswered reminder; sets a clear deadline.

Dear [Name],

I am following up on Invoice #___ for €8,500 issued on [Date], which remains unpaid 45 days past its due date. I sent a reminder on [prior email date] but have not received a response.

Please arrange payment by [specific date — 7 days from now] or contact me to discuss. I am happy to answer any questions about the invoice.

I look forward to your response.
[Your name / Company]
```

---

## Triggers

Use any of these phrases to trigger the skill:

| English | Russian |
|---------|---------|
| Write invoice reminder | Напиши напоминание об оплате счёта |
| Overdue invoice follow-up | Просроченный счёт — нужны письма |
| My client hasn't paid | Клиент не платит |
| Help me ask for payment without being aggressive | Помоги попросить об оплате без конфликта |
| Draft payment reminder sequence | Составь серию напоминаний об оплате |

---

**Version:** 1.0.0
**User guide:** [docs/USER-GUIDE.md](docs/USER-GUIDE.md)

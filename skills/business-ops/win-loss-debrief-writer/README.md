> [Версия на русском языке](README.ru.md)

# Win/Loss Debrief Writer

Turn closed deal notes into a structured debrief — decision drivers, objections, competitive context, and a trend row for your deal log.

---

## Overview

Win/Loss Debrief Writer generates a structured retrospective from notes about a closed deal — won or lost. It extracts decision drivers, objections encountered, competitive context, and concrete repeat/fix recommendations, then produces a single-line trend row ready to paste into a running deal log or spreadsheet. No CRM, no integrations required — just paste your notes. Use this skill immediately after closing or losing a deal, during weekly sales team reviews, or when building a pattern database across multiple deals.

---

## Requirements

- Deal notes in any format: meeting notes, emails, CRM text export, Slack messages, call transcript excerpt
- Optional: explicit outcome (WON / LOST), deal size, industry, customer name, competitor name
- No additional tools or skills required

**Recommended:** The more context you provide (deal size, competitor, timeline), the richer the output. Even 3–5 sentences produce a usable debrief.

---

## How to Use

1. **Gather your deal notes**
   - Copy notes from wherever they live: email thread, CRM, Notion doc, voice memo transcript
   - You can paste free-form text — no special formatting required

2. **Trigger the skill**
   - Say: "Win loss debrief" or "Analyze this deal"
   - Or in Russian: "Разбор сделки" or "Win/loss разбор"

3. **Paste your deal notes**
   - Include what happened, who said what, what the outcome was (if known)
   - Optionally add: deal size, competitor name, customer industry

4. **Review your debrief**
   - Get a structured markdown document with five sections and a trend row
   - Copy the Trend Row into your deal log; share the full debrief with your sales team

---

## Examples

### Example 1: Lost Deal — Enterprise SaaS

**Input:**
```
Had a final meeting with Nexora Inc. yesterday. They went with Velosify instead. 
Deal size was around $80k/year.
Main issue was our onboarding timeline — they needed to go live in 3 weeks, 
we quoted 6. Velosify apparently promised 2 weeks.
Also brought up price twice but seemed more about the timeline.
We offered a dedicated onboarding manager but they didn't think it would help enough.
No contract signed. Deal is dead.
```

**Output:**
```markdown
# Win/Loss Debrief — Nexora Inc.
**Outcome:** LOST
**Date:** Not specified
**Deal Size:** ~$80,000/year
**Competitor:** Velosify

---

## Decision Drivers
1. Onboarding timeline — competitor promised 2 weeks vs. our 6
2. Price — raised twice but secondary to timeline concern

## Objections Encountered
| Objection | How Handled | Status |
|-----------|-------------|--------|
| Onboarding too slow (need 3 weeks, quoted 6) | Offered dedicated onboarding manager | Unresolved |
| Price concern (raised twice) | Not explicitly countered | Unresolved |

## Competitive Context
- **Competitor:** Velosify
- **Their edge:** Faster onboarding promise (2 weeks)
- **Our edge:** Dedicated onboarding manager (offered)
- **Battlecard gap:** No accelerated onboarding tier to match Velosify's speed claim

## What to Repeat / Fix
**Fix next time:**
- Create an accelerated onboarding option (<4 weeks) for time-sensitive deals
- Address timeline objection earlier in the cycle — don't wait for final meeting

## Trend Row
> Copy this line into your deal log or spreadsheet:

`— | Nexora Inc. | LOST | $80k/yr | Velosify | Onboarding timeline | Create accelerated onboarding tier`
```

---

### Example 2: Won Deal — Professional Services

**Input:**
```
Closed Brightfield Consulting today. Annual contract, $45k.
They were also talking to Meridian but chose us in the end.
Main reasons: our industry experience in legal sector, and the personal attention 
our team gave during the pilot. They mentioned Meridian's support was slow.
One concern early on was our pricing — too high vs Meridian. 
We addressed it by showing ROI calculation and offering quarterly billing.
Signed yesterday. Start date is August 1.
```

**Output:**
```markdown
# Win/Loss Debrief — Brightfield Consulting
**Outcome:** WON
**Date:** Not specified (start August 1)
**Deal Size:** $45,000/year
**Competitor:** Meridian

---

## Decision Drivers
1. Industry expertise — legal sector experience was a key differentiator
2. Personal attention during pilot — team responsiveness stood out
3. Competitor's weak support — Meridian's slow support worked in our favor

## Objections Encountered
| Objection | How Handled | Status |
|-----------|-------------|--------|
| Pricing too high vs Meridian | ROI calculation + quarterly billing offered | Resolved |

## Competitive Context
- **Competitor:** Meridian
- **Their edge:** Lower price point
- **Our edge:** Legal sector expertise, responsive team, pilot experience
- **Battlecard gap:** None identified — positioning held

## What to Repeat / Fix
**Repeat next time:**
- Lead with legal sector case studies early in the cycle
- Offer a hands-on pilot with dedicated team attention
- Prepare ROI calculator for pricing objections before final proposal

## Trend Row
> Copy this line into your deal log or spreadsheet:

`— | Brightfield Consulting | WON | $45k/yr | Meridian | Industry expertise + pilot | Lead with sector case studies`
```

---

## Triggers

Use any of these phrases to trigger the skill:

| English | Russian |
|---------|---------|
| Win loss debrief | Win/loss разбор |
| Analyze this deal | Разбор сделки |
| We just lost a deal, help me understand why | Мы проиграли сделку — почему |
| Document what happened in this sales deal | Задокументируй что произошло в этой продаже |
| Debrief on a closed deal | Разбор закрытой сделки |

---

**Version:** 1.0.0

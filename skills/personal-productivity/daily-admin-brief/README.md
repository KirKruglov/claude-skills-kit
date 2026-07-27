> [Версия на русском языке](README.ru.md)

# Daily Admin Brief

Three tabs open at 9am — calendar, inbox, todo list. Paste all three, get one page you can actually run the day from.

---

## Overview

Daily Admin Brief turns a pasted calendar dump, a shortlist of inbox items, and your open todos into a single page: the three-to-five things that genuinely have to happen today, the places where your calendar is physically impossible, two-line reply stubs for the mail that only needs an acknowledgement, and the dates buried in someone's email that never made it onto your calendar. Use it in the first ten minutes of the day, or the evening before, when the three streams live in three tools and nobody has reconciled them. Everything runs on the text you paste — no Gmail, no Calendar, no OAuth, nothing leaves your machine.

---

## Requirements

- At least one of: a calendar dump for the day, an inbox shortlist (sender + subject + snippet), a list of open todos
- Any format — copied from a calendar view, a mail client, a notes file, or typed by hand. There is no schema to follow.
- No connectors, no integrations, no setup

**Works best with:** all three streams for a single day. One stream alone still produces a brief — the sections that depended on the missing streams are named as incomplete rather than quietly filled in.

---

## How to Use

1. **Copy the three dumps**
   - Select your day in the calendar and copy it — times, titles, whatever comes along. Noise (meeting links, attendee lists) is stripped for you.
   - From your inbox, copy the handful of items that actually matter. Not the whole mailbox — a shortlist.
   - Paste your todo list as it is. Checkboxes, bullets, or bare lines all work.

2. **Trigger the skill**
   - Say: "Daily admin brief" or "Brief me on my day"
   - In Russian: "Бриф на день" or "Разбери мой день"

3. **Paste, labelling the blocks if you like**
   - Labels (`Calendar:`, `Inbox:`, `Todos:`) are respected over the automatic guess, which helps with unusual formats.

4. **Read the page**
   - Top Actions first — each one names the pasted line it came from, so you can check it in a second.
   - Schedule Risk tells you what has to move before it becomes a problem at 11:00.
   - Draft Replies are text to copy into your mail client. Nothing is sent, ever.
   - Dates to Capture is the section that saves you: deadlines mentioned in email that are not on your calendar yet.

---

## Examples

### Example 1: All three streams

**Input:**
```
Calendar Mon 27 Jul
10:00-11:00 Team sync
10:30-11:15 1:1 Marina
14:00 Vendor decision — final
15:00-16:00 Q3 planning

Inbox
Ivan — Budget sign-off: "need it before the board pack goes out today"
Anna — Offer, Petrov: "candidate needs an answer by the 30th"
Ops newsletter — headcount policy change from August

Todos
- [ ] Follow up with the agency
- [ ] Send the deck to Marina
```

**Output (excerpt):**
```markdown
# Daily Admin Brief — Mon 27 Jul
Streams found: calendar, inbox, todos.

## Top Actions
1. **Send budget sign-off to Ivan** — he is blocked and the board pack goes out today.
   *(from: inbox — Ivan, "Budget sign-off")*
2. **Prep the 14:00 vendor decision** — it is final and there is no prep block anywhere today.
   *(from: calendar — "Vendor decision — final")*
3. **Send the deck to Marina before 10:30** — your 1:1 with her is today.
   *(from: todos — "Send the deck to Marina")*

## Schedule Risk
- **10:00–11:00 overlaps 10:30–11:15** — "Team sync" and "1:1 Marina". One has to move.
- **14:00 "Vendor decision — final"** — duration not stated; adjacency with 15:00 Q3 planning
  unverified.
- **Prep the 14:00 vendor decision** — no prep block on the calendar.

## Draft Replies — copy manually, nothing is sent
**→ Ivan, "Budget sign-off"**
> Ivan, the sign-off is with me today — I'll send it before […]. If the board pack closes
> earlier than that, tell me and I'll move it up.

## FYI
- Ops newsletter — headcount policy change from August. No action today.

## Needs Your Call
- "Follow up with the agency" has no deadline and no named person — who is this with?

## Dates to Capture — not on the pasted calendar
- **30 Jul** — offer deadline for Petrov. *(from: inbox — Anna, "candidate needs an answer by the 30th")*
- **1 Aug** — headcount policy takes effect. *(from: inbox — Ops newsletter)*
```

---

### Example 2: Calendar only

**Input:**
```
09:30 Review Q3 draft
10:00 Call with vendor
11:00 Standup
```

**Output (excerpt):**
```markdown
# Daily Admin Brief — today
Streams found: calendar. **No inbox and no todos provided** — Draft Replies skipped, and
Dates to Capture cannot be cross-checked against anything.

## Top Actions
1. **Prep "Review Q3 draft" before 09:30** — a review with no preparation block ahead of it.
   *(from: calendar — "Review Q3 draft")*

## Schedule Risk
- **09:30 "Review Q3 draft"** — duration not stated; adjacency with the 10:00 call unverified.
- **09:30 → 10:00 → 11:00** appear consecutive, but no durations are stated — chain partially
  unverified.

No inbox items were provided, so nothing is filed as FYI or drafted as a reply.
```

---

## Triggers

Use any of these phrases to trigger the skill:

| English | Russian |
|---------|---------|
| Daily admin brief | Бриф на день |
| Brief me on my day | Разбери мой день |
| I have three tabs open and no idea what to do first | У меня календарь, почта и задачи — с чего начать |
| Here is my calendar and inbox — what needs me today | Собери утренний разбор дел |

---

## What this skill does not do

It does not connect to Gmail, Outlook, Google Calendar, or any task manager, and it never sends a message — reply stubs are text for you to copy. It does not rewrite your calendar, propose time blocks, or apply a priority framework, and it will not invent an action that cannot be traced back to a line you pasted. Where the input is ambiguous, it asks rather than guesses.

---

> See [User Guide](docs/USER-GUIDE.md) for step-by-step scenarios and tips.

**Version:** 1.0.0

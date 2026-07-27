# Stream Parsing

How to split an unstructured paste into calendar / inbox / todo streams (Step 1), and what to do when a line fits more than one.

---

## 1. Precedence

1. **Explicit labels win.** If the user wrote `## Calendar`, `Почта:`, `TODO:`, `--- inbox ---`, or anything comparable, every line under that label belongs to that stream regardless of its shape.
2. **Structural cues** decide unlabelled lines (section 2).
3. **Ambiguity is declared, not resolved silently** (section 3).

---

## 2. Structural cues

| Stream | Signals |
|--------|---------|
| **Calendar** | A time (`10:00`, `2pm`, `14.00`) or an interval (`10:00-11:00`, `10:00–11:00`, `10-11`) at the start of the line; a duration (`1h`, `30 min`, `45м`); a date header (`Mon 27 Jul`, `27.07`, `понедельник`) followed by timed lines; recurring markers (`weekly`, `every Tue`, `еженедельно`) |
| **Inbox** | `From:` / `От:`; a name followed by a separator and a subject (`Ivan — Budget sign-off`, `Anna: re: offer`); mail markers (`Re:`, `Fwd:`, `Пересл.`); an email address; a snippet in quotes after a sender |
| **Todos** | Checkboxes (`- [ ]`, `[]`, `☐`); an imperative verb with no time and no sender (`Send the deck`, `Позвонить в банк`); bare noun phrases in a bullet list under no other signal; trailing tags (`#urgent`, `@work`, `!!`) |

**Dumps pasted from a real tool** carry extra noise — attendee lists, meeting links, `Организатор:`, `RSVP`, unread counts, thread counts. Strip the noise, keep the time / sender / subject / task text. Never let a meeting link or an email address end up in the brief.

---

## 3. Ambiguous lines

Some lines legitimately fit two streams. Rules, in order:

- **Time + sender + subject** (`15:00 Ivan — budget review`) → **calendar**. It is a scheduled event; the sender name is an attendee.
- **Imperative with a time** (`Call the bank at 11:00`) → **calendar** if the time is a fixed appointment, **todo** if the time reads as a self-imposed intention. When it is genuinely unclear, put it in **todos** and note the time under Schedule Risk as an unconfirmed commitment.
- **Sender with no subject and no time** (`Ivan`) → not enough to be an inbox item. List it under **Needs Your Call** as an unidentifiable line.
- **Deadline with no owner** (`Report due Thursday`) → **todos**, and always also surface it under **Dates to Capture** if no calendar entry matches it.
- **A line that fits nothing** → do not force it. Collect all such lines and, if there are more than two, add one line to **Needs Your Call**: `N lines could not be classified — {first few, quoted}`.

Never move a line into a stream the user did not provide at all. If no inbox was pasted, an ambiguous line cannot become an inbox item.

---

## 4. Deciding "no day-signal at all" (NEG3)

Stop and report only when **none** of the three streams can be identified: no times, no senders, no tasks. A pasted PRD, article, or contract will match nothing here.

Do not stop merely because one or two streams are missing — a calendar-only paste is a perfectly normal use of the skill (EC1). One stream is enough to proceed.

---

## 5. Detecting the same commitment in two streams

An inbox item and a todo frequently describe one commitment (`Reply to Sergey re: agency` / `Follow up with the agency`). Treat them as candidates for merging when they share a proper noun (person, company, project) **and** a compatible verb.

Do not merge them silently. Surface the pair under **Needs Your Call**:

```
- "Follow up with the agency" (todo) and "Reply to Sergey re: agency" (inbox) may be the
  same commitment — merge or keep separate?
```

If they clearly differ (different deadlines, different people), keep both and say nothing.

# Schedule Risk Rules

Full detection rules for Step 3 of the skill. The governing principle: **an unverifiable conflict is worse than no conflict**. A brief that cries "overlap!" on an event with no stated end time trains the user to ignore the section entirely.

---

## 1. Overlap vs. adjacency

| Input shape | Verdict | How to report |
|-------------|---------|---------------|
| Both events have start **and** end (or duration) and the intervals intersect | **Overlap** — assert it | `**11:00–12:00 overlaps 11:30–12:15** — "Team sync" and "1:1 Marina". One has to move.` |
| Both fully stated, intervals touch exactly (`10:00–11:00`, `11:00–12:00`) | **Back-to-back**, not an overlap | Report only as part of a run of three or more |
| One event has a start but no end/duration | **Unverified** — never assert an overlap | `**09:30 "Review Q3 draft"** — duration not stated; adjacency with the 10:00 call unverified.` |
| Neither event has an end | **Unverified adjacency** | Report both times as given, mark the whole pair `durations not stated` |
| An all-day / no-time entry (`Vacation`, `Deadline: Q3 report`) | Not a schedule conflict | Route to FYI, or to Dates to Capture if it carries a deadline |

**Duration inference is not allowed.** Do not assume 30 or 60 minutes because "meetings usually are". If the input does not state it, the pair is unverified.

---

## 2. Back-to-back runs

Report a run when **three or more** consecutive events have no gap between them. Two events touching is normal and not worth a line.

```
14:00 → 15:00 → 16:00 back-to-back, no gap before the vendor decision at 14:00.
```

If any event in the run lacks a duration, still report the run but mark it `chain partially unverified`.

---

## 3. Unbroken blocks

More than **three hours** of continuous meetings with no gap ≥ 15 minutes. Report the span and the total:

```
09:00–12:30 — 3.5h with no break.
```

Do not suggest where to put the break — that is calendar rewriting, which is out of scope.

---

## 4. Meetings that need prep

Flag an event as prep-needed when its title matches a decision-or-performance pattern **and** no earlier event in the day looks like preparation for it (a block whose title names the same subject, or a generic `prep` / `focus` / `подготовка` block).

**Title patterns (EN):** `review`, `interview`, `decision`, `presentation`, `demo`, `board`, `steering`, `QBR`, `retro`, `postmortem`, `1:1` with a name not seen elsewhere in the pasted material.

**Title patterns (RU):** `ревью`, `интервью`, `собеседование`, `решение`, `презентация`, `демо`, `совет директоров`, `защита`, `ретро`, `разбор`, `1:1` с незнакомым именем.

Report as:

```
**Prep the 14:00 vendor decision** — no prep block on the calendar.
```

A recurring `1:1` with a name that also appears in the inbox or todos is *not* flagged — the user clearly has context.

---

## 5. Timezones

- **No timezone stated anywhere:** compare times as given. Do not add a note; this is the normal case.
- **One timezone stated for the whole dump:** compare within it. No note needed.
- **Different timezones on different entries:** do not normalise. Flag once, above the conflict list:
  ```
  ⚠ timezone mismatch — verify before trusting the conflict list
  ```
  Show each entry with the timezone it was written with, and downgrade every overlap in the affected pairs to unverified.
- **A time expressed relative to another** (`30 min after the standup`): resolve it only if the anchor event has a stated time; otherwise leave it unresolved and say so.

---

## 6. Worked examples

### Example A — clean overlap

Input:
```
10:00-11:00 Team sync
10:30-11:15 1:1 Marina
13:00-14:00 Lunch
```

Output:
```
- **10:00–11:00 overlaps 10:30–11:15** — "Team sync" and "1:1 Marina". One has to move.
```
No other lines: two touching events would not qualify, and there is no run of three.

### Example B — missing durations

Input:
```
09:30 Review Q3 draft
10:00 Call with vendor
11:00 Standup
```

Output:
```
- **09:30 "Review Q3 draft"** — duration not stated; adjacency with the 10:00 call unverified.
- **09:30 → 10:00 → 11:00** appear consecutive, but no durations are stated — chain partially unverified.
- **"Review Q3 draft"** looks like it needs prep, and no prep block appears earlier in the day.
```

### Example C — mixed timezones

Input:
```
14:00 CET  Vendor decision
15:30 MSK  Board prep
```

Output:
```
⚠ timezone mismatch — verify before trusting the conflict list
- **14:00 CET "Vendor decision"** and **15:30 MSK "Board prep"** are in different timezones;
  overlap cannot be determined from the pasted material.
```

---

## 7. What never goes in this section

- Suggestions to move, shorten, or decline a meeting — the skill reports, it does not rewrite the calendar
- Time-blocking proposals or focus-time recommendations
- Judgements about whether a meeting was worth having

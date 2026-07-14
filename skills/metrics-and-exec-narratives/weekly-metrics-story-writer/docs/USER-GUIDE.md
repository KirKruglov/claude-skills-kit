# User Guide — Weekly Metrics Story Writer

## What This Skill Does

Every week you copy numbers from a dashboard and spend 30–60 minutes turning them into a written update for leadership or your team. This skill does that writing for you. Paste your metrics, answer two quick questions, and receive a polished email or Slack post ready to copy and send.

---

## Quick Start

**Trigger:** Type any of the following to start:
- "Weekly metrics story"
- "Write metrics narrative"
- "Metrics to email"
- Paste your numbers directly — the skill will recognise them

**Steps:**
1. Paste your metrics (any format)
2. Add one line of context: "We launched X on Tuesday" or "Nothing special this week"
3. Say your audience and format: "Leadership, email" or "Team, Slack" or "Both"
4. Receive your narrative — copy and send

---

## What Metrics Format Works?

Any text format is accepted. Examples:

**Table:**
```
| Metric         | This Week | Last Week |
|----------------|-----------|-----------|
| DAU            | 48,200    | 44,100    |
| 7-day Retention| 34%       | 36%       |
```

**List:**
```
DAU: 48,200 (was 44,100)
Retention: 34% (was 36%)
Revenue: $182k (was $175k)
```

**CSV:**
```
DAU,48200,44100
7-day Retention,34%,36%
Revenue,$182k,$175k
```

**Plain prose:**
```
DAU was 44k last week and hit 48k this week. Retention dropped slightly from 36 to 34 percent.
```

All of the above produce the same output quality. You don't need to clean up your data first.

---

## Choosing Your Format

**Email** — best for leadership updates, weekly OKR check-ins, or any written report that goes to stakeholders outside your immediate team. Structured, formal, ≤ 200 words.

**Slack** — best for team digests, product updates, or any channel where you want quick, scannable content. Conversational, uses Slack markdown, ≤ 120 words.

**Both** — generates both formats in one run. Useful when you send the same update to multiple audiences.

---

## Adding Context

Context is optional but makes the narrative significantly better. One line is enough:

- "Launched onboarding redesign Tuesday"
- "Support incident Wednesday, fixed Thursday morning"
- "Running A/B test on pricing page"
- "Nothing notable this week"

If you skip context entirely, the skill writes the narrative from the numbers alone and omits the Context section.

---

## Reading Your Output

The final output has two parts:

**1. The narrative** — your email or Slack post, ready to copy and send. No placeholders, no brackets.

**2. Signal summary** — a compact line at the end for your own notes:
```
Signal summary:
🟢 DAU · 🟢 Revenue · 🔴 Retention · 🟡 Churn
```

Green = good, Red = needs attention, Yellow = flat.

---

## Tips

- **Include a prior-period value for each metric** whenever possible. Without it, the skill can't show trends — it will still write a narrative, but without "grew 9%" context.
- **Name your metrics clearly.** "Users" is ambiguous; "DAU" or "Weekly Active Users" gives the skill enough to write a precise sentence.
- **One line of context goes a long way.** Even "Nothing unusual this week" helps the skill avoid inventing reasons for changes.
- **For recurring use**, keep a template file in Cowork with your standard metrics list and update the values each week before triggering the skill.

---

## Frequently Asked Questions

**Can I use a file instead of pasting?**  
Yes. If you have a `.md` file in your Cowork folder with metrics data, mention the file path: "Use the file `/reports/week-22.md`" and the skill will read it.

**What if I have 15 metrics?**  
The skill processes all of them but highlights the top 5 by signal strength in the narrative. The rest appear in the signal summary at the bottom.

**What if I don't know what the numbers mean?**  
The skill writes a narrative based on direction (up / down / flat) and the metric name. If the interpretation seems off, add a line of context and the output will improve.

**Can I ask for a different tone?**  
Yes. Say "more formal" or "more casual" and the skill applies that tone throughout without asking for confirmation.

**Does this skill save my data?**  
No. Metrics are processed in the current session only and are not stored between sessions.

> [Версия на русском языке](README.ru.md)

# Interview Debrief Synthesizer

Turn four sets of mismatched interview notes into one debrief you can actually reason over — evidence separated from impressions, with the disagreements named.

---

## Overview

Interview Debrief Synthesizer consolidates notes from several interviewers into a single comparable debrief. It separates evidence (what the candidate said or did, attributed to whoever observed it) from impressions (evaluative claims with nothing behind them), shows where interviewers contradict each other, and lists the competencies nobody probed. Use this skill after a final interview round when everyone sent notes in a different format, when two interviewers reached opposite conclusions and you need to see why, or when you suspect the decision is running on gut feel and want to check what the evidence actually supports.

---

## Requirements

- Interview notes from one or more interviewers, pasted as plain text — prose, bullets, ratings, fragments, or any mix
- Optional: a scorecard or the role requirements (makes "not probed" authoritative instead of inferred)
- Optional: candidate names, if several candidates are being compared
- No ATS, no integrations — everything runs on the text you paste

**Works best with:** notes from 2–5 interviewers on one candidate. Single-interviewer notes work too, but the disagreement section is skipped.

---

## How to Use

1. **Collect the notes**
   - Copy whatever each interviewer sent — Slack messages, doc comments, scribbled bullets. Inconsistent formats are the normal case, not a problem.
   - Label who wrote what if it isn't obvious; unlabelled blocks are marked `source not stated` rather than guessed.

2. **Trigger the skill**
   - Say: "Interview debrief" or "Synthesize these interview notes"
   - In Russian: "Дебриф по кандидату" or "Сведи заметки с интервью"

3. **Paste the notes, and the scorecard if you have one**
   - With a scorecard, the competency frame is taken verbatim from it
   - Without one, the frame is derived from the notes and labelled as such

4. **Read the debrief**
   - Check the evidence block first — anything in a blockquote is an impression nobody backed up
   - Take the disagreement questions into the decision meeting; they're the ones worth the room's time
   - Use "Not probed" to decide whether a follow-up conversation is needed before deciding

---

## Examples

### Example 1: Three interviewers, three formats

**Input:**
```
Maria (hiring manager): Talked through the migration she led. Started by asking what
our rollback story was before proposing anything. Confident. Would hire.

Tom: 3/5. Didn't seem senior to me. Couldn't name a decision he'd reversed when I asked.

Priya: really good culture fit! very collaborative. no notes on the technical side,
we mostly talked about the team.
```

**Output (excerpt):**
```markdown
## Debrief: candidate — Senior Engineer
Sources: 3 interviewers (Maria, Tom, Priya) · Competency frame: derived from notes

### Evidence by competency

**Judgement under uncertainty**
- Asked what the rollback story was before proposing anything — *Maria*
- Could not name a decision he had reversed when asked — *Tom*
> Impression only, no evidence: "confident", "would hire" — *Maria*
> Impression only, no evidence: "3/5", "didn't seem senior" — *Tom*

**Collaboration**
> Impression only, no evidence: "really good culture fit", "very collaborative" — *Priya*

### Where interviewers disagree

**Seniority** — Maria: led a migration, checks rollback before proposing. Tom: not senior,
no reversed decision to point to.
→ Question that would settle it: ask for a decision he changed his mind on mid-project,
  and what evidence moved him.

### Not probed

- Technical depth — Priya's session covered the team instead. A follow-up would need to ask:
  a design question with a constraint that forces a trade-off.

### Decision draft

**Rests on:** one evidence-backed strength (checks rollback before proposing) and one
evidence-backed gap (no reversed decision offered).
**Still unknown:** technical depth; the seniority disagreement is unresolved.
**Risks:** "culture fit" carries the entire collaboration competency with no behaviour attached.

The decision is yours — this is the basis for it, not the verdict.
```

---

### Example 2: Notes that are almost all impressions

**Input:**
```
Alex: strong hire
Sam: meh, wouldn't move forward
Dana: loved her! great energy
```

**Output (excerpt):**
```markdown
> **These notes contain almost no evidence.** All 5 statements are evaluative claims with no
> observed behaviour attached. The decision currently has no evidentiary basis — the follow-up
> questions below are what would give it one.

### What to ask each interviewer

- **Alex** wrote "strong hire". Ask: what did the candidate say or do that led there?
- **Sam** wrote "wouldn't move forward". Ask: which answer or behaviour was the deciding one?
- **Dana** wrote "great energy". Ask: what did she do in the session that showed it, and which
  competency does it speak to?
```

---

## Triggers

Use any of these phrases to trigger the skill:

| English | Russian |
|---------|---------|
| Interview debrief | Дебриф по кандидату |
| Synthesize interview notes | Сведи заметки с интервью |
| Interviewers disagree on this candidate | Интервьюеры разошлись в оценке |
| Pull together the notes from everyone who interviewed | Собери разбор по итогам собеседований |
| What did we actually learn about this candidate? | Что мы реально узнали о кандидате? |

---

## What this skill does not do

It emits no score, no ranking, and no hire/no-hire verdict. It also skips calibration statistics and interviewer-reliability scoring — on a handful of notes those would be false precision. The output is the basis for your decision, not the decision.

---

> See [User Guide](docs/USER-GUIDE.md) for step-by-step scenarios and tips.

**Version:** 1.0.0

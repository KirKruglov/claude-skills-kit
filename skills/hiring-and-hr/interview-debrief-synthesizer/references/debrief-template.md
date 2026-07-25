# Debrief Template

The full output skeleton, with every variant the skill has to produce. Headings render in the language of the request — the RU equivalents are in the mapping table in SKILL.md.

---

## Variant A: Single candidate, several interviewers (default)

```markdown
## Debrief: {candidate} — {role}
Sources: {N} interviewers ({names}) · Competency frame: {scorecard | derived from notes}

### Evidence by competency

**{Competency 1}**
- {observed behaviour, quoted or closely paraphrased} — *{interviewer}*
- {observed behaviour} — *{interviewer}*
> Impression only, no evidence: {claim} — *{interviewer}*

**{Competency 2}**
- {observed behaviour} — *source not stated*
> Impression only, no evidence: {claim}, {claim} — *{interviewer}*

### Comparison matrix

| | {Competency 1} | {Competency 2} | {Competency 3} |
|---|---|---|---|
| {Interviewer A} | {evidence, short} | {evidence, short} | — not probed |
| {Interviewer B} | {evidence, short} | impression only | — not probed |

### Where interviewers disagree

**{Competency}** — {Interviewer A}: {reading}. {Interviewer B}: {opposite reading}.
→ Question that would settle it: {question}

**{Competency}** — both saw {the same behaviour}, read it as {reading A} and {reading B}.
→ Question that would settle it: {question}

### Not probed

- {Competency} — nobody covered it. A follow-up would need to ask: {question}
- {Competency} — nobody covered it. A follow-up would need to ask: {question}

### Decision draft

**Rests on:** {evidence-backed findings, competency by competency}
**Still unknown:** {unprobed competencies + unresolved disagreements}
**Risks:** {protected-attribute or bias flags, if any — omit the line if none}

The decision is yours — this is the basis for it, not the verdict.
```

---

## Variant B: Several candidates compared

Everything is identical except the matrix, which flips orientation, and the evidence block, which is grouped by candidate first:

```markdown
### Evidence by competency

#### {Candidate 1}
**{Competency 1}**
- {observed behaviour} — *{interviewer}*

#### {Candidate 2}
**{Competency 1}**
- {observed behaviour} — *{interviewer}*

#### Unattributed
- {block that could not be assigned to a candidate with confidence}

### Comparison matrix

| | {Competency 1} | {Competency 2} |
|---|---|---|
| {Candidate 1} | {evidence, short} | — not probed |
| {Candidate 2} | {evidence, short} | {evidence, short} |
```

The matrix compares evidence, not scores. Never add a "total" column, a rank, or a recommendation row — the whole point is that the reader compares the underlying observations.

---

## Variant C: Single interviewer

Drop the disagreement section entirely and replace it with one line:

```markdown
### Where interviewers disagree

Only one interviewer's notes were provided — cross-interviewer comparison is not possible.
```

Do not invent a second perspective, and do not fill the section with the interviewer disagreeing with themselves. The matrix in this variant has a single row and still carries value: it shows which competencies one person covered and which nobody did.

---

## Variant D: Impressions only

When the notes carry almost no evidence, the finding leads. Put it directly under the header, before the evidence block:

```markdown
> **These notes contain almost no evidence.** {N} of {M} statements are evaluative claims with no
> observed behaviour attached. The decision currently has no evidentiary basis — the follow-up
> questions below are what would give it one.

### Evidence by competency

**{Competency}**
> Impression only, no evidence: {claim} — *{interviewer}*

### What to ask each interviewer

- **{Interviewer}** wrote "{impression}". Ask: what did the candidate say or do that led there?
- **{Interviewer}** wrote "{impression}". Ask: {specific question}
```

The "What to ask each interviewer" block replaces "Not probed" in this variant only — with no evidence anywhere, the unprobed list would be the entire frame and tells the reader nothing.

---

## Rendering rules

- **Attribution is mandatory.** Every evidence bullet ends with `— *{interviewer}*` or `— *source not stated*`.
- **Impressions live in blockquotes**, never as evidence bullets. Never merge them into a competency's evidence list.
- **Ratings keep their original scale**: `4/5`, `✓`, `yes with reservations` — reported as written, with the scale noted if it is not obvious. Never averaged, never normalized.
- **Quotes keep their original language** even when the debrief renders in the other one.
- **Empty sections are stated, not deleted** — `Not probed: nothing — every competency in the frame was covered` is a real finding and should be printed.
- **No scores anywhere.** No total, no rank, no hire/no-hire verdict, including in the matrix and the decision draft.

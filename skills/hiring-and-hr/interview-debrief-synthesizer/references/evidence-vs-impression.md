# Evidence vs. Impression

The classification rule behind Step 4 of the skill. Read this when a statement is not obviously one or the other.

---

## The rule

**Evidence** is a concrete thing the candidate said, did, built, or decided, reported closely enough that a second reader could form their own judgement of it.

**Impression** is an evaluative claim about the candidate with no observation attached. It reports the interviewer's conclusion, not the candidate's behaviour.

The test: *strip the interviewer's adjectives. Is anything left?*

- "Walked through sharding the orders table, chose range partitioning over hash, explained the trade-off for their query pattern" → strip the adjectives, the behaviour survives → **evidence**
- "Strong system design" → strip the adjectives, nothing is left → **impression**

---

## Why the split matters

Impressions are not worthless — they are what an experienced interviewer's judgement feels like from the inside. But they cannot be compared, challenged, or checked by a second person. When four interviewers submit four impressions, the debrief has nothing to reason over, and the hiring manager falls back on whichever interviewer is most confident or most senior.

Splitting them is what makes the notes comparable. It also makes the gap visible: a candidate can accumulate five glowing impressions and zero evidence, and that pattern is itself the most important finding in the debrief.

---

## The ambiguous middle

The hard case is a rating or verdict carrying a one-clause justification.

| Note | Classification | Why |
|------|----------------|-----|
| "4/5 on system design" | Impression | A number is a conclusion. No behaviour reported. |
| "4/5 on system design — walked through the sharding trade-off unprompted" | **Split it.** Evidence: "walked through the sharding trade-off unprompted". Impression: "4/5". | The justification clause reports behaviour and stands on its own; the rating is still a conclusion. Report both, attributed to the same interviewer. |
| "Not senior enough" | Impression | Pure conclusion. |
| "Not senior enough — couldn't name a decision they'd reversed" | **Split it.** Evidence: "could not name a decision they had reversed". Impression: "not senior enough". | The clause is a reportable observation from the interview. |
| "Seemed nervous" | Impression | An interpretation of demeanour, not a reported behaviour. |
| "Asked to restart the whiteboard question twice" | Evidence | Observable, checkable, no evaluation attached. |
| "Great culture fit" | Impression | Conclusion, and one worth watching — see the bias note below. |

**Rule of thumb:** when a note contains both a verdict and a because-clause, the because-clause is usually evidence and the verdict is usually an impression. Split rather than pick.

---

## Never manufacture evidence

The single most damaging failure mode is inventing a supporting detail to make an impression look grounded.

If an interviewer wrote "strong system design" and nothing else, the debrief says *impression only, no evidence*. It does **not** say "demonstrated strong system design skills during the architecture discussion" — that sentence adds a fact (that there was an architecture discussion, that something was demonstrated in it) which no one reported. A hiring manager reading that line would believe there was an observation behind it.

The same applies to filling gaps from plausibility: never infer what a candidate "must have" said because of the role, the seniority, or the other notes.

---

## Worked example (EN)

Raw note from one interviewer:

> Ana — round 3, system design. Really solid. 4/5. She walked through the read path first, then asked what our p99 target was before proposing a cache. Bit quiet at the start. Would hire.

Classification:

- **Evidence:** "walked through the read path first, then asked what the p99 target was before proposing a cache" — *Ana's interviewer*
- **Evidence:** "was quiet at the start of the session" — *Ana's interviewer* (observable behaviour, though it invites interpretation)
- **Impression:** "really solid", "4/5", "would hire" — *Ana's interviewer*

Note that "bit quiet at the start" is reported as observed behaviour, not as "seemed nervous" or "lacked confidence" — those would be the interviewer's interpretation of it, and they belong in the impression column if the interviewer actually wrote them.

---

## Worked example (RU)

Исходная заметка:

> Дмитрий, техническое интервью. Опыта хватает, но не тянет на сеньора. Спросил про нагрузку до того, как предлагать решение. На вопрос про откат релиза ответил размыто. 3 из 5.

Классификация:

- **Свидетельство:** «спросил про нагрузку до того, как предлагать решение» — *интервьюер Дмитрия*
- **Свидетельство:** «на вопрос про откат релиза ответил размыто» — *интервьюер Дмитрия*
- **Впечатление:** «опыта хватает, но не тянет на сеньора», «3 из 5» — *интервьюер Дмитрия*

Обратите внимание: «ответил размыто» — на грани. Это ближе к наблюдению, чем к выводу (интервьюер описывает, каким был ответ, а не выносит оценку кандидату), поэтому идёт в свидетельства — но в разборе стоит показать формулировку дословно, чтобы читатель сам решил, насколько она конкретна.

---

## Bias watch

Two patterns deserve a flag in the **Risks** block of the decision draft, not silent inclusion:

1. **Protected attributes as grounds** — age, marital status, nationality, gender, health, pregnancy, religion. Exclude the reasoning from evidence and decision; flag that the assessment rested on it.
2. **"Culture fit" with no behaviour attached** — an impression that reliably absorbs similarity bias. It is not automatically illegitimate, but in a debrief it should appear as an impression awaiting evidence, and it is worth naming when it is the only thing carrying a competency.

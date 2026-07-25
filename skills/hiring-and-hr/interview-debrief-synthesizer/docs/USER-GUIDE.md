# Interview Debrief Synthesizer User Guide

How to turn a pile of mismatched interview notes into a debrief you can take into a decision meeting.

---

## Quick Start

1. Copy the notes every interviewer sent you — Slack messages, doc comments, bullets, whatever arrived
2. Say: "Interview debrief" and paste them, labelling who wrote what
3. Read the debrief: evidence first, then the disagreement questions

**Result:** One document showing what was actually observed, who observed it, where interviewers contradict each other, and what nobody checked.

**Time:** ~3 minutes

---

## Scenarios

### Scenario 1: Four interviewers, four formats, decision tomorrow

**Situation:**

You are a hiring manager. Four people interviewed your finalist over two days. One sent three paragraphs of prose, one sent a 1–5 rating with no comments, one sent five bullets, and one sent a Slack message saying "yes from me". The decision meeting is tomorrow morning and you cannot line up what anyone actually saw.

**What to do:**

1. Paste all four sets of notes in one message
   - Put each interviewer's name above their block — attribution is what makes the output usable
   - Include the scorecard or the role requirements if you have them; without one the competency frame is inferred from the notes and labelled as such

2. Trigger the skill: "Interview debrief"

3. Read the evidence block first
   - Bullets are things the candidate said or did, each tagged with who saw it
   - Anything in a blockquote is an impression nobody backed up — that is not a criticism of the interviewer, it just cannot carry a decision on its own

4. Take the disagreement questions into the meeting
   - Each disagreement ends with the single question that would settle it
   - These are the items worth the room's time; the agreed parts usually are not

**Expected result:**

A debrief with five blocks: evidence by competency, a comparison matrix, disagreements, unprobed competencies, and a decision draft that visibly rests on the evidence. No score, no ranking, no verdict — the decision stays yours.

**Why this works:** the meeting stops being a round of confidence-weighted opinions and starts being a conversation about two or three specific open questions.

---

### Scenario 2: Two interviewers reached opposite conclusions

**Situation:**

You are a team lead. Your senior engineer says the candidate is a clear hire; your other engineer says not senior enough. Both were in technical sessions. You need to understand whether they saw different things or read the same thing differently — those call for completely different follow-ups.

**What to do:**

1. Paste both sets of notes, nothing else

2. Trigger the skill: "Interviewers disagree on this candidate"

3. Go straight to the disagreement section
   - It states both readings side by side with attribution, and does not pick a winner
   - Look at whether the underlying observations differ or match

4. Run the suggested question
   - If they saw different behaviours, a short follow-up interview usually resolves it
   - If they read the same behaviour differently, the conversation is between the two interviewers, not with the candidate

**Expected result:**

The disagreement is stated in terms of what each person observed, not in terms of who is more senior or more confident. You leave with one concrete question instead of a stalemate.

**Why this works:** the most common failure in a split debrief is that the disagreement gets resolved socially — by seniority or by whoever speaks last. Naming the observations behind each position makes that harder.

---

### Scenario 3: You suspect the decision has no evidence behind it

**Situation:**

You are a founder. Everyone liked the candidate. The notes say "strong", "great fit", "loved her". You have been burned by exactly this pattern before and want to check whether anything concrete is underneath.

**What to do:**

1. Paste the notes as they are — do not clean them up first

2. Trigger the skill: "What did we actually learn about this candidate?"

3. Read the lead finding
   - When notes are almost entirely impressions, the debrief says so up front and skips the pretence of an evidence block

4. Use the per-interviewer questions
   - Each one asks a specific person what the candidate said or did that led to their conclusion
   - Send them in a thread; the answers usually arrive in a few minutes and change the picture

**Expected result:**

An explicit statement that the decision currently has no evidentiary basis, plus a short list of questions that would give it one. Sometimes the answers confirm the enthusiasm; sometimes nobody can produce a single observation, which is itself the finding.

**Why this works:** unanimous enthusiasm is indistinguishable from unanimous vagueness until you ask. This makes the difference visible before the offer goes out.

---

## Tips

### Tip 1: Label who wrote what, even roughly

The debrief's value comes from attribution — "Tom saw X, Maria saw Y" is what makes a disagreement legible. Unlabelled blocks are marked `source not stated` rather than guessed, which is safe but much less useful. Initials are enough.

**Pro tip:** if a Slack export already has names on each line, paste it raw — no cleanup needed.

### Tip 2: Paste the scorecard when you have one

Without it, the competency frame is derived from what the notes happen to discuss, which means "not probed" only lists gaps visible from the notes themselves. With a scorecard, the skill compares against the list you actually committed to before the interviews — that is where the uncomfortable gaps show up.

### Tip 3: Don't clean up the notes first

Rewriting an interviewer's "3/5, didn't seem senior" into something tidier destroys exactly the signal being looked for. Ratings on incompatible scales, one-word verdicts, and half-sentences are all handled — and incompatible scales are reported as written rather than averaged into a fake common score.

**Pro tip:** the messier and more honest the input, the more the impression/evidence split has to work with.

---

**Version:** 1.0.0

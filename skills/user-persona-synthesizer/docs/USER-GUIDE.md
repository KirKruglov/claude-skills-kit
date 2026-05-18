# User Persona Synthesizer — User Guide

Learn how to turn your CustDev interview notes into structured, evidence-backed user persona cards.

---

## Quick Start

Here's the fastest way to get your personas:

1. Gather 3+ interview transcripts or notes (any format)
2. Say: "Synthesize personas from my interviews" and paste the content
3. Get back a markdown document with persona cards, verbatim quotes, and a synthesis summary

**Result:** Structured persona cards ready to paste into product documents or stakeholder decks.

**Time:** ~3 minutes

---

## Scenarios

### Scenario 1: Synthesizing Post-Discovery Personas for a Product Team

**Situation:**
You are a product manager who just completed 8 discovery interviews with potential users. The interviews were free-form, notes are scattered across different files, and now you need to present key user segments to your team at the next sprint planning. You have 30 minutes to pull this together.

**What to do:**

1. Gather all 8 interview notes into one place
   - Copy and paste them sequentially, separated by a clear label (e.g., "Interview 1:", "Interview 2:") so the skill can distinguish respondents

2. Trigger the skill by saying: "Synthesize personas from my interviews"
   - Paste all 8 sets of notes
   - Optionally add: "Focus on goals and frustrations" or "Aim for 3 personas"

3. Review the summary table first
   - Check how respondents clustered and whether the groupings feel right
   - If a cluster seems off, you can ask: "Can you merge Persona 1 and Persona 3?"

4. Use the persona cards in your sprint planning doc
   - Copy each card into your shared doc or Notion page
   - The verbatim quotes serve as evidence — no need to attribute them individually

**Expected result:**

You receive a document with:
- A summary table showing 2–4 persona clusters with respondent counts
- Individual persona cards (goals, frustrations, behaviours, and at least one quote each)
- Synthesis notes flagging any tensions between personas

You paste the cards directly into the sprint planning document. The team has a shared understanding of who they're building for, grounded in real data.

**Why this works:** Instead of reading 8 separate files yourself and manually looking for patterns, the skill clusters respondents and surfaces the signal. You save 1–2 hours and produce a more consistent result than manual synthesis.

---

### Scenario 2: Preparing Personas for a Stakeholder Presentation

**Situation:**
You are a UX researcher presenting findings from a 12-person interview study to product leadership. The presentation is in two days. Leadership is data-sceptical and will want to know "how many people actually said that" — so every claim needs to be backed by evidence.

**What to do:**

1. Compile all 12 interview transcripts
   - Full transcripts work best here (more quotes to choose from)
   - Label each clearly: "Respondent 1 — [role], [company type]:"

2. Say: "Create user personas from these transcripts"
   - Paste all transcripts
   - Add: "Include as many verbatim quotes as possible per persona"

3. Review the persona cards
   - Check the respondent counts in the summary table — these are your evidence numbers
   - Verify the verbatim quotes are actually from the transcripts (spot-check 2–3)
   - Use the Synthesis Notes section to address tensions during the presentation

4. Build your presentation slides from the cards
   - Each persona card = one slide (name, profile, goals, frustrations, 1–2 quotes)
   - The summary table becomes an overview slide
   - Synthesis tensions become the "implications" slide

**Expected result:**

You receive persona cards with:
- Respondent counts per persona (e.g., "7 of 12 respondents")
- Verbatim quotes sourced from the transcripts
- Synthesis notes on overlaps and contradictions between personas

Leadership can point at any claim and ask "how many people said this?" — the answer is right there in the respondent count. You present with confidence.

**Why this works:** The skill preserves the chain of evidence from raw transcript to structured card. Stakeholders see real numbers and real quotes, not fabricated archetypes.

---

### Scenario 3: Quick Pass on Sparse Notes

**Situation:**
You are a startup founder who conducted 4 quick user interviews over Zoom. You took rough notes — bullet points, not full transcripts. You need some direction on who your early users are before a pitch meeting tomorrow.

**What to do:**

1. Paste your 4 sets of rough notes as-is
   - Don't clean them up — the skill handles fragmented notes
   - Label each: "User 1:", "User 2:", etc.

2. Say: "Extract personas from transcripts"
   - Don't set expectations too high: sparse notes will produce simpler cards
   - The skill will note if the data is thin

3. Review with realistic expectations
   - You'll get 1–3 persona clusters based on what's available
   - A low-sample warning will appear: treat the personas as preliminary hypotheses
   - The synthesis notes will flag what you couldn't determine from the available data

4. Use as working hypotheses for the pitch
   - Reference personas as "early signals" rather than validated segments
   - Plan 5+ additional interviews to confirm or refute the patterns

**Expected result:**

You receive 1–2 preliminary persona cards with a low-sample warning. Each card includes what could be inferred from the rough notes — enough to structure your thinking, not enough to present as definitive research.

**Why this works:** Even sparse data, systematically organized, is more useful than a blank page. The skill gives you a working framework to refine after more interviews.

---

## Tips

### Tip 1: Label Interviews Clearly to Improve Clustering Accuracy

The skill identifies respondent boundaries using explicit labels ("Interview 1:", "Respondent:", "---") or structural cues. If your notes don't have clear separators, the skill may merge respondents incorrectly. Add a simple label before each set of notes — e.g., "User 1 — Product Manager, SaaS company:" — and clustering will be significantly more accurate.

**Pro tip:** Include the respondent's role and context in the label. This becomes part of the attribute extraction and makes persona names more descriptive.

### Tip 2: More Transcripts = More Reliable Patterns

With 3–5 interviews, you get preliminary hypotheses. With 8–12, you get reliable clusters that hold up under scrutiny. If you have a large batch (20+ interviews), you can split them by segment (e.g., "enterprise users" vs. "SMB users") and run the skill separately for each group, then compare the outputs.

**Pro tip:** If the skill returns only 1 persona for a large batch, it usually means your users are more homogenous than expected — or the interviews covered very different topics. Add context in the optional focus field: "Focus on job-to-be-done patterns."

### Tip 3: Use Verbatim Quotes as Standalone Evidence

The persona cards include quotes sourced directly from your transcripts. These aren't paraphrased — they're the actual words your users said. Use them as standalone evidence in product documents, design briefs, or roadmap discussions. A quote like "I rebuild the same deck from scratch every week" is more persuasive than a bullet point saying "repetitive work."

**Pro tip:** If a quote in the card doesn't sound right or you can't find it in the source, ask: "Show me which interview this quote came from." The skill can trace it back.

---

**Version:** 1.0.0
**Last updated:** 2026-05-18

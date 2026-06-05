# User Guide — Jobs-to-be-Done Extractor

## Quick Start

1. Gather your custdev files (interview notes or transcripts) in one folder — .md or .txt format
2. Trigger the skill: *"Extract jobs to be done"* or *"JTBD from interviews"*
3. Tell Claude which folder to use
4. Receive your JTBD map in seconds

---

## Scenarios

### Scenario 1: After a round of product interviews

**Situation:** You've completed 6 user interviews and saved your notes as separate .md files in a `research/interviews/` folder. You have a roadmap meeting tomorrow and need to present user needs.

**What to do:**
1. Say: *"Extract jobs to be done from my interview notes"*
2. When asked, provide the folder path: `research/interviews/`
3. Claude reads all 6 files, clusters motivation signals, and builds a JTBD map
4. Review the output: the table ranks jobs by frequency (how many interviewees mentioned them), with High/Medium/Low confidence labels
5. Paste the JTBD table and Evidence section into your meeting prep doc

**Expected result:** A ranked JTBD map with 4–8 statements, evidence quotes per job, and a Patterns & Gaps section highlighting which themes appeared most consistently.

---

### Scenario 2: Synthesizing notes from multiple researchers

**Situation:** Three team members conducted interviews independently and each saved their notes in the same shared folder. You need a unified view of what users want — without reading 12 separate files manually.

**What to do:**
1. Ensure all note files are in one folder (even from different researchers)
2. Trigger: *"Synthesize custdev notes — I have files from three interviewers"*
3. Claude processes all files and cross-references patterns
4. Check the "Patterns & Gaps" section: themes appearing across multiple interviewers' notes get High confidence; one-off observations get flagged as blind spots worth further investigation

**Expected result:** A synthesized JTBD map that surfaces shared patterns (High confidence) and outliers (Low confidence), saving hours of manual cross-referencing.

---

### Scenario 3: Processing raw interview transcripts

**Situation:** You have verbatim transcripts from recorded interviews — Q&A format with interleewer questions and respondent answers mixed together.

**What to do:**
1. Save transcripts as .txt or .md (no special formatting required)
2. Trigger: *"What are my users trying to do? I have interview transcripts"*
3. Claude focuses on respondent turns, ignoring interviewer questions
4. If transcript format is ambiguous, Claude notes this in the output

**Expected result:** JTBD statements extracted from respondent answers only, with direct quotes as evidence. Interviewer questions are excluded from the analysis.

---

## Tips

- **Optimal file count:** 5–10 files gives the most meaningful frequency analysis. Fewer than 3 limits cross-file comparison; more than 15 increases processing time but still works.
- **File quality matters:** Files with actual user quotes yield stronger evidence than paraphrased summaries. Even rough notes work — Claude extracts motivation signals, not polished prose.
- **Use the Patterns & Gaps section:** Single-source signals (Low confidence) are not noise — they may indicate underserved segments or unexplored needs worth follow-up research.

---

## Output Reference

The skill produces a JTBD map with four sections:

| Section | Contents |
|---------|----------|
| Jobs-to-be-Done table | Ranked JTBD statements, frequency, confidence, source files |
| Evidence | Verbatim (or near-verbatim) quotes per JTBD |
| Patterns & Gaps | Recurring themes (High confidence) + single-source signals |
| Notes | File count, skipped files, confidence scale definition |

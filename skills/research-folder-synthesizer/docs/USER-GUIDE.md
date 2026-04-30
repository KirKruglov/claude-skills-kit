# Research Folder Synthesizer — User Guide

Learn how to turn a folder of scattered research files into a structured thematic report.

---

## Quick Start

Here's the fastest way to get a synthesis:

1. Collect your research files into one folder (`.md` or `.txt`)
2. Say: "Synthesize my research folder" and provide the folder path
3. Get back `research-synthesis.md` with themes, key findings, and a source index

**Result:** A structured, ready-to-use synthesis document you can share or use as input for your next writing task.

**Time:** ~5 minutes for folders with up to 10 files.

---

## Scenarios

### Scenario 1: Preparing to Write a PRD After a UX Research Sprint

**Situation:**
You are a product manager who spent the past week running user interviews and collecting research. You now have 8 files: 4 interview-notes documents, 2 competitor snapshots, and 2 survey result summaries — all in a `/research/ux-sprint/` folder. Before writing the PRD, you need a clear picture of the key findings and user pain points.

**What to do:**

1. Confirm all files are in `.md` or `.txt` format in a single folder.
   - Rename any unusual files if needed; remove images or binary files.

2. Trigger the skill by saying: "Synthesize my research folder" or "Research synthesis — /research/ux-sprint/"
   - Add a focus question: "Focus on user pain points and unmet needs"

3. Provide the folder path when prompted.
   - The skill will list all files it found and begin reading them.

4. Review `research-synthesis.md` when complete.
   - Read the **Executive Summary** to get the high-level picture.
   - Use the **Themes** section as your PRD's "User Problems" structure.
   - Check **Contradictions & Gaps** to identify areas where you need more research.

**Expected result:**

You receive a document with 3–4 named themes (e.g., "Navigation Friction", "Search Relevance", "Onboarding Clarity"), each with key findings and source attribution. The contradictions section flags where interview data and survey data disagree — giving you specific follow-up questions.

**Why this works:** Instead of re-reading 8 files before writing, you have a single 2-page synthesis. Your PRD "Problems" section is essentially already drafted.

---

### Scenario 2: Consolidating Competitor Research Before a Strategy Review

**Situation:**
You are a consultant preparing for a quarterly strategy review. Over the past month, your team saved notes, article excerpts, and competitor profiles to a shared folder. The folder now has 12 files with varying structure. You need to walk the client through "what we know" in a 30-minute session tomorrow morning.

**What to do:**

1. Download or access the research folder locally (e.g., `/strategy/competitor-research/`).

2. Say: "Research synthesis — competitor research folder"
   - Add: "Focus question: Where are the main competitive gaps we can exploit?"

3. Provide the folder path.
   - The skill will process all 12 files and note any it skips (e.g., `.pdf` binaries).

4. Open `research-synthesis.md` and scan the Themes section.
   - Identify the 2–3 strongest themes to anchor your client presentation.
   - Copy the **Key Findings** bullets directly into your slide deck.
   - Use the **Source Index** to show the client which files back each claim.

**Expected result:**

You receive a synthesis with themes like "Competitor A's pricing advantage", "Market gap in self-service onboarding", and "Shared weakness: mobile experience." Each theme links back to specific files, so you can answer "where does that come from?" in the client session without re-reading everything.

**Why this works:** The synthesis replaces the 30 minutes you'd spend skimming 12 files the night before. You arrive prepared with a structured argument, not just raw notes.

---

### Scenario 3: Making Sense of a Research Dump Before Writing an Article

**Situation:**
You are a researcher or content creator. You've been saving notes and article excerpts about a topic for 3 weeks. You now have 15 files in `/notes/ai-agents-research/`. Some are in English, a few are in Russian. You need to write a 2,000-word article but aren't sure what the main narrative should be.

**What to do:**

1. Point the skill to your notes folder.
   - Say: "Synthesize all files in /notes/ai-agents-research/"

2. Optionally add a focus: "Focus on practical applications and limitations."

3. Read the **Executive Summary** in the output.
   - This is your article's thesis in 3–5 sentences.
   - If it doesn't feel right, note which themes seem most important and iterate.

4. Use the **Themes** section as your article's outline.
   - Each theme becomes a section in your article.
   - The **Key Findings** bullets become supporting evidence.

5. Check **Contradictions & Gaps** — these are natural tension points that make for compelling writing.

**Expected result:**

You receive a thematic map of your 15 files. The executive summary gives you an angle. The contradictions give you the "but on the other hand…" moments that make an article interesting. The source index tells you which files to re-read for each section.

**Why this works:** You skip the "staring at a blank page" problem. The synthesis gives you structure — all you have to do is write.

---

## Tips

### Tip 1: Use a Focus Question for More Targeted Synthesis

If you leave the focus question blank, the skill clusters by natural topic affinity. If you add a focus question, it weights the synthesis toward content relevant to your question. For best results, make the focus question specific and outcome-oriented: "What are the main barriers to adoption?" works better than "What do users think?"

**Pro tip:** Run the synthesis twice — once without a focus question (to see what the data says naturally) and once with one (to get a targeted answer). The two outputs are often complementary.

### Tip 2: Clean Up Binary Files Before Running

The skill skips unreadable files (images, `.pdf` binaries, `.docx` files) and lists them in a "Skipped files" note. If most of your research is in PDFs, convert them to `.txt` first (copy-paste the text, or use a text extraction tool). The more readable files you have, the richer the synthesis.

**Pro tip:** For PDFs you can't convert, paste the key excerpts into a `.md` file and save it as `source-name-excerpts.md` before running the skill.

### Tip 3: Use the Source Index to Trace Claims Back to Files

The source index at the end of `research-synthesis.md` maps each file to its main topic and language. When a stakeholder asks "where does this finding come from?", check the source attribution next to each key finding, then cross-reference the source index to find the original file. This is especially useful in client settings where transparency matters.

---

**Version:** 1.0.0
**Last updated:** 2026-04-30

# Industry Trend Brief — User Guide

Learn how to turn your weekly reading pile into a structured trend brief for your product team.

---

## Quick Start

Here's the fastest way to get a trend brief:

1. Save 3–5 articles or notes as md or txt files into one folder
2. Say: "Industry trend brief from [folder path]"
3. Get back a brief with ranked themes and product team takeaways

**Result:** A structured brief you can paste into a team update or use to prepare for a planning session.

**Time:** ~3 minutes

---

## Scenarios

### Scenario 1: Preparing for a Weekly Team Sync

**Situation:**

You are a product manager who spends 30–60 minutes a week reading industry news and saving interesting articles. Monday morning you have a team sync where you want to share what's happening in the market. Instead of reading everything again and summarizing on the fly, you want a brief ready to share.

**What to do:**

1. During the week, paste or save articles into a folder (e.g., `~/reading/weekly/`)
   - One file per article, md or txt format
   - Even rough copy-paste works — the skill handles unstructured text

2. On Monday morning, trigger the skill:
   - Say: "Industry trend brief from ~/reading/weekly/"
   - Or: "Trend signals from articles in [folder path]"

3. Review the brief before the sync
   - Check the **Summary** line — use it as your opening statement
   - Review **Takeaways** for each theme — these are ready-to-use talking points
   - Check **What to Watch** for topics worth mentioning as emerging

4. Share the brief with your team
   - Paste into Slack, Notion, or wherever your team syncs
   - Reference source filenames if teammates want to read further

**Expected result:**

You receive a brief with 3–5 ranked themes, each with a one-sentence takeaway. The sync preparation that used to take 20 minutes now takes 3. Your team gets curated signals instead of raw links.

**Why this works:** Instead of summarizing from memory, you get a structured output from your actual reading. The signal strength ranking tells you which themes deserve discussion time.

---

### Scenario 2: Building a Competitive Context for Roadmap Planning

**Situation:**

You are preparing for a quarterly roadmap review and want to add an "Industry Context" section to your deck. You've accumulated 8 articles and research snippets across the past month on topics like AI tooling, developer experience shifts, and enterprise procurement changes. You need a structured summary you can include without spending 2 hours writing it.

**What to do:**

1. Collect all accumulated articles into one folder
   - Rename files to describe the topic (e.g., `enterprise-ai-adoption.md`, `dev-experience-trends.txt`)
   - No need to clean up the content — rough pastes are fine

2. Trigger the skill:
   - Say: "Industry trend brief from [folder path]"
   - Or: "Summarize my industry reading for the roadmap"

3. Review the themed output
   - Each theme section maps to a potential section in your roadmap "Industry Context" slide
   - High-strength signals are backed by multiple sources — safe to include without caveats
   - Medium-strength signals can be framed as "emerging trends worth watching"

4. Paste theme sections into your deck or document
   - Use the **Takeaway for product team** line as the slide header or bullet point
   - Reference source files in footnotes for credibility

**Expected result:**

You receive a structured brief covering 3–4 industry themes with ranked signal strength. This becomes the "Industry Context" section of your roadmap, ready to paste with minimal editing. Time saved: 1–2 hours of manual synthesis.

**Why this works:** The skill turns scattered reading into a structured, sourced brief. High/medium signal strength ratings give you confidence about what to highlight versus what to hedge.

---

### Scenario 3: Single-Topic Deep Dive Before a Strategy Meeting

**Situation:**

You are heading into a strategy discussion about whether to invest in a new capability area (e.g., AI-powered onboarding). You've saved 4 articles specifically on that topic and want a thorough brief before the meeting — not a multi-theme overview, but a focused deep dive.

**What to do:**

1. Create a focused folder with only on-topic articles
   - 4 files covering different angles: market data, product examples, customer behavior, analyst commentary

2. Trigger the skill:
   - Say: "Industry trend brief from [folder path]"
   - The skill will detect single-topic coverage and automatically generate a deep-dive brief

3. Review the deep-dive output
   - The brief will show one theme with all extracted signals
   - Cross-source signals (same point from multiple articles) are merged — you see the consensus view
   - Diverging signals are listed separately, useful for surfacing tensions in the discussion

4. Use as pre-read material
   - Distribute the brief to meeting participants as preparation material
   - Reference specific signals ("three sources confirm X") during the discussion

**Expected result:**

You receive a focused brief on one topic with all relevant signals consolidated. It's more detailed than a multi-theme brief and easier to share as pre-read than sending 4 raw links.

**Why this works:** Single-topic mode gives depth where multi-theme mode gives breadth. For focused strategy sessions, you get a richer signal set instead of a superficial overview.

---

## Tips

### Tip 1: Name Files to Help with Source Attribution

The brief shows source filenames next to each signal. If files are named descriptively (e.g., `gartner-ai-report-2026.md` instead of `article1.md`), the brief is more useful — recipients know exactly where to find more context.

**Pro tip:** A quick rename before running the skill takes 30 seconds and makes the output significantly more shareable.

### Tip 2: For Fresh Signals, Include Dates or "This Week" Markers in File Names or Content

The skill looks for recency signals in content. If your articles have dates or phrases like "just launched" or "Q1 2026", these are used to prioritize recent signals over older ones. If files mix old and new content, the skill will flag this.

**Pro tip:** Add a date prefix to file names (e.g., `2026-05-27-ai-tools-article.md`) to make recency clear even if the article body doesn't have a date.

### Tip 3: Run It Weekly, Not Retroactively

The skill works best on a focused, time-bounded reading set — ideally 1 week's worth of articles. Running it on 3 months of accumulated content produces a wide but shallow brief. For deeper historical analysis, consider running it on 2-week batches and comparing the outputs.

**Pro tip:** Set up a recurring folder (e.g., `reading/2026-W22/`) and archive files weekly. This also makes past briefs easy to compare.

---

**Version:** 1.0.0
**Last updated:** 2026-05-29

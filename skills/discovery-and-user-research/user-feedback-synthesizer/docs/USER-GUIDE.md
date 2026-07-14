# user-feedback-synthesizer — User Guide

Turn raw feedback files into a prioritized insight report in one step — no tagging, no spreadsheets, no manual clustering.

---

## Quick Start

Open a conversation with Claude and say:

> "Synthesize feedback from [folder path or file list]"

Claude will process your files and save `feedback-insights-YYYY-MM-DD.md` to your working folder.

---

## Step-by-Step Walkthrough

**Step 1** — Collect your feedback files

Put all files you want to analyze in one folder. Supported formats: `.md`, `.txt`, `.csv`.

**Step 2** — Trigger the skill

Use one of these phrases:
- "Synthesize feedback from interviews/"
- "Analyze user interviews in /path/to/files"
- "User feedback report from feedback-batch/"

**Step 3** — (Optional) Add a focus area

Narrow the analysis to a specific topic:
> "Synthesize feedback from interviews/ — focus on checkout experience"

If no focus area is given, Claude will synthesize all themes found.

**Step 4** — Review the output

Open `feedback-insights-YYYY-MM-DD.md`. You'll find:
- Themes ranked by how many sources mention them
- Quotes that support each theme
- A prioritized insights table
- Open questions to investigate next

---

## Scenarios

### Scenario 1: Monthly user interview batch

**Situation:** You've finished 8 user interviews this month and saved each transcript as a `.md` file in `interviews/march/`.

**What to do:**
> "Synthesize feedback from interviews/march/"

**What you get:**
- Themes extracted from all 8 transcripts
- Top quotes per theme with source file references
- Insights table: High priority items backed by 3+ interviews, Medium by 2
- Open questions: signals that appeared in only 1 interview but seem important

---

### Scenario 2: Survey CSV export

**Situation:** Your NPS survey closed and you exported responses to `nps-q1.csv`. You want to know what drives dissatisfaction.

**What to do:**
> "User feedback report from nps-q1.csv — focus on dissatisfaction signals"

**What you get:**
- Themes extracted from survey rows
- Pain and Confusion signals prioritized
- A section of open questions for follow-up research

---

### Scenario 3: Mixed sources (interviews + support tickets)

**Situation:** You have interview transcripts in `.md`, and a ticket export in `.csv`. You want to compare what users say in interviews vs. what they escalate in support.

**What to do:**
> "Analyze user interviews — process interviews/ folder and tickets-export.csv together"

**What you get:**
- Unified theme list across both source types
- Source file references per quote show which themes come from interviews vs. tickets
- Split signals flagged when interview and ticket data conflict

---

## Tips

- **More files = better patterns.** With fewer than 3 files, Claude will warn that findings may reflect individual opinions rather than trends.
- **Use focus areas for targeted analysis.** If you have 20 files but only care about one topic, a focus area prevents noise.
- **Quotes are verbatim.** Claude never paraphrases. If a quote looks odd, it's because the source file contained that exact text.
- **Open Questions is your next research agenda.** Items listed there didn't reach threshold but may still matter — check them before closing the research cycle.

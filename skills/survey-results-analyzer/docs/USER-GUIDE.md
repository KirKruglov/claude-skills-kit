# Survey Results Analyzer User Guide

Learn how to analyze survey CSV exports and get structured insights — frequencies, themes, and Top-3 findings — in minutes.

---

## Quick Start

Here's the fastest way to get a survey analysis:

1. Export your survey as CSV (Google Forms → Responses → Download CSV)
2. Say: "Analyze survey results" and attach the file
3. Get back `survey-analysis-{filename}.md` with quantitative breakdown, theme clusters, and Top-3 insights

**Result:** A ready-to-share markdown report covering all questions — close-ended frequencies and open-ended themes.

**Time:** ~3 minutes

---

## Scenarios

### Scenario 1: Reviewing Post-Launch NPS Survey Before Stakeholder Meeting

**Situation:**
You are a product manager. Your team launched a new feature 2 weeks ago and collected 45 responses via Google Forms. The survey includes a satisfaction rating (1–5), an NPS score (1–10), and two open-ended questions ("What do you like?" and "What should we improve?"). You have a stakeholder review in 2 hours and need to present clear findings — not a raw spreadsheet.

**What to do:**

1. Export the survey data from Google Forms
   - Go to Responses tab → click the Google Sheets icon → File → Download → CSV
   - Save the file (e.g., `feature-launch-survey.csv`)

2. Trigger the skill by saying: "Analyze survey results"
   - Attach `feature-launch-survey.csv` or share the path in your workspace folder

3. Wait for the report (usually under 1 minute)
   - The skill auto-detects the Likert columns and open-ended columns
   - No setup or column mapping needed

4. Review the Top-3 Insights section first
   - Copy the 3 insight blocks directly into your stakeholder deck as "Key Findings"
   - Use the Quantitative section for supporting numbers
   - Use the Qualitative themes as "User Verbatims"

**Expected result:**

You receive `survey-analysis-feature-launch-survey.md` with:
- Summary table showing all 4 questions at a glance
- Quantitative section: satisfaction mean = 4.1/5, NPS mean = 7.8/10 with distribution breakdown
- Qualitative section: Top themes from both open-ended questions with frequency % and example quotes
- Top-3 Insights block ready to paste into your deck

You walk into the stakeholder meeting with a one-page narrative built from actual data — not "the survey looked positive overall."

**Why this works:** Instead of manually counting responses in a spreadsheet and guessing themes in open-ended feedback, the skill does both automatically. You save 1–2 hours of analysis work and present credible, evidence-backed findings.

---

### Scenario 2: Analyzing Team Retrospective Survey to Identify Process Issues

**Situation:**
You are an engineering lead. After a difficult quarter, your Agile coach ran a 5-question retrospective survey across 18 team members. The survey covers sprint rating (1–5), process quality (1–5), collaboration score (1–5), open blockers, and suggestions. You need to identify what's actually driving low scores — not guess — before the quarterly planning session next week.

**What to do:**

1. Export the retrospective survey CSV from your survey tool
   - SurveyMonkey: Analyze → Export → All responses → CSV
   - Typeform: Results → Export → CSV

2. Trigger the skill: "What are the key insights from this survey?"
   - Attach the CSV

3. Focus on the Qualitative Analysis section
   - Review theme clusters for "open blockers" — note the top theme and its % frequency
   - Look for themes that also appear in the "suggestions" column (cross-column pattern)

4. Review Top-3 Insights for cross-column correlations
   - If the skill finds that low sprint ratings correlate with specific qualitative themes, that's your root cause
   - Use this as the "problem statement" to open your quarterly planning session

5. Share the report with the Agile coach and team leads
   - Save `survey-analysis-retro.md` to your shared workspace folder
   - Use it as the basis for the retrospective discussion agenda

**Expected result:**

You receive a report showing:
- Three Likert columns with means and distributions (quickly see which dimension scores lowest)
- Two qualitative theme tables showing top blockers and suggestions grouped by frequency
- Top-3 Insights flagging any cross-column patterns (e.g., "team members citing communication gaps scored process quality 1.4 points lower than average")

You enter the planning session with a data-backed problem statement and concrete theme evidence — not anecdotes.

**Why this works:** The skill reads all 18 response rows across 5 columns and identifies what's systematic vs. isolated. You don't manually code open-ended responses. You get themes in minutes, not hours.

---

### Scenario 3: Synthesizing Customer Feedback Survey Across Multiple Questions

**Situation:**
You are a UX researcher. You ran a 6-question usability survey after a prototype test (12 participants). The survey includes task completion confidence (1–5), ease of use (1–5), time-on-task estimation (1–5), which features were confusing (multiple choice), and two open-ended fields (what worked, what didn't). You need to write a usability report for the design team — but you only have 30 minutes.

**What to do:**

1. Download the usability survey CSV from your tool
   - Make sure the CSV includes all 12 participant rows

2. Trigger: "I have a survey CSV to analyze"
   - Attach the file

3. Review the Summary Table first
   - Get a quick read: which Likert columns have means below 3.0 (problem areas)?
   - Check which multiple-choice option was selected most frequently

4. Dive into Qualitative Analysis for the two open-ended columns
   - Copy the theme tables into your usability report as "User-Reported Issues" and "User-Reported Successes"
   - Use the example quotes as direct verbatims in your report

5. Use Top-3 Insights as the executive summary
   - These map directly to your "Key Findings" section in a standard UX report

**Expected result:**

You receive a structured report with:
- 3 Likert means (you see at a glance that "ease of use" scored 2.8 — a red flag)
- 1 multiple-choice distribution (most selected option = "navigation was unclear")
- 2 qualitative theme tables with verbatims
- Top-3 Insights synthesizing the cross-column signal

You write your usability report in 30 minutes using the report as a scaffold. Design team immediately sees what's broken and has evidence to prioritize the navigation fix.

**Why this works:** The skill's Top-3 Insights cross all columns — so it catches the finding that "ease of use" scores are low AND "navigation confusion" is the #1 qualitative theme, linking the quantitative signal to the qualitative root cause.

---

## Tips

### Tip 1: Clean Your CSV Header Row Before Analyzing

Survey tools sometimes export messy headers like "Rate your experience with our product on a scale of 1 to 5 where 1 is very poor and 5 is excellent." The skill reads these as column identifiers — very long headers make the report harder to scan. Before running the analysis, shorten headers in your spreadsheet to 5–8 words (e.g., "Product experience (1–5)"). The report will be significantly cleaner.

**Pro tip:** Do this in Google Sheets before exporting to CSV — it takes 2 minutes and makes the Summary Table readable at a glance.

### Tip 2: Include at Least One Open-Ended Question for Richer Insights

The skill's Top-3 Insights engine generates the most actionable findings when it can cross-reference quantitative scores with qualitative themes. If your survey has only close-ended questions, the insights will be purely statistical. If you have at least one open-ended column, the skill can identify *why* scores are high or low — not just *that* they are.

**Pro tip:** Even a single "What else would you like to share?" field dramatically improves the insight quality. Run this survey again with one open-ended question added if your current results feel thin.

### Tip 3: Use the Report as a Stakeholder Artifact, Not Just Analysis

The output file (`survey-analysis-{name}.md`) is designed to be shared directly. Copy it into Notion, Confluence, or a shared Google Doc. The Summary Table works as a slide-ready table. The Top-3 Insights block works as an executive summary. You don't need to reformat — just copy-paste sections into your existing templates.

**Pro tip:** If you regularly present survey results to stakeholders, save the `survey-analysis-*.md` files in a dedicated `/surveys/` folder in your workspace. Over time, you'll have a searchable archive of all survey findings — useful for spotting trends across quarters.

---

**Version:** 1.0.0  
**Last updated:** 2026-05-19

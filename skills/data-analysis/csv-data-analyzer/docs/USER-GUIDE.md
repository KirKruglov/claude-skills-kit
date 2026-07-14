# User Guide: CSV Data Analyzer

This guide shows how to use the CSV Data Analyzer skill in three realistic scenarios. No technical background required.

---

## Quick Start

1. Have a CSV file ready in your Cowork workspace (upload it or confirm it's in your selected folder)
2. Say: **"Analyze my CSV"** (or any trigger phrase from the README)
3. Answer one question about what you want to understand
4. Read the insights — they're written in plain business language

That's it. No configuration, no code, no formulas.

---

## Scenario 1: Monthly Sales Report

**Situation:** You've exported your monthly sales data from your CRM into a CSV. You want to know which region and product performed best — but you don't want to open Excel and build pivot tables.

**What to do:**
1. Upload `sales-june.csv` to your Cowork workspace
2. Say: "Analyze this CSV file"
3. Claude profiles the data and asks: "What would you like to understand — summary statistics, trends over time, top/bottom items, comparisons between groups, or something else?"
4. Reply: "Which region had the most revenue?"
5. Claude returns a ranked table of regions by revenue with a 2-sentence interpretation

**Expected result:**
```
### Key Insights
1. EMEA generated 42% of total revenue ($1.2M), the highest across all regions.
2. APAC grew 18% vs. the previous period, while AMER declined 7%.
3. The top-performing region (EMEA) outperformed the lowest (LATAM) by 3.1x.
```

**Tips:**
- You can ask follow-up questions: "Now show me the top 3 products in EMEA"
- If Claude doesn't recognize a column name in your question, it will ask which column you mean — just answer naturally

---

## Scenario 2: Sprint Task Audit

**Situation:** Your sprint ends in 2 days. You've exported your task board to CSV and want a quick read on what's in what status and who's overloaded.

**What to do:**
1. Put `sprint-tasks.csv` in your selected Cowork folder
2. Say: "Help me understand this data"
3. Claude shows you column names and asks what you want to understand
4. Reply: "Show how tasks break down by status and assignee"
5. Claude groups the data and flags imbalances

**Expected result:**
```
### Key Insights
1. 38% of tasks are still "In Progress" with 2 days left in the sprint.
2. Alex has 11 open tasks — the most of any team member. Sara has 3.
3. All "Blocked" tasks (4 total) are assigned to the backend team.
```

**Tips:**
- You don't need to name the columns exactly — say "who has the most tasks" and Claude figures out the assignee column
- Use the follow-up suggestions to dig into blockers or overdue items

---

## Scenario 3: Survey Results

**Situation:** You ran a 20-question survey and exported responses as CSV. You want the headline numbers before your team meeting in 30 minutes.

**What to do:**
1. Upload `survey-results.csv`
2. Say: "What insights can you find in this spreadsheet?"
3. When asked what to understand, reply: "Summary stats and any obvious patterns"
4. Claude profiles each column, counts response distributions for choice questions, and summarizes open text patterns

**Expected result:**
```
### Key Insights
1. 78% of respondents rated onboarding 4 or 5 out of 5.
2. The lowest-rated item was "documentation clarity" with an average of 2.8/5.
3. 12 of 45 open-text responses mentioned "slow setup" as a frustration.
```

**Tips:**
- If your survey has many columns, tell Claude which section to focus on: "Focus on the onboarding questions (columns 5–9)"
- For open-text columns, Claude reads and summarizes patterns — no NLP tools needed

---

## Tips and Best Practices

**Before you start:**
- Make sure the CSV has a clear header row (first row = column names)
- If your file is very large (thousands of rows), Claude will sample it and let you know

**Getting better results:**
- Be specific in your follow-up: "Which product had the highest average order value?" works better than "tell me more"
- If Claude's column type detection seems off, mention it: "The 'revenue' column is in thousands, not full dollars"
- For time-based data, mention the time column by name: "The date column is called 'created_at'"

**When Claude asks a clarifying question:**
- Answer in plain language — you don't need to use technical terms
- If you're not sure what you want, say "what's most interesting in this data?" and Claude will pick the most notable finding

**Limitations to know:**
- Charts and visual graphs are not available in this skill — copy the data table into Excel or Google Sheets to visualize
- Claude does not modify or overwrite your original file
- Files larger than ~500 rows are sampled; for full-dataset analysis on very large files, consider the `data:analyze` skill (requires Claude Code)

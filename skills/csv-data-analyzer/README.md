# CSV Data Analyzer

Analyze any CSV file through a conversational flow — no code, no Python, no external plugins required. Claude reads your file, profiles its structure, and guides you to the insights you need through a single clarifying question.

Designed for non-technical users who regularly work with exported data: sales reports, task lists, CRM exports, survey results, expense files.

---

## Requirements

- A CSV file accessible in your Cowork workspace (uploaded or in the selected folder)
- No additional setup, API keys, or tools needed

---

## How to Use

1. Upload your CSV file to the Cowork workspace (or confirm it's in your selected folder)
2. Trigger the skill with one of the phrases below
3. Claude profiles your dataset and asks one question: what would you like to understand?
4. Answer in plain language — Claude performs the analysis and delivers numbered insights
5. Review the results and optionally explore follow-up directions

---

## Examples

**Example 1: Sales export**

> "Analyze my CSV" + uploads `sales-q1.csv`

Claude reads the file, reports: 847 rows, 6 columns (date, region, product, units, revenue, rep). Asks: "What would you like to understand — summary statistics, trends over time, top/bottom items, or something else?" User replies: "Which product made the most revenue?" → Claude returns a table of products ranked by revenue with plain-language interpretation.

**Example 2: Task list**

> "Help me understand this data" + points to `sprint-tasks.csv`

Claude profiles the file: 63 rows, columns include status, assignee, priority, estimate. User says: "Show me how tasks break down by status." Claude returns a grouped count table and notes that 40% of tasks are still in "In Progress" with the sprint ending this week.

---

## Triggers

| Language | Trigger Phrase |
|----------|---------------|
| EN | `analyze my CSV` |
| EN | `analyze this CSV file` |
| EN | `help me understand this data` |
| EN | `what insights can you find in this spreadsheet` |
| RU | `проанализируй CSV` |
| RU | `разбери мой файл данных` |
| RU | `что в этом CSV` |
| RU | `помоги понять данные из таблицы` |

---

## What This Skill Does and Doesn't Do

**Does:**
- Read CSV files directly from your Cowork workspace
- Profile structure: row count, column types, sparse columns, missing data
- Perform natural-language analysis: summaries, trends, rankings, group comparisons
- Deliver business-readable insights without technical jargon
- Handle large files by sampling (>500 rows)

**Doesn't:**
- Generate charts or visual output (suggest pasting the table into Excel/Sheets for that)
- Execute Python or other code
- Connect to external databases or APIs
- Modify or overwrite your original file

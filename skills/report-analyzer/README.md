> **[Версия на русском языке](../report-analyzer-ru/README.md)**

# Report Analyzer — Claude Cowork Skill

A skill for Claude Cowork that analyzes large reports (PDF, PPTX) and produces a structured summary with key data and insights.

## Who it's for

Product managers, marketers, analysts, finance professionals, C-level executives — anyone who works with a high volume of public reports from consulting firms and market research providers.

## Problem it solves

- Saves time reading 50–100 page reports
- Lets you quickly assess the content and value of a report
- Extracts key figures, data, and insights into a single compact document

## What it does

1. Takes a report file (PDF or PPTX)
2. Asks 3 clarifying questions: language, analysis focus, file format
3. Reads and analyzes the content
4. Produces a structured document (up to 1.5 pages)

## Output document structure

- **Report metadata** — title, author, date, length, language, type
- **Executive Summary** — core thesis in 3–5 sentences
- **Key figures and data** — table with metrics and context
- **Key insights** — 5–7 items
- **Report structure** — table of contents with section summaries

## Supported formats

**Input:** PDF, PPTX (Russian and English)

**Output:** .md, .pdf, .docx (user's choice)

## Triggers

`analyze report`, `report summary`, `report analysis`, `key takeaways`, `break down the report`, `what's in the report`, `summarize the report`

## Requirements

- Claude Cowork (desktop app)

All required libraries are installed automatically on the first run. No manual setup needed.

## Files

```
report-analyzer/
├── SKILL.md          — main skill file
├── README.md         — description (this file)
├── INSTRUCTION.md    — installation and usage guide
└── EXAMPLE.md        — sample output
```

## License

MIT

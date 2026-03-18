---
name: report-analyzer
description: "Analyze large PDF or PPTX reports (consulting, research, market analysis) and produce a structured summary with key data, insights, and section overview. Trigger this skill when the user mentions: 'analyze report', 'report summary', 'report analysis', 'key takeaways from report', 'break down the report', 'what's in the report', 'summarize the report'. Also trigger when a user uploads a PDF or PPTX file and asks to summarize, extract insights, or review it — even if they don't use the exact phrases above. If a large document is uploaded with any request related to understanding its contents, use this skill."
version: 1.0
---

# Skill: report-analyzer

Analyzes large reports (PDF, PPTX) and produces a structured summary with key data and insights.

Target audience: product managers, marketers, analysts, finance professionals, C-level executives.

---

## Workflow

### Step 1 — Locate the input file

The user specifies the report file name in their message. Claude must locate this file.

**Search order:**
1. Check the current project working directory (`input/` folder or project root)
2. Check `/mnt/user-data/uploads/` (if the file was uploaded via the interface)
3. If the user provided a full path — use it directly

**File search:**
```bash
# Search by name in working directory and uploads
find /mnt/user-data/uploads/ -iname "*.pdf" -o -iname "*.pptx" 2>/dev/null
find . -iname "*.pdf" -o -iname "*.pptx" 2>/dev/null
```

**If the file is not found** — ask the user:
> "Please specify the exact file name or path to the report. Supported formats: PDF, PPTX."

**If the format is not supported:**
> "This skill works with PDF and PPTX files. Please provide a file in one of these formats."

**Important:** copy the file to `/home/claude/` before processing to avoid modifying the original.

---

### Step 2 — Ask clarifying questions

Use `ask_user_input` for three questions simultaneously:

**Question 1** (single_select): "What language should the output be in?"
- Russian
- English

**Question 2** (single_select): "Analysis focus?"
- General overview
- Numbers and data
- Strategic takeaways
- Everything combined

**Question 3** (single_select): "Output file format?"
- .md
- .pdf
- .docx

---

### Step 3 — Read and process the file

**For PDF:**
```python
import pdfplumber

with pdfplumber.open("path/to/file.pdf") as pdf:
    text = ""
    for page in pdf.pages:
        text += page.extract_text() or ""
        # Extract tables
        tables = page.extract_tables()
```

Also extract metadata:
```python
from pypdf import PdfReader
reader = PdfReader("path/to/file.pdf")
meta = reader.metadata
pages_count = len(reader.pages)
```

**For PPTX:**
```bash
python -m markitdown presentation.pptx
```

If text extraction fails (scanned PDF) — use OCR:
```python
import pytesseract
from pdf2image import convert_from_path
images = convert_from_path('file.pdf')
for image in images:
    text += pytesseract.image_to_string(image)
```

---

### Step 4 — Perform analysis

Based on the extracted text, generate content according to the structure below.

**Analysis rules:**
- Extract only facts and data from the report — do not infer or fabricate
- All numbers must be exact — as in the original
- Formulate insights in the third person ("the authors note", "the report indicates")
- If data is contradictory — flag it explicitly
- Output document must not exceed 1.5 pages

**How to identify insights (selection criteria):**

An insight is a statement from the report that meets at least one criterion:

1. **Non-obvious** — the finding contradicts conventional wisdom or expectations ("contrary to popular belief...", "unexpectedly...")
2. **Quantitative shift** — a sharp change in a metric (growth/decline >20%, trend reversal, record)
3. **Causal relationship** — the report explicitly links cause and effect ("X led to Y", "the main driver is Z")
4. **Forecast or warning** — authors make a prediction or flag a risk with specific parameters
5. **Actionability** — a finding that enables a management decision (not just a description of the situation)

**How to formulate an insight:**
- One sentence, two at most
- Lead with the substance, not the context
- Include specific numbers where available
- Bad: "The AI market is growing" → Good: "The GenAI market grew 68% YoY to $127B, outpacing analyst forecasts by 15 p.p."

**Number of insights:** 5–7. If the report contains fewer significant findings — do not pad to 5 artificially.

**Adaptation by focus:**
- **General overview** — balanced across all sections
- **Numbers and data** — expanded data table, condensed insights
- **Strategic takeaways** — expanded insights, condensed data table
- **Everything combined** — all sections in full (within the 1.5-page limit)

---

### Step 5 — Generate the output file

Use the structure from the "Output document template" section below.

**By format:**
- `.md` — write directly via `create_file`
- `.pdf` — first generate `.md`, then use the `pdf` skill (read `/mnt/skills/public/pdf/SKILL.md`)
- `.docx` — first generate `.md`, then use the `docx` skill (read `/mnt/skills/public/docx/SKILL.md`)

**File naming:**
`report-summary_REPORT-NAME_YYYY-MM-DD.extension`

Example: `report-summary_mckinsey-ai-trends_2026-03-18.md`

Save the file to `/mnt/user-data/outputs/` and deliver to the user via `present_files`.

---

## Output document template

```markdown
# Report Summary: [Report Title]

**Analysis date:** [date]

---

## Report metadata

| Parameter | Value |
|-----------|-------|
| Title | [full title] |
| Author / source | [company or author] |
| Publication date | [date or year] |
| Length | [page count] |
| Original language | [language] |
| Type | [consulting / research / analytics / market review / other] |

---

## Executive Summary

[3–5 sentences: core thesis of the report, main argument, key conclusion]

---

## Key figures and data

| Metric / indicator | Value | Context |
|--------------------|-------|---------|
| [metric 1] | [value] | [explanation] |
| [metric 2] | [value] | [explanation] |
| ... | ... | ... |

---

## Key insights

1. [insight 1]
2. [insight 2]
3. [insight 3]
4. [insight 4]
5. [insight 5]

---

## Report structure

| Section | Summary |
|---------|---------|
| [Section 1] | [1–2 sentences] |
| [Section 2] | [1–2 sentences] |
| ... | ... |
```

---

## What to avoid

- Do not add personal assessments or recommendations — only report content
- Do not exceed 1.5 pages in the output document
- Do not use filler phrases ("Sure, here's the analysis...")
- Do not retell the entire report — highlight what matters
- Do not round or alter numbers from the original
- Do not create the file until all 3 questions are answered

---

## Dependencies

```bash
pip install pdfplumber pypdf markitdown --break-system-packages
```

For PPTX:
```bash
pip install "markitdown[pptx]" --break-system-packages
```

For OCR (scanned PDFs):
```bash
pip install pytesseract pdf2image --break-system-packages
```

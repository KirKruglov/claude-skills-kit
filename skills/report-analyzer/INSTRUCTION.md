# Guide: Installing and Using Report Analyzer

## Downloading from GitHub

### Option 1 — Download ZIP

1. Go to the repository page on GitHub
2. Click **Code > Download ZIP**
3. Unzip the archive — inside you'll find a `report-analyzer/` folder with the `SKILL.md` file

### Option 2 — Clone the repository

```bash
git clone https://github.com/KirKruglov/claude-skills-kit.git
```

### Option 3 — Download SKILL.md only

On the `SKILL.md` file page in GitHub, click **Raw**, then save the page (Ctrl+S / Cmd+S).

---

## Installing in Claude Cowork

### Method 1 — Via Settings (recommended)

1. Open Claude Cowork
2. Go to **Settings > Customize > Skills**
3. Click **Add Skill**
4. Point to the `report-analyzer/` folder on your computer

### Method 2 — Via command

In the Cowork window:
```
/plugin add report-analyzer
```

### Method 3 — Manual

Copy the `report-analyzer/` folder to the Cowork skills directory:
```
~/.claude/skills/report-analyzer/SKILL.md
```

After installation, the skill activates automatically when trigger phrases are used.

---

## Usage

### Step 1 — Prepare the report file

Place the report file (PDF or PPTX) in your Cowork project working folder — for example, in the `input/` folder. Or make sure the file is in any directory accessible to Cowork.

### Step 2 — Launch the skill

Type one of the trigger phrases in Cowork and specify the file name:

```
analyze report McKinsey_Global_AI_2025.pdf
```

```
report summary input/CB-Insights-State-of-AI-Q4.pptx
```

```
break down the report Statista_EV_Market_Report.pdf
```

Claude will find the file in the project working folder and start processing.

### Step 3 — Answer 3 questions

Claude will ask interactive questions:
1. **Output language** — Russian or English
2. **Analysis focus** — general overview / numbers and data / strategic takeaways / everything combined
3. **File format** — .md / .pdf / .docx

### Step 4 — Get the result

Claude will generate a summary file and offer it for download. The file is saved to the project's `output/` folder.

---

## Output structure

The output document (up to 1.5 pages) contains:

- **Report metadata** — title, author, date, length, language, type
- **Executive Summary** — core thesis in 3–5 sentences
- **Key figures and data** — table with metrics and context
- **Key insights** — 5–7 items with specific findings
- **Report structure** — table of contents with section summaries

---

## Supported formats

| Input | Output |
|-------|--------|
| PDF (incl. scanned with OCR) | .md |
| PPTX | .pdf |
| | .docx |

Input file languages: Russian, English.

---

## FAQ

**Do I need to install Python or any libraries?**
No. Cowork installs all required dependencies automatically on the first skill run.

**Does it work with scanned PDFs?**
Yes. If text cannot be extracted directly, the skill automatically runs OCR.

**Can I analyze a report in English and get the result in Russian?**
Yes. The input file language and the output language are independent settings.

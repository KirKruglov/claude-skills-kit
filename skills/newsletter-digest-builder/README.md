> [Версия на русском языке](README.ru.md)

# Newsletter Digest Builder

Turn a folder of saved articles and newsletters into a focused weekly digest — grouped by topic, ranked by relevance to your role.

---

## Overview

Newsletter Digest Builder takes a folder of saved articles and newsletters (.txt or .md files) and returns a structured weekly digest. It extracts titles and content from each file, groups articles into topic clusters, scores each item by relevance to your stated role (PM, marketer, or custom), and surfaces a "Read This Week" shortlist of 5–7 items. Use this skill when your inbox of saved articles has grown unmanageable, when you want to triage a week's worth of newsletters before a planning session, or when you need to quickly identify which reads are actually relevant to your current work.

Unlike single-file reading list tools, this skill processes an entire folder of articles in one pass — no manual triage required.

---

## Requirements

- A folder with saved articles in `.txt` or `.md` format — one article per file
  - Supported: files with article text, markdown newsletters, saved blog posts
  - Also works: files containing only a URL (digest will be based on URL metadata)
  - Minimum 1 file required; works best with 5–20 articles
- Your current role or focus area stated in your message (e.g., "PM focused on AI product launches" or "Marketer building B2B demand gen")
- No additional tools or skills required

**File tip:** Save newsletters as .txt or .md files in a dedicated folder (e.g., `newsletters/week-21/`). The skill reads all files in the folder in one pass.

---

## How to Use

1. **Prepare your article folder**
   - Save this week's newsletters and articles as `.txt` or `.md` files in a folder
   - Upload the files to the chat or point to the folder path

2. **Trigger the skill by saying:**
   - "Build my newsletter digest" or "Summarize my saved articles"
   - In Russian: "Собери дайджест из рассылок" or "Сделай еженедельный дайджест"

3. **State your role and focus area**
   - Add 1–2 sentences: "I'm a PM focused on AI tools for enterprise" or "Marketer working on SEO and content-led growth"
   - The skill will ask if you forget — it needs this for relevant prioritization

4. **Get your weekly digest**
   - Receive a markdown digest with a "Read This Week" shortlist (5–7 items) and a full list grouped by topic
   - Each item labeled [Must Read] / [Useful] / [Optional] based on relevance to your role

---

## Examples

### Example 1: PM Processing a Week of Newsletters

**Input folder contents (5 files):**
```
ai-product-lessons.md       — article: "What We Learned Shipping Our First AI Feature"
churn-analysis-guide.md     — article: "How to Run Churn Cohort Analysis"
design-tokens-deep-dive.md  — article: "Design Tokens Explained"
b2b-saas-benchmarks.txt     — article: "2026 B2B SaaS Benchmarks Report"
remote-leadership.txt       — article: "Leading Distributed Teams in 2026"
```

**Role:** "I'm a PM building an AI analytics product for B2B SaaS, focused on reducing time-to-insight."

**Output:**
```
## Weekly Digest — 2026-05-21
**Role:** PM building AI analytics for B2B SaaS, focus on time-to-insight
**Articles processed:** 5

---

### Read This Week (Top 3)
1. **What We Learned Shipping Our First AI Feature** — AI/Product · Core lessons directly applicable to your AI product work
2. **How to Run Churn Cohort Analysis** — Analytics · Directly relevant to your time-to-insight metric work
3. **2026 B2B SaaS Benchmarks Report** — Industry · Essential context for positioning your product

---

### Full List by Topic

#### AI / Product
- [Must Read] **What We Learned Shipping Our First AI Feature**

#### Analytics
- [Must Read] **How to Run Churn Cohort Analysis**

#### Industry
- [Must Read] **2026 B2B SaaS Benchmarks Report**

#### UX / Design
- [Useful] **Design Tokens Explained**

#### Leadership
- [Optional] **Leading Distributed Teams in 2026**

---

### Can Skip This Week
- [Optional] **Leading Distributed Teams in 2026** — leadership topic is tangential to your current product focus
```

---

### Example 2: Marketer Triaging a Busy Newsletter Week

**Input folder contents (8 files):** marketing newsletters, SEO articles, product launch posts, engineering deep-dives

**Role:** "Content marketer at a B2B SaaS company, focused on SEO and organic growth."

**Output:**
```
## Weekly Digest — 2026-05-21
**Role:** Content marketer, B2B SaaS, SEO and organic growth
**Articles processed:** 8

### Read This Week (Top 5)
1. **AI and the Future of SEO** — SEO · Directly relevant to your organic growth strategy
2. **Content-Led Growth Playbook** — Content Strategy · Core framework for your current focus
3. **B2B Keyword Research in 2026** — SEO · Actionable tactics for your SEO work
4. **LinkedIn Distribution Tactics** — Distribution · Useful for amplifying your content
5. **Brand Storytelling for SaaS** — Content Strategy · Strong secondary read for content quality

### Can Skip This Week
- [Optional] **Kubernetes Deployment Patterns** — engineering topic, outside your scope
- [Optional] **Venture Funding Trends Q1** — not relevant to content or SEO work
```

---

## Triggers

Use any of these phrases to trigger the skill:

| English | Russian |
|---------|---------|
| Build my newsletter digest | Собери дайджест из рассылок |
| Newsletter digest | Дайджест из статей |
| Summarize my saved articles | Сделай еженедельный дайджест |
| I have too many newsletters to read | У меня накопилось много статей |

---

**Version:** 1.0.0
**Full guide:** [docs/USER-GUIDE.md](docs/USER-GUIDE.md) · [docs/USER-GUIDE.ru.md](docs/USER-GUIDE.ru.md)

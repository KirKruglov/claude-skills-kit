# Reading List Prioritizer

Turn your pile of saved articles into a focused weekly reading plan — grouped by topic, ranked by relevance to your role.

---

## Overview

Reading List Prioritizer takes your personal reading list (a markdown file with article titles and links) and returns a structured weekly reading plan. It detects topics across your saved articles, scores each item by relevance to your current role and focus area, and surfaces a "Read this week" shortlist of 5–7 items. Use this skill when your saved reading list has grown unmanageable, when you want to prioritize articles for a specific project or focus area, or when you need to decide what to read before a planning or strategy session.

---

## Requirements

- A markdown file (.md) with your reading list
  - Supported formats: `[Title](URL)` links, bare URLs, plain text titles, or a mix
  - Minimum 3 items recommended; works with lists of any size
- Your current role or focus area stated in your message (e.g., "PM focused on AI product strategy")
- No additional tools or skills required

**File tip:** Export your reading list from Notion, Obsidian, or any note-taking app as a markdown file. Or paste the list directly into the chat.

---

## How to Use

1. **Prepare your reading list**
   - Export your saved articles as a `.md` file, or copy-paste the list into the chat
   - Include titles and/or URLs — plain text lines work too

2. **Trigger the skill by saying:**
   - "Prioritize my reading list" or "What should I read first this week?"
   - In Russian: "Расставь приоритеты в списке чтения" or "Что мне читать в первую очередь?"

3. **State your role and focus area**
   - Add 1–2 sentences: "I'm a product manager focused on AI tooling for enterprise" or "I work in content marketing, currently focused on SEO"
   - The skill will ask if you forget — it needs this to score relevance

4. **Get your reading plan**
   - Receive a markdown response with a "Read This Week" shortlist (5–7 items) and a full list grouped by topic
   - Each item is labeled [High] / [Med] / [Low] based on relevance to your stated focus

---

## Examples

### Example 1: PM Weekly Reading Prep

**Input:**
```
- [Why AI Products Fail](https://hbr.org/article-1)
- [Design Systems at Scale](https://nngroup.com/article-2)
- [The Future of Work](https://mckinsey.com/article-3)
- [GPT-4 Technical Report](https://arxiv.org/article-4)
- [Product Metrics That Matter](https://lenny.substack.com/article-5)
- [UX Research on Mobile](https://smashingmagazine.com/article-6)
- [Aggregation Theory](https://stratechery.com/article-7)
- [Managing Remote Teams](https://hbr.org/article-8)
```

**Role:** "I'm a PM building an AI writing assistant for B2B SaaS."

**Output:**
```
## Reading Plan — 2026-05-20
**Focus area:** PM building an AI writing assistant for B2B SaaS
**Total items:** 8

### Read This Week (Top 6)
1. Why AI Products Fail — AI/Strategy · Directly relevant: common failure modes for AI product teams
2. GPT-4 Technical Report — AI/Data · Core context for AI writing assistant decisions
3. Product Metrics That Matter — Product · Essential for defining success metrics for your product
4. Aggregation Theory — Business Strategy · Useful lens for platform/distribution thinking
5. Design Systems at Scale — UX/Design · Relevant for scaling the assistant's UI patterns
6. Managing Remote Teams — Leadership · Broadly relevant for PM managing distributed team

### Full List by Topic

#### AI / Data
- [High] Why AI Products Fail
- [High] GPT-4 Technical Report

#### Product Management
- [High] Product Metrics That Matter

#### UX / Design
- [Med] Design Systems at Scale
- [Low] UX Research on Mobile

#### Business Strategy
- [Med] Aggregation Theory
- [Med] The Future of Work

#### Leadership
- [Med] Managing Remote Teams

### Skippable This Week
- [Low] UX Research on Mobile — mobile UX research is tangential to a B2B web-based assistant
```

---

### Example 2: Content Marketer Focus-Filtered List

**Input:**
```
[Content-led Growth](https://contentledgrowth.com/post-1)
[SEO in the Age of AI](https://seoblog.com/post-2)
[B2B Copywriting Frameworks](https://copywriting.substack.com/post-3)
[Kubernetes Best Practices](https://devops.io/post-4)
[LinkedIn Algorithm 2026](https://socialmedia.tips/post-5)
[Writing for Developers](https://techwriting.dev/post-6)
```

**Role:** "Content marketer at a B2B SaaS company, focused on SEO and top-of-funnel."

**Output:**
```
## Reading Plan — 2026-05-20
**Focus area:** Content marketer at B2B SaaS, focused on SEO and top-of-funnel

### Read This Week (Top 4)
1. SEO in the Age of AI — SEO · Directly relevant to your core focus area
2. Content-led Growth — Content Strategy · Core topic for top-of-funnel planning
3. B2B Copywriting Frameworks — Copywriting · High value for B2B content quality
4. LinkedIn Algorithm 2026 — Social/Distribution · Useful for distribution of top-of-funnel content

### Full List by Topic

#### SEO
- [High] SEO in the Age of AI

#### Content Strategy
- [High] Content-led Growth
- [High] B2B Copywriting Frameworks

#### Social / Distribution
- [Med] LinkedIn Algorithm 2026

#### Technical / Developer
- [Low] Writing for Developers
- [Low] Kubernetes Best Practices

### Skippable This Week
- [Low] Writing for Developers — developer-focused writing not relevant to B2B content marketing
- [Low] Kubernetes Best Practices — engineering topic, outside your focus area
```

---

## Triggers

Use any of these phrases to trigger the skill:

| English | Russian |
|---------|---------|
| Prioritize my reading list | Расставь приоритеты в списке чтения |
| What should I read first? | Что мне читать в первую очередь? |
| Help me sort my articles by topic | Сгруппируй мои статьи по темам |
| Reading list prioritizer | Приоритизируй список статей |

---

**Version:** 1.0.0
**Full guide:** [docs/USER-GUIDE.md](docs/USER-GUIDE.md) · [docs/USER-GUIDE.ru.md](docs/USER-GUIDE.ru.md)

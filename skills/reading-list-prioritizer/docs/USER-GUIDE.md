# Reading List Prioritizer — User Guide

Learn how to turn your pile of saved articles into a focused, role-relevant reading plan in minutes.

---

## Quick Start

Here's the fastest way to get your prioritized reading plan:

1. Copy your saved article list (titles and/or URLs) into the chat
2. Say: "Prioritize my reading list" and add your role in one sentence
3. Get back a "Read This Week" shortlist and full list grouped by topic

**Result:** A structured reading plan with [High] / [Med] / [Low] labels and a top-7 shortlist.

**Time:** ~2 minutes

---

## Scenarios

### Scenario 1: Weekly Reading Prep for a Product Manager

**Situation:**
You are a product manager. Over the past week, you saved 15–20 articles from newsletters, Twitter/X, and blog subscriptions to read later. It's Monday morning, you have maybe 2 hours for reading this week, and you want to know which 5–7 articles are most worth your time — specifically for your current focus on shipping an AI feature.

**What to do:**

1. Export your saved articles as a markdown list
   - From Notion: use "Export as markdown"
   - From Obsidian: copy the relevant note
   - Or just paste your article list directly into the chat (one link per line)

2. Trigger the skill by saying: "Prioritize my reading list"
   - In the same message, add your focus: "I'm a PM working on an AI assistant for B2B customers, focused on reducing churn."

3. Upload the .md file or paste the list
   - The skill will parse titles and URLs, detect topics, and score relevance

4. Review the output
   - Start with **Read This Week** — these are your highest-value reads for this week
   - Skim the **Full List by Topic** to see if any [Med] items catch your eye
   - The **Skippable This Week** section saves you from guilt — ignore these without FOMO

**Expected result:**

You receive a plan like:

```
### Read This Week (Top 6)
1. Why AI Products Fail — AI/Strategy · Core context for your AI feature work
2. Churn Prediction Models — AI/Data · Directly relevant to your retention focus
3. Product Metrics That Matter — Product · Essential for defining success metrics
...
```

Each item comes with a one-sentence explanation of *why* it's relevant to your role. You can open just those 5–7 articles and be done.

**Why this works:** Instead of scrolling through 20 articles trying to decide what to read, you get a prioritized shortlist in 2 minutes. The skill considers your role — not just topic overlap — so you spend your reading time on things that actually move your work forward.

---

### Scenario 2: Refocusing Your Reading List After a Strategy Shift

**Situation:**
You are a content marketer. Three weeks ago your team pivoted from brand content to SEO-driven content. Your saved reading list still reflects your old focus — lots of brand strategy, thought leadership, and social media articles. You want to quickly identify what's still relevant and what you should deprioritize so you can focus on building your SEO knowledge.

**What to do:**

1. Open your reading list (wherever you keep it: Pocket, Notion, a text file)
   - Export or copy all saved items — include titles and URLs

2. Say: "What should I read first? I'm now focused on SEO and content-led growth for a B2B SaaS company."
   - Paste the full list in the same message

3. Review the scored output
   - [High] items are aligned with your new SEO focus → read these first
   - [Low] items are from your old brand strategy focus → add them to a "someday" list or delete

4. Archive the Skippable items
   - Copy the **Skippable This Week** list and move those links to an archive folder or simply remove them from your active reading list

**Expected result:**

You receive a grouped list that clearly separates your SEO-relevant reads from the brand strategy and social media articles that no longer fit your current focus. The [High] items give you a clear reading queue for the next 1–2 weeks.

**Why this works:** After a strategy pivot, your reading list is stale — but you haven't had time to manually review 30+ saved items. This skill does the triage in seconds, using your new focus as the scoring lens. You walk away with a clean, relevant reading queue aligned to where you actually need to grow.

---

### Scenario 3: Preparing for a Strategy or Planning Session

**Situation:**
You are a team lead preparing for your quarterly planning session next week. You want to arrive with fresh context on market trends, team management, and product strategy. You have a reading list of 12 articles saved over the past month, but you only have time to read 4–5 before the session.

**What to do:**

1. Copy your 12 saved articles into a markdown list
   - No need to organize them — paste in any order

2. Trigger the skill: "Prioritize my reading list for our quarterly planning session. I'm a team lead in a B2B SaaS company, focused on product strategy and team performance."

3. Review the "Read This Week" shortlist
   - Focus on the [High] items that cover strategy and leadership
   - Note any [Med] items that are specifically about market trends — those are secondary but useful for planning

4. Read in the recommended order
   - Start with the highest-relevance items first (your limited time is best spent there)

**Expected result:**

You receive a shortlist of 4–5 articles specifically relevant to your planning context — strategy frameworks, market signals, team performance data. You arrive at the planning session well-prepared without spending 3+ hours reading everything on your list.

**Why this works:** The skill understands that "quarterly planning" requires strategic context, not tactical how-tos. It ranks market and strategy articles higher than your other saved reads, so you spend your preparation time on what actually matters for the session.

---

## Tips

### Tip 1: Always State a Specific Focus, Not Just Your Role

Saying "I'm a PM" is less useful than "I'm a PM working on AI-powered search for e-commerce, focused on improving click-through rates." The more specific your focus, the more accurate the prioritization. The skill uses your stated focus to distinguish between [High] and [Med] relevance — vague roles lead to vague scoring.

**Pro tip:** If your focus changes week to week, update it in your trigger message. The skill re-scores every time, so you always get a fresh perspective.

### Tip 2: Use Tags in Your List for Better Topic Detection

If your reading list items have tags or notes appended (e.g., `[Article title](url) #strategy #ai`), include them — the skill will pick them up. This is especially helpful for items with generic titles or unfamiliar domains that might otherwise be miscategorized.

**Pro tip:** Even simple notes like "(seen on HN)" or "(from newsletter)" help the skill understand the source context and categorize items better.

### Tip 3: Re-run Weekly to Keep Your List Fresh

The best use of this skill is as a weekly ritual: paste your growing list each Monday, state your current week's focus, and get a fresh reading plan. As your focus shifts and your list grows, the prioritization evolves. Items that were [Low] one week may be [High] the next if your focus shifts toward that topic.

**Pro tip:** Keep a running "master list" in a markdown file and append new saves each week. Run the skill on the full list each Monday — the output gives you a clear "what to read now" view without having to manually triage.

---

**Version:** 1.0.0

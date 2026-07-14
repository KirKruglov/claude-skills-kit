# Newsletter Digest Builder — User Guide

Learn how to turn a folder of saved newsletters and articles into a focused weekly digest in minutes.

---

## Quick Start

Here's the fastest way to get your weekly digest:

1. Save this week's newsletters and articles as `.txt` or `.md` files in one folder
2. Upload the files and say: "Build my newsletter digest. I'm a [your role] focused on [your current priority]."
3. Get back a "Read This Week" shortlist and the full list grouped by topic

**Result:** A structured digest with [Must Read] / [Useful] / [Optional] labels and a top-7 shortlist.

**Time:** ~2 minutes

---

## Scenarios

### Scenario 1: PM Processing a Week of Newsletters Before Monday Planning

**Situation:**
You are a product manager. Each week you save 8–15 articles from newsletters, blog RSS, and Twitter/X bookmarks. It's Sunday evening and you want to walk into Monday's planning session with the right context — specifically around your current focus on reducing user onboarding friction. You don't have time to read everything, but you want to identify the 5–6 articles that are actually worth your Monday morning.

**What to do:**

1. Open your saved articles folder (or browser bookmarks export)
   - Save each article as a `.md` or `.txt` file, or use a browser extension that exports as markdown
   - Name files descriptively: `onboarding-best-practices.md`, `ai-product-metrics.txt`

2. Upload all files to the chat and say: "Build my newsletter digest"
   - In the same message, add your focus: "I'm a PM working on reducing onboarding friction for a B2B SaaS product."

3. Review the output
   - Start with **Read This Week** — these are your highest-value reads right now
   - Check if any [Useful] items in the **Full List by Topic** catch your eye — they're worth a skim
   - Use **Can Skip This Week** to guilt-free archive tangential articles

4. Open and read in shortlist order
   - The 1-sentence relevance note next to each item tells you exactly why it was selected — you'll know if it's worth reading in full

**Expected result:**

```
### Read This Week (Top 5)
1. **The Onboarding Moment That Matters** — Product · Directly on your current friction-reduction focus
2. **Activation Metrics for B2B SaaS** — Analytics · Core metrics framework for your onboarding work
3. **How Notion Redesigned Their First 5 Minutes** — Case Study · Real example applicable to your context
...
```

**Why this works:** Instead of opening 12 browser tabs on Sunday night, you get a 5-item reading list with relevance notes. You walk into Monday having read the articles that actually matter for your week's work.

---

### Scenario 2: Marketer Building a Weekly Content Brief from Saved Reads

**Situation:**
You are a content marketer. You subscribe to 6 newsletters and save articles throughout the week. On Friday, before drafting next week's content plan, you want to identify the trends and insights that could inspire your content topics. You need to quickly separate the strategy-relevant reads from the noise.

**What to do:**

1. At the end of each day, save interesting articles to a folder as `.txt` files
   - Use a consistent naming convention: `2026-05-19-seo-article.txt`
   - Include the source URL at the top of each file — the skill will use it for context

2. On Friday, upload the week's folder and say: "Сделай еженедельный дайджест" (or "Build my newsletter digest")
   - Add your context: "I'm a content marketer focused on SEO and organic growth for a B2B SaaS company. I'm looking for content angle inspiration."

3. Use the digest output to inform your content plan
   - [Must Read] items are likely the strongest content angle candidates — trends or insights your audience will find valuable
   - Topics appearing in multiple [Must Read] items signal a strong weekly theme worth covering
   - [Useful] items might suggest supporting angles or secondary topics

4. Note the dominant topics in the digest
   - If 4 out of 7 shortlisted items are about AI and SEO — that's your theme for the week

**Expected result:**

You receive a digest where the topic groupings reveal what the industry is discussing this week. The [Must Read] shortlist directly feeds your content brief, cutting your content planning research from 45 minutes to 10.

**Why this works:** Your saved articles are already a curated set of what you found interesting. The skill structures and prioritizes them in your professional context — so they become inputs for your work, not just a reading backlog.

---

### Scenario 3: Team Lead Staying Current Across Multiple Domains

**Situation:**
You are a team lead responsible for product, design, and engineering. You subscribe to newsletters across all three domains. Each week you accumulate 20–25 articles, but you can only read 5–7 realistically. You need to pick across domains intelligently — staying informed on strategy while also monitoring technical trends.

**What to do:**

1. Create a weekly articles folder with subfolders by domain, or just mix all files
   - The skill will auto-group by topic regardless of your folder structure

2. Upload all files and say: "Build my newsletter digest"
   - State your cross-domain focus: "I'm a team lead overseeing product, design, and engineering for a 15-person startup. Current priority: Q3 roadmap planning and hiring two senior engineers."

3. Review the topic-grouped full list
   - The full list shows you how many articles landed in each domain this week
   - You'll see immediately if you're over-reading in one area (e.g., too many engineering articles, few product strategy pieces)

4. Use "Can Skip This Week" as a declutter tool
   - Move skippable articles to an archive folder or delete them
   - Your active reading list stays lean and relevant

**Expected result:**

You receive a digest that spans all your domains, with [Must Read] items chosen for their direct relevance to Q3 planning and hiring — not just general interest. The cross-domain shortlist lets you stay informed broadly without spending 3+ hours on it.

**Why this works:** As a multi-domain lead, no single prioritization lens is enough. The skill uses your stated priorities (roadmap + hiring) to select the most cross-relevant reads — so you're not accidentally spending all your reading time in one domain.

---

## Tips

### Tip 1: Save Articles as You Find Them, Digest Weekly

The highest-value workflow is to save articles throughout the week as `.txt` or `.md` files into a dedicated folder, then run this skill once — on Sunday evening or Monday morning. You'll never need to manually triage your reading list again. Each digest is generated fresh, scored against your current focus.

**Pro tip:** Keep a single `newsletters/` folder and clear it after each digest. Your archive stays clean and each week starts fresh.

### Tip 2: State a Specific Focus, Not Just Your Title

"I'm a PM" gives less signal than "I'm a PM working on an AI writing assistant, focused on reducing first-session drop-off." The more specific your focus statement, the more accurate the [Must Read] / [Useful] / [Optional] scoring. The skill uses your focus to distinguish between directly relevant and broadly interesting articles.

**Pro tip:** If your focus shifts mid-week (e.g., a new project lands), update your focus statement in the trigger message. The skill re-scores from scratch each run.

### Tip 3: Include the Source URL at the Top of Each Saved File

When saving an article as `.txt` or `.md`, paste the URL on the first line. The skill uses domain signals (e.g., `lenny.substack.com` → PM newsletter, `nngroup.com` → UX research) to improve topic detection and relevance scoring. Files without URLs are scored based on title and body content only — still useful, but domain context improves accuracy.

---

**Version:** 1.0.0

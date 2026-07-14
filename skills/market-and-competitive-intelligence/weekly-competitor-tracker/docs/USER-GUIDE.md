# Weekly Competitor Tracker — User Guide

Learn how to set up and use Weekly Competitor Tracker to stay on top of competitor changes every week.

---

## Quick Start

Here's the fastest way to get your first delta-report:

1. Create a `competitors/` folder with one `.md` file per competitor
2. Add notes about each competitor (pricing, product, messaging — any format)
3. Say: "Track competitor changes" and provide the folder path
4. Get a baseline summary with instructions to save your snapshot

**Result:** A structured competitor overview saved as `competitor-delta-YYYY-MM-DD.md`, ready for your Monday review.

**Time:** ~5 minutes for setup + ~2 minutes per weekly run

---

## Scenarios

### Scenario 1: Setting Up Weekly Tracking for the First Time

**Situation:**

You are a product manager who monitors 3–4 competitors. Right now you keep scattered notes in different places — browser bookmarks, random docs, memory. You want a structured, repeatable process to check what's changed each week without spending 2 hours manually comparing notes.

**What to do:**

1. Create your competitor folder structure
   - Make a folder called `competitors/`
   - Create one `.md` file per competitor (e.g., `competitors/notion.md`, `competitors/coda.md`)
   - Add H2 sections to each file: `## Product`, `## Pricing`, `## Messaging`, `## Recent News`
   - Fill in what you know today

2. Trigger the skill for your first run
   - Say: "Track competitor changes" and provide the path to your `competitors/` folder
   - Since no snapshot exists yet, the skill will run in baseline mode

3. Review the baseline summary
   - You receive a `competitor-delta-YYYY-MM-DD.md` file with the current state of all competitors
   - This becomes your reference point going forward

4. Save your snapshot
   - Copy all files from `competitors/` to `competitors/snapshot/`
   - This sets your baseline — next week's run will compare against these versions

**Expected result:**

You have a clean `competitors/` folder with notes and a saved snapshot. Next Monday, you update your notes and run the skill again — and you'll get a proper delta showing exactly what changed. You've replaced 2 hours of manual comparison with a 10-minute weekly ritual.

**Why this works:** The folder-based approach means you control what goes in and when. You don't need any integrations or subscriptions — just markdown files you update as you learn things.

---

### Scenario 2: Monday Morning Competitive Review

**Situation:**

You are a team lead who prepares a weekly competitive brief for your product team. Every Monday you want a quick overview of what changed at each competitor — new pricing, product updates, messaging shifts — so you can brief the team at standup and flag anything that needs a response.

**What to do:**

1. Update your competitor notes (Sunday evening or Monday morning)
   - Open each file in `competitors/` and update with anything new you noticed during the week
   - Add notes under relevant sections: pricing change, feature launch, new marketing angle

2. Trigger the skill
   - Say: "Weekly competitor report" or "What changed with my competitors"
   - Provide the path to your `competitors/` folder

3. Review the delta-report
   - Open `competitor-delta-YYYY-MM-DD.md`
   - Start with the **Summary** table at the bottom — it shows each competitor's overall status at a glance (🔴/🟡/🟢)
   - For 🔴 competitors: dig into the "What Changed" table to understand the specific changes
   - For 🟢 competitors: no action needed

4. Brief your team
   - Share the delta-report in your team channel or paste the Summary table into your standup message
   - For significant changes (🔴): discuss implications for your roadmap or pricing

5. Update your snapshot after the review
   - Copy current files to `competitors/snapshot/` to reset the baseline for next week

**Expected result:**

You receive a markdown report with a per-competitor breakdown and a consolidated Summary table. The Monday brief takes 15 minutes instead of 45. Your team always has current competitive context without relying on you to remember everything.

**Why this works:** The delta format focuses attention on *what changed* rather than dumping all competitor information every week. High-significance changes (pricing, features) are surfaced first with a 🔴 flag, so you know where to focus.

---

### Scenario 3: Pre-Roadmap Competitive Snapshot

**Situation:**

You are preparing for a quarterly roadmap review. You want to share a competitive overview with the leadership team: where each competitor stands today and what's changed in the last month. You have four weeks of weekly snapshots saved and want to present a cumulative picture.

**What to do:**

1. Run the standard weekly delta for the most recent week
   - Say: "Track competitor changes" with your `competitors/` folder

2. Supplement with a narrative summary
   - After getting the delta-report, ask Claude: "Based on this delta-report and the previous three weeks, summarize the competitive trends for each competitor in 2–3 sentences."
   - Provide the last few delta-report files as context

3. Build your competitive slide
   - Use the Summary table from this week's report as your at-a-glance view
   - Use the narrative summary for each competitor as the "Key Takeaways" section of your slide

4. Flag strategic implications
   - For each 🔴 change: add a bullet noting what it means for your own roadmap or positioning

**Expected result:**

You have a clean one-page competitive brief ready for leadership: current state per competitor, what changed this quarter, and strategic implications. The whole preparation takes under 30 minutes instead of a half-day.

**Why this works:** The weekly delta-report files build up a structured history over time. You can feed several reports to Claude and ask for synthesis — turning raw notes into strategic narrative automatically.

---

## Tips

### Tip 1: Use Consistent Section Names Across All Competitor Files

The skill compares competitor files section by section. If you use `## Pricing` in one file and `## Price` in another, the diff may miss connections. Pick a standard set of sections and use them consistently:

- `## Product` — features, capabilities
- `## Pricing` — plans, tiers, prices
- `## Messaging` — tagline, positioning, homepage copy
- `## Recent News` — announcements, blog, press

**Pro tip:** Create a `competitors/_template.md` file with your standard sections and copy it whenever you add a new competitor.

### Tip 2: Keep Notes Factual and Timestamped for Better Diffs

The more specific your notes, the better the diff quality. Instead of "pricing changed," write: "Starter plan: was $39/mo, now $49/mo (April 2026)." Timestamped notes help you trace changes over time.

**Pro tip:** Add a `**Last updated:** YYYY-MM-DD` line at the top of each competitor file so you can tell at a glance when you last reviewed each one.

### Tip 3: Update Your Snapshot Immediately After Each Review

The most common mistake is forgetting to update the snapshot. If you skip a week, the next diff will show two weeks of changes bundled together, which can be harder to interpret.

**Pro tip:** Add "copy competitors/ to competitors/snapshot/" as the last step in your Monday ritual. It takes 30 seconds and ensures your next delta-report is clean and accurate.

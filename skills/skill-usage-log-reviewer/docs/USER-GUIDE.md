# Skill Usage Log Reviewer — User Guide

Learn how to audit your Claude skill collection and keep it lean.

---

## Quick Start

Here's the fastest way to audit your skills:

1. Say: "Audit my skills" and paste your list of installed skill names
2. Answer the usage questions (daily / weekly / monthly / never) for each skill
3. Get back a report with Keep / Review / Deactivate verdicts and a ready-to-use deactivation checklist

**Result:** A structured table telling you exactly which skills to remove and why.

**Time:** ~5 minutes

---

## Scenarios

### Scenario 1: Monthly Portfolio Clean-up

**Situation:**
You've been adding skills over the past two months and now have 15+ installed. Your Claude sessions feel noisy — the skill list in the sidebar is long, and you suspect half the skills you never actually trigger. You want to do a quick clean-up before starting a new project.

**What to do:**

1. Open your Claude settings and copy the list of active skill names
   - In Cowork, you can see skills in the left panel or in plugin settings
   - Just copy the names — no descriptions needed

2. Trigger the skill: "Audit my skills"
   - Paste the skill names when prompted
   - If you have quick usage notes handy, add them inline (e.g., "skill-x — never used")

3. Answer the usage questions
   - The skill will ask about your usage frequency in batches of 5–8 skills
   - Be honest — "never used" is the most useful answer here

4. Review the audit report
   - Focus on the ❌ Deactivate section first — these are safe to remove immediately
   - For ⚠️ Review items, decide if you've actually needed them in the last month

5. Deactivate the flagged skills
   - Go to Claude settings → Plugins/Skills
   - Remove each skill listed in the Deactivation Checklist

**Expected result:**

You receive a report showing exactly which skills are unused and why. The Deactivation Checklist is a ready-to-action list — you just open settings and remove each item. A typical 15-skill collection yields 4–6 deactivation candidates, reducing context load noticeably.

**Why this works:** Each installed skill adds tokens to every session via the system prompt. Removing 5 unused skills can save 500–1,500 tokens per session — which translates to faster responses and more room for actual work content.

---

### Scenario 2: Post-Plugin-Install Audit

**Situation:**
You just installed a new plugin bundle (e.g., "product-management" or "engineering") that added 8 new skills at once. You're not sure which of the new skills you'll actually use, and you don't want all 8 running indefinitely. You want to do a quick triage right after install.

**What to do:**

1. List the newly installed skills
   - After installing the plugin, note the names of the new skills added
   - Combine them with your existing skills or audit just the new batch

2. Trigger the skill: "Review my installed skills" or "Which skills should I deactivate"
   - Paste just the new skills, or the full list if you want a complete picture

3. Describe your use case for the plugin
   - Tell the skill why you installed this plugin (e.g., "I'm a PM and installed it for roadmap planning")
   - The skill will cross-reference skill purposes against your stated use case

4. Get the triage report
   - Skills aligned with your stated use case → ✅ Keep
   - Skills outside your role or workflow → ❌ Deactivate immediately

**Expected result:**

You receive a focused triage showing which of the 8 new skills fit your actual workflow. Typically 2–4 skills will be immediately relevant; the rest can be deactivated until needed.

**Why this works:** Plugin bundles are designed for broad audiences. A PM doesn't need all engineering skills, and a developer doesn't need all finance skills. Triaging after install keeps your collection role-specific from day one.

---

### Scenario 3: Quarterly Collection Review

**Situation:**
You've been using Claude for 6 months and your skill list has evolved organically. Some skills were great in Q1 but irrelevant now. You want a structured quarterly review to align your skill portfolio with your current work priorities.

**What to do:**

1. Export your full skill list
   - Go through your installed skills and list them all
   - Add a quick note on each: when you last used it (approximately)

2. Trigger the skill: "Skill usage review"
   - Provide the full list with usage notes

3. Review the duplicate detection output
   - The skill will flag any pairs with overlapping purpose (e.g., two meeting-prep skills)
   - Decide which of each pair better fits your current workflow

4. Use the Notes section of the report
   - Check collection-level observations (e.g., "You have 4 skills for meeting prep — consider keeping 1–2")
   - Use this to set a personal skill limit (e.g., max 10 active skills)

**Expected result:**

A complete quarterly snapshot of your skill portfolio — what's active, what's stale, what overlaps. The report doubles as a record of your skill portfolio health over time if you save it.

**Why this works:** Quarterly reviews prevent gradual bloat. Without a structured audit, collections tend to grow indefinitely. Setting a personal cap (e.g., 10 active skills) and reviewing quarterly keeps sessions fast and focused.

---

## Tips

### Tip 1: Be Blunt About "Never Used"

The most valuable information you can provide is honesty about skills you've never triggered. Don't keep a skill just because it sounded useful at install time. If you haven't used it in 30 days, mark it as "never used" — the skill will recommend deactivation, and you can always reinstall later.

**Pro tip:** Skills are cheap to reinstall. Deactivating a skill doesn't delete it — it just removes it from your active session context. You can add it back in 30 seconds if needed.

### Tip 2: Audit New Installs Within 2 Weeks

The best time to audit a skill is 2 weeks after installing it. By then you've had enough time to try it, but not so long that you've forgotten why you installed it. Waiting months means you'll have to dig through memory about whether you ever used a skill.

### Tip 3: Use the Report as a Skill Portfolio Log

Save the `skill-audit-report.md` file with a date in the filename (e.g., `skill-audit-2026-05.md`) and keep one per quarter. Over time, this becomes a personal log of how your skill usage evolves — useful for deciding when to add new skills and which categories you consistently use.

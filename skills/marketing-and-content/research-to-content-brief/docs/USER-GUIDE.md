# Research to Content Brief — User Guide

Learn how to turn your research notes into a structured content brief using this skill.

---

## Quick Start

Here's the fastest path to a content brief:

1. Collect your research notes into a folder (or copy-paste them)
2. Say: "Research to content brief" and provide the folder path or paste content
3. Optionally add: "for a blog post" (or landing page, social, email)
4. Receive `content-brief.md` ready to hand to a writer

**Result:** A structured brief with Audience, Core Message, Content Angles, Competitive Differentiation, Trend Hooks, and Recommended Formats.

**Time:** ~3 minutes

---

## Scenarios

### Scenario 1: Briefing a Writer After a Research Sprint

**Situation:**
You are a content marketer. Over the past week you accumulated 5 research files: notes from user interviews, competitor landing page observations, and trend snippets from industry newsletters. A writer is waiting for a brief, but you don't have time to read through all the notes manually and synthesize them.

**What to do:**

1. Collect all 5 research files into one folder
   - Files can be named anything — the skill categorizes them automatically
   - Mix of audience notes, competitor signals, and trend snippets is fine

2. Trigger the skill by saying: "Research to content brief — folder is /research/q2/"
   - Wait for the skill to read and categorize all files
   - It will extract audience pain points, competitive gaps, and trend hooks

3. Optionally narrow the output:
   - Add: "for a blog post" to get angle framing suited to long-form
   - Or "for a landing page" to get value-prop-first framing

4. Review the brief and fill any flagged sections:
   - Sections marked "NEEDS MANUAL INPUT" had no source data — add those manually
   - Content Angles will be grounded in your research, not generic advice

5. Hand the brief to your writer as the creation spec

**Expected result:**

You receive `content-brief.md` with:
- Audience section extracted from your interview notes
- Core Message synthesized from pain points + differentiation
- 2–3 Content Angles derived from real research, not made up
- Competitive Differentiation showing where competitors are silent
- Trend Hooks with source file citations

Your writer has a complete brief and doesn't need to ask you follow-up questions.

**Why this works:** Instead of manually synthesizing 5 files (30+ minutes), the skill reads and extracts everything in seconds, giving you a first-draft brief you can review and refine in 5 minutes.

---

### Scenario 2: Briefing Yourself Before Starting Content Production

**Situation:**
You are a product marketer writing content solo. You have a folder of notes from a competitive analysis you ran two weeks ago — but it's gotten stale in your head. You need a quick refresher and a content plan before you start writing the piece.

**What to do:**

1. Paste or point to your competitive analysis notes folder
   - Even a single mixed-notes file works

2. Say: "Create content brief from my notes — for social media"
   - The skill will tune angles and format recommendations for social

3. Review the Content Angles section:
   - These are the hooks you'll use for your posts
   - Each includes a rationale linked back to the research

4. Review the Competitive Differentiation section:
   - This shows what the competitors are NOT saying — your opening to own that angle

5. Use the brief as your writing guide:
   - Core Message = the thesis you keep returning to
   - Content Angles = post hooks or paragraph openers
   - Trend Hooks = timely peg for publishing now vs. later

**Expected result:**

You receive a brief that acts as your writing north star — Audience to keep in mind, Core Message to stay on topic, Angles to keep content varied, Trends to keep it timely.

**Why this works:** Two weeks after a research sprint, the key insights blur together. The brief surfaces the top signals from your notes so you write from evidence, not guesswork.

---

### Scenario 3: Synthesizing Mixed Notes Without a Clean Folder

**Situation:**
You are a freelance content strategist. Your research lives in a single messy markdown file — a mix of audience quotes, competitor observations, and trend notes all in one doc. You need a brief for a client call in 20 minutes.

**What to do:**

1. Open your mixed notes file and copy the content

2. Paste it into chat and say: "Turn my research notes into a brief"
   - The skill will auto-categorize the content by keyword heuristics
   - You'll see which parts were treated as audience notes, competitor signals, or trends

3. Review the source coverage section at the bottom of the brief:
   - Check that the categorization matches what you intended
   - If a note was miscategorized, you can re-run with explicit labels ("This section is competitor data:")

4. Use the brief for your client call:
   - Audience section = who you're targeting (confirm with client)
   - Content Angles = proposed content hooks (pitch 2–3, get feedback)
   - Competitive Differentiation = why their content will stand out

**Expected result:**

You get a rough brief in under 3 minutes — structured enough to run a productive client call, with sections flagged for any missing research so you know what to ask the client to provide.

**Why this works:** Even messy, mixed notes become a usable brief. The auto-categorization surfaces 80% of what's there, and the "NEEDS MANUAL INPUT" flags tell you exactly where the gaps are.

---

## Tips

### Tip 1: Label Your Note Types for Better Categorization

If your research files contain mixed content, add a simple label at the top of each section:
```
## Audience observations
...

## Competitor signals
...
```
This helps the skill categorize more accurately and produce a cleaner brief. Without labels, the skill uses keyword heuristics — which work, but explicit labels are faster and more reliable.

### Tip 2: Specify the Target Format for Better Angles

Adding "for a blog post" or "for a landing page" changes how the skill frames the Content Angles:
- **Blog post** → narrative hooks, problem-solution story structures
- **Landing page** → value props, objection handling, specificity
- **Social** → punchy angles, pattern interrupts, CTAs baked in
- **Email** → subject line hooks, personal framing ("You might recognize this...")

Without a format hint, you get general angles. With one, you get angles ready to write against.

### Tip 3: Use "NEEDS MANUAL INPUT" Sections as Your Research Gaps Checklist

If a section is flagged, it means your research folder doesn't cover that angle. Before briefing a writer, use that flag to decide: "Is this section important for this piece?" If yes — gather the missing research. If no — tell the writer to skip it. The flag is a feature, not a bug.

---

**Version:** 1.0.0
**Skill:** [SKILL.md](../SKILL.md) | [README.md](../README.md) | [README.ru.md](../README.ru.md)

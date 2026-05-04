# Cowork Plugin Audit — User Guide

Learn how to use Cowork Plugin Audit to clean up your plugin setup, reduce token usage, and keep your Cowork sessions lean.

---

## Quick Start

Here's the fastest way to get an audit:

1. Say: "Audit my plugins"
2. Describe your role and 2–3 main tasks in one message (e.g., "I'm a PM, I write specs and run sprint planning")
3. Paste your installed plugin list when asked
4. Get back an audit table with keep/disable recommendations

**Result:** A clear table showing which plugins to keep, which to disable, and why.

**Time:** ~3 minutes

---

## Scenarios

### Scenario 1: Cleaning Up After Installing Many Plugins

**Situation:**
You're a content marketer who just installed Claude Cowork and, during setup, added every available plugin "just in case." Three weeks in, you notice sessions feel slower and the responses sometimes reference tools you've never used. You want to slim down your setup to only the plugins relevant to your actual work: writing content, managing a content calendar, and synthesizing research.

**What to do:**

1. Trigger the skill by saying: "Cowork plugin audit" or "Which plugins should I disable"

2. Describe your workflow in one message:
   - "I'm a content marketer. I write blog posts, manage a content calendar, and synthesize research articles. I don't do sales, finance, or engineering work."

3. Paste your installed plugin list when prompted:
   - Example: `product-management, engineering, sales, data, finance, operations, skill-planner`

4. Review the audit table:
   - Focus on the **Recommendation** column — plugins marked `disable` are safe to turn off now
   - Plugins marked `disable-until-needed` can stay off until you start a project that needs them

5. Go to Cowork Settings → Plugins and disable the flagged plugins

**Expected result:**

You receive a table classifying each plugin and explaining why it does or doesn't fit your workflow. The summary tells you how many to keep, how many to remove, and estimates a moderate reduction in token usage. The optional Project Instructions block gives you ready text to paste into your project settings so removed plugins stay deactivated.

**Why this works:** By removing idle plugins, you reduce the number of skills loaded into every session context. Fewer irrelevant skills means faster, more focused responses and lower token cost per session.

---

### Scenario 2: Starting a New Project with a Different Focus

**Situation:**
You're a software engineer who mainly uses the `engineering` plugin. You've just been assigned to lead a cross-functional initiative that involves sprint planning, stakeholder updates, and risk tracking — all product management work. You want to add the `product-management` plugin temporarily and audit your full setup to ensure it matches the new project context.

**What to do:**

1. Install the `product-management` plugin in Cowork Settings

2. Trigger the skill: "Audit my plugins" or "Review my Cowork setup"

3. Describe your new workflow context:
   - "For the next 3 months I'm leading a cross-functional initiative. I'll be doing sprint planning, writing stakeholder updates, tracking risks, and reviewing metrics. I'll still do occasional code reviews but no active coding."

4. Paste your full plugin list: `engineering, product-management, data, sales, finance`

5. Review the output:
   - `product-management` → likely classified as `core` for this project
   - `engineering` → likely `contextual` (occasional code review only)
   - `sales`, `finance` → likely `idle` → `disable`

6. Copy the optional Project Instructions block into your project's instructions file

**Expected result:**

You get a project-specific audit confirming that your plugin configuration matches the new initiative. The instructions block serves as a reminder so the session doesn't accidentally activate `sales` or `finance` skills during planning sessions.

**Why this works:** Plugin context follows your project context. Auditing at project start ensures you have the right tools active — no more, no less.

---

### Scenario 3: Periodic Quarterly Review

**Situation:**
You're a freelance consultant who works across multiple client projects — marketing, operations, and product. Each project uses different plugins, and over time your "always active" list has grown to 7 plugins. You want to run a quarterly cleanup and figure out which plugins to keep globally vs. which to activate only per-project.

**What to do:**

1. Trigger the skill: "Audit my plugins"

2. Describe your overall cross-project workflow:
   - "I work on 3 types of projects: content marketing, operations optimization, and product roadmap consulting. Week to week I might switch between them. My most common tasks are writing reports, running workshops, and synthesizing research."

3. Paste your full plugin list: `product-management, operations, sales, data, engineering, finance, skill-planner`

4. Review the audit:
   - Look for plugins classified as `contextual` — these are safe candidates to disable globally and re-enable per project
   - Look for plugins classified as `idle` — these are candidates for permanent removal

5. Apply the recommendations:
   - Disable `idle` plugins permanently
   - For `contextual` plugins, note which project types need them and add a comment to your project templates

**Expected result:**

You receive a global-scope audit distinguishing your always-needed tools from project-type-specific ones. The summary helps you define a baseline "global" plugin set and a per-project checklist.

**Why this works:** Cross-project users often accumulate plugins that are only useful for one client type. The audit surfaces this pattern and gives you a structured way to manage a rotating setup instead of leaving everything always active.

---

## Tips

### Tip 1: Describe Tasks, Not Tools

When describing your workflow, focus on what you *do* (write specs, review code, track KPIs), not which tools you use. The skill maps tasks to plugins — your job is just to name the tasks accurately.

**Pro tip:** If you can't describe your tasks in 2–3 sentences, the plugin audit may be premature. Clarify your current project focus first, then run the audit.

### Tip 2: Re-run the Audit When Your Project Changes

Plugin recommendations are only valid for the workflow you described. When you start a new project or shift focus, run the audit again. A 5-minute re-audit at project start saves token waste for weeks.

### Tip 3: Use the Project Instructions Block as a Guard

If you copy the generated Project Instructions block into your project settings, Claude will avoid activating skills from disabled plugins even if a trigger phrase accidentally matches. This is especially useful for plugins like `sales` or `engineering` that have broad trigger phrases.

---

**Version:** 1.0.0 · **Last updated:** 2026-05-04

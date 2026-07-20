# Setup Wizard User Guide

Learn how to use Setup Wizard to get through a service setup without losing track of where you are.

---

## Quick Start

Here's the fastest way to run your first route:

1. Say: "help me set up example.com" — or, where slash commands are supported, `/setup-wizard https://example.com`
2. Answer the question about what you want to achieve (install / connect / configure / fix / migrate)
3. Confirm the one-line task statement the skill returns
4. Review the route map, then do one step at a time and send the requested evidence back

**Result:** The stated task is either completed and confirmed by an artifact, or you get a plain statement of what blocked it and what your options are.

**Time:** 10–40 minutes, depending on the service

---

## Scenarios

### Scenario 1: Installing a Tool You've Never Used

**Situation:**
Your team picked a new service and you need it running on your laptop today. The service's docs site has a dozen pages and you're not sure which ones apply to your OS and your plan.

**What to do:**

1. Start with the service link
   - "Help me install example-service — https://example-service.com"
   - Or, where slash commands are supported: `/setup-wizard https://example-service.com`

2. Answer the task question
   - "I want to install it from scratch on macOS and log in with my work account"

3. Give the clarifications
   - The skill asks only what it can't derive from the link — OS, version, how you plan to use it

4. Confirm the statement
   - `Task: install example-service on macOS and log in with an existing work account`
   - Say "yes" — the skill won't search the docs until you do

5. Work through the route
   - Each step gives one action and names the artifact to send
   - Send exact command output, not a description of it

**Expected result:**

A 3–5 step route ending with a verification step, then:
```
[setup-wizard] ✅ Route completed: 4/4

Task: install example-service on macOS and log in with an existing work account
Result: achieved
Confirmed by: `svc auth status` output showing the active account
Outside the route: team settings, CI integration
```

**Why this works:** The route is built from the pages that actually match your task and your OS, so you never follow a Linux instruction on a Mac or a paid-plan instruction on a free plan.

---

### Scenario 2: Fixing Something That Stopped Working

**Situation:**
An integration that worked last month now fails with an error you don't understand. You've already pasted the error into a search engine and found five contradictory forum threads.

**What to do:**

1. Start the skill with the service link and describe the failure
   - "The Slack integration on example.com stopped delivering messages, error: `webhook_not_found`"

2. Confirm the statement
   - `Task: restore message delivery from example.com to Slack, currently failing with webhook_not_found`

3. Follow the route the skill builds from the official troubleshooting pages
   - Typically: verify the current configuration → check the credential → re-create the connection → verify delivery

4. If a step fails, send the **full** error text
   - The skill triages inside that step: `Step 2, attempt 1`, `Step 2, attempt 2`…
   - The step number does not advance while the error is open

5. If three attempts fail, read the debrief
   - You get what's known, what's ruled out, and 2–3 concrete options — including contacting the service's support

**Expected result:**

Either the integration works again with an artifact proving it, or you have a precise, evidence-backed summary to hand to support — which is far faster than starting the conversation from scratch.

**Why this works:** The three-attempt ceiling stops the endless "try this too" loop. When the official path is exhausted, you get a decision to make instead of more guesses.

---

### Scenario 3: The Task Turns Out to Be Impossible on Your Plan

**Situation:**
You want to enable a feature you saw in a demo. You don't know it requires the Business tier.

**What to do:**

1. Name the task normally
   - "I want to enable SSO on example.com for my team"

2. Confirm the statement and let the skill read the docs

3. Read the stop message
   ```
   [setup-wizard] 🛑 No official documentation: SSO on the Starter plan

   SSO is documented as a Business-tier feature. Building a route is pointless
   until the plan changes. Options: upgrade the plan, restate the task
   (e.g. "set up 2FA for the team" — available on Starter), or ask sales.
   ```

4. Restate the task if you want to continue with something achievable

**Expected result:**

You find out in two minutes instead of after forty minutes of clicking through settings that don't contain the option.

**Why this works:** The skill checks preconditions — plan, permissions, dependencies — before building a route, and refuses to build one it knows will dead-end.

---

## Tips

### Tip 1: Give the Service Link, Not the Docs Link

The skill expects the service's own site as its argument and finds the relevant documentation itself, based on your confirmed task. If you paste a docs page instead, it still works, but it will confirm which service you mean first.

**Pro tip:** If the service lives in a Git repository (many developer tools do), the repository URL works just as well — official repos count as official documentation.

### Tip 2: Send Artifacts, Not Impressions

"It installed fine" does not close a step — and the skill will ask again without advancing the step number. Paste the actual command output, the full error text, or a screenshot of the window. This is what makes the final summary trustworthy: every closed step has evidence behind it.

**Pro tip:** Mask tokens, keys, and passwords before pasting. If you send one by accident, the skill will tell you and recommend revoking that key — do it immediately, chat history is not a safe place for secrets.

### Tip 3: Keep the Task Narrow

One route covers one task. "Install the CLI, set up the team, and wire it into CI" is three tasks — the skill will ask you to pick one. Narrow tasks produce short routes (2–3 steps) that you actually finish.

**Pro tip:** After finishing a route, just start another one for the next task. The service link is already known, so the second route starts faster.

---

**Version:** 1.0.0  
**Last updated:** 2026-07-20

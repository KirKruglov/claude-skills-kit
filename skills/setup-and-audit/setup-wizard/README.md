> [Версия на русском языке](README.ru.md)

# Setup Wizard

Get through any service setup one verified step at a time — no guesswork, no half-finished configuration.

---

## Overview

Setup Wizard walks you through a setup task on an external service or IT tool: installing from scratch, connecting an existing account, configuring a specific feature, fixing something that broke, upgrading, or migrating. It first asks what you actually want to achieve, confirms that statement with you, then reads the service's **official** documentation for exactly that task and builds a route with a fixed number of steps.

From there it dictates one step at a time. A step closes only when you send evidence — exact command output, the full error text, or a screenshot. Words like "seems to have worked" do not close a step. You perform every action yourself; the skill never runs commands, never edits files, and never invents steps from memory when the documentation does not cover your case.

---

## Requirements

- A link to the service or tool you want to set up (the service's own site, not a documentation page)
- A clear idea of what you want to achieve — installing, connecting, configuring, fixing, migrating
- The ability to send evidence back: copy command output, paste error text, or attach a screenshot
- Web access for the skill, so it can read the official documentation

**Note:** The skill deliberately does not run anything. It will not launch installers or checks for you and will decline requests to do so — you stay in control of every change to your machine and your account.

---

## How to Use

1. **Start with the service link**
   - Say "help me set up example.com" — or, where slash commands are supported, run `/setup-wizard https://example.com`
   - Without a link the skill will ask for one and wait

2. **Name your task**
   - Answer the open question about what you want to achieve
   - Add clarifications when asked (OS, version, how you plan to use it)

3. **Confirm the task statement**
   - The skill returns one line: `Task: <what, under which conditions>`
   - Nothing happens until you confirm it — this is the gate that keeps the route honest

4. **Review the route map**
   - You get the full list of steps and the total count N up front
   - If the route changes later, the skill announces it and shows the new map

5. **Work one step at a time**
   - Each reply gives one action, the expected result, and the artifact to send back
   - Mask tokens, keys, and passwords before sending anything

6. **Read the final summary**
   - Whether the stated task was achieved, what confirms it, and what was left outside the route

---

## Examples

### Example 1: Installing a CLI and connecting an account

**Input:** `/setup-wizard https://example-service.com` → "I want to install the CLI on macOS and log in with my existing account."

**Action:** The skill confirms the statement, finds the official install and authentication pages, and builds a 4-step route.

**Output:**
```
[setup-wizard] 🗺️ Building the route: 4 steps

Task: install the CLI on macOS and connect an existing account

1. Check the prerequisites
2. Install the CLI
3. Log in to the account
4. Verify the connection
```

Then, step by step:
```
[setup-wizard] ▶️ Running step 2/4: install the CLI

Step 2/4 — install the CLI
Action: run the install command from the official macOS instructions
Expected result: the command finishes without errors and `svc --version` prints a version
Send me: the full output of `svc --version`
```

---

### Example 2: The documentation does not cover your case

**Input:** "Help me set up example.com on Windows" — the official docs only describe Linux and macOS.

**Action:** The skill stops instead of improvising a Windows route out of blog posts.

**Output:**
```
[setup-wizard] 🛑 No official documentation: Windows installation for example.com

The official docs cover Linux and macOS only. I will not build a route from
third-party articles. Options: use WSL (if the Linux instructions apply there),
ask the service's support about Windows support, or restate the task.
```

---

### Example 3: A step that fails three times

**Input:** The login step returns an authentication error, and three attempts do not fix it.

**Action:** The skill stops the triage loop instead of looping forever.

**Output:**
```
[setup-wizard] 🛑 Stopping triage: step 3, 3 attempts

Known: the CLI is installed and reaches the server. Ruled out: wrong password,
expired local config, proxy interference.
Options:
1. Log in through the browser flow instead of the token flow
2. Roll back step 3 and re-run step 2 with the alternative install method
3. Contact the service's support with the error text from attempt 3
```

---

## Triggers

Use any of these phrases to trigger the skill:

| English | Russian |
|---------|---------|
| Set up this service | Настрой этот сервис |
| Help me install | Помоги установить |
| Walk me through the setup | Проведи по настройке |
| I can't get this tool configured | Не получается настроить инструмент |
| Guide me through connecting my account | Проведи по подключению аккаунта |
| `/setup-wizard <service-url>` | `/setup-wizard <ссылка-на-сервис>` |

---

**Version:** 1.0.0  
**Last updated:** 2026-07-20

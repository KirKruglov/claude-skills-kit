# Cowork Plugin Audit

Keep only the plugins that match your actual workflow — disable the rest to reduce token usage and noise.

---

## Overview

Cowork Plugin Audit analyzes your installed Claude Cowork plugins against your described workflow and produces a prioritized keep/disable recommendation table. It classifies each plugin as core, contextual, or idle, explains why, and estimates the potential impact on token consumption. Use this skill when you feel your Cowork sessions are getting slow or expensive, when you've recently installed several new plugins, when you're starting a project with a different focus, or when you want to periodically review and clean up your setup.

---

## Requirements

- A description of your current role and 2–3 primary tasks in Cowork (plain text)
- A list of your installed plugins (paste from Cowork Settings → Plugins)
- Optional: a project context file (`.md`) — the skill will read it automatically if present

No additional tools or skills required.

---

## How to Use

1. **Describe your workflow**
   - Prepare 2–3 sentences: your role and the main tasks you do in Cowork
   - Example: "I'm a product manager. I write specs, run sprint planning, and review metrics. I don't do coding or sales."

2. **Trigger the skill**
   - Say: "Audit my plugins" or "Cowork plugin audit"
   - Or in Russian: "Аудит плагинов" or "Какие плагины отключить"

3. **Provide your plugin list**
   - Paste the list of installed plugins when asked
   - If you're unsure of names, the skill will offer a standard reference list

4. **Review the audit table**
   - Each plugin gets a category (core / contextual / idle) and a recommendation (keep / disable / disable-until-needed)
   - The summary shows total counts and a qualitative token-savings estimate

5. **Apply the recommendations**
   - Disable suggested plugins in Cowork Settings
   - Optionally copy the generated Project Instructions block to prevent reactivation

---

## Examples

### Example 1: Product Manager Cleaning Up After Onboarding

**Input:**
```
Role: Product manager. I write feature specs, run sprint planning sessions, and review product metrics.
I don't do sales, engineering, or finance work.

Installed plugins: product-management, engineering, sales, data, finance, skill-planner
```

**Output:**
```
### Workflow Context
Product manager focused on specs, sprint planning, and metrics review.

### Audit Table

| Plugin             | Category    | Recommendation       | Rationale                                        |
|--------------------|-------------|----------------------|--------------------------------------------------|
| product-management | core        | keep                 | Specs and sprint planning are primary tasks      |
| data               | core        | keep                 | Metrics review requires data analysis skills     |
| skill-planner      | contextual  | disable-until-needed | Useful for skill research, not a daily task      |
| engineering        | idle        | disable              | No coding or code review in described workflow   |
| sales              | idle        | disable              | No sales tasks in described workflow             |
| finance            | idle        | disable              | No financial tasks in described workflow         |

### Summary
- Keep: 2 | Disable: 3 | Disable-until-needed: 1
- Estimated token impact: moderate reduction
```

---

### Example 2: Developer with Lean Setup

**Input:**
```
Role: Backend developer. I write code, debug issues, review PRs, and write technical documentation.

Installed plugins: engineering, product-management
```

**Output:**
```
### Workflow Context
Backend developer focused on coding, debugging, code review, and documentation.

### Audit Table

| Plugin             | Category   | Recommendation | Rationale                                            |
|--------------------|------------|----------------|------------------------------------------------------|
| engineering        | core       | keep           | Coding, debugging, and code review are primary tasks |
| product-management | contextual | keep           | Documentation tasks overlap with PM skills           |

### Summary
- Keep: 2 | Disable: 0 | Disable-until-needed: 0
- Estimated token impact: no changes recommended
```

---

## Triggers

Use any of these phrases to trigger the skill:

| English                          | Russian                              |
|----------------------------------|--------------------------------------|
| Audit my plugins                 | Аудит плагинов                       |
| Cowork plugin audit              | Проверь мои плагины Cowork           |
| Which plugins should I disable   | Какие плагины отключить              |
| Reduce token usage from plugins  | Снизь расход токенов на плагины      |
| Review my Cowork setup           | Проверь мою конфигурацию Cowork      |

---

📖 **[User Guide (EN)](docs/USER-GUIDE.md)** · **[Руководство (RU)](docs/USER-GUIDE.ru.md)**

**Version:** 1.0.0 · **Last updated:** 2026-05-04

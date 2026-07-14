> [Версия на русском языке](README.ru.md)

# Company Policy Drafter

Draft or update company policies in a structured, handbook-ready format — with a built-in legal review reminder and bilingual output.

---

## Overview

Company Policy Drafter creates or updates a single company policy (PTO, remote work, expenses, or AI-usage) in professional, handbook-ready language for SMB teams without in-house HR or legal staff. Every output includes a mandatory legal review flag so you never ship a policy without a compliance check. Use this skill when you need to write a new PTO or remote work policy from scratch, update an existing policy and communicate what changed to your team, or add a modern AI-usage policy to your employee handbook.

---

## Requirements

- Policy type (required): PTO / remote work / expenses / AI-usage / or describe your own
- Key parameters (optional): limits, rules, exceptions, effective date — if not provided, placeholders are inserted
- Existing policy text (optional): paste it to trigger update mode with a change-summary
- No additional tools, integrations, or external accounts needed

---

## How to Use

1. **Know what policy you need**
   - Choose a type: PTO, remote work, expenses, AI-usage, or describe a custom policy
   - Gather any specific values you want included (day limits, dollar caps, approval steps)

2. **Trigger the skill**
   - Say: "Draft a remote work policy" or "Write a PTO policy for my handbook"
   - For updates: "Update our AI-usage policy" and paste the existing text

3. **Provide your details**
   - Include any specific rules or parameters (or leave them out and fill in the placeholders later)
   - Optionally specify: language preference (EN only / RU only / both)

4. **Review your policy**
   - You'll receive a bilingual document (EN + RU) structured in five sections: Purpose, Scope, Rules, Procedure, Responsibility
   - The legal review flag is always included — consult a labor attorney before rolling out
   - In update mode, you also get a change-summary showing what changed and who to notify

---

## Examples

### Example 1: New PTO Policy from Scratch

**Input:**
```
Write a PTO policy. We give 20 days per year, requires 2 weeks' notice, no carryover.
```

**Output:**
```markdown
## PTO Policy / Политика отпусков

> ⚠️ Legal review required / Требуется юридическая проверка

### 🇬🇧 English Version

**Purpose:** Define paid time off entitlement and request procedures for all employees.

**Scope:** All full-time employees.

**Rules:**
- 20 days PTO per calendar year
- Unused days do not carry over to the next year
- PTO cannot be taken in advance of accrual

**Procedure:**
1. Submit a time-off request at least 2 weeks in advance
2. Get manager approval before booking travel

**Responsibility:** Direct managers approve requests; HR maintains records.

**Effective date:** [SPECIFY DATE]

---

### 🇷🇺 Русская версия
[... синхронизированная русскоязычная версия ...]

### Next Steps
- [ ] Fill in effective date
- [ ] Have reviewed by a legal advisor
- [ ] Distribute to all employees
```

---

### Example 2: Updating an AI-Usage Policy (Update Mode)

**Input:**
```
Update our AI-usage policy. Old policy: "Employees may not use AI tools for client work." 
New rule: AI tools are permitted for internal drafts but must not include confidential client data.
```

**Output:**
```markdown
## AI-Usage Policy / Политика использования AI

> ⚠️ Legal review required / Требуется юридическая проверка

### 🇬🇧 English Version

**Purpose:** Guide responsible use of AI tools in company workflows.

**Rules:**
- AI tools are permitted for internal drafts and non-client-facing work
- Confidential client data must never be entered into external AI tools
- All AI-generated content must be reviewed by a human before submission

[... Procedure, Responsibility, Effective date ...]

### Change Summary
- **What changed:** Permitting AI for internal drafts; adding confidentiality restriction
- **Who to notify:** All employees, especially client-facing teams
- **Notification deadline:** [SPECIFY DATE]
```

---

## Triggers

Use any of these phrases to trigger the skill:

| English | Russian |
|---------|---------|
| Draft a company policy | Напиши корпоративную политику |
| Write a PTO policy | Составь политику отпусков |
| I need a remote work policy for my handbook | Нужна политика удалённой работы для хендбука |
| Help me update our AI usage policy | Помоги обновить политику использования AI |
| Create an expenses policy | Создай политику возмещения расходов |
| Update our existing policy | Обнови существующую политику |

---

**Version:** 1.0.0  
**Last updated:** 2026-06-16

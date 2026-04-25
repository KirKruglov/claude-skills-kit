# Security Policy

## Supported Versions

Only the `main` branch is actively maintained (rolling release). No versioned releases exist.

## What Counts as a Security Issue

This repository contains Markdown skill instructions, not executable code. The following qualify as security issues:

- Prompt injections in `SKILL.md` that could cause Claude to take unintended actions
- Accidental exposure of private data in examples (emails, tokens, internal company names)
- Malicious or misleading links in documentation
- Instructions that violate [Anthropic's Usage Policies](https://www.anthropic.com/legal/usage-policy)

The following are **not** security issues — please use a regular bug report instead:

- Typos or unclear wording
- Skill logic errors or suboptimal outputs

## How to Report

**Preferred:** Use GitHub's private vulnerability reporting — go to `Security → Advisories → Report a vulnerability` in this repository. This keeps the report private until resolved.

**Alternative:** Open a thread in [GitHub Discussions](https://github.com/KirKruglov/claude-skills-kit/discussions) and mention `@KirKruglov` if confidentiality is not a concern.

## Response Time

Reports are handled on a best-effort basis. There is no guaranteed response SLA.

## Disclosure Policy

After a reported issue is resolved, a public Security Advisory will be published in this repository.

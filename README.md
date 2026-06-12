# OpenClaw Security Masterclass

> Companion repository for the **OpenClaw Security Masterclass** — lessons, copy-paste prompts, skills, and resources for running OpenClaw safely.

OpenClaw is powerful, but powerful tools are dangerous when they are wide open. This course takes you from a default, exposed setup to a hardened, well-understood one — using OpenClaw's own intelligence to harden itself, and a discipline of public-information-only workflows that never touch your sensitive systems.

> [!WARNING]
> **Never connect your personal email, calendar, bank accounts, or social media to OpenClaw.** Keep it isolated to public information sources only. See [The Golden Rules](lessons/04-the-golden-rules/README.md).

---

## Who this is for

Security professionals across roles — SOC analysts, CISOs, GRC and compliance officers, threat intelligence teams, vulnerability management, and third-party risk — who want to use OpenClaw to automate research and triage **without** putting their organisation at risk.

---

## Course outline

| # | Lesson | What you'll learn |
|---|--------|-------------------|
| 1 | [What Is OpenClaw](lessons/01-what-is-openclaw/README.md) | The agent, its building blocks, and why security matters |
| 2 | [OpenClaw Skills](lessons/02-openclaw-skills/README.md) | How skills extend the agent — with a working CVE-lookup skill |
| 3 | [Hardening Your Instance](lessons/03-hardening-your-instance/README.md) | 10 copy-paste prompts that let OpenClaw harden itself safely |
| 4 | [The Golden Rules](lessons/04-the-golden-rules/README.md) | Five non-negotiable principles for safe operation |
| 5 | [The Zapier MCP Playbook](lessons/05-zapier-mcp-playbook/README.md) | 10 public-information automation workflows |

---

## Repository layout

```
.
├── lessons/              # The written course, one folder per lesson
├── prompts/
│   ├── hardening/        # Copy-paste hardening prompts (Steps 1–10 + extras)
│   └── zapier-playbook/  # Copy-paste Zapier MCP workflow prompts (Scripts 1–10)
├── skills/
│   └── cve-lookup/       # Example SKILL.md you can install and study
└── resources/            # Curated channels, blogs, podcasts, and references
```

---

## How to use this repo

1. **Read the lessons in order** — start with [Lesson 1](lessons/01-what-is-openclaw/README.md).
2. **Harden first.** Before automating anything, work through [Lesson 3](lessons/03-hardening-your-instance/README.md) and apply the prompts in [`prompts/hardening/`](prompts/hardening/).
3. **Copy prompts, don't retype them.** Every hardening step and Zapier workflow has its own file under [`prompts/`](prompts/) so you can copy the exact text.
4. **Study the skill.** Read [`skills/cve-lookup/SKILL.md`](skills/cve-lookup/SKILL.md) before installing any skill from anyone — including this one.

---

## The one safety phrase to remember

Add this to almost any hardening prompt:

```text
Show me the proposed config diff first, and do not apply changes to exec
policy, sandboxing, MCP, sessions, or networking until I approve them.
```

---

## Disclaimer

This material is for **educational and defensive** purposes. Every workflow here uses **public information only** and creates **drafts, not sent messages**. Nothing in this course requires — or recommends — connecting OpenClaw to corporate infrastructure, SIEMs, ticketing systems, or internal networks.

*OpenClaw Security Masterclass • 2026*

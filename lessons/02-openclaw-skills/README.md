# Lesson 2 — What Are OpenClaw Skills?

Skills are how you extend OpenClaw beyond its built-in capabilities. **If OpenClaw is the brain, skills are the specialised training you give it.** A skill teaches the agent how to perform a specific type of task — consistently, repeatably, and within defined boundaries.

Without skills, OpenClaw improvises. With skills, it follows your playbook.

## Anatomy of a skill

A skill is a folder containing a `SKILL.md` file. The file has two parts:

1. **Frontmatter** (YAML) — metadata the agent uses to decide *when* and *how* to load the skill: its `name`, a `description` that tells the agent when to trigger it, a `version`, the `allowed-tools` it may use, and any binaries it `requires`.
2. **Body** (Markdown) — the actual playbook: when to use the skill, the workflow, the output format, and hard rules.

The `description` is the most important field for triggering: it is what the agent matches your request against. The `allowed-tools` list is the most important field for **security** — it is the skill's permission boundary.

## Worked example: CVE Lookup and Briefing

This skill lets you say *"Check CVE-2026-44112"* or *"What vulnerabilities were published today for Nginx?"* and get a structured analyst-ready brief with CVSS scores, exploitation status, affected versions, MITRE ATT&CK mapping, and recommended actions.

📄 The complete, installable file lives at **[`skills/cve-lookup/SKILL.md`](../../skills/cve-lookup/SKILL.md)**.

Key things to notice when you read it:

- **Scoped tools.** It only requests `web_search`, `web_fetch`, and `read_file` — no shell, no write access. A lookup skill has no business running commands.
- **A fixed output format.** Every brief looks the same, so it's easy to scan and to pipe into other workflows.
- **Anti-hallucination rules.** *"Never speculate about exploitation — report only confirmed data"* and *"If no data found, say so clearly; do not fabricate CVE details."* These rules are what make the skill trustworthy.

## The security lesson

Skills run with real capabilities. A skill you install can do anything its `allowed-tools` permit — including, in a badly-scoped skill, reading your files or running commands.

> [!CAUTION]
> The **ClawHavoc** campaign planted 1,184 malicious skills on ClawHub. **36% of all scanned ClawHub skills contain security flaws.** Read the `SKILL.md` before installing anything. If you did not write it and you have not read the code, do not install it.

This is **Golden Rule #3** — see [Lesson 4](../04-the-golden-rules/README.md).

### A checklist before you install any skill

- [ ] Open and read the entire `SKILL.md`, including frontmatter.
- [ ] Check `allowed-tools` — does a "read-only" skill ask for shell or write access?
- [ ] Look for any binaries it `requires` and understand why.
- [ ] Search the body for network calls to unfamiliar domains.
- [ ] Confirm there are anti-fabrication / confirmation rules for risky actions.
- [ ] If anything is unclear, don't install it.

---

⬅️ Previous: [Lesson 1](../01-what-is-openclaw/README.md) • ➡️ Next: [Lesson 3 — Hardening Your Instance](../03-hardening-your-instance/README.md)

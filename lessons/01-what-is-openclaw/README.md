# Lesson 1 — What Is OpenClaw

> [!NOTE]
> **Author TODO:** Drop your finished introduction to OpenClaw here. The draft below is a starting point built from concepts referenced throughout the course (skills, MCP, the gateway, `SOUL.md`, exec/sandbox policy, messaging integrations). Replace or expand it with your own product description, screenshots, and install steps.

## What it is

OpenClaw is an autonomous AI agent: you give it a goal in plain language and it plans, calls tools, and carries the task out on your behalf. It can browse the web, run commands, read and write files, manage long-running sessions, and connect to external services. That autonomy is exactly what makes it useful — and exactly what makes securing it non-optional.

## The building blocks you'll meet in this course

| Concept | What it is | Why it matters for security |
|---------|-----------|----------------------------|
| **Skills** | Reusable instructions (a `SKILL.md` file) that teach the agent a repeatable task | A malicious skill can exfiltrate data or run arbitrary commands — see [Lesson 2](../02-openclaw-skills/README.md) |
| **MCP / mcporter** | The Model Context Protocol layer that connects OpenClaw to external tools and data sources | Broad MCP access widens the blast radius of a compromise |
| **The Gateway** | The network endpoint that exposes OpenClaw | If bound to `0.0.0.0` without auth, anyone on the network can drive your agent |
| **Exec policy** | Rules governing which shell commands run, and when approval is required | Too loose = remote code execution; too strict = a deadlocked agent |
| **Sandbox** | The isolation boundary around the agent's filesystem and runtime | Limits how much damage a prompt injection or bad command can do |
| **`SOUL.md`** | The agent's standing policy/behaviour rules | Your first line of defence against prompt injection |
| **Messaging (Telegram / Discord)** | Channels you can talk to the agent through | An over-broad allowlist lets strangers issue commands |
| **Sessions & cron** | Persistent conversations and scheduled jobs | Useful for daily audits; also a persistence mechanism for attackers |

## Why this course exists

The default OpenClaw setup is, in the words of the course, *"a security nightmare."* But the same intelligence that makes it risky also makes it capable of **hardening itself** when you prompt it properly. The rest of this masterclass shows you how:

- **[Lesson 2](../02-openclaw-skills/README.md)** — extend OpenClaw with skills, and learn to vet them.
- **[Lesson 3](../03-hardening-your-instance/README.md)** — lock down your instance with 10 copy-paste prompts.
- **[Lesson 4](../04-the-golden-rules/README.md)** — the five rules you never break.
- **[Lesson 5](../05-zapier-mcp-playbook/README.md)** — put it to work with public-information-only automations.

---

➡️ Next: [Lesson 2 — What Are OpenClaw Skills?](../02-openclaw-skills/README.md)

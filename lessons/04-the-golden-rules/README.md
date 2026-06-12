# Lesson 4 — The Golden Rules

End every lesson — and every working session — with these non-negotiable principles.

> [!WARNING]
> **NEVER connect your personal email, calendar, bank accounts, or social media to OpenClaw.** Keep it isolated to public information sources only.

---

## Rule 1 — Start locked down, open up as needed

The default approach is to **deny everything** and grant permissions only when you need them for a specific task. Don't pre-approve access you might need someday. Approve it when you actually need it, and revoke it when you're done.

## Rule 2 — Use the strongest model available

Weaker and cheaper models are significantly **more vulnerable to prompt injection** attacks. Frontier-class models (e.g. Claude Opus/Sonnet, GPT-4o, GPT-5) are generally more resistant. **This is not the place to save money on API costs.**

## Rule 3 — Never install unvetted skills

The **ClawHavoc** campaign planted **1,184 malicious skills** on ClawHub. **36% of all scanned ClawHub skills contain security flaws.** Read the `SKILL.md` file before installing anything. **If you did not write it and you have not read the code, do not install it.** (See [Lesson 2](../02-openclaw-skills/README.md).)

## Rule 4 — Audit daily

Run `openclaw security audit --deep` **every single day.** Set it up as a cron job so it happens automatically. Security is not a one-time setup — it is a continuous process.

## Rule 5 — Dedicated machine, dedicated user

Run OpenClaw on a **dedicated machine or VM** — not on your primary workstation. Run it as a **standard user, never as root or admin.** If it gets compromised, the blast radius is limited to that machine and that user account.

---

> *"There is no perfectly secure setup. But there is a massive difference between being wide open and being hardened. These 10 steps get you from one to the other."*

---

⬅️ Previous: [Lesson 3](../03-hardening-your-instance/README.md) • ➡️ Next: [Lesson 5 — The Zapier MCP Playbook](../05-zapier-mcp-playbook/README.md)

# Lesson 3 — Hardening Your Instance

> *"OpenClaw is a security nightmare. But if you prompt it properly, it is intelligent enough to harden itself."*

## Before you begin

This lesson walks you through **10 steps to lock down your OpenClaw instance**. The approach is unique: you are **not** going to open a terminal and type commands manually. Instead you paste structured prompts directly into OpenClaw and let the agent harden itself. Each step has an exact prompt to copy, an explanation of what it does, and what to watch for.

> [!IMPORTANT]
> **This will not make OpenClaw bulletproof — nothing will.** But it will take you from being wide open to having significantly more security than you get by default. That difference is the difference between being an easy target and a hard one.

## The philosophy: harden without kneecapping

Naïve hardening — "lock everything down" — produces an agent that can't function: deny-by-default exec, `ask=always` everywhere, sandboxes that break MCP. The prompts in this lesson are deliberately written to **preserve normal operation** while removing the dangerous defaults. They tell the agent what *not* to break (MCP, mcporter, elevated mode, required state/config access) as explicitly as what to secure.

## The biggest rule

The single safest phrase you can add to almost any hardening prompt:

```text
Show me the proposed config diff first, and do not apply changes to exec
policy, sandboxing, MCP, sessions, or networking until I approve them.
```

Make the agent show its work before it changes anything load-bearing.

## The 10 steps

Each step has a ready-to-copy prompt file in [`prompts/hardening/`](../../prompts/hardening/).

| Step | Focus | Prompt |
|------|-------|--------|
| 1 | Audit first — find issues before fixing | [`01-audit-first.md`](../../prompts/hardening/01-audit-first.md) |
| 2 | Apply safe fixes — keep the system usable | [`02-apply-safe-fixes.md`](../../prompts/hardening/02-apply-safe-fixes.md) |
| 3 | Secure messaging — Telegram / Discord allowlists | [`03-secure-messaging.md`](../../prompts/hardening/03-secure-messaging.md) |
| 4 | Lock down the gateway — binding + token auth | [`04-lock-down-gateway.md`](../../prompts/hardening/04-lock-down-gateway.md) |
| 5 | Safer exec policy — approvals without deadlock | [`05-safer-exec-policy.md`](../../prompts/hardening/05-safer-exec-policy.md) |
| 6 | Safer tool policy — targeted, not blanket | [`06-safer-tool-policy.md`](../../prompts/hardening/06-safer-tool-policy.md) |
| 7 | Prompt-injection hardening — `SOUL.md` rules | [`07-prompt-injection-hardening.md`](../../prompts/hardening/07-prompt-injection-hardening.md) |
| 8 | Safer sandboxing — limit blast radius | [`08-safer-sandboxing.md`](../../prompts/hardening/08-safer-sandboxing.md) |
| 9 | Browser & profile isolation | [`09-browser-profile-isolation.md`](../../prompts/hardening/09-browser-profile-isolation.md) |
| 10 | Final safe hardening pass | [`10-final-hardening-pass.md`](../../prompts/hardening/10-final-hardening-pass.md) |

Two extras:

- **[One-prompt version](../../prompts/hardening/one-prompt-version.md)** — the whole pass in a single prompt, for when you want it fast.
- **[The golden safety phrase](../../prompts/hardening/golden-safety-phrase.md)** — the one line to staple onto anything.

## What "safe" means here — the guardrails baked into every prompt

These prompts deliberately instruct the agent **NOT** to:

- set exec to deny-by-default
- set `ask=always` globally
- disable elevated mode
- switch to message-only mode
- deny `fs` / `runtime` / `automation` / `session` tools wholesale
- set workspace access to `none`
- block MCP or mcporter

…and **TO** preserve MCP/mcporter access, normal CLI/admin commands, sessions, gateway management, cron, diagnostics, and required state/config filesystem access.

## How to run the lesson

1. Start at **Step 1** and actually read the audit output before doing anything else.
2. Work the steps in order — each builds on the last.
3. At every step that touches exec, sandbox, MCP, sessions, or networking, **make the agent show the diff and wait for your approval.**
4. Finish with **Step 10**, then re-run the audit to confirm.

---

⬅️ Previous: [Lesson 2](../02-openclaw-skills/README.md) • ➡️ Next: [Lesson 4 — The Golden Rules](../04-the-golden-rules/README.md)

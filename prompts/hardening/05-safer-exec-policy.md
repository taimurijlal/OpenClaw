# Step 5 — Safer Exec Policy

**What it does:** Hardens command-execution approvals so risky commands still prompt, while normal OpenClaw and mcporter admin keeps working — no deadlocks.

```text
Review my exec approval policy and harden it without breaking normal OpenClaw administration.

Goals:
- Keep approval prompts for clearly risky commands
- Allow normal safe admin commands needed for OpenClaw and mcporter to function
- Keep fallback usable rather than deadlocking the agent
- Preserve access to mcporter, MCP inspection, gateway management, and basic diagnostics

Do not set:
- deny-by-default for all exec
- ask=always for everything
- askFallback=deny unless absolutely necessary
- security=allowlist unless you also include the normal OpenClaw and mcporter admin commands I use

Show me the proposed exec policy and approvals file before applying it.
```

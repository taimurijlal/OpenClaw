# Step 6 — Safer Tool Policy

**What it does:** Tightens the tool policy with targeted restrictions instead of blanket denies, keeping MCP, mcporter, sessions, gateway admin, and cron available.

```text
Review my tool policy and make it more secure while preserving normal operation.

Requirements:
- Keep filesystem access limited where reasonable, but do not block required OpenClaw state/config access
- Keep MCP, mcporter, sessions, gateway admin, and cron available unless there is a specific reason to restrict them
- Do not switch to message-only mode
- Do not disable elevated mode
- Do not deny runtime, fs, automation, or sessions wholesale

Prefer targeted restrictions over blanket denies.
Show me all proposed config changes before applying them.
```

# Step 2 — Apply Safe Fixes

**What it does:** Fixes the audit findings while keeping the system usable — least-restrictive secure fixes, nothing that deadlocks the agent.

```text
Please fix the audit findings, but keep the system usable.

Rules:
- Do not set exec to deny-by-default
- Do not disable elevated mode
- Do not set workspace access to none
- Do not block MCP, mcporter, gateway, sessions, or cron unless I explicitly ask
- Prefer the least restrictive secure fix that preserves normal OpenClaw operation

Show me each config change before applying it if it affects tools, sandboxing, approvals, or networking.
```

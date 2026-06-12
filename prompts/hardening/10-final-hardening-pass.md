# Step 10 — Final Safe Hardening Pass

**What it does:** A full hardening sweep across every area — permissions, gateway, messaging, `SOUL.md`, browser isolation, exec policy, and sandbox — while preserving day-to-day usability. Finish here, then re-run the audit from Step 1.

```text
Run a full security hardening pass, but preserve day-to-day usability.

Please review and improve:
1. file permissions on OpenClaw config files
2. gateway binding and token auth
3. messaging allowlists and pairing
4. SOUL.md safety rules for credentials, destructive commands, sudo, and prompt injection
5. browser/profile isolation if relevant
6. a reasonable exec approval policy that still allows OpenClaw and mcporter administration
7. sandbox settings only if they do not break MCP, mcporter, sessions, gateway admin, or state/config access
8. final audit and summary

Constraints:
- Do not set exec to deny-by-default
- Do not set ask=always globally
- Do not disable elevated mode
- Do not switch to message-only
- Do not deny fs/runtime/automation/session tools wholesale
- Do not set workspace access to none
- Do not block MCP or mcporter

Show me proposed config changes before applying anything that affects exec policy, sandboxing, MCP, sessions, or networking.
```

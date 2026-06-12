# One-Prompt Version

**What it does:** The entire hardening pass condensed into a single prompt — for when you want the whole thing fast. Still preserves normal admin usability and still asks for approval before load-bearing changes.

```text
Please harden my OpenClaw setup, but keep it fully usable for normal admin tasks.

Secure:
- gateway binding and auth
- config file permissions
- messaging allowlists
- prompt-injection resistance
- browser/profile isolation where relevant

Preserve:
- MCP and mcporter access
- normal OpenClaw CLI/admin commands
- sessions, gateway management, cron, and diagnostics
- elevated mode
- required state/config filesystem access

Do not:
- set exec deny-by-default
- set ask=always globally
- disable elevated mode
- switch to message-only
- deny fs/runtime/automation/session tools wholesale
- set workspace access to none

Show me all proposed changes before applying any exec-policy, sandbox, MCP, or networking changes.
```

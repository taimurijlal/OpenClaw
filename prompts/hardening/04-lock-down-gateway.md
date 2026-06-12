# Step 4 — Lock Down the Gateway

**What it does:** Verifies the gateway isn't publicly exposed — binds it to localhost, enables token auth, and keeps the token out of plaintext where practical.

```text
Check my gateway configuration.

Please verify:
1. Whether it is bound to 127.0.0.1 or 0.0.0.0
2. Whether token auth is enabled
3. Whether it appears publicly exposed

If needed, fix it by:
- binding to 127.0.0.1
- enabling token auth
- storing the token outside plaintext config where practical

Do not change exec approvals, sandbox mode, or MCP settings as part of this task.
Show me the exact changes before restart.
```

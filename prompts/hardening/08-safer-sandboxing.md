# Step 8 — Safer Sandboxing

**What it does:** Recommends the safest sandbox that still lets OpenClaw operate — a moderate sandbox that limits blast radius without making the agent unusable.

```text
Review sandbox settings and recommend the safest configuration that still allows normal OpenClaw operation.

Rules:
- Do not set workspace access to none unless you first prove the agent can still access required OpenClaw state and config
- Do not enforce a sandbox mode that breaks mcporter, MCP, or normal diagnostics
- Prefer a moderate sandbox that limits blast radius without making the agent unusable

Show me the recommendation first, explain tradeoffs, and wait for approval before applying it.
```

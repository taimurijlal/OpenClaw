# The Golden Safety Phrase

The single safest phrase you can add to almost **any** hardening prompt. Staple it onto anything that might touch load-bearing settings.

```text
Show me the proposed config diff first, and do not apply changes to exec policy, sandboxing, MCP, sessions, or networking until I approve them.
```

**Why it works:** it forces the agent to surface its intended changes as a reviewable diff *before* acting, so you stay in the loop on exactly the settings that can break — or unlock — your instance.

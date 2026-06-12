# Script 10 — The Complete Morning Pipeline

**Audience:** SOC leads, CISOs, security managers • **Cadence:** Daily at 07:00

> *"70 minutes of manual morning triage, replaced by a 10-minute review. Every day. No corporate system connections needed."*

Runs 4 public-information checks in sequence and delivers a unified morning briefing via Slack and Google Docs. No corporate systems touched.

**Zapier actions to enable:**
- YouTube: Find Video
- Slack: Send Channel Message
- Google Docs: Create Document from Text
- Gmail: Create Draft Email

```text
Run my complete morning security pipeline.

Execute ALL of the following in sequence:

=== PHASE 1: THREAT INTELLIGENCE ===
Search the web for cybersecurity news from the last
24 hours. Find: new CVEs (CVSS >= 7), CISA KEV
additions, active campaigns, major breaches, and
critical vendor patches from Microsoft, Google, AWS,
Fortinet, Palo Alto, CrowdStrike, Cisco.
Categorise as Critical / High / Notable.

=== PHASE 2: EXPLOIT INTELLIGENCE ===
Check for new CISA KEV entries. Search for newly
published proof-of-concept exploits. Check if any
actively exploited CVEs affect common enterprise
tech: Windows, Exchange, Fortinet, Cisco, Chrome,
VMware, Kubernetes.

=== PHASE 3: YOUTUBE RESEARCH ===
Search YouTube for new security videos uploaded in
the last 24 hours from: John Hammond, NetworkChuck,
LiveOverflow, IppSec, SANS, DEF CON, 13Cubed,
The Cyber Mentor. Classify as Must Watch / Worth
Watching / Archive.

=== PHASE 4: INDUSTRY CONTEXT ===
Search for any major data breaches or ransomware
incidents disclosed in the last 24 hours. Identify
the sector, attack vector, and scale.

=== PHASE 5: COMPILE AND DISTRIBUTE ===
Compile ALL findings into a single morning briefing:

# Security Morning Briefing — [TODAY]
## Threat Landscape
[Critical and high items from Phase 1]
## Exploit Intelligence
[KEV additions and new PoCs from Phase 2]
## New Research
[Top 3 YouTube videos from Phase 3]
## Breach Watch
[New breaches from Phase 4, or "no new breaches"]
## Today's Action Items
[Prioritised list of what needs attention]

Save as Google Doc: "Morning Brief — [DATE]"
Post summary to Slack #security-daily.
Draft Gmail to [YOUR-EMAIL] with link to Doc.
DO NOT SEND the email — draft only.
```

---

## What this replaces

Without this script: check email (10 min), check CISA (5 min), scan security news (15 min), check YouTube (10 min), check breach trackers (10 min), search for new PoCs (10 min), draft team update (15 min). **Total: 75 minutes.** With this script: paste the prompt, review the output, approve the Slack post. **Total: 10 minutes.** 65 minutes per day → 5.4 hours per week → **23 hours per month** returned to higher-value work.

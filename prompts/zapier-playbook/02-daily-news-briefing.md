# Script 2 — Daily Cybersecurity News Briefing

**Audience:** SOC leads, CISOs, security managers • **Cadence:** Daily at 07:00

Searches the web for the latest cybersecurity news, summarises the top stories, saves a briefing to Google Docs, and distributes via draft email and Slack.

**Zapier actions to enable:**
- Gmail: Create Draft Email
- Google Docs: Create Document from Text
- Slack: Send Channel Message

```text
Generate my daily cybersecurity morning briefing.

TASKS:
1. Search the web for cybersecurity news from the last
24 hours. Focus on:
- New CVE disclosures with CVSS >= 7.0
- CISA advisories or KEV additions
- Active ransomware campaigns or APT activity
- Major data breaches or incidents
- Vendor security patches (Microsoft, Google, AWS, Fortinet, Palo Alto, CrowdStrike)
- Regulatory or compliance updates

2. Categorise findings as:
CRITICAL — Active exploitation or major breach
HIGH — New high-severity CVE with PoC available
NOTABLE — Industry trends, research, advisories

3. Write a structured briefing (under 500 words) with:
- Executive summary (3 sentences)
- Critical items (if any)
- High items
- Notable items
- Source links for each item

4. Draft a Gmail to [SECURITY-TEAM@COMPANY.COM]
with subject "Daily Security Briefing — [DATE]"
containing the briefing. DO NOT SEND — draft only.

5. Post a short summary (3–5 bullet points) to
the Slack channel #security-daily.
```

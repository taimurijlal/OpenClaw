# Script 6 — Ransomware and Threat Actor Tracker

**Audience:** Threat intelligence, SOC analysts, CISOs • **Cadence:** Weekly

Searches public sources for ransomware gang activity, APT campaign disclosures, and threat actor TTPs. Delivers a structured intelligence summary to Slack.

**Zapier actions to enable:**
- Slack: Send Channel Message
- Google Docs: Create Document from Text

```text
Generate a weekly ransomware and threat actor report.

TASKS:
1. Search the web for ransomware activity in the last
7 days. Look for:
- New victims claimed by ransomware groups
- New ransomware variants or rebrands
- Law enforcement takedowns or arrests
- Ransomware-as-a-Service (RaaS) changes
- Decryptors released
Focus on groups: LockBit, BlackCat/ALPHV, Cl0p,
Play, 8Base, Akira, Medusa, Black Basta, Royal,
Rhysida and any newly emerged groups.

2. Search for APT campaign disclosures from:
- Security vendor blogs (Mandiant, CrowdStrike,
Microsoft Threat Intelligence, Recorded Future,
SentinelOne, Kaspersky, ESET)
- CISA / NSA / NCSC joint advisories
- Academic or independent researcher reports

3. For each finding, include:
- Threat actor / group name
- Activity summary (2–3 sentences)
- Targeted industries or regions
- Notable TTPs or tools used
- IOCs if publicly available
- Source URL

4. Save the full report as Google Doc:
"Threat Actor Report — Week of [DATE]"

5. Post a summary to Slack #threat-intel:
"🔍 Weekly Threat Actor Roundup — [DATE RANGE]"
- Ransomware: [X] new campaigns / [X] victims
- APT: [X] new disclosures
- Top concern: [most significant finding]
- Full report: [Google Doc link]
```

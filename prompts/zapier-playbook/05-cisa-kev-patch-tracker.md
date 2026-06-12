# Script 5 — CISA KEV and Patch Tuesday Tracker

**Audience:** Vulnerability management, all security roles • **Cadence:** Daily + monthly (Patch Tuesday)

Monitors CISA's Known Exploited Vulnerabilities catalogue and major vendor patch releases. Posts actionable alerts to Slack so your team knows what's being actively exploited right now.

**Zapier actions to enable:**
- Slack: Send Channel Message
- Google Sheets: Create Spreadsheet Row (optional — for tracking)

```text
Run my daily CISA KEV and patch intelligence check.

TASKS:
1. Search for any new additions to the CISA Known
Exploited Vulnerabilities (KEV) catalogue in the
last 24 hours. For each new entry report:
- CVE ID
- Vendor / Product
- Vulnerability description
- CISA remediation deadline
- Whether a patch is available

2. Check for new security patches or advisories from:
- Microsoft (especially on Patch Tuesday weeks)
- Google Chrome / Android
- Apple (iOS, macOS)
- Fortinet / Palo Alto / Cisco
- VMware / Broadcom
- Linux kernel advisories
Focus on anything rated Critical or being actively exploited.

3. Search for new publicly available exploit code
(PoC) for any CVE published in the last 7 days.

4. Post to Slack #security-vulns in this format:
"🛡️ Vulnerability Intelligence — [DATE]"
"🔴 CISA KEV Additions (actively exploited):"
[List each with CVE, product, deadline]
"🟠 New Critical Patches Available:"
[List each with vendor, advisory, severity]
"⚠️ New Public PoC Exploits:"
[List any new PoCs with CVE and target]
If nothing in a category, note "✅ None today."

5. If any CISA KEV additions affect common enterprise
technologies (Windows, Exchange, Fortinet, Cisco,
Chrome, VMware), add "🚨 ACTION REQUIRED" at the
top of the Slack message.
```

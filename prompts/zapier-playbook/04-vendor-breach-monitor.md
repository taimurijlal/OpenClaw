# Script 4 — Vendor Security Breach Monitor

**Audience:** GRC, third-party risk management • **Cadence:** Daily

Monitors public news for data breaches or security incidents affecting your key vendors and suppliers, then alerts you via Slack.

**Zapier actions to enable:**
- Google Sheets: All readonly only
- Slack: Send Direct Message or Send Channel Message
- Gmail: Create Draft Email

```text
Run a vendor security check against our vendor list.

1. Read the Google Sheet "[Critical Vendors]" which
has columns: Vendor Name, Service Provided,
Data Classification, Contract Renewal Date.

2. For EACH vendor, search the web for:
- "[Vendor Name] data breach 2026"
- "[Vendor Name] security incident"
- "[Vendor Name] CVE vulnerability"
- "[Vendor Name] ransomware"

3. If you find ANY security incidents from the last
30 days, create an alert with: vendor name,
incident summary, source URL, data classification,
recommended action.

4. If incidents found: post to Slack #grc-team with
full details and draft a Gmail to the vendor's
contact requesting a status update. DO NOT SEND.

5. If no incidents: post to Slack #grc-team:
"✅ Vendor check complete — no incidents found
for [X] vendors. Next check: tomorrow."
```

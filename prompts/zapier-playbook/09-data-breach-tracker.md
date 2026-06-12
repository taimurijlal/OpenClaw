# Script 9 — Public Data Breach Tracker

**Audience:** CISOs, GRC, security awareness • **Cadence:** Weekly

Tracks publicly disclosed data breaches, analyses patterns, and delivers a breach landscape summary. Invaluable for CISOs who need industry context for board briefings and risk assessments.

**Zapier actions to enable:**
- Slack: Send Channel Message
- Google Sheets: Create Spreadsheet Row
- Google Docs: Create Document from Text

```text
Generate the weekly data breach intelligence report.

TASKS:
1. Search the web for data breaches publicly disclosed
in the last 7 days. Search for:
- "data breach 2026 this week"
- "data breach notification"
- "records exposed 2026"
- "ransomware victim"
- HaveIBeenPwned new breaches

2. For each breach found, record:
- Organisation name
- Industry sector
- Type of breach (ransomware, misconfiguration, insider threat, phishing, supply chain, etc.)
- Records affected (number if known)
- Data types exposed (PII, financial, health, credentials, etc.)
- Root cause (if disclosed)
- Source URL

3. Log each breach to Google Sheet
"[Breach Intelligence Log]"

4. Write a brief analysis (200 words) covering:
- Total breaches this week
- Most affected industry
- Most common attack vector
- Trend vs previous weeks (increasing/decreasing)
- One key lesson for our security programme

5. Save analysis as Google Doc:
"Breach Intelligence — Week of [DATE]"

6. Post to Slack #security-daily:
"📊 Breach Intelligence — [DATE RANGE]"
"[X] breaches disclosed this week"
"Top sector: [industry] | Top vector: [type]"
"Largest: [org name] — [X] records"
"Full report: [Google Doc link]"
```

# Script 1 — YouTube Security Research Monitor

**Audience:** All security roles • **Cadence:** Daily

Searches YouTube for the latest uploads from top cybersecurity channels and delivers a curated digest directly to Slack. No spreadsheet needed — fast, clean, daily.

**Zapier actions to enable:**
- YouTube: Find Video (search by keyword or channel)
- Slack: Send Channel Message

```text
Do a YouTube security research roundup for today.

Search YouTube for videos uploaded in the last
24 hours from these channels and topics:

CHANNELS:
- John Hammond
- NetworkChuck
- LiveOverflow
- IppSec
- David Bombal
- The Cyber Mentor
- SANS Institute
- Black Hat / DEF CON
- 13Cubed (DFIR)
- Professor Messer

ALSO SEARCH KEYWORDS:
- "cybersecurity news today"
- "CVE 2026 exploit"
- "zero day"
- "ransomware attack 2026"
- "red team tutorial"
- "DFIR walkthrough"
- "bug bounty"

For each video found, classify as:
- MUST WATCH: active exploitation, zero-days, critical CVEs, major breach analysis
- WORTH WATCHING: tutorials, walkthroughs, tools
- ARCHIVE: general awareness, beginner content

Post to Slack #security-research in this format:
"🎬 Security Research Roundup — [TODAY'S DATE]"
"[X] new videos found"
"🔴 MUST WATCH:"
"[Title] — [Channel] — [URL]"
"[1-sentence summary of why it matters]"
"🟡 WORTH WATCHING:"
"[Title] — [Channel] — [URL]"

If nothing new today, post:
"✅ No new critical security videos today."
```

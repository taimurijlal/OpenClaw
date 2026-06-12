# Script 3 — GRC Compliance Deadline Tracker

**Audience:** GRC professionals, compliance officers • **Cadence:** Weekly

Reviews your compliance deadlines spreadsheet, checks which ones are approaching, and alerts the GRC team via Slack.

**Zapier actions to enable:**
- Google Sheets: Lookup Spreadsheet Rows (read deadlines)
- Google Calendar: Create Detailed Event
- Slack: Send Channel Message
- Gmail: Create Draft Email

```text
Run our weekly GRC compliance check.

1. Read the Google Sheet "[Compliance Tracker]" which
has columns: Framework, Control ID, Activity,
Due Date, Owner, Status, Last Completed.

2. Identify all compliance activities that are:
- Due within the next 14 days (URGENT)
- Due within the next 30 days (UPCOMING)
- Overdue (due date passed, status != Complete)

3. For each URGENT item, create a Google Calendar
event 3 business days before the due date with:
- Title: "[FRAMEWORK] — [ACTIVITY] Due [DATE]"
- Description: Control ID, owner, what's needed
- Set a 1-day-before reminder

4. For any OVERDUE items, draft a Gmail to the owner
with a polite reminder. DO NOT SEND.

5. Post a summary to Slack #grc-team:
"📋 Weekly Compliance Status"
- X items overdue (list them)
- X items due in 14 days
- X items due in 30 days
- Next audit: [date and framework]
```

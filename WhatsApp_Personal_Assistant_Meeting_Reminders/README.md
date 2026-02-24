# WhatsApp Personal Assistant Meeting Reminders

**Status:** 🔴 Inactive  
**Node Count:** 61  
**Connection Ratio:** 98%  
**Workflow ID:** `45EAcPCy6dUpK2B6`

## Description
Full WhatsApp PA: schedules meeting reminders every 5 minutes, handles inbound intents (search, insert, meeting check), logs messages to DB, and manages contact records.

## Flow Diagram
See `FLOW_DIAGRAM.png`

## Process Steps
1. **Schedule Trigger (5 min)** – Poll for upcoming meetings
2. **Find Upcoming Meetings (Postgres)** – Query meetings within reminder window
3. **Any Meetings to Remind?** – Branch: yes/no
4. **Format Reminder Messages** – Build WhatsApp message text
5. **Has Scheduler Phone?** – Route to scheduler vs contact
6. **Send Reminder via WhatsApp** – Deliver reminder to both parties
7. **Mark Reminder as Sent (DB)** – Update reminder status
8. **Check Intent (AI)** – Classify: search / insert / schedule
9. **Supabase / Postgres** – DB read/write for contacts & meetings

## Key Node Types
- `openAi`
- `scheduleTrigger`
- `noOp`
- `webhook`
- `memoryBufferWindow`
- `switch`
- `toolCode`
- `supabase`
- `executeWorkflow`
- `lmChatOpenAi`
- `code`
- `respondToWebhook`

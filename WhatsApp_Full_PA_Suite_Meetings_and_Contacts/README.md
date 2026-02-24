# WhatsApp Full PA Suite Meetings and Contacts

**Status:** 🔴 Inactive  
**Node Count:** 83  
**Connection Ratio:** 99%  
**Workflow ID:** `TPFWUeCTVdPyRbpg`

## Description
Comprehensive Personal Assistant over WhatsApp: meeting reminders, contact search/insert, thread reply logging, and inbound message classification — all in one workflow.

## Flow Diagram
See `FLOW_DIAGRAM.png`

## Process Steps
1. **Schedule Trigger / Webhook** – Periodic check or inbound message
2. **Find Upcoming Meetings (Postgres)** – Check reminder queue
3. **Format & Send Reminder** – WhatsApp to scheduler and contact
4. **Check Intent** – Classify: search / insert / meeting / reply
5. **Insert or Search Contact (Supabase)** – Handle contact requests
6. **Process Reply / Log Thread** – Handle message thread replies
7. **Respond Success via Webhook** – Acknowledge completion

## Key Node Types
- `openAi`
- `scheduleTrigger`
- `noOp`
- `webhook`
- `toolCode`
- `switch`
- `supabase`
- `memoryBufferWindow`
- `executeWorkflow`
- `lmChatOpenAi`
- `code`
- `respondToWebhook`

# Email and Meeting Prioritization Agent

**Status:** 🔴 Inactive  
**Node Count:** 141  
**Connection Ratio:** 97%  
**Workflow ID:** `IYVeT7Sl8a2giPES`

## Description
Combined AI agent: prioritizes emails and manages meeting reminders. Runs on schedule, classifies intents (email reply / meeting reminder / contact search), routes to sub-workflows.

## Flow Diagram
See `FLOW_DIAGRAM.png`

## Process Steps
1. **Schedule Trigger (5 min)** – Periodic run
2. **Find Upcoming Meetings** – Query Postgres for reminders due
3. **Any Meetings to Remind?** – Branch based on count
4. **Send Reminder (WhatsApp)** – Message scheduler & contact
5. **Execute Workflow Trigger** – Also handles inbound WhatsApp
6. **Check Intent (AI)** – Email / Search / Insert / Meeting
7. **Search / Insert Contact (DB)** – Fulfil database request
8. **Respond Success** – Return result via webhook

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
- `outputParserStructured`
- `code`

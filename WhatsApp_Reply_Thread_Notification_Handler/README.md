# WhatsApp Reply Thread Notification Handler

**Status:** 🔴 Inactive  
**Node Count:** 17  
**Connection Ratio:** 100%  
**Workflow ID:** `GJ017uIt02A9iuQ7`

## Description
Sub-workflow that processes WhatsApp thread replies: marks threads as replied in Postgres, formats dual notifications, sends WhatsApp messages, and logs replies.

## Flow Diagram
See `FLOW_DIAGRAM.png`

## Process Steps
1. **Execute Workflow Trigger** – Called by parent workflow
2. **Process Reply (Code)** – Extract reply data and metadata
3. **Mark Thread as Replied (Postgres)** – Update thread status in DB
4. **Format Notification Messages** – Build WhatsApp text for user & sender
5. **Send Notification to User** – HTTP → WhatsApp API
6. **Send Confirmation to Sender** – HTTP → WhatsApp API
7. **Log Reply to Message Log (Postgres)** – Persist reply record

## Key Node Types
- `code`
- `executeWorkflowTrigger`
- `postgres`
- `httpRequest`

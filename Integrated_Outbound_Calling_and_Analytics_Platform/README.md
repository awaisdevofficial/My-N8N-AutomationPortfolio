# Integrated Outbound Calling and Analytics Platform

**Status:** 🟢 Active  
**Node Count:** 247  
**Connection Ratio:** 97%  
**Workflow ID:** `V9HqnohZieKgp3kJ`

## Description
Integrated calling platform: orchestrates outbound calls, tracks status via polling, analyzes outcomes with OpenAI, and logs results to Supabase and Google Sheets.

## Flow Diagram
See `FLOW_DIAGRAM.png`

## Process Steps
1. **Webhook / Manual Trigger** – Initiate call campaign
2. **Get Row(s) (Google Sheets)** – Load call list
3. **HTTP Request (VAPI)** – Initiate call
4. **Store Call Details (Supabase)** – Save call record
5. **Wait 60 Seconds + Poll Status** – Check call completion
6. **OpenAI – Analyze Outcome** – Classify result
7. **Update Sheets + Supabase** – Sync results
8. **Respond to Webhook** – Return status

## Key Node Types
- `openAi`
- `googleSheets`
- `splitInBatches`
- `stickyNote`
- `code`
- `respondToWebhook`
- `httpRequest`
- `merge`
- `noOp`
- `scheduleTrigger`
- `set`
- `manualTrigger`

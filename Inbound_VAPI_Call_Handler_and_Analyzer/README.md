# Inbound VAPI Call Handler and Analyzer

**Status:** 🟢 Active  
**Node Count:** 93  
**Connection Ratio:** 96%  
**Workflow ID:** `BDqG5mWtcsDL6Pns`

## Description
Handles inbound VAPI voice calls: creates SIP trunk credentials, provisions inbound agents, waits for call completion, analyzes call summary with AI, and updates database records.

## Flow Diagram
See `FLOW_DIAGRAM.png`

## Process Steps
1. **Webhook / Manual Trigger** – Receive inbound call event
2. **Set SIP Credentials** – Configure SIP trunk parameters
3. **Create SIP Trunk + Inbound Agent** – Provision VAPI agent via API
4. **Wait 60 Seconds** – Poll for call completion
5. **Check Call Status (VAPI API)** – Has call ended?
6. **Analyze Call Summary (OpenAI)** – AI: outcome / sentiment / action
7. **Update Row (Supabase)** – Store call result and notes

## Key Node Types
- `openAi`
- `stickyNote`
- `code`
- `manualTrigger`
- `httpRequest`
- `supabase`
- `merge`
- `set`
- `webhook`
- `if`
- `switch`
- `wait`

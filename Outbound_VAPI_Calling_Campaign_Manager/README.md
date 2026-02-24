# Outbound VAPI Calling Campaign Manager

**Status:** 🟢 Active  
**Node Count:** 316  
**Connection Ratio:** 97%  
**Workflow ID:** `dwz8CA6JqCA7lWjT`

## Description
Large outbound calling campaign manager: fetches customer batches from Supabase, initiates VAPI calls, waits for completion, AI-analyzes each outcome, and updates records.

## Flow Diagram
See `FLOW_DIAGRAM.png`

## Process Steps
1. **Schedule / Manual / Webhook Trigger** – Start outbound campaign
2. **Fetch Customer Batch (Supabase)** – Load contacts to call
3. **Loop Over Items** – Iterate customers
4. **Initiate VAPI Call** – Dial each customer
5. **Wait 60 Seconds** – Allow call to complete
6. **Check Call Status (API)** – Completed / No Answer / Error
7. **Analyze Call Summary (OpenAI)** – Extract outcome and action
8. **Update Supabase Record** – Store result and next step
9. **Conditional Branching** – Book meeting / retry / archive

## Key Node Types
- `openAi`
- `switch`
- `splitInBatches`
- `code`
- `scheduleTrigger`
- `httpRequest`
- `merge`
- `manualTrigger`
- `webhook`
- `if`
- `supabase`
- `wait`

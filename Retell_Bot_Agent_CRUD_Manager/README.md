# Retell Bot Agent CRUD Manager

**Status:** 🟢 Active  
**Node Count:** 133  
**Connection Ratio:** 100%  
**Workflow ID:** `8HLewVAPEIeQAAuQ`

## Description
Master Retell bot manager: handles create/edit/delete of agents and LLMs via webhook, routes operations via Switch, and manages call records in Supabase with full CRUD.

## Flow Diagram
See `FLOW_DIAGRAM.png`

## Process Steps
1. **Webhook** – Receive agent operation request
2. **Switch** – Route: create / edit / delete / get
3. **HTTP Request (Retell API)** – Perform agent CRUD operation
4. **Create / Update / Delete (Supabase)** – Sync to database
5. **Wait + Poll** – If async, wait for completion
6. **Respond to Webhook** – Return operation result

## Key Node Types
- `splitInBatches`
- `respondToWebhook`
- `code`
- `httpRequest`
- `supabase`
- `filter`
- `set`
- `aggregate`
- `webhook`
- `switch`
- `wait`
- `dateTime`

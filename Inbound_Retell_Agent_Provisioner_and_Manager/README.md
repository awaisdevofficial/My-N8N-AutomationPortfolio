# Inbound Retell Agent Provisioner and Manager

**Status:** 🟢 Active  
**Node Count:** 71  
**Connection Ratio:** 99%  
**Workflow ID:** `f1XPpj85a3IxAVsx`

## Description
Manages inbound Retell AI caller setup: creates LLM + agent configs, fetches and assigns phone numbers, handles create/edit/delete via switch routing, and sends email confirmations.

## Flow Diagram
See `FLOW_DIAGRAM.png`

## Process Steps
1. **Webhook** – Receive provisioning or call request
2. **Switch** – Route: create / edit / delete / get agent
3. **Create Retell LLM** – POST LLM configuration
4. **Create Agent** – Register agent with LLM
5. **Link Phone to Agent** – Bind phone number
6. **Get / Update / Delete (Supabase)** – Sync to database
7. **Send Email Confirmation** – Notify requester
8. **Respond to Webhook** – Return agent details

## Key Node Types
- `openAi`
- `switch`
- `emailSend`
- `respondToWebhook`
- `code`
- `httpRequest`
- `filter`
- `set`
- `webhook`
- `if`
- `supabase`

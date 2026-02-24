# Error Logger AI Diagnosis and Alerts

**Status:** 🔴 Inactive  
**Node Count:** 13  
**Connection Ratio:** 85%  
**Workflow ID:** `j5rFGZ70CY9Wny3O`

## Description
Error monitoring and diagnosis: captures n8n workflow errors, runs AI diagnosis with OpenAI + SerpAPI, logs to Qdrant vector DB, sends email alerts, and posts to Discord ops channel.

## Flow Diagram
See `FLOW_DIAGRAM.png`

## Process Steps
1. **Error Trigger** – Catch any workflow failure
2. **Code in JavaScript** – Extract error details and context
3. **AI Agent (OpenAI)** – Diagnose root cause and suggest fix
4. **SerpAPI Tool** – Search for known solutions
5. **Qdrant Vector Store** – Embed and log error for future reference
6. **Send Email Alert** – Notify engineering team
7. **Create Discord Channel / Post** – Alert ops team

## Key Node Types
- `emailSend`
- `toolSerpApi`
- `code`
- `vectorStoreQdrant`
- `httpRequest`
- `agent`
- `errorTrigger`
- `manualTrigger`
- `discord`
- `embeddingsOpenAi`
- `lmChatOpenAi`

# PA Email Drafter and WhatsApp Responder

**Status:** 🔴 Inactive  
**Node Count:** 13  
**Connection Ratio:** 100%  
**Workflow ID:** `h6jj9lXH9ffJVnsu`

## Description
Personal assistant email workflow: receives WhatsApp commands, classifies intent via AI agent, drafts Gmail emails, sends WhatsApp responses, and maintains conversation memory.

## Flow Diagram
See `FLOW_DIAGRAM.png`

## Process Steps
1. **Webhook (WhatsApp)** – Receive PA command via WhatsApp
2. **AI Agent (OpenAI)** – Understand email intent with memory
3. **Structured Output Parser** – Extract action type + content
4. **Switch – Action Type** – Draft / Send / Search / Reply
5. **Create Draft (Gmail)** – Compose email draft
6. **Send Message (WhatsApp)** – Confirm action to user
7. **Update / Get Row (Supabase)** – Log and retrieve user context

## Key Node Types
- `outputParserStructured`
- `gmail`
- `supabase`
- `httpRequest`
- `webhook`
- `agent`
- `memoryBufferWindow`
- `switch`
- `lmChatOpenAi`

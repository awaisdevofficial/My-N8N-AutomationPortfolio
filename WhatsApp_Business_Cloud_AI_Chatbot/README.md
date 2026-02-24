# WhatsApp Business Cloud AI Chatbot

**Status:** 🟢 Active  
**Node Count:** 26  
**Connection Ratio:** 100%  
**Workflow ID:** `q3b13O9Giyn0Xy6m`

## Description
Full WhatsApp Business Cloud chatbot: handles text and audio messages, AI agent with memory, TTS audio replies, contact tracking in Supabase, and webhook verification.

## Flow Diagram
See `FLOW_DIAGRAM.png`

## Process Steps
1. **Webhook (WhatsApp Business Cloud)** – Receive inbound message
2. **Switch – Message Type** – Text / Audio / Image
3. **AI Agent (OpenAI) + Simple Memory** – Generate contextual reply
4. **OpenAI TTS – Generate Audio** – Convert reply to voice
5. **Switch – Reply Format** – Text vs audio reply
6. **Send Message (WhatsApp Business Cloud)** – Deliver response
7. **Create / Get / Update Row (Supabase)** – Track user and conversation

## Key Node Types
- `openAi`
- `respondToWebhook`
- `httpRequest`
- `supabase`
- `whatsApp`
- `set`
- `webhook`
- `agent`
- `memoryBufferWindow`
- `switch`
- `lmChatOpenAi`

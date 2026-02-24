# WhatsApp Evolution API AI Voice Text Bot

**Status:** 🟢 Active  
**Node Count:** 14  
**Connection Ratio:** 100%  
**Workflow ID:** `avlGibA5wM6eS9WR`

## Description
WhatsApp bot using Evolution API: handles text and voice messages, AI Agent with memory, generates audio replies via OpenAI TTS, and routes by message type.

## Flow Diagram
See `FLOW_DIAGRAM.png`

## Process Steps
1. **Webhook (Evolution API)** – Receive WhatsApp message
2. **Switch – Message Type** – Text / Audio / Other
3. **AI Agent (OpenAI)** – Process text with memory
4. **Generate Audio (OpenAI TTS)** – Convert reply to voice
5. **Switch – Response Type** – Text reply vs audio reply
6. **Send Message (WhatsApp)** – Deliver via Evolution API
7. **Get Row (Supabase)** – Lookup user context

## Key Node Types
- `openAi`
- `httpRequest`
- `supabase`
- `whatsApp`
- `set`
- `webhook`
- `agent`
- `memoryBufferWindow`
- `switch`
- `lmChatOpenAi`

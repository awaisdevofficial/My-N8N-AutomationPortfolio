# WhatsApp AI Agent Audio and Doc Processing

**Status:** 🟢 Active  
**Node Count:** 244  
**Connection Ratio:** 100%  
**Workflow ID:** `c6szUJViEdOgfLrX`

## Description
Advanced WhatsApp AI agent: handles text and audio (Whisper transcription), processes documents, manages contact and thread context, sends AI replies, and schedules meetings.

## Flow Diagram
See `FLOW_DIAGRAM.png`

## Process Steps
1. **Webhook (WhatsApp)** – Receive text or audio message
2. **Switch – Message Type** – Text / Audio / Document
3. **Download Audio + Whisper Transcription** – Convert voice to text
4. **Prepare AI Context** – Load conversation history
5. **AI Agent (GPT-4o-mini)** – Generate intelligent response
6. **Format AI Response** – Structure reply text
7. **Send Response via WhatsApp** – Deliver reply
8. **Log Thread + Update Contact (Postgres)** – Persist conversation
9. **Schedule Meeting Tool** – If meeting intent detected

## Key Node Types
- `openAi`
- `noOp`
- `webhook`
- `googleGemini`
- `memoryBufferWindow`
- `switch`
- `toolCode`
- `supabase`
- `executeWorkflow`
- `lmChatOpenAi`
- `outputParserStructured`
- `respondToWebhook`

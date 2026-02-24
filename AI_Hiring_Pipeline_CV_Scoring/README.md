# AI Hiring Pipeline CV Scoring

**Status:** 🟢 Active  
**Node Count:** 60  
**Connection Ratio:** 100%  
**Workflow ID:** `6bo1pWbInvXV955I`

## Description
End-to-end hiring pipeline: receives CVs, extracts info with AI, scores candidates using Gemini/OpenAI structured output, stores in Supabase, and sends notifications.

## Flow Diagram
See `FLOW_DIAGRAM.png`

## Process Steps
1. **Webhook** – Receive job application / CV
2. **Compression + PDF Extract** – Decompress & parse CV text
3. **AI Agent (Gemini)** – Extract candidate details
4. **Structured Output Parser** – Normalize to JSON schema
5. **Scoring Agent (OpenAI)** – Rate candidate fit 0-100
6. **Supabase – Create/Update Row** – Save candidate record
7. **Conditional Filter** – Qualified vs rejected routing
8. **Email / Notification** – Inform recruiter and candidate

## Key Node Types
- `outputParserStructured`
- `switch`
- `emailSend`
- `pdfVector`
- `merge`
- `filter`
- `webhook`
- `if`
- `agent`
- `compression`
- `supabase`
- `googleGemini`

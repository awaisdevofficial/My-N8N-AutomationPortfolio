# AI Recruitment CV Parser and Scorer

**Status:** 🔴 Inactive  
**Node Count:** 49  
**Connection Ratio:** 94%  
**Workflow ID:** `gh4B0gR1hbS5y9vH`

## Description
AI recruitment tool: scheduled CV processing from Gmail/uploads, extracts candidate info with OpenAI information extractor, scores with AI, stores in Supabase, notifies via WhatsApp.

## Flow Diagram
See `FLOW_DIAGRAM.png`

## Process Steps
1. **Schedule Trigger** – Check for new applications
2. **HTTP Request / Gmail** – Fetch CVs from inbox or URL
3. **Compression + Extract from File** – Unzip and parse PDF/DOCX
4. **Information Extractor (OpenAI)** – Pull name, skills, experience
5. **Structured Output Parser** – Normalize to schema
6. **AI Scoring Agent** – Rate candidate fit
7. **Create / Update Row (Supabase)** – Store candidate record
8. **WhatsApp / Email Notification** – Alert recruiter

## Key Node Types
- `outputParserStructured`
- `gmail`
- `stickyNote`
- `scheduleTrigger`
- `code`
- `supabase`
- `httpRequest`
- `filter`
- `whatsApp`
- `informationExtractor`
- `set`
- `merge`

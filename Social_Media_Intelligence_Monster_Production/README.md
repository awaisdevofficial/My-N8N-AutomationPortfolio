# Social Media Intelligence Monster Production

**Status:** 🟢 Active  
**Node Count:** 651  
**Connection Ratio:** 95%  
**Workflow ID:** `WPQ88yMD7qOwCg8v`

## Description
Production social media intelligence system: scheduled scraping of company + top 5 competitors across all platforms. Uses Apify, Gemini AI analysis, and stores everything in Supabase.

## Flow Diagram
See `FLOW_DIAGRAM.png`

## Process Steps
1. **Schedule Trigger** – Daily automated run
2. **Company Social Router** – Parse company social handles
3. **Top 5 Competitors Discovery** – Identify competitor accounts
4. **Apify – FB / IG / LinkedIn / TikTok** – Run all platform scrapers
5. **Encapsulate Per Platform** – Normalize + structure data
6. **Gemini AI Analyst** – Competitive intelligence report
7. **ElevenLabs TTS (optional)** – Convert insights to audio
8. **Supabase – Store Analysis** – Persist all data

## Key Node Types
- `editImage`
- `openAi`
- `splitInBatches`
- `scheduleTrigger`
- `noOp`
- `merge`
- `facebookGraphApi`
- `webhook`
- `googleGemini`
- `convertToFile`
- `supabase`
- `switch`

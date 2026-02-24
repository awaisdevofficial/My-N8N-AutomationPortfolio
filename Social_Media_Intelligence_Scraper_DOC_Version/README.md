# Social Media Intelligence Scraper DOC Version

**Status:** 🔴 Inactive  
**Node Count:** 530  
**Connection Ratio:** 92%  
**Workflow ID:** `Tn2zpY9DPTUIa84a`

## Description
Documentation version of the Social Media Intelligence system: scrapes company + top 5 competitors across FB/IG/LinkedIn/TikTok using Apify, and runs Gemini AI analysis.

## Flow Diagram
See `FLOW_DIAGRAM.png`

## Process Steps
1. **Manual / Schedule Trigger** – Start scraping run
2. **Company Social Router** – Extract company social handles
3. **Top 5 Competitors Scraper** – Identify competitor profiles
4. **Apify – FB/IG/LinkedIn/TikTok** – Run platform-specific scrapers
5. **Encapsulate Per Platform** – Normalize data structure
6. **Gemini AI Analyst** – Generate competitive insights
7. **Supabase – Store Results** – Save posts and analysis

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

# Social Media Competitor Intelligence Production

**Status:** 🟢 Active  
**Node Count:** 305  
**Connection Ratio:** 98%  
**Workflow ID:** `bC7hpYGYTwn3Jj6m`

## Description
Production social media intelligence: scrapes company + competitors on all platforms with Apify, analyzes with Gemini, and stores structured competitive intelligence in Supabase.

## Flow Diagram
See `FLOW_DIAGRAM.png`

## Process Steps
1. **Schedule / Manual Trigger** – Start intelligence run
2. **Company Social Router** – Extract company handles
3. **Apify – All Platform Scrapers** – Scrape FB / IG / LinkedIn / TikTok
4. **Top 5 Competitors** – Run competitor discovery
5. **Encapsulate Per Platform** – Structure raw scraped data
6. **Gemini AI Analyst** – Generate intelligence report
7. **Supabase – Store Intel** – Persist posts, metrics, insights

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

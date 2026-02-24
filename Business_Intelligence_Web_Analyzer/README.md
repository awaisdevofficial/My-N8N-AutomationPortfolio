# Business Intelligence Web Analyzer

**Status:** 🔴 Inactive  
**Node Count:** 32  
**Connection Ratio:** 100%  
**Workflow ID:** `glVBg3fT6Mc3bhs5`

## Description
Business intelligence analyzer: runs PageSpeed audits, scrapes social handles via Apify, discovers competitors via SerpAPI, generates AI recommendations, and stores all data in Supabase.

## Flow Diagram
See `FLOW_DIAGRAM.png`

## Process Steps
1. **Manual Trigger** – Start analysis for a business
2. **PageSpeed API Audit** – Analyze website performance
3. **Process PageSpeed Data** – Extract scores and metrics
4. **Split Social Handles** – Parse FB/IG/LinkedIn/TikTok handles
5. **Apify – Social Profile Scrapers** – Scrape each platform
6. **SerpAPI – Competitor Search** – Find top 5 competitors
7. **AI Recommendations (OpenAI)** – Generate action plan
8. **Supabase – Insert All Results** – Store analysis and competitors

## Key Node Types
- `supabaseTool`
- `switch`
- `serpApi`
- `code`
- `supabase`
- `httpRequest`
- `set`
- `limit`
- `apify`
- `agent`
- `manualTrigger`
- `lmChatOpenAi`

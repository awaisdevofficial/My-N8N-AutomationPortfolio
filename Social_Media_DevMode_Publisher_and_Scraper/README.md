# Social Media DevMode Publisher and Scraper

**Status:** 🔴 Inactive  
**Node Count:** 270  
**Connection Ratio:** 94%  
**Workflow ID:** `W9AdKUtwsaalJfn4`

## Description
Development/staging version of the social media pipeline: publishes posts (photos, videos, reels) to Facebook and scrapes company/competitor profiles with Apify + Gemini AI.

## Flow Diagram
See `FLOW_DIAGRAM.png`

## Process Steps
1. **Webhook / Schedule Trigger** – Receive publish or scrape request
2. **Check Platform** – Route to correct social network
3. **Get Page Access Token** – Authenticate with platform
4. **Check Media Type** – Photo / Video / Reel / Carousel
5. **Post to Facebook** – Upload and publish content
6. **Update Post Status (Supabase)** – Mark published / failed
7. **Apify Scrapers (FB/IG/LD/TK)** – Run competitor scraping
8. **Gemini AI Analysis** – Generate insights from scraped data

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
- `switch`
- `supabase`

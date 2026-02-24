# Lead Phone Scraper to Sheets and Database

**Status:** 🟢 Active  
**Node Count:** 10  
**Connection Ratio:** 90%  
**Workflow ID:** `jE3pZ994JO2Ho8lo`

## Description
Automated lead data collector: runs Apify scrapers on schedule, extracts phone numbers, validates data, saves to both Google Sheets and Postgres, and can be triggered as sub-workflow.

## Flow Diagram
See `FLOW_DIAGRAM.png`

## Process Steps
1. **Schedule Trigger / Sub-Workflow Trigger** – Start scraping run
2. **Apify – Run Actor** – Scrape target website for leads
3. **Extract Phone Numbers (Code)** – Parse phone numbers from data
4. **Filter Valid Data** – Remove invalid/empty entries
5. **Validate Input** – Schema and format validation
6. **Add to Google Sheets** – Append lead data to sheet
7. **Save to Database (Postgres)** – Persist structured record

## Key Node Types
- `googleSheets`
- `postgres`
- `scheduleTrigger`
- `noOp`
- `code`
- `if`
- `apify`
- `executeWorkflowTrigger`

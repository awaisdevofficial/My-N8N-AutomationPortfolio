# Founders Profile Scraper to Database

**Status:** 🟢 Active  
**Node Count:** 8  
**Connection Ratio:** 50%  
**Workflow ID:** `3Xk0y4MdaHuXnkna`

## Description
Scrapes co-founder and founder profiles from external sources and stores structured data into Supabase via webhook trigger.

## Flow Diagram
See `FLOW_DIAGRAM.png`

## Process Steps
1. **Webhook / Trigger** – Start profile collection
2. **founders-profile-ext** – Extract founder profile data
3. **HTTP Request** – Fetch additional data from external API
4. **Code in JavaScript** – Transform and clean data
5. **Create a row (Supabase)** – Save founder record to database

## Key Node Types
- `stickyNote`
- `code`
- `httpRequest`
- `webhook`
- `supabase`

# Facebook Ads Campaign Creator

**Status:** 🔴 Inactive  
**Node Count:** 16  
**Connection Ratio:** 75%  
**Workflow ID:** `695T143JXJiyI6Vl`

## Description
Creates Facebook ad campaigns (boosted posts), sets up ad sets and creatives via Meta API, then initiates a voice AI phone call as follow-up.

## Flow Diagram
See `FLOW_DIAGRAM.png`

## Process Steps
1. **Webhook** – Receive campaign creation request
2. **Set Variables** – Configure campaign parameters
3. **Create Campaign (Meta API)** – POST /campaigns
4. **Create Ad Set** – Define targeting & budget
5. **Create Creative** – Upload ad creative
6. **Create Ad (Boost Post)** – Publish the ad
7. **Create Phone Call (AI)** – Initiate follow-up call

## Key Node Types
- `set`
- `webhook`
- `stickyNote`
- `httpRequest`

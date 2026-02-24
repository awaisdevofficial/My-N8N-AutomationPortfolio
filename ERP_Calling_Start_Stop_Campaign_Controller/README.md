# ERP Calling Start Stop Campaign Controller

**Status:** 🟢 Active  
**Node Count:** 42  
**Connection Ratio:** 60%  
**Workflow ID:** `wRvC8WyzmFoOgYS7`

## Description
ERP calling campaign controller: webhook-triggered start/stop, fetches pending customers, initiates VAPI calls, tracks outcomes, and syncs results to Google Sheets.

## Flow Diagram
See `FLOW_DIAGRAM.png`

## Process Steps
1. **Webhook Trigger** – Start or stop calling campaign
2. **Fetch Pending Customers (ERP)** – Load contacts needing calls
3. **Calculate Available Slots** – Determine batch size
4. **Initiate VAPI Call per Customer** – Dial contact
5. **Wait 60 Seconds + Poll** – Check call completion
6. **Analyze Call Summary (AI)** – Booked / Declined / No Answer
7. **Update Google Sheets** – Sync outcome to reporting sheet
8. **HTTP Request (ERP API)** – Update ERP system record

## Key Node Types
- `googleSheets`
- `stickyNote`
- `code`
- `noOp`
- `httpRequest`
- `webhook`
- `if`
- `manualTrigger`
- `wait`

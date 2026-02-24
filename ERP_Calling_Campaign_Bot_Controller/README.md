# ERP Calling Campaign Bot Controller

**Status:** 🟢 Active  
**Node Count:** 196  
**Connection Ratio:** 58%  
**Workflow ID:** `N0qUORRNEzMpxQxT`

## Description
Large ERP-integrated calling bot controller with start/stop logic. Fetches pending customers, calculates call slots, initiates VAPI calls in batches, and tracks outcomes.

## Flow Diagram
See `FLOW_DIAGRAM.png`

## Process Steps
1. **Webhook / Manual Trigger** – Start or stop campaign
2. **Fetch Pending Customers** – Query ERP / Supabase for contact list
3. **Calculate Available Call Slots** – Limit concurrent calls
4. **Process Customer Data** – Prepare call payload per contact
5. **Initiate VAPI Call** – Dial customer via VAPI API
6. **Wait 60 Seconds** – Poll for completion
7. **Check Call Status** – Completed / No Answer / Failed
8. **Analyze Call Summary (AI)** – Meeting booked vs declined
9. **Update ERP / Supabase** – Write outcome back to system

## Key Node Types
- `stickyNote`
- `code`
- `noOp`
- `httpRequest`
- `webhook`
- `if`
- `manualTrigger`
- `wait`

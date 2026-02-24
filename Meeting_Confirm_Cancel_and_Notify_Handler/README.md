# Meeting Confirm Cancel and Notify Handler

**Status:** 🔴 Inactive  
**Node Count:** 21  
**Connection Ratio:** 100%  
**Workflow ID:** `jxagZ78YKcHxcuRW`

## Description
Meeting lifecycle manager: validates inbound responses, finds pending meetings in Postgres, branches on confirmed vs cancelled, updates status, and WhatsApps all parties.

## Flow Diagram
See `FLOW_DIAGRAM.png`

## Process Steps
1. **Execute Workflow Trigger** – Receive meeting response
2. **Validate & Classify Response** – Confirmed / Cancelled / Invalid
3. **Find Pending Meeting (Postgres)** – Locate meeting record by ID
4. **Meeting Found?** – Branch: found vs not found error
5. **Is Confirmed?** – Branch: confirm vs cancel path
6. **Update Status (Postgres)** – Write: Scheduled or Cancelled
7. **Format Messages (Code)** – Build WhatsApp text for all parties
8. **Notify Scheduler + Contact** – HTTP → WhatsApp API both users

## Key Node Types
- `postgres`
- `code`
- `httpRequest`
- `if`
- `executeWorkflowTrigger`

# VAPI Assistant Switch Provisioner

**Status:** 🔴 Inactive  
**Node Count:** 79  
**Connection Ratio:** 72%  
**Workflow ID:** `UHBgh9Tu9NKUV4su`

## Description
VAPI assistant provisioner with form-based input and switch routing. Creates and updates VAPI assistants in bulk from database records, supporting multiple config variations.

## Flow Diagram
See `FLOW_DIAGRAM.png`

## Process Steps
1. **Form Submission / Manual Trigger** – Input assistant parameters
2. **Get Rows (Supabase)** – Fetch assistant config records
3. **Loop Over Items** – Iterate each assistant to create
4. **Switch / If** – Route by assistant type
5. **Create Assistant (VAPI API)** – POST assistant config
6. **Update Row (Supabase)** – Store VAPI assistant ID

## Key Node Types
- `openAi`
- `switch`
- `splitInBatches`
- `stickyNote`
- `code`
- `supabase`
- `httpRequest`
- `merge`
- `set`
- `webhook`
- `if`
- `manualTrigger`

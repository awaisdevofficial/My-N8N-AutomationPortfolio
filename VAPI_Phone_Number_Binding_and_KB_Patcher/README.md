# VAPI Phone Number Binding and KB Patcher

**Status:** 🟢 Active  
**Node Count:** 20  
**Connection Ratio:** 80%  
**Workflow ID:** `v2aVgz8txvZJerq5`

## Description
VAPI configuration manager: imports phone numbers from Twilio/Vonage, binds them to VAPI assistants, creates and uploads knowledge base files, and patches assistants with the new KB.

## Flow Diagram
See `FLOW_DIAGRAM.png`

## Process Steps
1. **Form Submission / Manual Trigger** – Start configuration process
2. **Twilio/Vonage Number Import** – Fetch available phone numbers
3. **Loop Over Items** – Iterate each number
4. **VAPI Number Binding** – Link number to VAPI assistant
5. **Making Knowledge Base** – Create KB in VAPI
6. **Uploading File to VAPI** – Upload KB document
7. **Patch Assistant with KB** – Update assistant config
8. **Insert / Delete Rows (Data Table)** – Track processed numbers

## Key Node Types
- `splitInBatches`
- `httpRequest`
- `dataTable`
- `if`
- `manualTrigger`
- `formTrigger`
- `wait`

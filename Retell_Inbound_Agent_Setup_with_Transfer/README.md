# Retell Inbound Agent Setup with Transfer

**Status:** 🔴 Inactive  
**Node Count:** 12  
**Connection Ratio:** 100%  
**Workflow ID:** `SqgDK9fwPmBv819c`

## Description
Provisions a complete Retell inbound call setup with transfer capability: creates LLM, agent, purchases phone number, links it, and verifies configuration.

## Flow Diagram
See `FLOW_DIAGRAM.png`

## Process Steps
1. **Manual / Test Trigger** – Start provisioning
2. **Step 1: Create Retell LLM** – POST LLM config to Retell API
3. **Step 2: Create Agent** – Register agent with LLM ID
4. **Step 3: Buy Phone Number** – Purchase number via Retell API
5. **Step 4: Link Phone to Agent** – Bind number to agent
6. **Merge Results** – Combine all created resource IDs
7. **Verify Setup (OpenAI)** – Confirm configuration is correct

## Key Node Types
- `manualTrigger`
- `openAi`
- `httpRequest`
- `merge`

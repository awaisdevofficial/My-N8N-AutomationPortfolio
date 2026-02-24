# Retell VAPI Batch Testing Suite

**Status:** 🔴 Inactive  
**Node Count:** 16  
**Connection Ratio:** 94%  
**Workflow ID:** `QxEK9TxyxVqpDgMi`

## Description
Automated testing suite for Retell AI and VAPI: creates LLMs, agents, and phone number bindings in bulk, then runs batch calls and checks statuses in a loop.

## Flow Diagram
See `FLOW_DIAGRAM.png`

## Process Steps
1. **Manual Trigger** – Start batch test run
2. **Format CSV** – Load test cases from CSV
3. **Loop Over Items** – Iterate each test case
4. **Create Retell LLM** – Provision LLM config
5. **Create Agent** – Register agent with LLM
6. **Bind Phone Number** – Link number to agent
7. **Batch Call (Retell / VAPI)** – Initiate test call
8. **Get Call / Check Status** – Poll until complete

## Key Node Types
- `splitInBatches`
- `code`
- `httpRequest`
- `if`
- `wait`

# AI Chat Agent for Video Meetings

**Status:** 🔴 Inactive  
**Node Count:** 3  
**Connection Ratio:** 100%  
**Workflow ID:** `w8suhODD9u5W9j6T`

## Description
AI chat agent for video meetings: listens via chat trigger and uses OpenAI GPT to respond to messages in real-time during meetings.

## Flow Diagram
See `FLOW_DIAGRAM.png`

## Process Steps
1. **Chat Message Received** – Detect new chat message
2. **OpenAI Chat Model** – Process message with GPT
3. **AI Agent** – Generate and stream response

## Key Node Types
- `chatTrigger`
- `lmChatOpenAi`
- `agent`

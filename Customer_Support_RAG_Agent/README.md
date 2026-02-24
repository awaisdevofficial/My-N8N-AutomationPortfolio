# Customer Support RAG Agent

**Status:** 🟢 Active  
**Node Count:** 6  
**Connection Ratio:** 100%  
**Workflow ID:** `1onFiCPvyzcK4erC`

## Description
AI customer support agent using RAG. Receives queries via webhook, searches Qdrant vector store with OpenAI embeddings, and returns grounded answers.

## Flow Diagram
See `FLOW_DIAGRAM.png`

## Process Steps
1. **Webhook** – Receive inbound customer query
2. **Embeddings OpenAI** – Embed query for semantic search
3. **Qdrant Vector Store** – Retrieve relevant knowledge chunks
4. **AI Agent (OpenAI)** – Generate grounded answer from context
5. **Respond to Webhook** – Return AI response to caller

## Key Node Types
- `respondToWebhook`
- `webhook`
- `agent`
- `vectorStoreQdrant`
- `embeddingsOpenAi`
- `lmChatOpenAi`

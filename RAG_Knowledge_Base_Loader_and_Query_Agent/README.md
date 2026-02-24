# RAG Knowledge Base Loader and Query Agent

**Status:** 🟢 Active  
**Node Count:** 12  
**Connection Ratio:** 100%  
**Workflow ID:** `XVdCAum8FDKvnvRX`

## Description
Dual-purpose RAG workflow: manually seeds Qdrant vector store with documents (chunked + embedded), and responds to webhook queries using an OpenAI AI agent over the knowledge base.

## Flow Diagram
See `FLOW_DIAGRAM.png`

## Process Steps
1. **Manual Trigger** – Seed mode: load documents
2. **Default Data Loader** – Import documents
3. **Recursive Text Splitter** – Chunk into segments
4. **Embeddings OpenAI** – Vectorize chunks
5. **Qdrant Vector Store** – Upsert vectors to collection
6. **Webhook** – Query mode: receive user question
7. **AI Agent (OpenAI)** – Answer using RAG context
8. **Respond to Webhook** – Return answer to caller

## Key Node Types
- `respondToWebhook`
- `textSplitterRecursiveCharacterTextSplitter`
- `documentDefaultDataLoader`
- `set`
- `webhook`
- `agent`
- `vectorStoreQdrant`
- `manualTrigger`
- `embeddingsOpenAi`
- `lmChatOpenAi`

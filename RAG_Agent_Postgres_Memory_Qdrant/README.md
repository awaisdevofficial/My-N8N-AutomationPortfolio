# RAG Agent Postgres Memory Qdrant

**Status:** 🟢 Active  
**Node Count:** 12  
**Connection Ratio:** 100%  
**Workflow ID:** `OKcSJ20eALfPix56`

## Description
RAG AI agent with persistent Postgres chat memory. Loads documents into Qdrant, splits with recursive splitter, and answers webhook queries with full conversation context.

## Flow Diagram
See `FLOW_DIAGRAM.png`

## Process Steps
1. **Manual Trigger** – Seed mode: load documents
2. **Default Data Loader** – Import documents
3. **Recursive Character Text Splitter** – Chunk documents
4. **Embeddings OpenAI** – Embed chunks
5. **Qdrant Vector Store** – Upsert embeddings
6. **Webhook** – Receive user question
7. **AI Agent + Postgres Chat Memory** – Answer with context + history
8. **Respond to Webhook** – Return AI answer

## Key Node Types
- `memoryPostgresChat`
- `respondToWebhook`
- `textSplitterRecursiveCharacterTextSplitter`
- `documentDefaultDataLoader`
- `set`
- `webhook`
- `agent`
- `vectorStoreQdrant`
- `manualTrigger`
- `embeddingsOpenAi`

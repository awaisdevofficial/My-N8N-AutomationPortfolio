# Veo Text to Video Generation Pipeline

**Status:** 🔴 Inactive  
**Node Count:** 112  
**Connection Ratio:** 97%  
**Workflow ID:** `in5Y2ibUaI31k1EY`

## Description
Multi-video generation pipeline using Google Veo: generates up to 8 parallel videos from text prompts, polls completion, merges via FFmpeg API, and saves to Postgres and file storage.

## Flow Diagram
See `FLOW_DIAGRAM.png`

## Process Steps
1. **Manual Trigger / Form** – Input video prompts
2. **Video Prompts Splitter** – Distribute prompts to parallel branches
3. **Text to Video (Veo API) x8** – Submit up to 8 generation jobs
4. **Wait + Poll Status per Branch** – Check each video completion
5. **Extract Video URL** – Get download link
6. **All Videos Ready?** – Gate: wait for all branches
7. **Merge Videos (FFmpeg API)** – Combine into single output
8. **Save to Postgres / File** – Persist result

## Key Node Types
- `postgres`
- `executeWorkflowTrigger`
- `readWriteFile`
- `code`
- `manualTrigger`
- `httpRequest`
- `merge`
- `set`
- `writeBinaryFile`
- `webhook`
- `form`
- `if`

# AI Video Generator FAL and Replicate

**Status:** 🔴 Inactive  
**Node Count:** 26  
**Connection Ratio:** 100%  
**Workflow ID:** `9lJooGbj5gdJzmy1`

## Description
Generates videos using FAL.ai (Wan2.1) and Replicate (Wan2.1) APIs. Polls prediction status with retry logic, downloads the final video file on completion.

## Flow Diagram
See `FLOW_DIAGRAM.png`

## Process Steps
1. **Manual Trigger** – Start generation manually
2. **Set Prompt & Config** – Define prompt, dimensions, model
3. **Submit to FAL / Replicate** – Queue video generation job
4. **Wait 5-10 Seconds** – Initial wait before polling
5. **Check Prediction Status** – Poll API for job status
6. **Is Completed?** – Branch: done vs retry
7. **Should Continue Retrying?** – Max retry guard
8. **Extract Video URL** – Get output URL from response
9. **Download Video File** – Fetch final MP4 to memory

## Key Node Types
- `code`
- `httpRequest`
- `set`
- `if`
- `manualTrigger`
- `wait`

# ComfyUI Multi Mode AI Media Generator

**Status:** 🔴 Inactive  
**Node Count:** 49  
**Connection Ratio:** 90%  
**Workflow ID:** `yy9Q26ayRNUNI3M9`

## Description
Multi-mode AI media generator via ComfyUI: text-to-image (Flux), image-to-image, text-to-video, and image-to-video (Wan2.2 with ElevenLabs audio). Routes by request type.

## Flow Diagram
See `FLOW_DIAGRAM.png`

## Process Steps
1. **Webhook** – Receive generation request with type
2. **Switch – Generation Type** – T2I Realistic / T2I Illustrative / T2V / I2V
3. **Build ComfyUI Workflow (Code)** – Construct ComfyUI JSON prompt
4. **Queue to ComfyUI** – POST prompt to ComfyUI /prompt endpoint
5. **Extract Prompt ID** – Get job ID from response
6. **Wait N Seconds** – Allow generation time
7. **Check ComfyUI History** – Poll /history endpoint
8. **Extract Filename** – Get output file path
9. **Download Generated File** – Fetch image or video
10. **Respond to Webhook** – Return file to requester

## Key Node Types
- `stickyNote`
- `respondToWebhook`
- `code`
- `httpRequest`
- `set`
- `webhook`
- `convertToFile`
- `switch`
- `wait`

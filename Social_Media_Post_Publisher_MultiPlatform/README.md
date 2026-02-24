# Social Media Post Publisher MultiPlatform

**Status:** 🔴 Inactive  
**Node Count:** 129  
**Connection Ratio:** 93%  
**Workflow ID:** `CUYMy2NlL4SvKCRn`

## Description
Publishes social media posts across platforms. Receives requests via webhook, fetches content from Postgres, checks platform, gets access tokens, and posts photos/videos.

## Flow Diagram
See `FLOW_DIAGRAM.png`

## Process Steps
1. **Webhook / Sub-Workflow Trigger** – Receive publish request
2. **Get Main Content (Postgres)** – Fetch post text and media URL
3. **Check Platform** – Route: Facebook / Instagram / Other
4. **Get Page Access Token** – Authenticate with platform API
5. **Check Media Type** – Photo vs Video vs Reel
6. **Post Photo / Video** – Upload and publish
7. **Update Post Status (DB)** – Mark as published or failed
8. **Respond to Webhook** – Return publish result

## Key Node Types
- `switch`
- `postgres`
- `stickyNote`
- `code`
- `respondToWebhook`
- `httpRequest`
- `merge`
- `wait`
- `webhook`
- `if`
- `supabase`
- `executeWorkflowTrigger`

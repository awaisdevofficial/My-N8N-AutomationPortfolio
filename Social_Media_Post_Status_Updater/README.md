# Social Media Post Status Updater

**Status:** 🔴 Inactive  
**Node Count:** 9  
**Connection Ratio:** 100%  
**Workflow ID:** `cscJd973XnnUOjB6`

## Description
Lightweight social media post status update workflow: fetches post records from Supabase, merges data, calls external APIs to update post state, and routes via Switch.

## Flow Diagram
See `FLOW_DIAGRAM.png`

## Process Steps
1. **Webhook** – Receive update trigger
2. **Get Post Rows (Supabase)** – Fetch post and page records
3. **Merge Data** – Combine post + page info
4. **Switch** – Route by platform or action type
5. **HTTP Request (Platform API)** – Call social media API to update
6. **Respond to Webhook** – Return update result

## Key Node Types
- `switch`
- `respondToWebhook`
- `httpRequest`
- `merge`
- `webhook`
- `supabase`

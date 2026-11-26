---
title: Create a broadcast
description: Four steps — a template, a segment, sending, and the statistics.
---

The WhatsApp channel must already be connected. Then there are four steps.

## 1. Create a template

Do it in the [Channels](https://platform.1msg.io/channels) section of the dashboard, through the API with [addTemplate](https://1msg.io/docs/reference/whatsapp/add-template), or from an assistant over [MCP](https://platform.1msg.io/developers/mcp). A marketing or utility broadcast needs an approved template. Plain text inside an open 24-hour window goes out without one.

## 2. Create a segment

The segment decides who receives the message. A fixed list is one you build yourself: by hand, from a CSV, or by a selection from Inbox. A dynamic list is taken from Inbox when the broadcast is sent.

## 3. Create the broadcast

Open [Campaigns](https://platform.1msg.io/messaging/campaigns) and click **New campaign**. Choose the channel and the segment, and fill in the template or the text. Check the preview and send a test to your phone. Then send now or pick a time, and the broadcast goes out on its own. You see the cost forecast before sending, and you pay only for delivered messages.

## 4. View the statistics

Open the broadcast. The overview shows delivery and the actual cost. The Recipients, Replies, and Errors tabs show the detail: who read, replied, or unsubscribed, who was skipped, and where an error happened.

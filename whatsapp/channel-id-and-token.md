---
title: Channel ID + JWT
description: Where to find a channel's ID and JWT token, how to pass them in an API request and what the authorization errors mean.
---

Every API request carries two things: a **Channel ID** — which number you send from — and a **JWT token** — proof that the request is yours. Both come from the channel page.

Below: where to find them, how to put them in a request, how to verify, and what to do if the request fails.

## Step 1. Open the channel page

Sign in to [**platform.1msg.io**](https://platform.1msg.io/) and open the channel you will send from. If several numbers are connected, each is a separate channel with its own token.

If you do not have an account yet, start with [Quick start](../platform/quickstart.md): you can activate a test channel and send your first message without waiting for Meta approval.

## Step 2. Copy the Channel ID and token

On the channel page you will find:

* **Channel ID** — a short identifier; it becomes part of the request URL;
* **JWT Token** — a string you must send with every request.

The token is a password. Anyone who has it can send messages on behalf of your business. Store it in server environment variables: not in frontend code, not in a public repository, and not in screenshots.

## Step 3. Put them in the request

Requests go to [**api.1msg.io**](https://api.1msg.io/). The Channel ID goes in the URL right after the host:

```
https://api.1msg.io/{channelId}/sendMessage
```

You can pass the token in two ways. They are equivalent: the API looks for it first in the request body, then in the query string, then in the header.

**In the header — recommended:**

```bash
curl -X POST "https://api.1msg.io/{channelId}/sendMessage" \
  -H "Authorization: Bearer {token}" \
  -H "Content-Type: application/json" \
  -d '{"phone": "79001234567", "body": "Hello 1msg"}'
```

A token in the header does not end up in server access logs or browser history — so this is preferred for production.

**In the query string:**

```bash
curl -X POST "https://api.1msg.io/{channelId}/sendMessage?token={token}" \
  -H "Content-Type: application/json" \
  -d '{"phone": "79001234567", "body": "Hello 1msg"}'
```

Handy for a quick check, but the token will land in access logs and on proxies. Do not use this in production.

## Step 4. Verify that it works

Open [Playground](https://platform.1msg.io/dashboard/playground) in the dashboard. It fills in the Channel ID and token for you, and shows the ready request JSON, the API response, and what arrives at the webhook. If the message was delivered, the Channel ID + token pair works — and you can reuse the same JSON in your code.

## If something goes wrong

**`token is required`, code 401.** The token did not reach the API. Make sure it is present in at least one place: body or header.

**`access denied`, code 403.** The most common error. It means one of two things: the token is wrong (typo, truncated when copied) or it belongs to a different channel than the one in the URL. Copy the ID and token again from the same channel page.

**`Invalid API KEY`, code 401.** The token reached WhatsApp but was rejected there. Usually the channel is no longer connected — check its status in the dashboard.

**`Instance not found`, code 404.** The Channel ID in the URL is wrong — make sure it was copied in full and without spaces.

## One channel — one token

Each channel has its own token. If a business has several WhatsApp numbers, it also has several channels and several tokens. A token from one channel will not work for sending from another.

## What's next

* [Quick start](../platform/quickstart.md) — from the first message to production
* [Connection WABA](./connect-waba/README.md) — connect your own number
* [API reference](https://docs.1msg.io/) — all methods

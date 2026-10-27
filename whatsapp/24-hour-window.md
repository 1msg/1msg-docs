---
title: 24-hour conversation window
description: When you can send any message to a customer on WhatsApp and when only a pre-approved template will do.
---

The 24-hour conversation window is the period during which a business can freely send any messages to a customer in response to their last contact. While the window is open, paid templates are not required. When it is closed, you can only write using a pre-approved paid template.

This is a Meta rule, not a 1MSG rule: it works the same way for every WhatsApp Business API provider.

## How the window works

1. **The window opens** when the business receives a message from the customer. The message can be anything: a question, a request, or simply a greeting.
2. From the moment the **last** inbound message is received, the business has 24 hours to send messages. During that time you can send any messages that comply with WhatsApp policy without paid templates — that is, hold a normal conversation.
3. **After 24 hours** from the last inbound message, the window closes. After that, free-form messages cannot be sent until the customer writes again.
4. **While the window is closed**, you can only send pre-approved paid templates.
5. **To reopen the window**, the customer must send a new message. After that, the countdown starts over — another 24 hours of free-form conversation.

Example: the customer wrote at 11:00 — until 11:00 the next day you can reply freely.

Your own messages do not open or extend the window.

Separately: messages sent from the WhatsApp Business app do not create or extend the Cloud API window — the limit applies only to messages through the Cloud API.

## What you can do while the window is open

Any messages that comply with WhatsApp policy: text, files, images, buttons, lists. A template is not required.

## What to do when the window is closed

Send a pre-approved template. Choose the category by situation:

* **MARKETING** — start a conversation, announce a promotion or new product, collect feedback;
* **UTILITY** — respond to a customer action: order confirmation, transaction, subscription status;
* **AUTHENTICATION** — one-time codes for registration, sign-in, or access recovery.

Steps:

1. The window is closed → send a template.
2. The customer replies → the window is open.
3. For the next 24 hours, converse freely.

More on templates — in the section on creating and sending templates.

## How much it costs

An open window does not mean “free.” As of July 1, 2025, Meta charges for each delivered template message, not for the conversation. Inside the window, free-form messages do not require templates; utility templates (UTILITY) inside the window are free; marketing templates are always paid.

Details — [Messaging costs](../platform/billing/messaging-costs.md).

## What’s next

* [Quick start](../platform/quickstart.md)
* Creating and sending templates
* [Messaging costs](../platform/billing/messaging-costs.md) — rates and template categories
* [API reference](https://docs.1msg.io/) — `/sendMessage` and `/sendTemplate` methods

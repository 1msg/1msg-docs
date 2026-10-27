---
title: Messaging costs
description: How template message billing works in WhatsApp Business API (WABA).
---

## Quick summary — key points

* A **24-hour customer service window** opens when a user sends you a message.
* Inside this window, you can reply with **free-form messages**.
* Outside the 24-hour window, you can only send **template messages**.
* **Marketing templates are always paid**, even within the 24-hour window.
* **Utility templates are always paid**, even within the 24-hour window
* **Authentication templates** (OTP, verification codes) are billed separately by Meta.
* We apply the official Meta pricing with only a **5% markup**, while most providers charge around **15%**.

## What is the 24-hour window

When a user sends you any message, WhatsApp opens a 24-hour customer service window.

Example, customer send message at 11:00 AM

`"Hello, where is my order?"`

Until 11:00 AM the next day, the business can:

* send free-form messages;
* reply without templates;
* communicate freely within the session.

## Types of template messages

| Category | Purpose |
| --- | --- |
| Marketing | Promotions, discounts, campaigns |
| Utility | Order updates, receipts, notifications |
| Authentication | OTP, login codes, 2FA |

### Pricing

[Cost per message in USD on the WhatsApp Business Platform, effective October 1, 2026 (XLSX)](./assets/whatsapp-rates-2026-10-01.xlsx)

### 1. Marketing Templates

Marketing templates are **ALWAYS** paid. Even if the user messaged you just a minute ago.

### 2. Utility Templates

Utility Templates are **ALWAYS** paid. Even if the user messaged you just a minute ago

### 3. Authentication Templates

* can be sent outside the 24-hour window;
* always billed;
* typically cheaper than marketing templates;
* strictly limited use cases.

## Billing rules summary

| Message type            | Within 24h window                                                            | Outside 24h window |
| ----------------------- | ---------------------------------------------------------------------------- | ------------------ |
| Free-form message       | The first 1,000 incoming messages are free; additional messages are charged. | Not allowed        |
| Marketing template      | Paid                                                                         | Paid               |
| Utility template        | Paid                                                                         | Paid               |
| Authentication template | Paid (Meta rate)                                                             | Paid (Meta rate)   |

## Important rule

Free-form messages:

* are only allowed within the 24-hour window;
* cannot be sent outside the window.

After the window closes, **templates are mandatory**.

## Pricing model in our platform

We use official Meta pricing.

Additionally:

* our platform applies only a **5% markup**;
* this is significantly lower than the market average (\~15%).

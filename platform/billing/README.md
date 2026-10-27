---
title: Pricing and Billing
description: How the platform subscription and the WhatsApp conversation balance are paid, charged and topped up.
---

The platform uses two separate payment mechanisms:

1. Platform subscription — paid via Stripe
2. WhatsApp (WABA) conversation session balance — managed separately from the subscription

> [!NOTE]
> The subscription fee is not charged from the balance. The balance is used only for WhatsApp conversation session charges.

## Subscription via Stripe

Platform subscriptions are processed through Stripe Billing.

After subscribing, you can manage your subscription through the Stripe Customer Portal available in the [Billing](https://platform.1msg.io/manage/billing) section inside the platform.

The Customer Portal allows you to:

* view your current plan
* change your subscription plan
* cancel your subscription
* renew or reactivate your subscription
* update your payment card
* change billing address and billing information
* view invoices and payment receipts
* download invoice PDFs
* retry failed payments

All subscription-related operations are handled directly through the Stripe Customer Portal.

About subscription plans:

* [Subscription plans](./subscription-plans.md)

## Balance for WhatsApp Conversation Sessions (WABA)

The balance is used exclusively for WhatsApp conversation session charges through WABA.

The platform uses a postpaid billing model. This means conversation session charges are applied after actual usage.

If the balance becomes negative, during the next successful charge or top-up:

* the outstanding debt is deducted first
* then the remaining amount is credited to the balance

Example:

* if the balance is `-3 USD`
* and an automatic charge / top-up of `10 USD` is performed

then:

* `3 USD` will be used to cover the debt
* `10 USD` will be credited to the balance

## How Charges Are Calculated

The system calculates the cost of used conversation sessions and processes charges once per hour based on actual usage.

Pricing depends on the conversation category:

* Marketing
* Utility
* Authentication / Authorization

Current conversation pricing is provided in a separate pricing document.

* [Messaging costs](./messaging-costs.md)

## Negative Balance and Channel Blocking

If the balance becomes negative, the system automatically attempts to charge the linked payment card.

During the automatic charge:

* the negative balance is covered first
* then an additional `10 USD` is charged to restore a positive balance

Only one automatic charge attempt is performed.

* If the payment succeeds — the balance is restored automatically
* If the payment fails — the channel will be blocked until the balance is manually replenished

To avoid channel interruption, it is recommended to maintain a positive balance or enable Auto Top-Up.

## Auto Top-Up

To automatically maintain a positive balance, it is recommended to enable the Auto Top-Up feature.

When configuring Auto Top-Up, you need to specify:

* the balance threshold
* the top-up amount

When the balance falls below the configured threshold, the system automatically attempts to charge the payment card and replenish the balance.

### Auto Top-Up Failure Handling

For each automatic top-up, the system performs up to 3 payment attempts.

* If one of the attempts succeeds — the balance is replenished automatically
* If all 3 attempts fail — Auto Top-Up will be disabled for the current payment method

If the balance later becomes negative, the channel may be suspended until the balance is manually replenished.

## Manual Balance Top-Up

The balance can be replenished separately from the platform subscription.

Balance funds are used only for:

* WhatsApp conversation session charges

The platform subscription continues to be billed separately through Stripe Subscription Billing.

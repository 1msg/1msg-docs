---
title: Campaigns
description: Send one WhatsApp message to many recipients at once from a connected channel.
---

A campaign sends one WhatsApp message to many recipients at once from a connected channel. You choose the audience, the message, and when it goes out, and after it starts you see delivery and cost on the same screen.

> [!NOTE]
> **For developers.** You can use the [Campaigns API](/docs/reference/campaigns). Every capability described below is available in the API. Choose the option that suits you: the dashboard or the API.

![Campaigns](./assets/campaign-ui-screencast.gif)

## Quick start

**Before you start.** The WhatsApp channel must be connected.

1. **Create a template.** Do it in the [Channels](https://platform.1msg.io/channels) section of the dashboard, through the API with [addTemplate](https://1msg.io/docs/reference/whatsapp/add-template), or from an assistant over [MCP](https://platform.1msg.io/developers/mcp). A marketing or utility campaign needs an approved template. Plain text inside an open 24-hour window goes out without one.
2. **Create a segment.** Open **Campaigns → Segments → [New segment](https://platform.1msg.io/messaging/campaigns/segments/new)**. Add people by hand, from a CSV, or by a condition from Inbox, and set the attributes you want inserted into the message.
3. **Create the campaign.** To create one, open [Campaigns](https://platform.1msg.io/messaging/campaigns) and click **New campaign**. Choose the channel and the segment, and fill in the template or the text. Check the preview, send a test, then send now or schedule it.
4. **View the statistics.** Open the campaign. The overview shows delivery and the actual cost. The Recipients, Replies, and Errors tabs show the detail.

The guides: [Create a segment](./segment.md), [Create a campaign](./create.md), and [Campaign analytics](./analytics.md).

> [!NOTE]
> **For developers.** Campaigns have their own API. Methods, fields and examples are in the [API reference](https://1msg.io/docs/reference/campaigns).

## Capabilities

### Everything you need for a first campaign

**An audience in a couple of minutes.** Add people by hand, upload a CSV, or collect them straight from Inbox, for example every dialog of one teammate.

**Preview.** See the message as the recipient will, before it is sent.

**Test send.** Send one copy to your phone and check the text for real.

**Send now or on a schedule.** Pick a time, and the campaign goes out on its own.

**Cost without surprises.** You see the cost forecast before sending, and you pay only for delivered messages.

**The result on one screen.** How many were sent, delivered, and read, and how many replies and errors there were.

### When you want more

**An audience that builds itself.** A dynamic segment picks recipients by Inbox rules: open dialogs, the 24-hour window, the assignee, the last message. You no longer export and clean lists by hand.

**A message that sounds personal.** “Anna, your order #1234 is on the way, and you have a 15% discount.” Any detail about the contact is filled into the template, and nobody receives a message with a blank spot.

**Your own daily limit.** The campaign splits itself into portions and stays within your number’s tier.

**Message lifetime.** The offer is only for today? Set how long the message stays relevant. If Meta does not deliver it in that time, the customer does not receive it and does not see an outdated offer tomorrow.

**Full control of the launch.** A campaign that is already sending can be paused and resumed. A scheduled one can go back to draft so you can edit it.

**Stoplist.** People who opt out land there automatically. Marketing messages are not sent to them, and you do not pay for those messages.

**Detailed analytics.** Who read, replied, tapped which button, or unsubscribed: numbers for each person, replies, skips, and errors.

**Retry for undelivered.** In one step, create a new campaign only from the people the message did not reach.

**Expense report.** Gather spend by channel, period, or the campaigns you select.

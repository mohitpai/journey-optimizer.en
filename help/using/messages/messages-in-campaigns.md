---
title: Add messages in campaigns
description: Learn how to add messages in a campaign
feature: Overview
topic: Content Management
role: User
level: Beginner
---

# Add messages in campaigns{#messages-in- campaigns}

In your campaigns, select the channel to design and personalize the message you want to send to your audience. When you add an email, a SMS or a Push to your campaign, you can send it immediately or schedule the message.

>[!NOTE]
>You can also create journeys to send triggered messages. Learn more [in this section](messages-in-journeys.md).

Learn how to add and configure messages in a campaign [in this section](../campaigns/create-campaign.md) 

   Learn detailed steps to create your message content in the following page:

   * [Create an email](create-email.md)
   * [Create a push notifications](create-push.md)
   * [Create an SMS message](create-sms.md)

## Enable Send-time optimization{#sto-in-journeys}

For email and push notifications, you can enable **[!UICONTROL Send-time optimization]**.
    
Use **[!UICONTROL Send-time optimization]** to schedule personalized send times for each user to grow the open and click rates of your messages. [Learn more](../messages/send-time-optimization.md).

## Advanced parameters{#adv-settings}

Advanced parameters are read-only and hidden by default. 

To access advanced parameters, click the **[!UICONTROL Show read-only fields]** icon on the top of the messsage pane.

![](assets/show-read-only.png)

Advanced parameters are displayed at the bottom of the message pane. These parameters are defined by the [system administrator](../start/path/administrator.md) in the [channel surface](../configuration/channel-surfaces.md) (i.e. message preset) associated with the message.

For push notifications, you can display the following parameters: Token, AppID, AppPlatform.

![](assets/push-adv-parameters.png)

For email, you can display the primary email address.

For specific use, you can override these values in specific contexts. To force a value, click the **Enable parameter override** icon to the right of the field. This option may be useful for example to:

* Test an email, you can add your email address. After you have published the journey, the email is sent to you.
* Refer to the email address of the subscribers of a list. Learn more in [this use case](../building-journeys/message-to-subscribers-uc.md).

Click the same icon to hide advanced settings.

## Browse messages{#browse-message}

When multiple messages are used in a journey, you can switch from one to another from the **Edit Content** screen.

![](assets/inline-messages-multi-content.png)

You can then [check alerts](alerts.md) and [simulate](../design/preview.md) each content from a single view.

## Duplicate a message {#duplicate-message}

You can copy an existing message from the journey canvas.

To perform this, follow the steps below:

1. Select the message you want to copy.

1. Use the **[!UICONTROL Copy]** button from the **[!UICONTROL Action]** pane.

   ![](assets/message-duplicate.png)

1. Enter **crtl+V** to paste the message.

   The message is added to the journey canevas. All settings and configuration will be copied to the new message.

   ![](assets/message-duplicated.png)

1. Rename the message to be able to differenciate the initial message from the copy, for example when editing messages, as below:

   ![](assets/multi-message.png)


>[!NOTE]
>
>For emails, you can also turn an existing message to a template. [Learn more](../design/email-templates.md).

## Delete a message{#delete-message}

To delete a message, use the trash icon on the top of the channel action activity pane.

![](assets/delete-message.png)

Use the **[!UICONTROL Confirm]** button to validate.

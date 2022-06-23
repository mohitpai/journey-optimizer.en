---
title: Create an SMS message
description: Learn how to create an SMS message in Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 1f88626a-b491-4b36-8e3f-57f2b7567dd0
---
# Create an SMS message {#create-sms}

>[!CONTEXTUALHELP]
>id="ajo_message_sms"
>title="SMS creation"
>abstract="Add your text message and start personalizing it with the Expression Editor."

Once you [created a message](get-started-content.md), use the **[!UICONTROL SMS]** tab to define the settings and content for the SMS message.


>[!AVAILABILITY]
>
>The SMS channel is currently only available for a set of organizations (Limited Availability). For more information, contact your Adobe representative.

![](assets/sms_1.png)

If this is your first time creating an SMS message, make sure the SMS channel has been configured. [Learn more](../configuration/sms-configuration.md).

## Define your SMS content{#sms-content}

To start personalizing your SMS message, follow these steps:

1. Click the **[!UICONTROL Add text message]** field to open the Expression editor.

    ![](assets/sms_3.png)

1. Use the Expression Editor to define content. You can use any attribute to personalize content, such as the profile name or city. Learn more about personalization in the Expression Editor in [this section](../personalization/personalize.md)

    >[!NOTE]
    >
    > An SMS message can have up to 160 characters, including spaces and line breaks.

    ![](assets/sms_2.png)

1. Click **[!UICONTROL Save]** when your message is ready.

## Validate your SMS{#sms-preview}

Once your message content has been defined, you can use test profiles to preview and test it. If you inserted [personalized content](../personalization/personalize.md), you can check how this content is displayed in the message, leveraging test profile data.

To visualize how your SMS message displays on mobile devices, browse to the **[!UICONTROL Preview]** tab.

For more on this, refer to [this section](../design/preview.md).

## Publish your SMS {#sms-publish}

Once your message is ready, you can publish it to make it available for execution with the **[!UICONTROL Publish]** button. This action publishes the new version of the message that will be used for the next executions in your journeys.

Your SMS message can now be used in a journey. [Learn how to create journeys](../building-journeys/journey-gs.md).

## Opt-in and opt-out{#sms-opt-in-out}

For all marketing messages, the SMS must contain a way for the recipients to easily unsubscribe. Once unsubscribed, the profiles are automatically removed from the audience of future marketing messages. Adding an unsubscription link is not mandatory for transactional messages.

SMS recipients can reply with opt-in and opt-out keywords. In accordance with the industry standards and regulations, Adobe Journey Optimizer automatically processes the following keywords in incoming messages: START, STOP, and UNSTOP. These keywords trigger automatic standard replies from the SMS provider.

**Related topics**

* [Configure SMS channel](../configuration/sms-configuration.md)
* [SMS report](../reports/journey-global-report.md#sms-global)
* [Create a new message](get-started-content.md)
* [Add a message in a journey](../building-journeys/journeys-message.md)

---
title: Get started with messages
description: Learn how to create, test and publish personalized messages in Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 712dc172-6c0d-4ce8-ba16-de99d65fc641
---
# Get started with messages {#get-started-contents-messages}

>[!CONTEXTUALHELP]
>id="ajo_journey_message"
>title="Message activity"
>abstract="Use the Message activity to send a push, SMS or email message."

Use [!DNL Journey Optimizer] to create and send personalized push notifications, SMS and email messages, and leverage multiple resources like assets and contents in a single place. 

[!DNL Journey Optimizer] messages are built in the context of journeys <!--and campaigns-->. You can:

* Use [!DNL Journey Optimizer] **email designing capabilities** to create or import responsive emails.

* Leverage **Adobe Experience Manager Assets Essentials** to enrich your emails, build and manage your own assets database.

* Find **Adobe Stock photos** to build your content and improve your email design.

* Enhance customers' experience by creating personalized **push notifications, SMS and email messages** based on their profile attributes.

* **Create messages** based on these contents, then publish them.

To add messages in your journeys, simply add a push, SMS or email activity in the canevas. 

>[!NOTE]
>
>Users can access, create, edit and/or publish messages depending on their product profile. Learn more about user permissions [in this section](../administration/permissions.md).

## Add messages in your journeys{#messages-in-journeys}

Steps to add a message in a journey are detailed below.

1. Start your journey with an [Event](../building-journeys/general-events.md) or a [Read Segment](../building-journeys/read-segment.md) activity.

1. From the **Actions** section of the palette, drag and drop an **email**, an **SMS** or a **Push** activity into the canvas.  

   ![](assets/add-a-message.png)

1. Select the message and enter a label and a description.

1. Select the message **[!UICONTROL Category]**: choose **Marketing** for commercial messages, or choose **Transactional** for non-commercial messages such as order confirmation, password reset notifications, or delivery information.


   >[!CAUTION]
   >
   >Marketing-type messages must include an [opt-out link](../messages/consent.md#opt-out-management). This is not required for transactional messages: these messages can be sent to profiles who unsubscribed from marketing communications.

1. Select the message **[!UICONTROL Surface]** (i.e. message preset) to use to send your message. 

   A surface is a message configuration which has been defined by a [System Administrator](../start/path/administrator.md). It contains all the technical parameters for sending the message, such as header parameters (From), subdomain, and [frequency rules](../configuration/frequency-rules.md#apply-frequency-rule). [Learn more](../configuration/message-presets.md).

   >[!CAUTION]
   >
   >You must choose a valid message surface for the selected message category and channel.
   
   You can access and modify the message's label, description and surface at any time using the **[!UICONTROL Properties]** button in the message interface.

1. Create the message content. 

   Learn detailed steps to create your message content in the following page:

   * [Create an email](create-email.md)
   * [Create a push notifications](create-push.md)
   * [Create an SMS message](create-sms.md)

## Browse messages

When multiple messages are used in a journey, you can switch from one to another from the Edit Content window.

![](assets/inline-messages-multi-content.png)

You can then [check alerts](alerts.md) and [simulate](../design/preview.md) each content from a single window.

## Enable Send-time optimization{#sto-in-journeys}

For email and push notifications, you can enable **[!UICONTROL Send-time optimization]**.
    
Use **[!UICONTROL Send-time optimization]** to schedule personalized send times for each user to grow the open and click rates of your messages. [Learn more](../messages/send-time-optimization.md).

## Advanced parameters{#sto-in-journeys}

Advanced parameters are read-only and hidden by default. 

To access advanced parameters, click the **[!UICONTROL Show read-only fields]** icon on the top of the messsage panel.

![](assets/show-read-only.png)

Advanced parameters are displayed at the bottom of the message panel. These parameters are defined by the [system administrator](../start/path/administrator.md) in the [surface](../configuration/message-presets.md) (or preset) associated to the message.

For push notifications, you can display the following parameters: Token, AppID, AppPlatform.

![](assets/push-adv-parameters.png)

For email, you can display the primary email address.

For specific use, you can override these values in specific contexts. To force a value, click the **Enable parameter override** icon to the right of the field. This option may be useful for example to:

* Test an email, you can add your email address. After you have published the journey, the email is sent to you.
* YRefer to the email address of the subscribers of a list. Learn more in [this use case](../building-journeys/message-to-subscribers-uc.md).

Click the same icon to reset to the default parameter.

## Delete a message

To delete a message, use the trash icon on the top of the message activity panel.

![](assets/delete-message.png)

Click the **[!UICONTROL Confirm]** button to validate.

<!--
## Duplicate a message {#duplicate-message}

To create a message from an existing one, follow the steps below.

1. Open the message you want to copy.

1. Use the **[!UICONTROL Duplicate]** button from the message interface.

   ![](assets/message-duplicate.png)

   All settings and configuration will be copied to the new message.

1. You can rename the message before confirming duplication.

   ![](assets/message-duplicate-confirm.png)

1. A confirmation message displays at the bottom of the window once the new message is created.

You can also duplicate a message from the message list, using the dedicated icon from the quick actions menu.

![](assets/message-duplicate-from-list.png)

The same confirmation process applies.

-->
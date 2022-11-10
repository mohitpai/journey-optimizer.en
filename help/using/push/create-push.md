---
solution: Journey Optimizer
product: journey optimizer
title: Configure a push notification
description: Learn how to create a push notification in Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 2ebbcd7d-dcfc-4528-974d-6230fc0dca3d
---
# Create a push notification {#create-push-notification}

>[!CONTEXTUALHELP]
>id="ajo_message_push"
>title="Push message creation"
>abstract="Add your push message and start personalizing it with the Expression editor."

## Create a campaign and a push notification {#create-push--campaign}

To create a push notification, follow the steps below:

1. Access the **[!UICONTROL Campaigns]** menu, then click **[!UICONTROL Create campaign]**.

1. In the **[!UICONTROL Properties]** section, specify when you want to execute the campaign.

1. In the **[!UICONTROL Actions]** section, choose the **[!UICONTROL In-app message]** and the **[!UICONTROL App surface]** previously configured for your push notification. Then, click **[!UICONTROL Create]**. 

    [Learn more on Push configuration](../push/push-configuration.md).

1. From the **[!UICONTROL Properties]** section, edit your Campaign's **[!UICONTROL Title]** and **[!UICONTROL Description]**.

1. Click the **[!UICONTROL Select audience]** button to define the audience to target from the list of available Adobe Experience Platform segments. [Learn more](../segment/about-segments.md).

1. In the **[!UICONTROL Identity namespace]** field, choose the namespace to use in order to identify the individuals from the selected segment. [Learn more](../event/about-creating.md#select-the-namespace).

1. Campaigns are designed to be executed on a specific date or on a recurring frequency. Learn how to configure the **[!UICONTROL Schedule]** of your campaign in [this section](../campaigns/create-campaign.md#schedule). 

1. From the **[!UICONTROL Action triggers]** menu, choose the **[!UICONTROL Frequency]** of your push notification:

    * Once
    * Daily
    * Weekly
    * Monthly

You can now start designing your content with the **[!UICONTROL Edit content]** button. For more information on how to design your push notification, refer to [this page](../push/design-push.md).

## Validate your push notification{#push-preview}

Once your message content has been defined, you can use test profiles to preview and test it. If you inserted [personalized content](../personalization/personalize.md), you can check how this content is displayed in the message, leveraging test profile data.

To visualize how your push notification displays on mobile devices, click the **[!UICONTROL Simulate content]** tab. Learn more about content simulation in [this section](../design/preview.md).

You must also check alerts in the upper section of the editor.  Some of them are simple warnings, but others can prevent you from using the message. Learn more in [this section](alerts.md).

![](assets/push-alert-button.png)

**Related topics**

<!--
* [Understand push notification flow](../push/push-gs.md)
-->
* [Configure push channel](../push/push-gs.md)
* [Create a new message](get-started-content.md)
* [Add a message in a journey](../building-journeys/journeys-message.md)
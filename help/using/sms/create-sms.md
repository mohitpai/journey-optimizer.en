---
solution: Journey Optimizer
product: journey optimizer
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
>abstract="Add your text message and start personalizing it with the Expression editor."

>[!NOTE]
>
>In accordance with the industry standards and regulations, all SMS marketing messages must contain a way for the recipients to easily unsubscribe. To do this, SMS recipients can reply with opt-in and opt-out keywords. [Learn how to manage opt-out](../privacy/opt-out.md#sms-opt-out-management-sms-opt-out-management)

## Create an SMS message in a journey or campaign {#create-sms-journey-campaign}

To start personalizing your SMS message, follow these steps:

>[!BEGINTABS]

>[!TAB Add an SMS message to a Journey]

1. Open your journey then drag and drop an SMS activity from the Actions section of the palette.

    ![](assets/sms_create_1.png)

1. Provide basic information on your message (label, description, category), then choose the message surface to use.

    ![](assets/sms_create_2.png)

    For more information on how to configure a journey, refer to [this page](../building-journeys/journey-gs.md)

You can now start designing the content of your SMS message from the **[!UICONTROL Edit content]** button. [Design your SMS content](#sms-content)

>[!TAB Add an SMS message to a Campaign]

1. Create a new scheduled or API-triggered campaign, select **[!UICONTROL SMS]** as your action and choose the **[!UICONTROL App surface]** to use. [Learn more on SMS configuration](sms-configuration.md).

    ![](assets/sms_create_3.png)

1. Click **[!UICONTROL Create]**.

1. From the **[!UICONTROL Properties]** section, edit your Campaign's **[!UICONTROL Title]** and **[!UICONTROL Description]**.

    ![](assets/sms_create_4.png)

1. In the **[!UICONTROL Actions tracking]** section, specify if you want to track clicks on links in your SMS message.

1. Click the **[!UICONTROL Select audience]** button to define the audience to target from the list of available Adobe Experience Platform segments. [Learn more](../segment/about-segments.md).

1. In the **[!UICONTROL Identity namespace]** field, choose the namespace to use in order to identify the individuals from the selected segment. [Learn more](../event/about-creating.md#select-the-namespace).

    ![](assets/sms_create_5.png)

1. Campaigns are designed to be executed on a specific date or on a recurring frequency. Learn how to configure the **[!UICONTROL Schedule]** of your campaign in [this section](../campaigns/create-campaign.md#schedule). 

1. From the **[!UICONTROL Action triggers]** menu, choose the **[!UICONTROL Frequency]** of your SMS message:

    * Once
    * Daily
    * Weekly
    * Month
    
You can now start designing the content of your SMS message from the **[!UICONTROL Edit content]** button. [Design your SMS content](#sms-content)

>[!ENDTABS]

## Define your SMS content{#sms-content}

1. From the journey or campaign configuration screen, click the **[!UICONTROL Edit content]** button to configure the SMS content.

1. Click the **[!UICONTROL Message]** field to open the Expression editor.

    ![](assets/sms-content.png)

1. Use the Expression editor to define content and add dynamic content. You can use any attribute, such as the profile name or city. Learn more about [personalization](../personalization/personalize.md) and [dynamic content](../personalization/get-started-dynamic-content.md) in the Expression editor.

1. Click **[!UICONTROL Save]** and check your message in the preview. [Learn more](send-sms.md)

    ![](assets/sms-content-preview.png)

**Related topics**

* [Configure SMS channel](sms-configuration.md)
* [SMS report](../reports/journey-global-report.md#sms-global)
* [Add a message in a journey](../building-journeys/journeys-message.md)

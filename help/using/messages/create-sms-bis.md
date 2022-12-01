---
solution: Journey Optimizer
product: journey optimizer
title: Create an SMS message
description: Learn how to create an SMS message in Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
hide: yes
hidefromtoc: yes
---
# Create an SMS message {#create-sms-bis}

>[!NOTE]
>
>In accordance with the industry standards and regulations, all SMS marketing messages must contain a way for the recipients to easily unsubscribe. To do this, SMS recipients can reply with opt-in and opt-out keywords. 

## Create an SMS message in a journey or campaign

To start personalizing your SMS message, follow these steps:

>[!BEGINTABS]

>[!TAB Add an SMS message to a Journey]

1. Open your journey then drag and drop an SMS activity from the Actions section of the palette.

1. Provide basic information on your message (label, description, category), then choose the message surface to use.

    For more information on how to configure a journey, refer to.

You can now start designing the content of your SMS message from the **[!UICONTROL Edit content]** button. 

>[!TAB Add an SMS message to a Campaign]

1. Create a new scheduled or API-triggered campaign, select **[!UICONTROL SMS]** as your action and choose the **[!UICONTROL App surface]** to use.

1. Click **[!UICONTROL Create]**.

1. From the **[!UICONTROL Properties]** section, edit your Campaign's **[!UICONTROL Title]** and **[!UICONTROL Description]**.

1. In the **[!UICONTROL Actions tracking]** section, specify if you want to track clicks on links in your SMS message.

1. Click the **[!UICONTROL Select audience]** button to define the audience to target from the list of available Adobe Experience Platform segments. 

1. In the **[!UICONTROL Identity namespace]** field, choose the namespace to use in order to identify the individuals from the selected segment.

1. Campaigns are designed to be executed on a specific date or on a recurring frequency. Learn how to configure the **[!UICONTROL Schedule]** of your campaign in. 

1. From the **[!UICONTROL Action triggers]** menu, choose the **[!UICONTROL Frequency]** of your SMS message:

    * Once
    * Daily
    * Weekly
    * Month
    
You can now start designing the content of your SMS message from the **[!UICONTROL Edit content]** button.

>[!ENDTABS]

## Define your SMS content

1. From the journey or campaign configuration screen, click the **[!UICONTROL Edit content]** button to configure the SMS content.

1. Click the **[!UICONTROL Message]** field to open the Expression editor.

1. Use the Expression editor to define content and add dynamic content. You can use any attribute, such as the profile name or city. 

1. Click **[!UICONTROL Save]** and check your message in the preview.

1. When your SMS message is ready, complete the configuration of your to send it.

## Validate your SMS

>[!NOTE]
>
> For better deliverability, you should always use the phone numbers in the formats supported by the provider. For example, Twilio and Sinch only support phone numbers in E.164 format.

Once your message content has been defined, you can use test profiles to preview and test it. If you inserted, you can check how this content is displayed in the message, using test profile data.

To visualize how your SMS message displays on mobile devices, click the **[!UICONTROL Simulate content]** tab. Learn more about content simulation in.

You must also check alerts in the upper section of the editor.  Some of them are simple warnings, but others can prevent you from using the message. Learn more in.

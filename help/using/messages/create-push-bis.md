---
solution: Journey Optimizer
product: journey optimizer
title: Configure a push notification
description: Learn how to create a push notification in Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
hide: yes
hidefromtoc: yes
---
# Create a push notification {#create-push-notification-bis}

## Create the push notification in a journey or campaign {#create}

To create a push notification, follow the steps below:

>[!BEGINTABS]

>[!TAB Add a Push to a Journey]

1. Open your journey then drag and drop a Push activity from the Actions section of the palette.

1. Provide basic information on your message (label, description, category), then choose the message surface to use.

    For more information on how to configure a journey, refer to 

1. From the journey configuration screen, click the **[!UICONTROL Edit content]** button to configure the push content.

1. Once your message content has been defined, you can use test profiles to preview and test it. 

1. When your push is ready, complete the configuration of your to send it.

    To track the behavior of your recipients through push openings and/or interactions, make sure that the dedicated options in the tracking section are enabled in the .

>[!TAB Add a Push to a Campaign]

1. Create a new scheduled or API-triggered campaign, select **[!UICONTROL Push notification]** as your action and choose the **[!UICONTROL App surface]** to use.

1. Click **[!UICONTROL Create]**.

1. From the **[!UICONTROL Properties]** section, edit your Campaign's **[!UICONTROL Title]** and **[!UICONTROL Description]**.

1. Click the **[!UICONTROL Select audience]** button to define the audience to target from the list of available Adobe Experience Platform segments.

1. In the **[!UICONTROL Identity namespace]** field, choose the namespace to use in order to identify the individuals from the selected segment.

1. Campaigns are designed to be executed on a specific date or on a recurring frequency. Learn how to configure the **[!UICONTROL Schedule]** of your campaign in. 

1. From the **[!UICONTROL Action triggers]** menu, choose the **[!UICONTROL Frequency]** of your push notification:

    * Once
    * Daily
    * Weekly
    * Monthly

1. From the campaign configuration screen, click the **[!UICONTROL Edit content]** button to configure the push content.

1. Once your message content has been defined, you can use test profiles to preview and test it. 

1. When your push is ready, complete the configuration of your to send it.

    To track the behavior of your recipients through push openings and/or interactions, make sure that the dedicated options in the tracking section are enabled in the).

>[!ENDTABS]

## Rapid delivery mode {#rapid-delivery}

Rapid delivery mode, previously known as Burst mode in journeys, is a [!DNL Journey Optimizer] add-on that allows very fast push message sending in large volumes though campaigns.

Rapid delivery is used when delay in message delivery is business-critical, when you want to send an urgent push alert on mobile phones, for example a breaking news to users who have installed your news channel app.

For more information on performances when using Rapid delivery mode, refer to.

### Prerequisites {#prerequisites}

Rapid delivery messaging comes with the following requirements:

* Rapid delivery is available for **[!UICONTROL Scheduled]** campaigns only, and is not available for API-triggered campaigns,
* No personalization is allowed in the push message,
* The target audience must contain less than 30M profiles,
* You can execute up to 5 campaigns simultaneously using the Rapid delivery mode.

### Activate Rapid delivery mode

1. Create a push notification campaign and toggle on the **[!UICONTROL Rapid delivery]** option.

1. Configure the message content and select the audience to target.
    
    >[!IMPORTANT]
    >
    >Ensure that the message content does not include any personalization, and that the audience contains less than 30M profiles.

1. Review and activate your campaign as usual. Note that, in test mode, messages are not sent via the Rapid delivery mode.
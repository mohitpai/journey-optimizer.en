---
title: SMS configuration
description: Learn how to configure your environment to send SMS messages with Journey Optimizer
role: Admin
level: Intermediate
exl-id: 7099d44e-5d5d-4eef-9477-f68f4eaa1983
---
# Configure SMS channel {#sms-configuration}

[!DNL Journey Optimizer] allows you to create your journeys and send messages to targeted audience. 

## Create new API credential {#create-api}

To configure your SMS vendor with Journey Optimizer, follow these steps:

1. Access the **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL API Credentials]** menu, then click **[!UICONTROL Create API credential]**.

1. Select your **[!UICONTROL SMS vendor]**.

1. Enter a **[!UICONTROL Name]** for your API Credential.

1. Enter your **[!UICONTROL Service ID]** and **[!UICONTROL API Token]**. 

    >[!NOTE]
    >
    > Sinch requires special API credentials. To find your **[!UICONTROL Service ID]** and **[!UICONTROL API Token]**, access SMS > APIs menu from your Sinch account, 


## Create a message preset for SMS messages {#message-preset-sms}

Once your SMS channel has been configured, you need to create a message preset to be able to send SMS messages from **[!DNL Journey Optimizer]**.

Learn how to create and configure a message preset in [this section](message-presets.md).

You are now ready to send SMS messages with Journey Optimizer.

* Learn how to create an SMS message in [this page](../create-sms.md).
* Learn how to send add a message in a journey in [this section](../building-journeys/journeys-message.md).

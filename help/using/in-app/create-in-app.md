---
title: Create an In-app notification
description: Learn how to create an In-app message in Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
keywords: in-app, message, creation, start
badge: label="Beta" type="Informative"
exl-id: b3b79fe2-7db3-490d-9c3d-87267aa55eea
---
# Create an In-app message {#create-in-app}

>[!IMPORTANT]
>
>The In-app feature is currently available as a beta to select users only. 

## Create a campaign and an In-app message{#create-in-app-in-a-campaign}

To create an In-app message, follow the steps below:

1. Access the **[!UICONTROL Campaigns]** menu, then click **[!UICONTROL Create campaign]**.

1. In the **[!UICONTROL Properties]** section, specify when you want to execute the campaign.

1. In the **[!UICONTROL Actions]** section, choose the **[!UICONTROL In-app message]** and the **[!UICONTROL App surface]** previously configured for your In-app message. Then, click **[!UICONTROL Create]**. 

    [Learn more on In-app configuration](inapp-configuration.md).

    ![](assets/in_app_create_1.png)

1. From the **[!UICONTROL Properties]** section, edit your Campaign's **[!UICONTROL Title]** and **[!UICONTROL Description]**.

1. To assign custom or core data usage labels to the landing page, select **[!UICONTROL Manage access]**. [Learn more](../administration/object-based-access.md).

1. Click the **[!UICONTROL Select audience]** button to define the audience to target from the list of available Adobe Experience Platform segments. [Learn more](../segment/about-segments.md).

    ![](assets/in_app_create_2.png)

1. In the **[!UICONTROL Identity namespace]** field, choose the namespace to use in order to identify the individuals from the selected segment. [Learn more](../event/about-creating.md#select-the-namespace).

1. Choose the frequency of your trigger when your In-app message is active:

    * **[!UICONTROL Show every time]**: Always show the message when the events selected in the **[!UICONTROL Mobile app trigger]** drop-down occur.
    * **[!UICONTROL Show once]**: Only show this message the first time the events selected in the **[!UICONTROL Mobile app trigger]** drop-down occur.
    * **[!UICONTROL Show until click through]**: Show this message when the events selected in the **[!UICONTROL Mobile app trigger]** drop-down occur until an interact event is sent by the SDK with an action of "clicked".

1. From the **[!UICONTROL Mobile app trigger]** dropdown(s), choose the event(s) and criteria that will trigger your message:

    1. From the left drop-down, select the event required to trigger the message.
    1. From the right drop-down, select the validation required on the selected event.
    1. Click the **[!UICONTROL Add]** button if you want the trigger to consider multiple events or criteria. Then, repeat the steps above.
    1. Select how your events are linked, e.g. choose **[!UICONTROL And]** if you want **both** triggers to be true in order for a message to be shown or choose **[!UICONTROL Or]** if you want the message to be shown if **either** of the triggers are true.

    ![](assets/in_app_create_3.png)

1. Choose the event that triggers your message from the **[!UICONTROL Mobile app trigger]**
drop-down. 
    
    By choosing a trigger, you choose which user action causes the In-app message to display.

    ![](assets/in_app_create_3.png)

1. Campaigns are designed to be executed on a specific date or on a recurring frequency. Learn how to configure the **[!UICONTROL Schedule]** of your campaign in [this section](../campaigns/create-campaign.md#schedule). 

    ![](assets/in-app-schedule.png)

1. You can now start designing your content with the **[!UICONTROL Edit content]** button. 

    ![](assets/in_app_create_4.png)

## Send your In-App messages{#in-app-send}

### Preview on device {#preview-device}

You can preview the In-app notification in a specific device.

1. Click **[!UICONTROL Preview on device]**.

    ![](assets/in_app_create_6.png)

1. From the **[!UICONTROL Connect to device]** window, click **[!UICONTROL Start]**.

1. Type in the **[!UICONTROL Base URL]** of your application and click **[!UICONTROL Next]**.

    ![](assets/in_app_create_7.png)

1. Scan the QR code with your device and enter the PIN code displayed. 

Your In-app message can now be triggered directly on your device allowing you to preview and review your message on an actual device. 

### Review and activate your In-App notification{#in-app-review}

Once your In-App message is created, and its content defined and personalized, you can review and activate it.

To perform this, follow the steps below:

1. Use the **[!UICONTROL Review to activate]** button to display a summary of your message.

    The summary allows you to modify your campaign if necessary, and to check if any parameter is incorrect or missing.

    ![](assets/in_app_create_5.png)

1. Check that your campaign is correctly configured, then click **[!UICONTROL Activate]**.

Your campaign is now activated. The In-App notification configured in the campaign is sent immediately, or on the specified date.

Once sent, you can measure the impact of your In-App messages within the Campaign report. For more on reporting, refer to [this section](../reports/campaign-global-report.md#inapp-report).

**Related topics:**

* [Design In-app message](design-in-app.md)
* [In-app report](../reports/campaign-global-report.md#inapp-report)
* [In-app configuration](inapp-configuration.md)

## How-to video{#video}

The video below shows how to create, configure, and publish In-app messages in your campaigns.

>[!VIDEO](https://video.tv.adobe.com/v/3410430?quality=12&learn=on)

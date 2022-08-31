---
title: Create a campaign
description: Learn how to create campaigns in [!DNL Journey Optimizer]
feature: Overview
topic: Content Management
role: User
level: Intermediate
exl-id: 7c4afc98-0d79-4e26-90f8-558bac037169
---
# Create a campaign {#create-campaign}

>[!NOTE]
>
>Before creating a new campaign, make sure you have a surface channel (i.e. message preset) and an Adobe Experience Platform segment ready for use. Learn more in these sections:
>
>* [Create channel surfaces](../configuration/channel-surfaces.md) 
>* [Get started with segments](../segment/about-segments.md)

## Create your 1st campaign {#create}

1. Access the **[!UICONTROL Campaigns]** menu, then click **[!UICONTROL Create campaign]**.

    >[!NOTE]
    >
    >You can also duplicate an existing live campaign to create a new one. [Learn more](modify-stop-campaign.md#duplicate)

    ![](assets/create-campaign.png)

<!--1. In the **[!UICONTROL Properties]** section, specify when you want to execute the campaign:

    * **[!UICONTROL Scheduled]**: execute the campaign immediately or on a specified date. Scheduled campaigns are aimed at sending **marketing** type messages.
    * **[!UICONTROL API-triggered]**: execute the campaign using an API call. API-triggered campaigns are aimed at sending **transactional** messages, i.e. messages sent out following an action performed by an individual: password reset, card abandonment etc. [Learn how to trigger a campaign using APIs](api-triggered-campaigns.md)-->

1. In the **[!UICONTROL Actions]** section, choose the channel and the channel surface to use to send your message, then click **[!UICONTROL Create]**.

    A surface is a configuration which has been defined by a [System Administrator](../start/path/administrator.md). It contains all the technical parameters for sending the message, such as header parameters, subdomain, mobile apps, etc. [Learn more](../configuration/channel-surfaces.md).

    ![](assets/create-campaign-action.png)

    >[!NOTE]
    >
    >Only channel surfaces compatible with the marketing campaign type are listed in the drop-down list.

<!--Only channel surfaces compatible with the campaign type (marketing or transactional) are listed in the drop-down list.-->

1. Specify a title and a description for the campaign.

    <!--To test the content of your message, toggle the **[!UICONTROL Content experiment]** option on. This allows you to test multiple variables of a delivery on populations samples, in order to define which treatment has the biggest impact on the targeted population.[Learn more about content experiment](../campaigns/content-experiment.md).-->

1. In the **[!UICONTROL Actions]** section, configure the message to send with the campaign:

    1. Click the **[!UICONTROL Edit content]** button, then configure and design your message content. [Learn more on messages](../messages/get-started-content.md).

        Learn detailed steps to create your message content in the following page:

        * [Create an email](../messages/create-email.md)
        * [Create a push notifications](../messages/create-push.md)
        * [Create an SMS message](../messages/create-sms.md)

    1. Once your content is defined, use the **[!UICONTROL Simulate content]** button to preview and test your content with test profiles. [Learn more](../design/preview.md).

    1. Click the arrow to go back to the campaign creation screen.

        ![](assets/create-campaign-design.png)

    1. In the **[!UICONTROL Actions tracking]** section, specify if you want to track how your recipients react to your delivery: you can track clicks and/or opens.
        
        Tracking results will be accessible from the campaign report once the campaign has been executed. [Learn more on campaign reports](../reports/campaign-global-report.md)

1. Define the audience to target. To do this, click the **[!UICONTROL Select audience]** button to display the list of available Adobe Experience Platform segments. [Learn more on segments](../segment/about-segments.md)

    <!-- NOTE For API-triggered campaigns, the audience needs to be set via API call. [Learn more](api-triggered-campaigns.md)-->

    In the **[!UICONTROL Identity namespace]** field, choose the namespace to use in order to identify the individuals from the selected segment. [Learn more on namespaces](../event/about-creating.md#select-the-namespace)

    ![](assets/create-campaign-namespace.png)

    >[!NOTE]
    >
    >Individuals belonging to a segment that does not have the selected identity (namespace) among their different identities will not be targeted by the campaign.

    <!--If you are are creating an API-triggered campaign, the **[!UICONTROL cURL request]** section allows you to retrieve the **[!UICONTROL Campaign ID]** to use in the API call. [Learn more](api-triggered-campaigns.md)-->

1. To execute your campaign on a specific date or on a recurring frequency, configure the **[!UICONTROL Schedule]** section. [Learn how to schedule campaigns](#schedule)

Once your campaign is ready, you can review and publish it. [Learn more](#review-activate)

## Review and activate a campaign {#review-activate} 

Once your campaign has been configured, you need to review its parameter and content before activating it. To do this, follow these steps:

1. In the campaign configuration screen, click **[!UICONTROL Review to activate]** to display a summary of the campaign.

    The summary allows you to modify your campaign if necessary, and to check if any parameter is incorrect or missing.

    >[!IMPORTANT]
    >
    >In case of errors, you cannot activate the campaign. Resolve the errors before proceeding.

    ![](assets/create-campaign-alerts.png)

1. Check that your campaign is correctly configured, then click **[!UICONTROL Activate]**.

    ![](assets/create-campaign-review.png)

1. The campaign is now activated. Its status is **[!UICONTROL Live]**, or **[!UICONTROL Scheduled]** if you entered a start date. [Learn more on campaigns statuses](get-started-with-campaigns.md#statuses). 
    
    The message configured in the campaign is sent immediately or on the specified date.

    >[!NOTE]
    >
    >The **[!UICONTROL Completed]** status is automatically assigned to a campaign 3 days after it has been activated or at the campaign's end date if it has a recurring execution.
    >
    >If no end date has been specified, the campaign will keep the **[!UICONTROL Live]** status. To change it, you need to stop the campaign manually. [Learn how to stop a campaign](modify-stop-campaign.md) 

1. Once a campaign has been activated, you can check at any time its information by opening it. The summary allows you to get statistics about number of targeted profiles and delivered and failed actions.

    You can also get additional statistics in dedicated reports by clicking the **[!UICONTROL Reports]** button. [Learn more](../reports/campaign-global-report.md)

    ![](assets/create-campaign-summary.png)

## Schedule a campaign {#schedule}

By default, campaigns start once they have been activated manually, and end as soon as the message has been sent once.

You can define a frequency at which the campaign's message should be sent. To do this, use the **[!UICONTROL Action triggers]** options in the campaign creation screen to specify if the campaign should be executed daily, weekly, or monthly.

If you do not want to execute your campaign right after its activation, you can specify the a date and time at which the message should be sent using the **[!UICONTROL Campaign start]** option. The  **[!UICONTROL Campaign end]** option allows you to specify when a recurring campaign should stop being executed.

![](assets/create-campaign-schedule.png)

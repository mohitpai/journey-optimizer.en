---
solution: Journey Optimizer
product: journey optimizer
title: Get started with campaigns
description: Learn more about campaigns in Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Intermediate
keywords: campaign, how to , start, optimizer
exl-id: e2506a43-e4f5-48af-bd14-ab76c54b7c90
---
# Get started with campaigns {#get-started-campaigns}

>[!CONTEXTUALHELP]
>id="campaigns_list"
>title="Campaigns"
>abstract="Create campaigns to deliver one-time content to a specific segment across various channels. Before creating your campaign, make sure you have a channel surface (i.e. message preset) and an Adobe Experience Platform segment ready for use."

Use Journey Optimizer campaigns to deliver one-time content to a specific segment using various channels. When using journeys, actions are executed in sequence. With campaigns, actions are performed simultaneously, either immediately, or based on a specified schedule.

You can create two types of campaigns:

* **Scheduled campaigns** allow for simple ad-hoc batch communications for marketing use cases like promotional offers, engagement campaigns, announcements, legal notices, or policy updates.
* **API Triggered Campaigns** allow for simple transactional/operational messages with REST APIs (password reset, card abandonment, etc.), where the need may involve personalization using profile attributes and contextual data from payload.

The main steps to create a campaign are as follows:

![](assets/create-campaign-process.png)

➡️ [Discover this feature in video](#video)

## Before starting {#campaign-prerequisites}

Check the following prerequisites before starting creating your first campaign in Journey Optimizer:

1. **You need proper permissions**. Campaigns are only available to users with access to a campaign related **[!UICONTROL Product profile]** such as Campaign administrator, Campaign approver, Campaign manager and/or Campaign viewer. 
    
    If you cannot access campaigns, your permissions must be extended. If you have access to [Adobe Admin Console](https://adminconsole.adobe.com/){target="_blank"} for your organization, follow the steps below. If not, contact your Journey Optimizer Administrator.

    +++Learn how to assign campaign permissions

    To assign the corresponding **[!UICONTROL Product profile]** to your users:

    1. From [Adobe Admin Console](https://adminconsole.adobe.com/){target="_blank"}, select the [!DNL Adobe Experience Platform] product.

    1. Browse to the **[!UICONTROL Product profile]** tab, select one of the built-in campaign related **[!UICONTROL Product profile]**: Campaign administrator, Campaign approver, Campaign manager or Campaign viewer. 

        For more information on Journey Optimizer campaign **[!UICONTROL Product profiles]** and **[!UICONTROL Permissions]**, [refer to this page](../administration/ootb-product-profiles.md).

        ![](assets/do-not-localize/admin_1.png)

    1. Click **[!UICONTROL Add user]** to assign to your user the selected **[!UICONTROL Product profile]**.

        ![](assets/do-not-localize/admin_2.png)

    1. Type-in your user's name, group, or email address and click **[!UICONTROL Save]**.

    Your user is now able to access **[!UICONTROL Campaigns]**. 

    +++

1. **You need an audience**. Audience segments need to be available before creating the campaign. Learn more about audience creation [in this page](../segment/about-segments.md).
1. **You need a channel surface**. To be able to select a channel, you must have the corresponding channel surface (i.e preset) created and available. Learn more about channel surfaces [in this page](../configuration/channel-surfaces.md).

## How-to video {#video}

Learn how to create your first campaign.

>[!VIDEO](https://video.tv.adobe.com/v/346680?quality=12)

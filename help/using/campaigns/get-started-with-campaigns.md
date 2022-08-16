---
title: Get started with campaigns
description: Learn more about campaigns in [!DNL Journey Optimizer]
feature: Overview
topic: Content Management
role: User
level: Intermediate
hide: yes
hidefromtoc: yes
exl-id: e2506a43-e4f5-48af-bd14-ab76c54b7c90
---
# Get started with campaigns {#get-started-campaigns}

>[!CONTEXTUALHELP]
>id="campaigns_list"
>title="Campaigns"
>abstract="With Campaigns, you can deliver one-time content to a specific segment across multiple channels. Before creating a new campaign, make sure you have a channel surface (i.e. message preset) and an Adobe Experience Platform segment ready for use."

## About campaigns {#about}

Campaigns allow you to deliver one-time content to a specific segment using multiple channels. Unlike journeys, where actions are designed to be executed in sequence, campaigns execute actions simultaneously, either immediately, or on a specified schedule. 

You can create two types of campaigns:

* **Scheduled campaigns** allow for simple ad-hoc batch communications for marketing use cases like promotional offers, engagement campaigns, announcements, legal notices, or policy updates.
* **API Triggered Campaigns** allow for simple transactional/operational messages with REST APIs (password reset, card abandonment, etc.), where the need may involve personalization using profile attributes and contextual data from payload.

Learn how to work with campaigns:
* [Create a campaign](create-campaign.md)
* [Create API-triggered campaigns](api-triggered-campaigns.md)
* [Modify or stop a campaign](modify-stop-campaign.md)
* [Campaign live report](campaign-live-report.md)
* [Campaign global report](campaign-global-report.md)

## Access campaigns {#access}

Campaigns are accessible from the **[!UICONTROL Campaigns]** menu.

By default, the list shows all campaigns with the **[!UICONTROL Draft]**, **[!UICONTROL Scheduled]**, and **[!UICONTROL Live]** statuses. To display stopped, completed and archived campaigns, you need to clear the filter.

![](assets/create-campaign-list.png)

## Campaign statuses {#statuses}

Campaigns can have multiple statuses:

* **[!UICONTROL Draft]**: The campaign is being edited, it has not been activated.
* **[!UICONTROL Activating]**: The campaign is being activated.
* **[!UICONTROL Live]**: The campaign has been activated.
* **[!UICONTROL Scheduled]**: The campaign has been configured to be activated on a specific start date.
* **[!UICONTROL Stopped]**: The campaign has been stopped manually. You cannot activate or reuse it anymore (see [Stop a campaign](modify-stop-campaign.md#stop))
* **[!UICONTROL Completed]**: The campaign is complete.
* **[!UICONTROL Archived]**: The campaign has been archived.

>[!NOTE]
>
>The "Open draft version" icon next to a **[!UICONTROL Live]** or **[!UICONTROL Scheduled]** status indicates that a new version of the campaign has been created and has not been activated yet (see [Modify a campaign](modify-stop-campaign.md#modify)).

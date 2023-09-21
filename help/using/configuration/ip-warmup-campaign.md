---
solution: Journey Optimizer
product: journey optimizer
title: Create IP warmup campaigns
description: Learn how to create an IP warmup campaign
feature: Application Settings
topic: Administration
role: Admin
level: Experienced
keywords: IP, pools, group, subdomains, deliverability
hide: yes
hidefromtoc: yes

---
# Create IP warmup campaigns {#create-ip-warmup-campaign}

>[!CONTEXTUALHELP]
>id="ajo_campaign_ip_warmup"
>title="Activate the IP warmup plan option"
>abstract="Select the IP warmup plan activation option. Once the campaign is live, it can be associated with an IP warmup plan."

>[!BEGINSHADEBOX]

What you'll find in this documentation guide:

* [Get started with IP warmup](ip-warmup-gs.md)
* **[Create IP warmup campaigns](ip-warmup-campaign.md)**
* [Create an IP warmup plan](ip-warmup-plan.md)
* [Run the IP warmup plan](ip-warmup-running.md)

>[!ENDSHADEBOX]

You need to create one or more campaigns with a specific option enabled so that they can be used in an IP warmup plan.

To create an IP warmup campaign, follow the steps below.

1. Create an email [surface](channel-surfaces.md) for the domain and the IPs that you have identified for your warmup plan.<!--how do you identify these or who does it at the customer level?-->

    >[!NOTE]
    >
    >Learn how to select the domain and IPs to use in an email surface in [this section](using/email/email-settings.md#subdomains-and-ip-pools).

1. Create a [campaign](../campaigns/create-campaign.md) and select the [Email](../email/create-email.md#create-email-journey-campaign) action.

1. Select the surface that you created for IP warmup.

    ![](assets/ip-warmup-campaign-surface.png)

    <!--You must use the same surface as the one that will be used for the asociated IP warmup plan. [Learn how to create an IP warmup plan](#create-ip-warmup-plan)-->

1. Click **[!UICONTROL Create]**.

1. From the **[!UICONTROL Schedule]** section, select **[!UICONTROL IP warmup plan activation]**.

    ![](assets/ip-warmup-campaign-plan-activation.png)

    The campaign [schedule](../campaigns/create-campaign.md#schedule) will be driven by the [IP warmup plan](ip-warmup-plan.md) it will be associated with, meaning that the schedule is not defined any more in the campaign itself.

1. [Activate](../campaigns/review-activate-campaign.md) the campaign. Once live, it is ready for use in an IP warmup plan.

>[!NOTE]
>
>For a live campaign with IP warmup plan activated, the **[!UICONTROL Delete]** button is available until it is associated with an IP warmup plan.

For more information on how to configure a campaign, refer to [this page](../campaigns/get-started-with-campaigns.md).


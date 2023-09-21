---
solution: Journey Optimizer
product: journey optimizer
title: Create an IP warmup plan
description: Learn how to create an IP warmup plan
feature: Application Settings
topic: Administration
role: Admin
level: Experienced
keywords: IP, pools, group, subdomains, deliverability
hide: yes
hidefromtoc: yes

---
# Create an IP warmup plan {#ip-warmup}

>[!BEGINSHADEBOX]

What you'll find in this documentation guide:

* [Get started with IP warmup](ip-warmup-gs.md)
* [Create IP warmup campaigns](ip-warmup-campaign.md)
* **[Create an IP warmup plan](ip-warmup-plan.md)**
* [Run the IP warmup plan](ip-warmup-running.md)

>[!ENDSHADEBOX]

Once you [created one or more campaigns](ip-warmup-campaign.md) with a dedicated surface and the IP warmup option enabled, you can start creating your IP warmup plan.

## Access and manage IP warmup plans {#manage-ip-warmup-plans}

1. Access the **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL IP warmup plans]** menu. All the IP warmup plans created so far are displayed.

    ![](assets/ip-warmup-filter-list.png)

1. You can filter on the status. The different statuses are:

    * **Not started**: no run has happened
    * **In progress**: as soon as one run has started <!--or is done?-->
    * **Paused**
    * **Completed**: all the runs in the plan are done

1. To delete an IP warmup plan, select the **[!UICONTROL Delete]** icon next to a list item and confirm deletion.

    ![](assets/ip-warmup-delete-plan.png)

    >[!CAUTION]
    >
    >The selected IP warmup plan will be permanently deleted.

## Create an IP warmup plan {#create-ip-warmup-plan}

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_upload"
>title="Specify your IP warmup plan"
>abstract="Download the CSV template and fill it with data for IP warmup phases and target number of profiles."

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_surface"
>title="Select a marketing surface"
>abstract="You must select the same surface as the one selected in the campaign you want to associate with your IP warmup plan."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/channel-surfaces.html" text="Set up channel surfaces"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/channel-surfaces.html" text="Create IP warmup campaigns"

When one or more live campaigns with the **[!UICONTROL IP warmup plan activation]** option enabled are activated, you can associate them with an IP warmup plan.

>[!CAUTION]
>
>To create, edit and delete the IP warmup plans, you must have the **[!UICONTROL Deliverability Consultant]** permission. <!--Learn more on managing [!DNL Journey Optimizer] users' access rights in [this section](../administration/permissions-overview.md).-->
>
>Work with your deliverability consultant to make sure your IP warmup plan template is correctly set up. <!--TBC-->

1. Access the **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL IP warmup plans]** menu, then click **[!UICONTROL Create IP warmup plan]**.

    ![](assets/ip-warmup-create-plan.png)

1. Fill in the IP warmup plan details: give it a name and a description.

    ![](assets/ip-warmup-plan-details.png)

1. Select a [surface](channel-surfaces.md). Only marketing surfaces are available for selection. [Learn more on email type](../email/email-settings.md#email-type)

    >[!CAUTION]
    >
    >You must select the same surface as the one selected in the campaign you want to associate with your IP warmup plan. [Learn how to create an IP warmup campaign](#create-ip-warmup-campaign)

1. Upload the Excel file containing your IP warmup plan<!--which formats are allowed?-->. You can use the template provided by the deliverability team.<!--TBC?--> [Learn more](#upload-plan)
    <!--
    You can also download the Excel template from the [!DNL Journey Optimizer] user interface and upload it after filling it with the IP warmup details.-->

    ![](assets/ip-warmup-upload-success.png)

1. Click **[!UICONTROL Create]**. The number of phases defined in the file you uploaded are automatically displayed will all the runs for each phase. [Learn more](#upload-plan)

    ![](assets/ip-warmup-plan-phases.png)

### Re-upload an IP warmup plan {#re-upload-plan}

You can re-upload another IP warmup plan using the corresponding button.

![](assets/ip-warmup-re-upload-plan.png)

>[!NOTE]
>
>The IP warmup plan details will change as per the newly uploaded file. The complete runs and the activated runs are not be affected.

### Upload the file containing the plan {#upload-plan}

Below is an example of a file containing an IP warmup plan.

![](assets/ip-warmup-sample-file.png)

Each phase correspond to a period composed of several runs, to which you will assign a single campaign.

For each run, you have a certain number of recipients and you will define a date when this run will be executed.

You can have as many columns as you want for the domains you want to deliver to. In this example, you have three columns: Gmail, Adobe and Others, meaning that

The idea is to have more runs in the first phases and to progressively increase the number of targeted addresses while reducing the number of runs.

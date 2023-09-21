---
solution: Journey Optimizer
product: journey optimizer
title: Run the IP warmup plan
description: Learn how to run and monitor an IP warmup plan
feature: Application Settings
topic: Administration
role: Admin
level: Experienced
keywords: IP, pools, group, subdomains, deliverability
hide: yes
hidefromtoc: yes

---
# Run the IP warmup plan {#ip-warmup-running}

>[!BEGINSHADEBOX]

What you'll find in this documentation guide:

* [Get started with IP warmup](ip-warmup-gs.md)
* [Create IP warmup campaigns](ip-warmup-campaign.md)
* [Create an IP warmup plan](ip-warmup-plan.md)
* **[Run the IP warmup plan](ip-warmup-running.md)**

>[!ENDSHADEBOX]

## Define the phases {#define-phases}

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_campaigns_excluded"
>title="Select campaigns audiences to exclude"
>abstract="Select the audiences from other campaigns that you want to exclude from the current phase."

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_domains_excluded"
>title="Select domain groups to exclude"
>abstract="Select the domains that you want to exclude from the current phase."

You need to associate the campaign and audience at phase level and turns on some settings as needed for all runs associated with a single creative/campaign

At phase level, system ensures that previously targeted + new profiles are picked up AND at iteration level, system ensures that each run is having unique profiles and the count matches what is stated in plan

1. For each phase, select the campaign you want to associate with this phase of the IP warmup plan.

    ![](assets/ip-warmup-plan-select-campaign.png)

    Note the following:

    * Only the campaigns with the **[!UICONTROL IP warmup plan activation]** option enabled <!--and live?--> are available for selection. [Learn more](#create-ip-warmup-campaign)
    
    * You must select a campaign that uses the same surface as the one selected for the current IP warmup plan.

    * You cannot select a campaign that is already in use in another IP warmup campaign.

1. For each phase, the following applies:

    * **[!UICONTROL Profile exclusion]** - The profiles from the previous runs of that phase are always excluded. For example, if on run #1 Leo got covered in the first 6300 people being targeted, the system will automatically ensure that Leo doesn't get the mail in run #2.

    * **[!UICONTROL Campaign audiences excluded]** - Select the audiences from other <!--executed/live?-->campaigns that you want to exclude from the current phase.

        For example, you may be executing a phase and had to split it for any reason. In such a case, in phase 2, you would like to include the campaign used in phase 1 in this section so that in phase 2, previously contacted people from phase 1 are not included. This can be done not just with campaigns used in same IP warmup plan but also from another IP warmup plan too.

    * **[!UICONTROL Domains groups excluded]** - Select the domains you want to exclude from that phase, for example Gmail. <!--??-->

        After running IP warmup for some days, you realize that ISP reputation with a domain say hotmail is not good and you wish to resolve it with ISP but do not wish to stop IP warmup plan. In such a case, you may put the domain group hotmail in excluded category.

        >[!NOTE]
        >
        >Domain exclusion requires a non-executed phase so you may have to split a running phase to add excclusions. Similarly, if domain group is not an OOTB domain group, then you may have to create domain group in Excel and upload and then exclude the same.

    ![](assets/ip-warmup-plan-phase-1.png)

1. You can add a phase if needed - it will be added after the last current phase. Use the **[!UICONTROL Delete phase]** button to remove any unwanted phase.

    ![](assets/ip-warmup-plan-add-delete-phases.png)

    >[!CAUTION]
    >
    >You cannot undo the **[!UICONTROL Delete]** action.
    >
    >If you delete all the phases from the IP warmup plan, we recommend to re-upload a plan.

## Define the runs {#define-runs}

1. Select a schedule for each run. <!--which is actually a window of opportunity. meaning? how many hours? shall we specify that to clarify?-->

    ![](assets/ip-warmup-plan-send-time.png)

1. Select an end time, which basically means the window within which we can execute warmup campaign in case there is any delays in audience job. If not specified, we will attempt at start time and fail. If end time is provided, we will execute the run between that window.

1. Activate each run. Make sure you schedule a time early enough to allow for the segmentation job to be run. <!--explain how you can evaluate a proper time-->

    >[!CAUTION]
    >
    >Each run must be activated at least 12 hours before the actual send time. Otherwise, segmentation may not be completed. <!--How do you know when segmentation is complete? Is there a way to prevent user from scheduling less than 12 hours before the segmentation job?-->

<!--Sart to execute on every day basis by simply clicking the play button > for each run? do you have to come back every day to activate each run? or can you schedule them one after the other?)-->

1. If the campaign execution has not started, you can stop a run.<!--why?-->

    Once the campaign execution has started, the **[!UICONTROL Stop]** button becomes unavailable. <!--TBC in UI-->

    ![](assets/ip-warmup-plan-stop-run.png)

1. To add a run, select **[!UICONTROL Add a run below]** from the three dots icon.

    ![](assets/ip-warmup-plan-run-more-actions.png)

1. At any point, if you want to use a different campaign starting from a specific run, select the **[!UICONTROL Split to a new phase option]** from the three dots icon. A new phase is created for the remaining runs of the current phase. Follow the steps [above](#define-phases) to define the new phase.

    For example, if you select this option for run #4, runs #4 to #8 will be moved to a new phase.

<!--
You don't have to decide the campaign upfront. You can do a split later. It's a work in progress plan: you activate one run at a time with a campaign and you always have the flexibility to modify it while working on it.

But need to explain in which case you want to modify campaigns, provide examples
-->

## Monitor the plan

A run can have the following statuses<!--TBC with Medha-->:

* **[!UICONTROL Completed]**: 
* **[!UICONTROL Failed]**:
* **[!UICONTROL Cancelled]**: you stopped the run before the campaign execution has started.

Benefits :

* Reports will continue to show up at campaign level with similar capabilities as today. But the IP warmup plan also serves as a consolidated report at one single place of how many executions were done and so on.

* Single place to manage and view how IP warm is progressing.

* Consolidated report at creative/campaign level as all runs for a phase 
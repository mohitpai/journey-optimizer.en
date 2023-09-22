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

1. In the **[!UICONTROL Profile exclusion]** section, you can see that the profiles from the previous runs of that phase are always excluded. For example, if in Run #1 a profile got covered in the first 4800 people being targeted, the system will automatically ensure that the same profile doesn't receive the email in Run #2.

1. From the **[!UICONTROL Campaign audiences excluded]** section, select the audiences from other <!--executed/live?-->campaigns that you want to exclude from the current phase.

    ![](assets/ip-warmup-plan-exclude-campaigns.png)

    For example, while executing Phase 1, you had to [split it](#split-phase) for any reason. Therefore, you can exclude the campaign used in Phase 1 so that previously contacted profiles from Phase 1 are not included in Phase 2. You can also exclude campaigns from other IP warmup plans.

1. From the **[!UICONTROL Domains groups excluded]** section, select the domains you want to exclude from that phase.

    ![](assets/ip-warmup-plan-exclude-domains.png)

    For example, after running IP warmup for some days, you realize that ISP reputation with a domain (i.e. Adobe) is not good and you wish to resolve it without stopping your IP warmup plan. In such a case, you can exclude the Adobe domain group.

    >[!NOTE]
    >
    >Domain exclusion requires a non-executed phase, so you may have to split a running phase to add exclusions. Similarly, if domain group is not an OOTB domain group, you need to add this domain group to the Excel file, upload it and then exclude the domain.

    ![](assets/ip-warmup-plan-phase-1.png)

1. You can add a phase if needed. It will be added after the last current phase.

1. Use the **[!UICONTROL Delete phase]** button to remove any unwanted phase.

    ![](assets/ip-warmup-plan-add-delete-phases.png)

    >[!CAUTION]
    >
    >You cannot undo the **[!UICONTROL Delete]** action.
    >
    >If you delete all the phases from the IP warmup plan, we recommend to re-upload a plan.

## Define the runs {#define-runs}

1. Select a schedule for each run. <!--which is actually a window of opportunity. meaning? how many hours? shall we specify that to clarify?-->

    ![](assets/ip-warmup-plan-send-time.png)

1. Select an end time, which defines the window within which the IP warmup campaign can be executed in case there is any delays in audience segmentation job execution. If no end time is specified, the execution is attempted at the start time and will fail if the segmentation was not completed.

1. Activate each run. Make sure you schedule a time early enough to allow for the segmentation job to be run. <!--explain how you can evaluate a proper time-->

    >[!CAUTION]
    >
    >Each run must be activated at least 12 hours before the actual send time. Otherwise, segmentation may not be completed. <!--How do you know when segmentation is complete? Is there a way to prevent user from scheduling less than 12 hours before the segmentation job?-->

    <!--Sart to execute on every day basis by simply clicking the play button > for each run? do you have to come back every day to activate each run? or can you schedule them one after the other?)-->

1. If the campaign execution has not started, you can stop a run.<!--why?-->

    >[!NOTE]
    >
    >Once the campaign execution has started, the **[!UICONTROL Stop]** button becomes unavailable. <!--TBC in UI-->

    ![](assets/ip-warmup-plan-stop-run.png)

1. To add a run, select **[!UICONTROL Add a run below]** from the three dots icon.

    ![](assets/ip-warmup-plan-run-more-actions.png)

## Split a phase {#split-phase}

At any point, if you want to use a different campaign starting from a specific run, select the **[!UICONTROL Split to a new phase option]** from the three dots icon.

A new phase is created for the remaining runs of the current phase. Follow the steps [above](#define-phases) to define the new phase.

For example, if you select this option for Run #4, Runs #4 to #8 will be moved to a new phase.

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
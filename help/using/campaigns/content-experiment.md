---
title: Create a Content Experiment
description: Learn how to create a content experiment in your campaigns
feature: Overview
topic: Content Management
role: User
level: Beginner
hide: yes
hidefromtoc: yes
exl-id: bd35ae19-8713-4571-80bc-5f40e642d121
---
# Create a content experiment {#content-experiment}

>[!AVAILABILITY]
>
>The **Content Experiment** feature is currently only available for a set of organizations (Limited Availability). For more information, contact your Adobe representative.

Use Journey Optimizer Content Experiment to define multiple delivery treatments. The audience of interest is randomly allocated to each treatment in order to determine which one performs best with respect to the metric of interest. You can choose to vary the email’s content, subject, or sender. 

>[!NOTE]
>
>Before starting with Content Experiment, make sure that your reporting configuration is set for your custom datasets. Learn more in [this section](reporting-configuration.md).

In the example below, the delivery target has been split into two groups, each representing 45% of the targeted population, and a holdout group of 10%, who will not receive the delivery.

Each person in the targeted audience will receive one version of the email, with a subject line that is one of the following two:

* one directly promoting a 10% offer on the new collection and an image.
* the other one only advertising a special offer without specifying the 10% off without any image. 

The goal here is to see if recipients will interact with the email depending on the received experiment. We therefore will choose **[!UICONTROL Email Opens]** as the primary goal metric in this Content Experiment.

![](assets/content_experiment.png)

## Create your campaign {#campaign-experiment}

1. From the **[!UICONTROL Campaigns]** page, click **[!UICONTROL Create campaign]**.

    ![](assets/content_experiment_1.png)

1. Select **[!UICONTROL Email]** then the **[!UICONTROL Surface]** you want to use for this delivery. For more on this, refer to the [Channel surfaces](../configuration/channel-surfaces.md) page.

    ![](assets/content_experiment_2.png)

1. Click **[!UICONTROL Create]**.

1. Set up the **[!UICONTROL Properties]** of your delivery:
    * **[!UICONTROL Title]**
    * **[!UICONTROL Description]**
    * **[!UICONTROL Category]**: **[!UICONTROL Marketing]** / **[!UICONTROL Transactional]**

1. To start your content experiment, toggle the **[!UICONTROL Content experiment]** option. The **[!UICONTROL Content experiment]** menu appears.

    ![](assets/content_experiment_3.png)

1. Set up the **[!UICONTROL Audience]** and **[!UICONTROL Schedule]** parameters for your deliveries. [Learn more](create-campaign.md)

1. Click **[!UICONTROL Edit content]** to start personalizing your different **[!UICONTROL Treatments]**.

    ![](assets/content_experiment_4.png)

## Create your treatments {#treatment-experiment}

1. From the **[!UICONTROL Edit content]** window, add the **[!UICONTROL Subject line]** for your Treatment A email and click **[!UICONTROL Save]**.

    For this treatment, we specify the offer directly in the subject line.

    ![](assets/content_experiment_5.png)

1. Click **[!UICONTROL Email designer]** to start personalizing your deliveries. 

    ![](assets/content_experiment_6.png)

1. After designing your email, click **[!UICONTROL Save]** and get back to the **[!UICONTROL Edit content]** window to create Treatment B. 

1.  From the **[!UICONTROL More actions]** button, click **[!UICONTROL Duplicate]**. 

    You can also choose to start a new treatment from scratch clicking the **[!UICONTROL Content experiment]** button to access the advanced options then **[!UICONTROL Add treatment]**.

    ![](assets/content_experiment_7.png)

1. Change the **[!UICONTROL Title]** of your treatment to better differentiate them.

    ![](assets/content_experiment_8.png)

1. Select the email delivery linked to your newly created **[!UICONTROL Treatment]**.

1. Add the **[!UICONTROL Subject line]** for your delivery. 

    For this treatment, we choose to not specify the offer in the **[!UICONTROL Subject line]**.

    ![](assets/content_experiment_9.png)

1. Click **[!UICONTROL Email designer]** to further personalize the Treatment B delivery if needed.

Once your treatments are personalized, you can start configuring your Content Experiment.

## Configure your Content Experiment {#configure-experiment}

1. When both deliveries are personalized, from the **[!UICONTROL Edit content]** window, select **[!UICONTROL Configure content experiment]**.

    ![](assets/content_experiment_10.png)

1. Select the objectives you want to set for your experiment.

    For our experiment, we select **[!UICONTROL Email open]** to test if recipients will open their emails if the promo code is in the subject line.

    ![](assets/content_experiment_11.png)

1. Choose to add a **[!UICONTROL Holdout]** group to your delivery. This group will not receive any content from this campaign. 

    Switching on the toggle bar will automatically take 10% of your population, you can adjust this percentage if needed.

    ![](assets/content_experiment_12.png)

1. You can then choose to allocate a precise percentage to each **[!UICONTROL Treatment]** or simply switch on the **[!UICONTROL Distribute evenly]** toggle bar.

    ![](assets/content_experiment_13.png)

1. Click **[!UICONTROL Save]** when your configuration is set.

1. When your content experiment is ready, you can click **[!UICONTROL Review to activate]** to display a summary of the campaign. Alerts display if any parameter is incorrect or missing.

    ![](assets/content_experiment_15.png)

1. Check that your campaign is correctly configured, then click **[!UICONTROL Activate]** to launch it.

    ![](assets/content_experiment_14.png)

After configuring your experimentation and campaign, you can follow the success of your delivery with the Campaign report.

## Objectives report {#objectives-global}

>[!AVAILABILITY]
>
>The Content experiment feature is currently only available for a set of organizations (Limited Availability). For more information, contact your Adobe representative.

![](assets/performance_report.gif)

The **[!UICONTROL Objectives]** tab of your Campaign report allows you to better fine-tune your deliveries' reports by targeting one specific metric.

The **[!UICONTROL Objectives]** listed are linked to **[!UICONTROL Datasets]** that define a connection to a system in order to retrieve additional information. A list of built-in **[!UICONTROL Objectives]** is available but you can add your own by adding new **[!UICONTROL Dataset]**. For the detailed procedure, refer to this [section](reporting-configuration.md).

After selecting the Objectives you want to target on, the two **[!UICONTROL Performance overview]** and **[!UICONTROL Campaign objective]** widgets will provide a detailed summary of your delivery performance. 

With the **[!UICONTROL Campaign objective]** widget, you can also choose to compare your main objective with another metric.

Note that each widget can be resized and deleted if needed. For more information on this, refer to this [section](../reports/global-report.md#modify-dashboard).

## Experimentation report {#experimentation-global}

>[!AVAILABILITY]
>
>The Content experiment feature is currently only available for a set of organizations (Limited Availability). For more information, contact your Adobe representative.

![](assets/experimentation_report_3.png)

From your Campaign **[!UICONTROL Global report]**, the **[!UICONTROL Experimentation]** tab details the main information relative to how each variant is performing and if there is a best performer.

Note that defining the best performer might take some time, it will be represented by this icon ![](assets/experimentation_report_1.png).

The **[!UICONTROL Experiment result]** widget details the performance of each variant. You can change your baseline by selecting one of the treatment from the **[!UICONTROL Baseline]** the drop-down. The best treatment will be represented with a star icon.

The table presents the following metrics:

* **[!UICONTROL Profiles]**: Number of profiles targeted for this treatment.

*  **[!UICONTROL Unique outbound clicks]**: Total count of clicks across outbound channels.

*  **[!UICONTROL Count per profile]**: Total value of the Experiment objective metric divided by the number of profiles.

*  **[!UICONTROL Confidence interval]**: Percentage difference in performance between the baseline and the best performing treatment. [Learn more](../campaigns/experiment-calculations.md#confidence-intervals).

*  **[!UICONTROL Average lift]**: Percentage improvement in conversion rate of a given treatment over the baseline. [Learn more](../campaigns/experiment-calculations.md#understand-lift)

*  **[!UICONTROL Confidence]**: Evidence that a given treatment is the same as the baseline treatment. [Learn more](../campaigns/experiment-calculations.md#understand-confidence)

For a deep-dive in these results and how to interpret them, refer to [this page](../campaigns/get-started-experiment.md#interpret-results).

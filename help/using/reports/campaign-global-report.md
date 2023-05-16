---
solution: Journey Optimizer
product: journey optimizer
title: Campaign Global report
description: Learn how to use data from the Campaign Global report
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: fa64f5b8-75f2-40e6-8566-5766fafe6cd6
---
# Campaign global report {#campaign-global-report}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_report"
>title="Campaign global report"
>abstract="The Campaign global report allows to measure the impact of your campaigns over a selected time period. Your report is divided into different widgets detailing your campaign's success and errors. Each reporting dashboard can be modified by resizing or removing widgets."

Campaign global report can be accessed directly from your Campaign with the **[!UICONTROL View report]** button.

![](assets/campaign_report_global_5.png)

The Campaign **[!UICONTROL Global report]** page will be displayed with the following tabs:

* [Campaign](#campaign-global)
* [Email](#email-global)
* [In-app](#inapp-global)
* [Push](#push-global)
* [SMS](#sms-global)
* [Web](#web-tab)

The Campaign **[!UICONTROL Global report]** is divided into different widgets detailing your campaign's success and errors. Each widget can be resized and deleted if needed. For more information on this, refer to this [section](../reports/global-report.md#modify-dashboard).

For a detailed list of every metric available in Adobe Journey Optimizer, refer to [this page](global-report.md#list-of-components-global.md)

## Campaign tab {#campaign-global}

### Delivery {#delivery-global}

![](assets/campaign_report_global_1.png)

The **[!UICONTROL Campaign's Statistics]** widget details the main information relative to your campaign:

* **[!UICONTROL Entered profiles]**: Number of profiles who started the journey.

* **[!UICONTROL Actions delivered]**: Total number of unique times an action in the journey has been delivered.

* **[!UICONTROL Actions failed in %]**: Total number of unique times an action failed in the journey compared to the total number of unique times an action has been delivered.

### Objectives report {#objectives-global}

![](assets/performance_report.gif)

The **[!UICONTROL Objectives]** tab allows you to better fine-tune your deliveries' reports by targeting one specific metric.

The **[!UICONTROL Objectives]** listed are linked to **[!UICONTROL Datasets]** that define a connection to a system in order to retrieve additional information. A list of built-in **[!UICONTROL Objectives]** is available but you can add your own by adding new **[!UICONTROL Dataset]**. For the detailed procedure, refer to this [section](../campaigns/reporting-configuration.md).

After selecting the Objectives you want to target on, the two **[!UICONTROL Performance overview]** and **[!UICONTROL Campaign objective]** widgets will provide a detailed summary of your delivery performance. 

With the **[!UICONTROL Campaign objective]** widget, you can also choose to compare your main objective with another metric.

### Experimentation report {#experimentation-global}

![](assets/experimentation_report_3.png)

The **[!UICONTROL Experimentation]** tab provides key insights into the performance of each variant, and identifies the most successful one.

Note that defining the best performer might take some time, it will be represented by this icon ![](assets/experimentation_report_1.png).

+++Learn more on the different metrics and widgets available for the Experimentation report.

The **[!UICONTROL Experiment result]** widget details the performance of each variant. You can change your baseline by selecting one of the treatment from the **[!UICONTROL Baseline]** the drop-down. The best treatment will be represented with a star icon.

The table presents the following metrics:

* **[!UICONTROL Lift over baseline]**: Measure of the percentage improvement in conversion rate of a given treatment over the baseline.

*  **[!UICONTROL Confidence]**: Evidence that a given treatment is the same as the baseline treatment. [Learn more](../campaigns/experiment-calculations.md#understand-confidence)

*  **[!UICONTROL Unique outbound clicks]**: Total count of clicks across outbound channels.

* **[!UICONTROL Profiles]**: Number of profiles targeted for this treatment.

*  **[!UICONTROL Unique outbound clicks/profiles]**: Total value of the Success metric, previously selected when creating your Experiments, divided by the number of profiles.

The **[!UICONTROL Confidence interval]** graph measures uncertainty around improvement. It details the percentage difference in performance between the baseline and the best performing treatment. [Learn more](../campaigns/experiment-calculations.md#confidence-intervals). 
+++

For a deep-dive in these results and how to interpret them, refer to [this page](../campaigns/get-started-experiment.md#interpret-results).

## Email tab {#email-global}

![](assets/campaign_report_global_2.png)

From your Campaign **[!UICONTROL Global report]**, the **[!UICONTROL Email]** tab details the main information relative to the email deliveries sent in your Campaign.

+++Learn more on the different metrics and widgets available for the Email report.

The **[!UICONTROL Email Sending Statistics]** graph details the success of your delivery:

* **[!UICONTROL Targeted]**: Total number of messages processed during the delivery analysis.

* **[!UICONTROL Sent]**: Total number of sends for the delivery.

* **[!UICONTROL Delivered]**: Number of messages successfully sent, in relation to the total number of sent messages.

* **[!UICONTROL Delivery Rate]**: Percentage of messages successfully sent.

* **[!UICONTROL Bounces]**: Total of errors cumulated during delivery and automatic return processing in relation to the total number of sent messages.

* **[!UICONTROL Bounce Rate]**: Percentage of emails that bounced compared to emails sent.

* **[!UICONTROL Errors]**: Total number of errors that occurred during a delivery preventing it from being sent to profiles.

* **[!UICONTROL Error Rate]**: Percentage of errors that occurred during a delivery preventing it from being sent compared to emails sent.

* **[!UICONTROL Retries]**: Number of emails in the queue for retries.

* **[!UICONTROL Excluded]**: Number of profiles which have been excluded by Adobe Journey Optimizer.

The **[!UICONTROL Email - Tracking statistics]** widget contains the available data for recipient activity for your delivery:

* **[!UICONTROL Opens]**: Number of times the delivery was opened in a delivery.

* **[!UICONTROL Unique Opens]**: Percentage of opened deliveries.

* **[!UICONTROL Open Rate]**: Total number of opened emails compared to the number of delivered emails.

* **[!UICONTROL Clicks]**: Number of times a content was clicked in an email.

* **[!UICONTROL Unique Clicks]**:Number of recipients who clicked on a content in an email.

* **[!UICONTROL Unique Click Rate]**: Percentage of users who interacted with the delivery.

* **[!UICONTROL Unsubscriptions]**: Number of clicks on the unsubscription link.

* **[!UICONTROL Spam complaints]**: Number of times a message was declared as spam or junk.

The **[!UICONTROL Sending Statistics]** graph contains the data available for sent emails, such as:

* **[!UICONTROL Delivered]**: Number of messages successfully sent, in relation to the total number of sent messages.

* **[!UICONTROL Bounces]**: Total of errors cumulated during delivery and automatic return processing in relation to the total number of sent messages.

* **[!UICONTROL Retries]**: Number of emails in the queue for retries.

* **[!UICONTROL Errors]**: Total number of errors that occurred during a delivery preventing it from being sent to profiles.

The **[!UICONTROL Bounce Reasons]** and **[!UICONTROL Bounce categories]** widgets contain the data available related to bounced messages, such as:

* **[!UICONTROL Hard bounce]**: The total number of permanent errors, such as a wrong email address. This involves an error message that explicitly states that the address is invalid, such as Unknown user.

* **[!UICONTROL Soft bounce]**: The total number of temporary errors, such as a a full inbox.

* **[!UICONTROL Ignored]**: The total number of temporary, such as Out of office, or a technical error, for example if the sender type is postmaster.

For more information on bounces, refer to the [Suppression list](../reports/suppression-list.md) page.

The **[!UICONTROL Error Reasons]** graph and table allow you to see which error occurred during your delivery.

The **[!UICONTROL Excluded reasons]** graph and table display the different reasons that prevented user profiles, excluded from the targeted profiles, from receiving the message.

The **[!UICONTROL Email - Top Url]** graph and table details which URLs from your delivery are the most visited.

The **[!UICONTROL Email - Top recipient domain]** graph and table details which domains are the most used by recipients to open the email.

>[!NOTE]
>
>The **[!UICONTROL Optimized vs non optimized]** and **[!UICONTROL Send time optimization]**  widgets are only available if the Send-Time Optimization option is activated for your delivery. For more information on Send-Time Optimization, refer to [this page](../building-journeys/journeys-message.md#send-time-optimization).

The **[!UICONTROL Optimized vs non optimized]** graph details the main information relative to your message whether they are optimized or not:

* **[!UICONTROL Sent]**: Total number of sends for the delivery.
* **[!UICONTROL Opens]**: Number of times the delivery was opened in a delivery.
* **[!UICONTROL Clicks]**: Number of times a content was clicked in an email.

The **[!UICONTROL Send time optimization]** details the success of your delivery depending on the sending method: optimized or normal.

* **[!UICONTROL Delivered]**: Number of messages successfully sent, in relation to the total number of sent messages.
* **[!UICONTROL Bounces]**: Total of errors cumulated during delivery and automatic return processing in relation to the total number of sent messages.
+++

## In-app tab {#inapp-global}

From your Campaign **[!UICONTROL Global report]**, the **[!UICONTROL In-app]** tab details the main information relative to the In-app deliveries sent in your campaign.

![](assets/campaign_report_global_6.png)

+++Learn more on the different metrics and widgets available for the In-app report.

The **[!UICONTROL In-app performance]** KPIs detail the main information relative to your visitors’ engagement with your In-app messages, such as:

* **[!UICONTROL Unique impressions]**: number of unique users to whom the In-app message was delivered.

* **[!UICONTROL Impressions]**: total number of In-app messages delivered to all users.

* **[!UICONTROL Click rate]**: percentage of users who interacted with the buttons included in the In-app message compared to users who saw the message.

* **[!UICONTROL Dismiss rate]**: percentage of In-app messages that recipients dismissed.

The **[!UICONTROL In-app summary]** graph shows the evolution of your In-app impressions for the concerned period.

The **[!UICONTROL Clicks by button]** graph and table contain the available data for recipient behavior per button:

* **[!UICONTROL Clicks]**: total number of recipients who interacted with the buttons included in the In-app message.

* **[!UICONTROL Click rate]**: percentage of users who interacted with the buttons included in the In-app message compared to users who saw the message.
+++

## Push notification tab {#push-global}

From your Campaign **[!UICONTROL Global report]**, the **[!UICONTROL Push notification]** tab details the main information relative to the push deliveries sent in your campaign.

![](assets/campaign_report_global_3.png)

+++Learn more on the different metrics and widgets available for the Push report.

The **[!UICONTROL Push notification - Sending statistics]** table details the main information relative to your push notifications with graph and KPIs:

* **[!UICONTROL Targeted]**: Total number of messages processed during the delivery analysis.

* **[!UICONTROL Sent]**: Total number of sends for the delivery.

* **[!UICONTROL Delivered]**: Number of messages successfully sent, in relation to the total number of sent messages.

* **[!UICONTROL Delivery Rate]**: Percentage of messages successfully sent.

* **[!UICONTROL Bounces]**: Total of errors cumulated during delivery and automatic return processing in relation to the total number of sent messages.

* **[!UICONTROL Bounce Rate]**: Percentage of push notifications that bounced compared to push notifications sent.

* **[!UICONTROL Errors]**: Total number of errors that occurred during a delivery preventing it from being sent to profiles.

* **[!UICONTROL Error Rate]**: Percentage of errors that occurred during a delivery preventing it from being sent compared to push notifications sent.

* **[!UICONTROL Excluded]**: Number of profiles which have been excluded by Adobe Journey Optimizer.

The **[!UICONTROL Push - Tracking statistics]** contains the available data for recipient activity for your delivery:

* **[!UICONTROL Opens]**: Number of times a message was opened in a delivery.

* **[!UICONTROL Open Rate]**: Percentage of opened push notifications.

* **[!UICONTROL Actions]**: Total number of actions on the push notification delivered, e.g. button click or dismissal.

* **[!UICONTROL Engagements]**: Total number of opens and actions for this push notification, i.e. if the profile opened the push or if a button was clicked on.

* **[!UICONTROL Engagement Rate]**: Percentage of opens and actions for this push notification, i.e. if the profile opened the push or if a button was clicked on.

The **[!UICONTROL Push notification summary]** graph contains the data available for sent push notifications, such as:

* **[!UICONTROL Opens]**: Number of times a message was opened in a delivery.

* **[!UICONTROL Actions]**: Total number of actions on the push notification delivered, e.g. button click or dismissal.

* **[!UICONTROL Bounces]**: Total of errors cumulated during delivery and automatic return processing in relation to the total number of sent messages.

* **[!UICONTROL Delivered]**: Number of messages successfully sent, in relation to the total number of sent messages.

* **[!UICONTROL Errors]**: Total number of errors that occurred during a delivery preventing it from being sent to profiles.

>[!NOTE]
>
>The **[!UICONTROL Optimized vs non optimized]** and **[!UICONTROL Send time optimization]**  widgets are only available if the Send-Time Optimization option is activated for your delivery. For more information on Send-Time Optimization, refer to [this page](../building-journeys/journeys-message.md#send-time-optimization).

The **[!UICONTROL Optimized vs non optimized]** graph details the main information relative to your message whether they are optimized or not:

* **[!UICONTROL Delivered]**: Number of messages successfully sent, in relation to the total number of sent messages.
* **[!UICONTROL Opens]**: Number of times the delivery was opened in a delivery.
* **[!UICONTROL Actions]**: Total number of actions on the push notification delivered, e.g. button click or dismissal.

The **[!UICONTROL Send time optimization]** details the success of your delivery depending on the sending method: optimized or normal.

* **[!UICONTROL Delivered]**: Number of messages successfully sent, in relation to the total number of sent messages.
* **[!UICONTROL Bounces]**: Total of errors cumulated during delivery and automatic return processing in relation to the total number of sent messages.

The **[!UICONTROL Error Reasons]** graph and table allow you to see which error occurred during your delivery.

The **[!UICONTROL Excluded reasons]** graph and table display the different reasons that prevented user profiles, excluded from the targeted profiles, from receiving the message.

The **[!UICONTROL Tracking by platform]**, **[!UICONTROL Sending by platform]** and **[!UICONTROL Breakdown by platform]** graphs and tables details the success of your push notification depending on your recipient's operational system.
+++

## SMS tab {#sms-global}

From your Campaign **[!UICONTROL Global report]**, the **[!UICONTROL SMS]** tab details the main information relative to the SMS deliveries sent in your campaign.

![](assets/campaign_report_global_4.png)

+++Learn more on the different metrics and widgets available for the SMS report.

The **[!UICONTROL SMS - Sending statistics]** table details the success of your delivery:

* **[!UICONTROL Targeted]**: Number of user profiles who qualify as target profiles for this delivery.

* **[!UICONTROL Excluded]**: Number of user profiles, excluded from the targeted profiles, who did not receive the message.

* **[!UICONTROL Sent]**: Total number of sends for the delivery.

* **[!UICONTROL Delivered]**: Number of messages successfully sent, in relation to the total number of sent messages.

* **[!UICONTROL Bounces]**: Total of errors cumulated during delivery and automatic return processing in relation to the total number of sent messages.

* **[!UICONTROL Errors]**: Total number of errors that occurred during a delivery preventing it from being sent to profiles.

The **[!UICONTROL SMS Performance by date]** widget details the main information relative to your message with a graph:

* **[!UICONTROL Sent]**: Total number of sends for the delivery.

* **[!UICONTROL Delivered]**: Number of messages successfully sent, in relation to the total number of sent messages.

* **[!UICONTROL Bounces]**: Total of errors cumulated during delivery and automatic return processing in relation to the total number of sent messages.

* **[!UICONTROL Errors]**: Total number of errors that occurred during a delivery preventing it from being sent to profiles.

The **[!UICONTROL Exclude Reasons]**, **[!UICONTROL Bounces Reasons]** and **[!UICONTROL Error Reasons]** graphs and tables allow you to see which error and exclusions occurred during your delivery.

The **[!UICONTROL SMS - Clicks by links]** and **[!UICONTROL SMS - Tracking statistics]** widgets detail the main information relative to your visitors’ engagement with your URLs.

+++

## Web tab {#web-tab}

From your Campaign **[!UICONTROL Global report]**, the **[!UICONTROL Web]** tab details the main information relative to your Web pages.

![](assets/web-report.png)

+++Learn more on the different metrics and widgets available for the Web report.

The **[!UICONTROL Web performance]** KPIs detail the main information relative to your visitors' engagement with your web experiences, such as:

* **[!UICONTROL Unique impressions]**: number of unique users to whom the web experience was delivered.

* **[!UICONTROL Impressions]**: total number of web experiences delivered to all users.

* **[!UICONTROL Click rate]**: percentage of visitors who interacted with the various elements on your web pages.

The **[!UICONTROL Web summary]** graph shows the evolution of your web experiences (impressions, unique impressions and clicks) for the concerned period.

The **[!UICONTROL Clicks by element]** table details the main information relative to your visitors' engagement with the various elements on your web pages.
+++

## Additional resources

* [Get started with campaigns](../campaigns/get-started-with-campaigns.md)
* [Create a campaign](../campaigns/create-campaign.md)
* [Create API-triggered campaigns](../campaigns/api-triggered-campaigns.md)
* [Modify or stop a campaign](../campaigns/modify-stop-campaign.md)
* [Campaign live report](campaign-live-report.md)

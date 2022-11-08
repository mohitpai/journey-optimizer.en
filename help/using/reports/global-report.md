---
solution: Journey Optimizer
product: journey optimizer
title: Global report
description: Learn how to use data from the global report
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: ec15e700-7659-4dbf-8446-6534ea48c5c8
---
# Get started with Global Report {#global-report}

>[!NOTE]
>
> If custom queries are made through APIs when using Query service, please expect some delay for your reports.

Use the **[!UICONTROL Global report]** to measure the impact of your journeys and deliveries over a selected time period.

* If you want to target a journey or deliveries in the context of a journey, from the **[!UICONTROL Journeys]** menu, access your journey and click the **[!UICONTROL View report]** button. You can then find the Journey, Email, SMS and Push global reports.

    ![](assets/report_journey.png)

* If you want to target a campaign, from the **[!UICONTROL Campaigns]** menu, access your campaign and click the **[!UICONTROL Reports]** button.

    ![](assets/report_campaign.png)

* If you want to switch from the **[!UICONTROL Live report]** to the **[!UICONTROL Global report]** for your delivery, click **[!UICONTROL All time]** from the tab switcher.

    ![](assets/report_5.png)

For a detailed list of every metric available in Adobe Journey Optimizer, refer to [this page](#list-of-components-global)

## Customize dashboard {#modify-dashboard}

Each reporting dashboard can be modified by changing the time period and resizing or removing widgets. Changing the widgets only impacts the current user's dashboard. Other users will see their own dashboards or the ones set by default.

1. From your Global report, select a Start and End time to target specific data.

    ![](assets/report_modify_1.png)

1. Choose if you want to exclude test events from your reports with the toggle bar. For more information on test events, refer to [this page](../building-journeys/testing-the-journey.md).

    Note that the **[!UICONTROL Exclude test events]** option is only available for Journey reports.

    ![](assets/report_modify_2.png)

1. Click **[!UICONTROL Modify]** to start customizing your dashboard.

    ![](assets/report_modify_3.png)

1. Adjust the widgets size by dragging its bottom-right corner.

    ![](assets/report_modify_4.png)

1. Click **[!UICONTROL Remove]** to remove any widget you don't need.

    ![](assets/report_modify_5.png)

1. Once you are satisfied with the display order and the size of your widgets, click **[!UICONTROL Save]**.

Your dashboard is now saved. Your different changes will be reapplied for a later use of your live reports. If needed, use the **[!UICONTROL Reset]** option to restore the default widgets and widgets' order.

## List of components {#list-of-components-global}

The tables below give you the list of metrics used in reports and their definitions depending on the delivery type.

### Journey metrics {#journey-metrics}

<table> 
 <thead> 
  <tr> 
   <th> Metric<br/> </th> 
   <th> Definition<br/> </th> 
</tr>
 </thead> 
 <tbody> 
  <tr> 
   <td>Actions successfully executed<br/> </td> 
   <td> Total number of Actions successfully executed for a journey.<br/> </td> 
</tr> 
  <tr> 
   <td> Entered profiles<br/> </td> 
   <td> Total number of individuals who reached the entry event of the journey.<br/> </td> 
</tr>
  <tr> 
   <td> Error in action<br/> </td> 
   <td>Total number of errors that occurred for Actions.<br/> </td> 
</tr> 
  <tr> 
   <td> Exited profiles<br/> </td> 
   <td> Total number of individuals who exited the journey.<br/> </td> 
</tr> 
  <tr> 
   <td> Failed individual journey<br/> </td> 
   <td> Total number of individual journeys that were not successfully executed.<br/> </td> 
</tr> 
 </tbody> 
</table>

### Email and SMS metrics {#email-and-sms-metrics}

<table> 
 <thead> 
  <tr> 
   <th> Metric<br/> </th> 
   <th> Definition<br/> </th> 
</tr>
 </thead> 
 <tbody>
  <tr> 
   <td> Bounces<br/> </td> 
   <td> Total of errors cumulated during delivery and automatic return processing in relation to the total number of sent messages.<br/> </td> 
</tr> 
  <tr> 
   <td> Bounce Rate<br/> </td> 
   <td> Percentage of emails that bounced compared to emails sent.<br/> </td> 
</tr>
  <tr> 
   <td> Clicks<br/> </td> 
   <td> Number of times a content was clicked in an email.<br/> </td> 
</tr> 
  <tr> 
   <td> Delivered <br/> </td> 
   <td> Number of messages successfully sent, in relation to the total number of sent messages.<br/></td> 
</tr> 
  <tr> 
   <td> Delivery Rate<br/> </td> 
   <td> Percentage of messages successfully sent.<br/> </td> 
</tr>
  <tr> 
   <td> Errors<br/> </td> 
   <td> Total number of errors that occurred during a delivery preventing it from being sent to profiles.<br/> </td> 
</tr> 
  <tr> 
   <td> Error Rate<br/> </td> 
   <td> Percentage of errors that occurred during a delivery preventing it from being sent compared to emails sent.<br/> </td> 
</tr>
  <tr> 
   <td> Excluded<br/> </td> 
   <td> Number of profiles which have been excluded by Adobe Journey Optimizer.<br/> </td> 
</tr>
  <tr> 
   <td> Hard bounce<br/> </td> 
   <td> The total number of permanent errors, such as a wrong email address. This involves an error message that explicitly states that the address is invalid, such as Unknown user.<br/> </td>
</tr>
  <tr> 
   <td> Ignored<br/> </td> 
   <td> The total number of temporary, such as Out of office, or a technical error, for example if the sender type is postmaster.<br/> </td> 
</tr>
   <tr> 
   <td>Offer click rate<br/> </td> 
   <td>Percentage of users who interacted with the offer.<br/> </td> 
</tr>
   <tr> 
   <td>Offer impression rate<br/> </td> 
   <td>Percentage of opened offers compared to the number of sent offers.<br/> </td> 
</tr>
   <tr> 
   <td>Offer name<br/> </td> 
   <td> Name of the offer added in the delivery. For more information on placement, refer to this <a href="../offers/offer-library/creating-personalized-offers.md">page</a>.<br/> </td> 
</tr>
   <tr> 
   <td>Offer sent<br/> </td> 
   <td>Total number of sends for the offer.<br/> </td> 
</tr> 
  <tr>
   <td>Opens<br/> </td> 
   <td> Number of times the message was opened.<br/> </td> 
</tr> 
  <tr> 
   <td> Open Rate<br/> </td> 
   <td> Total number of opened emails compared to the number of delivered emails.<br/> </td> 
</tr>
  <tr> 
   <td>Placement name<br/> </td> 
   <td> Name of your placement used to display your offer. For more information on placement, refer to this <a href="../offers/offer-library/creating-placements.md">page</a>. </td> 
</tr> 
  <tr> 
   <td> Retries<br/> </td> 
   <td> Number of emails in the queue for retries.<br/> </td> 
</tr> 
  <tr> 
   <td> Sent<br/> </td> 
   <td> Total number of sends for the delivery.<br/> </td> 
</tr>
  <tr> 
   <td> Soft bounce<br/> </td> 
   <td> Total number of temporary errors, such as a full inbox.<br/> </td> 
</tr>
  <tr> 
   <td> Spam complaints<br/> </td> 
   <td> Number of times a message was declared as spam or junk.<br/> </td> 
</tr>
  <tr> 
   <td> Targeted<br/> </td> 
   <td> Total number of messages processed during the delivery analysis.<br/> </td> 
</tr> 
  <tr> 
   <td> Unique Clicks<br/> </td> 
   <td> Number of recipients who clicked on a content in an email.<br/> </td> 
</tr> 
  <tr> 
   <td>Unique Click Rate<br/> </td> 
   <td> Percentage of users who interacted with the delivery.<br/> </td> 
</tr>
  <tr> 
   <td> Unique Opens<br/> </td> 
   <td>Number of recipients who opened the delivery.<br/> </td> 
</tr> 
  <tr> 
   <td> Unsubscriptions<br/> </td> 
   <td> Number of clicks on the unsubscription link.<br/> </td> 
</tr> 
 </tbody> 
</table>

### Experimentation metrics {#experimentation-metrics}

<table> 
 <thead> 
  <tr> 
   <th> Metric<br/> </th> 
   <th> Definition<br/> </th> 
</tr>
 </thead> 
 <tbody>
  <tr> 
   <td>App installs<br/> </td> 
   <td><br/> </td> 
</tr>
  <tr> 
   <td>App launches<br/> </td> 
   <td><br/> </td> 
</tr>
 <tr> 
   <td>Average lift<br/> </td> 
   <td> Percentage improvement in conversion rate of a given treatment over the baseline.<a href="../campaigns/experiment-calculations.md#understand-lift">Learn more</a>.<br/> </td> 
  </tr>
  <tr> 
   <td>Confidence<br/> </td> 
   <td>Evidence that a given treatment is the same as the baseline treatment. <a href="../campaigns/experiment-calculations.md#understand-confidence">Learn more</a>.<br/> </td> 
</tr>
  <tr> 
   <td>Confidence interval<br/> </td> 
   <td>Percentage difference in performance between the baseline and the best performing treatment. <a href="../campaigns/experiment-calculations.md#understand-intervals">Learn more</a>.<br/> </td> 
</tr> 
  <tr> 
   <td>Count per profile<br/> </td> 
   <td>Total value of the Experiment objective metric divided by the number of profiles.<br/> </td> 
</tr>
  <tr> 
   <td>Email Opens<br/> </td> 
   <td>.<br/> </td> 
</tr>
  <tr> 
   <td>Email Unsubscribes<br/> </td> 
   <td><br/> </td> 
</tr>
  <tr> 
   <td>First app launches<br/> </td> 
   <td><br/> </td> 
</tr>
  <tr> 
   <td>Outbound Clicks<br/> </td> 
   <td><br/> </td> 
</tr>
  <tr> 
   <td>Profiles<br/> </td> 
   <td>Number of profiles targeted for this treatment.<br/> </td> 
</tr>
  <tr> 
   <td>Unique email opens<br/> </td> 
   <td><br/> </td>
<tr>
  <tr> 
   <td>Unique email unsubscribes<br/> </td> 
   <td><br/> </td>
</tr>
  <tr> 
   <td>Unique installs<br/> </td> 
   <td><br/> </td> 
</tr>
  <tr> 
   <td>Unique launches<br/> </td> 
   <td><br/> </td> 
</tr> 
  <tr> 
   <td>Unique outbound clicks<br/> </td> 
   <td><br/> </td> 
</tr>
  <tr> 
   <td>Unique upgrades<br/> </td> 
   <td><br/> </td> 
</tr>
   <td>Upgrades<br/> </td> 
   <td><br/> </td> 
</tr> 
</tbody> 
</table>

### Push notification metrics

<table> 
 <thead> 
  <tr> 
   <th> Metric<br/> </th> 
   <th> Definition<br/> </th> 
</tr>
 </thead> 
 <tbody>
 <tr> 
   <td>Actions<br/> </td> 
   <td> Total number of actions on the push notification delivered, e.g. button click or dismissal.<br/> </td> 
</tr>
  <tr> 
   <td>Bounces<br/> </td> 
   <td> Total of errors cumulated during delivery and automatic return processing in relation to the total number of sent messages.<br/> </td> 
</tr> 
  <tr> 
   <td> Bounce Rate<br/> </td> 
   <td> Percentage of push notifications that bounced compared to push notifications sent.<br/> </td>
</tr>
  <tr> 
   <td> Delivered<br/> </td> 
   <td> Number of messages successfully sent, in relation to the total number of sent messages.<br/> </td> 
</tr> 
  <tr> 
   <td> Delivery rate<br/> </td> 
   <td> Percentage of push notifications successfully sent.<br/> </td> 
</tr>
  <tr> 
   <td>Engagements<br/> </td> 
   <td> Total number of opens and actions for this push notification, i.e. if the profile opened the push or if a button was clicked on.<br/> </td> 
</tr> 
  <tr> 
   <td> Engagement Rate<br/> </td> 
   <td> Percentage of opens and actions for this push notification, i.e. if the profile opened the push or if a button was clicked on.<br/> </td> 
</tr>
  <tr> 
   <td> Errors<br/> </td> 
   <td> Total number of errors that occurred during a delivery preventing it from being sent to profiles.<br/> </td> 
</tr>
  <tr> 
   <td> Error Rate<br/> </td> 
   <td> Percentage of errors that occurred during a delivery preventing it from being sent compared to push notifications sent.<br/> </td> 
</tr> 
  <tr> 
   <td> Excluded<br/> </td> 
   <td> Number of profiles which have been excluded by Adobe Journey Optimizer.<br/> </td> 
</tr>
  <tr> 
   <td> Opens<br/> </td> 
   <td> Total number of push notifications delivered to the device and clicked on by users thus opening the app. This is similar to the Push Click except a Push Open will not be triggered if the notification was dismissed.<br/> </td> 
</tr> 
  <tr> 
   <td> Open rate<br/> </td> 
   <td> Percentage of opened push notifications.<br/> </td> 
</tr> 
  <tr> 
   <td> Sent<br/> </td> 
   <td> Total number of sends for the delivery.<br/> </td> 
</tr> 
  <tr> 
   <td> Targeted<br/> </td> 
   <td> Total number of push messages processed during the delivery analysis.<br/> </td> 
</tr>  
 </tbody> 
</table>

### Landing page metrics {#landing-page-metrics}

<table> 
 <thead> 
  <tr> 
   <th> Metric<br/> </th> 
   <th> Definition<br/> </th> 
</tr>
 </thead> 
 <tbody>
 <tr> 
  <td>Bounces<br/> </td> 
   <td>Number of persons who didn't interact with the landing page and didn't complete the action of subscribing.<br/> </td> 
</tr>
 <tr> 
   <td>Bounce rate<br/> </td> 
   <td>Number of persons who didn't interact with the landing page and didn't complete the action of subscribing, in relation to the total number of visits.<br/> </td> 
</tr>
 <tr>
  <tr> 
   <td>Clicks<br/> </td> 
   <td>Number of times a content was clicked on in the landing page.<br/> </td> 
</tr>
 <tr> 
   <td>Click rate<br/> </td> 
   <td>Percentage of clicks in the landing page.<br/> </td>
</tr>
<tr>
<td>Conversion<br/> </td> 
   <td>Number of persons who interacted with the landing page, e.g. subscribed to a form.<br/> </td> 
</tr>
<tr>
   <td>Conversion rate<br/> </td> 
   <td>Number of persons who interacted with the landing page, e.g. subscribed to a form, in relation to the total number of visits.<br/> </td> 
</tr>
 <tr> 
   <td>Journey(s)<br/> </td> 
   <td>Number of visits to your landing page coming from a journey.<br/> </td> 
</tr>
 <tr> 
   <td>Other sources<br/> </td> 
   <td>Number of visits to your landing page coming from an external source instead of a journey.<br/> </td> 
</tr>
 <tr> 
   <td>Total visits<br/> </td> 
   <td> Total number of visits to your landing page coming from journeys and external sources, including multiple visits of one recipient.<br/> </td> 
</tr>
 <tr> 
   <td>Unique visitors<br/> </td> 
   <td>Number of persons who visited your landing page, multiple visits of one recipient are not taken into account.<br/> </td> 
</tr>
 <tr> 
   <td>Visits<br/> </td> 
   <td>Number of visits to your landing page, including multiple visits of one recipient.<br/> </td> 
</tr>
 </tbody> 
</table>

### Push notification metrics

<table> 
 <thead> 
  <tr> 
   <th> Metric<br/> </th> 
   <th> Definition<br/> </th> 
</tr>
 </thead> 
 <tbody>
 <tr> 
   <td>Actions<br/> </td> 
   <td> Total number of actions on the push notification delivered, e.g. button click or dismissal.<br/> </td> 
</tr>
  <tr> 
   <td>Bounces<br/> </td> 
   <td> Total of errors cumulated during delivery and automatic return processing in relation to the total number of sent messages.<br/> </td> 
</tr> 
  <tr> 
   <td> Bounce Rate<br/> </td> 
   <td> Percentage of push notifications that bounced compared to push notifications sent.<br/> </td>
</tr>
  <tr> 
   <td> Delivered<br/> </td> 
   <td> Number of messages successfully sent, in relation to the total number of sent messages.<br/> </td> 
</tr> 
  <tr> 
   <td> Delivery rate<br/> </td> 
   <td> Percentage of push notifications successfully sent.<br/> </td> 
</tr>
  <tr> 
   <td>Engagements<br/> </td> 
   <td> Total number of opens and actions for this push notification, i.e. if the profile opened the push or if a button was clicked on.<br/> </td> 
</tr> 
  <tr> 
   <td> Engagement Rate<br/> </td> 
   <td> Percentage of opens and actions for this push notification, i.e. if the profile opened the push or if a button was clicked on.<br/> </td> 
</tr>
  <tr> 
   <td> Errors<br/> </td> 
   <td> Total number of errors that occurred during a delivery preventing it from being sent to profiles.<br/> </td> 
</tr>
  <tr> 
   <td> Error Rate<br/> </td> 
   <td> Percentage of errors that occurred during a delivery preventing it from being sent compared to push notifications sent.<br/> </td> 
</tr> 
  <tr> 
   <td> Excluded<br/> </td> 
   <td> Number of profiles which have been excluded by Adobe Journey Optimizer.<br/> </td> 
</tr>
  <tr> 
   <td> Opens<br/> </td> 
   <td> Total number of push notifications delivered to the device and clicked on by users thus opening the app. This is similar to the Push Click except a Push Open will not be triggered if the notification was dismissed.<br/> </td> 
</tr> 
  <tr> 
   <td> Open rate<br/> </td> 
   <td> Percentage of opened push notifications.<br/> </td> 
</tr> 
  <tr> 
   <td> Sent<br/> </td> 
   <td> Total number of sends for the delivery.<br/> </td> 
</tr> 
  <tr> 
   <td> Targeted<br/> </td> 
   <td> Total number of push messages processed during the delivery analysis.<br/> </td> 
</tr>  
 </tbody> 
</table>

<!--
### In-app metrics {#inapp-metrics}
<table> 
 <thead> 
  <tr> 
   <th> Metric<br/> </th> 
   <th> Definition<br/> </th> 
</tr>
 </thead> 
 <tbody>
 <tr> 
   <td>Clicks<br/> </td> 
   <td>Total number of recipients who interacted with the buttons included in the In-app message.<br/> </td> 
</tr>
  <tr> 
   <td>Click rate<br/> </td> 
   <td>Percentage of users who interacted with the buttons included in the In-app message compared to users who saw the message.<br/> </td> 
</tr> 
  <tr> 
   <td>Dismiss rate<br/> </td> 
   <td> Percentage of In-app messages that recipients dismissed.<br/> </td> 
</tr> 
  <tr> 
   <td>Impressions<br/> </td> 
   <td> Total number of In-app messages delivered to all users.<br/> </td>
</tr>
  <tr> 
   <td>Unique impressions<br/> </td> 
   <td>Number of unique users to whom the In-app message was delivered.<br/> </td>
</tr>
 </tbody> 
</table>
-->

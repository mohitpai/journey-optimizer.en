---
solution: Journey Optimizer
product: journey optimizer
title: Release notes
description: Journey Optimizer Release notes
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
---
# Release notes {#release-notes}

[!DNL Adobe Journey Optimizer] continuously delivers new features, enhancements to existing features, and bug fixes. All changes are consolidated on the last week of each month in these release notes. 

Previous release notes are available in [this page](release-notes-2023.md). You can also consult the [latest documentation updates](documentation-updates.md) page for more changes.

[!DNL Adobe Journey Optimizer] is built natively on [!DNL Adobe Experience Platform] and inherits from its latest innovations and improvements. Learn more about these changes in [Adobe Experience Platform Release Notes](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html){target="_blank"}.

![Newsletter](../assets/do-not-localize/nl-icon.png) Sign up for the [Adobe Journey Optimizer quarterly newsletter](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"} today, and receive the latest product updates, exciting stories, use cases, tips and more delivered directly to your inbox every quarter.

## March 2023 Release Notes {#mar-2023}

### New capabilities{#mar-2023-features}

<table>
<thead>
<tr>
<th><strong>In-app channel (General Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now send personalized In-app messages to your app users within a campaign. Use Journey Optimizer to design notifications and customize the message layout, display, text, and buttons to create a seamless experience.</p>
<img src="assets/do-not-localize/in-app.gif"/>
<p>For more information, refer to the <a href="../in-app/get-started-in-app.md">detailed documentation</a>.</p>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>SMS click tracking</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>With SMS click tracking, you can monitor the performance of your shortened URLs, identify who clicked on them, and use this data to retarget those customers with subsequent campaigns.</p>
<img src="assets/do-not-localize/sms-tracking.gif"/>
<p>For more information, refer to the <a href="../sms/create-sms.md#sms-content">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Use Tags in your Journeys (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>As a Journey Optimizer practitioner, you can now organize your business objects using tags. Tags are a quick and easy way of classifying objects to improve search. This feature is currently in beta and only available for Journeys.</p>
<p>For more information, refer to the <a href="../building-journeys/tags.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>

### Improvements {#mar-2023-improvements}

**Journeys**

* The new **Throttling API** allows you to set a limit on the number of events sent per second, preventing overwhelming traffic spikes on your external systems or API. When the set limit is reached, all subsequent API calls are queued and processed as soon as possible, in the order they were received. Please note that this feature supports only one throttling configuration across all your sandboxes. [Learn more](../configuration/external-systems.md)
* The Journey canvas has been enhanced for a simpler and improved user experience. At the end of each path in the canvas, the empty place holders have been removed. You can now simply add your activities by dragging them at the end of a path.
* In the journey canvas, the label of the **End** tag is no longer automatically set with the previous activity's name. Users can manually add a custom label if needed.
* The default timeout and error duration in journey properties has been changed from 5 to 30 seconds. [Learn more](../configuration/external-systems.md#timeout)
* The default throttling rate in read segment activities has been changed from 20,000 to 5,000 messages per second. [Learn more](../building-journeys/read-segment.md#configuring-segment-trigger-activity)

<!-- 
* When adding an Email, SMS or Push action in a journey, the surface is now pre-filled, by default, with the last used surface for that channel.
* A new type of system alert has been introduced. You can now get notified when a custom action fails. [Learn more](../reports/alerts.md)
* Timeout and error management has been improved in journeys. Timeout and error paths are now always added on the canvas. A new toolbar button is available to show/hide these paths. [Learn more](../building-journeys/journey-gs.md#timeout_and_error)
* The Journey dashboard is now split in two tabs:
    * Use the **Overview** tab to access a new dashboard which displays key metrics related to your journeys.
    * Use the **Browse** tab to access list of all journeys.
-->

**Decision management**

* To prevent any potential confusion with the recent release of tags feature across  Adobe Experience Platform, Decision Management tags have been renamed to "Collection qualifiers".

    Note that although the term "tag" is no longer used in Decision management user interface, it is still used in backend services such as APIs and datasets.

* You can now reset the offer capping counter on a daily, weekly or monthly basis. [Learn more](../offers/offer-library/add-constraints.md#capping)

* You can also choose which Adobe Experience Platform event should be looked at for offer decisioning capping. [Learn more](../offers/offer-library/add-constraints.md#capping)

* Additional parameters have been added in placements creation screen. They allow you to control whether an offer can be duplicated across multiple placements, and to specify if the offer's content and metadata should be included in the API response. [Learn more](../offers/offer-library/creating-placements.md)

**Personalization**

* You can now include default fallback text for string-based profile attributes in the Expression Editor. These values will display if the selected attributes return no result. [Learn more](../personalization/personalization-build-expressions.md#add)

**Reporting**

* The reporting widget functionality has been improved with the ability to customize how users view their data. With this improvement, users can now choose between multiple visualization options, including graph, table, and donut charts.

    To have access to the latest widgets, please note that you will have to reset the different reporting dashboards. For more information on dashboard customization, refer to the [detailed documentation](../reports/global-report.md#modify-dashboard).

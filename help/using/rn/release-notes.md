---
solution: Journey Optimizer
product: journey optimizer
title: Release notes
description: Journey Optimizer Release notes
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
---
# Release Notes {#release-notes}

[!DNL Adobe Journey Optimizer] continuously delivers new features, enhancements to existing features, and bug fixes. All changes are consolidated on the last week of each month in these release notes. 

Previous release notes are available in [this page](release-notes-2022.md). You can also consult the [latest documentation updates](documentation-updates.md) page for more changes.

[!DNL Adobe Journey Optimizer] is built natively on [!DNL Adobe Experience Platform] and inherits from its latest innovations and improvements. Learn more about these changes in [Adobe Experience Platform Release Notes](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html){target="_blank"}.

![Newsletter](../assets/do-not-localize/nl-icon.png) Sign up for the [Adobe Journey Optimizer quarterly newsletter](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"} today, and receive the latest product updates, exciting stories, use cases, tips and more delivered directly to your inbox every quarter.

## February 2023 Early Release Notes {#feb-2023}

This section contains prerelease information. Release dates, features, and other information are subject to change without notice.

Availability: **February 22, 2023**



<table>
<thead>
<tr>
<th><strong>Performance Measurement in campaigns</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now measure the performance of your campaigns across inbound and outbound through dedicated reports. Adobe Journey Optimizer reports can retrieve additional metrics to use in the Objectives tab of your campaign reports. </p>
<img src="assets/do-not-localize/performance_report.gif"/>
<!--p>For more information, refer to the <a href="../privacy/data-hygiene.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>

+++ Learn more about Performance Measurement

The **[!UICONTROL Objectives]** tab of your Campaign report allows you to better fine-tune your deliveries' reports by targeting one specific metric. With this feature, you can effectively track and analyze your campaign's performance and make informed decisions to improve your results.

The **[!UICONTROL Objectives]** listed are linked to **[!UICONTROL Datasets]** that define a connection to a system in order to retrieve additional information. A list of pre-configured **[!UICONTROL Objectives]** is available, but you can also customize your report by adding new **[!UICONTROL Datasets]** and defining your own objectives. 

By selecting the desired Objectives, the **[!UICONTROL Performance overview]** and **[!UICONTROL Campaign objective]** widgets provide a comprehensive and insightful summary of your delivery performance, allowing you to closely monitor and evaluate the success of your campaign.

With the **[!UICONTROL Campaign objective]** widget, you can also choose to compare your primary objective against another performance metric.

Note that each widget can be resized and deleted if needed.
+++



<table>
<thead>
<tr>
<th><strong>Export Journey Optimizer datasets to cloud storage destinations (beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now establish a live connection with cloud storage locations in order to export the content of your datasets. Available destinations are: Amazon S3 Cloud Storage, Azure Blob, Azure Data Lake Gen 2, Data Landing Zone, Google Cloud Storage, SFTP.</p>
<p>This feature is currently available as a beta to select users only.</p>
<!--p>For more information, refer to the <a href="../privacy/data-hygiene.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Tags in journeys</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>As a Journey Optimizer practitioner, you can now organize your business objects using tags. Tags are a quick and easy way of classifying objects to improve search. Tags are currently only available for Journeys.</p>
</td>
</tr>
</tbody>
</table>



### Improvements {#feb-2023-improvements}

**Journeys**

* The **Re-entrance wait period** field has been added to the journey properties. This field allows you to define the time to wait before allowing a profile to enter the journey again in unitary journeys (starting with an event or a segment qualification). This prevents journeys from being erroneously triggered multiple times for the same event. By default the field is set to 5 minutes. [Learn more](../building-journeys/journey-gs.md#entrance)

* Improvements have been made for **journey start and end dates**. If you have not specified a start date, it is now automatically added at publication time. For **Read segment** journeys, you can now add an end date. This allows profiles to exit automatically when the date is reached. [Learn more](../building-journeys/journey-gs.md#dates)



## January 2023 Release {#jan-2023-release}

### New capabilities{#jan-2023-features}

<table>
<thead>
<tr>
<th><strong>Data Hygiene</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Experience Platform provides a suite of data hygiene capabilities that allow you to manage your stored data through programmatic deletions of consumer records and datasets. This capability is now available for Adobe Journey Optimizer. </p>
<p>You can manage your data stores to ensure that information is used as expected, is updated when incorrect data needs fixing, and is deleted when organizational policies deem it necessary.</p>
<p><strong>Caution</strong> - Data Hygiene capabilities are currently only available for organizations that have purchased the <strong>Healthcare Shield</strong> and <strong>Privacy and Security Shield</strong> add-on offerings.</p><p>For more information, refer to the <a href="../privacy/data-hygiene.md">detailed documentation</a>.
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Email content templates</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now create standalone content templates that can be leveraged across journeys and campaigns for quick reuse.</p> 
</p>
<img src="assets/do-not-localize/content-template.gif"/>
<p>Learn how to create, edit, and use content templates in <a href="https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/email-channel/content-templates.html">this video</a>. For more information, refer to the <a href="../email/content-templates.md">detailed documentation</a>.
</p>
</td>
</tr>
</tbody>
</table>

### Improvements {#jan-2023-improvements}

**Journeys**

<!--
* The **Re-entrance wait period** field has been added to the journey properties. This field allows you to define the time to wait before allowing a profile to enter the journey again in unitary journeys (starting with an event or a segment qualification). This prevents journeys from being erroneously triggered multiple times for the same event. By default the field is set to 5 minutes. [Learn more](../building-journeys/journey-gs.md#entrance)

* Improvements have been made for **journey start and end dates**. If you have not specified a start date, it is now automatically added at publication time. For **Read segment** journeys, you can now add an end date. This allows profiles to exit automatically when the date is reached. [Learn more](../building-journeys/journey-gs.md#dates)
-->

* When adding a **Segment qualification** or **Read segment** in a journey, the namespace is now pre-filled, by default, with the last used namespace. Refer to the [Segment qualification](../building-journeys/segment-qualification-events.md#about-segment-qualification) and [Read segment](../building-journeys/read-segment.md#configuring-segment-trigger-activity) sections.

* In the journey canvas, a new button is available in the toolbar which allows you to download a screenshot of your journey. 

**Email Designer**

* You can now export the email content from the **Export HTML** menu. Exported files are available in an archive (.ZIP) file.

**Administration**

* A new subsection provides recommendations on building the **Reply to (email)** address and ensuring proper reply management. [Learn more](../email/email-settings.md#reply-to-email)

* When creating or editing **IP pools**, the associated PTR records are now displayed in the IP list and when hovering over the selected IP addresses. [Learn more](../configuration/ip-pools.md#create-ip-pool)

* After an IP pool has been selected in a channel surface, PTR record information is now visible when hovering over the IP addresses. [Learn more](../email/email-settings.md#subdomains-and-ip-pools)

* The user interface for editing [PTR records](../configuration/ptr-records.md#edit-ptr-record) and [execution fields](../configuration/primary-email-addresses.md) has been updated.

* The user interface for creating and editing subdomains has been improved. [Learn more](../configuration/delegate-subdomain.md)

* The suppression list **Recent uploads** screen has been updated. [Learn more](../configuration/manage-suppression-list.md#recent-uploads)

**Campaigns**

* A sample cURL request allowing API-triggered campaigns execution is now automatically generated and made available in the campaign screen. [Learn more](../campaigns/api-triggered-campaigns.md)

<!--
**Decision management**

* Additional parameters have been added in placements creation screen. They allow you to control whether an offer can be duplicated across multiple placements, and to specify if the offer's content and metadata should be included in the API response. [Learn more](../offers/offer-library/creating-placements.md)-->

<!--* It is now possible to reset the offer capping counter on a daily, weekly or monthly basis. [Learn more](../offers/offer-library/add-constraints.md#capping)-->

**Personalization**

* New helper functions are available: formatCurrency, charCodeAt, stringToDate, toString, formatNumber, and toHexString. Additionally, the toDateTimeOnly function now accepts string, date, long and int field types. [Learn more](../personalization/functions/functions.md)

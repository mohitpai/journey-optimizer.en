---
solution: Journey Optimizer
product: journey optimizer
title: Release notes
description: Journey Optimizer Release notes
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
---
# Release Notes {#release-notes}

This page lists all the new features and improvements for [!DNL Journey Optimizer]. You can also consult the [latest documentation updates](documentation-updates.md) page for more changes.

[!DNL Adobe Journey Optimizer] is built natively on [!DNL Adobe Experience Platform] and inherits from its latest innovations and improvements. Learn more about these changes in [Adobe Experience Platform Release Notes](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html){target="_blank"}.

![Newsletter](../assets/do-not-localize/nl-icon.png) Sign up for the [Adobe Journey Optimizer quarterly newsletter](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"} today, and receive the latest product updates, exciting stories, use cases, tips and more delivered directly to your inbox every quarter.


## October 2022 Release {#oct-2022-release}

<!--

### New capability{#oct-2022-features}

<table>
<thead>
<tr>
<th><strong>Direct Mail Channel (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now add direct mail messages in your campaigns and journeys. Direct mail is an offline channel that allows you to personalize and generate the files required by direct mail providers to send mail to your customers.</p>
<p>When you prepare a direct mail delivery, Journey Optimizer generates a file including all the targeted profiles and the chosen contact information (postal address for example). You will then be able to send this file to your direct mail provider who will take care of the actual sending.</p>
</td>
</tr>
</tbody>
</table>

-->

### Improvements {#oct-2022-improvements}

**Journeys**

* The **Force reentrance on recurrence** option has been added in recurring read segment schedule parameters. This option allows you to make all the profiles still present in the journey automatically exit it on the next execution. When the option is deactivated, profiles must finish the journey before they can reenter in another occurrence. [Learn more](../building-journeys/read-segment.md#configuring-segment-trigger-activity)

**Administration**

* A message was added to the user interface to warn that subdomain, landing page subdomain, PTR record and IP pool configurations are common to all sandboxes and thus any modification to one of these configurations will also impact the production sandboxes.
* The steps to upload the suppression list as a CSV file from the user interface have been modified. [Learn more](../configuration/manage-suppression-list.md#download-suppression-list)

**Campaigns**

* You can now archive completed and stopped campaigns. [Learn more](../campaigns/modify-stop-campaign.md#archive)

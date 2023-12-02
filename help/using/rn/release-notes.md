---
solution: Journey Optimizer
product: journey optimizer
title: Release notes
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
description: Journey Optimizer Release notes
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
---
# Release notes {#release-notes}


>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="What's new?"
>abstract="**Adobe Journey Optimizer** continuously delivers new features, enhancements to existing features, and bug fixes. All changes are consolidated on the last week of each month in these release notes."

[!DNL Adobe Journey Optimizer] continuously delivers new features, enhancements to existing features, and bug fixes. All changes are consolidated on the last week of each month in these release notes. 

Previous release notes are available in [this page](release-notes-2023.md). You can also consult the [latest documentation updates](documentation-updates.md) page for more changes.

[!DNL Adobe Journey Optimizer] is built natively on [!DNL Adobe Experience Platform] and inherits from its latest innovations and improvements. Learn more about these changes in [Adobe Experience Platform Release Notes](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html){target="_blank"}.

![Newsletter](../assets/do-not-localize/nl-icon.png) Sign up for the [Adobe Journey Optimizer quarterly newsletter](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"} today, and receive the latest product updates, exciting stories, use cases, tips and more delivered directly to your inbox every quarter.

## October 2023 release notes {#oct-rn-2023}

### New capabilities{#oct-2023-features}

This release brings the new capabilities listed below.

<table>
<thead>
<tr>
<th><strong>Sandbox tooling</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sandbox tooling allows you to copy objects across multiple sandboxes by leveraging package export and import. A package can consist of a single object or multiple objects. Any objects that are included in a package must be from the same sandbox.</p>
<!--img src="../data/assets/dataset-export-setup.png"-->
<p>For more information, refer to the <a href="../building-journeys/copy-to-sandbox.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>

<!-- table>
<thead>
<tr>
<th><strong>Composed audiences in journeys</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now use audiences created in composition workflows in your journeys to target customers. Once an audience composition is published, and the audience saved, use a Read Audience activity to select this new audience in your journey canvas.</p>
<img src="assets/channel-reports.png"/>
<p>For more information, refer to the <a href="../audience/get-started-audience-orchestration.md">detailed documentation</a>.</p>
</tr>
</tbody>
</table -->

<table>
<thead>
<tr>
<th><strong>Multimedia Message Service (MMS) in SMS</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>With the SMS Channel, you can now enhance your communication by sending Multimedia Message Service (MMS) messages, enabling the sharing of images, GIFs, or videos with your customers. Note that this feature is currently available with Sinch only.</p>
<img src="assets/do-not-localize/mms.gif"/>
<p>For more information, refer to the <a href="../sms/create-sms.md#mms-content">detailed documentation</a>.</p>
</tr>
</tbody>
</table>

### Improvements {#oct-2023-improvements}

This release comes with the improvements listed below.

**Audiences**

* You can now target audiences uploaded from a CSV file into journeys and campaigns. [Learn more](../audience/about-audiences.md#segments-in-journey-optimizer)
* You can now target audiences created through audience composition and leverage enrichment attributes in Journeys. [Learn more](../building-journeys/read-audience.md)

>[!AVAILABILITY]
>
>These capabilities are currently available as a private beta.

<!--
**Spam scoring for emails**

* When simulating an email content, a new option enables you to check how your content performs against inboxes spam filtering. This feature is currently proposed to a set of customers only (Limited Availability), and available for the Email channel.--> 

**Campaigns**

<!--* You can now stop a live one-time campaign, make modifications and resume it again. This improvement is available in Beta.-->
* When an error occurs within one of your campaigns, a warning icon now appears in the campaigns list alongside the campaign's status. [Learn more](../campaigns/modify-stop-campaign.md#statuses)

**Journeys**

* The maximum duration that you can define in any wait time is now 29 days instead of 30. This improvement has been introduced to prevent wait durations from exceeding the 30 days journey lifespan. This applies to:

   * the **Amount of Time** field in the [wait activity](../building-journeys/wait-activity.md)
   * the **Re-entrance wait period** in [journey properties](../building-journeys/journey-gs.md#entrance)
   * the **Wait for** field in the timeout definition of [event activities](../building-journeys/general-events.md#events-specific-time).

<!--
**Consent in channel configuration**

* You can now select a marketing action at the channel surface level. When used in a surface, all consent policies associated with that marketing action are leveraged in order to respect the preferences of your customers.-->

**Decision management**

* Several labels relating to offer capping in the decision management interface have been updated. [Learn more](../offers/offer-library/add-constraints.md#capping)


---
title: Release notes
description: Journey Optimizer Release notes
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
---
# Release Notes {#release-notes}

This page lists all the new features and improvements for [!DNL Journey Optimizer]. You can also consult the [latest documentation updates](documentation-updates.md) page for more changes.

[!DNL Adobe Journey Optimizer] is built natively on [!DNL Adobe Experience Platform] and inherits from its latest innovations and improvements. Learn more about these changes in [Adobe Experience Platform Release Notes](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html){target="_blank"}.

![Newsletter](../assets/do-not-localize/nl-icon.png) Sign up for the [Adobe Journey Optimizer quarterly newsletter](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"} today, and receive the latest product updates, exciting stories, use cases, tips and more delivered directly to your inbox every quarter.

## September 2022 Release{#sept-2022-release}

### New capabilities{#sept-2022-features}


<table>
<thead>
<tr>
<th><strong>New Dynamic Expression Builder</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now create conditional content blocks across different authoring services to personalize your content.</p>
<p>In addition to the Personalization Expression Library, the Expression Editor provides a new Conditional Rule Builder to help you design and save your content blocks.</p>
<p>For more information, refer to the <a href="../building-journeys/read-segment.md#configuring-segment-trigger-activity">detailed documentation</a>.
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Data Access Control</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Through attribute-based access control, administrators can control access to specific objects based on certain attributes. These attributes can be metadata added to an object, such as labels. Starting this release, administrators can also define user roles that have access to only specific fields and/or objects, and data that correspond to those fields and/or objects.</p>
<p>For more information, refer to the <a href="../building-journeys/read-segment.md#configuring-segment-trigger-activity">detailed documentation</a>.
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Data Governance and Privacy</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>With its Data Usage Labelling and Enforcement (DULE) governance framework, Journey Optimizer can now leverage Adobe Experience Platform governance policies to prevent sensitive fields from being exported to third-party systems through custom actions. If the system identifies a restricted field in the custom action parameters, an error is displayed preventing you from publishing the journey.</p>
<p>For more information, refer to the <a href="../building-journeys/read-segment.md#configuring-segment-trigger-activity">detailed documentation</a>.
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Permission Management</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer supports defining user roles and access policies to manage permissions for features and objects. Through <strong>Adobe Experience Cloud Permissions</strong>, you can create and manage roles, as well as assign the desired resource permissions for these roles. Permissions also allow you to manage the labels, sandboxes, and users associated with a specific role.</p>
<p>For more information, refer to the <a href="../building-journeys/read-segment.md#configuring-segment-trigger-activity">detailed documentation</a>.
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Alerting and Monitoring</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>As a Journey Optimizer user, you can now access system alerts through the user interface. You can view the available alerts and subscribe to them. For Journey Optimizer, we provide a pre-configured alert which will warn you if a Read Segment activity has not processed any profile during the defined time frame.</p>
<p>For more information, refer to the <a href="../building-journeys/read-segment.md#configuring-segment-trigger-activity">detailed documentation</a>.
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Data Hygiene</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Experience Platform provides a suite of data hygiene capabilities that allow you manage your stored data through programmatic deletions of consumer records and datasets. This capability is now available for Adobe Journey Optimizer. </p>
<p>You can manage your data stores to ensure that information is used as expected, is updated when incorrect data needs fixing, and is deleted when organizational policies deem it necessary.</p>
<p><strong>Caution</strong> - Data Hygiene capabilities are currently only available for organizations that have purchased the Healthcare Shield add-on offering.</p>
<p>For more information, refer to the <a href="../building-journeys/read-segment.md#configuring-segment-trigger-activity">detailed documentation</a>.
</td>
</tr>
</tbody>
</table>

### Improvements{#sept-2022-improvements}

**Journeys**

*  The **Entity Dataset** is now available as an out-of-the-box dataset in Adobe Journey Optimizer. This lookup dataset includes meta data to enrich the tracking and feedback datasets information. This will help you improve your reports and queries with more comprehensible data.
* A new guardrail has been added to unitary journeys (starting with an event or a segment qualification) to prevent journeys from being erroneously triggered multiple times for the same event. Profile re-entrance will now be temporally blocked by default for 5 minutes.	

**Administration**

* When enabling or disabling the allowed list, a new warning now displays to detail impacts when enabling/disabling the allowed list. Learn more
* The user interface for creating channel surfaces has been updated. Learn more
* The user interface for enabling/disabling and adding emails/domains to the allowed list has been updated.	Learn more

**Audit controls**

* With Journey Optimizer, you can identify actions performed by users in the system on various services and capabilities like campaigns, journeys, messages, landing pages etc. Audit log resources now include changes on various other actions, and are recorded automatically as the activity occurs. Learn more

**Archiving**

* Journey Optimizer now comes with a new capability to export your message templates, and archive the format and the structure of the message, without personal data. Learn more

**Landing pages**

* The user interface for creating landing page presets and landing page subdomains has been improved. Learn more

### Other changes{#sept-2022-other}

* Journey Burst Mode has been replaced by Campaign Rapid delivery mode. Learn more
* To improve performance, Experience event field groups can not longer be used in journeys starting with a Read segment or Segment qualification activity. This change only applies to new journeys. Existing ones will keep the current behaviour.	

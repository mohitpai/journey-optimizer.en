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
<th><strong>HIPAA Compliance</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer enables compliance with the the Health Insurance Portability and Accountability Act (HIPAA).</p>
<p>HIPAA readiness capabilities include:</p>
<ul>
<li>Data access control</li>
<li>Data usage labelling governance</li>
<li>Audit controls</li>
<li>Archiving capabilities for all channels</li>
<li>Refined permissions management</li>
<li>Data hygiene</li>
<li></li>
</ul>
<p>Caution: some of these capabilities are available through a specific Healthcare Shield add-on offering, available in the US only.</p> 
<p>For more information, refer to the <a href="../building-journeys/read-segment.md#configuring-segment-trigger-activity">detailed documentation</a>.
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Alerting and monitoring</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>As a Journey Optimizer user, you can now access system alerts through the user interface. You can view the available alerts and subscribe to them. For Journey Optimizer, we provide a pre-configured alert which will warn you if a Read Segment activity has not processed any profile within the allotted threshold.</p>
<p>For more information, refer to the <a href="../building-journeys/read-segment.md#configuring-segment-trigger-activity">detailed documentation</a>.
</td>
</tr>
</tbody>
</table>


### Improvements{#sept-2022-improvements}

**Landing pages**

* The user interface for creating landing page presets and landing page subdomains has been improved. Learn more

**Journeys**

* A new guardrail has been added to unitary journeys (starting with an event or a segment qualification) to prevent journeys from being erroneously triggered multiple times for the same event. Profile re-entrance will now be temporally blocked by default for 5 minutes.	

*  The **AJO Entity Dataset** is now available as an out-of-the-box dataset in Adobe Journey Optimizer. This dataset denormalises the data such that you can easily join feedback/tracking datasets to this dataset to get meaningful information like subject/title/messageName, etc.

**Administration**

* When enabling or disabling the allowed list, a new warning now displays to explain more clearly the implications of enabling/disabling the allowed list. Learn more
* The user interface for creating channel surfaces has been updated. Learn more
* The user interface for enabling/disabling and adding emails/domains to the allowed list has been updated.	Learn more

### Other changes{#sept-2022-other}

* Journey Burst Mode has been replaced by Campaign Rapid delivery mode. Learn more
* To improve performance, Experience event field groups can not longer be used in journeys starting with a Read segment or Segment qualification activity. This change only applies to new journeys. Existing ones will keep the current behaviour.	
	
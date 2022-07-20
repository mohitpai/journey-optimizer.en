---
title: Release notes
description: Journey Optimizer Release notes
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
---
# Release Notes {#release-notes}

This page lists all the new features and improvements for [!DNL Journey Optimizer]. You can also consult the [latest documentation updates](documentation-updates.md) page for more changes.

[!DNL Adobe Journey Optimizer] is built natively on [!DNL Adobe Experience Platform] and inherits from its latest innovations and improvements. Learn more about these changes in [Adobe Experience Platform Release Notes](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html){target="_blank"}.

![Newsletter](../assets/do-not-localize/nl-icon.png) Sign up for the [Adobe Journey Optimizer quarterly newsletter](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"} today, and receive the latest product updates, exciting stories, use cases, tips and more delivered directly to your inbox every quarter. 

## July 2022 Release {#july-2022-release}

### New capabilities 

<table>
<thead>
<tr>
<th><strong>New message authoring flow</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer provides a new flow for message authoring in Journeys and Campaigns. Existing messages must be migrated to this new stack.</p>
<p>For more information, refer to the <a href="inline-messages.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Attribute-based access control (limited availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now identify schema fields with labels that define organizational or data usage scopes. Administrators can use the Permeissions interface to define access policies covering XDM schema fields and better manage the access given to users or groups of users (internal, external, or third-party users), and manage access to specific types of data (i.e. Sensitive Personal Data/SPD).</p>
<p>The use of Attribute-based access control is currently restricted to selected users, and will be deployed to all environments in a future release.</p>
<p>For more information, refer to the <a href="inline-messages.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Batch decisioning jobs</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now run batch decisioning jobs from the user interface, so that I do not need a developer to run batch api jobs and I can reduce the time needed for marketing. This new interface allows you to create jobs and manage current/past jobs.</p>
<p>For more information, refer to the detailed documentation.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Automatically use the best performing offer in your decisions (limited availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now use personalized optimization model systems in Decision Management. This new type of model allows you to optimize and personalize offers based on segments and offer performance.</p>
<p>The use of personalized optimization AI models is currently restricted to selected users, and will be deployed to all environments in a future release.</p>
<img src="assets/do-not-localize/ai-ranking.gif"/>
<p>For more information, refer to the <a href="../offers/ranking/personalized-optimization-model.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>

### Improvements

**Journeys**

* **Ending a journey** - In the journey canvas, the **End** activity has been removed from the palette. End tags are now added by default at the end of each path and cannot be removed. This improvement allows better reporting of where a customer dropped out of the journey, without any action from the user.

**Messages**

* Message presets are now **surfaces**.

**Administration**

* **Allowed list in the UI** - You can now use the Journey Optimizer user interface to add new email addresses or domains to the allowed list.

* **Allowed list logic update** - Now the allowed list logic applies as soon as the feature is enabled, even if the list is empty. However when the list is empty, no email is sent out.	

* **Personalize URL parameters** - You can now use the Expression Editor to configure URL tracking parameters in your message surfaces (i.e message presets). [Learn more](../configuration/email-settings.md#url-tracking)

    This improvement also applies when adding URLs as content to your offers' representations.

**Reporting**

* **Performance measurement** - A new **Reporting** tab is now available in the Administration > Configurations menu to set up reporting data sources.

**Offer Decisioning**

* **Audience size** - A new audience size estimate component is now displayed in the user interface when creating a rule, when selecting a segment or a rule to set an offer eligibility, or when adding a segment or a rule to a decision scope.
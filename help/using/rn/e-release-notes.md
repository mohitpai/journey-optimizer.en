---
solution: Journey Optimizer
product: journey optimizer
title: Release notes
description: Journey Optimizer early Release notes
hide: yes
hidefromtoc: yes
---
# Early release notes {#e-release-notes}

[!DNL Adobe Journey Optimizer] continuously delivers new features, enhancements to existing features, and bug fixes. All changes are consolidated on the last week of each month in the [release notes](release-notes.md). 

Early release notes below are subject to change without prior notice until the release availability date. Links, screens and updated documentation are published  in the [release notes](release-notes.md), at the release date.

## September 2023 early release notes {#sept-rn-2023}

**Release date**: Sept 26-27, 2023

### New capabilities{#sept-2023-features}

This release brings the new capabilities listed below.


<table>
<thead>
<tr>
<th><strong>Consolidated Channel Reports</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>The Channel Report feature offers analysts and marketers a comprehensive overview of traffic and engagement metrics at the channel level. To access the 'Report' menu, you must have the 'View Channel Reports' permission.</p>
<img src="assets/channel-reports.png"/>
<!--p>For more information, refer to the <a href="../in-app/get-started-in-app.md">detailed documentation</a>.</p-->
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Dataset Export Destinations (GA)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer datasets export to Cloud Storage Destinations is now generally available. This feature allows you to establish a live connection with cloud storage locations in order to export the content of your datasets.</p>
<img src="../data/assets/dataset-export-setup.png">
<!--p>For more information, refer to the <a href="../audience/get-started-audience-orchestration.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Per-Sandbox mobile application credentials storage</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>This new feature allows you to easily manage and associate push credentials with a dedicated sandbox in App Surfaces.</p>
<p>For more information, refer to the <a href="../in-app/inapp-configuration.md">detailed documentation</a>.</p>
</tr>
</tbody>
</table>

### Improvements {#sept-2023-improvements}

This release comes with the improvements listed below.

<!--**Audiences**

* You can now target audiences uploaded from a CSV file into journeys and campaigns.
* You can now target audiences resulting from composition workflows into journeys. -->

**Personalization**

* In addition to visual fragments, it is now possible to create, save and reuse expression fragments from the Journey Optimizer interface through the Expression Editor. Expression fragments replace the previously saved expressions.    
* You can now use Adobe Experience Platform computed attributes for personalization in Journey Optimizer. Computed attributes are aggregated values that are computed based on Profile-enabled Experience Event datasets ingested into Adobe Experience Platform.    

**Alerting**

* Two new types of system alerts have been introduced. You can now get notified when a custom action or read segment fails.

**Web channel**

* You can now select which specific views your want to apply your web page modifications to. A view can be defined as a whole site or a group of visual elements on a site, such as the home page, the entirety of the products site or the delivery preferences frame on all the checkout pages.  
* When editing a page using the web designer, you can now add new changes to your content directly from the Modifications pane - without the need to select a component and edit it from the designer interface.
* When setting up web subdomains, you now have the option of adding you own subdomain - in addition to using a subdomain already delegated to Adobe.    

**Journeys**

* The custom action response capabilities are now GA. This allows you to leverage API call responses in custom actions and orchestrate your journey based on these responses. In addition, a new guardrail has been added to limit all customs actions to 5000 calls/s per endpoint.
* When duplicating a journey, you can now define the name of the journey copy.
* The maximum duration that you can define in the Wait activity is now 29 days instead of 30.

**Email channel**

A new option in the email surface configuration allows to choose to send transactional messages to profiles even if their email addresses are on the Adobe Journey Optimizer suppression list.    

<!--**Decision management**

Enhancements have been made to the audience picker in journeys or campaigns, with the addition of new columns displaying the origin and update frequency of audiences.    -->
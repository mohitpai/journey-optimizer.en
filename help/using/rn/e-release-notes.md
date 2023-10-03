---
solution: Journey Optimizer
product: journey optimizer
title: Release notes
description: Journey Optimizer early Release notes
hide: yes
hidefromtoc: yes
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
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

<table>
<thead>
<tr>
<th><strong>Computed attributes</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Computed attributes enables capability to easily summarize event data into profile attributes via an intuitive user interface for enhanced behavior-based segmentation, personalization, and activation. With this feature, you can create computed attributes in a self serve manner, manage them, and use them in segmentation, Real-time Customer Profile destinations or Journey Optimizer.<br/><br/>
Additionally, computed attributes simplifies segmentation and journey workflows to help you seamlessly deliver relevant experiences. Learn more in the <a href="https://experienceleague.adobe.com/docs/experience-platform/profile/computed-attributes/overview.html">detailed documentation</a>.</p>
<img src="assets/do-not-localize/computed-attributes.gif">
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

**Alerting**

* A new type of system alert has been introduced. You can now get notified when a read audience fails.

**Web channel**

* Single-page applications (SPAs) can be now authored in the web designer visual editor, which allows you to select which specific views you want to apply your web page modifications to. A view can be defined as a whole site or a group of visual elements on a site, such as the home page, the entirety of the products site or the delivery preferences frame on all the checkout pages. To create and run Adobe Journey Optimizer web campaigns on SPAs, one-time developer setup is needed to define the views in the Adobe Experience Platform Web SDK implementation.

* When editing a page using the web designer, you can now add new changes to your content directly from the **Modifications** pane - without the need to select a component and edit it from the designer interface.
* When setting up web subdomains, you now have the option of adding you own subdomain - in addition to using a subdomain already delegated to Adobe.    

**Journeys**

* Support of custom action responses is now GA. This allows you to leverage API call responses in custom actions and orchestrate your journey based on these responses. In addition, a new guardrail has been added to limit all customs actions to 5000 calls/s per endpoint.
* When duplicating a journey, you can now define the name of the journey copy.

<!--
* The maximum duration that you can define in the Wait activity is now 29 days instead of 30.
-->

**Email channel**

A new option in the email surface configuration allows to choose to send transactional messages to profiles even if their email addresses are on the Adobe Journey Optimizer suppression list.   

**SMS channel**

Two new fields, **Opt-in message** and **Help message**, have been added to the API configuration screen, allowing users to customize responses for inbound keywords. Note that this is only available for Sinch SMS provider.

**Reporting**

You can now export Journey Optimizer reports as CSV file. [Learn more](../reports/global-report.md#export-reports)

<!--**Decision management**

Enhancements have been made to the audience picker in journeys or campaigns, with the addition of new columns displaying the origin and update frequency of audiences.    -->

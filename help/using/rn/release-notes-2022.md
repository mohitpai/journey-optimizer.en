---
title: Release notes
description: Journey Optimizer Release notes
---
# Release Notes {#release-notes}

This page lists all the features and improvements for [!DNL Journey Optimizer] released in 2022. 

The latest release notes are available [in this page](release-notes.md).

## April 2022 Release {#april-2022-release}

### Improvements

**Landing pages** 

* **New option for opt-in/opt-out checkboxes** - You can now insert a single checkbox for opt-in/opt-out in subscription landing pages. Users need to check the box to consent (opt-in), and uncheck it to remove their consent (opt-out). [Learn more](../landing-pages/design-lp.md#define-lp-specific-content)

* **Pre-fill landing pages fields** - It is now possible to give users the ability to pre-fill the landing page fields with profile information. [Learn more](../landing-pages/create-lp.md#configure-primary-page)

**Decision Management**

* **Decisioning API on Edge** - Edge Decisioning API can deliver and render personalized offers that are managed in Offer Decisioning. You can create your offers and other related objects using the Offer Decisioning user interface (UI) or APIs. [Learn more](../offers/api-reference/offer-delivery-api/edge-decisioning-api.md)

**Administration**

* **PTR submit duration** - The duration for PTR edit to be effective is now a few hours. [Learn more](../configuration/ptr-records.md#processing)

**Email Design**

* **20 new email templates** are now available to design your email content in Journey Optimizer.

**User interface**

* **Contextual help in Journey Optimizer UI** - Contextual help links have been added to multiple pages in Journey Optimizer. When available, click the "i" icon to view a quick description of the current functionality and access related articles.	

**Integration with Adobe Campaign Standard**

As an Adobe Campaign Standard customer, you can now send emails, push notifications and SMS using Journey Optimizer. Use the new built-in actions to leverage Campaign Standard Transactional Messaging capabilities into Journey Optimizer.  [Learn more](../action/acs-action.md)

<!--
### Fixes

* Fixed an issue which caused tracking reports not to be available as the `JourneyActionId` was not properly populated. PLATIR-19854, CJM-26006
* Fixed an error on business events which could block the journey publication. CJM-25931
* Fixed an issue which could prevent images in Email Designer templates from being displayed. PLATIR-18176, CJM-25008
-->

## March 2022 Release {#march-2022-release}

### Improvements

**Journeys**

* To avoid having unnecessary fields in the unified profile schema, the Journey Step Event schema is no longer enabled for profiles by default. If needed, you can activate it. [Learn more](../reports/sharing-overview.md)
* New step events related to export jobs are now sent by Journey Optimizer to Adobe Experience Platform. Examples of queries have been added to documentation. [Learn more](../reports/query-examples.md)

**Decision Management**

* You can now specify if offer capping is applied across all users or to one specific profile, and to all placements or per placement. [Learn more](../offers/offer-library/add-constraints.md#capping)
* The Batch Decisioning API allows organizations to use offer decisioning functionality for all profiles in a given segment in one call. The offer content for each profiles in the segment is placed in an AEP dataset where it is available for custom batch workflows. [Learn more](../offers/api-reference/offer-delivery-api/batch-decisioning-api.md)

**Administration**

* You can now enable/disable the unsubscribe link in/from the email header at the message preset level, and set a custom unsubscribe URL at the message level. [Learn more](../configuration/message-presets.md#list-unsubscribe)
* The allowed list will can now be enabled and disabled through the [!DNL Journey Optimizer] interface on production and non-production sandboxes. [Learn more](../reports/allow-list.md#enable-allow-list)

**Personalization**

* You can now save more than 40 personalization expressions in the library. [Learn more](../personalization/personalization-library.md)

## February 2022 Release {#feb-2022-release}

### New capabilities 

<table>
<thead>
<tr>
<th><strong>Subscription Landing Pages</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now create and design landing pages in Journey Optimizer, and direct your users to online forms where they can opt-in or opt-out from receiving your communications, or subscribe to a specific service such as a newsletter.</p>
<p>For more information, refer to the <a href="../landing-pages/create-lp.md">detailed documentation</a> and related <a href="../landing-pages/lp-use-cases.md">sample use case</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>New Personalization Expression Library</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer now provides a library where you can access predefined personalization expressions. These expressions are configured by Admin users.</p>
<p>For more information, refer to the <a href="../personalization/personalization-library.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>


<!--table>
<thead>
<tr>
<th><strong>API Developer Site and Suppression API</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer provide RESTful APIs that allow you to programmatically perform key operations in your applications.
Developer SDK for Journey Optimizer is now available with the Suppression API (beta).</p>
<p>With this API, you can control your outgoing messages using suppression and allow lists.
The suppression list helps you with honoring the ISPs’ feedback to preserve sending IP reputation. The allow list helps you ensure that you send only to those email addresses which are in the allowed list, and typically to ensure that you don't send mails to customers from your development sandbox.</p>
<p>See <a href="https://developer.adobe.com/journey-optimizer-apis/">Adobe Journey Optimizer APIs</a>.</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Pass information to track your messages with UTM Tracking Parameters</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>In Journey Optimizer message content, you can now add UTM parameters to your links: they can provide additional data about that link, and help you identify where and why a person clicked on your link.</p>
<p>For more information, refer to the <a href="../configuration/message-presets.md#configure-email-settings">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>

### Improvements

**Journeys**

* To optimize performance, all journeys in test mode that have not been triggered for a week will now switch back to the Draft status. [Read more](../building-journeys/testing-the-journey.md#important_notes)
* The integration between Journey Optimizer and Adobe Campaign Classic has been optimized to improve performance. The capping default configuration has been changed to 4000 calls / 5 minutes.	[Read more](../action/acc-action.md#important-notes)

**Reporting**

* Deliveries can now be filtered depending on their status:
    * From the Message Execution list, you can now exclude proofs from your deliveries' list.
    * From your Live/Global reports, you can choose to exclude test events.

* You can now access to reports on Send Time Optimization data: the number of persons who were messages immediately and the number of persons who were messaged with 1-hour optimization, 2 hours optimization, etc.

<!--* Offer Decisioning reports are now available in Journey Optimizer. You can access the following metrics: Offers sent - Offers' impression rate - Offers' click rate - Breakdown report on Offers' sent.-->

**Decision Management**

* Rankings and AI ranking are now grouped together into a single tab.	

## January 2022 Release {#january-2022-release}

### New capabilities 

<table>
<thead>
<tr>
<th><strong>Journeys - Optimize your IP ramp up with Profile cap conditions</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>When configuring a <strong>Condition</strong> activity in a journey, you can now define a profile cap. This new condition type allows you to set a maximum number of profiles for a journey path. When this limit is reached, the entering profiles take an alternate path. This allows you to ramp up the volume of your deliveries (IP ramp up). For example, you may want to ramp up your deliveries on a domain by splitting the execution: send 1000 messages on day 1, 2000 on day 2, etc.</p>
<p>For more information, refer to the <a href="../building-journeys/condition-activity.md#profile_cap">detailed documentation</a> and related <a href="../building-journeys/ramp-up-deliveries-uc.md">sample use case</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journeys - Read segment improvement</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>The <strong>Incremental read</strong> option has been added to recurring <strong>Read Segment</strong> activities. This option allows you to only target the individuals who entered the segment since the last execution of the journey. The first execution always targets all segment members.</p>
<p>For more information, refer to the <a href="../building-journeys/read-segment.md#configuring-segment-trigger-activity">detailed documentation</a>.
</td>
</tr>
</tbody>
</table>

### Improvements

**Journeys**

* Journey Optimizer step events can now be linked to other datasets in [Adobe Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html). The **profileID** field, in the built-in Journey Step Event schema, is now defined as an identity field. [Learn more](../reports/sharing-overview.md#integration-cja)

**Offer Decisioning**

* When you update an offer, fallback offer, offer collection, or offer decision which is directly or indirectly referenced in a published message, the updates are now automatically reflected in the corresponding message, without the need to republish it. [Learn more](../offers/offers-e2e.md#insert-decision-in-email)

* When simulating which offers will be delivered for a given test profile, you can now modify the default simulation settings, and view the code corresponding to your simulations that can be used for troubleshooting purpose. [Learn more](../offers/offer-activities/simulation.md#define-simulation-settings)

**Administration**

* Administrators can now edit PTR records with a CNAME set up subdomain. [Learn more](../configuration/ptr-records.md#edit-ptr-subdomains-cname)

**Personalization**

* **Add to favorites** - To help improve efficiency when working with personalization we’ve introduced the concept of saving favorites. Adding different attributes to your favorites menu provides quick access to your most frequency used items. [Learn more](../personalization/personalize.md#fav)

---
title: Permission levels
description: Learn about high and low level permissions
topic: Administration
role: Admin
level: Intermediate
exl-id: 1b286f9d-43ef-4b80-b4ee-136da857bb95
---
# Permission levels {#high-low-permissions}

![](../assets/do-not-localize/permissions.png)

Each product profile is composed of permissions allowing users to access the different features. 
They can be divided into two types:

* **High-level permission**: represents the different permissions that can be assigned to **[!UICONTROL Product profile]** in the [!DNL Admin console], such as **[!DNL Publish journeys]** and **[!DNL Manage subdomains delegation]**. High level permissions encompass low level permissions.

* **Low-level permission**: represents the different permissions that come from the high level permission.

For example, the **[!DNL Journey administrator]** product profile is assigned the **[!DNL Manage journeys]** permission. From this permission results the low-level permissions which will allow the Journey administrator to write, read and delete journeys.

## Journey capability {#journey-capability}

### [!DNL Manage journeys] permission {#manage-journeys}

The **[!DNL Manage journeys]** high-level permission allows users to create new and edit/delete existing Journeys, as well as access to the objects that are used in the journey canvas to build the journey flow.

It includes the following low-level permissions: 

* Journey Optimizer specific:

  * journeys.read
  * journeys.write
  * journeys.delete
  * messages.read

* Adobe Experience Platform specific:

  * segments.read
  * profiles.read
  * datasets.read
  * schemas.read

### [!DNL Publish journeys] permission {#publish-journeys}

The **[!DNL Publish journeys]** high-level permission allows users to publish journeys.

It includes the following low-level permissions: 

* Journey Optimizer specific:
  * journeys.publish
  * journeys.read

### [!DNL View journeys] permission {#view-journeys}

The **[!DNL View journeys]** high-level permission allows users to browse and view journeys.

It includes the following low-level permissions: 

* Journey Optimizer specific:
  * journeys.read

* Adobe Experience Platform specific:
  * segments.read
  * profiles.read

### [!DNL Manage journeys events, data sources and actions] permission {#manage-journeys-events}

The **[!DNL Manage journeys events, data sources and actions]** high-level permission allows users to configure event and data configurations.

It includes the following low-level permissions: 

* Journey Optimizer specific:
  * journeys_events.read
  * journeys_events.write
  * journeys_events.delete
  * journeys_data_sources.read
  * journeys_data_sources.write
  * journeys_data_sources.delete 
  * journeys_actions.read
  * journeys_actions.write
  * journeys_actions.delete

* Adobe Experience Platform specific:
  * schemas.read
  * datasets.read
  * identity_namespace.read

### [!DNL View journeys events, data sources and actions] permission {#view-journeys-event}

The **[!DNL View journeys events, data sources and actions]** high-level permission allows users to use event and data in the journey flow.

It includes the following low-level permissions:

* Journey Optimizer specific: 
  * journeys_events.read
  * journeys_data_sources.read
  * journeys_actions.read

* Adobe Experience Platform specific:
  *  schemas.read
  * datasets.read
  * identity_namespace.read

### [!DNL View journeys report] permission {#view-journeys-report}

The **[!DNL View journeys report]** high-level permission allows users to read-only journey report.

It includes the following low-level permissions: 

* Journey Optimizer specific: 
  * journeys_report.read
  * messages_report.read

* Adobe Experience Platform specific:
  * datasets.read
  * queries.read
  * queries.write
  * queries.delete

## Message capability {#message-capability}

### [!DNL Manage messages] permission {#manage-messages}

The **[!DNL Manage messages]** high-level permission allows users to create and edit/delete message.

It includes the following low-level permissions:

* Journey Optimizer specific: 
  *  messages.write
  * messages.read
  * messages.delete
  * messages_presets.read

* Adobe Experience Platform specific:
  * segments.read
  * schemas.read 

### [!DNL Manage messages preview and test] permission {#mange-messages-preview}

The **[!DNL Manage messages preview and test]** high-level permission allows users to preview personalized message.

It includes the following low-level permissions: 

* Journey Optimizer specific: 
  * messages.publish
  * messages_preview_and_test.write
  * messages.publish

* Adobe Experience Platform specific:
  * profiles.read
  * profiles.write
  * schemas.read
  * datasets.write
  * datasets.read
  * identity_namespace.read
  * segments.read
  * queries.write
  * merge_policies.read

### [!DNL Publish messages] permission {#publish-messages}

The **[!DNL Publish messages]** high-level permission allows users to publish messages.

It includes the following low-level permissions:

* Journey Optimizer specific: 
  * messages.publish

* Adobe Experience Platform specific:
  * profiles.read
  * schemas.read
  * datasets.read

### [!DNL View messages] permission {#view-messages}

The **[!DNL View messages]** high-level permission allows users to read messages only.

It includes the following low-level permissions:

* Journey Optimizer specific: 
  * messages.read
  * messages_presets.read

* Adobe Experience Platform specific:
  * schemas.read 
  * segments.read

### [!DNL View messages report] permission {#view-message-reports}

The **[!DNL View messages report]** high-level permission allows users to to read-only email and push report.

It includes the following low-level permissions:

* Journey Optimizer specific:
  * messages_report.read
  * datasets.read
  * queries.read
  * queries.write
  * queries.delete
  * journey.read

## Decision management capability {#decisions-permissions}

### [!DNL Manage decisions] permission {#manage-decisioning}

The **[!DNL Manage decisions]** high-level permission allows users to create new and edit/delete existing **[!DNL Activity entities]**, as well as manage the objects that are used in those activities to make the decisions.

It includes the following low-level permissions: 

* Decision management specific:
  * activities.read
  * activities.write
  * activities.delete
  * offers.read
  * offers.write
  * offers.delete
  * placements.read
  * placements.write
  * placements.delete
  * ranking_strategy.read

* Adobe Experience Platform specific:
  * datasets.read
  * datasets.write
  * datasets.delete
  * schemas.read
  * profile.read
  * segments.read

### [!DNL View decisions] permission {#view-decisions}

The **[!DNL View decisions]** high-level permission allows users to use an existing Activity and related business objects to make the decisions. 

It includes the following low-level permissions: 

* Decision management specific: 
  * activities.read
  * offers.read
  * placements.read
  * ranking_strategy.read

* Adobe Experience Platform specific:
  * schemas.read
  * segment.read
  * datasets.read
  * datasets.write
  * datasets.delete

### [!DNL Publish offers decisioning] permission {#publish-decisions}

The **[!DNL Publish offers decisioning]** high-level permission allows users to access to approve/un-approve Offer activities.

It includes the following low-level permissions: 

* Decision management specific:
  * offers_activity.read
  * offers.read
  * offers.write
  * offers.delete
  * placements.read
  * placements.write
  * placements.delete
  * ranking_strategy.read

* Adobe Experience Platform specific:
  * schemas.read
  * segment.read 
  * datasets.read
  * profiles.read

### [!DNL Manage ranking strategies] permission {#manage-decisions}

The **[!DNL Manage ranking strategies]** high-level permission allows users to read, create, edit, and delete custom messages report and use action features.

It includes the following low-level permissions: 

* Decision management specific:
  * ranking_strategy.read
  * ranking_strategy.write
  * ranking_strategy.delete
  * activities.read
  * offers.read
  * placements.read

## Administration capability {#administration-permissions}

### [!DNL Manage subdomains delegation] permission {#manage-subdomain}

The **[!DNL Manage subdomains delegation]** high-level permission allows users to create, edit and delete subdomain delegations (including IP pool).

It includes the following low-level permissions: 

* subdomains_delegation.read
* subdomains_delegation.write
* subdomains_delegation.delete

### [!DNL Manage PTR records] permission {#manage-ptr}

The **[!DNL Manage PTR records]** high-level permission allows users to read and edit PTR records that have been configured based on the subdomain.

It includes the following low-level permissions:

* PTR_records.read
* PTR_records.write
* subdomains_delegation.read

### [!DNL View PTR records] permission {#view-ptr}

The **[!DNL View PTR records]** high-level permission allows users to view PTR records that have been configured based on the subdomain.

It includes the following low-level permissions:

* PTR_records.read
* subdomains_delegation.read

### [!DNL Manage IP pools] permission {#manage-ip-pools}

The **[!DNL Manage IP pools]** high-level permission allows users to create, edit and delete the affinity definition.

It includes the following low-level permissions: 

* IP_pools.read
* IP_pools.write
* IP_pools.delete

### [!DNL Manage messages general settings] permission {#manage-message-settings}

The **[!DNL Manage messages general settings]** high-level permission allows users to create, edit and delete global settings at the sandbox level.

It includes the following low-level permissions: 

* Journey Optimizer specific: 
  * messages_general_settings.read
  * messages_general_settings.write
  * messages_general_settings.delete
* Adobe Experience Platform specific:
  * schemas.read

### [!DNL View messages general settings] permission {#view-message-settings}

The **[!DNL View messages general settings]** high-level permission allows users to view messages general settings such as the execution address.

It includes the following low-level permissions:

* Journey Optimizer specific: 
  * messages_general_settings.read
* Adobe Experience Platform specific: 
  * schemas.read

### [!DNL Manage messages presets] permission {#manage-message-presets}

The **[!DNL Manage messages presets]** high-level permission allows users to create, edit and delete message presets across channels at the sandbox level.

It includes the following low-level permissions: 

* Journey Optimizer specific:
  * messages_presets.read
  * messages_presets.write
  * messages_presets.delete
  * subdomains_delegation.read
  * IP_pools.read
  * mobile_setting.read (from Adobe Experience Platform Launch)

### [!DNL View messages presets] permission {#view-message-presets}

The **[!DNL View messages presets]** high-level permission allows users to view message presets in order to know which messages presets to use when creating a message. 

It includes the following low-level permissions: 

* messages_presets.read
* subdomains_delegation.read
* IP_pools.read
* mobile_setting.read (from Adobe Experience Platform Data Collection)

### [!DNL Manage suppression] permission {#manage-suppression}

The **[!DNL Manage suppression]** high-level permission allows users to define the number of bounces before an email address is added to the suppression list, as well as to add and delete entries to/from the suppression list.

It includes the following low-level permissions: 

* suppression_rules.read
* suppression_rules.write
* suppression_rules.delete
* suppression_list.write
* suppression_list.delete

### [!DNL View suppression list] permission {#view-suppression-list}

The **[!DNL View suppression list]** high-level permission allows users to view the suppression list content and settings. 

It includes the following low-level permissions: 

* Journey Optimizer specific: 
  * suppression_list.view

* Adobe Experience Platform specific:
  * profiles.read
  * datasets.read

### [!DNL Export suppression list] permission {#export-suppression-list}

The **[!DNL Export suppression list]** high-level permission allows users to download the suppression list as a CSV file.

It includes the following low-level permissions:

* Journey Optimizer specific: 
  * suppression_list.export

* Adobe Experience Platform specific:
  * profiles.read
  * datasets.read

### [!DNL Manage landing page settings] permission {#manage-landing-page-settings}

The **[!DNL Manage landing page settings]** high-level permission allows users to read, create and edit landing page subdomains and preset settings.

It includes the following low-level permissions:

* Journey Optimizer specific: 
  * landing_page_subdomain.read
  * landing_page_subdomain.write
  * landing_page_subdomain.delete
  * landing_page_preset.read
  * landing_page_preset.write
  * landing_page_preset.delete

---
title: Built-in product profiles
description: Learn about the built-in product profiles
feature: Access Management
topic: Administration
role: Admin
level: Intermediate
exl-id: 5a968bd8-cf76-4242-aa80-3cfb3d551511
---
# Built-in product profiles {#ootb-product-profiles}


## About permissions related to messages{#message-permissions}

Adobe Journey Optimizer released new inline authoring capabilities which allows you to create and author your messages directly from a journey or a campaign. 

This feature will impact the permissions as follows:

| Permission's name | Will be included in |
|:-:|:-:|
| **[!DNL View Messages]** | **[!DNL View Journeys]** |
| **[!DNL View Message reports]** | **[!DNL View Journeys Report]** |
| **[!DNL Manage Messages]** | **[!DNL Manage Journey]** |
| **[!DNL Publish Messages]** | **[!DNL Publish Journeys]** |
| **[!DNL Manage Messages Preview and Test]** | **[!DNL Manage Journeys]** |

**After July 25**, permissions related to **Messages** are still be available since Messages can still be accessed to enable transition and you can still save them as template.

**As of September 6th**, permissions related to **Messages** will be removed and Messages will not be accessible anymore.

>[!WARNING]
>
>If you have users assigned to the **[!DNL Message Manager]** product profile only, without the **[!DNL Journey manager]** product profile, you need to assign a new product profile for them to be able to continue editing content.


## [!DNL Campaign Administrator] {#campaign-administrator}

The **[!DNL Campaign Administrator]** product profile allows the administration menus with the possibility to manage and publish Campaigns and Decision management. 

This product profile includes the following permissions:

| Capability | Permissions|
|-|-|
|Campaigns| <ul><li> **[!DNL Manage campaigns]**: read, create, edit, and delete campaigns.</li><li>**[!DNL Publish campaigns]**: publish campaigns.</li><li>**[!DNL View campaigns report]**: read and edit campaigns report.</li></ul>|
|Administration|<ul><li>**[!DNL Manage subdomains delegation]**: read, create, edit, and delete subdomain delegation.</li><li>**[!DNL Manage IP pools]**: read, create, edit, and delete ip pool.</li><li>**[!DNL Manage PTR records]**: read and edit PTR records.</li><li>**[!DNL View PTR records]**: read-only access to PTR records.</li><li> **[!DNL Manage messages general settings]**: read, create, edit, and delete message general settings.</li><li>**[!DNL Manage messages presets]**: read, create, edit, and delete content branding.</li><li>**[!DNL Manage suppression rules]**: access read, create, edit and delete suppression rules.</li><li>**[!DNL Export suppression list]**: access to export suppression list as a CSV file.</li><li>**[!DNL View suppression list]**: read and export local suppression list.</li><li>**[!DNL Manage alerts]**: enable/disable alerts for campaigns, messages and entitlements.</li><li>**[!DNL Manage landing page settings]**: read, create, edit, and delete landing page settings.</li><li>**[!DNL Manage SMS settings]**: read, create, edit, and delete SMS settings.</li></ul>|
|Decision management|<ul><li>**[!DNL Manage decisions]**: read, create, edit, and delete decisions.</li><li>**[!DNL Manage ranking strategies]**: read, create, edit, and delete ranking strategies.</li></ul>|
|Adobe Experience Platform|<ul><li>**[!DNL Sandbox]**: grant access to sandboxes.</li><li>**[!DNL Manage segments]**: read, create, edit, and delete segments.</li><li>**[!DNL Manage profiles]**: read, create, edit, and delete profiles.</li><li>**[!DNL Read datasets]**: read-only access to datasets.</li><li>**[!DNL Read schemas]**: read-only access to schemas.</li><li>**[!DNL Read Identity namespace]**: read-only access to identity namespace.</li><li>**[!DNL Manage merge policies]**: read, create, edit, and delete merge policies.</li></ul>|

## [!DNL Campaign Approver] {#campaign-approver}

The **[!DNL Campaign Approver]** product profile allows users to approve deliveries and publish them. They can later check the success of their deliveries with the **[!DNL Campaigns]** reports. 

| Capability | Permissions|
|-|-|
|Campaigns| <ul><li>**[!DNL Manage campaigns]**: read, create, edit, and delete campaigns.</li><li>**[!DNL Publish campaigns]**: publish campaigns.</li><li>**[!DNL View Campaigns report]**: read, edit journey reports.</li></ul>|
|Decision management| <ul><li>**[!DNL Manage decisions]**: read, create, edit, and delete decisioning entities.</li><li>**[!DNL Manage ranking strategies]**: read, create, edit, and delete custom messages reports and use action features.</li></ul>|
|Adobe Experience Platform| <ul><li>**[!DNL Manage segments]**: read, create, edit, and delete segments.</li><li>**[!DNL Manage profiles]**: read, create, edit, and delete profiles.</li><li>**[!DNL Read datasets]**: read-only access to datasets.</li><li>**[!DNL Read schemas]**: read-only access to schemas.</li><li>**[!DNL Manage merge policies]**: read, create, edit, and delete merge policies.</li></ul>|
|Administration| <ul><li>**[!DNL View messages presets]**: read-only access to messages presets.</li></ul>|

## [!DNL Campaign Manager] {#campaign-manager}

The **[!DNL Campaign Manager]** product profile allows users to create and edit **[!UICONTROL Campaigns]** and every capability linked to **[!UICONTROL Campaigns]** but will not be able to publish them.

This product profile includes the following permissions:

| Capability | Permissions|
|-|-|
|Campaigns| <ul><li>**[!DNL Manage campaigns]**: read, create, edit, and delete campaigns.</li><li>**[!DNL View campaigns report]**: read, edit journey report.</li></ul>|
|Decision management| <ul><li>**[!DNL Manage decisions]**: read, create, edit, and delete decisioning entities.</li><li>**[!DNL Manage ranking strategies]**: read, create, edit, and delete custom messages reports and use action features.</li></ul>|
|Adobe Experience Platform| <ul><li> **[!DNL Manage segments]**: read, create, edit, and delete segments.</li><li>**[!DNL Manage profiles]**: read, create, edit, and delete profiles.</li><li>**[!DNL Read datasets]**: read-only access to datasets.</li><li>**[!DNL Read schemas]**: read-only access to schemas.</li><li>**[!DNL Manage merge policies]**: read, create, edit, and delete merge policies.</li></ul>|
|Administration| <ul><li>**[!DNL View messages presets]**: read-only access to messages presets.</li></ul>|

## [!DNL Campaign Viewer] {#campaign-viewer}

The **[!DNL Campaign Viewer]** product profile allows read-only access to the **[!UICONTROL Campaigns]** and **[!UICONTROL Decision management]** capabilities. 

Users assigned to this product profile will not be able to edit or publish. 

This product profile includes the following permissions:

| Capability | Permissions|
|-|-|
|Campaigns| <ul><li>**[!DNL View campaigns]**: read-only access to campaigns.</li><li>**[!DNL View campaigns report]**: read-only access to campaigns reports.</li></ul>|
|Decision management| <ul><li>**[!DNL View decisions]**: read-only access to decisions entities.</li></ul>|

## [!DNL Journey Administrator] {#journey-administrator}

The **[!DNL Journey Administrator]** product profile allows the administration menus with the possibility to manage and publish Journeys and Decision management. 

This product profile includes the following permissions:

| Capability | Permissions|
|-|-|
|Journeys| <ul><li> **[!DNL Manage journeys]**: read, create, edit, and delete journeys.</li><li>**[!DNL Publish journeys]**: publish journeys.</li><li>**[!DNL Manage journeys events, data sources and actions]**: read, create, edit, and delete events, sources or actions.</li><li>**[!DNL View journeys report]**: read and edit journeys report.</li></ul>|
|Administration|<ul><li>**[!DNL Manage subdomains delegation]**: read, create, edit, and delete subdomain delegation.</li><li>**[!DNL Manage IP pools]**: read, create, edit, and delete ip pool.</li><li>**[!DNL Manage PTR records]**: read and edit PTR records.</li><li>**[!DNL View PTR records]**: read-only access to PTR records.</li><li>**[!DNL Manage channel surfaces]**: read, create, edit, and delete content branding.</li><li>**[!DNL Manage Landing page settings]**: create, edit and delete Landing page subdomains and Landing page presets.</li><li> **[!DNL Manage messages general settings]**: read, create, edit, and delete message general settings.</li><li>**[!DNL Manage SMS settings]**: create, edit and delete API credentials and SMS channel surfaces required to enable SMS channel.</li><li>**[!DNL Manage suppression rules]**: access read, create, edit and delete suppression rules.</li><li>**[!DNL View suppression list]**: read and export local suppression list.</li><li>**[!DNL Manage alerts]**: enable/disable alerts for journeys and entitlements.</li></ul>|
|Decision management|<ul><li>**[!DNL Manage decisions]**: read, create, edit, and delete decisions.</li><li>**[!DNL Manage ranking strategies]**: read, create, edit, and delete ranking strategies.</li></ul>|
|Adobe Experience Platform|<ul><li>**[!DNL Sandbox]**: grant access to sandboxes.</li><li>**[!DNL Manage segments]**: read, create, edit, and delete segments.</li><li>**[!DNL Manage profiles]**: read, create, edit, and delete profiles.</li><li>**[!DNL Read datasets]**: read-only access to datasets.</li><li>**[!DNL Read schemas]**: read-only access to schemas.</li><li>**[!DNL Read Identity namespace]**: read-only access to identity namespace.</li><li>**[!DNL Manage merge policies]**: read, create, edit, and delete merge policies.</li></ul>|
|Journey Optimizer Library|<ul><li>**[!DNL Manage Library Items]**: add and delete saved expressions in the [!DNL Journey Optimizer] Library.</li></ul>|

## [!DNL Journey Approver] {#journey-approver}

The **[!DNL Journey Approver]** product profile allows users to approve deliveries and publish them. They can later check the success of their deliveries with the **[!DNL Journey]** reports. 

This product profile includes the following permissions:

| Capability | Permissions|
|-|-|
|Journeys| <ul><li>**[!DNL Manage journeys]**: read, create, edit, and delete journeys.</li><li>**[!DNL Publish journey]**: publish journeys.</li><li>**[!DNL View journeys events, data sources and actions]**: read-only access to journey events, journey custom actions and journey data sources sources.</li><li>**[!DNL View journeys report]**: read, edit journey reports.</li></ul>|
|Decision management| <ul><li>**[!DNL Manage decisions]**: read, create, edit, and delete decisioning entities.</li><li>**[!DNL Manage ranking strategies]**: read, create, edit, and delete custom reports and use action features.</li></ul>|
|Adobe Experience Platform| <ul><li>**[!DNL Manage segments]**: read, create, edit, and delete segments.</li><li>**[!DNL Manage profiles]**: read, create, edit, and delete profiles.</li><li>**[!DNL Read datasets]**: read-only access to datasets.</li><li>**[!DNL Read schemas]**: read-only access to schemas.</li><li>**[!DNL Manage merge policies]**: read, create, edit, and delete merge policies.</li></ul>|
|Administration| <ul><li>**[!DNL View channel surfaces]**: read-only access to channel surfaces.</li></ul>|

## [!DNL Journey Manager] {#journey-manager}

The **[!DNL Journey Manager]** product profile allows users to create and edit **[!UICONTROL Journeys]** and every capability linked to **[!UICONTROL Journeys]** but will not be able to publish them.

This product profile includes the following permissions:

| Capability | Permissions|
|-|-|
|Journeys| <ul><li>**[!DNL Manage journeys]**: read, create, edit, and delete journeys.</li><li>**[!DNL View journeys events]**: read-only access to journey events, journey custom actions and journey data sources sources.</li><li>**[!DNL View journeys report]**: read, edit journey report.</li></ul>|
|Decision management| <ul><li>**[!DNL Manage decisions]**: read, create, edit, and delete decisioning entities.</li><li>**[!DNL Manage ranking strategies]**: read, create, edit, and delete custom reports and use action features.</li></ul>|
|Adobe Experience Platform| <ul><li> **[!DNL Manage segments]**: read, create, edit, and delete segments.</li><li>**[!DNL Manage profiles]**: read, create, edit, and delete profiles.</li><li>**[!DNL Read datasets]**: read-only access to datasets.</li><li>**[!DNL Read schemas]**: read-only access to schemas.</li><li>**[!DNL Manage merge policies]**: read, create, edit, and delete merge policies.</li></ul>|
|Administration| <ul><li>**[!DNL View channel surfaces]**: read-only access to channel surfaces.</li></ul>|

## [!DNL Journey Viewer] {#journey-viewer}

The **[!DNL Journey viewer]** product profile allows read-only access to the **[!UICONTROL Journeys]** and **[!UICONTROL Decision management]** capabilities. 

Users assigned to this product profile will not be able to edit or publish. 

This product profile includes the following permissions:

| Capability | Permissions|
|-|-|
|Journeys| <ul><li>**[!DNL View journeys]**: read-only access to journeys.</li><li>**[!DNL View journeys event, data sources, actions]**: read-only access to journeys events and data sources.</li><li>**[!DNL View journeys report]**: read-only access to journeys reports.</li></ul>|
|Decision management| <ul><li>**[!DNL View decisions]**: read-only access to decisions entities.</li></ul>|

## [!DNL Decisioning manager] {#decisioning-manager}

The **[!DNL Decisioning manager]** product profile only allows the **[!UICONTROL Decision management]** menu. Users assigned to this product profile will only be able to manage, view and publish decisions. 

This product profile includes the following permissions:

| Capability | Permissions|
|-|-|
|Decision management| <ul><li>**[!DNL Manage decisions]**: read, create, edit, and delete decisioning entities.</li><li>**[!DNL View decisions]**:  read-only access to decisioning entities.</li><li>**[!DNL Manage ranking strategies]**: read, create, edit, and delete custom reports and use action features.</li><li>**[!DNL Publish decisions]**: activate or deactivate decisioning activities.</li></ul>|

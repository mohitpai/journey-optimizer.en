---
solution: Journey Optimizer
product: journey optimizer
title: Get started with [!DNL Journey Optimizer] configuration
description: Learn more about [!DNL Journey Optimizer] configuration
role: Admin
level: Intermediate
exl-id: 0964a484-f957-4aae-a571-61b2a1615026
feature: Application Settings
topic: Administration
---

# Get started with [!DNL Journey Optimizer] configuration {#start-optimizer-configuration}

When accessing [!DNL Journey Optimizer] for the first time, you are provisioned a production sandbox and allocated a certain number of IPs depending on your contract.

To be able to create your journeys and send messages, you need to go through the configuration steps below.

## Configure messages and channels

Define channel surfaces, adapt and customize the messages.

* [Delegate to Adobe the subdomains](about-subdomain-delegation.md) you want to use to send emails and [create IP pools](ip-pools.md) to group together IP addresses provisioned with your instance.

* Manage the number of days during which retries are performed before sending email addresses to the suppression list. [Learn more](manage-suppression-list.md)

* Define push notifications settings in both [!DNL Adobe Experience Platform] and [!DNL Adobe Experience Platform Launch]. [Learn more](../push/push-gs.md)

    <!--* Understand the push notification flow. [Learn more](../push/push-gs.md)-->

* Configure your instance to send SMS (currently only available for a set of organizations - Limited Availability). [Learn more](../sms/sms-configuration.md)

* Create channel surfaces to configure all the technical parameters required to deliver messages. [Learn more](channel-surfaces.md)

* Determine which email address and/or phone number to use in priority for your recipients when several addresses/numbers are available in Adobe Experience Platform. [Learn more](primary-email-addresses.md)

## Configure journeys

In order to build journeys, you need to configure **[!UICONTROL Data Sources]**, **[!UICONTROL Events]** and **[!UICONTROL Actions]**. [Learn more](about-data-sources-events-actions.md)

![](assets/admin-menu.png)

* The **data source** configuration allows you to define a connection to a system to retrieve additional information that will be used in your journeys. [Learn more](../datasource/about-data-sources.md)

* **Events** allow you to trigger your journeys unitarily to send messages, in real-time, to the individual flowing into the journey. In the event configuration, you configure the events expected in the journeys. The incoming events' data is normalized following the Adobe Experience Data Model (XDM). Events come from Streaming Ingestion APIs for authenticated and unauthenticated events (such as Adobe Mobile SDK events). [Learn more](../event/about-events.md)
    
* [!DNL Journey Optimizer] comes with built-in message capabilities that allow you to design and send your content. If you are using a third-party system to send your messages, create a **custom action**. [Learn more](../action/action.md)
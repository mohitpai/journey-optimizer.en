---
solution: Journey Optimizer
product: journey optimizer
title: Alerts
description: Learn how to manage alerts
feature: Alerts
topic: Administration
role: Admin
level: Intermediate
exl-id: 0855ca5b-c7af-41c4-ad51-bed820ae5ecf
---
# Get Started with Alerts {#alerts}

## Alerting capabilities {#alerting-capabilities}

You can access system alerts through the user interface, or receive an email when a failure happens. You can view the available alerts and subscribe to them.  When a certain set of conditions in your operations is reached (such as a potential problem when the system breaches a threshold), alert messages are delivered to any users in your organization whohave subscribed to them. 

<!--These messages can repeat over a pre-defined time interval until the alert has been resolved.-->

Learn more about alerts in Adobe Experience Platform [documentation](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/overview.html).

To learn how to subscribe to alerts and configure them, refer to this [page](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/ui.html).

In the left menu, under **Administration**, click **Alerts**. Two pre-configured alerts for Journey Optimizer are available: the [alert for custom actions](#alert-custom-actions) and the [alert for Read Audience activities](#alert-read-audiences). These alerts are detailed below.

You can subscribe to each rule individually from the user interface, by selecting the **Subscribe** option from the **Alerts** dashboard. Use the same method to unsubscribe.

![](assets/alert-subscribe.png)

You can also subscribe to alerts through [I/O Event notifications](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/subscribe.html), however, alert rules are organized into different subscription packages. 

If an unexpected behavior occurs, an alert notification is sent to the subscribers. Based on the user preferences, alerts are sent by email, or directly within Journey Optimizer notification center, in the top right corner of the user interface.

When an alert is resolved, subscribers receive a "Resolved" notification.

>[!WARNING]
>
>Adobe Journey Optimizer specific alerts apply only to **live** journeys. Alerts are not triggered for journeys in test mode.

## Alert on custom actions {#alert-custom-actions}

This alert warns you if a custom action fails. We consider there is a failure where there has been more than 1% of errors on a specific custom action over the last 5 minutes. This is evaluated every 30 seconds.

![](assets/alerts-custom-action.png)

Alerts on custom actions are resolved when:

* Over the last 5 minutes, there has not been any error on that custom action (or errors below the 1% threshold).

* No profile reached that custom action.

The I/O event subscription name corresponding to the custom action alert is **Journey Custom Action Failure**.

## Alert on Read Audience activities {#alert-read-audiences}

This alert warns you if a **Read Segment** activity has not processed any profile 10 mins after scheduled time of execution. This failure can be caused by technical issues, because the audience is empty.

![](assets/alerts1.png)

Alerts on **Read Audience** activities only apply to recurring journeys. **Read Audience** activities in live journeys that have a schedule to run **Once** or **As soon as possible** are ignored.

Alerts on **Read Audience** are resolved when a profile enters the **Read Audience** node.

The I/O event subscription name corresponding to the **Read segment** alert is **Journey read segment Delays, Failures and Errors**.

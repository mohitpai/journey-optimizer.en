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

Journey Optimizer leverages Adobe Experience Platform alerting capabilities. This allows you to access system alerts through the user interface. You can view the available alerts and subscribe to them. 

When a certain set of conditions in your operations is reached (such as a potential problem when the system breaches a threshold), alert messages are delivered to any users in your organization who have subscribed to them. 

<!--These messages can repeat over a pre-defined time interval until the alert has been resolved.-->

Learn more on alerts in Adobe Experience Platform [documentation](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/overview.html).
To learn how to subscribe to alerts and configure them, refer to this [page](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/ui.html).

>[!AVAILABILITY]
>
>Some design changes are in progress for the ‘Read Audience Trigger Unsuccessful’ alert, hence this alert is paused for now, and has been temporary removed from the user interface. Once these changes are released, the alert will be surfaced again, and you will be able to subscribe to it.

In the left menu, under **Administration**, click **Alerts**. A pre-configured alert for Journey Optimizer is available. This alert warns you if a custom action fails. We consider there is a failure where there has been more than 1% of errors on a specific custom action over the last 5 minutes. This is evaluated every 30 seconds.

![](assets/alerts-custom-action.png)


<!--A pre-configured alert for Journey Optimizer is available. This alert will warn you if a read segment node has not processed any profile during the defined time frame.

![](assets/alerts1.png)-->

If an unexpected behavior occurs, an alert notification is sent to the subscribers of the alert through email or directly within Journey Optimizer, in the top right corner of the interface, based on user preferences.

![](assets/alerts2.png)

When an alert is resolved, you receive a "Resolved" notification. For the custom action alert, this can happen for two reasons:
* Over the last 5 minutes, there has not been any error on that custom action (or errors below the 1% threshold).
* No profile reached that custom action.

When [viewing alert rules in Adobe Experience Platform UI](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/ui.html), you can subscribe to each rule individually. When subscribing to alerts through [I/O Event notifications](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/subscribe.html), however, alert rules are organized into different subscription packages. The I/O event subscription name corresponding to the custom action alert is: "Journey Custom Action Failure".

<!--The I/O event subscription name corresponding to the Read segment alert is: "Journey read segment Delays, Failures and Errors".-->

>[!WARNING]
>
>These alerts apply only to live journeys. Alerts will not be triggered for journeys in test mode.


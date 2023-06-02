---
title: Create an In-app notification in a Journey
description: Learn how to create an In-app message in Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
keywords: in-app, message, creation, start
hide: yes
hidefromtoc: yes
exl-id: b774e34f-8225-41a0-a2ec-b91d3a86cf2b
badge: label="Beta" type="Informative"
---
# Create an In-app message in a Journey {#create-in-app-journey}

1. Open your journey, then drag and drop an **[!UICONTROL In-app]** activity from the **[!UICONTROL Actions]** section of the palette.

    When a profile reaches the end of their journey, any in-app messages displayed to them will automatically expire. For that reason, a Wait activity is automatically added after your In-app activity to ensure proper timing.

    ![](assets/in_app_journey_1.png)

1. Enter a **[!UICONTROL Label]** and **[!UICONTROL Description]** for your message.

1. Choose the [In-app surface](inapp-configuration.md) to use.

    ![](assets/in_app_journey_2.png)

1. You can now start designing your content with the **[!UICONTROL Edit content]** button. [Learn more](design-in-app.md)

1. Click **[!UICONTROL Edit trigger]** to configure your Trigger. 

    ![](assets/in_app_journey_4.png)

1. From the **[!UICONTROL In-app message trigger]** window, choose the event(s) and criteria that will trigger your message:

    1. Click **[!UICONTROL Add condition]** if you want the trigger to consider multiple events or criteria. 
    1. From the **[!UICONTROL Select an event]** drop-down, select the type of event for your trigger.
    1. Select how your events are linked, e.g. choose **[!UICONTROL And]** if you want **both** triggers to be true in order for a message to be shown or choose **[!UICONTROL Or]** if you want the message to be shown if **either** of the triggers are true.
    1. Click **[!UICONTROL Make group]** to group triggers together.

    ![](assets/in_app_journey_3.png)

1. Choose the frequency your trigger when your In-app message is active:

    * **[!UICONTROL Show every time]**: Always show the message when the events selected in the **[!UICONTROL Mobile app trigger]** drop-down occur.
    * **[!UICONTROL Show once]**: Only show this message the first time the events selected in the **[!UICONTROL Mobile app trigger]** drop-down occur.
    * **[!UICONTROL Show until click through]**: Show this message when the events selected in the **[!UICONTROL Mobile app trigger]** drop-down occur until an interact event is sent by the SDK with an action of "clicked".

1. If necessary, complete your journey flow by dragging and dropping additional actions or events. [Learn more](../building-journeys/about-journey-activities.md)

1. Once your In-app message is ready, finalize the configuration and publish your journey to activate it.

For more information on how to configure a journey, refer to [this page](../building-journeys/journey-gs.md).

## In-app activity limitations {#in-app-activity-limitations}

* This feature is currently not available for Healthcare customers.

* Personalization can only contain profile attributes.

* In-app display is tied to the journey lifespan, meaning that when the journey ends for a profile, all In-app messages within that journey will cease to be displayed for that profile.  Consequently, it is not possible to stop an In-app message directly from a journey activity. Instead, you will need to end the entire journey to stop the In-app messages from being displayed to the profile.

* In test mode, the In-app display depends on the journey's lifespan. To prevent the journey from ending too early during testing, adjust the **[!UICONTROL Wait time]** value for your **[!UICONTROL Wait]** activities. 

* **[!UICONTROL Reaction]** activities can not be used to react to an In-app open or click.

* An activation delay happens between the moment a user profile reaches an In-app activity in the canvas and the time they start seeing that In-app message. This delay can range from 15 minutes to 1 hour.

**Related topics:**

* [Design In-app message](design-in-app.md)
* [Test and send your In-app message](send-in-app.md)
* [In-app report](../reports/campaign-global-report.md#inapp-report)
* [In-app configuration](inapp-configuration.md)

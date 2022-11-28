---
solution: Journey Optimizer
product: journey optimizer
title: Get started with journey activities
description: Get started with journey activities
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 239b3d72-3be0-4a82-84e6-f219e33ddca4
---
# Get started with journey activities {#about-journey-activities}

Combine the different event, orchestration and action activities to build your multi-step cross-channel scenarios.

## Events activities {#event-activities}

Events are what trigger a personalized journey, such as an online purchase. Once someone enters a journey, they move through as an individual, and no two individuals are moving along at the same rate or along the same path. When you start your journey with an event, the journey is triggered when the event is received. Each person in the journey then follows, individually, the next steps defined in your journey. 

Events configured by the technical user (see [this page](../event/about-events.md)) are all displayed in the first category of the palette, on the left side of the screen. The following events activities are available:

* [General events](../building-journeys/general-events.md)
* [Reaction](../building-journeys/reaction-events.md)
* [Segment Qualification](../building-journeys/segment-qualification-events.md)

 ![](assets/journey43.png)

Start your journey by drag and dropping an event activity. You can also double-click on it.

 ![](assets/journey44.png)

## Orchestration activities {#orchestration-activities}

Orchestration activities are different conditions that help determine the next step in the journey. It can be if the person has an open support case or not, the weather forecast at their current location, if they completed a purchase or not, or reached 10 000 loyalty points.

From the palette, on the left-hand side of the screen, the following orchestration activities are available:

* [Condition](../building-journeys/condition-activity.md)
* [Wait](../building-journeys/wait-activity.md)
* [Read Segment](../building-journeys/read-segment.md)

![](assets/journey49.png)

## Action activities {#action-activities}

Actions are what you want to happen as result of some kind of trigger, like sending a message. It is the piece of journey that the customer experiences. 

From the palette, on the left-hand side of the screen, below **[!UICONTROL Events]** and **[!UICONTROL Orchestration]**, you can find the **[!UICONTROL Actions]** category. The following action activities are available:

* [Email, SMS, Push](../building-journeys/journeys-message.md)
* [Custom actions](../building-journeys/using-custom-actions.md)
* [Jump](../building-journeys/jump.md)

![](assets/journey58.png)

These activities represent the different available communication channels. You can combine them to create a cross-channel scenario. 

If you have configured custom actions, they also appear here. [Learn more](../building-journeys/using-custom-actions.md)).

## Best practices {#best-practices}

Most activities allow you to define a **[!UICONTROL Label]**. This adds a suffix to the name that will appear under your activity in the canvas. This is useful if you use the same activity several times in your journey and want to identify them more easily. It will also make debugging easier in case of errors and it will make reports easier to read. You can also add an optional **[!UICONTROL Description]**.

![](assets/journey59bis.png)

When an error occurs in an action or a condition, the journey of an individual stops. The only way to make it continue is to check the box **[!UICONTROL Add an alternative path in case of a timeout or an error]**. See [this section](../building-journeys/using-the-journey-designer.md#paths).

![](assets/journey42.png)

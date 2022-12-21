---
solution: Journey Optimizer
product: journey optimizer
title: Adobe Analytics integration
description: Learn how to leverage Adobe Analytics data
feature: Events
topic: Administration
role: Admin
level: Intermediate
exl-id: 9d842722-e5eb-4743-849d-b7ba9448062f
---
# Adobe Analytics integration {#analytics-data}

## Leverage Adobe Analytics or Web SDK data {#leverage-analytics-data}

You can leverage all of the web behavioral event data (through Adobe Analytics or Web SDK) that you are already capturing and streaming into Adobe Experience Platform in order to trigger journeys and automate experiences for your customers.

>[!NOTE]
>
>This section only applies for rule-based events and customers who need to use Adobe Analytics or WebSDK data.

For this to work with Adobe Analytics, you need to activate, in Adobe Experience Platform, the report suite that you want to use. To do this, follow the steps below:

1. Connect to Adobe Experience Platform and browse to **[!UICONTROL Sources]**.

1. In the Adobe Analytics section, select **[!UICONTROL Add data]**

    ![](assets/ajo-aa_1.png)

1. From the list of available Adobe Analytics report suites, select the **[!UICONTROL Report suite]** to enable. Then, click **[!UICONTROL Next]**.

    ![](assets/ajo-aa_2.png)

1. Choose if you want to use a Default or Custom schema.

1. From the **[!UICONTROL Dataflow detail]** screen, choose a **[!UICONTROL Dataflow name]**.

1. Once your configuration is complete, click **[!UICONTROL Finish]**. 

    ![](assets/ajo-aa_3.png)

This enables the Analytics source connector for that report suite. Whenever the data comes in, it is transformed into an Experience event and sent into Adobe Experience Platform. 

![](assets/ajo-aa_4.png)

Learn more about Adobe Analytics source connector in  [Adobe Experience Platform documentation](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/analytics.html){target="_blank"} and [tutorial](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/adobe-applications/analytics.html){target="_blank"}.

## Create a journey with an event using Adobe Analytics or Web SDK data {#event-analytics}

After implementing your integration with Adobe Analytics with the [Adobe Analytics sources](#leverage-analytics-data) or with the [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html), you can create an event which can later be used in a journey.

In this example, we will target users who added a product to their carts:

* If the order is completed, they will receive a follow-up email two days later to ask for feedbacks.
* If the order is not completed, they will receive an email to remind them to complete the order.

1. From Adobe Journey Optimizer, access the **[!UICONTROL Configuration]** menu. 

1. Then, select **[!UICONTROL Manage]** from the **[!UICONTROL Events]** card.

    ![](assets/ajo-aa_5.png)

1. Click **[!UICONTROL Create event]**. The event configuration pane opens on the right side of the screen.

1. Fill in the **[!UICONTROL Event]** parameters:

    * **[!UICONTROL Name]**: Personalize the name of your **[!UICONTROL Event]**.
    * **[!UICONTROL Type]**: Choose the **[!UICONTROL Unitary]** Type. [Learn more](../event/about-events.md)
    * **[!UICONTROL Event ID type]**: Choose the **[!UICONTROL Rule based]** Event ID type. [Learn more](../event/about-events.md#event-id-type)
    * **[!UICONTROL Schema]**: Select the Analytics or WebSDK schema created in the section above.
    * **[!UICONTROL Fields]**: Select the Payload fields. [Learn more](../event/about-creating.md#define-the-payload-fields)
    * **[!UICONTROL Event ID condition]**: Define the condition that will be used by the system to identify the events that will trigger your journey. 
        
        Here, the Event is triggered when customers add an item to their carts.
    * **[!UICONTROL Profile Identifier]**: Choose a field from your payload fields or define a formula to identify the person associated to the event.

    ![](assets/ajo-aa_6.png)

1. When configured, select **[!UICONTROL Save]**. Your event is now ready to be used in a journey.

1. From the **[!UICONTROL Journeys]**, you can now start creating your journey. For more on this, refer to [this section](../building-journeys/journey-gs.md).

1. Add your previously configured Analytics events to your journey.

    ![](assets/ajo-aa_8.png)

1. Add an Event which will be triggered if an order is completed.

1. From your **[!UICONTROL Event menu]**, select the **[!UICONTROL Define the event timeout]** and **[!UICONTROL Set a timeout path]** options.

    ![](assets/ajo-aa_9.png)

1. From the timeout path, add an **[!UICONTROL Email]** action. This path will be used to send an email to customers who didn't complete an order to remind them that their carts are still available.

1. Add a **[!UICONTROL Wait]** activity after your main path and set it to the needed duration.

    ![](assets/ajo-aa_10.png)

1. Then, add an **[!UICONTROL Email action]**. In this email, the customers will be prompted to give feedbacks on the placed order.

You can now publish your journey after testing its validity. [Learn more](../building-journeys/publishing-the-journey.md)

![](assets/ajo-aa_7.png)

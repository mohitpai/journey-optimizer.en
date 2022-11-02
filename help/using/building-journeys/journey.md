---
solution: Journey Optimizer
product: journey optimizer
title: General principle
description: General principle
feature: Journeys
topic: Content Management
role: User
level: Beginner
exl-id: 73cfd48b-72e6-4b72-bbdf-700a32a34bda
---
# General principle{#jo-general-principle}

[!DNL Journey Optimizer] allow you to build real-time orchestration use cases leveraging contextual data stored in events or data sources.

Design multistep advanced scenarios powered by following capabilities:

* Send real-time **unitary delivery** triggered when an event is received, or **in batch** using Adobe Experience Platform segments.

* Leverage **contextual data** from events, information from Adobe Experience Platform, or data from third-party API services.

* Use the **built-in actions** to send messages designed in [!DNL Journey Optimizer] or create **custom actions** if you're using a third-party system to send your messages.

* With the **journey designer**, build your multistep use cases: easily drag and drop an entry event or a read segment activity, add conditions and send personalized messages.

## Journey lifecycle{#journey-lifecyle}

### Profiles in journeys{#profile-journey}

In a unitary journey:

* If re-entrance is enabled, a profile can enter a journey several times, but cannot do it until he fully exited that previous instance of the journey.

* If re-entrance is disabled, a profile cannot enter multiple times the same journey

For more information on profile re-entrance, refer to this [section](../building-journeys/journey-gs.md#change-properties).

In a read segment journey:

* For non-recurring journeys: the profile enters once and only once the journey.
* for recurring journeys: the profile enters the journey on each recurrence, if he is in the segment/expected status. If he was still in the journey from a previous recurrence, he will restart it from the beginning.

In business event journeys starting with a read segment :

Knowing that this journey is based on the reception of a business event, if the profile is qualified in the expected segment, he will enter the journey for each business event received, meaning that this profile can be multiple times in the same journey, at the same time, but in the context of different business events.

Unitary journeys (starting with an event or a segment qualification) include a guardrail that prevents journeys from being erroneously triggered multiple times for the same event. Profile re-entrance is temporally blocked by default for 5 minutes. For instance, if an event triggers a journey at 12:01 for a specific profile and another one arrives at 12:03 (whether it is the same event or a different one triggering the same journey) that journey will not start again for this profile.


### Journey ending{#journey-ending}

A journey can end for an individual in two specific contexts:

* The person arrives at the last activity of a path.
* The person arrives at a **Condition** activity (or a **Wait** activity with a condition) and does not match any of the conditions.

The person can then re-enter the journey if re-entrance is allowed. See [this page](../building-journeys/journey-gs.md#change-properties)

To terminate a live journey, we recommend that you close it. The arrival of new customers in the journey will then be blocked. Customers who already entered in the journey are able to experience it to the end. See [this section](../building-journeys/journey.md#close-journey)

You can stop a journey only if an emergency occurred and all processing needs to be ended immediately on a journey. People who already entered a journey are all stopped in their progress. See [this section](../building-journeys/journey.md#stop-journey)

>[!NOTE]
>
>Note that you cannot resume a closed or stopped journey.

#### Journey end tag{#end-tag}

While authoring a journey, an "end tag" is displayed at the end of each path. This node cannot be added by a user, cannot be removed and only its label can be changed. It marks the end of each path of the journey. If the journey has several paths, we recommend that you add a label to each end to make reports easier to read. See [this page](../reports/live-report.md).

![](assets/journey-end.png)

<!--

### End activity{#journey-end-activity}

The **[!UICONTROL End]** activity allows you to mark the end of each path of the journey. It is not mandatory but recommended for visual clarity. See [this page](../building-journeys/end-activity.md)

![](assets/journey54.png)

-->

#### Close a journey{#close-journey}

A journey can close because of the following reasons:

* The journey is closed manually via the **[!UICONTROL Close to new entrances]** button. 
* A one-shot segment based journey that has finished executing.
* After the last occurrence of a recurring segment based journey.

Closing a journey manually ensures that customers who already entered the journey can finish their path but new users are not able to enter the journey. When a journey is closed (for any of the reasons above), it will have the status **[!UICONTROL Closed]**. The journey stops letting new individuals enter the journey. Persons already in the journey can finish the journey normally. After the default global timeout of 30 days, the journey will switch to the **Finished** status. See this [section](../building-journeys/journey-gs.md#global_timeout).

A closed journey version cannot be restarted or deleted. You can create a new version of it or duplicate it. Only finished journeys can be deleted.

To close a journey from the list of journeys, click the **[!UICONTROL Ellipsis]** button that is located to the right of the journey name and select **[!UICONTROL Close to new entrances]**.

![](assets/journey-finish-quick-action.png)

You can also:

1. In the **[!UICONTROL Journeys]** list, click on the journey you want to close.
1. On the top-right, click the down arrow.

    ![](assets/finish_drop_down_list.png)

1. Click **[!UICONTROL Close to new entrances]**, and confirm in the dialog box.

#### Stop a journey{#stop-journey}

In case you need to stop the progress of all individuals in the journey, you can stop it. Stopping the journey will timeout all individuals in the journey. However, stopping a journey involves that people who already entered a journey are all stopped in their progress. The journey is basically switched off. If you want to put an end to a journey we recommend that you close it. 

A stopped journey version cannot be restarted.

When stopped, the journey status is set to **[!UICONTROL Stopped]**. 

You can stop a journey, for example, if a marketer realizes that the journey targets the wrong audience or a custom action supposed to deliver messages is not working correctly. To stop a journey from the list of journeys, click the **[!UICONTROL Ellipsis]** button that is located to the right of the journey name and select **[!UICONTROL Stop]**.

![](assets/journey-finish-quick-action.png)

You can also:

1. In the **[!UICONTROL Journeys]** list, click on the journey you want to stop.
1. On the top-right, click on the down arrow.
   ![](assets/finish_drop_down_list.png)
1. Click **[!UICONTROL Stop]**, and confirm in the dialog box.



## Journey versions{#journey-versions}

In the journey list, all journey versions are displayed with the version number. See [this page](../building-journeys/using-the-journey-designer.md). 

When you search for a journey, newest versions appear at the top of the list the first time the application opens. Then, you can define the sorting you want and the application will keep it as a user preference. The journey's version is also displayed at the top of the journey edition interface, above the canvas.

![](assets/journeyversions1.png)

>[!NOTE]
>
>In most cases, a profile cannot be present multiple times in the same journey, at the same time. If re-entrance is enabled, a profile can reenter a journey, but cannot do it until he fully exited that previous instance of the journey. [Read more](#journey-ending)

If you need to modify to a live journey, create a new version of your journey.

1. Open the latest version of your live journey, click **[!UICONTROL Create a new version]** and confirm.

    ![](assets/journeyversions2.png)

    >[!NOTE]
    >
    >You can only create a new version from the latest version of a journey.

1. Make your modifications, click **[!UICONTROL Publish]** and confirm.

    ![](assets/journeyversions3.png)

From the moment the journey is published, individuals will start to flow into the latest version of the journey. People who have already entered a previous version stay in it until they finish the journey. If they later re-enter the same journey, they will go into the latest version.

Journey versions can be stopped individually. All versions of journeys have the same name.

When you publish a new version of a journey, the previous version automatically ends and switches to the **Closed** status. No entrance in the journey can happen. Even if you stop the latest version, the previous version stays closed.

>[!NOTE]
>
>Learn more about journey versions guardrails and limitations, in [this page](../start/guardrails.md#journey-versions-limitations)
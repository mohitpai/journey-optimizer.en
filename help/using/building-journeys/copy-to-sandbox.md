---
title: Copy a journey to another sandox
description: Learn how to copy a journey to another sandox
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 8c63f2f2-5cec-4cb2-b3bf-2387eefb5002
---
# Copy a journey to another sandbox {#copy-to-sandbox}

>[!CONTEXTUALHELP]
>id="ajo_journey_copy_main"
>title="Copy a journey to another sandbox"
>abstract="Journey Optimizer allows you to copy an entire journey from one sandbox to another. For example, you can copy a journey from the Stage sandbox environment to your Production sandbox. In addition to the Journey itself, Journey Optimizer also copies most of the objects the journey depends on."

>[!CONTEXTUALHELP]
>id="ajo_journey_copy_sandbox_details"
>title="Sandbox details"
>abstract="Select the destination sandbox you want to copy the journey to. Only sandboxes within your IMS organization are available."

>[!CONTEXTUALHELP]
>id="ajo_journey_copy_object_details"
>title="Object details"
>abstract="This is the journey you are going to copy."

>[!CONTEXTUALHELP]
>id="ajo_journey_copy_dependent_objects"
>title="Dependent objects"
>abstract="This is the list of associated objects used in the journey. This list displays the name, the object type, as well as the internal Journey Optimizer ID."

Journey Optimizer allows you to copy an entire journey from one sandbox to another. For example, you can copy a journey from your Stage sandbox environment to your Production sandbox. In addition to the journey itself, Journey Optimizer also copies most of the objects the journey depends on: segments, surfaces (i.e. presets), schemas, events and actions. Refer to the [limitations](../building-journeys/copy-to-sandbox.md#limitations)

>[!CAUTION]
>
>We do not guarantee that all linked elements will be copied to the destination sandbox. We strongly recommend that you perform a thorough check before publishing the journey. This will allow you to idenity any potential missing object. 

The copied objects in the target sandbox are unique and there is no risk of overwriting existing elements. Both the journey and any messages inside the journey are brought over in draft mode. This allows you to perform a thorough validation before publication on the target sandbox. The copy process only copies over the metadata about the journey and the objects in that Journey. No profile or dataset data is being copied as part of this process. 

To copy a journey to another sandbox, follow these steps:

1. In the JOURNEY MANAGEMENT menu section, click **[!UICONTROL Journeys]**. The list of journeys is displayed.

2. Search for the journey you want to copy, click the **More actions** icon (the three dots next to the journey name) and click **Copy to sandbox**.

   ![](assets/copy-sandbox1.png)

   The **Copy to sandbox** screen is displayed.

   ![](assets/copy-sandbox2.png)

3. Select the **Target sandbox** from the drop-down field. Only sandboxes within your IMS organization are available.

4. Review the **Dependent objects** section. This is the list of associated objects used in the journey. This list displays the name, the object type, as well as the internal Journey Optimizer ID.

5. Click the **Copy** button, in the top-right corner, to start copying the journey to the target sandbox.

   ![](assets/copy-sandbox3.png)

   The copying process begins and the progress of each individual object is displayed. The copying process varies based on the complexity of the journey and how many objects need to be copied over. If an error is encountered, a message is displayed for the related object. 

   ![](assets/copy-sandbox4.png)

6. Once the copying is complete, click **Close**. 

7. Access your target sandbox and perform a thorough check of all the copied objects. 

## Copy process and limitations {#limitations}

We do not guarantee that all linked elements will be copied to the destination sandbox. We strongly recommend that you perform a thorough check. Identify any potential missing object and create them manually before publishing the journey.

The following objects are copied:

* Segment

   A segment can only be copied once from one sandbox to another. Once a segment is copied, it is not editable on the destination sandbox.

* Schema

   The schemas used in this journey are copied.

* Message

   The channel action activities used in the journey. Fields used for personalization in the message are not checked for completeness. Content blocks are not copied.

* Journey - canvas details

   The representation of the journey on the canvas including the objects in the journey such as conditions, actions, events, read segments, etc. The Jump activity is excluded from the copy.

* Event

   The events and the event details used in the journey are copied.

* Action

   The actions and action details used in the journey are copied.

Surfaces (i.e. presets) are not copied over. The system automatically selects the closest possible match on the destination sandbox, based on message type and surface name. If there are no surfaces found on the target sandbox, then the surface copy will fail. This will mean that the message copy will fail as well because a message requires a surface to be available for setup. In this case at least one surface needs to be created, for the right channel of the message, in order for the copy to work.

For Schemas, Merge Policies and Segments, the second time these objects attempt to be copied, they will only be referenced. They will be treated as objects that already exist and will be copied again. This means that these objects can only be copied once.

There is a five minute delay before Adobe Journey Optimizer can reference Schemas, Merge Policies and Segments without seeing an error in the canvas. Wait five minutes and these references will be available.

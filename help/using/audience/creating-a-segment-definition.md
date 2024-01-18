---
solution: Journey Optimizer
product: journey optimizer
title: Build segment definitions
description: Learn how to create audiences through segment definitions
feature: Audiences, Profiles
topic: Content Management
role: User
level: Beginner
exl-id: 289aac5d-6cdb-411f-985e-3acef58050a8
---
# Build segment definitions {#build-segments}

>[!CONTEXTUALHELP]
>id="ajo_ao_create_rule"
>title="Create a rule"
>abstract="The Build rule creation method allows you to create a new audience definition using Adobe Experience Platform Segmentation Service."

In this example, we will build an audience to target all customers living in Atlanta, San Francisco, or Seattle and born after 1980. All these customers should have opened the Luma application within the last 7 days, then made a purchase within 2 hours after opening the application.

➡️ [Learn how to create audiences in this video](#video-segment)

1. From the **[!UICONTROL Audiences]** menu, click the **[!UICONTROL Create audience]** button and select **[!UICONTROL Build rule]**.
    
    ![](assets/create-segment.png)

    The segment definition screen allows you to configure all the required fields to define your audience. Learn how to configure audiences in the [Segmentation Service documentation](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html){target="_blank"}.

    ![](assets/segment-builder.png)

1. In the **[!UICONTROL Audience properties]** pane, provide a name and a description (optional) for the audience.

    ![](assets/segment-properties.png)

1. Drag and drop the desired fields from the left pane into the center workspace, then configure them according to your needs.

    >[!NOTE]
    >
    >Note that the fields available in the left pane vary depending on how the **XDM Individual Profile** and **XDM ExperienceEvent** schemas have been configured for your organization.  Learn more in the [Experience Data Model (XDM) documentation](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html){target="_blank"}.

    ![](assets/drag-fields.png)

    In this example, we need to rely on **Attributes** and **Events** fields to build the audience:

    * **Attributes**: profiles living in Atlanta, San Francisco or Seattle born after 1980

        ![](assets/add-attributes.png)
        
    * **Events**: profiles who opened the Luma application within the last 7 days, then made a purchase within 2 hours after opening the application.

        ![](assets/add-events.png)

        >[!NOTE]
        >
        >Adobe recommends not using open and send events with streaming segmentation. Instead, use real user-activity signals like clicks, purchases, or beacon data. For frequency or suppression logic, use business rules rather than send events. [Learn more](about-audiences.md#open-and-send-event-guardrails)

1. As you are adding and configuring new fields in the workspace, the **[!UICONTROL Audience Properties]** pane is automatically updated with information on the estimated profiles belonging to the audience.

    ![](assets/segment-estimate.png)

1. Once the audience is ready, click **[!UICONTROL Save]**. It displays in the list of Adobe Experience Platform audiences. Note that a search bar is available to help you search a specific audience in the list.

The audience can now be used in your journeys. For more on this, refer to [this section](../audience/about-audiences.md).

## How-to video{#video-segment}

Understand how Journey Optimizer uses rules to generate audience and learn how to use attributes, events, and existing audiences to create an audience.

>[!VIDEO](https://video.tv.adobe.com/v/3425020?quality=12)

---
product: experience platform
solution: Experience Platform
title: Create ranking strategies
description: Learn how to create ranking strategies in Adobe Experience Platform.
feature: Ranking Formulas
role: User
level: Intermediate
exl-id: 81d07ec8-e808-4bc6-97b1-b9f7db2aec22
---
# AI rankings {#ai-rankings}

## Get started with AI rankings {#get-started-with-ai-rankings}

<!--If you are an [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/home.html){target="_blank"} user leveraging the **Offer Decisioning** application service,-->You can use an trained model system that ranks offers to display for a given profile.

>[!CAUTION]
>
>The use of AI ranking is currently available in early access to select users only.

This feature enables you to create different **ranking strategies** based on your business goals. Using these different goal-based strategies in a decision (formerly known as offer activity), the trained model system will help you understand how the different ranking strategies are impacting your goals.

For example, you can select a ranking strategy for the email channel and another one for the push channel. For each channel, the trained model system will leverage multiple data points to determine which offer should be presented first for a given placement, rather than taking into account the offers’ priority scores or a [ranking formula](create-ranking-formulas.md).

<!--This feature is not enabled by default. To be able to use it, reach out to your Adobe contact.-->

Once a ranking strategy has been created, assign it to a placement in a decision. Learn more in [Configure offers selection in decisions](../offer-activities/configure-offer-selection.md).

### Auto-optimization model {#auto-optimization}

Currently in [!DNL Journey Optimizer] the only supported model type for AI ranking is **auto-optimization**.

An auto-optimization model aims to serve offers that maximize the return, based on the Key performance indicators (KPIs) that you set. <!--These KPIs could be in the form of conversion rates, revenue, etc.-->At this point, auto-optimization focuses on optimizing offer clicks with offer conversion as the target.

>[!NOTE]
>
>The auto-optimization model does not use any contextual or user profile data. It optimizes results based on global performance of the offers.

With auto-optimization, the challenge is to balance exploratory learning and exploitation of that learning. This principle is known as **"multi-armed bandit" approach**.

To tackle this challenge, the auto-optimization model uses the **Thompson Sampling** method, which allows to identify which option to pursue to maximize the expected rewards. In other words, Thompson Sampling is a type of reinforcement learning technique for solving the exploration-exploitation dilemma in a multi-armed bandit problem. 

The Thompson Sampling method also enables to handle challenges such as the "cold start" problem, i.e. when a new offer is introduced in the campaign, it does not have any history that it could train from.

## Create a ranking strategy {#create-ranking-strategy}

To create a ranking strategy, follow the steps below:

1. Access the **[!UICONTROL Components]** menu, then select the **[!UICONTROL AI rankings]** tab.

    ![](../../assets/ai-ranking-list.png)

    All the ranking strategies created so far are listed.

1. Click the **[!UICONTROL Create strategy]** button.

1. Fill in the following fields:

    ![](../../assets/ai-ranking-fields.png)

    * **[!UICONTROL Name]**: Unique name that you must provide.

    * **[!UICONTROL Model type]**: Currently the only supported model type is **[!UICONTROL Auto-optimization]**.<!--More will be supported in the future so the drop-down list will be enabled.-->

    * **[!UICONTROL Optimization metric]**:
    
        This option enables marketers to choose how the machine-learn model should be built and trained: based on offers displayed, offers clicked in email, and/or offers clicked on the web.

        >[!NOTE]
        >
        >You can select all metric types if needed.

        There are two types of optimization metrics:
        * **[!UICONTROL Impression]**: Currently impression events correspond to all offers that are displayed.
        * **[!UICONTROL Conversion]**: Conversion events correspond to all offers that result in clicks via email or web.

        All selected impression events and/or conversion events will be automatically captured using the Web SDK or the Mobile SDK that has been provided. Learn more on this in [Adobe Experience Platform Web SDK overview](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=en).

    * **[!UICONTROL Dataset ID]**: For conversion, you need to provide a dataset where events are collected by selecting it from the drop-down list. Learn how to create such dataset in [this section](#create-dataset). <!--This dataset needs to be associated with a schema that must have the **[!UICONTROL Proposition Interactions]** field group (previously known as mixin) associated with it.-->

    ![](../../assets/ai-ranking-dataset-id.png)
    
    >[!CAUTION]
    >
    >Only the datasets created from schemas associated with the **[!UICONTROL Experience Event - Proposition Interactions]** field group (previously known as mixin) are displayed in the drop-down list.

1. Save and activate the ranking strategy.

    ![](../../assets/ai-ranking-save-activate.png)

It is now ready to be used in a decision to rank eligible offers for a placement. Learn more in [this section](../offer-activities/configure-offer-selection.md#use-ranking-strategy).<!--TBC?-->

## Create a dataset to collect events {#create-dataset}

You need to create a dataset where conversion events will be collected. Start by creating the schema that will be used in your dataset:

1. From the **[!UICONTROL Data Management]** menu, select **[!UICONTROL Schema]**, go to the **[!UICONTROL Browse]** tab and click **[!UICONTROL Create schema]**.

    ![](../../assets/ai-ranking-create-schema.png)

1. Choose **[!UICONTROL XDM ExperienceEvent]**.

    ![](../../assets/ai-ranking-xdm-event.png)

    >[!NOTE]
    >
    >    Learn more on XDM schemas and fields groups in the [XDM System overview documentation](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=en).


1. In the **[!UICONTROL Search]** field, type "proposition interaction" and select the **[!UICONTROL Experience Event - Proposition Interactions]** field group.

    ![](../../assets/ai-ranking-proposition-interactions.png)

    >[!CAUTION]
    >
    >    The schema that will be used in your dataset must have the **[!UICONTROL Experience Event - Proposition Interactions]** field group associated with it. Otherwise you will not be able to use it in your ranking strategy.

1. Click **[!UICONTROL Add field groups]**.

    ![](../../assets/ai-ranking-add-field-group.png)

    >[!NOTE]
    >Field group was previously known as mixin.
    >    

1. Type a name and save the schema.<!--How do you edit the fields in this new schema? Examples?-->

>[!NOTE]
>
>    Learn more on building schemas in [Basics of schema composition](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=en#understanding-schemas).

You're now ready to create a dataset using this schema. To do this, follow the steps below:

1. From the **[!UICONTROL Data Management]** menu, select **[!UICONTROL Datasets]**, go to the **[!UICONTROL Browse]** tab and click **[!UICONTROL Create dataset]**.

    ![](../../assets/ai-ranking-create-dataset.png)

1. Select **[!UICONTROL Create dataset from schema]**.

    ![](../../assets/ai-ranking-create-dataset-from-schema.png)
    
1. Select the schema you just created from the list.

    ![](../../assets/ai-ranking-dataset-select-schema.png)

1. Click **[!UICONTROL Next]**.

1. Provide a unique name for the dataset in the **[!UICONTROL Name]** field and click **[!UICONTROL Finish]**.

    ![](../../assets/ai-ranking-dataset-name.png)

The dataset is now ready to be selected to collect event data when [creating a ranking strategy](#create-ranking-strategy).

## Offer schema requirements {#schema-requirements}

At this point, you must have:

* created the ranking strategy,
* defined which type of event you want to capture - offer displayed (impression) and/or offer clicked (conversion),
* and in which dataset you want to collect the event data.

Now each time an offer is displayed and/or clicked, you want the corresponding event to be automatically captured by the **[!UICONTROL Experience Event - Proposition Interactions]** field group using the [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/web-sdk-faq.html#what-is-adobe-experience-platform-web-sdk%3F){target="_blank"} or Mobile SDK.

To be able to send in event types (offer displayed or offer clicked), you must set the correct value for each event type in an experience event that is sent into Adobe Experience Platform. Below are the schema requirements you need to implement into your JavaScript code:

**Scenario:** Offer displayed
**Event type:** `decisioning.propositionDisplay`
**Source:** Web.sdk/Alloy.js (`sendEvent command -> xdm : {eventType, interactionMixin}`) or batch ingestion
**Sample payload:**

```
{
    "@id": "a7864a96-1eac-4934-ab44-54ad037b4f2b",
    "xdm:timestamp": "2020-09-26T15:52:25+00:00",
    "xdm:eventType": "decisioning.propositionDisplay",
    "https://ns.adobe.com/experience/decisioning/propositions":
    [
        {
            "xdm:items":
            [
                {
                    "xdm:id": "personalized-offer:f67bab756ed6ee4",
                },
                {
                    "xdm:id": "personalized-offer:f67bab756ed6ee5",
                }
            ],
            "xdm:id": "3cc33a7e-13ca-4b19-b25d-c816eff9a70a", //decision event id - taken from experience event for “nextBestOffer”
            "xdm:scope": "scope:12cfc3fa94281acb", //decision scope id - taken from experience event for “nextBestOffer”
        }
    ]
}
```

**Scenario:** Offer clicked
**Event type:** `decisioning.propositionInteract`
**Source:** Web.sdk/Alloy.js (`sendEvent command -> xdm : {eventType, interactionMixin}`) or batch ingestion
**Sample payload:**

```
{
    "@id": "a7864a96-1eac-4934-ab44-54ad037b4f2b",
    "xdm:timestamp": "2020-09-26T15:52:25+00:00",
    "xdm:eventType": "decisioning.propositionInteract",
    "https://ns.adobe.com/experience/decisioning/propositions":
    [
        {
            "xdm:items":
            [
                {
                    "xdm:id": "personalized-offer:f67bab756ed6ee4"
                },
                {
                    "xdm:id": "personalized-offer:f67bab756ed6ee5"
                },
            ],
            "xdm:id": "3cc33a7e-13ca-4b19-b25d-c816eff9a70a", //decision event id
            "xdm:scope": "scope:12cfc3fa94281acb", //decision scope id
        }
    ]
}
```

<!--
## Using a ranking strategy {#using-ranking}

To use the ranking strategy you created above, follow the steps below:

Once a ranking strategy has been created, you can assign it to a placement in a decision (previously known as offer activity). For more on this, see [Configure offers selection in decisions](../offer-activities/configure-offer-selection.md).

1. Create a decision.
1. Add a placement.
1. Add a collection.
1. Choose to rank offers by AI ranking (select it from the drop-down list).
1. Click Add ranking.
1. Select the ranking strategy that you created. All the details of the ranking strategy are displayed.
1. Click Next to confirm.
1. Save your decision.

It is now ready to be used in a decision to rank eligible offers for a placement (see [Configure offers selection in decisions](../offer-activities/configure-offer-selection.md)).
-->


---
solution: Journey Optimizer
title: Consent
description: Conent
feature: Actions
topic: Administration
role: Admin
level: Intermediate
hide: yes
hidefromtoc: yes
---
# Consent management (beta) {#consent-management}

Adobe Experience Platform allows you to easily adopt and enforce marketing policies to respect the consent preferences of their customers. Consent policies are defined in Adobe Experience Platform. Refer to [this documentation](https://experienceleague.adobe.com/docs/experience-platform/data-governance/policies/user-guide.html?lang=en#consent-policy).

In Journey Optimizer, you can apply these consent policies to your custom actions. Customers who have not consented to receive email, push or SMS communication will be excluded and will not receive the message. 

In Journey Optimizer, consent is defined:

* when **configuring a custom action**, you define a channel and marketing action. See this [section](../action/consent.md#consent-custom-action)
* when adding the **custom action in a journey**, you define an additional marketing action. See this [section](../action/consent.md#consent-journey)

## Important notes {#important-notes}

* All activities used in a journey, other than a Read Segment or a Custom Action, are not taken into account. Segment qualification is not taken into account, even if it is used to start a journey.
* If you added conditions and other actions after the custom action, the profile will continue the journey even if he was excluded by a consent policy in the custom action.
* To refresh policies in a custom action positioned in a journey, your journey must have no errors. 

There are two types of latency regaring the use of consent policies:

* **User latency**: the delay from the time a profile changes a consent settings to the moment it is applied in Experience Platform. This can take up to 48h. 
* **Consent policy latency**: the delay from the time a consent policy is created or updated to the moment it is applied. This can take up to 6 hours

## Configuring the custom action {#consent-custom-action}

>[!CONTEXTUALHELP]
>id="ajo-consent-required-marketing-action"
>title="Define a required marketing action"
>abstract="The Required Marketing Action indicates the custom action that will be applied when the action is used in a journey. This cannot be modified on the canvas." 

When configuring a custom action, two fields are used for consent.

The **Channel** field allows you to select the channel related to this custom action: **Email**, **SMS**, or **Push notification**. It will prefill the **Required marketing action** field with the default marketing action for the selected channel. If you select **other**, no marketing action will be defined by default. 

![](assets/consent1.png)

The **Required marketing action** allows you to select the consent policy that you want to apply to the custom action. A default marketing action is selected, but you can click the down arrow to select any available marketing actions from the list.

![](assets/consent2.png)

For certain types of important communications, for example a transactional message sent to reset the client's password, you may not want to apply a consent policy. You will then select **None** in the **Required marketing action** field.

The other steps for configuring a custom action are detailed in [this section](../action/about-custom-action-configuration.md#consent-management).  

### Building the journey {#consent-journey}

>[!CONTEXTUALHELP]
>id="ajo-consent-additional-marketing-action"
>title="Required marketing action"
>abstract="A required marketing action is defined while creating a custom action. This required marketing action cannot be removed from the action or modified." 

>[!CONTEXTUALHELP]
>id="ajo-consent-refresh-policies"
>title="Visualize consent policies that will apply at runtime"
>abstract="Marketing actions bring in consent policies that combine action parameters and individual profile consent values to filter out users. Get the latest definition of these policies by clicking the button to refresh." 

When adding the custom action in a journey, several options allows you to manage consent. Click the **Show read-only fields** to display all parameters.

The **Channel** and **Required marketing action**, defined when configuring the custom action, are displayed at the top of the screen. You cannot modify these fields.

![](assets/consent4.png)

You can define an **Additional marketing action** to set the type of custom action. This allows you to define the purpose of the custom action in this journey. In addition to the required marketing action, which is usually specific to a channel, you can define an additional marketing action which will be specific to the custom action in this particular journey. For example: a workout communication, a newsletter, fitness communication, etc. Both the required marketing action and the additional marketing action will apply.

![](assets/consent3.png)

Click the **Refresh policies** button, at the bottom of the screen, to update and check the list of policies taken into consideration for this custom action. The following data is taken into account for consent:

* marketing actions and additional marketing actions defined in the custom action
* attributes defined in the custom action
* attributes used in the segment, when using a Read segment

>[!NOTE]
>
>Please note that there can be a latency, refer to this [this section](../action/consent.md#important-notes)

The other steps for configuring a custom action in a journey are detailed in [this section](../building-journeys/using-custom-actions.md).  


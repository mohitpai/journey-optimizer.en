---
solution: Journey Optimizer
product: journey optimizer
title: Manage opt-out
description: Learn how to manage opt-out and privacy
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: c5bae757-a109-45f8-bf8d-182044a73cca
---
# Manage opt-out {#consent}

Providing to recipients the capability to unsubscribe from receiving communications from a brand is a legal requirement, as well as ensuring this choice is honored. Learn more about the applicable legislation in the [Experience Platform documentation](https://experienceleague.adobe.com/docs/experience-platform/privacy/regulations/overview.html#regulations){target="_blank"}.

**Why is it important?**

* Failing to comply with these regulations introduces regulatory legal risks for your brand.
* It helps you avoid sending unsolicited communications to your recipients, which could make them mark your messages as spam and harm your reputation.

## Manage unsubscriptions in journeys and campaigns {#opt-out-ajo}

When sending messages from journeys or campaigns, you must always ensure that customers can unsubscribe from future communications. Once unsubscribed, the profiles are automatically removed from the audience of future marketing messages. 

While **[!DNL Journey Optimizer]** provides ways of managing opt-out in emails and SMS messages, push notifications do not require any action on your side, as recipients can unsubscribe through their devices themselves. For example, upon downloading or when using your app, they can select to stop notifications. Similarly, they can change the notification settings through the mobile operating system.

Learn how to manage opt-out in Journey Optimizer email and SMS messages in these sections: 

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="../email/email-opt-out.md">
<img alt="Lead" src="../assets/do-not-localize/privacy-email-optout.jpeg" width="50%">
</a>
<div><a href="../email/email-opt-out.md"><strong>Email opt-out management</strong>
</div>
<p>
</td>
<td>
<a href="../sms/sms-opt-out.md">
<img alt="Infrequent" src="../assets/do-not-localize/privacy-sms-opt-out.jpeg" width="50%">
</a>
<div>
<a href="../sms/sms-opt-out.md"><strong>SMS opt-out management</strong></a>
</div>
<p></td>
</tr></table>

>[!NOTE]
>
>In [!DNL Journey Optimizer], consent is handled by the Experience Platform [Consent schema](https://experienceleague.adobe.com/docs/experience-platform/xdm/field-groups/profile/consents.html){target="_blank"}. By default, the value for the consent field is empty and treated as consent to receive your communications. You can modify this default value while onboarding to one of the possible values listed [here](https://experienceleague.adobe.com/docs/experience-platform/xdm/data-types/consents.html#choice-values){target="_blank"}.

## Implement personalization consent {#opt-out-personalization}

Your customers can also opt out from being presented personalized contents. Once a profile has opted out from personalization, you need to ensure that their data is not used for personalization and you must replace any personalized content with a fallback variant.

### In Decision Management

When leveraging offers, personalization preferences are not automatically implemented in [decision scopes](../offers/offer-activities/create-offer-activities.md#add-decision-scopes) used from a [decisioning](../offers/api-reference/offer-delivery-api/decisioning-api.md) API request or [edge decisioning](../offers/api-reference/offer-delivery-api/edge-decisioning-api.md) API request. In this case, you need to manually enforce personalization consent. To do so, follow the steps below.

>[!NOTE]
>
>Decision scopes used in [!DNL Journey Optimizer] authored channels satisfy this requirement from the journey or campaign they belong to.



1. Create an [Adobe Experience Platform audience](../segment/about-segments.md) using a profile attribute such as: *"Consents to Personalization = True"* to target users who have consented to personalization.

1. When creating a [decision](../offers/offer-activities/create-offer-activities.md), add a decision scope and define an eligibility constraint based on this audience for each evaluation criteria collection that contains personalized offers.

1. Create a [fallback offer](../offers/offer-library/creating-fallback-offers.md) that does not include personalized content.

1. [Assign](../offers/offer-activities/create-offer-activities.md#add-fallback) the non-personalized fallback offer to the decision.

1. [Review and save](../offers/offer-activities/create-offer-activities.md#review) the decision.

If a user has:

* consented for personalization, the decision scope will determine the best offer for that profile.

* not consented for personalization, the corresponding profile will not be eligible for any of the offers that are in the evaluation criteria and will therefore receive the non-personalized fallback offer.

>[!NOTE]
>
>Consent for having profile data used in [data modeling](../offers/ranking/ai-models.md) is not supported yet in [!DNL Journey Optimizer].


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

## About opt-out management {#about}

Providing the capability to recipients to unsubscribe from receiving communications from a brand is a legal requirement. Learn more about the applicable legislation in the [Experience Platform documentation](https://experienceleague.adobe.com/docs/experience-platform/privacy/regulations/overview.html#regulations){target="_blank"}.

**Why is it important?**

* Failing to comply with these regulations introduces regulatory legal risks for your brand.
* It helps you avoid sending unsolicited communications to your recipients, which could make them mark your messages as spam and harm your reputation.

## Opt-out management in Journey Optimizer {#opt-out-ajo}

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
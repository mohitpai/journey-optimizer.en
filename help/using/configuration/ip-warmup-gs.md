---
solution: Journey Optimizer
product: journey optimizer
title: Get started with IP warmup plans
description: Learn how to implement an IP warmup plan
feature: Application Settings
topic: Administration
role: Admin
level: Experienced
keywords: IP, pools, group, subdomains, deliverability
hide: yes
hidefromtoc: yes

---
# Get started with IP warmup plans {#ip-warmup-gs}

<!--
>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_plan"
>title="Define your IP warmup plan"
>abstract="You can perform IP warmup workflows directly from the Journey Optimizer interface in a standardized and efficient way that follows the best practices for optimal deliverability."
-->

>[!BEGINSHADEBOX]

What you'll find in this documentation guide:

* **[Get started with IP warmup](ip-warmup-gs.md)**
* [Create IP warmup campaigns](ip-warmup-campaign.md)
* [Create an IP warmup plan](ip-warmup-plan.md)
* [Run the IP warmup plan](ip-warmup-running.md)

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>The IP warmup feature is currently available as a beta to select users only. To join the beta program, contact Adobe Customer Care.

With [!DNL Journey Optimizer], you can easily perform IP warmup workflows directly from the user interface in a standardized and efficient way that follows the best practices for optimal deliverability.

>[!CAUTION]
>
>This feature only applies to the email channel.

When emails are sent using a new platform, Internet service providers (ISPs) are suspicious of IP addresses that are not recognized. If large volumes of emails are suddenly sent, the ISPs often mark them as spam.

To avoid being marked as spam, you can progressively increase the volume sent using IP warmup plan feature. A new option in the **[!UICONTROL Administration]** menu allows you to do it more smoothly instead of creating complex daily journeys. This should ensure smooth development of the start-up phase and enable you to reduce the overall rate of invalid addresses.

>[!NOTE]
>
>Learn more on increasing your email reputation with IP warming in the [Deliverability Best Practice Guide](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/generic-resources/increase-reputation-with-ip-warming.html).

<!--
Benefits

* Standardization on Campaign which will be easy for practitioners too > why?

* No more pain of creating queries, audiences and testing those as system will create the audiences. 

* Ease of excluding domains and changing the plan with help of simple toggles to exclude OR by editing numbers inline or create new phases or reupload plan if drastic change. No more pain of editing audience definitions, journey conditions

* There is an expectation that with this, it will ease around 30% of effort and will be much better experience for consultant/partner/practitioner - right from planning to execution to reporting
-->

The key steps to implement an IP warmup plan are as follows:

1. You first need to create one or more campaigns with the IP warmup option enabled. [Learn more](ip-warmup-campaign.md) <!--this is usually done by a marketer persona??)-->

1. Create an IP warmup plan in [!DNL Journey Optimizer] and upload the Excel sheet previously filled in with your IP warmup data. [Learn more](ip-warmup-plan.md) <!--this is usually done by a deliverability consultant??-->

1. Select a campaign for each phase of your plan and activate the corresponding runs. [Learn more](ip-warmup-running.md)

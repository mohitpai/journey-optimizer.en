---
title: Condition activity
description: Learn about condition activity
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 496c7666-a133-4aeb-be8e-c37b3b9bf5f9
hide: yes
hidefromtoc: yes
---

# Establish your reputation as a sender

If you recently moved to another email service provider, IP address, or email domain or subdomain, you need to establish your reputation as a sender. Otherwise, your deliveries might be blocked or moved to the spam folder of the recipients' mailbox.

To warm up your IP, you can gradually ramp up the number of your deliveries. See this [use case](../building-journeys/ramp-up-deliveries-uc.md).

## Profile cap condition type {#profile_cap}

Other condition types are detailed in this [section](../building-journeys/condition-activity.md).

Use this condition type to set a maximum number of profiles for a journey path. When this limit is reached, the entering profiles take an alternate path.

You can use this condition type to ramp up the volume of your deliveries. See this [use case](../building-journeys/ramp-up-deliveries-uc.md).

The default cap is 1000. You can set an integer value from 1 to 20,000.

The counter applies only to the selected journey version. The counter is reset to zero after 180 days. After a reset, the entering profiles take the nominal path again until the counter limit is reached.

The nominal path always has priority over the alternate path, even if you move the alternate path above the nominal path on the journey canvas.

![](../assets/profile-cap-condition.png)

## Use case: ramp up your deliveries

If you recently moved to another email service provider, IP address, or email domain or subdomain, you need to establish your reputation as a sender. Otherwise, your deliveries might be blocked or moved to the spam folder of the recipients' mailbox. Learn how to increase your email reputation with IP warming in the [Deliverability Best Practice Guide](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/generic-resources/increase-reputation-with-ip-warming.html){target="_blank"}.

To warm up your IP, you can gradually ramp up the number of your deliveries. Read more about [optimizing deliverability in Journey Optimizer](../deliverability.md).

The purpose of this use case is to create a journey to ramp up your email deliveries. To configure this journey, follow these steps:

1. Create a journey. [Read more](journey-gs.md).

1. Add a **[!UICONTROL Condition]** activity to the journey. [Read more](condition-activity.md).

1. In the **[!UICONTROL Condition]** activity settings, set the maximum number of recipients for your delivery:

   1. In the **[!UICONTROL Condition]** activity settings, set the **[!UICONTROL Type]** field to **[!UICONTROL Profile cap]**. [Read more](condition-activity.md#profile_cap).

   1. Set the **[!UICONTROL Limit]** field to the maximum number of recipients for this delivery.

    ![](../assets/profile-cap-condition.png)

      You can gradually increase this limit up to the total number of your subscribers.

1. Add a **[!UICONTROL Message]** activity to the nominal path after the **[!UICONTROL Condition]** activity.

    ![](../assets/ramp-up-deliveries-message.png)

    When the journey runs, the message is sent the entering profiles, up to the maximum number of profiles that you have specified. When this limit is reached, the entering profiles take the alternate path.

1. Complete the journey with the activities of your choice.

After your IP has warmed up, you can remove this condition.


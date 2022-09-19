---
title: Release notes
description: Journey Optimizer Release notes
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
---
# Release Notes {#release-notes}

This page lists all the new features and improvements for [!DNL Journey Optimizer]. You can also consult the [latest documentation updates](documentation-updates.md) page for more changes.

[!DNL Adobe Journey Optimizer] is built natively on [!DNL Adobe Experience Platform] and inherits from its latest innovations and improvements. Learn more about these changes in [Adobe Experience Platform Release Notes](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html){target="_blank"}.

![Newsletter](../assets/do-not-localize/nl-icon.png) Sign up for the [Adobe Journey Optimizer quarterly newsletter](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"} today, and receive the latest product updates, exciting stories, use cases, tips and more delivered directly to your inbox every quarter.

## September 2022 Release {#sept-2022-release}

### New capabilities

### Improvements

**Administration**

* The user interface for creating channel surfaces, creating IP pools, managing the suppression list and the allowed list, and configuring the SMS channel has been updated. [Learn more](../configuration/get-started-configuration.md)

**Decision management**

* **Capping frequency** - It is now possible to reset the offer capping counter on a daily, weekly or monthly basis - for example, every other Sunday at 12pm UTC. [Learn more](../offers/offer-library/add-constraints.md#capping)

**Journeys**

* A new guardrail has been added to unitary journeys (starting with an event or a segment qualification) to prevent journeys from being erroneously triggered multiple times for the same event. Profile re-entrance will now be temporally blocked by default for 5 minutes. [Learn more](../start/guardrails.md#events-g)

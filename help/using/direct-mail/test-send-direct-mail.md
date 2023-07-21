---
title: Test & send a direct mail message
description: Learn how to test and send a direct mail message in Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
keyword: direct, mail, configuration, direct-mail, provider
---
# Test & send a direct mail message {#direct-mail-test-send}

## Preview the extraction file {#preview-dm}

Once the content of the extraction file has been defined, you can use test profiles to preview and test it. If you inserted personalized content, you can check how this content is displayed in the message, using test profile data.

1. Click **[!UICONTROL Simulate content]**.

1. Click **[!UICONTROL Manage test profiles]** to add a test profile.

1. Find your test profile with the **[!UICONTROL Identity namespace]** and **[!UICONTROL Identity value]** fields. Then, click **[!UICONTROL Add profile]**.

1. Once you selected your test profile, you can close the **[!UICONTROL Add test profile]** window.

1. From the **Preview & test** window, test profile data is added to the message content.

## Validate your direct mail message {#dm-validate}

You must check alerts in the upper section of the editor. Some of them are simple warnings, but others can prevent you from sending the message. Two types of alerts can happen: warnings and errors.

* **Warnings** refer to recommendations and best practices. For example, a warning message is displayed if your SMS message is empty.

* **Errors** prevent you from publishing the campaign, as long as they are not resolved. For example, an error message warns you when the subject line is missing.

## Send your direct mail message {#dm-send}

When your direct mail message is ready, complete the configuration of your [campaign](../campaigns/create-campaign.md) to send it.

When the campaign will start, the extraction file will be automatically generated and exported to the server specified in your [file routing configuration](../direct-mail/direct-mail-configuration.md).

Once sent, you can measure the impact of your direct mail messages within the Campaign reports. For more on reporting, refer to this section.
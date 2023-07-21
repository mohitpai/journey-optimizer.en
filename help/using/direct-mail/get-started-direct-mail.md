---
title: Get started with direct mail
description: Learn how to create and a direct mail message in Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
keywords: direct mail, message, campaign
---
# Create a direct mail message {#create-direct}

Direct mail is an offline channel that allows you to personalize and generate the extraction files required by direct mail providers to send mail to your customers.

When you create a direct mail, Journey Optimizer generates a file including all the targeted profiles and the chosen data (postal address, profile attributes for example). Your direct mail provider will then be able to retrieve that file and will take care of the actual sending.

Direct mail messages can only be created in the context of scheduled campaigns. They are not available for use in API-triggered campaigns or in journeys.

>[!IMPORTANT]
>
>Before sending a direct mail message, make sure you have configured:
>
>1. A [file routing configuration](../direct-mail/direct-mail-configuration.md#file-routing-configuration) which specifies the server where the extraction file should be uploaded and stored,
>1. A [direct mail message surface](../direct-mail/direct-mail-configuration.md#direct-mail-surface) which will reference the file routing configuration.

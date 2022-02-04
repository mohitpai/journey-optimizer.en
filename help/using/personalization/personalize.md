---
title: Personalize content in Journey Optimizer
description: Get Started with personalization.
feature: Personalization
topic: Personalization
role: Data Engineer
level: Beginner
exl-id: f448780b-91bc-455e-bf10-9a9aee0a0b24
---
# Get started with personalization{#add-personalization}

Discover [!DNL Adobe Journey Optimizer] personalization capabilities to adapt your messages to each specific recipient by leveraging the data and information you have about them. It can be their first name, interests, where they live, what they bought, and more.

➡️ [Learn how to personalize a message in these videos](#video-perso)

[!DNL Journey Optimizer] uses an **inline** simple personalization syntax based on Handlebars which allows you to create expressions with contents enclosed by double curly braces **{{}}**. You can add multiple expressions in the same content or field without restrictions. Learn more in [Personalization syntax](personalization-syntax.md).

The personalization is based on the profile data that are managed by the **XDM Individual Profile** schema defined in Adobe Experience Platform. Learn more in [Adobe Experience Platform Data Model (XDM) documentation](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html){target="_blank"}.

>[!CAUTION]
>The **XDM Individual Profile** schema is the only schema you can use to personalize content in [!DNL Journey Optimizer].

**Examples:**

* `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}`

* `Hello {{profile.person.name.fullName}}`

When processing the message (email and push), Journey Optimizer replaces the expression with the data contained in the Experience Cloud Platform database:  `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}` becomes “Hello John Doe”.

## How-to videos{#video-perso}

Learn how to use contextual event information from a journey to personalize a message.

>[!VIDEO](https://video.tv.adobe.com/v/334165?quality=12)

Learn how to use contextual event information from a journey to personalize a message.

>[!VIDEO](https://video.tv.adobe.com/v/334078?quality=12)

---
title: Ranking methods
description: Learn how to work with ranking methods
feature: Experience Decisioning, Ranking
topic: Integrations
role: User
level: Intermediate
hide: yes
hidefromtoc: yes
badge: label="Beta"
exl-id: c1d69bc9-4486-4037-b218-f4f704b2ba9c
---
# Ranking methods {#rankings}

>[!CONTEXTUALHELP]
>id="ajo_exd_config_formulas"
>title="Create ranking formulas"
>abstract="Formulas allow you to define rules that will determine which item should be presented first, rather than taking into account the item's priority scores. Once a ranking method has been created, you can assign it to a decision strategy to define which items should be selected first."

>[!BEGINSHADEBOX]

What you'll find in this documentation guide:

* [Get started with Experience Decisioning](gs-experience-decisioning.md)
* Manage your decision items
    * [Configure the items catalog](catalogs.md)
    * [Create decision items](items.md)
    * [Manage items collections](collections.md)
* Configure items' selection
    * [Create decision rules](rules.md)
    * **[Create ranking methods](ranking.md)**
* [Create selection strategies](selection-strategies.md)
* [Create decision policies](create-decision.md)

>[!ENDSHADEBOX]

Ranking methods allow you to rank items to display for a given profile. Once a ranking method has been created, you can assign it to a decision strategy to define which items should be selected first.

Ranking methods are accessible from the **[!UICONTROL Configuration]** / **[!UICONTROL Ranking methods]** menu. Two types of ranking methods are available:

* **Formulas** allow you to define rules that will determine which item should be presented first, rather than taking into account the item's priority scores.

* **AI models** allow you to use trained model systems that will leverage multiple data points to determine which item should be presented first.

![](assets/ranking-create.png)

Detailed information on each type of ranking method and how to create them is available in the decision management documentation accessible here:

* [Ranking formulas](../offers/ranking/create-ranking-formulas.md)
* [AI models](../offers/ranking/ai-models.md)

---
solution: Journey Optimizer
product: journey optimizer
title: Search, filter, organize
description: Learn more about Journey Optimizer User Interface
feature: Overview
topic: Content Management
role: User
level: Intermediate
---

# Search, filter, organize {#search-filter-organize}

## Search{#unified-search}

Anywhere from Adobe Journey Optimizer interface, use the Unified Adobe Experience Cloud search capability on the center of the top bar to find assets, journeys, datasets, and more across your sandboxes. 

Start entering content to display top results. Help articles about the entered keywords also show up in the results.

![](assets/unified-search.png)

Press **Enter** to access all results and filter by business object.

![](assets/search-and-filter.png)

## Filter lists{#filter-lists}

In most of the lists, use the search bar to find specific items, and define filtering criteria.

Filters can be accessed by clicking on the filter icon on the top left of a list. The filter menu allows you to filter the displayed elements according to different criteria: You can choose to display only elements of a certain type or status, the ones you created, or the ones modified in the last 30 days. Options differ depending on the context.

Additionally, you can use Unified tags to filter a list depending on the tags assigned to an object. For now, tags are available for journeys and campaigns. [Learn how to work with tags](#tags)

>[!NOTE]
>
>Note that columns displayed can be personalized using the configuration button on the top right of the lists. Personalization is saved for each user.

In the lists, you can perform basic actions on each element. For example, you can duplicate or delete an item.

![](assets/journey4.png)

## Work with Unified tags {#tags}

With Adobe Experience Platform [Unified Tags](https://experienceleague.adobe.com/docs/experience-platform/administrative-tags/overview.html), you can easily classify your Journey Optimizer journeys and campaigns to improve search from the lists.

>[!AVAILABILITY]
>
>Unified tags are currently in Beta. The documentation and the functionality are subject to change.

### Add tags to an object

The **Tags** field, in the [journey](../building-journeys/journey-gs.md#change-properties) or [campaign](../campaigns/create-campaign.md#create) properties, allows you to define tags for your object. You can either select an existing tag, or create a new one.

Start typing the name of the desired tag and select it from the list. If it is not available, click **Create** to create a new one and add it. You can define as many tags as needed.

![](assets/tags1.png)

The list of tags defined is displayed below the **Tags** field. 

>[!NOTE]
>
> Tags are case in-sensitive
> 
> If you duplicate or create a new version of a journey or campaign, tags are preserved.

### Filter on tags

The journeys and campaigns lists display a dedicated column so you can easily visualize your tags. 

A filter is also available to only display journeys or campaigns with certain tags.

![](assets/tags2.png)

You can add or remove tags from any type of journey or campaign (live, draft, etc). To do this, click the **More actions** icon next to the object, and select **Edit tags**. 

![](assets/tags3.png)

### Manage tags

Administrators can delete tags and organize them by categories using the **Tags** menu, under **ADMINISTRATION**. Learn more on tags management in the [Unified Tags documentation](https://experienceleague.adobe.com/docs/experience-platform/administrative-tags/ui/managing-tags.html). 

>[!NOTE]
>
> Tags created directly from the **[!UICONTROL Tags]** field in Journey Optimizer are automatically added to the built-in "Uncategorized" category.

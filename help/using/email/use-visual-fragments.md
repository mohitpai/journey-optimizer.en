---
solution: Journey Optimizer
product: journey optimizer
title: Use visual fragments
description: Learn how to use visual fragments when creating emails in Journey Optimizer campaigns and journeys
feature: Overview
topic: Content Management
role: User
level: Beginner

---
# Add visual fragments to your emails {#use-visual-fragments}

You can use a visual fragment in an [email](get-started-email-design.md) within a journey or a campaign, or in a [content template](../content-management/content-templates.md).

>[!NOTE]
>
>Learn how to create and manage fragments in [this section](../content-management/fragments.md).

➡️ [Learn how to manage, author and use fragments in this video](../content-management/fragments.md#video-fragments)

## Use a fragment {#use-fragment}

1. Open any email or template content using the [Email Designer](get-started-email-design.md).

1. Select the **[!UICONTROL Fragments]** icon from the left rail.

    ![](assets/fragments-in-designer.png)

1. The list of all visual fragments created on the current sandbox is displayed. You can:

    * Search for a specific fragment by starting typing its label.
    * Sort fragments in ascending or descending order.
    * Change the way the fragments are displayed (cards or list view).

    >[!NOTE]
    >
    >Fragments are sorted by creation date: recently added visual fragments are shown first in the list.

1. You can search and refresh the list.

    >[!NOTE]
    >
    >If some fragments were modified or added while you are editing your content, the list will be updated with the latest changes.

1. Drag and drop any fragment from the list into the area where you want to insert it.

    ![](assets/fragment-insert.png)

1. Like any other component, you can move the fragment around in your content.

1. Select the fragment to display the corresponding pane on the right. From there, you can delete the fragment from your content, or duplicate it. You can also perform these actions directly from the contextual menu that displays on top of the fragment.

    ![](assets/fragment-right-pane.png)

1. From the **[!UICONTROL Settings]** tab, you can:

    * Choose the devices you want the fragment to be displayed on.
    * Open the fragment in a new tab to edit it if needed. [Learn more](../content-management/fragments.md#edit-fragments)
    * Explore references. [Learn more](../content-management/fragments.md#explore-references)

1. You can further customize your fragment using the **[!UICONTROL Styles]** tab.

1. If needed, you can break the inheritance with the original fragment. [Learn more](#break-inheritance)

1. Add as many fragments as you want and **[!UICONTROL Save]** your changes.

## Break inheritance {#break-inheritance}

When you edit a visual fragment, the changes are synchronized. They are automatically propagated to all **[!UICONTROL Draft]** journeys/campaigns and content templates containing that fragment.

>[!NOTE]
>
>The changes are not propagated to emails used in **[!UICONTROL Live]** journeys or campaigns.

When added to an email or a content template, fragments are synchronized by default.

However, you can break the inheritance from the original fragment. In that case, the content of the fragment is copied into the current design, and the changes are not synchronized anymore.

To break inheritance, follow the steps below:

1. Select the fragment.

1. Click the unlock icon from the contextual toolbar.

    ![](assets/fragment-break-inheritance.png)

1. That fragment becomes a standalone element that is not linked anymore to the original fragment. Edit it as any other content component in your content. [Learn more](content-components.md)


---
title: Create an email
description: Learn how to create an email in Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: c77dc420-a375-4376-ad86-ac740e214c3c
---
# Create a landing page {#create-lp}

To access the landing page list, select **[!UICONTROL Journey Management]** > **[!UICONTROL Landing pages]** from the left menu.

![](../assets/lp_access-list.png)

The **[!UICONTROL Landing Pages]** list displays all the landing pages created. You can filter them based on their status or modification date.

## Create the landing page

The steps to create a landing page are as follows.

1. From the landing page list, click **[!UICONTROL Create landing page]**.

    ![](../assets/lp_create-lp.png)

1. Add a title. You can add a description if needed.

    ![](../assets/lp_create-lp-details.png)

1. Click **[!UICONTROL Create]**.

1. The landing primary page and its properties display. Configure the primary page. See [here](#design-lp-content)

    ![](../assets/lp_primary-page.png)

1. Click the + icon to add a subpage. Learn more [here](#design-lp-content)

## Configure the primary page {#configure-primary-page}

1. You can change the page name, which is **[!UICONTROL Primary page]** by default.

1. Edit the content of your page using the content designer. Hover the mouse over the primary page and click **[!UICONTROL Open Designer]**, or click the corresponding button from the right palette. Learn how to design landing page content [here]((#design-lp-content)

    ![](../assets/lp_open-designer.png)

1. Define your landing page URL.

    ![](../assets/lp_access-url.png)

    >[!NOTE]
    >
    >The first part is pre-filled and cannot be edited through the user interface. To set it up, contact your Adobe representative or the [Adobe Customer Care Support Team](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/support-for-experience-cloud.ug.html){target="_blank"}.

1. You can define an expiry date for your page. In that case, you must select an action upon page expiry:

    * **[!UICONTROL Redirect URL]**: Enter the URL of the page the users will be redirected to when the page expires.
    * **[!UICONTROL Custom page]**: Configure a subpage and select it from the drop-down list that displays. Learn more [here](#configure-subpages)
    * **[!UICONTROL Browser error]**: Type the error text that will be displayed instead of the page.

    ![](../assets/lp_expiry-date.png)

1. In the **[!UICONTROL Additional data]** section, (you can define how the data entered in the landing page is managed once it has been submitted by a user)??

1. You can create a journey to send a confirmation message to users when they submit the form from this page. Click **[!UICONTROL Create journey]** to start configuring this journey from here. You will be redirected to the **[!UICONTROL Journey Management]** > **[!UICONTROL Journeys]** list. Learn more on [building journeys](../building-journeys/journey-gs.md#jo-build).

## Configure subpages {#configure-subpages}

## Design the landing page content {#design-lp-content}

1. Click **[!UICONTROL Open Designer]**. The Content Designer opens and enables you to design content. [Learn more](../design-emails.md) on designing content with the [!DNL Journey Optimizer] Content Designer. You can:

    * **Design your landing page from scratch** through the content designer's interface and leverage images from [Adobe Experience Manager Assets Essentials](assets-essentials.md). Learn how to design your content or use built-in templates [in this section](../create-email-content.md).

    * **Code or paste raw HTML** directly in the content designer. Learn how to code your own content [in this section](../existing-content.md#import-raw-html-code).

    * **Import existing HTML content** from a file or a .zip folder. Learn how to import content [in this section](../existing-content.md#import-html-content-from-file).

1. Use the landing page-specific **[!UICONTROL Form]** component from the left palette to add checkboxes.

    ![](../assets/lp_designer-form-component.png)

***

**Questions**

* Will the name Email Designer be kept if you can also design LP with the same tool?

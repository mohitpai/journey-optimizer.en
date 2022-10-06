---
title: Author a web page
description: Learn how to author a web page and edit its content in Journey Optimizer
feature: Web channel
topic: Content Management
role: User
level: Beginner
hide: yes
hidefromtoc: yes
---
# Author web pages {#author-web}

In order to add modifications to your website:

* You must download the [Adobe Experience Cloud Visual Editing Helper](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target="_blank"} browser extension on Chrome to access the web designer.

    >[!CAUTION]
    >
    >Currently to author web pages you can only use Chrome.

    <!--Add link to documentation (first to be documented for Target so we should be able to use the same doc).-->

* You need to implement the [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html){target="_blank"} on your website.

## Create a web campaign {#create-web-campaign}

1. Create a campaign. [Learn more](../campaigns/create-campaign.md)

1. Select the **[!UICONTROL Web]** action.

    ![](assets/web-create-campaign.png)

1. Set a web surface, meaning the URL where the content will be delivered.

    >[!NOTE]
    >
    >    A web surface represents a web property identified by an URL that can match a single page URL or multiple pages, allowing users to deliver the modifications across one or multiple web pages.

    You can either:

    * Enter or select a **[!UICONTROL Page URL]** (will then be converted to a surface string) if you want to apply the changes to a single page only.

    ![](assets/web-campaign-surface.png)
    
    * Define a **[!UICONTROL Pages matching rule]** to target multiple URLs matching the same rule - for example, if you want to apply the changes to a hero banner accross a whole website or add a top image that displays on all the product pages of a website.

    ![](assets/web-campaign-matching-rule.png)

1. Select **[!UICONTROL Create]**.

1. From the **[!UICONTROL Action]** tab of the campaign, select **[!UICONTROL Edit content]**.

    ![](assets/web-edit-content.png)

1. Enter the URL of the page you want to personalize.

    >[!NOTE]
    >
    >If you entered a single URL as the web surface, the URL to personalize is already populated. If you defined a **[!UICONTROL Pages matching rule]**, you must enter any URL matching this rule. The changes will be applied to all pages matching the rule.

    ![](assets/web-edit-enter-url.png)

    >[!CAUTION]
    >
    >The web page must be implemented using the [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html){target="_blank"}.


1. The content of the page displays. Click **[!UICONTROL Open web designer]** to edit it.

    ![](assets/web-open-designer.png)

## Edit a web page content {#edit-web-content}

Once you created a web action from the campaign, follow the steps below to edit its content with the web designer.

![](assets/web-designer.png)

1. You can replace an image, a link, etc.

1. You can duplicate and delete any element.

1. From the **[!UICONTROL Components]** pane on the left, you can add the following components to your web page and edit them as you need:

    * [Divider](../design/content-components.md#divider)
    * [HTML](../design/content-components.md#HTML)
    * [Image](../design/content-components.md#image)
    * Heading - Using this component is similar to using the **[!UICONTROL Text]** component in the email designer. [Learn more](../design/content-components.md#text)
    * Paragraph - Using this component is similar to using the **[!UICONTROL Text]** component in the email designer. [Learn more](../design/content-components.md#text)
    * Link - Learn how to define link styling in [this section](../design/styling-links.md)
    * [Offer decision](../design/deliver-personalized-offers.md)

    ![](assets/web-designer-components.png)

1. Hover in the page and click the **[!UICONTROL Insert before]** or **[!UICONTROL Insert after]** button to append the component to an existing element on the page.

    ![](assets/web-designer-insert-components.png)

1. From the container that displays for this component, edit the component content as needed.

    ![](assets/web-designer-edit-html.png)

1. Adjust the styles that display from the **[!UICONTROL Container]** pane on the right, such as background, text color, border, size, position, etc. depending on the selected component.

    ![](assets/web-designer-html-style.png)

1. Select the **[!UICONTROL Expand/Collapse Breadcrumbs]** button on the lower left side of the screen to quickly display information about the selected element.

    ![](assets/web-designer-breadcrumbs.png)

    When you hover over the breadcrumbs, the corresponding element is highlighted in the editor. Using it you can easily navigate to any parent, sibling, or child element within the visual editor.

## Browse mode {#browse-mode}

You can swap from the default **[!UICONTROL Design]** mode to the **[!UICONTROL Browse]** mode using the dedicated button.

![](assets/web-designer-browse-mode.png)

From the **[!UICONTROL Browse]** mode, you can navigate to the exact page from the selected surface you want to personalize.

It is especially useful when dealing with pages that are behind authentication or that are not available from the start at a certain URL. For example, you will be able to authenticate, navigate to your account page or to your cart page and then switch back to **[!UICONTROL Design]** mode in order to perform the changes on your desired page.

## Change device size

You can change the device size to a predefined size such as **[!UICONTROL Tablet]** or **[!UICONTROL Mobile landscape]**, or define a custom size. Enter the desired number of pixels to define a custom size.

You can also change the zoom focus - from 25% to 400%.

![](assets/web-designer-device.png)

## Manage modifications on a web page {#manage-modifications}

You can easily manage all the components, adjustments and styles you added to your page.

1. Select the **[!UICONTROL Modifications]** button to display the corresponding pane on the left.

    ![](assets/web-designer-modifications-pane.png)

1. You can review each of the changes you made to the page.

1. Select an unwanted modification and click the delete icon to remove it.

    ![](assets/web-designer-modifications-delete.png)

    >[!CAUTION]
    >
    >Proceed with care when deleting an action as it may impact subsequent actions.

1. You can also cancel and redo actions using the corresponding buttons on top right of the screen.

    <!--![](assets/web-designer-cancel-redo.png)-->

## Add personalization and offers to a web page

To add personalization, select a container and select the personalization icon from the contextual menu bar that displays. Add your changes using the Expression editor. [Learn more](../personalization/personalization-build-expressions.md)

![](assets/web-designer-personalization.png)

Use the **[!UICONTROL Offer decision]** component to insert [offers](../offers/get-started/starting-offer-decisioning.md) into your messages. It will leverage Decision Management to pick the best offer to deliver to your customers. [Learn more](../design/deliver-personalized-offers.md)

![](assets/web-designer-offer.png)

## Preview and test

>[!CAUTION]
>
>You must have test profiles available to simulate which offers will be delivered to them. Learn how to [create test profiles](../../segment/creating-test-profiles.md).

1. Click **[!UICONTROL Simulate content]**.

    ![](assets/web-designer-simulate.png)

1. Click **[!UICONTROL Manage test profiles]** to select one or more test profiles.
1. A preview of your modified web page is displayed. You can either open in the default browser or copy the test URL to use it in a different browser.

    ![](assets/web-designer-preview.png)

<!--See simulation.md and preview.md-->
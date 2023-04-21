---
title: Author web pages
description: Learn how to author a web page and edit its content in Journey Optimizer
feature: Web Channel
topic: Content Management
role: User
level: Beginner
exl-id: 3847ac1d-2c0a-4f80-8df9-e8e304faf261
badge: label="Beta" type="Informative"
---
# Author web pages {#author-web}

Once you [added a web action](create-web.md#create-web-campaign) to your campaign, you can edit the content of your site using the web designer. 

In [!DNL Journey Optimizer], web authoring is powered by the **Adobe Experience Cloud Visual Helper** chrome browser extension. [Learn more](web-prerequisites.md#visual-authoring-prerequisites)

>[!CAUTION]
>
>To be able to access and author web pages in the [!DNL Journey Optimizer] user interface, make sure you follow the prerequisites listed in [this section](web-prerequisites.md).

## Edit web page content {#edit-web-content}

>[!CONTEXTUALHELP]
>id="ajo_web_url_to_edit_surface"
>title="Confirm the URL to edit"
>abstract="Confirm the URL of the specific web page to use for editing the content that will be applied on the web surface defined above. The web page must be implemented using the Adobe Experience Platform Web SDK."
>additional-url="https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html" text="Learn more"

>[!CONTEXTUALHELP]
>id="ajo_web_url_to_edit_rule"
>title="Enter the URL to edit"
>abstract="Enter the URL of a specific web page to use for editing the content that will be applied to all pages matching the rule. The web page must be implemented using Adobe Experience Platform Web SDK."
>additional-url="https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html" text="Learn more"

To start authoring your web campaign, follow the steps below.

1. From the **[!UICONTROL Action]** tab of the [campaign](create-web.md#create-web-campaign), select **[!UICONTROL Edit content]**.<!--change screen with rule-->

    ![](assets/web-campaign-edit-content.png)

1. If you created a pages matching rule, you must enter any URL matching this rule: the changes will be applied to all pages matching the rule. The content of the page displays.

    >[!NOTE]
    >
    >If you entered a single URL as the web surface, the URL to personalize is already populated.

    ![](assets/web-edit-enter-url.png)

    >[!CAUTION]
    >
    >The web page must include the [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html){target="_blank"}. [Learn more](web-prerequisites.md#implementation-prerequisites)
    
1. Click **[!UICONTROL Edit web page]** to start authoring it. The web designer displays.

    ![](assets/web-designer.png)

    >[!NOTE]
    >
    >If you attempt to load a website that fails to load, a message displays suggesting that you install the [Visual Editing Helper browser extension](#install-visual-editing-helper). See some tips for troubleshooting in [this section](web-prerequisites.md#troubleshooting).

1. Select any element from the canvas, such as image, button, paragraph, text, container, heading, link etc. [Learn more](#content-components)

1. Use:

    * The contextual menu to edit its content, layout, insert links or personalization, etc.

        ![](assets/web-designer-contextual-bar.png)

    * The icons on top of the right panel to edit, duplicate, delete or hide each element.

        ![](assets/web-designer-right-panel-icons.png)

    * The right panel that changes dynamically according to the selected element. For example, you can edit the background, typography, border, size, position, spacing, effects or inline styles of an element.

        ![](assets/web-designer-right-panel.png)

>[!NOTE]
>
>The web content designer is mostly similar to the email designer. Learn more on [designing content with [!DNL Journey Optimizer]](../email/get-started-email-design.md).

## Use components {#content-components}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_components"
>title="Add components to your web page"
>abstract="You can add a number of components to your web page and edit them as you need."

1. From the **[!UICONTROL Components]** pane on the left, select an item. You can add the following components to your web page and edit them as you need:

    * [Divider](../email/content-components.md#divider)
    * [HTML](../email/content-components.md#HTML)
    * [Image](../email/content-components.md#image)
    * Heading - Using this component is similar to using the **[!UICONTROL Text]** component in the email designer. [Learn more](../email/content-components.md#text)
    * Paragraph - Using this component is similar to using the **[!UICONTROL Text]** component in the email designer. [Learn more](../email/content-components.md#text)
    * Link
    * [Offer decision](../email/add-offers-email.md)

    ![](assets/web-designer-components.png)

1. Hover in the page and click the **[!UICONTROL Insert before]** or **[!UICONTROL Insert after]** button to append the component to an existing element on the page.

    ![](assets/web-designer-insert-components.png)

    >[!NOTE]
    >
    >To unselect a component, click the **[!UICONTROL ESC]** button in the contextual blue banner displayed on top of the canvas.

1. Edit the component as needed directly in the content of your page.

    ![](assets/web-designer-edit-header.png)

1. Adjust the styles that display from the contextual pane on the right, such as background, text color, border, size, position, etc. - depending on the selected component.

    ![](assets/web-designer-header-style.png)

## Manage modifications {#manage-modifications}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_modifications"
>title="Easily manage all your changes"
>abstract="Using this pane, you can navigate through and manage all the adjustments and styles you added to your web page."

You can easily manage all the components, adjustments and styles you added to your web page.

1. Select the **[!UICONTROL Modifications]** icon to display the corresponding pane on the left.

    ![](assets/web-designer-modifications-pane.png)

1. You can review each of the changes you made to the page.

1. Select an unwanted modification and click the delete icon to remove it.

    ![](assets/web-designer-modifications-delete.png)

    >[!CAUTION]
    >
    >Proceed with care when deleting an action as it may impact subsequent actions.

1. Use the **[!UICONTROL More actions]** button on top of the **[!UICONTROL Modifications]** pane to delete all modifications at once.

    ![](assets/web-designer-delete-modifications.png)

1. From the **[!UICONTROL More actions]** menu you can also delete only the invalid modifications, meaning the changes that were overriden by other changes. For example, if you modify the color of a text and then you delete that text, the color modification becomes invalid as the text does not exist anymore.

1. You can also cancel and redo actions using the **[!UICONTROL Undo/Redo]** button on top right of the screen.

    ![](assets/web-designer-undo-redo.png)

    Click and hold the button to switch between the **[!UICONTROL Undo]** and **[!UICONTROL Redo]** options. Then click the button itself to apply the desired action.

## Use click tracking {#use-click-tracing}

This ability in the web designer allows you to select any element of your website and track the clicks on that element.

Once your campaign is live, you can check the number of clicks for each element in the campaign web report. This information can be useful to improve your website users' experience. For example, if the [web reports](../web-report.md) show that many users click an element that is not actually clickable, you may want to add a link to that element.

1. Select an element in your page and choose **[!UICONTROL Click track element]** from the contextual menu.

    ![](assets/web-designer-click-track.png)
    
    >[!NOTE]
    >
    >Any item, clickable or not, can be selected.

1. The corresponding tracked action automatically displays in the **[!UICONTROL Click track]** pane on the left. 

    ![](assets/web-designer-click-track-pane.png)

1. Add a label to manage all your tracked elements and find them easily in the reports.

    ![](assets/web-designer-click-tracking-label.png)

1. Repeat the steps above to select as many other elements as you need for click tracking. The corresponding actions are all listed on the left pane.

    ![](assets/web-designer-click-tracking-actions.png)

1. To remove click tracking on an element, select the corresponding delete icon.

Once your campaign is active, you can check the campaign report **[!UICONTROL Web]** tab to compare the number of impressions, click rate and number of clicks by element. [Learn more](web-report.md#web-tab)

## Navigate through the web designer {#navigate-web-designer}

### Use breadcrumbs {#breadcrumbs}

1. Select any element from the canvas.

1. Click the **[!UICONTROL Expand/Collapse Breadcrumbs]** button on the lower left side of the screen to quickly display information about the selected element.

    ![](assets/web-designer-breadcrumbs.png)

1. When you hover over the breadcrumbs, the corresponding element is highlighted in the editor.

1. Using it you can easily navigate to any parent, sibling, or child element within the visual editor.

### Swap to browse mode {#browse-mode}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_browse"
>title="Use the browse mode"
>abstract="From this mode, you can navigate to the exact page from the selected surface you want to personalize."

You can swap from the default **[!UICONTROL Design]** mode to the **[!UICONTROL Browse]** mode using the dedicated button.

![](assets/web-designer-browse-mode.png)

From the **[!UICONTROL Browse]** mode, you can navigate to the exact page from the selected surface you want to personalize.

It is especially useful when dealing with pages that are behind authentication or that are not available from the start at a certain URL. For example, you will be able to authenticate, navigate to your account page or to your cart page, and then switch back to **[!UICONTROL Design]** mode in order to perform the changes on your desired page.

### Change device size {#change-device-size}

You can change the device size of the web designer display to a predefined size such as **[!UICONTROL Tablet]** or **[!UICONTROL Mobile landscape]**, or define a custom size by entering the desired number of pixels.

You can also change the zoom focus - from 25% to 400%.

![](assets/web-designer-device.png)

The ability to change the device size is designed for responsive sites that render well on various devices, windows, and screen sizes. Responsive sites automatically adjust and adapt to any screen size, including desktops, laptops, tablets, or mobile phones.

>[!CAUTION]
>
>You can edit a web experience with a specific device size. However, these changes apply to all sizes and devices, not just the device size that you're working in. Similarly, editing an experience in the normal desktop view changes the page for all screen sizes, not just the desktop view. Currently, [!DNL Journey Optimizer] does not support device size-specific page changes.

## Add personalization and offers 

To add personalization, select a container and select the personalization icon from the contextual menu bar that displays. Add your changes using the Expression editor. [Learn more](../personalization/personalization-build-expressions.md)

![](assets/web-designer-personalization.png)

Use the **[!UICONTROL Offer decision]** component to insert [offers](../offers/get-started/starting-offer-decisioning.md) into your web pages. The process is the same as when [adding an offer to an email](../email/add-offers-email.md). It will leverage Decision Management to pick the best offer to deliver to your customers.

![](assets/web-designer-offer.png)

## Test the web campaign {#test-web-campaign}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_preview"
>title="Preview your web experience"
>abstract="Get a simulation of what your web experience will look like."

To display a preview of your modified web experience, follow the steps below.

>[!CAUTION]
>
>You must have test profiles available to simulate which offers will be delivered to them. Learn how to [create test profiles](../segment/creating-test-profiles.md).

1. From either the web campaign edit content screen, select **[!UICONTROL Simulate content]**.

    <!--![](assets/web-designer-simulate.png)-->

    ![](assets/web-campaign-simulate.png)

1. Click **[!UICONTROL Manage test profiles]** to select one or more test profiles.
1. A preview of your modified web page is displayed.

    ![](assets/web-designer-preview.png)

1. You can also open it in the default browser, or copy the test URL to paste it in any browser. This allows you to share the link with your team and stakeholders who will be able to preview the new web experience in any browser before the campaign goes live.

    >[!NOTE]
    >
    >When copying the test URL, the content displayed is the one personalized for the test profile used when the content simulation was generated in [!DNL Journey Optimizer].


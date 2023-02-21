---
title: Author web pages
description: Learn how to author a web page and edit its content in Journey Optimizer
feature: Web Channel
topic: Content Management
role: User
level: Beginner
hide: yes
hidefromtoc: yes
exl-id: 3847ac1d-2c0a-4f80-8df9-e8e304faf261
---
# Author web pages {#author-web}

>[!AVAILABILITY]
>
>The web channel feature is currently available as a beta to select users only.

In [!DNL Journey Optimizer] web authoring is powered by the Adobe Experience Cloud Visual Helper chrome browser extension. [Learn more](visual-editing-helper.md)

To be able to access and author web pages in the [!DNL Journey Optimizer] user interface, follow the prerequisites listed in [this section](create-web.md#prerequesites).

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

<!--Confirm the URL to use for authoring content on the surface. Typically the Authoring URL will be the surface URL itself, but you may include extra parameters if required. The page must include the Adobe Experience Platform Web SDK.-->

Once you created a web action from the campaign, you can edit your content using the web designer. To do so, follow the steps below.

>[!CAUTION]
>
>To be accessed in [!DNL Journey Optimizer], your web page must be implemented using the [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html){target="_blank"}.

1. From the **[!UICONTROL Action]** tab of the campaign, select **[!UICONTROL Edit content]** to start authoring your web campaign.

1. If you created a pages matching rule, you must enter any URL matching this rule. The changes will be applied to all pages matching the rule.

    >[!NOTE]
    >
    >If you entered a single URL as the web surface, the URL to personalize is already populated.

    ![](assets/web-edit-enter-url.png)

1. The content of the page displays.

    >[!CAUTION]
    >
    >The web page must include the [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html){target="_blank"}.
    
1. Click **[!UICONTROL Open web designer]** to edit it. [Learn more](author-web.md)

    ![](assets/web-open-designer.png)

1. The web designer displays.

    ![](assets/web-designer.png)

1. Select any element from the canvas, such as image, button, paragraph, text, container, heading, link etc. and use:

    * The contextual menu to edit its content, layout, insert links or personalization, etc.

        ![](assets/web-designer-contextual-bar.png)

    * The icons on top of the right panel to edit, duplicate, delete or hide each element.

        ![](assets/web-designer-right-panel-icons.png)

    * The right panel that changes dynamically according to the selected element. For example, you can edit the background, typography, border, size, position, spacing, effects or inline styles of an element.

        ![](assets/web-designer-right-panel.png)

## Use content components {#content-components}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_components"
>title="Add content components to your web page"
>abstract="You can add a number of components to your web page and edit them as you need."

1. From the **[!UICONTROL Components]** pane on the left, you can add the following components to your web page and edit them as you need:

    * [Divider](../email/content-components.md#divider)
    * [HTML](../email/content-components.md#HTML)
    * [Image](../email/content-components.md#image)
    * Heading - Using this component is similar to using the **[!UICONTROL Text]** component in the email designer. [Learn more](../email/content-components.md#text)
    * Paragraph - Using this component is similar to using the **[!UICONTROL Text]** component in the email designer. [Learn more](../email/content-components.md#text)
    * Link - Learn how to define link styling in [this section](../email/styling-links.md)
    * [Offer decision](../email/add-offers-email.md)

    ![](assets/web-designer-components.png)

1. Hover in the page and click the **[!UICONTROL Insert before]** or **[!UICONTROL Insert after]** button to append the component to an existing element on the page.

    ![](assets/web-designer-insert-components.png)

1. From the container that displays for this component, edit the component content as needed.

    ![](assets/web-designer-edit-html.png)

1. Adjust the styles that display from the **[!UICONTROL Container]** pane on the right, such as background, text color, border, size, position, etc. depending on the selected component.

    ![](assets/web-designer-html-style.png)

## Navigate through the web designer

### Use breadcrumbs

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

### Change device size

You can change the device size to a predefined size such as **[!UICONTROL Tablet]** or **[!UICONTROL Mobile landscape]**, or define a custom size. Enter the desired number of pixels to define a custom size.

You can also change the zoom focus - from 25% to 400%.

![](assets/web-designer-device.png)

## Manage modifications {#manage-modifications}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_modifications"
>title="Easily manage all your changes"
>abstract="Using this pane, you can navigate through and manage all the adjustments and styles you added to your web page."

You can easily manage all the components, adjustments and styles you added to your web page.

1. Select the **[!UICONTROL Modifications]** button to display the corresponding pane on the left.

    ![](assets/web-designer-modifications-pane.png)

1. You can review each of the changes you made to the page.

1. Select an unwanted modification and click the delete icon to remove it.

    ![](assets/web-designer-modifications-delete.png)

    >[!CAUTION]
    >
    >Proceed with care when deleting an action as it may impact subsequent actions.

1. You can also cancel and redo actions using the **[!UICONTROL Undo/Redo]** button on top right of the screen.

    ![](assets/web-designer-undo-redo.png)

    Click and hold the button to switch between the **[!UICONTROL Undo]** and **[!UICONTROL Redo]** options. Then click the button itself to apply the desired action.

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

1. From either the **[!UICONTROL Edit content]** screen or the web designer, select **[!UICONTROL Simulate content]**.

    ![](assets/web-designer-simulate.png)

1. Click **[!UICONTROL Manage test profiles]** to select one or more test profiles.
1. A preview of your modified web page is displayed.

    ![](assets/web-designer-preview.png)

1. You can also copy the test URL to paste it in any browser, or open it in the default browser.

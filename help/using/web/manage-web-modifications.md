---
title: Manage web modifications
description: Learn how to manage modifications in Journey Optimizer web page content
feature: Web Channel
topic: Content Management
role: User
level: Beginner

---
# Manage web modifications {#manage-web-modifications}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_modifications"
>title="Easily manage all your changes"
>abstract="Using this pane, you can navigate through and manage all the adjustments and styles you added to your web page."

You can easily manage all the components, adjustments and styles you added to your web page. You can also add modifications directly from the dedicated pane.

## Work with the Modifications pane {#use-modifications-pane}

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
<!-->
## Add modifications from the dedicated pane {#add-modifications}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_head"
>title="Use custom code"
>abstract="Select Page `<head>`, custom code is added to the `<head>` section and its execution does not wait for body or page-load events. Add only `<script>` and `<style>` elements. Adding `<div>` tags and other elements might cause remaining `<head>` elements to pop into the `<body>`."

When editing a page using the web designer, you can now add new changes to your content directly from the **[!UICONTROL Modifications]** pane - without the need to select a component and edit it from the web designer interface.


1. Select the **[!UICONTROL Modifications]** icon to display the corresponding pane on the left.

Select Add a modification.

Select the modification type.

It can be either CSS selector or Page `<Head>`.


CSS :
In the CSS Element Selector box, specify the desired CSS element that you want to modify, select an action type ( Set Content or Set Attribute), then fill in the required information and the desired content.

Custom code :
Specify an optional name, select or deselect the Add Code in the `<HEAD>` Section check box, as desired, then add your custom code.

What is a head section?
The `<head>` element is a container for metadata (data about data) and is placed between the `<html>` tag and the `<body>` tag.

If you select Page `<HEAD>`, custom code is added to the `<head>` section and its execution does not wait for body or page-load events. Add only `<script>` and `<style>` elements. Adding `<div>` tags and other elements might cause remaining `<head>` elements to pop into the `<body>`. If you are using at.js, all offers will deliver asynchronously.

    If you select Page <Head>,  code is executed at the beginning of the page load.
     
    You can execute the JavaScript code in the <head> tag. Execution of code does not wait for the <body> tag to be present in the DOM.
    Selectors for subsequent visual actions depend on the HTML elements added in this tab.
    The Custom Code panel is commonly used to add JavaScript or CSS to the top of the page.


Click Advanced editing options. The Expression editor opens. 

You can leverage the [!DNL Journey Optimizer] Expression editor with all its personalization and authoring capabilities. [Learn more](../personalization/personalization-build-expressions.md)

Save your changes.

Click the More actions button to Edit, get Info or Delete your modification.
-->
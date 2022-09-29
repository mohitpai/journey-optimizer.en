---
title: Create an In-App message
description: Learn how to create an In-App message in Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
---
# Create an In-app message {#create-in-app}

![](assets/.png)

1. Access the **[!UICONTROL Campaigns]** menu, then click **[!UICONTROL Create campaign]**.

1. In the **[!UICONTROL Actions]** section, choose the **[!UICONTROL In-app channel]** and the **[!UICONTROL Channel surface]** to use to send your message, then click **[!UICONTROL Create]**.

    For more information on surfaces, refer to this page.

1. From the **[!UICONTROL Properties]** section, edit your Campaign's **[!UICONTROL Title]** and **[!UICONTROL Description]**.

1. Define the audience to target. To do this, click the **[!UICONTROL Select audience]** button to display the list of available Adobe Experience Platform segments. Learn more on segment.

1. In the **[!UICONTROL Identity namespace]** field, choose the namespace to use in order to identify the individuals from the selected segment. Learn more on namespaces.

1. Choose the frequency of your trigger when your In-App message will be active:

    * **[!UICONTROL Show every time]**
    * **[!UICONTROL Show once]**
    * **[!UICONTROL Show until click through]**

1. Choose the event that will trigger your message from the **[!UICONTROL Mobile app trigger]**
drop-down. 
    
    By choosing a trigger, you choose an action done by users which will cause the In-App message to be displayed.

1. To execute your campaign on a specific date or on a recurring frequency, configure the **[!UICONTROL Schedule]** section. Learn how to schedule campaigns.

1. You can now start editing your content with the **[!UICONTROL Edit content]** button.

1. Once your In-app message is configured and personalized, click **[!UICONTROL Review to activate]** to display a summary of your message.

    The summary allows you to modify your campaign if necessary, and to check if any parameter is incorrect or missing.

1. 

## Design content {#design-content}

### Message Layout {#message-layout}

**[!UICONTROL Message Layout]** provides four different layout options to choose from depending on your messaging needs:

* **[!UICONTROL Fullscreen]**: This type of layout covers the entire screen of your audience devices.
    
    It supports media (image, video), text and button components.

* **[!UICONTROL Modal]**: This layout appears in a large alert-style window, your application is still visible in the background.

    It supports media (image, video), text and button components.

* **[!UICONTROL Banner]**: This type of layout appears as a native OS alert message.

    You can only add a **[!UICONTROL Header]** and a **[!UICONTROL Body]** to your message.

* **[!UICONTROL Custom]**: The custom message mode allows you to directly import and edit one of your pre-configured HTML message.

    For more information on this, refer to Create a custom In-app message.

### Content tab {#content-tab}

#### Close button {#close-button}

Choose the **[!UICONTROL Style]** of your **[!UICONTROL Close button]**:
* **[!UICONTROL Simple]**
* **[!UICONTROL Circle]**
* **[!UICONTROL Custom image]** from a Media URL or your Assets.

++++
Learn more on advanced formatting.

Check the **[!UICONTROL Color]** option to choose the color and opacity of your button.
+++

#### Media {#add-media}

The **[!UICONTROL Media]** field allows you to add media to your In-app message to create a compelling experience for end user.

Type-in your Media URL or click the **[!UICONTROL Select Assets]** icon to directly add assets stored in your Assets library to your In-app message. [Learn more about asset management](../design/assets-essentials.md).

++++
Learn more on advanced formatting.

Choose the **[!UICONTROL Max height]** and **[!UICONTROL Max width]** of your media. 
+++

#### Header and Body {#title-body}

To compose your message, type your text in the **[!UICONTROL Header]** and **[!UICONTROL Body]** fields.

You can also use the **[!UICONTROL Personalization]** icon to define content and personalization data.
</br>Learn more about personalization in the Expression Editor [in this section]().

++++
Learn more on advanced formatting.

If the **[!UICONTROL Advanced formatting mode]** is switched on, you can choose for your **[!UICONTROL Header]** and **[!UICONTROL Body]**:

* the **[!UICONTROL Font]**
* the **[!UICONTROL Pt size]**
* the **[!UICONTROL Font Color]**
* the **[!UICONTROL Alignment]**
+++

#### Buttons {#buttons}

Add buttons for users to interact with your In-app message.

To personalize your button, edit the Button #1 text (primary) field. You can also use the **[!UICONTROL Personalization]** icon to define content and personalization data.
Choose your **[!UICONTROL Interact event]** and your **[!UICONTROL Target]** which will define your button's action after users interacted with it.

To add multiple buttons, click **[!UICONTROL Add button]**.

++++
Learn more on advanced formatting.

If the **[!UICONTROL Advanced formatting mode]** is switched on, you can choose for your **[!UICONTROL Buttons]**:

* the **[!UICONTROL Font]**
* the **[!UICONTROL Pt size]**
* the **[!UICONTROL Font Color]**
* the **[!UICONTROL Alignment]**
* the **[!UICONTROL Button style]**
* the **[!UICONTROL Radius]**
* the **[!UICONTROL Button color]**
+++

### Settings tab {#settings-tab}

#### Preview {#preview-tab}

With the URL provided in the App preview field, you can preview your In-app message directly from your browser.

#### Layout {#message}

Choose your **[!UICONTROL Background color]** or **[!UICONTROL Background image]** 

#### Message {#message}

UI takeover

++++
Learn more on advanced formatting.

If the **[!UICONTROL Advanced formatting mode]** is switched on, you can further personalize your message with the following options:

* **[!UICONTROL Customize gestures]**
* **[!UICONTROL UI takeover]**
* **[!UICONTROL Customize UI takeover]**
* **[!UICONTROL Customize size]**
* **[!UICONTROL Customize position]**
* **[!UICONTROL Customize animation]**
* **[!UICONTROL Message round corner]**
* **[!UICONTROL Corner radius]**

## Create a custom In-app message {#custom-inapp}

Use the Custom message layout to import raw HTML and/or code your own content.

1. After clicking the **[!UICONTROL Edit content]** button, select the Custom message layout.

1. From the **[!UICONTROL Content]** tab, select the HTML message options:

    * **[!UICONTROL Compose]** to enter or paste your raw HTML code.
        
        Use the left pane to leverage Journey Optimizer personalization capabilities. For more on this, refer to this section.

    * **[!UICONTROL Import]** to import the HTML or .zip file containing your HTML content.

1. 
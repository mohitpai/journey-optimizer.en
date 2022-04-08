---
title: Get started with messages
description: Learn how to create messages in Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 712dc172-6c0d-4ce8-ba16-de99d65fc641
---
# Get started with messages {#get-started-contents-messages}

Use [!DNL Journey Optimizer] to leverage multiple resources like assets and contents in a single place, and create and publish personalized push notifications and email messages.

* Leverage [!DNL Journey Optimizer] **email designing capabilities** to create or import responsive emails.

* Leverage **Adobe Experience Manager Assets Essentials** to build your own assets database, and enrich your emails.

* Enhance customers' experience by creating **personalized push and email messages** based on their profile attributes.

* **Create push and email messages** based on these contents, then publish them.

## Access messages {#access-messages}

Messages are available from the **[!UICONTROL Messages]** shortcut on the left navigation. All messages are listed, sorted by publication date (for published messages) or creation date (for draft messages).

>[!NOTE]
>
>Users can access, create, edit and/or publish messages depending on their product profile. Learn more about user permissions [in this section](../administration/permissions.md).

![](assets/messages-list.png)

* Use the **[!UICONTROL Show recents]** toggle to add direct links to the messages you accessed in the last 5 days.

   ![](assets/show-recent-messages.png)

* Use the filter icon to display only drafted, published or messages being published. You can also search on message label, as below:

   ![](assets/filter-messages.png)

* You can archive unused messages to clear the message list using the dedicated icon from the quick actions menu.

   ![](assets/archive-message.png)

   Use the filter icon to display all archived messages and click the **[!UICONTROL Unarchive]** icon to remove an item from the list of archived messages.

   >[!NOTE]
   >
   >You cannot open an archived message. You must unarchive it first.

## Create a new message {#create-new-message}

To create a new message, follow the steps below:

1. Access the message list, then click **[!UICONTROL Create Message]**.

1. Define the message properties.

   ![](assets/create-message-properties.png)
    
   * Enter a **[!UICONTROL Title]** (mandatory) and a **[!UICONTROL Description]**. 

   * Select the **[!UICONTROL Message category]**: Marketing or Transactional.

   * Select the channel(s) you want to use for that message: Email and/or Push notification. You must select at least one channel to be able to create the message.

   * Select the **[!UICONTROL Preset]** to use for the message.
        
      Presets include all the parameters that are required for an email and/or push notification to be sent according to your brand. [Learn more about presets](../configuration/message-presets.md).

   >[!CAUTION]
   >
   >You must choose a valid message preset for the selected category and channel(s).

   Note that you can access and modify the message's title, description and preset at any time using the **[!UICONTROL Properties]** button in the message interface.

1. Click **[!UICONTROL Create]** to confirm message creation. Your message is added in the message list, in the **[!UICONTROL Draft]** status.

    One tab is available for each selected channel. Use these tabs to configure the content for each channel. You can remove a tab by selecting it and clicking the **[!UICONTROL Delete channel]** button on the right. 

    ![](assets/create-messages-content.png)

    You can now create the content of the message and adapt settings. Detailed information about email and push notification configuration is available in the following sections:

    * [Create an email](create-email.md)
    * [Create a push notifications](create-push.md)

    >[!NOTE]
    >   
    >You can personalize your messages using profiles' data using the expression editor. For more on personalization, refer to [this section](../personalization/personalize.md).

1. Control the rendering of your messages, and check personalization settings with test profiles, using the preview section on the left-hand side. For more on this, refer to [this section](../design/preview.md).

    ![](assets/messages-simple-preview.png)

1. Check alerts in the upper section of the editor.  Some of them are simple warnings, but others can prevent you from publishing the message. Learn more in [this section](alerts.md).

1. You can now publish your message by clicking the **[!UICONTROL Publish]** button, or keep it as a draft and publish it later on. For more on how to publish messages, refer to [this section](publish-manage-message.md).

## Duplicate a message {#duplicate-message}

To create a message from an existing one, follow the steps below.

1. Open the message you want to copy.

1. Use the **[!UICONTROL Duplicate]** button from the message interface.

   ![](assets/message-duplicate.png)

   All settings and configuration will be copied to the new message.

1. You can rename the message before confirming duplication.

   ![](assets/message-duplicate-confirm.png)

1. A confirmation message displays at the bottom of the window once the new message is created.

You can also duplicate a message from the message list, using the dedicated icon from the quick actions menu.

![](assets/message-duplicate-from-list.png)

The same confirmation process applies.


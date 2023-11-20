---
solution: Journey Optimizer
product: journey optimizer
title: Create content templates
description: Learn how to create templates to reuse content in Journey Optimizer campaigns and journeys
feature: Templates
topic: Content Management
role: User
level: Beginner
exl-id: 327de13a-1c99-4d5e-86cf-8180fb7aaf23
---
# Work with content templates {#content-templates}
 
For an accelerated and improved design process, you can create standalone templates to easily reuse custom content across [!DNL Journey Optimizer] campaigns and journeys.

This functionality enables content-oriented users to work on templates outside campaigns or journeys. Marketing users can then reuse and adapt these standalone content templates inside their own journeys or campaigns.

![](../rn/assets/do-not-localize/content-template.gif)


>[!NOTE]
>
>Currently only the **email** content templates are supported.

For example, a user within your company is in charge of content only, and therefore has no access to campaigns or journeys. However, this user can create an email template that your organization's marketers will be able to select for use in all emails as a starting point.

You can also create and manage content templates using APIs. For more on this, refer to the [Journey Optimizer APIs documentation](https://developer.adobe.com/journey-optimizer-apis/references/content/){target="_blank"}.

➡️ [Learn how to create and use templates in this video](#video-templates)

>[!CAUTION]
>
>To create, edit and delete content templates, you must have the **[!DNL Manage library items]** permission included in the **[!DNL Content Library Manager]** product profile. [Learn more](../administration/ootb-product-profiles.md#content-library-manager)

## Access and manage templates {#access-manage-templates}

To access the content template list, select **[!UICONTROL Content Management]** > **[!UICONTROL Content Templates]** from the left menu.

![](../email/assets/content-template-list.png)

All the templates that were created on the current sandbox - either from a journey or a campaign using the [Save as template](#save-as-template) option, either from the **[!UICONTROL Content Templates]** menu - are displayed.

You can sort content templates by creation or modification date. You can also choose to display only the items that you created or modified.

![](../email/assets/content-template-list-filters.png)

To edit a template content, click the desired item from the list and select **[!UICONTROL Edit content]**.

![](../email/assets/content-template-edit.png)

To delete a template, select the trash icon next to the desired template.

![](../email/assets/content-template-list-delete.png)

>[!NOTE]
>
>When a template is edited or deleted, campaigns or journeys including emails created using this template are not impacted.

## Create content templates {#create-content-templates}

>[!CONTEXTUALHELP]
>id="ajo_create_template"
>title="Define your own content template"
>abstract="Create a standalone custom template from scratch to make your content reusable across multiple journeys and campaigns."

There are two ways you can create content templates:

* Create a content template from scratch, using the left rail **[!UICONTROL Content Templates]** menu. [Learn how](#create-template-from-scratch)

* When designing an email within a campaign or a journey, save your email content as template. [Learn how](#save-as-template)

Once saved, your content template is available for use in a campaign or a journey. Whether created from scratch or from a previous email, you can now use this template when building any [email](../email/get-started-email-design.md) within [!DNL Journey Optimizer]. [Learn how](../email/use-email-templates.md)

>[!NOTE]
>
>* Changes made to content templates are not propagated to campaigns or journeys, whether they are live or draft.
>
>* Similarly, when templates are used in a campaign or a journey, any edits you make to your campaign and journey content do not impact the previously used content template.

### Create template from scratch {#create-template-from-scratch}

To create a content template from scratch, follow the steps below.

1. Access the content template list through the **[!UICONTROL Content Management]** > **[!UICONTROL Content Templates]** left menu.

1. Select **[!UICONTROL Create template]**.

1. Fill in the template details.

    ![](../email/assets/content-template-details.png)

    >[!NOTE]
    >
    >Currently only the **Email** channel and **HTML** type are supported.

1. To assign custom or core data usage labels to the template, select **[!UICONTROL Manage access]**. [Learn more on Object Level Access Control (OLAC)](../administration/object-based-access.md).

1. Select or create Adobe Experience Platform tags from the **[!UICONTROL Tags]** field to categorize your template for improved search. [Learn more](../start/search-filter-categorize.md#tags)

1. Click **[!UICONTROL Create]** and choose how you want to design your template from the different options:

    * [Design your email from scratch](../email/content-from-scratch.md) through the Email Designer's interface.

    * [Code or copy-paste raw HTML](../email/code-content.md) directly into the Email Designer.

    * [Import existing HTML content](../email/existing-content.md) from a file or a .zip folder.

    * Use existing content from a list of built-in or custom templates. The steps to use a content template in an email are described in [this section](../email/use-email-templates.md).

    ![](../email/assets/content-template-design.png)

1. The [Email Designer](../email/get-started-email-design.md) displays. Edit your content as needed, the same way you would do for any email inside a journey or a campaign, according to the option you selected.

    You can test your content if needed. [Learn how](#test-template)

1. Once your template is ready, click **[!UICONTROL Save]**.

1. If needed, click the arrow next to the template name to go back to the **[!UICONTROL Details]** screen and edit your template.

    ![](../email/assets/content-template-designer-back.png)

This template is now ready to be used when building any email within [!DNL Journey Optimizer]. [Learn how](../email/use-email-templates.md)

### Save as template {#save-as-template}

>[!CONTEXTUALHELP]
>id="ajo_messages_depecrated_inventory"
>title="Learn how to migrate your messages"
>abstract="On July 25 2022, the Messages menu disappeared and messages are now authored directly from a Journey. If you want to re-use your legacy messages in journeys, you need to save them as templates."

When designing an [email](../email/get-started-email-design.md) in a campaign or a journey, you can save your email content for future reuse. To do this, follow the steps below.

1. In the Email Designer, click the ellipsis on top right of the screen.

1. Select **[!UICONTROL Save as content template]** from the drop-down menu.

    ![](../email/assets/email_designer-save-template.png)

1. Add a name and description for this template.

    ![](../email/assets/email_designer-template-name.png)

1. To assign custom or core data usage labels to the template, select **[!UICONTROL Manage access]**. [Learn more](../administration/object-based-access.md).

1. Select or create an Adobe Experience Platform tag from the **Tags** field to categorize your template. [Learn more](../start/search-filter-categorize.md#tags)

1. Click **[!UICONTROL Save]**.

1. The template is saved into the **[!UICONTROL Content Templates]** list, accessible from the [!DNL Journey Optimizer] dedicated menu. It becomes a standalone content template that can be accessed, edited and deleted as any other item on that list. [Learn more](#access-manage-templates)

You can now use this template when building any [email](../email/get-started-email-design.md) within [!DNL Journey Optimizer]. [Learn how](../email/use-email-templates.md)

>[!NOTE]
>
>Any change to that new template is not propagated to the email it comes from. Similarly, when the original content is edited within that email, the new template is not modified.

## Test your content template {#test-template}

You can test the rendering of any email content template, whether created from scratch or from an email. To do so, follow the steps below.

1. Access the content template list through the **[!UICONTROL Content Management]** > **[!UICONTROL Content Templates]** menu and select any template.

1. Click **[!UICONTROL Edit content]** from the **[!UICONTROL Template properties]**.

1. Click **[!UICONTROL Simulate Content]** and select a test profile to check your email rendering. You can choose the desktop or mobile view. [Learn more](../content-management/preview-test.md)

    ![](../email/assets/content-template-stimulate.png)

1. You can send a proof to test your content and have it approved by some internal users before using it in a journey or a campaign.

    * To do so, click the **[!UICONTROL Send proof]** button and follow the steps described in [this section](../content-management/proofs.md).
    
    * Before sending the proof, you must select the [email surface](../configuration/channel-surfaces.md) that will be used to test your content.

        ![](../email/assets/content-template-stimulate-proof-surface.png)

>[!CAUTION]
>
>Currently tracking is not supported when testing email content templates, meaning that tracking events, UTM parameters and landing page links will not be effective in the proofs that are being sent from a template. To test tracking, [use the content template](../email/use-email-templates.md) in an email and [send a proof](../content-management/preview-test.md#send-proofs).

## How-to video {#video-templates}

Learn how to create, edit, and use content templates in [!DNL Journey Optimizer].

>[!VIDEO](https://video.tv.adobe.com/v/3413743/?quality=12)

---
solution: Journey Optimizer
product: journey optimizer
title: Work with AEM templates
description: Learn how to create templates in AEM and export them into Journey Optimizer
hide: yes
hidefromtoc: yes
feature: Overview
topic: Content Management
role: User
level: Beginner

---
# Work with Adobe Experience Manager templates {#aem-templates}

Use Abobe Journey Optimizer to personalize and send messages built from Adobe Experience Manager templates. You can use Adobe Experience Manager as a source of content to create and design templates, and send them to Adobe Journey Optimizer. Once shared, these templates are available as email templates in Adobe Journey Optimizer email designer.

>[!AVAILABILITY]
>
>Integration with Adobe Experience Manager is currently available as a beta to select users only.
> As a beta user, use [this form](https://forms.office.com/pages/responsepage.aspx?id=Wht7-jR7h0OUrtLBeN7O4Wf0cbVTQ3tCpW_unE-w8-JUN1FaNlAzNkhPSUdaSkJXVFRCNTRJNVRFSy4u){target="_blank"} to share feedback.

## Before starting{#aem-templates-start}

Before starting using this capability, make sure your are aligned with the following requirements.

### Experience Manager settings{#aem-templates-settings}

This capability is available starting Adobe Experience Manager 6.5.14. You must connect to Adobe Experience Manager Sites on your Managed Services Author environment.

As a part of the beta program, the Cloud Service configuration was performed by Adobe in Adobe Experience Manager to connect to Adobe Journey Optimizer. 

### Permissions{#aem-templates-permissions}

To share a template in Adobe Experience Manager, the following permissions are required: 

To create, edit and delete content templates in Adobe Journey Optimizer, you must have the **[!DNL Manage Library Items]** permission included in the **[!DNL Content Library Manager]** product profile. [Learn more](../administration/ootb-product-profiles.md#content-library-manager)


### Guardrails and limitations{#aem-templates-limitations}

* The Experience Manager template must not contain personalization. Personalization is performed in Journey Optimizer only.
* Bulk template export is not supported: you can export Experience Manager templates one by one only.

## Send a template to Journey Optimizer{#aem-templates-send}

To export an Adobe Experience Manager template to Adobe Journey Optimizer, follow the steps below:

1. Browse to the **Outbound Marketing** section of the user interface.

    ![](assets/aem-outbound-menu.png)

1. Access your content library, select your template and choose **Send to**.

    ![](assets/aem-send-template.png)

1. Enter the name of the content template and select the target sandbox.

    ![](assets/aem-send-template-settings.png)
    
1. Click the **Send** button to validate. Once export is finished, a message is displayed in the user interface.

The template is added to Adobe Journey Optimizer content templates of the selected sandbox.

## Use and personalize an Adobe Experience Manager template{#aem-templates-perso}

Once the Experience Manager template is available in Journey Optimizer as a content template, you can identify and incorporate the necessary content for the email, including personalization.

Learn how to edit and personalize an email content in [this section](content-from-scratch.md).

When your content template is ready, [test and validate it](content-templates.md#test-template). You can then [create emails based on this template](email-templates.md), and complete the configuration of your [journey](../building-journeys/journey-gs.md) or [campaign](../campaigns/create-campaign.md) to send the message.


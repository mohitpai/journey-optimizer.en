---
title: Define landing page presets
description: Learn how to configure your environment to create and use landing pages with Journey Optimizer
role: Admin
level: Intermediate
exl-id: 7cf1f083-bef0-40b5-8ddd-920a9d108eca
---
# Define landing page presets {#lp-presets}

When [creating a landing page](../landing-pages/create-lp.md#create-a-lp), you must select a landing page preset to be able to build the landing page and leverage it through **[!DNL Journey Optimizer]**.

## Access landing page presets {#access-lp-presets}

To access landing page presets, follow the steps below.

1. Access the **[!UICONTROL Administration]** > **[!UICONTROL Channels]** menu.

1. Select **[!UICONTROL Branding]** > **[!UICONTROL Landing page presets]**.

    ![](assets/lp_presets-access.png)

1. Click any preset label to access the landing page preset details.

    ![](assets/lp_preset-details.png)

## Create a landing page preset {#lp-create-preset}

To create a landing page preset, follow the steps below.

>[!NOTE]
>
>To be able to create a preset, make sure you have previously configured at least one landing page subdomain. [Learn how](lp-subdomains.md)

1. Access the **[!UICONTROL Administration]** > **[!UICONTROL Channels]** menu, then select **[!UICONTROL Branding]** > **[!UICONTROL Landing page presets]**.

1. Select **[!UICONTROL Create landing page preset]**.

    ![](assets/lp_create-preset-temp.png)

1. Enter a name and a description for the preset.

    >[!NOTE]
    >
    > Names must begin with a letter (A-Z). It can only contain alpha-numeric characters. You can also use underscore `_`, dot`.` and hyphen `-` characters.

1. Select a landing page subdomain from the drop-down list.

    ![](assets/lp_preset-subdomain.png)

    >[!NOTE]
    >
    >To be able to select a subdomain, make sure you have previously configured at least one landing page subdomain. [Learn how](#lp-subdomains)

    The settings corresponding to the selected subdomain display.

1. If you want to select the landing page subdomain as the tracking URL, check the **[!UICONTROL Same as landing page subdomain]** option. [Learn more on tracking](../design/message-tracking.md)

    ![](assets/lp_preset-subdomain-settings-same.png)

    For example, if the landing page URL is 'pages.mail.luma.com', and the tracking URL is 'data.mail.luma.com', you can choose 'pages.mail.luma.com' to be used as the tracking subdomain.

1. Click **[!UICONTROL Submit]** to confirm the landing page preset creation. You can also save the preset as draft and resume its configuration later on.

   ![](assets/lp_preset-subdomain-settings-submit.png)

1. Once the landing page preset has been created, it displays in the list with the **[!UICONTROL Active]** status. It is ready to be used for your landing pages.

    ![](assets/lp-preset-active-temp.png)

You are now ready to [create landing pages](../landing-pages/create-lp.md) in [!DNL Journey Optimizer].
<!--
>[!NOTE]
>
>Learn how to create channel surfaces for push notifications and emails in [this section](message-presets.md).-->

**Related topics**:

* [Get started with landing pages](../landing-pages/get-started-lp.md)
* [Create a landing page](../landing-pages/create-lp.md#create-a-lp)

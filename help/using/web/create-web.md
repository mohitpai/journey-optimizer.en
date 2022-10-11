---
title: Author a web page
description: Learn how to author a web page and edit its content in Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner

---
# Create web experiences {#create-web}

[!DNL Journey Optimizer] allows you to personalize the web experience you deliver to your customers through inbound web campaigns.

To be able to access and author web pages in the [!DNL Journey Optimizer] user interface, follow the prerequisites below:

* To add modifications to your website, you need to implement the [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html){target="_blank"} on your website.

* To access the [!DNL Journey Optimizer] web designer, you must download the [Adobe Experience Cloud Visual Editing Helper](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target="_blank"} browser extension on Chrome.

>[!CAUTION]
>
>Google Chrome is currently the only browser that supports authoring web pages in [!DNL Journey Optimizer].

<!--Add link to Target??-->

## Create a web campaign {#create-web-campaign}

To start building your web experience through a campaign, follow the steps below.

>[!CAUTION]
>
>Currently in [!DNL Journey Optimizer] you can only create web experiences using **campaigns**.

1. Create a campaign. [Learn more](../campaigns/create-campaign.md)

1. Select the **[!UICONTROL Web]** action.

    ![](assets/web-create-campaign.png)

1. Define a web surface.

    >[!NOTE]
    >
    >A web surface is a web property identified by a URL where the content will be delivered. It can match a single page URL or multiple pages, allowing you to deliver modifications across one or several web pages.

    You can either enter a **[!UICONTROL Page URL]** if you want to apply the changes to a single page only.

    ![](assets/web-campaign-surface.png)
    
1. Or you can build a **[!UICONTROL Pages matching rule]** to target multiple URLs matching the same rule - for example, if you want to apply the changes to a hero banner accross a whole website or add a top image that displays on all the product pages of a website.

    To do so, select **[!UICONTROL Pages matching rule]** and click **[!UICONTROL Create rule]**.

    ![](assets/web-campaign-matching-rule.png)

1. Define your criteria for the **[!UICONTROL Domain]** and **[!UICONTROL Page]** fields.

    For example, if you want to edit elements that are displayed on all the women product pages of your Luma website, select **[!UICONTROL Domain]** > **[!UICONTROL Starts with]** > `luma` and **[!UICONTROL Page]** > **[!UICONTROL Contains]** > `women`.

    ![](assets/web-pages-matching-rule.png)

1. Save your changes. The rule is displayed in the **[!UICONTROL Create campaign]** screen.

    ![](assets/web-pages-matching-rule-example.png)

1. Once you defined the web surface, select **[!UICONTROL Create]**. You can now configure your campaign properties and settings.

## Configure the web campaign {#configure-web-campaign}

1. In the **[!UICONTROL Properties]** tab, you can edit the campaign name and add a description if needed.

    ![](assets/web-campaign-properties.png)

1. Select **[!UICONTROL Content experiment]** to test content treatments with parts of the audience, in order to determine which treatment performs best with respect to a specific metric. [Learn more](../campaigns/content-experiment.md)

    >[!AVAILABILITY]
    >
    >The **Content Experiment** feature is currently only available for a set of organizations (Limited Availability). For more information, contact your Adobe representative.

1. To assign custom or core data usage labels to the web campaign, select the **[!UICONTROL Manage access]** button on top of the screen. [Learn more on Object Level Access Control (OLAC)](../administration/object-based-access.md)

1. From the **[!UICONTROL Action]** tab of the campaign, select **[!UICONTROL Edit content]** to start authoring your web campaign. [Learn more]

    ![](assets/web-edit-content.png)

1. Define the web campaign audience. By default, the web campaign will be visible to all visitors, or to a specific audience that you can select here.

    ![](assets/web-campaign-audience.png)

    >[!NOTE]
    >
    >Learn more on namespaces in the [Adobe Experience Platform documentation](https://experienceleague.adobe.com/docs/experience-platform/identity/namespaces.html){target="_blank"}.


1. Define a schedule for your web campaign. By default, it starts when manually activated and ends when manually stopped, but you can also define specific dates and times.

    ![](assets/web-campaign-schedule.png)

## Test the web campaign {#test-web-campaign}

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

>[!NOTE]
>
>If your content includes contextual data, it may not be rendered in the preview. You can execute the campaign using API to run end-to-end tests with contextual data. <!--To check with email designer / personalization sections? Link?-->

## Activate the web campaign {#activate-web-campaign}

1. Once you edited your content as desired using the web designer, go back to the web campaign.

1. Select **[!UICONTROL Review to activate]**.

    ![](assets/web-designer-review.png)

1. Review and dit the properties, audience and schedule if needed.

1. Select **[!UICONTROL Activate]**.

## Stop a web campaign

1. Select the campaign.

1. From the top menu, select **[!UICONTROL Stop campaign]**.

1. The modifications you added will not be visible anymore to the audience you defined.


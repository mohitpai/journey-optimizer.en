---
solution: Journey Optimizer
product: journey optimizer
title: Configure web subdomains
description: Learn how to set up web subdomains with Journey Optimizer
role: Admin
level: Intermediate
hide: yes
hidefromtoc: yes
keywords: web, subdomains, configuration
badge: label="Beta" type="Informative"

---
# Configure web subdomains {#web-subdomains}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_web_header"
>title="Delegate a web subdomain"
>abstract="You will be setting up your subdomain for web channel use. You can use a subdomain that is already delegated to Adobe or configure another subdomain."

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_web"
>title="Delegate a web subdomain"
>abstract="You must configure a subdomain to use for your web experiences, as you will need this subdomain to create a web surface. You can use a subdomain already delegated to Adobe or configure a new subdomain."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/web/xxx" text="Create web surfaces"

>[!CONTEXTUALHELP]
>id="ajo_admin_config_web_subdomain"
>title="Select a web subdomain"
>abstract="To be able to create a web surface, make sure you have previously configured at least one web subdomain to pick from the Subdomain name list."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/web/xxx" text="Create web surfaces"

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_web_default"
>title="Set a default subdomain"
>abstract="You can create several web subdomains, but only the default subdomain will be used. You can change the one that is used by default, but only one can be used at a time."

>[!BEGINSHADEBOX]

What you'll find in this documentation:

* [Get started with web channel](get-started-web.md)
* [Prerequisites](web-prerequisites.md)
* [Create web experiences](create-web.md)
* [Author web pages](author-web.md)
* **[Configure web subdomains](web-subdomains.md)**
* [Web reporting](web-report.md)

>[!ENDSHADEBOX]

When authoring web experiences, if you add content coming from the [Adobe Experience Manager Assets Essentials](../email/assets-essentials.md) library, you  must set up the subdomain that will be used to publish this content.
<!-->
>[!NOTE]
>Before using [!DNL Adobe Experience Manager Assets Essentials], you must add users to the **Assets Essentials Consumer Users** or/and **Assets Essentials Users** Product profiles, or you must deploy [!DNL Adobe Experience Manager Assets Essentials] for your organization. Learn more in the [Deploy Assets Essentials](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/deploy-administer.html){target="_blank"} section.-->

You can use a subdomain that is already delegated to Adobe, or you can configure another subdomain. Learn more on delegating subdomains to Adobe in [this section](../configuration/delegate-subdomain.md).

>[!CAUTION]
>
>Web subdomain configuration is common to all environments. Therefore:
>
>* To access and edit web subdomains, you must have the **[!UICONTROL Manage Web Subdomains<!--???-->]** permission on the production sandbox.
>
> * Any modification to a web subdomain will also impact the production sandboxes.

You can create several web subdomains, but only the **default** subdomain will be used. You can change the one that is used by default, but only one can be used at a time.

## Set up a web subdomain

1. Access the **[!UICONTROL Administration]** > **[!UICONTROL Channels]** menu, then select **[!UICONTROL Web configuration]** > **[!UICONTROL Web subdomains]**.

    ![](assets/web_access-subdomains.png)

1. Click **[!UICONTROL Set up subdomain]**.

    ![](assets/web_set-up-subdomain.png)

1. From the **[!UICONTROL Configuration type]** section, choose if you want to [use a subdomain already delegated to Adobe](#web-use-existing-subdomain) or [add your own domain](#web-configure-new-subdomain).

1. To set this subdomain as default, select the corresponding option.

    >[!NOTE]
    >
    >You can create several web subdomains, but only the **default** subdomain will be used. You can change the one that is used by default, but only one can be used at a time.

1. Click **[!UICONTROL Submit]**.

1. Once submitted, the subdomain displays in the list with the **[!UICONTROL Processing]** status. For more on subdomains' statuses, refer to [this section](../configuration/about-subdomain-delegation.md#access-delegated-subdomains).

    >[!NOTE]
    >
    >Before being able to use that subdomain for your web experiences, you must wait until Adobe performs the required checks, which can take up to 4 hours.<!--Learn more in [this section](delegate-subdomain.md#subdomain-validation).-->

1. Once the checks are successful, the subdomain gets the **[!UICONTROL Success]** status. It is ready to be used to create web channel surfaces.

1. The Default badge is displayed next the subdomain that is currently used as default. You can change the default subdomain, but only a subdomain with the **[!UICONTROL Success]** status can be set as default.

1. You can delete a subdomain > under what conditions?

## Use an existing subdomain {#web-use-existing-subdomain}

To use a subdomain that is already delegated to Adobe, follow the steps below.

1. Select **[!UICONTROL Use delegated subdomain]** from the **[!UICONTROL Configuration type]** section.

    ![](assets/web_use-delegated-subdomain.png)

1. Enter the prefix that will display in your web URL.

    >[!NOTE]
    >
    >Only alpha-numeric characters and hyphens are allowed.

1. Select a delegated subdomain from the list.

    >[!NOTE]
    >
    >You cannot select a subdomain that is already used as web subdomain.
    
    <!--Capital letters are not allowed in subdomains. TBC by PM-->

    ![](assets/web_prefix-and-subdomain.png)

    <!--Note that you cannot use multiple delegated subdomains of the same parent domain. For example, if 'marketing1.yourcompany.com' is already delegated to Adobe for your web messages, you will not be able to use 'marketing2.yourcompany.com'. However, multi-level subdomains being supported for web, you may proceed using a subdomain of 'marketing1.yourcompany.com' (such as 'email.marketing1.yourcompany.com'), or a different parent domain.-->

    >[!CAUTION]
    >
    >If you select a domain that was delegated to Adobe using the [CNAME method](../configuration/delegate-subdomain.md#cname-subdomain-delegation), you must create the DNS record on your hosting platform. To generate the DNS record, the process is the same as when you configure a new web subdomain. Learn how in [this section](#web-configure-new-subdomain).

## Configure a new subdomain {#web-configure-new-subdomain}

>[!CONTEXTUALHELP]
>id="ajo_admin_web_subdomain_dns"
>title="Generate the matching DNS record"
>abstract="To configure a new web subdomain, you need to copy the Adobe nameserver information displayed in the Journey Optimizer interface and paste it into your domain-hosting solution to generate the matching DNS record. Once the checks are successful, the subdomain is ready to be used to create web surfaces."

To configure a new subdomain, follow the steps below.

1. Select **[!UICONTROL Add your own domain]** from the **[!UICONTROL Configuration type]** section.

    ![](assets/web_add-your-own-subdomain.png)

1. Specify the subdomain to delegate.

    >[!CAUTION]
    >
    >You cannot use an existing web subdomain.
    >
    >Capital letters are not allowed in subdomains.
    
    Delegating an invalid subdomain to Adobe is not allowed. Make sure you enter a valid subdomain which is owned by your organization, such as marketing.yourcompany.com.
    
    >[!NOTE]
    >
    >Multi-level subdomains (of the same parent domain) are supported. For example, you can use 'web.marketing.yourcompany.com'.

1. The record to be placed in your DNS servers displays. Copy this record, or download a CSV file, then navigate to your domain-hosting solution to generate the matching DNS record.

1. Make sure that DNS record has been generated into your domain-hosting solution. If everything is configured properly, check the box "I confirm...", then click **[!UICONTROL Submit]**.

    ![](assets/web_add-your-own-subdomain-confirm.png)

    >[!NOTE]
    >
    >When you configure a new web subdomain, it will always point to a CNAME record.

    Note that the subdomain will be marked as **[!UICONTROL Failed]** if you fail to create the validation record on your hosting solution.


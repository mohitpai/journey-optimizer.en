---
title: Manage opt-out
description: Learn how to manage opt-out and privacy
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: c5bae757-a109-45f8-bf8d-182044a73cca
---
# Manage opt-out {#consent}

Use [!DNL Journey Optimizer] to track your recipients' consent for communication and understand how they want to engage with your brand by managing their preferences and subscriptions.

Regulations such as GDPR state that you must comply with specific requirements before being able to use information from Data Subjects. Moreover, Data Subjects should be able to modify their consent at any time.

**Why is it important?**

* Failing to comply with these regulations introduces regulatory legal risks for your brand.
* It helps you avoid sending unsolicited communications to your recipients, which could make them mark your messages as spam and harm your reputation.

Learn more on managing Privacy and the applicable regulations in the [Experience Platform documentation](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html){target="_blank"}.

## Opt-out management {#opt-out-management}

Providing the capability to recipients to unsubscribe from receiving communications from a brand is a legal requirement. Learn more about the applicable legislation in the [Experience Platform documentation](https://experienceleague.adobe.com/docs/experience-platform/privacy/regulations/overview.html#regulations){target="_blank"}.

Therefore, you must always include an **unsubscribe link** in every email sent out to recipients:

* Upon clicking this link, the recipients will be directed to a landing page including a button to confirm opting out.
* Upon clicking the opt-out button, an Adobe I/O call will be made to update the profile data with this information. [Learn more about this](#consent-service-api).

### Add an unsubscribe link {#add-unsubscribe-link}

To add an unsubscribe link, follow the steps below:

1. Build your unsubscription landing page.

1. Host it on the third-party system of your choice.

1. [Create a message](create-message.md) in [!DNL Journey Optimizer].

1. Select text in your content and insert a link using the contextual toolbar.

    ![](assets/opt-out-insert-link.png)

1. Select **[!UICONTROL Unsubscription link]** from the **[!UICONTROL Link type]** drop-down list.

    ![](assets/opt-out-link-type.png)

1. In the **[!UICONTROL Link]** field, paste the link to your landing page.

    ![](assets/opt-out-link-url.png)

1. Click **[!UICONTROL Save]**.

1. Save your content and [publish your message](publish-manage-message.md).

    >[!NOTE]
    >
    >Your third-party landing page URL will include three parameters that will be used to update the profiles' preferences through an Adobe I/O call.​ [Learn more in this section](#consent-service-api).

1. Send your message with the link to your landing page through a [journey](../building-journeys/journey.md).

1. Once the message is received, if the recipient clicks the unsubscribe link, your landing page is displayed.

    ![](assets/opt-out-lp-example.png)

1. If the recipient clicks the opt-out button in the landing page (here, the **Unsubscribe** button), the profile data is updated through an [Adobe I/O call](#opt-out-api).

    The opted-out recipient is then redirected to a confirmation message screen indicating that opting out was successful.

    ![](assets/opt-out-confirmation-example.png)

    As a result, this user will not receive communication from your brand unless subscribed again.

To check that the corresponding profile's choice has been updated, go to Experience Platform and access the profile by selecting an identity namespace and a corresponding identity value. Learn more in the [Experience Platform documentation](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html#getting-started){target="_blank"}.

![](assets/opt-out-profile-choice.png)

In the **[!UICONTROL Attributes]** tab, you can see the value for **[!UICONTROL choice]** has changed to **[!UICONTROL no]**.

### Opt-out API call {#opt-out-api}

Once the recipient has opted out by clicking the unsubscribe link, an Adobe I/O API is called to update the corresponding profile's preference.

This Adobe I/O POST call is as follows:

Endpoint: platform.adobe.io/journey/imp/consent/preferences

Query parameters:

* **params**: contains the encrypted payload
* **sig**: signature
* **pid**: encrypted profile ID

These parameters are available from the unsubscribe link sent to your recipient, i.e. the URL that will open your third-party landing page for a given recipient:

![](assets/opt-out-parameters.png)

Header requirements:

* x-api-key
* x-gw-ims-org-id
* x-sandbox-name 
* authorization (user token from your technical account)

Request body:

```
{
   "marketing": [
       {
            "type": "email",           
            "choice": "no",          
            "scope": "channel"       
        }
    ],
 
}
```

[!DNL Journey Optimizer] will use these parameters to update the corresponding profile's choice.

## One-click opt-out {#one-click-opt-out}

As many customers look for an easier process to unsubscribe, you can also add a one-click opt-out link into your email content. This link will enable your recipients to quickly unsubscribe from your communications, without being redirected to a landing page where they need to confirm opting out.

Learn how to add an opt-out link to your message content in [this section](message-tracking.md#one-click-opt-out-link).

Once your message is sent through a [journey](../building-journeys/journey.md), if a recipient clicks the opt-out link, their profile is immediately opted out.

## Unsubscribe link in header {#unsubscribe-email}

If the recipients' email client supports displaying an unsubscribe link in the email header, emails sent with [!DNL Journey Optimizer] automatically include this link.

For example, the unsubscribe link will display like this in Gmail:

![](assets/unsubscribe-email.png)

Depending on the email client, clicking the unsubscribe link from the header will have one of the following impacts:

* The corresponding profile is immediately opted out and this choice is updated in Experience Platform. Learn more in the [Experience Platform documentation](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html#getting-started){target="_blank"}.

* It has the same effect as clicking the unsubscribe link from the email content: the recipient is redirected to a landing page including a button to confirm opting out. Learn more on opt-out management in [this section](#opt-out-management).

## Push opt-out management {#push-opt-out-management}

Push recipients can unsubscribe through their devices themselves.

For example, upon downloading or when using your app, they can select to stop notifications. Similarly, they can change the notification settings through the mobile operating system.

---
solution: Journey Optimizer
product: journey optimizer
title: SMS opt-out management
description: Learn how to manage opt-out with SMS messages
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 59ea67d9-e90c-4ad0-afb9-d0e0fd868855
---
# SMS opt-out management {#sms-opt-out}

In accordance with the industry standards and regulations, all SMS marketing messages must contain a way for the recipients to easily unsubscribe. [Learn more on privacy & opt-out management](../privacy/opt-out.md)

By default, Adobe Journey Optimizer handles standard English-language reply messages such as STOP, UNSTOP, and START for Toll-Free and Long Code messages, in accordance with industry standards for native integration such as Sinch and Twilio. These keywords typically trigger an automatic standard reply from your 3rd party provider (e.g. Twilio, Sinch, etc.). You can confirm this directly with your provider or via their documentation site. 

No steps are required to ensure that SMS opt-out capabilities are working in Adobe Journey Optimizer as the keyword responses STOP, UNSTOP, and START will be automatically recognized.

In addition to Adobe Journey Optimizer stopping the send based on the opt-out status (for direct integrations with Twilio or Sinch), most SMS gateway providers also maintain a block list ensuring you that an SMS message will not be delivered to an individual who has chosen to opt out. If you are using a provider other than Sinch or Twilio and sending an SMS via [custom channel](../building-journeys/using-custom-actions.md), you need to confirm this with your provider. 

>[!IMPORTANT]
>
>Text message campaigns may be subject to various legal compliance requirements depending on the nature of your text messaging campaign, the location from where you are sending your text messages, and the location of your recipients. <br>While Adobe Journey Optimizer will handle the messages on long codes and toll-free numbers as detailed above, you should consult your legal counsel to ensure that your text messaging campaign conforms to all applicable legal compliance requirements.

## Short Codes {#short-codes}

By default, Adobe Journey Optimizer will not handle opt-out, opt-in or help keywords for short code numbers.

You must ensure that your short code is compliant to all industry rules and regulations for opt-out handling.

## Alphanumeric Sender ID {#alphanumeric}

Alphanumeric Sender IDs are for one-way messaging only, and are unable to receive inbound messages. As a result, Adobe Journey Optimizer’s SMS STOP, START, HELP keywords are not applicable for Alpha Sender IDs. You must provide other instructions, such as writing to the Support team, calling a Support phone line, or texting another phone number or code to allow users to opt out from messages sent via Alphanumeric Sender ID.

## Video {#video-sms}

To learn more on how native inbound keyword support (START, STOP and UNSTOP) works for SMS, refer to the following video:

>[!VIDEO](https://video.tv.adobe.com/v/344026?quality=12)

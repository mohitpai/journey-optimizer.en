---
solution: Journey Optimizer
product: journey optimizer
title: Manage opt-out
description: Learn how to manage opt-out and privacy
feature: Journeys
topic: Content Management
role: User
level: Intermediate

---
# Implement consent for opt-out for personalization {#cpes-opt-out}


## Expression Editor

Expressions Editor while personalizing images, text, subject line  ( Segment in Campaigns) - UI and Headless 

Personalization editor itself does not perform any consent checks or enforcement as it is not involved in the delivery of message actions. Personalization editor adheres to rights based acces control labels provided by unified profile service to allow/disallow different fields to be used for personalization. Message preview and render service will mask identified fields with sensitive information. 

In AJO Campaigns, the enforcement of consent policy can happen in two places. Customers can include consent policy definitions as part of the audience or segment creation to ensure that the audience selected for the campaign has already filtered out profiles that do not match the consent criteria. Secondarily, message runtime service will perform a general consent check at the channel level to ensure that profiles have opted-in to receive marketing communications on the specific channel. The AJO Campaign object itself does not perform any additional consent policy enforcement checks at this time. 

AJO Campaign and Personalization steps for manually enforcing consent:

A user's opt-in status and personalization preferences should be part of the audience rules and definition before activation in a Journey Optimizer Campaign. A marketing user in Adobe Experience Platform can add a consent check to their audience by creating a new audience composition or by defining a new segment using rule builder.

If using audience composer, you can split your audience using profile attributes. Once you have made your selections on the appropriate consent attributes you wish to check, you can save the resulting audiences for activation in a Campaign. Keep in mind that if you create an audience that has not given consent for personalization and you then select this audience for activation in a Campaign, personalization tools will remain available. It is up to the marketing user to understand that if they are working with an audience that should not receive personalization, that they should not use personalization tools.

To create a split audience in audience composition follow these steps:

1. Select your starting audience.

1. Click the plus icon to create a split audience.

1. In the Split properties choose "attribute split" as the type.

1. In the attribute field click the pencil icon to bring up the attribute selection window.

1. Type in Choice value to search for the personalization consent attribute (note this will be the attribute path profile.consents.personalize.content.val

1. Select this attribute.

1. In Path 1 - choose a label to help you define the non-personalized audience.

1. Choose the appropriate value from this list: https://experienceleague.adobe.com/docs/experience-platform/xdm/data-types/consents.html?lang=en#choice-values

    In this case we will use a "n" to signify NO as the opt-out for personalization

    You can create a separate path for other choice values or you can choose to delete remaining paths and turn on "other profiles" which would include all other profiles that did not have a choice value of "n".

1. Once finished, click in the box where it says "Save Audience". A new properties window will open up allowing you to choose what name you want to use for the derived audiences.

1. Once finished, publish the audience composition.

If using the segment rule builder to create your audience you can select personalization and consent value choices as exclusion parameters in the audience definition. By adding in the exclusion parameters you can create a single audience segment of profiles where individuals that have not given consent are filtered out.


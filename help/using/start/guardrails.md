---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer guardrails and limitations
description: Learn more about Journey Optimizer guardrails
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 5d59f21c-f76e-45a9-a839-55816e39758a
---
# Guardrails and limitations {#limitations}

Entitlements, product limitations and performance guardrails are listed in [Adobe Journey Optimizer product description page](https://helpx.adobe.com/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}.

You also need to be aware of [Guardrails for Real-time Customer Profile data before starting](https://experienceleague.adobe.com/docs/experience-platform/profile/guardrails.html){target="_blank"}.

You will find below additional guardrails and limitations when using [!DNL Adobe Journey Optimizer].

## Supported browsers {#browsers}

Adobe [!DNL Journey Optimizer] interface is designed to work optimally in the latest version of Google Chrome. You might have trouble using certain features on older versions or other browsers.

## Message guardrails {#message-guardrails}

* You cannot add attachments to an email with [!DNL Journey Optimizer].
* You cannot use the same sending domain to send out messages from [!DNL Adobe Journey Optimizer] and from another product, such as [!DNL Adobe Campaign] or [!DNL Adobe Marketo Engage] for example.


## Landing pages guardrails {#lp-guardrails}

* Only one **Form** component can be used in a single primary page.
* The **Form** component cannot be used in subpages.
* You cannot add a preheader to a landing page.
* You cannot select the **Code your own** option when designing a landing primary page.

## Journey guardrails {#journeys-guardrails}

### General journey guardrails {#journeys-guardrails-journeys}

* The number of activities in a journey is limited to 50. The number of activities is displayed on the upper left section of the journey canvas. This will help in readability, QA and troubleshooting. 
* As you publish journeys, we automatically scale and adjust to ensure maximum throughput and stability. As you near the milestone of 100 live journeys at one time, you will see a notification appear in the UI on this achievement. If you see this notification and have a need to extend your journeys beyond 100 live journeys at a time, please create a ticket for customer care and we will help you reach your goals. 

### General actions {#general-actions-g}

* There is no sending throttling.
* Three retries are systematically performed in case of an error. You cannot adjust the number of retries according to the error message received. Retries are performed for all HTTP errors except for HTTP 401, 403 and 404.
* The built-in **Reaction** event allows you to react to out-of-the-box actions. Learn more in [this page](../building-journeys/reaction-events.md). If you want to react to a message sent via a custom action, you need to configure a dedicated event.
* You cannot place two actions in parallel, you must add them one after the other.
* A profile cannot be present multiple times in the same journey, at the same time. If re-entrance is enabled, a profile can reenter a journey, but cannot do it until he fully exited that previous instance of the journey. [Read more](../building-journeys/end-journey.md)

### Journey versions {#journey-versions-g}

* A journey starting with an event activity in v1 cannot start with something else than an event in further versions. You cannot start a journey with a **Audience Qualification** event. 
* A journey starting with a **Audience Qualification** activity in v1 must always start with a **Audience Qualification** in further versions. 
* The audience and namespace chosen in **Audience Qualification** (first node) cannot be changed in new versions.
* The re-entrance rule must be the same in all journey versions.
* A journey starting with a **Read Audience** cannot start with another event in next versions.
* You cannot create a new version of a read audience journey with incremental read. You need to duplicate the journey.

### Custom actions {#custom-actions-g}

* The custom action URL does not support dynamic parameters.
* Only POST and PUT call methods are supported
* The name of the query parameter or header must not start with "." or "$"
* IP addresses are not allowed
* Internal Adobe addresses (`.adobe.*`) are not allowed in URLs and APIs.
* Built-in custom actions cannot be removed.

### Events {#events-g}

* For system-generated events, streaming data used to initiate a customer journey must be configured within Journey Optimizer first to get a unique orchestration ID. This orchestration ID must be appended to the streaming payload coming into Adobe Experience Platform. This limitation does not apply to rule-based events.
* Business events cannot be used in conjunction with unitary events or audience qualification activities.
* Unitary journeys (starting with an event or an audience qualification) include a guardrail that prevents journeys from being erroneously triggered multiple times for the same event. Profile re-entrance is temporally blocked by default for 5 minutes. For instance, if an event triggers a journey at 12:01 for a specific profile and another one arrives at 12:03 (whether it is the same event or a different one triggering the same journey) that journey will not start again for this profile.
* Journey Optimizer requires events to be streamed to Data Collection Core Service (DCCS) to be able to trigger a journey. Events ingested in batch or events from internal Journey Optimizer datasets (Message Feedback, Email Tracking, etc.) cannot be used to trigger a journey. For use cases where you cannot get streamed events, please build an audience based on those events and use the **Read Audience** activity instead. Audience qualification can technically be used, but can cause downstream challenges based on the actions used.

### Data sources {#data-sources-g}

* External data sources can be leveraged within a customer journey to lookup external data in real time. These sources must be usable via REST API, support JSON and be able to handle the volume of requests.
* Internal Adobe addresses (`.adobe.*`) are not allowed in URLs and APIs.

### Journeys and profile creation {#journeys-limitation-profile-creation}
 
There is a delay associated to API based profile creation/update in Adobe Experience Platform. The Service Level Target (SLT) in terms of latency is < 1 min from ingestion to Unified Profile for 95th percentile of requests, at a volume of 20K Requests per second (RPS).

If a journey is triggered simultaneously to a profile creation and immediately checks/retrieves information from Profile Service, it might not work properly.

You can choose from one of these two solutions:

* Add a wait activity after the first event, to give Adobe Experience Platform the time it needs to perform the ingestion to Profile Service.

* Set up a journey that does not immediately leverage the profile. For example, if the journey is designed to confirm an account creation, the experience event could contain information needed to send the first confirmation message (first name, last name, email address, etc.). 

### Read audience {#read-segment-g}

* Streamed audiences are always up-to-date but batch audiences will not be calculated at retrieval time. They are only evaluated every day at the daily batch evaluation time.
* For journeys using a Read Audience activity, there is a maximum number of journeys that can start at the exact same time. Retries will be performed by the system but please avoid having more than five journeys (with Read Audience, scheduled or starting "as soon as possible") starting at the exact same time by spreading them over time, for example 5 to 10 minutes apart.

### Expression editor {#expression-editor}

* Experience event field groups can not be used in journeys starting with a Read audience, an Audience qualification or a business event activity. You need to create a new audience and use an inaudience condition in the journey.


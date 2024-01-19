---
solution: Journey Optimizer
product: journey optimizer
title: DMARC record
description: Learn how to set DMARC record in Journey Optimizer
feature: Subdomains, Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: subdomain, domain, mail, dmarc, record
hide: yes
hidefromtoc: yes

---
# DMARC record important update{#dmarc-record}


>[!CAUTION]
>
>Following on the recent Gmail and Yahoo announcements for bulk senders, Journey Optimizer now supports the DMARC authentication technology.

As part of their enforcing industry best practices, Google and Yahoo will both be requiring that you have a DMARC record for any domain you use to send email to them. This new requirement is starting on **February 1st, 2024**.

Learn more on Google and Yahoo's requirements for DMARC record in [this section](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/guidance-around-changes-to-google-and-yahoo.html?lang=en#dmarc%3A){target="_blank"}.

Learn more on the announced changes at Google and Yahoo on [this page](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/guidance-around-changes-to-google-and-yahoo.html?lang=en#dmarc%3A){target="_blank"}.

Next you wtill have an action or next steps for you section which will state:

You have to set it up for all your subdomains
* If you have fully delegated the domain to us, then you have two options
    * Set up DMARC on parent domain of the delegated domain in your hosting solution, OR
    * Set up DMARC on delegated domain using our upcoming feature in admin UI with no extra work on hosting solution
* If you have set up CNAME for your sending domains, then you have two options
    * Set up DMARC on subdomain OR parent domain of the subdomain in your hosting solution, OR
    * Setup DMARC using our upcoming feature in admin UI. However, it will require not just our UI but also entry in hosting solution.

More details on our upcoming feature come soon.

In addition, you may include the impact if not set by copying the section relevant for DMARC  from below section (copied from link above). Now, either we pull out just DMARC related things. Or here you may educate that announcement is for DMARC and one click unsub and here is the latest on timelines for both features.

Updates to timelines have been forthcoming since the original announcement in October. 

The most recent timelines look like:

Gmail:

* February 2024 – Temporary bounces designed to provide warning of non-compliance will begin. Emails will still be delivered as normal after a short delay if you are not yet in compliance. If you are fully in compliance there will be no temporary bounces and you won't notice a thing.
* April 2024 – Blocks will begin for senders who are not in compliance with everything except List-Unsubscribe 1-Click. Only a portion of non-compliant email will be blocked at first, with the % blocked increasing over time.
* June 1st, 2024 – Any sender not in full compliance, including List-Unsubscribe 1-Click, will experience blocking.

Yahoo:

Has not provided exact dates, but has said "the rollout of enforcement will begin in February 2024. Enforcement will be gradually rolled out".

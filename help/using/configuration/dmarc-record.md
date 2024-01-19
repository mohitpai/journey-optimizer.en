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

---
# DMARC record {#dmarc-record}

>[!CONTEXTUALHELP]
>id="ajo_admin_dmarc_record"
>title="Set the DMARC record"
>abstract="Set DMARC record to avoid deliverability issues with ISPs"

>[!CAUTION]
>
>Following on the recent Gmail and Yahoo announcements for bulk senders, Journey Optimizer now supports the DMARC authentication technology. //You must update all the subdomains you already created on your instance to include DMARC support.//

It's important to do it by February 1st
Doc will come soon

Starting on 

You have 2 options:

* Do it as of now on your own: set it up with your IT department - whenever you want

* Do it in AJO - but in that case you need to wait until Jan 30

    * Full delegation: you can do it on Jan 30 (AJO release)

    * CNAME plan it with your IT department so it's not time-consuming but you need to plan it

As part of their enforcing industry best practices, Google and Yahoo will both be requiring that you have a DMARC record for any domain you use to send email to them. This new requirement is starting on **February 1st, 2024**.

Learn more on Google and Yahoo's requirements for DMARC record in [this section](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/guidance-around-changes-to-google-and-yahoo.html?lang=en#dmarc%3A){target="_blank"}.

Learn more on the announced changes at Google and Yahoo on [this page](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/guidance-around-changes-to-google-and-yahoo.html?lang=en#dmarc%3A){target="_blank"}.

DMARC, which stands for **Domain-based Message Authentication, Reporting, and Conformance**, is an email authentication protocol that helps protect against email spoofing, phishing, and other fraudulent activities.

* Email authentication:

    * SPF (Sender Policy Framework): DMARC relies on SPF to authenticate the sending mail server's identity. SPF helps verify that the email message comes from an authorized source by checking the sending server's IP address against a list of authorized IP addresses for the domain.
    * DKIM (DomainKeys Identified Mail): DMARC also uses DKIM to add a digital signature to email messages, allowing the recipient to verify the message's integrity and authenticity.

* DMARC helps prevent malicious actors from sending emails that appear to come from your domain. By setting up DMARC, you can specify how email providers should handle messages that fail authentication checks, reducing the likelihood that phishing emails will reach recipients.

* DMARC helps improve email deliverability by providing a clear policy for email providers to follow when encountering messages claiming to be from your domain. This can reduce the chances of legitimate emails being marked as spam or rejected.

* By implementing DMARC, you can protect your brand reputation by ensuring that unauthorized parties cannot abuse your domain for phishing or other malicious activities. This is particularly important for businesses and organizations that rely on email communication with customers and partners.

Setting up a DMARC record involves adding a DNS TXT record to your domain's DNS settings. This record specifies your DMARC policy, such as whether to quarantine or reject messages that fail authentication. Implementing DMARC is a proactive step towards enhancing email security and protecting both your organization and your recipients from email-based threats.

[Learn more on DMARC in the Deliverability Best Practice Guide](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/technotes/implement-dmarc.html){target="_blank"} to better understand the impact of DMARC on email deliverability.

If you don't add DMARC, you will be put in quarantine (at least).

please ensure that you have a genuine inbox where you can receive in your control - you manage this inbox (shouldn't be Adobe inbox)

Recommendation is 24 because generally
if less, evaluate your capacity / check your > chat GPT

Google and Yahoo, and probably all other main ISPs

for CNAME in the edition flow you need to Download the CSV file again (not for fully delegated)

new DMARC record

In RN > put it first
All subdomains must be updated with DMARC support




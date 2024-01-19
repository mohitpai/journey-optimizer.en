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
>abstract="Set DMARC record to avoid deliverability issues with ISPs. As part of their enforcing industry best practices, Google and Yahoo are both requiring that you have a DMARC record for any domain you use to send email to them."

>[!CAUTION]
>
>Following on the recent Gmail and Yahoo announcements for bulk senders, Journey Optimizer now supports the DMARC authentication technology.

<!--TO ADD TO AJO HOME PAGE (first tab)

>[!TAB Mandatory DMARC update]

As part of their enforcing industry best practices, Google and Yahoo will both be requiring that you have a DMARC record for any domain you use to send email to them, starting on **February 1st, 2024**. Make sure that you have DMARC record set up for all the subdomains that you have delegated to Adobe in Journey Optimizer.

[![image](using/assets/do-not-localize/learn-more-button.svg)](using/configuration/dmarc-record-update.md)
-->

As part of their enforcing industry best practices, Google and Yahoo will both be requiring that you have a **DMARC record** for any domain you use to send email to them. This new requirement is starting on **February 1st, 2024**.

Learn more on Google and Yahoo's requirement in [this section](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/guidance-around-changes-to-google-and-yahoo.html?lang=en#dmarc%3A){target="_blank"}.

>[!CAUTION]
>
>Failing to comply with this new requirement from Gmail and Yahoo is expected to result in emails landing into the spam folder or getting blocked.

Consequently, Adobe strongly recommends you ensure that you have DMARC record set up for all the subdomains that you have delegated to Adobe in [!DNL Journey Optimizer]. Follow either one of the two options below:

* Set up DMARC on your subdomains, or on the parent domain of your subdomains, **in your hosting solution**.

* Set up DMARC on your delegated subdomains **using the new feature in the [!DNL Journey Optimizer] administration UI** - with no extra work on your hosting solution. [Learn more](#implement-dmarc)

    >[!CAUTION]
    >
    >If you have set up [CNAME delegation](delegate-subdomain.md#cname-subdomain-delegation) for your sending subdomains, it will also require some entry into your hosting solution. Make sure you coordinate with your IT department so that they can perform the update as soon as the [!DNL Journey Optimizer] feature is available (on January 30, 2024). <!--and be ready on February 1st, 2024-->

>[!NOTE]
>
>Learn more on implementing DMARC in the [Deliverability Best Practice Guide](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/technotes/implement-dmarc.html#about){target="_blank"} to better understand the impact on email deliverability.

## What is DMARC?

DMARC, which stands for **Domain-based Message Authentication, Reporting, and Conformance**, is an email authentication protocol that helps protect against email spoofing, phishing, and other fraudulent activities.

* Email authentication:

    * SPF (Sender Policy Framework): DMARC relies on SPF to authenticate the sending mail server's identity. SPF helps verify that the email message comes from an authorized source by checking the sending server's IP address against a list of authorized IP addresses for the domain.
    * DKIM (DomainKeys Identified Mail): DMARC also uses DKIM to add a digital signature to email messages, allowing the recipient to verify the message's integrity and authenticity.

* DMARC helps prevent malicious actors from sending emails that appear to come from your domain. By setting up DMARC, you can specify how email providers should handle messages that fail authentication checks, reducing the likelihood that phishing emails will reach recipients.

* DMARC helps improve email deliverability by providing a clear policy for email providers to follow when encountering messages claiming to be from your domain. This can reduce the chances of legitimate emails being marked as spam or rejected.

* By implementing DMARC, you can protect your brand reputation by ensuring that unauthorized parties cannot abuse your domain for phishing or other malicious activities. This is particularly important for businesses and organizations that rely on email communication with customers and partners.

Setting up a DMARC record involves adding a DNS TXT record to your domain's DNS settings. This record specifies your DMARC policy, such as whether to quarantine or reject messages that fail authentication. Implementing DMARC is a proactive step towards enhancing email security and protecting both your organization and your recipients from email-based threats.

## Implement DMARC {#implement-dmarc}

* If you don't add DMARC, you will be put in quarantine (at least).

* Ensure that you have a genuine inbox where you can receive in your control - you manage this inbox (shouldn't be Adobe inbox)

Recommendation is 24 because generally this is what ISPs have.
if less, evaluate your capacity / check your > chat GPT

If a DMARC record is detected, you can copy-paste the same values as listed or change them if needed.

If you put nothing, default values will be used.

### Fully delegated subdomains

### Subdomains delegated using CNAME

for CNAME in the edition flow you need to download the CSV file again (not for fully delegated)






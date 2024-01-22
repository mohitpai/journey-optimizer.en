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

Consequently, Adobe strongly recommends you ensure that you have DMARC record set up for all the subdomains that you have delegated to Adobe in [!DNL Journey Optimizer]. Follow the steps below that apply to your case:

* If you have [fully delegated](delegate-subdomain.md#full-subdomain-delegation) your sending subdomains to Adobe, follow either one of the two options below:

    * Set up DMARC on the parent domain of your delegated subdomains **in your hosting solution**.

    * Set up DMARC on your delegated subdomains **using the upcoming feature in the [!DNL Journey Optimizer] administration UI** - with no extra work on your hosting solution.

* If you have set up [CNAME delegation](delegate-subdomain.md#cname-subdomain-delegation) for your sending subdomains, follow either one of the two options below:

    * Set up DMARC on your subdomains or on the parent domain of your subdomains **in your hosting solution**.

    * Set up DMARC on your delegated subdomains **using the upcoming feature in the [!DNL Journey Optimizer] administration UI**. However, it will also require entry in your hosting solution. Consequently, make sure you coordinate with your IT department so that they can perform the update as soon as the [!DNL Journey Optimizer] feature is available (on January, 30). <!--and be ready on February 1st, 2024-->
    
**More details on the [!DNL Journey Optimizer] DMARC upcoming feature will come soon.**

>[!NOTE]
>
>Learn more on implementing DMARC in the [Deliverability Best Practice Guide](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/technotes/implement-dmarc.html#about){target="_blank"} to better understand the impact on email deliverability.

## What is DMARC?

DMARC, which stands for **Domain-based Message Authentication, Reporting, and Conformance**, is an email authentication method/protocol that allows domain owners the ability to protect their domain from unauthorized use. 

Offering a way to authenticate the sender's domain,  it helps prevent malicious actors from sending emails that appear to come from your domain.

DMARC also provides feedback on email authentication status and allows senders to control what happens to emails that fail authentication. This includes options to monitor, quarantine or reject mail depending on which DMARC policy has been implemented.

<!--Setting up a DMARC record involves adding a DNS TXT record to your domain's DNS settings. This record specifies your DMARC policy, such as whether to quarantine or reject messages that fail authentication. Implementing DMARC is a proactive step towards enhancing email security and protecting both your organization and your recipients from email-based threats.-->

DMARC has three policy options:

* Monitor (p=none): Instructs the mailbox provider/ISP to do whatever they would normally do to the message.
* Quarantine (p=quarantine): Instructs the mailbox provider/ISP to deliver mail that does not pass DMARC to the recipient's spam or junk folder.
* Reject (p=reject): Instructs the mailbox provider/ISP to block mail that does not pass DMARC resulting in a bounce.

## How does DMARC work?

SPF and DKIM are both used to associate an email with a domain and work together to authenticate email. DMARC takes this one step further and helps to prevent spoofing by matching the domain checked by DKIM and SPF. To pass DMARC, a message must pass SPF or DKIM. If both of these fail authentication, DMARC will fail, and the email will be delivered according to your selected DMARC policy.

* SPF (Sender Policy Framework): DMARC relies on SPF to authenticate the sending mail server's identity. SPF helps verify that the email message comes from an authorized source by checking the sending server's IP address against a list of authorized IP addresses for the domain.
* DKIM (DomainKeys Identified Mail): DMARC also uses DKIM to add a digital signature to email messages, allowing the recipient to verify the message's integrity and authenticity.

>[!NOTE]
>
>DMARC requires alignment between the 'From" and 'Return-Path' address.


<!--

* DMARC helps prevent malicious actors from sending emails that appear to come from your domain. By setting up DMARC, you can specify how email providers should handle messages that fail authentication checks, reducing the likelihood that phishing emails will reach recipients.

* DMARC helps improve email deliverability by providing a clear policy for email providers to follow when encountering messages claiming to be from your domain. This can reduce the chances of legitimate emails being marked as spam or rejected.

DMARC helps protect against email spoofing, phishing, and other fraudulent activities.

It allows you to decide how a mailbox provider should handle emails that fail SPF and DKIM checks, providing a way to authenticate the sender's domain and prevent unauthorized use of the domain for malicious purposes.

-->


## Implement DMARC {#implement-dmarc}

To implement DMARC, follow the steps below that apply to your case.

* If you don't add DMARC, you will be put in quarantine (at least).

### Fully delegated subdomains

Set the action that the recipient server will perform if DMARC fails.

DMARC has three policy options:

* Monitor (p=none): Instructs the mailbox provider/ISP to do whatever they would normally do to the message. This is the default value.
* Quarantine (p=quarantine): Instructs the mailbox provider/ISP to deliver mail that does not pass DMARC to the recipient's spam or junk folder.
* Reject (p=reject): Instructs the mailbox provider/ISP to block mail that does not pass DMARC resulting in a bounce.

Emails to receive aggregate DMARC reports and forensic DMARC failure reports: you can add up to 5 addresses.

* Ensure that you have a genuine inbox where you can receive in your control - you manage this inbox (shouldn't be Adobe inbox)

Applicable percentage of emails to apply DMARC: 

Reporting interval: Recommendation is 24 because generally this is what ISPs have.
if less, evaluate your capacity / check your > chat GPT

If a DMARC record is detected, you can copy-paste the same values as listed or change them if needed.

If you put nothing, default values will be used.

### Subdomains delegated using CNAME

for CNAME in the edition flow you need to download the CSV file again (not for fully delegated)






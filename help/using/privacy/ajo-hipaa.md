---
title: Journey Optimizer and HIPAA compliance
description: Learn about HIPAA compliance with Journey Optimizer
feature: Privacy
role: User
level: Intermediate
---
# Journey Optimizer and HIPAA compliance {#ajo-hipaa}

Adobe Journey Optimizer enables compliance with the the Health Insurance Portability and Accountability Act (HIPAA). This legislation governs the use of electronic medical records, and includes provisions to protect the security and privacy of personally identifiable health-related data, called Protected Health Information (PHI). Adobe Journey Optimizer services are HIPAA-compliant which means these capabilities can enable you to use our solutions in a way that you can meet your obligations under HIPAA regulations.

Ultimately companies are responsible for ensuring their compliance with their legal obligations, that Adobe solutions meet their compliance needs, and that they secure the solutions in an appropriate way. 

>[!CAUTION]
>
>Some of the HIPAA readiness capabilities listed below are available through a specific Healthcare Shield add-on offering.
>This add-on is a HIPAA-ready offering built on Adobe Experience Cloud applications which empower healthcare brands and companies.
> 

HIPAA readiness capabilities in Journey Optimizer cover:

* **Permissions** -  Journey Optimizer supports defining user roles and access policies to manage permissions for features and objects. Through **Adobe Experience Cloud Permissions**, you can create and manage roles, as well as assign the desired resource permissions for these roles. Permissions also allow you to manage the labels, sandboxes, and users associated with a specific role.

* **Data Access Control** - Through attribute-based access control, administrators can control access to specific objects based on certain attributes. These attributes can be metadata added to an object, such as labels. Administrators can also define user roles that have access to only specific fields and/or objects, and data that correspond to those fields and/or objects.

* **Data Governance** - With its Data Usage Labelling and Enforcement (DULE) governance framework, Journey Optimizer lets you define labels to restrict sensitive fields from being transfered to an external system through a custom action in a journey. 

* **Audit Controls** - With Journey Optimizer, you can identify actions performed by users in the system on various services and capabilities like campaigns, journeys, messages, landing pages etc. This allows you to increase the visibility of activities performed in the system, troubleshoot issues, and help your business comply with regulations and corporate data stewardship policies. Audit log resources include changes on attribute-based access control, and are recorded automatically as the activity occurs. Learn more [in this page](audit-logs.md).

* **Archiving** - Journey Optimizer provides BCC capabilities to archive emails. For SMS, you need to work with your SMS partner (Twilio or Sinch) to archive your messages. In addition, Journey Optimizer now comes with a new capability to export your message templates, and archive the format and the structure of the message, without personal data.

* **Data encryption** - All datasets used for input/output of models will follow Adobe Experience Platform guidelines. Platform Data Encryption applies for data at-rest and in-transit. Learn more in [Adobe Experience Platform documentation](https://experienceleague.adobe.com/docs/experience-platform/landing/governance-privacy-security/encryption.html?lang=en){_blank}

* **Automated Consent Enforcement** - Adobe Experience Platform allows you to easily adopt and enforce marketing policies to respect the consent preferences of your customers. Consent policies are defined in Adobe Experience Platform. In Journey Optimizer, you can apply these consent policies to your custom actions. For example you can define consent policies to exclude customers who have not consented to receive email, push or SMS communication. Learn more [in this page](../action/consent.md).
    *CAUTION*:  Automated Consent Enforcement is currently only available for organizations that have purchased the Healthcare Shield add-on offering.

* **Data hygiene** - Experience Platform provides a suite of data hygiene capabilities that allow you manage your stored data through programmatic deletions of consumer records and datasets. This capability is now available for Adobe Journey Optimizer. You can manage your data stores to ensure that information is used as expected, is updated when incorrect data needs fixing, and is deleted when organizational policies deem it necessary.
    *CAUTION*:  Data Hygiene capabilities are currently only available for organizations that have purchased the Healthcare Shield add-on offering.


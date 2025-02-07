---
description: Learn about browser support and get common questions answered for administrators in the Adobe Experience Cloud.
keywords: core services, Experience Cloud, Experience Platform, Analytics, Target, user management.
solution: Experience Cloud
title: Frequently asked questions about Experience Cloud 
index: yes
feature: Admin Console
topic: Administration
role: Administrator
level: Experienced
exl-id: 062576da-328e-4b46-9e71-5a25733d607a
---
# Frequently asked questions about Experience Cloud

Learn about browser support and common questions and answers for administrators in the Experience Cloud.

## What browsers are supported in Experience Cloud?

* Microsoft Edge (current and back two versions)
* Google Chrome (current and back two versions)
* Mozilla Firefox (current and back two versions)
* Safari (current and back two versions)
* Opera (current and back two versions)

## How do I know if my solutions are enabled for core services?

If your implementation has not been provisioned for core services, see [Enable your solutions for core services](../core-services/core-services.md#concept_07ED1D5C64234E77976E6D572E78FB9C), which describes how to: 

1. [Join the Experience Cloud and become an administrator](../core-services/core-services.md#section_2423F0BD3DF642658103310EE5EA6154)
1. [Implement the Experience Cloud ID Service using Experience Platform Launch](https://docs.adobe.com/content/help/en/launch/using/intro/get-started/quick-start.html).
1. [Map Report Suites to an Experience Cloud Organization](../core-services/core-services.md#concept_apg_zq2_rw)
1. [(Analytics only) Modernize Your Analytics AppMeasurement Code](../core-services/core-services.md#section_1798D9D0F05C47E29816AC4EEB9A0913)
1. [(Adobe Target only) Modernize Your Adobe Target Implementation](../core-services/core-services.md#section_C2F4493C7A36406DAE2266B429A4BD24)
1. [Verify the implementation](../core-services/core-services.md#section_E641782A0F4F44AF8C9C91216BE330D5)
1. [Manage users and products](../core-services/core-services.md#section_B6E95F4E0E12483CB9DA99CBC0C5A4AF)
1. [Start using core services](../core-services/core-services.md#section_960C06093623462E8EA247B3E97274A1)

For more assistance, [Contact Adobe Support](https://helpx.adobe.com/marketing-cloud/contact-support.html).

## Does Adobe charge my company for Experience Cloud access?

No. The Experience Cloud is included at no additional charge. However, certain core services might have additional costs.

## Why does my company need to log in through the Experience Cloud interface?

The functionality provided by the Experience Cloud interface adds new value to your business. It also will be the standard path for accessing solutions going forward, eventually replacing other individual solution login flows. Logging in through the Experience Cloud will facilitate a smoother transition later.

## How do I resolve concerns about migrating my company?

[Contact Adobe Support](https://helpx.adobe.com/marketing-cloud/contact-support.html). 

## What is _provisioning?_

Provisioning in the Experience Cloud means:

* Your users can begin logging in to the [!DNL Experience Cloud] and linking solutions.
* They can begin to use the features available through the Experience Cloud, such as People.
* You can become prepared to retire your solution-specific login process.
* You can retain access control to solutions.

## How do I manage users and product profiles?

* See the [Admin Console User Guide](https://helpx.adobe.com/enterprise/administering/user-guide.html) for help.

* User entitlements and product management is performed in the [Adobe Admin Console](https://adminconsole.adobe.com/enterprise) (product link).

* **Important:** Analytics administrators, see [Manage Analytics Users in the Admin Console](https://docs.adobe.com/content/help/en/analytics/admin/user-product-management/user-management/migrate-users/c-migration-tool.html) about migrating user IDs from Analytics Admin Tools to the Admin Console. 

## What do I do if someone cannot log in to the Experience Cloud?

Admin Console administrators can grant access to users. Users are sent emails with sign-in instructions. 

You might need to [Contact Adobe Support](https://helpx.adobe.com/marketing-cloud/contact-support.html) to verify that your company has been fully provisioned.

## Where can a user go to manage account linking?

Some users might need to link their solution (Analytics) account to the Adobe ID or Enterprise ID. 

See [Link a solution account to an Adobe ID](../admin-getting-started/organizations.md#task_FD389E78640848919E247AC5E95B8369). 

## How do I manage user account profiles and organizations?

See [Manage user accounts](../admin-getting-started/organizations.md#topic_C31CB834F109465A82ED57FF0563B3F1). 

## What is an organization?

An *organization* is the entity that enables an administrator to configure groups and users, and to control single sign-on in the Experience Cloud. The organization functions like a log-in company that spans all the Experience Cloud products and solutions. Most often, an organization is your company name. However, a company can have many organizations. 

## Where can I find my IMS Organization ID?

See [Finding your Organization ID](organizations.md). 

The Organization ID is displayed on the Experience Cloud landing page and the [Admin Console landing page](https://adminconsole.adobe.com). 

Alternatively, administrators can log into the Admin console (Navigate to [https://adminconsole.adobe.com](https://adminconsole.adobe.com#)) for a specific organization, and you will be able to see your IMS org ID in the URL. 

For example, in the following URL: 

`https://adminconsole.adobe.com/C538193582390300A495CC9@AdobeOrg/overview` 

the ID is: 

`C538193582390300A495CC9@AdobeOrg`

## What should I do when one of my users leaves my company?

Their access should be removed from the solution itself. They will not be able to access the product from the Experience Cloud or through the direct login. You should also remove them at the Experience Cloud level.

## What is an Adobe ID?

See [Identity Types](https://helpx.adobe.com/enterprise/help/identity.html).

## Can I link solution accounts for my users?

No. Users must link their own solutions with their user names and passwords.

## Why do I see Social when my company does not have it?

Adobe Social is a product that can be sold with Analytics. Therefore, if you have Analytics you will see this solution, but you will not have access unless you have purchased it.

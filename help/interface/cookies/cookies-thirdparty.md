---
description: Learn about how support for third-party cookies has become increasingly limited across browsers.
keywords: cookies;privacy
solution: Experience Cloud,Analytics,Target
title: How changes to third-party cookie support impacts customers 
uuid: 27332e0d-6932-4a6e-b97b-0adeced0b050
feature: Cookies
topic: Administration
role: Administrator
level: Experienced
exl-id: 3d12a1b1-c952-4b42-815d-f64b31429cec
---
# How changes to third-party cookie support impact customers{#how-changes-to-third-party-cookie-support-impacts-customers}

As the support for third-party cookies has become more and more limited across browsers, Adobe has been working on new solutions that carefully balance customer requirements with the consumer's right to privacy across the Adobe Experience Cloud solutions.

The following list outlines how third-party cookie support impacts current implementations of the Adobe Experience Cloud solutions:

## Adobe Analytics and Adobe Target

* Customers with a [first-party implementation](/help/interface/cookies/cookies-first-party.md) would remain largely unaffected. 
* Customers that are not using first-party implementation can implement the [Experience Platform ID Service](https://docs.adobe.com/content/help/en/id-service/using/implementation/implementation-guides.html) to store the ID cookie as a first-party cookie without a first-party implementation.

## Adobe Experience Manager

* Because Adobe Experience Manager operates wholly within the customer's domain, there is minimal interaction with third-party cookies and thus minimal to no impact.

## Adobe Social

* Social would not be impacted as long as the customer has the newest ver­sion of the code.

## Adobe Advertising Cloud

* Search:

  * Where search is optimized based on Adobe Analytics data, search would be impacted in the same way as Adobe Analytics.
  * Collection of conversion data should be unaffected.

* Display:

  * Display remarketing today is entirely dependent upon the usage of third-party cookies.
  * Display is also heavily dependent on the availability of various advertising network cookies for synchronization.
  * Overall impact is unknown. However, per the first point, display is affected more than other services.
  * We are working internally and with our advertising partners to evaluate the full extent to the impact on ad delivery.

* Social:

  * There is no impact to Facebook market­place ads.
  * Facebook Exchange (FBX) will be affected the same as display ad delivery.

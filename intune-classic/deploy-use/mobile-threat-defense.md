---
# required metadata

title: Intune Mobile threat defense 
description: Protect access to company resources based on device risk.
keywords:
author: andredm7
ms.author: andredm
manager: angrobe
ms.date: 03/01/2017
ms.topic: article
ms.prod:
ms.service: microsoft-intune
ms.technology:
ms.assetid: 08d87906-8158-4d5e-a49d-ad919efef3d1
ROBOTS: NOINDEX,NOFOLLOW

# optional metadata

#audience:
#ms.devlang:
ms.reviewer: heenamac
ms.suite: ems
#ms.tgt_pltfrm:
ms.custom: intune-classic

---

# Intune Mobile Threat Defense connectors

[!INCLUDE[classic-portal](../includes/classic-portal.md)]

Intune Mobile Threat Defense connectors allow you to leverage your chosen Mobile Threat Defense vendor as a source of information for your compliance policies and conditional access rules. This allows IT Administrators to add a layer of protection to their corporate resources such as Exchange and Sharepoint, specifically from compromised mobile devices.

## What problem does this solve?

Companies need to protect sensitive data from emerging threats including physical, app-based, and network-based threats, as well as operating system vulnerabilities.
Historically, companies have been proactive when protecting PCs from attack, while mobile devices go un-monitored and unprotected. Mobile platforms have built-in protection such as app isolation and vetted consumer app stores, but these platforms remain vulnerable to sophisticated attacks. Today, more employees use devices for work and need access to sensitive information. Devices need to be protected from increasingly sophisticated attacks.

## How the Intune Mobile Threat Defense connectors work?

The connector protects company resources by creating a channel of communication between Intune and your chosen Mobile Threat Defense vendor. Intune Mobile Threat Defense partners offer intuitive, easy to deploy applications for mobile devices which actively scan and analyze threat information to share with Intune, for either reporting or enforcement purposes. For example, if a connected Mobile Threat Defense app reports to the Mobile Threat Defense vendor that a phone on your network is currently connected to a network which is vulnerable to Man in the Middle attacks, this information is shared with and categorized to an appropriate risk level (low/medium/high) – which can then be compared with your configured risk level allowances in Intune to determine if access to certain resources of your choice should be revoked while the device is compromised.

## Sample scenarios

When a device is considered infected by the Mobile Threat Defense solution:

![Mobile Threat Defense infected device](../media/mtp/MTD-image-1.png)

Access is granted when the device is remediated:

![Mobile Threat Defense Access granted](../media/mtp/MTD-image-2.png)

## Mobile Threat Defense partners

Learn how to protect access to company resource based on device, network, and application risk with:

- [Lookout](/intune-classic/deploy-use/lookout-mobile-threat-defense-connector)
- [Skycure](/intune-classic/deploy-use/skycure-mobile-threat-defense-connector)

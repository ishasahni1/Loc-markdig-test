---
# required metadata

title: Configure app protection policies during an Intune migration
description: This article provides the necessary steps to set up app protection policies during an Intune migration.
keywords:
author: andredm7
ms.author: andredm
manager: angrobe
ms.date: 07/12/2017
ms.topic: article
ms.prod:
ms.service: microsoft-intune
ms.technology:
ms.assetid: 93cda587-bf56-4d41-b123-9fe203fad788

# optional metadata

#ROBOTS:
#audience:
#ms.devlang:
ms.reviewer: dagerrit
ms.suite: ems
#ms.tgt_pltfrm:
#ms.custom:

---

# Configure app protection policies (optional)


App protection policies allow you to:
* Encrypt apps
* Define a PIN when the app is accessed
* Block apps from running on jail-broken or rooted devices, and many other protections.

If the user's phone is lost or stolen, you can selectively wipe the corporate data remotely while leaving the personal data intact.

App protection policies apply security at the app level and do not require device enrollment. You can use them with devices enrolled into Intune or not. Additionally, you can apply them to devices enrolled into a third-party MDM provider.

## App protection policies with LOB apps

You can also extend the mobile app protection policies to your line-of-business (LOB) apps by using the [Microsoft Intune App SDK](app-sdk-get-started.md) or the Microsoft Intune App Wrapping Tool for both [IOS](https://www.microsoft.com/download/details.aspx?id=45218&751be11f-ede8-5a0c-058c-2ee190a24fa6=True) and [Android](https://www.microsoft.com/download/details.aspx?id=47267) platforms.

## How do app protection policies help during migration?

In a migration, you must remove devices from the old MDM provider and enroll them into Intune. You should plan for this and encourage your end-users to leave the old MDM provider and immediately enroll into Intune. However, during the migration there may be users who delay completing the enrollment process and whose devices are not managed by either MDM provider.

This period can leave your organization more vulnerable to device theft and corporate data loss if corporate resource access is still allowed. It may also lead to lower user productivity if corporate resource access is blocked.

Intune can offer corporate data protections during the migration so you can still have security coverage for your corporate data when there’s no device-level management.

As you disable conditional access in the old MDM provider, users can still be productive while you on-board them into Intune.

## Task list for app protection policies

1. [Create an app protection policy](app-protection-policies.md#create-an-app-protection-policy)
2. [Deploy a policy](app-protection-policies.md#deploy-a-policy-to-users)


## Next steps

[Special migration considerations](migration-guide-considerations.md)

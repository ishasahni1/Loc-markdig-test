---
# required metadata

title: Getting started with policies
titlesuffix: "Azure portal"
description: Create policies to prevent users from doing unauthorized things with their devices.
keywords:
author: arob98
ms.author: angrobe
manager: angrobe
ms.date: 10/31/2017
ms.topic: article
ms.prod:
ms.service: microsoft-intune
ms.technology:
ms.assetid: 1ac74ba5-7441-44ac-98b5-9d8bb8899747


# optional metadata

#ROBOTS:
#audience:
#ms.devlang:
ms.reviewer:
ms.suite: ems
#ms.tgt_pltfrm:
ms.custom: intune-azure
---

# Get started with policies

One of the main goals of getting started with Intune is enrolling devices to make sure that they are compliant with corporate policies. Compliance policies not only help you to manage specialized device types, such as corporate-owned kiosks, but also personal (Bring Your Own) devices, tablets, and user-less devices.

![Compliance dashboard with very little data](/intune/media/generic-compliance-dashboard.png)

Compliance policies provide the following management capabilities for mobile devices:

* Regulate numbers of devices each user enrolls
* Manage devices settings (e.g. device-level encryption, password length, camera usage)
* Deliver apps, email profiles, VPN profiles, etc.
* Evaluate device-level criteria for security compliance policies

You create compliance policies for each platform separately. For this exercise, we’ll stick to iOS. The following policies are available for iOS devices:

* PIN or password configuration
* Device encryption
* Jailbroken device
* Email profile
* Minimum OS version
* Maximum OS version

__How do I create a policy?__

1. Sign in to the [Azure portal](https://portal.azure.com).
2. **Search resources**, search for **Intune**.
3. Select **Device compliance**.
4. On the **Device compliance** blade, select **Policies**.
5. Select **Create Policy**, then fill in the details, like **Name** and **Description**. Choose **iOS** as the **Platform**.
6. In **Settings**, select **System Security**, then toggle **Require a password to unlock mobile devices** to **Require**. You can also set other rules, such as **Minimum password length**, **Required password type**, and **Number of non-alphanumeric characters in password**. When you’ve finished setting up your policy, select **OK**.
7. Return to the **Create policy** blade, then select **Create**.
8. Once the policy is created, select **Assignments** to assign it to your test group. Select your test group – which should have your test user in it – then assign the policy to that group by clicking **Save**.
9. Wait a few minutes, then your enrolled device should prompt you that it needs an updated password in order to remain compliant with corporate policy. You can also manually check for this in the **Company Portal app for iOS** by tapping on the device name, then the **Sync** button.

## Next steps

[Get started enrolling devices](get-started-enroll.md) - Learn the enrollment experience by going through a full enrollment experience of an iOS device.

## Learn more

* [Monitor Intune Device compliance policies](compliance-policy-monitor.md)
* [Common ways to use conditional access policies with Intune](conditional-access-intune-common-ways-use.md)

---
# required metadata

title: Set up Intune
description: Requirements and prerequisites for starting to use your Intune subscription
keywords:
author: arob98
ms.author: angrobe
manager: angrobe
ms.date: 10/31/2017
ms.topic: get-started-article
ms.prod:
ms.service: microsoft-intune
ms.technology:
ms.assetid: d158503c-1276-422b-ab81-5f66c1cd7e7a

# optional metadata

#ROBOTS:
#audience:
#ms.devlang:
ms.reviewer: angrobe
ms.suite: ems
#ms.tgt_pltfrm:
ms.custom: intune-classic

---


# Set up Intune

[!INCLUDE [both-portals](./includes/note-for-both-portals.md)]

These set-up steps help you enable mobile device management (MDM). Devices must be managed before you can give users access to company resources or manage settings on those devices.

Some steps, such as setting up an Intune subscription and setting the MDM authority, are required for most scenarios. Other steps, such as configuring a custom domain or adding apps, are optional depending upon your company's needs.

If you're currently using Microsoft System Center Configuration Manager to manage computers and servers, you can [extend Configuration Manager to manage mobile devices](https://docs.microsoft.com/sccm/mdm/understand/choose-between-standalone-intune-and-hybrid-mobile-device-management).

>[!TIP]
>If you purchase at least 150 licenses for Intune in an eligible plan, you can use the *FastTrack Center Benefit*. With this service, Microsoft specialists work with you to get your environment ready for Intune. See [FastTrack Center Benefit for Enterprise Mobility + Security (EMS)](https://docs.microsoft.com/enterprise-mobility-security/Solutions/enterprise-mobility-fasttrack-program).



| Steps |                                                                                                                       Status                                                                                                                       |
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   1   |                                        [Supported configurations](supported-devices-browsers.md) - Need-to-know info before you start. This includes supported configurations and networking requirements.                                         |
|   2   |                                                                 [Sign in to Intune](account-sign-up.md) - Sign in to your trial subscription or create a new Intune subscription.                                                                  |
|   3   |                [Configure domain name](custom-domain-name-configure.md) - Set DNS registration to connect your company's domain name with Intune. This gives users a familiar domain when connecting to Intune and using resources.                |
|   4   |                                   [Add users](users-add.md) - Manually add users or connect Active Directory to sync users with Intune. Required unless your devices are "userless" kiosk devices, for example.                                    |
|   5   |                                            [Assign licenses](licenses-assign.md) - Give users permission to use Intune. Each user or userless device requires an Intune license to access the service.                                             |
|   6   |                                               [Add groups](groups-add.md) - Use user and device groups to simplify management tasks. Groups are used to assign apps, settings, and other resources.                                                |
|   7   |                                                                        [Add apps](apps-add.md) - Apps can be assigned to groups and automatically or optionally installed.                                                                         |
|   8   | [Configure devices](device-profiles.md) - Set up profiles that manage device settings. Device profiles can preconfigure settings for email, VPN, Wi-Fi, and device features. They can also restrict devices to help protect both devices and data. |
|   9   |       [Customize Company Portal](company-portal-app.md) - Customize the Intune Company Portal that users use to enroll devices and install apps. These settings appear in both the Company Portal app and the Intune Company Portal website.       |
|  10   |                                [Enable device enrollment](mdm-authority-set.md) - Enable Intune management of iOS, Windows, Android, and Mac devices by setting the MDM authority and enabling specific platforms.                                 |


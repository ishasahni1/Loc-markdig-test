---
# required metadata

title: Logout the user of an iOS device with Intune 
titlesuffix: "Azure portal"
description: Learn how to log out the current user of an iOS device with Intune."
keywords:
author: arob98
ms.author: angrobe
manager: angrobe
ms.date: 07/13/2017
ms.topic: get-started-article
ms.prod:
ms.service: microsoft-intune
ms.technology:
ms.assetid: 702bc46c-1a6f-4689-bd53-3b778a447baa

# optional metadata

#ROBOTS:
#audience:
#ms.devlang:
#ms.reviewer: ilwu
ms.suite: ems
#ms.tgt_pltfrm:
ms.custom: intune-azure

---

# Logout the current user on Intune-managed iOS devices


[!INCLUDE [azure_portal](./includes/azure_portal.md)]

The **Logout current user** action logs out the current user on a shared iPad device that is configured to manage the iOS Classroom app using an [iOS education profile](education-settings-configure-ios.md). 

## Supported platforms

- Windows - Not supported
- Windows Phone - Not supported
- iOS - Supported on iOS 9.3 and later (shared iPad devices only)
- macOS - Not supported
- Android - Not supported

## How to logout the current user

1.  Sign into the Azure portal.
2.  Choose **More Services** > **Monitoring + Management** > **Intune**.
3.  On the **Intune** blade, choose **Devices**.
4.  On the **Devices and groups** blade, choose **All devices**.
5.  From the list of devices you manage, choose an iOS device, and then choose the **Logout current user** device remote action.

## Next steps

To see the status of the action you just took, on the **Devices and groups** blade, choose **Device Actions**.

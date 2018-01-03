---
# required metadata

title: Create Intune device configuration profiles
titlesuffix: "Azure portal"
description: Learn how to create Intune device configuration profiles."
keywords:
author: arob98
ms.author: angrobe
manager: angrobe
ms.date: 05/16/2017
ms.topic: article
ms.prod:
ms.service: microsoft-intune
ms.technology:
ms.assetid: d98aceff-eb35-4e3e-8e40-5f300e7335cc

# optional metadata

#ROBOTS:
#audience:
#ms.devlang:
ms.reviewer: heenamac
ms.suite: ems
#ms.tgt_pltfrm:
ms.custom: intune-azure

---

# How to create device configuration profiles in Microsoft Intune

[!INCLUDE[azure_portal](./includes/azure_portal.md)]


1. Sign into the Azure portal.
2. Choose **More Services** > **Monitoring + Management** > **Intune**.
3. On the **Intune** blade, choose **Configure devices**.
4. On the **Device Configuration** blade, choose **Manage** > **Profiles**.
5. On the blade showing the list of profiles, choose **Create Profile**.
6. On the **Create Profile** blade, specify the following items:
   - **Name** - Enter a descriptive name for the new profile.
   - **Description** -  Enter an optional description for the profile.
   - **Platform** -  Select the platform type for the profile you want to create.
   - **Profile type** - Select the type of profile you want to create. The list of available types differs depending on the platform you chose.
   - **Settings** - See the following topics for information about the settings for each profile type:
       -  [Device feature settings](device-features-configure.md)
       -  [Device restriction settings](device-restrictions-configure.md)
       -  [Email settings](email-settings-configure.md)
       -  [VPN settings](vpn-settings-configure.md)
       -  [Wi-Fi settings](wi-fi-settings-configure.md)
       -  [Windows 10 edition upgrade settings](edition-upgrade-configure-windows-10.md)
       -  [Certificate settings](certificates-configure.md)
       -  [Windows Information Protection settings](windows-information-protection-configure.md)
       -  [Education settings](education-settings-configure.md)
       -  [Custom settings](custom-settings-configure.md)

     ![Create device profile](./media/create-device-profile.png)
7. Once you are done configuring settings, on the **Create Profile** blade, choose **Create**.

The profile is created and appears on the profiles list blade.
If you want to go ahead and assign this profile to groups, see [How to assign device profiles](device-profile-assign.md).


### Next steps
For information about how to assign device profiles, see [How to assign device profiles with Microsoft Intune](device-profile-assign.md).

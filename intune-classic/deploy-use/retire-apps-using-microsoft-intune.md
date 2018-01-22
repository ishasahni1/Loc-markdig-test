---
# required metadata

title: Retire apps 
description: Learn how to retire or uninstall apps using Intune.
keywords:
author: mattbriggs
ms.author: mabrigg
manager: angrobe
ms.date: 12/27/2016
ms.topic: article
ms.prod:
ms.service: microsoft-intune
ms.technology:
ms.assetid: 6fbf0805-1144-4e08-bafd-4f181d932bf2
ROBOTS: NOINDEX,NOFOLLOW

# optional metadata

#audience:
#ms.devlang:
ms.reviewer: jeffgilb
ms.suite: ems
#ms.tgt_pltfrm:
ms.custom: intune-classic

---

# Retire apps using Microsoft Intune

[!INCLUDE [classic-portal](../includes/classic-portal.md)]

To retire an app, you simply uninstall it. When you deploy and manage apps with Intune, the process for uninstalling the app is the same for both mobile devices and Windows PCs. The app must support the uninstallation process for this procedure to succeed.

## Uninstall an app

1.  In the [Microsoft Intune administration console](https://manage.microsoft.com), choose **Apps** &gt; **Apps**.

2.  Select the app you want to uninstall (one that has been previously deployed), and then choose **Manage Deployment**.

3.  On the **Deployment Action** page, select **Uninstall** from the **Approval** column.

When the device or computer next checks for apps, the app will be uninstalled.

### See also
[Add apps in Microsoft Intune](add-apps.md)

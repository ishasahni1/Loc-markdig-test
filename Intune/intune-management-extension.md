---
# required metadata

title: Manage PowerShell scripts in Intune for Windows 10 devices
titlesuffix: "Azure portal"
description: Learn how to upload PowerShell scripts in Intune to run on Windows 10 devices. 
keywords:
author: dougeby
manager: angrobe
ms.date: 11/08/2017
ms.topic: article
ms.prod:
ms.service: microsoft-intune
ms.technology:
ms.assetid: 768b6f08-3eff-4551-b139-095b3cfd1f89

# optional metadata

#ROBOTS:
#audience:
#ms.devlang:
ms.reviewer:
ms.suite: ems
#ms.tgt_pltfrm:
ms.custom: intune-azure

---

# Manage PowerShell scripts in Intune for Windows 10 devices
The Intune management extension lets you upload PowerShell scripts in Intune to run on Windows 10 devices. The management extension supplements Windows 10 mobile device management (MDM) capabilities and makes it easier for you to move to modern management.

## Moving to modern management
End-user computing is going through a digital transformation. Classic, traditional IT focuses on a single device platform, business-owned devices, users that work from the office, and a variety of manual, reactive IT processes. The modern workplace, however, enables multiple device platforms that are both user and business owned, allow users to work from anywhere, and provide automated and proactive IT processes. 

MDM services, such as Microsoft Intune, can manage Windows 10 devices by using the MDM protocol. The built-in Windows 10 management client is able to communicate with Intune to perform enterprise management tasks. It helps you drive toward modern management on Windows 10 devices. However, there are certain capabilities that you might need, such as advanced device configuration, troubleshooting, and legacy Win32 app management that currently isn't available in Windows 10 MDM. For these capabilities, you might run the Intune software client on your Windows 10 devices. As a result, you are not able to use the new capabilities that Windows 10 MDM provides. [Compare the differences between the Intune software client and Windows 10 MDM](https://docs.microsoft.com/intune-classic/deploy-use/pc-management-comparison).

The Intune management extension supplements the in-box Windows 10 MDM capabilities. You can create PowerShell scripts to run on the Windows 10 devices that provide the capabilities you need. For example, you can create a PowerShell script that installs a legacy Win32 app on your Windows 10 devices, upload the script to Intune, assign the script to an Azure Active Directory (AD) group, and run the script on Windows 10 devices. You can then monitor the run status of the script on Windows 10 devices from start to finish.

## Prerequisites
The Intune management extension has the following prerequisites:
- Devices must be joined to Azure AD
- Devices must run Windows 10, version 1607 or later

## Create a PowerShell script policy 
1. Sign into the [Azure portal](https://portal.azure.com).
2. Choose **More Services** > **Monitoring + Management** > **Intune**.
3. On the **Intune** blade, choose **Device configuration**.
4. On the **Device Configuration** blade, choose **Manage** > **PowerShell scripts**.
5. On the **PowerShell scripts** blade, choose **Add script**.
6. On the **Add PowerShell Script** blade, enter a **Name** and **Description** for the PowerShell script.
7. For **Script location**, browse for the PowerShell script. The script must be less than 10 KB (ASCII) or 5 KB (Unicode).
8. Choose **Configure**, and then choose whether to run the script with the user's credentials on the device (**Yes**) or system context(**No**). By default, the script runs in the system context. Select **Yes** unless the script is required to run in the system context. 
  ![Add PowerShell script blade](./media/mgmt-extension-add-script.png)
9. Choose whether the script must be signed by a trusted publisher (**Yes**). By default, there is no requirement for the script to be signed. 
10. Click **OK** and then click **Create** to save the script.

## Assign a PowerShell script policy
1. Sign into the [Azure portal](https://portal.azure.com).
2. Choose **More Services** > **Monitoring + Management** > **Intune**.
3. On the **Intune** blade, choose **Device configuration**.
4. On the **Device Configuration** blade, choose **Manage** > **PowerShell scripts**.
5. On the **PowerShell scripts** blade, select the script to assign, and then choose **Manage** > **Assignments**.
  ![Add PowerShell script blade](./media/mgmt-extension-assignments.png)
 
6. Choose **Select Groups** to list available Azure AD groups. 
7. Select the groups, and then click **Select** to assign the policy to the selected groups.

The Intune management extension synchronizes to Intune once every hour. After you assign the policy to the Azure AD groups, the PowerShell script is run and the run results are reported. 
 
## Monitor run status for PowerShell scripts
You can monitor the run status of PowerShell scripts for users and devices in the Azure portal.
1. Sign into the [Azure portal](https://portal.azure.com).
2. Choose **More Services** > **Monitoring + Management** > **Intune**.
3. On the **Intune** blade, choose **Device configuration**.
4. On the **Device Configuration** blade, choose **Manage** > **PowerShell scripts**.
5. On the **PowerShell scripts** blade, select the script to monitor, and then choose **Monitor**, and then one of the following reports:
   - **Device status**
   - **User status**

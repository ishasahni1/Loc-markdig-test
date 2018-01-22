---
# required metadata

title: Set up the Check Point SandBlast integration with Intune
titlesuffix: "Azure portal"
description: "Set up the Check Point SandBlast integration with Intune"
keywords:
author: andredm7
ms.author: andredm
manager: angrobe
ms.date: 07/03/2017
ms.topic: article
ms.prod:
ms.service: microsoft-intune
ms.technology:
ms.assetid: 1e9b1576-b239-48cc-a672-da6b5fb7be0a

# optional metadata

#ROBOTS:
#audience:
#ms.devlang:
ms.reviewer: heenamac
ms.suite: ems
#ms.tgt_pltfrm:
ms.custom: intune-azure

---

# Integrate Check Point SandBlast Mobile with Intune

## Before you begin

> [!NOTE] 
> The steps below need to be taken in the [Check Point SandBlast Mobile MTD console](https://intune-4.eu1.locsec.net/).

Before starting the process of integrating Check Point SandBlast Mobile with Intune, make sure you have the following:

-   Microsoft Intune subscription

-   Azure Active Directory admin credentials to grant the following permissions:

    -   Sign in and read user profile

    -   Access the directory as the signed-in user

    -   Read directory data

    -   Send device information to Intune

-   Admin credentials to access Check Point SandBlast Mobile MTD console.

### Check Point SandBlast app authorization

The Check Point SandBlast app authorization process consists of the following:

-   Allow the Check Point SandBlast Mobile service to communicate information related to device health state back to Intune.

-   CheckPoint SandBlast Mobile syncs with Azure AD Enrollment Group membership to populate its device’s database.

-   Allow Check Point SandBlast admin console to use Azure AD Single Sign On (SSO).

-   Allow the Check Point SandBlast Mobile app to sign in using Azure AD SSO.

## To set up Check Point SandBlast Mobile integration

1.  Go to [Check Point SandBlast Mobile MTD console](https://intune-4.eu1.locsec.net/) and sign in with your credentials.

2.  Click on the **Settings** tab.

3.  Choose **Device management**, then **Settings**.

4.  Choose **Microsoft Intune** from the **MDM Service** drop-down list.

5.  Once you set Microsoft Intune as the MDM Service, the **Microsoft Intune Configuration** window pops up, choose the **Add to my organization** for each device platform: iOS, Android and Windows to authorize Check Point SandBlast Mobile to communicate with Intune and Azure AD.

    ![Check Point MTD Intune configuration](./media/checkpoint-MTD-1.PNG)

    > [!IMPORTANT]
    > You must add all device platforms to proceed to the next step.

6.  Choose **Accept** to authorize the Check Point SandBlast Mobile app to communicate with Intune and Azure Active Directory.

7.  Once you enabled all device platforms, you need to enter the Azure AD security group.

8.  Choose **Verify**, once the Azure AD security group is successfully verified, choose **Save**.

## Next steps

- [Set up Check Point SandBlast Mobile apps](mtd-apps-ios-app-configuration-policy-add-assign.md)
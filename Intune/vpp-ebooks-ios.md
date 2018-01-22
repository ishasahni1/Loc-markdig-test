---
# required metadata

title: Manage volume-purchased iOS eBooks
titlesuffix: "Azure portal"
description: Learn about how you can sync books you purchased in volume from the iOS store into Intune and then manage and track their usage."
keywords:
author: mattbriggs
ms.author: mabrigg
manager: angrobe
ms.date: 08/17/2017
ms.topic: article
ms.prod:
ms.service: microsoft-intune
ms.technology:
ms.assetid: f5617074-2384-4812-b913-dc94f64c0818

# optional metadata

#ROBOTS:
#audience:
#ms.devlang:
ms.reviewer: mghadial
ms.suite: ems
#ms.tgt_pltfrm:
ms.custom: intune-azure
---

# How to manage iOS eBooks you purchased through a volume-purchase program with Microsoft Intune


[!INCLUDE [azure_portal](./includes/azure_portal.md)]

The Apple Volume Purchase Program (VPP) lets you purchase multiple licenses for a book that you want to distribute to users in your company. You can distribute books from the Business, or Education stores.

Microsoft Intune helps you synchronize, manage, and assign books that you purchased through this program. You can import license information from the store and track how many of the licenses you have used.

The procedures to manage books are similar to [managing VPP apps](vpp-apps-ios.md).

## Manage volume-purchased books for iOS devices
You buy multiple licenses for iOS books through the [Apple Volume Purchase Program for Business](http://www.apple.com/business/vpp/) or the [Apple Volume Purchase Program for Education](http://volume.itunes.apple.com/us/store). This process involves setting up an Apple VPP account from the Apple website and uploading the Apple VPP token to Intune.  You can then synchronize your volume purchase information with Intune and track your volume-purchased book use.

## Before you start
Before you start, get a VPP token from Apple and upload it to your Intune account. Additionally:

* You can associate up to 256 VPP tokens with your Intune account.
* If you previously used a VPP token with a different product, you must generate a new one to use with Intune.
* Each token is valid for one year.
* By default, Intune syncs with the Apple VPP service twice a day. You can start a manual sync at any time.
* After you have imported the VPP token to Intune, do not import the same token to any other device management solution. Doing so might result in the loss of license assignment and user records.
* Before you start to use iOS books with Intune, remove any existing VPP user accounts created with other mobile device management (MDM) vendors. Intune does not synchronize those user accounts into Intune as a security measure. Intune synchronizes only data from the Apple VPP service that Intune created.
* When you assign a book to a device, that device must have the built-in iBooks app installed. If it is not, the end user must reinstall the app before they can read the book. You cannot currently use Intune to restore removed built-in apps.
* You can only assign books from the Apple Volume Purchase Program site. You cannot upload, then assign books you created in-house.
* You cannot currently assign books to end-user categories in the same way as you do apps.
* You cannot reclaim a license once the book is assigned.
* When a user with an eligible device first tries to install a VPP book, they must join the Apple Volume Purchase program before they can install a book. You can also assign licenses to security groups with managed Apple IDs. If you do this, then users are not prompted for their Apple ID when a book is installed.

## To get and upload an Apple VPP token

1. Sign into the Azure portal.
2. Choose **More Services** > **Monitoring + Management** > **Intune**.
3. On the **Intune** blade, choose **Mobile apps**.
1.  In the **Mobile Apps** workload, choose **Setup** > **iOS VPP Tokens**.
2.  On the list of VPP tokens blade, click **Add**.
3.  On the **New VPP Token** blade, specify the following information:
    - **VPP token file** - Ensure you have signed for the Volume Purchase Program for Business or the Volume Purchase Program for Education. Then, download the Apple VPP token for your account and select it here.
    - **Apple ID** - Enter the Apple ID of the account associated with the volume-purchase program.
    - **Type of VPP account** - Choose from **Business** or **Education**.
4. When you are done, click **Upload**.

The token is displayed in the list of tokens blade.


You can synchronize the data held by Apple with Intune at any time by choosing **Sync now**.

## To assign a volume-purchased app

1. In the **eBooks** workload, choose **Manage** > **All eBooks**.
2. On the list of books blade, choose the book you want to assign, and then choose '**...**' > **Assign Groups**.
3. On the <*book name*> - **Groups Assigned** blade, choose **Manage** > **Groups Assigned**.
4. Choose **Assign Groups** then, on the **Select groups** blade, choose the Azure AD user groups to which you want to assign the book. Device groups are currently not supported.
Choose an assignment action of **Available**, or **Required**. 
5. Once you are done, choose **Save**.

## Next steps

See [How to monitor apps](apps-monitor.md) for information to help you monitor book assignments.







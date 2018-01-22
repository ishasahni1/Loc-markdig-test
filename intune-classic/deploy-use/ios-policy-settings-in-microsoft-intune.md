---
# required metadata

title: iOS policy settings 
description: Create policies that control settings and features on iOS devices that you manage with Intune.
keywords:
author: vhorne
ms.author: victorh
manager: angrobe
ms.date: 11/03/2017
ms.topic: article
ms.prod:
ms.service: microsoft-intune
ms.technology:
ms.assetid: ab46be6c-ab73-4c99-8492-66d1dd418293
ROBOTS: NOINDEX,NOFOLLOW

# optional metadata

#audience:
#ms.devlang:
ms.reviewer: heenamac
ms.suite: ems
#ms.tgt_pltfrm:
ms.custom: intune-classic

---

# iOS policy settings in Microsoft Intune

[!INCLUDE [classic-portal](../includes/classic-portal.md)]

Intune supplies a range of built-in general settings that you can configure on iOS devices. Additionally, you can use the Apple Configurator tool to create custom settings that are not available from Intune.

## General configuration policy settings

Use the Microsoft Intune **iOS general configuration policy** to configure settings for:

-   **General device, and security settings**. Choose from a list of predefined settings that let you control a range of features and functionality on the device.

-   **Kiosk mode**. Lock a device to allow only certain features to work. For example, you can allow a device to run only one managed app that you specify, or you can disable the volume buttons on a device. These settings might be used for a demonstration model of a device, or a device that is dedicated to performing only one function, such as a point-of-sale device.

-   **Compliant and noncompliant apps**. Specify a list of apps that are compliant or not compliant in your company. On Android and iOS devices, the **Noncompliant Apps Report** can be used to view the compliance of apps that you specified in the list against the apps that users have installed (but cannot actually block the installation of the app).

> [!TIP]
> You can configure terms and conditions for users to ensure that they acknowledge that apps on their device (including personal apps) will be evaluated, and noncompliant apps will be either blocked or reported as noncompliant. Users must accept these terms and conditions before they can enroll their device and use the company portal to get apps. For more information about using terms and conditions, see [Terms and conditions policy settings in Microsoft Intune](terms-and-condition-policy-settings-in-microsoft-intune.md).

If the setting you are looking for does not appear in this topic, you might be able to create it by using an iOS custom policy that lets you import settings you created by using the [Apple Configurator tool](https://itunes.apple.com/us/app/apple-configurator/id434433123?mt=12). For more information, see "Custom policy settings" later in this topic.

### Security settings
All settings apply to iOS 8.0 and later.


|                                           Setting name                                            |                                                            Details                                                             |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
|                   <strong>Require a password to unlock mobile devices</strong>                    |                        Specify whether the user is required to enter a password to access their device.                        |
|                              <strong>Required password type</strong>                              |                   Specify the type of password that will be required, such as numeric only or alphanumeric.                    |
|                <strong>Number of complex characters required in password</strong>                 | Specify the number of symbol characters (like <strong>#</strong> or <strong>@</strong>) that must be included in the password. |
|                             <strong>Minimum password length</strong>                              |                                   Specify the minimum number of characters in the password.                                    |
|                              <strong>Allow simple passwords</strong>                              |                          Allow simple passwords like <strong>0000</strong> and <strong>1234</strong>.                          |
|     <strong>Number of repeated sign-in failures to allow before the device is wiped</strong>      |                       Specify the number of failed login attempts before this setting wipes the device.                        |
|          <strong>Minutes of inactivity before password is required</strong><sup>1</sup>           |                   Specify how long the device can remain idle before the user must re-enter their password.                    |
|                            <strong>Password expiration (days)</strong>                            |                             Specify the number of days before the device password must be changed.                             |
|                            <strong>Remember password history</strong>                             |                           Specify whether the user can use passwords that they have previously used.                           |
| <strong>Remember password history</strong> – <strong>Prevent reuse of previous passwords</strong> |                           Specify the number of previously used passwords that the device remembers.                           |
|            <strong>Minutes of inactivity before screen turns off</strong><sup>1</sup>             |                             Specify the number of minutes before the device display is turned off.                             |
|                             <strong>Allow fingerprint unlock</strong>                             |                                        Allow using a fingerprint to unlock the device.                                         |

<sup>1</sup> For iOS devices, when you configure the settings **Minutes of inactivity before screen turns off** and **Minutes of inactivity before password is required**, they are applied in sequence. For example, if you set the value for both settings to **5** minutes, the screen will turn off automatically after 5 minutes, and the device will be locked after an additional 5 minutes. However, if the user turns off the screen manually, the second setting is immediately applied. In the same example, after the user turns off the screen, the device will lock 5 minutes later.

### System settings
All settings apply to iOS 8.0 and later.

|Setting name|Details|
|----------------|-------|
|**Allow screenshot**|Allow the user to capture the contents of the screen as an image.|
|**Allow control center in lock screen**|Allow the user to access the control center app when the device is locked.|
|**Allow notification view in lock screen**|Allow the user to access the notifications view without unlocking the device.|
|**Allow today view in lock screen**|Allow the user to view notifications when the device is locked.|
|**Allow untrusted TLS certificates**|Allow untrusted Transport Layer Security certificates on the device.|
|**Allow diagnostic data submission**|Allow or block the device from submitting diagnostic data to Apple.|
|**Allow passbook while locked**|Allow the user to access the Passbook app while the device is locked.|

### Cloud settings for documents and data
All settings apply to iOS 8.0 and later.

|Setting name|Details|
|----------------|-------|
|**Allow backup to iCloud**|Allow the user to back up the device to iCloud.|
|**Allow document sync to iCloud**|Allow document and key-value synchronization to your iCloud storage space.|
|**Allow Photo Stream sync to iCloud**|Lets users enable **My Photo Stream** on their device which allow photos to sync to iCloud and be available on all the users devices.|
|**Require encrypted backup**|Require any device backups to be encrypted.|
|**Allow managed apps to sync data to iCloud**|Allow apps that you manage with Intune to sync data to the user's iCloud account.|
|**Allow Handoff to continue activities on another device**|Allow the user to continue work that they started on an iOS device on another iOS or Mac OS X device.|
|**Allow iCloud Photo Sharing**|Set to **No** to disable **iCloud Photo Sharing** on the device.|
|**Allow iCloud Photo Library**|If set to **No**, disables the use of iCloud photo library which lets users store photos and videos in the cloud.   Any photos not fully downloaded from iCloud Photo Library to the device will be removed from the device if this is set to **No**.|

### Application settings for the browser
All settings apply to iOS 8.0 and later.

|Setting name|Details|
|----------------|-------|
|**Allow Safari**|Specify whether the Safari browser can be used on the device.|
|**Allow autofill**|Allow the user to change autocomplete settings in the browser.|
|**Allow pop-up blocker**|Enable or disable the browser pop-up blocker.|
|**Allow cookies**|Allow the browser to use cookies.|
|**Allow Java scripting**|Allow Java scripts to run in the browser.|
|**Allow fraud warning**|Allow fraud warnings in the browser.|

### Application settings for apps
All settings apply to iOS 8.0 and later.

|Setting name|Details|
|----------------|-------|
|**Allow installing apps**|Allow the device to access the app store and install apps.|
|**Require a password to access application store**|Require the user to enter a password before they can visit the app store.|
|**Allow in-app purchases**|Allow store purchases to be made from within a running app.|
|**Allow managed documents in other unmanaged apps**|Allow corporate documents to be viewed in any app.<br>**Example:** You want to prevent users from saving files from the OneDrive app to Dropbox. Configure this setting as no. After the device receives the policy (for example, after a restart), it will no longer allow saving.|
|**Allow unmanaged documents in other managed apps**|Allow any document to be viewed in corporate managed apps.|
|**Allow video conferencing**|Allow video conferencing apps such as FaceTime on the device.|
|**Allow the user to trust new enterprise app authors**|Lets the user select to trust apps that were not downloaded from the app store.|


### Application settings for games
All settings apply to iOS 8.0 and later.

|Setting name|Details|
|----------------|-------|
|**Allow adding Game Center friends**|Allow the user to add friends in Game Center.|
|**Allow multiplayer gaming**|Allow the user to play multiplayer games on the device.|

### Application settings for media content
All settings apply to iOS 8.0 and later.

|Setting name|Details|
|----------------|-------|
|**Ratings region**|Select a region, then select the maximum rating that users can download for **Movies**, **TV Shows** and **Apps**.|
|**Allow adult content in media store**|Allow the device to access content rated as adult from the store.|
|**Allow the user to download content from the iBook store flagged as 'Erotica'**|Allow the user to download books with the "Erotica" category.|


### Device capabilities settings for hardware
All settings apply to iOS 8.0 and later.

|Setting name|Details|
|----------------|-------|
|**Allow camera**|Specify whether the camera on the device can be used.|
|**Force paired Apple Watches to use wrist detection**|When enabled, the Apple Watch won't display notifications when it is not being worn.|
|**Require a pairing password for outgoing AirPlay requests**|Require a pairing password when the user uses AirPlay to stream content to other Apple devices.|

### Device capabilities settings for cellular
All settings apply to iOS 8.0 and later.

|Setting name|Details|
|----------------|-------|
|**Allow voice roaming**|Allow voice roaming when the device is on a cellular network.|
|**Allow data roaming**|Allow data roaming when the device is on a cellular network.|
|**Allow global background fetch while roaming**|Allow the device to fetch data such as email while it is roaming on a cellular network.|

### Device capabilities settings for features
All settings apply to iOS 8.0 and later.

|Setting name|Details|
|----------------|-------|
|**Allow Siri**|Allow use of the Siri voice assistant on the device.|
|**Allow Siri while device is locked**|Allow use of the Siri voice assistant on the device while it is locked.|
|**Allow voice dialing**|Allow use of the voice dialing feature on the device.|
|**Do not allow Airdrop from managed apps**|Stops managed apps from being able to send data via. Airdrop.|


### Settings for compliant and noncompliant apps
In the **Compliant &amp; Noncompliant Apps** list, specify a list of compliant or noncompliant apps by using the following information.

> [!NOTE]
> A single policy can contain only a list of compliant apps or a list of noncompliant apps. You cannot specify both in the same policy.

|Setting name|Details|
|----------------|--------------------|
|**Report noncompliance when users install the listed apps**|List the apps (not managed by Intune) that users are not allowed to install and run.|
|**Report noncompliance when users install apps which are not listed**|List the apps that users are allowed to install. To remain compliant, users must not install apps that are not listed. Apps that are managed by Intune are automatically allowed.|
|**Add**|Add an app to the selected list. Specify a name of your choice, optionally the app publisher, and the URL to the app in the app store. Read "How to specify URLs to app stores" later in this topic for more help.|
|**Import Apps**|Import a list of apps you have specified in a comma-separated values file. In the file, use this format: application name, publisher, app URL.|
|**Edit**|Edit the name, publisher, and URL of the selected app.|
|**Delete**|Delete the selected app from the list.|

Policies containing compliant and noncompliant app settings must be deployed to groups of users.

### Kiosk mode settings

|                                            Setting name                                            |                                                                                                                                      Details                                                                                                                                       |
|----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <strong>Select a managed app that will be allowed to run when the device is in kiosk mode</strong> | Choose <strong>Browse</strong>, and then specify the managed app or app from a store that will be allowed to run when the device is in kiosk mode. No other apps will be allowed to run on the device. For more help, see "How to specify URLs to app stores" later in this topic. |
|                                    <strong>Allow touch</strong>                                    |                                                                                                                  Enable or disable the touchscreen on the device.                                                                                                                  |
|                               <strong>Allow screen rotation</strong>                               |                                                                                                Enable or disable changing the screen orientation when the user rotates the device.                                                                                                 |
|                               <strong>Allow volume buttons</strong>                                |                                                                                                           Enable or disable the use of the volume buttons on the device.                                                                                                           |
|                                <strong>Allow ringer switch</strong>                                |                                                                                                             Enable or disable the ringer (mute) switch on the device.                                                                                                              |
|                          <strong>Allow screen sleep wake button</strong>                           |                                                                                                           Enable or disable the screen sleep wake button on the device.                                                                                                            |
|                                  <strong>Allow auto lock</strong>                                  |                                                                                                                 Enable or disable automatic locking of the device.                                                                                                                 |
|                                 <strong>Enable mono audio</strong>                                 |                                                                                                      Enable or disable the accessibility setting <strong>Mono audio</strong>.                                                                                                      |
|                                 <strong>Enable voice over</strong>                                 |                                                                               Enable or disable the accessibility setting <strong>VoiceOver</strong>, which reads aloud text on the device display.                                                                                |
|                           <strong>Enable voice over adjustments</strong>                           |                                                                  Enable or disable voiceover adjustments, which let the user adjust the VoiceOver function (for example, how fast on-screen text is read aloud).                                                                   |
|                                    <strong>Enable zoom</strong>                                    |                                                                         Enable or disable the <strong>Zoom</strong> accessibility setting, which lets the user use touch to zoom in to the device display.                                                                         |
|                              <strong>Enable zoom adjustments</strong>                              |                                                                                                  Enable or disable zoom adjustments, which let the user adjust the zoom function.                                                                                                  |
|                               <strong>Enable invert colors</strong>                                |                                                                    Enable or disable the <strong>Invert Colors</strong> accessibility setting, which adjusts the display to help users with visual impairments.                                                                    |
|                         <strong>Enable invert colors adjustments</strong>                          |                                                                                         Enable or disable invert colors adjustments, which let the user adjust the invert colors function.                                                                                         |
|                              <strong>Enable assistive touch</strong>                               |                                                     Enable or disable the <strong>Assistive Touch</strong> accessibility setting, which helps the user perform on-screen gestures that might be difficult for them to perform.                                                     |
|                        <strong>Enable assistive touch adjustments</strong>                         |                                                                                       Enable or disable assistive touch adjustments, which let the user adjust the assistive touch function.                                                                                       |
|                              <strong>Enable speech selection</strong>                              |                                                                        Enable or disable the <strong>Speak Selection</strong> accessibility settings, which can read aloud the text that the user selects.                                                                         |

> [!NOTE]
> The following notes apply to kiosk mode settings for iOS devices:
>
> -   Before you can configure an iOS device for kiosk mode, you must use the [Apple Configurator tool](https://itunes.apple.com/us/app/apple-configurator/id434433123?mt=12) or the [Apple Device Enrollment Program](ios-device-enrollment-program-in-microsoft-intune.md) to put the device into supervised mode. For more information about the Apple Configurator tool, see your Apple documentation.
> -   If the iOS app that you specify is installed after you deploy the configuration policy, the device will not enter kiosk mode until after it is restarted.

### Reference information for compliant and noncompliant apps

Use the **Noncompliant Apps Report** to view the compliance of allowed and blocked apps.

##### To run the Noncompliant Apps Report

1.  In the [Microsoft Intune administration console](https://manage.microsoft.com), choose **Reports** &gt; **Noncompliant Apps Report**.

2.  Select the device groups that you want to check, select whether you want to check for compliant apps, noncompliant apps, or both, and then choose **View Report**.

#### How to specify URLs to app stores
To specify an app URL in the compliant and noncompliant apps list, or in the **Select a managed app that will be allowed to run when the device is in kiosk mode** option (iOS only), use the following format:

1. Using a search engine, find the app that you want to use in the iTunes App Store and open the page for the app.

2. Copy the URL of the page and use this as the URL to configure the compliant or noncompliant apps list or the app that you want to run in kiosk mode.

**Example:** Search for **Microsoft Word for iPad**. The URL that you use will be **https://itunes.apple.com/us/app/microsoft-word-for-ipad/id586447913?mt=8**.

> [!NOTE]
> You can also use the iTunes software to find the app and then use the **Copy Link** command to get the app URL.

### Enrollment settings
All settings apply to iOS 8.0 and later.

|Setting name|Details|
|----------------|--------------------|
|**Allow Activation Lock when the device is in supervised mode**|Enable Activation Lock on supervised iOS devices.|

### Supervised mode settings
You can configure the following settings on devices running iOS 8.0 and later that are in supervised mode.

### Supervised mode settings for device restrictions

|Setting name|Details|
|----------------|--------------------|
|**Allow account modification**|Allow the user to change account settings such as email configurations.|
|**Allow changes to app cellular data usage settings**|Allow the user to control which apps are allowed to use cellular data.|
|**Allow the use of the erase all content and settings option on the device**|Allow the user to use the option of erasing all content and settings on the device.|
|**Allow the user to enable restrictions in the device settings**|Allow the user to configure device restrictions (parental controls) on the device.|
|**Allow host pairing to control the devices an iOS device can pair with**|Allow host pairing to let the administrator control which devices an iOS device can pair with.|
|**Allow the user to install configuration profiles and certificates**|Allow the user to install configuration profiles and certificates.|
|**Allow device name modification**|Allow the user to change the name of the device.|
|**Allow passcode modification**|Allow the device password to be added, changed, or removed.|
|**Allow Apple Watch pairing**|Allow the device to pair with an Apple Watch.|
|**Allow notification settings modification**|Allow the user to change the device notification settings.|
|**Allow wallpaper modification**|Allow the user to change the device wallpaper.|

### Supervised mode settings for feature restrictions

|Setting name|Details|
|----------------|--------------------|
|**Allow AirDrop**|Allow use of the AirDrop feature to exchange content with nearby devices.|
|**Allow Siri to query user-generated content from the Internet**|Allow Siri to access websites to answer questions.|
|**Use Siri profanity filter**|Prevents Siri from dictating, or speaking profane language.|
|**Allow Spotlight search to return results from the Internet**|Let Spotlight search connect to the Internet to provide further results.|
|**Allow word definition lookup**|Allow the iOS feature that lets you highlight a word and look up it's definition.|
|**Allow predictive keyboards**|Allow the use of predictive keyboards that suggest words the user might want.|
|**Allow auto-correction**|Lets the device automatically correct misspelled words.|
|**Allow keyboard spell-check**|Allows the device spell checker.|
|**Allow keyboard shortcuts**|Allows use of keyboard shortcuts.|

### Supervised mode settings for app restrictions

|Setting name|Details|
|----------------|--------------------|
|**Allow enterprise app trust settings modification**|Lets users change the trust settings for enterprise apps.|
|**Allow installing apps using Apple Configuration and iTunes only**|Enables or disables the App Store from the device home screen. Users can still use iTunes, or the Apple Configurator tool to install and update apps.|
|**Allow automatic app downloads**|Allow apps purchased on other devices to automatically download to this device. This setting does not affect app updates.|
|**Allow changes to the Find My Friends app settings**|Allow the user to change settings for the Find My Friends app.|
|**Allow access to the iBooks store**|Allow the user to browse and purchase books from the iBooks store.|
|**Allow use of the Messages app on the device**|Allow use of the Messages app to send text messages.|
|**Allow use of Podcasts**|Allow use of the Podcasts app.|
|**Allow use of Music service**|Allow use of the Apple Music app.|
|**Allow iTunes Radio service**|Allow use of the iTunes Radio app.|
|**Allow Apple News**|Allow use of the Apple News app.|
|**Allow Game Center**|Allow use of the Game Center app.|


### Show or Hide Apps

Use the **Hidden and shown apps list** to control the following on supervised devices running iOS 9.3 or later:

- Specify a list of apps that will be hidden from users. Users cannot view, or launch these apps.
- Specify a list of apps that users can view and launch. No other apps can be viewed or launched.


#### How to create a hidden or shown app list

Specify the following settings:

|Setting name|Details|
|-|-|
|**Hidden and shown apps list**|Enable this setting if you want to create a hidden, or shown apps list.|
|**Hide the listed apps from users**|Select this option if you want to create a list of apps that will be hidden from users.<br>When you create this list type, all apps except for the iOS **Settings** and **Phone** (for iPhones) apps can be hidden.|
|**Show only the listed apps to users**|Select this option if you want to create a list of apps that are displayed to users.<br>When you create this list type, all other apps except for the iOS **Settings** and **Phone** (for iPhones) apps are hidden.<br>Additionally, you must add the Company Portal, and any apps you have deployed, and manage with Intune to the list.|
|**Add**|Adds an app to the selected list.<br>For the hidden list, you must specify the **Name**, **Publisher**, and **App URL or Bundle ID** of each app you want to hide.<br>For the shown list, you can either **Select a managed app** which gives you a list of apps you manage with Intune to select from, or Select a store app, after which you must specify the **Name**, **Publisher**, and **App URL or Bundle ID** of each app you want to display.|
|**Import Apps**|Imports a list of apps you have specified in a comma-separated values file. Use the format, application name, publisher, app URL in the file.|
|**Edit**|Let’s you edit the name, publisher and URL of the selected app.|
|**Delete**|Deletes the selected app from the list.|

#### App information for built-in iOS apps

Use the information in this list to identify the name, publisher, and bundle ID of the built-in iOS apps that you might want to show or hide. If you want to show or hide all of the apps in the list, you can copy the data below into a text file with the extension **.csv**, then use the **Import Apps** option to import all of the apps simultaneously.

```
,com.apple.AppStore,App Store,Apple
,com.apple.calculator,Calculator,Apple
,com.apple.mobilecal,Calendar,Apple
,com.apple.camera,Camera,Apple
,com.apple.mobiletimer,Clock,Apple
,com.apple.compass,Compass,Apple
,com.apple.MobileAddressBook,Contacts,Apple
,com.apple.facetime,FaceTime,Apple
,com.apple.mobileme.fmf1,Find Friends,Apple
,com.apple.mobileme.fmip1,Find iPhone,Apple
,com.apple.gamecenter,Game Center,Apple
,com.apple.mobilegarageband,GarageBand,Apple
,com.apple.Health,Health,Apple
,com.apple.iBooks,iBooks,Apple
,com.apple.MobileStore,iTunes Store,Apple
,com.apple.itunesu,iTunes U,Apple
,com.apple.Keynote,Keynote,Apple
,com.apple.mobilemail,Mail,Apple
,com.apple.MapsMaps,Apple
,com.apple.MobileSMS,Messages,Apple
,com.apple.Music,Music,Apple
,com.apple.news,News,Apple
,com.apple.mobilenotes,Notes,Apple
,com.apple.Numbers,Numbers,Apple
,com.apple.Pages,Pages,Apple
,com.apple.Photo-Booth,Photo Booth,Apple
,com.apple.mobileslideshow,Photos,Apple
,com.apple.podcasts,Podcasts,Apple
,com.apple.reminders,Reminders,Apple
,com.apple.MobileSafari,Safari,Apple
,com.apple.Preferences,Settings,Apple
,com.apple.stocks,Stocks,Apple
,com.apple.tips,Tips,Apple
,com.apple.videos,Videos,Apple
,com.apple.VoiceMemos,VoiceMemos,Apple
,com.apple.Passbook,Wallet,Apple
,com.apple.Bridge,Watch,Apple
,com.apple.weather,Weather,Apple
```




## Custom policy settings

Use the Microsoft Intune **iOS custom policy** to deploy settings that you created by using the [Apple Configurator tool](https://itunes.apple.com/us/app/apple-configurator/id434433123?mt=12) to iOS devices. This tool lets you create many settings that control the operation of these devices and export them to a configuration profile. You can then import this configuration profile into an Intune iOS custom policy and deploy the settings to users and devices in your organization.

This capability allows you to deploy iOS settings that are not configurable with Intune general configuration policies.

### Prerequisites
Before you start, you must have installed the Apple Configurator and created a configuration file that contains the settings that you want to deploy to users or devices. You can download and learn about the Apple Configurator from [the Mac App Store](https://itunes.apple.com/us/app/apple-configurator/id434433123?mt=12).

> [!NOTE]
> Intune does not report the compliance of individual settings in an iOS custom policy. However, the overall compliance of the policy is reported.

### General settings

|Setting name|Details|
    |----------------|--------------------|
    |**Name**|Enter a unique name for the iOS custom policy to help you identify it in the Intune console.|
    |**Description**|Provide a description that gives an overview of the iOS custom policy and other relevant information that helps you to locate it.|

### Custom settings

|Setting name|Details|
    |----------------|--------------------|
|**Custom configuration profile name (displayed to users)**|Provide a name for the policy as it will be displayed on the device, and in Intune policy reports.|
|**Configuration profile file**|Choose **Import**, and then browse to the configuration profile that you created by using the Apple Configurator. **Note:** Ensure that the settings you export from the Apple Configurator tool are compatible with the version of iOS on the devices to which you deploy the iOS custom policy. For information about how incompatible settings are resolved, search for **Configuration Profile Reference** and **Mobile Device Management Protocol Reference** on the [Apple Developer](https://developer.apple.com/) website.|
    |**Configuration profile details**|Display the XML code for the configuration profile that you imported.|

### See also
[Manage settings and features on your devices with Microsoft Intune policies](manage-settings-and-features-on-your-devices-with-microsoft-intune-policies.md)

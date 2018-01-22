---
# required metadata

title: Intune Wi-Fi settings for iOS devices
titleSuffix: "Azure portal"
description: Learn the Intune settings you can use to configure Wi-Fi connections on iOS devices."
keywords:
author: vhorne
ms.author: victorh
manager: angrobe
ms.date: 02/15/2017
ms.topic: article
ms.prod:
ms.service: microsoft-intune
ms.technology:
ms.assetid: 89229a5e-3421-4221-a62f-fa800620cc0d

# optional metadata

#ROBOTS:
#audience:
#ms.devlang:
ms.reviewer: heenamac
ms.suite: ems
#ms.tgt_pltfrm:
ms.custom: intune-azure

---

# Wi-Fi settings for iOS devices in Microsoft Intune

[!INCLUDE [azure_portal](./includes/azure_portal.md)]

## Wi-Fi settings for basic and enterprise profiles

- **Network name** - Enter a name for this Wi-Fi connection. This is the name that users will see when they browse the list of available connections on their device.
- **SSID** - Short for service set identifier. This is the real name of the wireless network that devices will connect to. However, users only see the network name you created above when they choose the connection.
- **Connect automatically** - Makes the device connect whenever it is in the range of this network.
- **Hidden network** - Prevents this network from being shown in the list of available networks on the device.
- **Proxy settings** - Choose from:
    - **None** - No proxy settings will be configured.
    - **Manual** - Enter the **Proxy server address** (as an IP address), and it's associated **Port number**.
    - **Automatic** - Use a file to configure the proxy server. Enter the **Proxy server URL** (for example **http://proxy.contoso.com**) which contains the configuration file.

## Wi-Fi settings for basic profiles only

- **Security type** - Select the security protocol to use to authenticate to the Wi-Fi network from:
    - **Open (no authentication)** - Only use this option if the network is unsecured.
    - **WPA/WPA2 - Personal**
    - **WEP**

## Wi-Fi settings for enterprise profiles only

- **EAP type** - Choose the Extensible Authentication Protocol (EAP) type used to authenticate secured wireless connections from:
    - **EAP-FAST**
    - **EAP-SIM**
    - **EAP-TLS**
    - **EAP-TTLS**
    - **LEAP**
    - **PEAP**

### Further options when you choose an EAP type


|Setting name|More information|Use when|
|--------------|-------------|----------|
|**Protected Access Credential (PAC) Settings**|Select to use protected access credentials to establish an authenticated tunnel between the client and the authentication server. Select one of:<br>- **Use PAC** - Use an existing PAC file is used if present.<br>- **Use and Provision PAC** - Provision the PAC file to your devices.<br>- **Use and Provision PAC Anonymously** - Provision the PAC file to your devices and ensure that the PAC file is provisioned without authenticating the server.|EAP type is **EAP-FAST**|

#### Server Trust


|Setting name|More information|Use when|
|--------------|-------------|----------|
|**Certificate server names**|Specify one or more common names used in the certificates issued by your trusted certificate authority (CA). If you provide this information, you can bypass the dynamic trust dialog that is displayed on end users devices when they connect to this Wi-Fi network.|EAP type is **EAP-TLS**, **EAP-TTLS**, or **PEAP**.|
|**Root certificate for server validation**|Choose the trusted root certificate profile used to authenticate the connection. |EAP type is **EAP-TLS**, **EAP-TTLS**, or **PEAP**|
|**Identity privacy (outer identity)**|Specify the text sent in response to an EAP identity request. This text can be any value. During authentication, this anonymous identity is initially sent, and then followed by the real identification sent in a secure tunnel.|EAP type is **PEAP**|


#### Client Authentication


|                                     Setting name                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         More information                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |                  Use when                  |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <strong>Client certificate for client authentication (Identity certificate)</strong> |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         Choose the SCEP or PKCS certificate profile used to authenticate the connection.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |    EAP type is <strong>EAP-TLS</strong>    |
|                        <strong>Authentication method</strong>                        | Select the authentication method for the connection:<br>- <strong>Certificates</strong> to select the SCEP or PKCS the client certificate that is the identity certificate presented to the server.<br><br>- <strong>Username and Password</strong> to specify a different method for authentication. <br><br>If you selected <strong>Username and Password</strong>, configure:<br><br>-  <strong>Non-EAP method (inner identity)</strong>, then select how you will authenticate the connection from:<br>- <strong>None</strong><br>- <strong>Unencrypted password (PAP)</strong><br>- <strong>Challenge Handshake Authentication Protocol (CHAP)</strong><br>- <strong>Microsoft CHAP (MS-CHAP)</strong><br>- <strong>Microsoft CHAP Version 2 (MS-CHAP v2)</strong><br>The available options depend on the EAP type you selected.<br><br><strong>and</strong><br><br>- <strong>Identity privacy (outer identity)</strong> - Specify the text sent in response to an EAP identity request. This text can be any value. During authentication, this anonymous identity is initially sent, and then followed by the real identification sent in a secure tunnel. | EAP type is <strong>EAP-TTLS</strong> or * |


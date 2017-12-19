---
# required metadata

title: Intune VPN settings for Windows 10 devices
titlesuffix: "Azure portal"
description: Learn about the Intune settings you can use to configure VPN connections on Windows 10 devices."
keywords:
author: vhorne
ms.author: victorh
manager: angrobe
ms.date: 10/20/2017
ms.topic: article
ms.prod:
ms.service: microsoft-intune
ms.technology:
ms.assetid: 495e4ed6-b2ef-47cc-a110-13fa9b5f85a6

# optional metadata

#ROBOTS:
#audience:
#ms.devlang:
ms.reviewer: karanda
ms.suite: ems
#ms.tgt_pltfrm:
ms.custom: intune-azure

---

# VPN settings for Windows 10 devices in Microsoft Intune

[!INCLUDE[azure_portal](./includes/azure_portal.md)]

Depending on the settings you choose, not all values in the list below will be configurable.


## Base VPN settings


- **Connection name** - Enter a name for this connection. End users will see this name when they browse their device for the list of available VPN connections.
- **Servers** - Add one or more VPN servers that devices will connect to.
	- **Add** - Opens the **Add Row** blade where you can specify the following information:
		- **Description** - Specify a descriptive name for the server like **Contoso VPN server**.
		- **IP address or FQDN** - Provide the IP address or fully qualified domain name of the VPN server that devices will connect to. Examples: **192.168.1.1**, **vpn.contoso.com**.
		- **Default server** - Enables this server as the default server that devices will use to establish the connection. Make sure to set only one server as the default.
	- **Import** - Browse to a file containing a comma-separated list of servers in the format description, IP address or FQDN, Default server. Choose **OK** to import these into the **Servers** list.
	- **Export** - Exports the list of servers to a comma-separated-values (csv) file.

**Connection type** - Select the VPN connection type from the following list of vendors:
- **Automatic**
- **Check Point Capsule VPN**
- **Citrix VPN**
- **Dell SonicWALL Mobile Connect**
- **F5 Edge Client**
- **IKEv2**
- **L2TP**
- **PPTP**
- **Pulse Secure**


**Login group or domain** (Dell SonicWALL Mobile Connect only) - Specify the name of the login group or domain that you want to connect to.

**Custom XML**/**EAP XML** - Specify any custom XML commands that configure the VPN connection.

**Example for Pulse Secure:**

```
	<pulse-schema><isSingleSignOnCredential>true</isSingleSignOnCredential></pulse-schema>
```

**Example for CheckPoint Mobile VPN:**

```
	<CheckPointVPN port="443" name="CheckPointSelfhost" sso="true" debug="3" />
```

**Example for Dell SonicWALL Mobile Connect:**

```
	<MobileConnect><Compression>false</Compression><debugLogging>True</debugLogging><packetCapture>False</packetCapture></MobileConnect>
```

**Example for F5 Edge Client:**

```
	<f5-vpn-conf><single-sign-on-credential /></f5-vpn-conf>
```

Refer to each manufacturer's VPN documentation for more information about how to write custom XML commands.

**Split tunneling** - **Enable** or **Disable** this option which lets devices decide which connection to use depending on the traffic. For example, a user in a hotel will use the VPN connection to access work files, but use the hotel's standard network for regular web browsing.
- **Split tunneling routes for this VPN connection** - Add optional routes for third-party VPN providers. Specify a destination prefix, and a prefix size for each.

## Apps and Traffic Rules

**Restrict VPN connection to these apps** - Enable this option if you only want apps you specify to use the VPN connection.
**Associated Apps** - Provide a list of apps that will automatically use the VPN connection. The type of app will determine the app identifier. For a universal app, provide the package family name. For a desktop app, provide the file path of the app.

>[!IMPORTANT]
>We recommend that you secure all lists of apps that you compile for use in configuration of per-app VPN. If an unauthorized user modifies your list and you import it into the per-app VPN app list, you will potentially authorize VPN access to apps that should not have access. One way you can secure app lists is by using an access control list (ACL).

**Network traffic rules for this VPN connection** - Select which protocols, and which local and remote port and address ranges, will be enabled for the VPN connection. If you do not create a network traffic rule, all protocols, ports, and address ranges are enabled. After you create a rule, the VPN connection will use only the protocols, ports, and address ranges that you specify in that rule.


## Conditional Access

**Conditional access for this VPN connection** - Enables device compliance flow from the client. When enabled, the VPN client will attempt to communicate with Azure Active Directory to get a certificate to use for authentication. The VPN should be set up to use certificate authentication, and the VPN server must trust the server returned by Azure Active Directory.

**Single sign-on (SSO) with alternate certificate** - For device compliance, use a certificate different from the VPN authentication certificate for Kerberos authentication. Specify the certificate with the following settings: 

- **Extended key usage** - Name for extended key usage (EKU).
- **Object Identifier** - Object identifier for EKU.
- **Issuer hash** - Thumbprint for SSO certificate.

## DNS Settings

**DNS names and servers for this VPN connection** - Select which DNS servers the VPN connection will use after the connection is established.
For each server. specify:
- **DNS Name**
- **DNS Server**
- **Proxy**

## Proxy settings

- **Automatically detect proxy settings** - If your VPN server requires a proxy server for the connection, specify whether you want devices to automatically detect the connection settings. For more information, see your Windows Server documentation.
- **Automatic configuration script** - Use a file to configure the proxy server. Enter the **Proxy server URL** (for example **http://proxy.contoso.com**) which contains the configuration file.
- **Use proxy server** - Enable this option if you want to manually enter the proxy server settings.
	- **Address** - Enter the proxy server address (as an IP address).
	- **Port number** - Enter the port number associated with the proxy server.
- **Bypass proxy for local addresses** - If your VPN server requires a proxy server for the connection, select this option if you do not want to use the proxy server for local addresses that you specify. For more information, see your Windows Server documentation.

---
title: Zoo License Manager Help
description: The Zoo keeps your Rhino licenses in one place and lets you share them with Rhino users on your network.
---
# Advanced Zoo Topics

To begin using the Zoo:

- The Zoo requires the Microsoft .NET Framework 4.
- [Download](http://wiki.mcneel.com/zoo/home) and install the Zoo on a Windows-based server or workstation.
- Make sure **TCP Port 80 (HTTP)** is open on any firewall software that is running on the server or workstation.
- Run the **Zoo Administrator (ZooAdmin.exe)** and add the license keys for Rhino or your Rhino-based products.
- Install Rhino or your Rhino-based products. During the installation, select **Network Node** as your license type and specify either the host name or IP address of your Zoo server.

If you already have Rhino installed, then launch Rhino and click **Tools → Options → Licenses**. Select your Rhino license and click **Convert**. Then, close Rhino and restart. At startup, select **Network Node** as your license type and specify either the host name or IP address of your Zoo server.

## How does Rhino find the Zoo?

When Rhino 5 needs a license from a Zoo 5 server, it determines the name of the Zoo 5 server by looking in the following locations in order:

1. Looks in the Current User hive of the Windows Registry for the host name or IP address of your Zoo server.
2. Looks in the Local Machine hive of the Windows Registry for the host name or IP address of your Zoo server.
3. Queries your Domain Name System (DNS) server for the default Zoo server name.

#### Registry Key - Current User

When searching in HKEY_CURRENT_USER, of the Windows Registry, for the host name or IP address of your Zoo server, both Rhino 5 32-bit and Rhino 5 64-bit will look in this location:

```
Hive:HKEY_CURRENT_USER
Key:   Software\McNeel\Rhinoceros\5.0\License Manager
Name:  Server
Type:  REG_SZ
Value: <host name or IP address>
```

#### Registry Key - Local Machine

If you are using a 32-bit version of Windows, then when searching in HKEY_LOCAL_MACHINE, of the Windows Registry, for the host name or IP address of your Zoo server, Rhino 5 32-bit will look in this location:

```
Hive:  HKEY_LOCAL_MACHINE
Key:   Software\McNeel\Rhinoceros\5.0\License Manager
Name:  Server
Type:  REG_SZ
Value: <host name or IP address>
```

If you are using a 64-bit version of Windows, then when searching in HKEY_LOCAL_MACHINE, of the Windows Registry, for the host name or IP address of your Zoo server, both Rhino 5 32-bit and Rhino 5 64-bit will look in this location:

```
Hive:  HKEY_LOCAL_MACHINE
Key:   SOFTWARE\Wow6432Node\McNeel\Rhinoceros\5.0\License Manager
Name:  Server
Type:  REG_SZ
Value: <host name or IP address>
```

#### DNS

If a host name or IP address is not found in the above locations, then the license manager will query the system's default DNS server using the default Zoo server host name.

The default Zoo server host name is:

`__mcneel.__zoo5.<your second-level domain>`

For example, of your organization's second-level domain name is **mycorp.com**, then Rhino's license manager will query the system's default DNS server for a host named **__mcneel.__zoo5.mycorp.com**.

To make it easier to deploy Rhino and Rhino-based products on your network, you might consider adding a **CNAME**, or Canonical Name, record to your organization's DNS server. A CNAME record specifies that the domain name is an alias of another, canonical domain name.

# Viewing Events

The Zoo logs all activities in the Windows Event Log. To view the Windows Event Log, run the **Zoo Administrator **(ZooAdmin.exe), and then click **View → Event Viewer**.

![zoo_event_log.png](http://docs.mcneel.com/zoo/5/en/images/zoo_event_log.png)

All Zoo event log entries can be fond in the **McNeel** folder inside of the **Applications and Services Logs** folder. When troubleshooting Zoo issues, it is a good idea to check the Windows Event Log to see if there is any indication of trouble.
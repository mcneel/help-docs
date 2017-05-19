---
title: Zoo License Manager Help
description: The Zoo keeps your Rhino licenses in one place and lets you share them with Rhino users on your network.
---
# Installation

To begin using the Zoo:

1. [Install the Zoo](#installing-on-the-server) on a single Windows computer.  The Zoo server must run on a Windows computer.
2. [Install Rhino](#installing-on-the-clients) on the clients computers.  Both Rhino for Windows and Rhino for Mac can be installed as clients to the Zoo.

## Installing on the Server

1. The Zoo requires the [Microsoft .NET Framework 4.5](https://www.microsoft.com/en-us/download/details.aspx?id=30653). You can ensure that Microsoft .NET Framework 4.5 is installed on your system using [Windows Update](http://windows.microsoft.com/en-us/windows/windows-update).
2. Download](http://www.rhino3d.com/download/zoo/6/latest) and install the Zoo on a Windows-based server or workstation.
3. Make sure [TCP Port 80 (HTTP)](http://wiki.mcneel.com/it/zoo/window7firewall) is open on any firewall software that is running on the server or workstation.
4. Run the Zoo Administrator (ZooAdmin.exe) and [add the license]({{site.url}}/{{page.language}}/zoo/6/help/manage#adding-licenses) keys for Rhino or your Rhino-based products.

## Installing on the Clients

For a new install of Rhino:

1. Install Rhino or your Rhino-based products. During the installation, select Network Node as your license type
2. specify either the [host name or IP address](https://wiki.mcneel.com/zoo/determinezoohost) of your Zoo server.

If you already have Rhino installed: 

1. Launch Rhino
2. Click Tools → Options → Licenses 
3. Select your Rhino license, click Convert
4. Then, close Rhino and restart. 
5. At startup, select Network Node as your license type and specify either the [host name or IP address](https://wiki.mcneel.com/zoo/determinezoohost) of your Zoo server.

## Moving the Zoo

Moving the Zoo license manager software from one server to another is really no different than installing the Zoo software from scratch.

Note, there is no way to “move” or “copy” McNeel product CD-Keys from one Zoo server to another. Product CD-Keys must be added to the new Zoo server just as you did with your original Zoo server.
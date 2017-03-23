---
title: Zoo License Manager Help
description: The Zoo keeps your Rhino licenses in one place and lets you share them with Rhino users on your network.
productname: Zoo License Manager
language: en
productpath: zoo
productversionpath: 6
type: help
collectionname: Help
keywords: ['zoo', 'rhinoceros', 'license', 'manager']
layout: zoo-help-page
---

# Overview

The Zoo lets you share, or float, the licenses of Rhino and Rhino-based products among users on the same network. When one of these products is installed as a **Network Node**, instead of as a Standalone Node, it will work like this:

- When a Network Node starts, it requests a license from the Zoo.
- An unused license is assigned to the Network Node.
- When a Network Node shuts down, the license is returned to the Zoo's license pool.

# Features

The Zoo had a number of unique features:

- **Free** - The Zoo is a free [download](http://wiki.mcneel.com/zoo/home).

- **No extra costs** - Special versions of Rhino and Rhino-based products are not needed.

- **No special hardware is needed** - The Zoo will run on any system on your network.

- **Simple setup** - Install the Zoo on any system on your network, and then enter the license keys into the Zoo instead of the individual systems.

- **Routable** - The Zoo works on both single-segments networks, or networks where systems are separated by routers.

- **Multiple server** - You can have more than one Zoo server running at a time, with each serving different clients.

- **Mixed environment** - A mixture of Network Nodes and Standalone Nodes on the same network is supported.

- **Check out** - License keys can be checked out so laptop users can disconnect from the network. The key can be checked in again when the laptop is reconnected to the network.

- **Robust** - Network nodes will keep working even if the network connection or server is down, but Network Nodes cannot start up without access to the Zoo.

- **Runs as a service** - The Zoo is a Windows Service. If you reboot the system with the Zoo, you do not have to log onto the computer to start the Zoo.

  # What's New?

  Zoo 5 is a brand new version of the Zoo. Completely rewritten, Zoo 5 provides a number of new features not found in prior Zoo versions, including:

  - **Standard Internet Protocol Support** - Clients communicate with Zoo 5 using TCP Port 80 (HTTP). This makes it much easier for system administrators to route Zoo requests on complex networks or even over the Internet.
  - **Firewall Friendly** - Zoo 5 requires the client to periodically check with the server, but never initiates connections back to the client. Administrators no longer need to open additional firewall ports on client machines.
  - **Limited License Check Out** - Prior Zoo version allows for license check out to support laptop users or for business travel. But there was no limit to the check out duration. Zoo 5 allows the administrator to specify the license check out duration.
  - **Remote License Monitoring** - Zoo 5 allows users and administrators to monitor license usage from the convenience of their web browser.
  - **3rd Party Plug-in Support** - Prior Zoo version only maintained licenses for McNeel product (e.g. Rhino. Flamingo, Bongo, Brazil, and Penguin). Zoo 5 allows 3rd party plug-in developers to add support for their products to the Zoo.
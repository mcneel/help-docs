---
---

{: #kanchor318}
# Licenses
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/options.png](images/options.png) [Properties](properties-toolbar.html)  [Standard](standard-toolbar.html)  [Tools](tools-toolbar.html) 
Menus
Tools
Options
TheLicenseoptions display the license status of the current Rhino license.
Licenses
Options
 ** [Check In](#checkinlicense) ** 
 ** [Check Out](#checkoutlicense) ** 
 **![images/convertlicense.png](images/convertlicense.png)Convert** 
Converts a standalone license to a network node.
You must have a Zoo license server on your network.
![images/zoologo-90x90.png](images/zoologo-90x90.png)

# Related commands

## CheckOutLicense
{: #kanchor325}
{: #kanchor324}
{: #kanchor323}
{: #kanchor322}
{: #kanchor321}
{: #kanchor320}
{: #kanchor319}
{: #checkoutlicense}
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/-no-toolbar-button.png](images/-no-toolbar-button.png) [Not on toolbars.](toolbarwhattodo.html) 
Menus
Tools
License Manager![images/menuarrow.gif](images/menuarrow.gif)
Check Out License
TheCheckOutLicensecommand checks a license out from the [network license manager (Zoo)](#licensemanager).
Details
When you run theCheckOutLicensecommand, the Rhino license converts to a standalone node from a network node. You can then remove your computer from the network and continue to run Rhino.
TheCheckOutLicensecommand allows users to check out a license from the license manager. This converts their network node to a standalone node. The user can then run Rhino without being connected to the network.
When reconnect to the network, they must run theCheckInLicensecommand to check their keys back into the Zoo.

## CheckInLicense
{: #kanchor327}
{: #kanchor326}
{: #checkinlicense}
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/-no-toolbar-button.png](images/-no-toolbar-button.png) [Not on toolbars.](toolbarwhattodo.html) 
Menus
Tools
License Manager![images/menuarrow.gif](images/menuarrow.gif)
Check In License
TheCheckInLicensecommand checks in a license key to the network license manager.
When you run theCheckInLicensecommand, the Rhino license key converts a network node from a standalone node, and the license key checks into the [network license manager (Zoo)](#licensemanager).

## Network License Manager (The Zoo)
{: #licensemanager}
Manages assignment of Rhino licenses among members of a network.
To script the installation process and allow more efficient use of Rhino licenses, network administrators now have the option of installing Rhino as a network node. Network nodes obtain license keys at run time from the Zoo, unlike standalone Rhino, which requires that a license key be entered on each system.
When a Rhino network node starts, a request for a license key is sent to the Zoo. If the number of available keys has not been exceeded, the Zoo assigns a key to the workstation, and the number of available licenses is reduced by one. When a node shuts down, the license is added back to the available license pool.
The Zoo will run on any system in a network. All of the nodes must be in the same network. The Zoo uses an inter-process communications mechanism that is used by several networking services. Thus, the Zoo should operate reliably in both Microsoft Network and Domain networking environments. For details on setting up a network, contact your network administrator.
The Zoo can be [downloaded](http://download.mcneel.com/zoo/) free of charge.
Features include:
No special version of Rhino is needed.No special hardware is needed.Commercial versions of Rhino will work either as a standalone license or as a network node. This is an installation option.Standalone license keys can easily be converted to network nodes and back.All the nodes will keep working even if the network connection or server is down, but no new ones can start up without access to the Zoo.The Zoo will run on any system in the network.Very little administration is required. The license keys are typed into the Zoo instead of on individual systems.A network can have a mix of nodes and standalone licenses.Rhino license keys can be checked out so laptop users can disconnect from the network. The license key can be checked in again when the laptop is reconnected to the network.To save options for use on other computers
![images/optionsexport.png](images/optionsexport.png) [OptionsExport](optionsexport.html) 
Save [Options](options.html) settings to a file.
![images/optionsimport.png](images/optionsimport.png) [OptionsImport](optionsexport.html#optionsimport) 
Restore [Options](options.html) settings from a file.
See also
 [McNeel Wiki:&#160;Zoo License Manager](http://wiki.mcneel.com/zoo/home) 
 [Work with files](sak-file.html) 
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](licenses.html) 


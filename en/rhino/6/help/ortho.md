---
---

{: #kanchor1633}{: #kanchor1634}{: #kanchor1635}{: #kanchor1636}{: #kanchor1637}{: #kanchor1638}{: #kanchor1639}{: #kanchor1640}
# Ortho
TheOrthocommand specify the angle at which the movement of the cursor is restricted when [ortho](#) mode is active.
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/ortho.png](images/ortho.png) [Object Snap](object-snap-toolbar.html) 
Menus
![images/-no-menu-item.png](images/-no-menu-item.png) [Not on menus.](menuwhattodo.html) 
 [Status bar](rhino-window.html#appwindow-statusbar) 
Ortho
Shortcut
ShiftF8
The Ortho command restricts the movement of the cursor to multiples of a specified angle from the last point created.
Note
TheOrthocommand, clickingOrthoin the status bar, and theF8key, are all toggles. Holding [Shift](shift-key.html) changes the mode while you hold the key down.The [SetOrtho](#setortho) command prompts for a setting with the optionsOn,Off, andToggle. This is useful for inclusion in a script for the [ReadCommandFile](rhinoscripting.html#readcommandfile) command.When Ortho is on, [id="a2005">marker]() movement is restricted to points at multiples of a specified angle from the last point created. The default angle is 90 degrees.
# OrthoAngle
{: #orthoangle}
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/orthoangle.png](images/orthoangle.png) [Object Snap](object-snap-toolbar.html) 
Menus
![images/-no-menu-item.png](images/-no-menu-item.png) [Not on menus.](menuwhattodo.html) 
 [Status bar](rhino-window.html#appwindow-statusbar) 
Right-click Ortho pane![images/menuarrow.gif](images/menuarrow.gif)
Set Ortho Angle
The OrthoAngle command specifies the angle at which the movement of the cursor is restricted when [ortho](#) mode is active.
Steps
Type the new angle.{: #setortho}
# SetOrtho
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/-no-toolbar-button.png](images/-no-toolbar-button.png) [Not on toolbars.](toolbarwhattodo.html) 
Menus
![images/-no-menu-item.png](images/-no-menu-item.png) [Not on menus.](menuwhattodo.html) 
 [Status bar](rhino-window.html#statusbarpanes) 
Right-click Ortho pane![images/menuarrow.gif](images/menuarrow.gif)
Ortho On/Off
The SetOrtho command turns [ortho](#) mode on, off, or toggles the current state.
This is useful for inclusion in a script file for the [ReadCommandFile](rhinoscripting.html#readcommandfile) command.
Steps
 [Specify a command line option.](specifycommandlineoption.html) Command-line options
On
Off
Toggle
See also
 [Use modeling aids](sak-modelingaids.html) 
 [Model with precision](sak-precisionmodeling.html) 
 [Cursor constraints](cursor-constraints.html) 
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](ortho.html) 


---
---

{: #kanchor1679}{: #kanchor1680}{: #kanchor1681}{: #kanchor1682}{: #kanchor1683}{: #kanchor1684}
# Planar
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/-no-toolbar-button.png](images/-no-toolbar-button.png) [Not on toolbars.](toolbarwhattodo.html) 
Menus
![images/-no-menu-item.png](images/-no-menu-item.png) [Not on menus.](menuwhattodo.html) 
 [Status bar](rhino-window.html#appwindow-statusbar) 
Planar
The Planar command limits successive picked locations to the same construction plane elevation as the previous location.
Planar mode aids in creating planar objects with commands that allow free picking. Successive points have the same construction plane elevation.
Example
From theCurvemenu, clickFree-form, then clickControl Points.Pick the first point in the lower part of theTopviewport.Move the cursor to the Front viewport and continue drawing.You will see that all the points you pick define a planar curve at the same elevation in the Front viewport. (Watch the Top and Right viewports). That elevation for the Front viewport was defined by the very first point you placed in the Top viewport.WithPlanaroff, the subsequent points would be at elevation 0 in the Front viewport.Note
Each point picked in a viewport will have the same elevation from that viewport's construction plane as the previous point, regardless of where the previous point was picked.Planar mode can be overridden with [elevator mode](cursor-constraints.html#elevator-mode) or [object snaps](object-snaps.html).
# SetPlanar
{: #setplanar}
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/-no-toolbar-button.png](images/-no-toolbar-button.png) [Not on toolbars.](toolbarwhattodo.html) 
Menus
![images/-no-menu-item.png](images/-no-menu-item.png) [Not on menus.](menuwhattodo.html) 
 [Status bar![images/menuarrow.gif](images/menuarrow.gif)](rhino-window.html#statusbarpanes) 
Right-click Planar pane![images/menuarrow.gif](images/menuarrow.gif)
Planar Mode On/Off
The SetPlanar command turns [Planar](#) mode on, off, or toggles the current state.
Steps
 [Specify a command line option.](specifycommandlineoption.html) This is useful for inclusion in a script file for the [ReadCommandFile](rhinoscripting.html#readcommandfile) command.Command-line options
On
Off
Toggle
See also
 [Use modeling aids](sak-modelingaids.html) 
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](planar.html) 


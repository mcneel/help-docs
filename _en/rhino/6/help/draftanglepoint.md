---
---


# DraftAnglePoint
{: #kanchor787}
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/-no-toolbar-button.png](images/-no-toolbar-button.png) [Not on toolbars.](toolbarwhattodo.html) 
Menus
![images/-no-menu-item.png](images/-no-menu-item.png) [Not on menus.](menuwhattodo.html) 
The DraftAnglePoint command places a point object at a surface's draft angle break location.
Draft angle is used to design injection-molded parts that must eject from molds.
Steps
 [Select](select-objects.html) a surface near the draft point, and press [Enter](enter-key.html) .Tip
One way to find locations on the surface close to the desired draft angle is to turn on [DraftAngleAnlaysis](draftangleanalysis.html). Set the upper and lower limits to bracket the desired angle closely. For example, if the angle is 5, set the limits to 4.9 and 5.1.Use a dense analysis mesh. Points can then be picked along the strip dividing the red from the blue parts of the surface. The pick will then produce a draft angle point.Command-line options
Angle
The angle in world coordinates of a line tangent to the surface at the draft angle point.
PullDirection
The direction of the part ejection in world coordinates.
Edge
Restricts the point placement to an edge.
See also
 [Analyze objects](sak-analysis.html) 
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](draftanglepoint.html) 


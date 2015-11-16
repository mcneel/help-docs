---
---

{: #kanchor1877}{: #kanchor1878}{: #kanchor1879}{: #kanchor1880}
# Revolve
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/revolve.png](images/revolve.png) [Surface Creation](surface-creation-toolbar.html)  [Surface Sidebar](surface-sidebar-toolbar.html) 
Menus
Surface
Revolve
![images/history-tag.png](images/history-tag.png) [&#160;History enabled](historyenabled.html) 
![images/creasesplitting-tag.png](images/creasesplitting-tag.png)&#160; [Crease splitting enabled](creasesplttingenabled.html) 
The Revolve command creates a surface by revolving a profile curve that defines the surface shape around an axis.
Steps
 [Select](select-objects.html) curves. [Pick](pick-location.html) the start of the revolve axis.Pick the end of the revolve axis.Specify options.Your browser does not support the video tag.Command-line options
DeleteInput
Yes
Deletes the original geometry.
No
Retains the original geometry.
Deformable
IfYes, the surface is rebuilt on the 'around' direction to a degree-3 non-rational surface. Specify how many points in that direction. Deformable revolves can be deformed smoothly with point editing.
IfNo, the resulting revolved surface is an exact revolve: a rational surface with fully-multiple knots at the quadrants. This kind of surface is not easy to deform smoothly by point editing.
PointCount
The PointCount option specifies the number of [control points](controlpoint.html) in the result.
FullCircle
TheFullCircleoption revolves the input curve 360 degrees as a shortcut for specifying 360 degrees as the revolve angle.
AskForStartAngle
TheYesoption allows setting the angle (a number of degrees away from the current input curve location) the revolve will start.
TheNooption starts the revolve from 0 (the input curve location).
SplitAtTangents
Yes
Creates a single surface.
No
Creates a polysurface when the input curves are joined tangent curves. Faces in the resulting polysurface correspond to the tangent sub-curves in the input curves.
![images/extrudesplitattangents-yes.png](images/extrudesplitattangents-yes.png)
Original polycurve (left), SplitAtTangents=No (center), SplitAtTangents=Yes (right).
Note
When this option is used, the output will be a polysurface.When [UseExtrusions](useextrusions.html) is on, this setting has no effect.See also
 [Create surfaces](sak-surface.html) 
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](revolve.html) 


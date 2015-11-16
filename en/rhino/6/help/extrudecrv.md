---
---


# ExtrudeCrv
{: #kanchor995}
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/extrudesrf.png](images/extrudesrf.png) [Extrude](extrude-toolbar.html)  [Extrude Solid](extrude-solid-toolbar.html)  [Solids Creation](solid-creation-toolbar.html)  [Solids Sidebar](solids-sidebar-toolbar.html)  [Surface Sidebar](surface-sidebar-toolbar.html)  [Surface Creation](surface-creation-toolbar.html) 
Menus
Solid
Extrude Planar Curve![images/menuarrow.gif](images/menuarrow.gif)
Straight
Surface
Extrude Curve![images/menuarrow.gif](images/menuarrow.gif)
Straight
![images/history-tag.png](images/history-tag.png) [&#160;History enabled](historyenabled.html) 
![images/extrusion-tag.png](images/extrusion-tag.png)&#160; [Extrusions enabled](extrusionsenabled.html) 
The ExtrudeCrv command creates a surface by tracing the path of a curve in a straight line.
Steps
 [Select](select-objects.html) a curve. [Specify a distance](distance-pick-2pts.html) .Your browser does not support the video tag.Note
If the curve is not planar, then it will be extruded in the z&#160;direction of the active viewport's construction plane. If the curve is planar, it will be extruded in the normal direction of the plane of the curve.Unlike [Lofts](loft.html) and [Sweeps](sweep1.html), the initial orientation of the profile curve or surface is maintained through the extrusion.If the input is a non-planar polycurve or a planar polycurve where the extrusion direction is not normal to the curve plane, the result will be a [polysurface](polysurface.html) rather than an [extrusion object](useextrusions.html) .Command-line options
SetBasePoint
Specify a location that serves as the first point when picking two points that set the extrusion distance.
Direction
Two points establish the direction angle.
Direction steps
 [Pick](pick-location.html) a base point.Pick a second point that establishes the direction angle.BothSides
The BothSides option draws the object on both sides of the start point, creating the object twice as long as you indicate.
![images/line-bothsides.png](images/line-bothsides.png)
The BothSides option demonstrated with the [Line](line.html) command.
Solid
If the profile curve is closed and planar, both ends of the extruded object are filled with planar surfaces and joined to make a closed polysurface.
ToBoundary
Extrudes the object to a boundary surface.
DeleteInput
Yes
Deletes the original geometry.
No
Retains the original geometry.
SplitAtTangents
Yes
Creates a single surface.
No
Creates a polysurface when the input curves are joined tangent curves. Faces in the resulting polysurface correspond to the tangent sub-curves in the input curves.
![images/extrudesplitattangents-yes.png](images/extrudesplitattangents-yes.png)
Original polycurve (left), SplitAtTangents=No (center), SplitAtTangents=Yes (right).
Note
When this option is used, the output will be a polysurface.When [UseExtrusions](useextrusions.html) is on, this setting has no effect.See also
 [Extrude curves and surfaces](sak-extrude.html) 
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](extrudecrv.html) 


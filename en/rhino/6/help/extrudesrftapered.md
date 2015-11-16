---
---


# ExtrudeSrfTapered
{: #kanchor1007}
{: #kanchor1006}
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/extrudesrftapered.png](images/extrudesrftapered.png) [Extrude Solid](extrude-solid-toolbar.html) 
Menus
Solid
Extrude Surface![images/menuarrow.gif](images/menuarrow.gif)
Tapered
![images/history-tag.png](images/history-tag.png) [&#160;History enabled](historyenabled.html) 
The ExtrudeSrfTapered command creates a solid by tracing the path of the surface edges in a straight line tapering in or out at a specified draft angle.
Steps
 [Select](select-objects.html) a surface. [Specify a distance](distance-pick-2pts.html) .Your browser does not support the video tag.Note
If the curve is not planar, then it will be extruded in the z&#160;direction of the active viewport's construction plane. If the curve is planar, it will be extruded in the normal direction of the plane of the curve.Unlike [Lofts](loft.html) and [Sweeps](sweep1.html), the initial orientation of the profile curve or surface is maintained through the extrusion.If the input is a non-planar polycurve or a planar polycurve where the extrusion direction is not normal to the curve plane, the result will be a [polysurface](polysurface.html) rather than an [extrusion object](useextrusions.html) .Command-line options
SetBasePoint
Specify a location that serves as the first point when picking two points that set the extrusion distance.
Direction
Two points establish the direction angle.
Direction steps
 [Pick](pick-location.html) a base point.Pick a second point that establishes the direction angle.DraftAngle
Specify the *draft angle* for the taper.
The draft angle depends on the construction plane orientation. When the surface is vertical/perpendicular to the construction plane, the draft angle is zero. When the surface is parallel to the construction plane, the draft angle is 90 degrees.
Solid
If the profile curve is closed and planar, both ends of the extruded object are filled with planar surfaces and joined to make a closed polysurface.
Corners
Specifies how corner [continuity](continuity-descriptions.html) is handled.
Sharp
The corners of the tapered surfaces will extend to meet at sharp corners with position (G0) continuity.
Round
The corners of the tapered surfaces will be filled with filleted segments with tangent (G1) continuity.
Smooth
The corners of the tapered surfaces will be filled with blend segments with curvature (G2) continuity.
DeleteInput
Yes
Deletes the original geometry.
No
Retains the original geometry.
FlipAngle
Toggles the draft angle direction.
See also
 [Extrude curves and surfaces](sak-extrude.html) 
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](extrudesrftapered.html) 


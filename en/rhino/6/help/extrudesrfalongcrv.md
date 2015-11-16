---
---


# ExtrudeSrfAlongCrv
{: #kanchor1005}
{: #kanchor1004}
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/extrudesrfalongcrv.png](images/extrudesrfalongcrv.png) [Extrude Solid](extrude-solid-toolbar.html)  [Solid Editing](solid-editing-toolbar.html)  [Solid Tools](solid-tools-toolbar.html) 
Menus
Solid
Extrude Surface![images/menuarrow.gif](images/menuarrow.gif)
Along Curve
![images/history-tag.png](images/history-tag.png) [&#160;History enabled](historyenabled.html) 
The ExtrudeSrfAlongCrv command creates a solid by tracing the path of the surface edges along another path curve.
Steps
 [Select](select-objects.html) a surface.Select the path curve near the start.Your browser does not support the video tag.Note
If the curve is not planar, then it will be extruded in the z&#160;direction of the active viewport's construction plane. If the curve is planar, it will be extruded in the normal direction of the plane of the curve.Unlike [Lofts](loft.html) and [Sweeps](sweep1.html), the initial orientation of the profile curve or surface is maintained through the extrusion.If the input is a non-planar polycurve or a planar polycurve where the extrusion direction is not normal to the curve plane, the result will be a [polysurface](polysurface.html) rather than an [extrusion object](useextrusions.html) .Command-line options
Solid
If the profile curve is closed and planar, both ends of the extruded object are filled with planar surfaces and joined to make a closed polysurface.
DeleteInput
Yes
Deletes the original geometry.
No
Retains the original geometry.
SubCurve
TheSubCurveoption extrudes a curve the distance specified by picking two points along a curve.
The extruded surface starts from the beginning of the curve, not the first picked point. Picking the points only establishes the extrusion distance.
Subcurve steps
 [Select](select-objects.html) the path curve. [Pick](pick-location.html) a start along the path curve.Pick an end along the path curve.Your browser does not support the video tag.ToBoundary
Extrudes the object to a boundary surface.
See also
 [Extrude curves and surfaces](sak-extrude.html) 
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](extrudesrfalongcrv.html) 


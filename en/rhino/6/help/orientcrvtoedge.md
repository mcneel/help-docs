---
---

{: #kanchor1624}{: #kanchor1625}
# OrientCrvToEdge
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/orientcrvtoedge.png](images/orientcrvtoedge.png) [Transform](transform-toolbar.html) 
Menus
Transform
Orient![images/menuarrow.gif](images/menuarrow.gif)
Curve to Edge
The OrientCrvToEdge command copies and aligns a curve to a surface edge.
Steps
 [Select](select-objects.html) a curve near an end.Select a target surface edge. [Pick](pick-location.html) target edge points along the edge to align the curve.Your browser does not support the video tag.Command-line options
Copy
![images/history-tag.png](images/history-tag.png) [&#160;History enabled](historyenabled.html) 
The Copy option specifies whether or not the objects are copied. A plus sign![images/copyplus.png](images/copyplus.png)appears at the cursor when copy mode is on.
The [RememberCopyOptions](remembercopyoptions.html) command determines whether the selected option is used as the default.
FlipSurface
Changes the [normal direction](dir.html) of the surface.
ReverseCurve
Changes the [direction](dir.html) of the curve.
Note
If the curve already starts on the edge, it is copied to a new location on the edge with the same orientation as the original curve had to the surface.If the curve does not start on the edge, it is rotated so the picked end of the curve is tangent to the surface and perpendicular to the edge.If the curve tangent at the picked location is in the same direction as the active view's construction plane, the curve is not re-oriented to be tangent with the surface.See also
![images/orient.png](images/orient.png) [Orient](orient.html) 
Transform objects using two reference and two target points.
![images/orient3pt-orient-rt.png](images/orient3pt-orient-rt.png) [Orient3Pt](orient3pt.html) 
Transform objects using three reference and three target points.
![images/orientoncrv.png](images/orientoncrv.png) [OrientOnCrv](orientoncrv.html) 
Transform objects along a curve normal.
![images/orientonsrf.png](images/orientonsrf.png) [OrientOnSrf](orientonsrf.html) 
Transform objects normal to a surface.
 [Transform objects](sak-transform.html) 
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](orientcrvtoedge.html) 


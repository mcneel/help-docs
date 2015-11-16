---
---


# EndBulge
{: #kanchor918}
{: #kanchor917}
{: #kanchor916}
{: #kanchor915}
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/endbulge.png](images/endbulge.png) [Point Edit](point-edit-toolbar.html) 
![images/endbulge-srf.png](images/endbulge-srf.png) [Surface Tools](surface-tools-toolbar.html) 
Menus
Edit
Surface![images/menuarrow.gif](images/menuarrow.gif)
Adjust End Bulge
The EndBulge command adjusts the shape of a curve at its end or a surface near an untrimmed edge.
Steps
 [Select](select-objects.html) a curve.Select a point indicator.Drag the point indicator to a new location, and press [Enter](enter-key.html) .Your browser does not support the video tag.Command-line options
Continuity 1 / Continuity 2
Sets the continuity for each end of the curve or surface.
Your browser does not support the video tag.
Note
The EndBulge command lets you edit the shape of a curve without changing the tangent direction and the curvature of the curve. This is especially useful with curves that conform to other geometry, as with the Blend command.The curve's [control points](controlpoint.html) are constrained along a path that keeps the direction and curvature from changing.Turn on the [CurvatureGraph](curvaturegraph.html) when using EndBulge to watch the graph change while the curve is being adjusted.To edit a surface edge
 [Select](select-objects.html) a surface edge. [Pick](pick-location.html) a location on the edge you want to influence.Define a region along the edge on either side of the point you choose to edit. This region will be changed according to the adjustments, but the effect of the editing will taper off to zero at each end of the region. If you do not define a region, the adjustment is the same along the entire edge.Pick the start of the area on the edge to edit, or press [Enter](enter-key.html) to edit entire edge.Pick the end of the area.Drag control points to edit the edge bulge.Your browser does not support the video tag.Command-line options
Continuity
Sets the [continuity](continuity-descriptions.html) for the blend.
Tangency
Position and curve direction.
Curvature
Position, direction, and radius of curvature.
PreserveOtherEnd
Maintains the specified continuity at the other end of the object from the edit area.
Your browser does not support the video tag.None
No constraint.
Position
Location only.
Tangency
Position and curve direction.
Curvature
Position, direction, and radius of curvature.
See also
 [Edit objects using control points](sak-pointediting.html).
 [Edit surfaces](sak-surfacetools.html) 
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](endbulge.html) 


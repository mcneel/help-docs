---
---


# ChamferSrf
{: #kanchor267}
{: #kanchor266}
{: #kanchor265}
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/chamfersrf.png](images/chamfersrf.png) [Surfaces](surface-tools-toolbar.html) 
Menus
Surface
Chamfer Surfaces
![images/history-tag.png](images/history-tag.png) [&#160;History enabled](historyenabled.html) 
The ChamferSrf command creates a ruled surface as a bevel between two input surface edges.
Your browser does not support the video tag.Steps
 [Select](select-objects.html) the first surface.Click the surface at the side you want to keep after chamfering.Select the second surface.Click the surface at the side you want to keep after chamfering.Infinite Plane: TypeIPfor [InfinitePlane](infiniteplane.html) options.
Warning
This command works on the analogy of rolling a ball of a defined radius along the edges of the surfaces. If a corner is narrower than the ball radius, the ball cannot negotiate the turn, which can cause the command to fail.
Note
Component surfaces will be selected and unjoined from their polysurfaces.The first chamfer distance is the distance from the location where the two surfaces would intersect to the chamfer point on the first surface.The second chamfer distance is the distance from the location where the two surfaces would intersect if extended to the chamfer point on the second surface.Command-line options
Distances
The [distance](distance-pick-2pts.html) from the intersection of the surfaces to the edge of the chamfer.
Extend
Extends the chamfer surface as far as it can along surface.
Your browser does not support the video tag.Trim
 [History](history.html) only works ifTrim=No.
Yes
Trims the original surfaces to the intersections with the resulting surface.
No
Does not trim.
Split
Splits the original surfaces at the resulting surface edges.
Your browser does not support the video tag.See also
 [Fillet, blend, or chamfer between curves and surfaces](sak-fillet-blend-chamfer.html) 
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](chamfersrf.html) 


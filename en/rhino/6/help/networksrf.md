---
---

{: #kanchor1531}{: #kanchor1532}
# NetworkSrf
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/networksrf.png](images/networksrf.png) [Surface Creation](surface-creation-toolbar.html)  [Surface Sidebar](surface-sidebar-toolbar.html) 
Menus
Surface
Curve Network
![images/history-tag.png](images/history-tag.png) [&#160;History enabled](historyenabled.html) 
The NetworkSrf command creates a surface from a network of crossing curves.
All curves in one direction must cross all curves in the other direction and cannot cross each other.
Steps
 [Select](select-objects.html) curves.Your browser does not support the video tag.Command-Line Options
NoAutoSort
Turns off automatic sorting so you can select the curves manually.
Surface from Curve Network Options
Tolerances
Edge curves
Sets the tolerance for the edge curves. The edges of the surface will be within this value from the edge curves.
Interior curves
Sets the tolerance for the interior curves. The interior of the curve's surface will be within this value.
If the curves themselves are farther apart from each other than the tolerance values, the best guess is made at the surface.
Angle
If the edge curves are surface edges, and you want the surface matching the adjacent surfaces with tangency or curvature continuity, this is the accuracy used to match the surface [normals](dir.html).
Edge Matching
Determines how the edges match the input geometry.
Loose
The surface will match to the input edge curves with less accuracy.
Position / Tangency / Curvature
Sets the [continuity](continuity-descriptions.html) for the edge match.
See also
 [Create surfaces](sak-surface.html) 
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](networksrf.html) 


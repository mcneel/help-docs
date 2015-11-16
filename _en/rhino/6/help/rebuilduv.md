---
---

{: #kanchor1833}
# RebuildUV
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/rebuilduv.png](images/rebuilduv.png) [Surface Tools](surface-tools-toolbar.html) 
Menus
![images/-no-menu-item.png](images/-no-menu-item.png) [Not on menus.](menuwhattodo.html) 
The RebuildUV command reconstructs selected surfaces to a specified control point number in either the u or v&#160;directions independently.
Steps
 [Select](select-objects.html) surfaces to rebuild.Your browser does not support the video tag.Command-line options
Direction(Surfaces only)
Specify the u, v, or both [directions](curvesurfacedirection.html).
PointCount
The PointCount option specifies the number of [control points](controlpoint.html) in the result.
Type
Loose
The surface [control points](controlpoint.html) are created at the same locations as the control points of the original. This is a good option if the control points will be edited later.
Normal
The surface has an average amount of stretching between the curves. This is a good choice when the curves are proceeding in a relatively straight path or there is a lot of space between the curves.
Straight sections
Creates a ruled surface. The sections between the curves are straight.
Tight
The surface closely follows the original. This is a good choice when the input curves are going around a corner.
Uniform
Makes the object [knot vectors](knot.html) uniform.
DeleteInput
Yes
Deletes the original geometry.
No
Retains the original geometry.
CurrentLayer
The output will be on the current layer.
See also
 [Edit surfaces](sak-surfacetools.html) 
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](rebuilduv.html) 


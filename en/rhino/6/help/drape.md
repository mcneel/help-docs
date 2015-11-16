---
---


# Drape
{: #kanchor796}
{: #kanchor795}
{: #kanchor794}
{: #kanchor793}
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/drape.png](images/drape.png) [Surface Sidebar](surface-sidebar-toolbar.html)  [Surface Creation](surface-creation-toolbar.html) 
Menus
Surface
Drape
The Drape command creates a surface through points defined at the intersection of objects and points projected toward the construction plane in the current viewport.
Steps
Drag a rectangle over the objects.A surface is created that drapes over the objects.Your browser does not support the video tag.Note
Drape works over meshes, surfaces, and solids.Drape samples locations in the render depth buffer (z&#160;buffer) and then uses them for the surface control point locations. Because of this, the surface will always sag more than the original.The Drape command uses the deepest point in the view for the base level of the drape surface. It only sees mesh or render mesh objects.Command-line options
AutoSpacing
Yes
All points within the draped surface are evenly-spaced at a distance set by the Spacing option. The lower the number, the more dense the surface will be.
Spacing
Sets the [control point](controlpoint.html) spacing.
No
Controls custom spacing for the points.
U/V
Sets the number of [control points](controlpoint.html) in the surface in the u and v [directions](curvesurfacedirection.html).
AutoDetectMaxDepth
Yes
Stops the draped surface at what is automatically determined to be the farthest visible point within the rectangle.
No
Controls the custom depth setting.
MaxDepth
Sets the maximum depth the draped surface. This can be farther away from (1.0) and/or closer to the camera (0.0), providing complete or partial coverage of an object.

# DrapePt
{: #kanchor799}
{: #kanchor798}
{: #kanchor797}
{: #drapept}
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/drapept.png](images/drapept.png) [Point](point-toolbar.html) 
Menus
Curve
Point Object![images/menuarrow.gif](images/menuarrow.gif)
Drape Points
The DrapePt command creates a grid of point objects at the intersections of objects and points projected toward the construction plane in the current viewport.
Steps
Drag a rectangle over the objects to drape.A grid of points is created over the objects.Command-line options
AutoSpacing
Yes
All points within the draped surface are evenly-spaced at a distance set by the Spacing option. The lower the number, the more dense the surface will be.
Spacing
Sets the [control point](controlpoint.html) spacing.
No
Controls custom spacing for the points.
U/V
Sets the number of [control points](controlpoint.html) in the surface in the u and v [directions](curvesurfacedirection.html).
AutoDetectMaxDepth
Yes
Stops the draped surface at what is automatically determined to be the farthest visible point within the rectangle.
No
Controls the custom depth setting.
MaxDepth
Sets the maximum depth the draped surface. This can be farther away from (1.0) and/or closer to the camera (0.0), providing complete or partial coverage of an object.
See also
![images/point.png](images/point.png) [Point](point.html) 
Draw a single point object.
 [Create surfaces](sak-surface.html) 
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](drape.html) 


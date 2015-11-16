---
---

{: #kanchor1303}{: #kanchor1304}{: #kanchor1305}
# Line
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/line.png](images/line.png) [Lines](lines-toolbar.html)  [Curve Drawing](curve-drawing-toolbar.html) 
Menus
Curve
Line![images/menuarrow.gif](images/menuarrow.gif)
Single Line
Line Segments
Perpendicular from Curve
Perpendicular to 2 Curves
Tangent from Curve
Tangent to 2 Curves
Tangent, Perpendicular
Angled
Bisector
From 4 Points
Normal to Surface
Vertical to CPlane
The Line command draws one line segment.
![images/line.png](images/line.png)
Steps
 [Pick](pick-location.html) the start of the line.Pick the end of the line.Use object snaps to reference existing geometry.
Command-line options{: #line-bothsides}
BothSides
The BothSides option draws the object on both sides of the start point, creating the object twice as long as you indicate.
![images/line-bothsides.png](images/line-bothsides.png)
The BothSides option demonstrated with the [Line](#) command.
{: #normal}Normal
TheNormaloption draws the line normal to a location on a surface.
![images/line-normal.png](images/line-normal.png)
Normal steps
 [Select](select-objects.html) a surface. [Pick](pick-location.html) the start of the line on the surface.Pick the end of the line or type a length, and press [Enter](enter-key.html) .Normal option
IgnoreTrims
IfYes, surface trims are ignored. When the marker misses the untrimmed surface, the *no-access cursor* is shown.
![images/noaccesscursor.png](images/noaccesscursor.png)
No access cursor.
{: #angled}Angled
The Angled option draws the line at a specified angle from a reference line.
![images/line-angled.png](images/line-angled.png)
Angled steps
 [Pick](pick-location.html) the start of a base (reference) line.Pick the end of a base (reference) line.Type the pivot angle, and press [Enter](enter-key.html) .Pick the end of the line.{: #vertical}Vertical
The Vertical option draws the line vertical to the construction plane.
![images/line-vertical.png](images/line-vertical.png)
Vertical steps
 [Pick](pick-location.html) the start of the line.Pick the end of the line or type a length and press [Enter](enter-key.html) .{: #fourpoint}FourPoint
The FourPoint option draws the line using two points to establish direction and two points to establish length.
![images/line-4point.png](images/line-4point.png)
FourPoint steps
 [Pick](pick-location.html) the start of the base line (reference location).Pick the end of the base line (second reference location).Pick the start of the line.Pick the end of the line.{: #bisector}Bisector
The Bisector option draws the line that bisects a specified angle.
![images/line-bisector.png](images/line-bisector.png)
Bisector steps
 [Pick](pick-location.html) the start of the bisector line.Pick the start of the angle to bisect.Pick the end of the angle to bisect.Pick the end of the line or type a length, and press [Enter](enter-key.html) .{: #perpendicular}Perpendicular
The Perpendicular option draws the line perpendicular to or from a curve.
![images/line-perpendicular.png](images/line-perpendicular.png)
Perpendicular steps
 [Pick](pick-location.html) the start of the line on a curve.Pick the end of the line.Perpendicular options
Point
The Point option allows you to [pick](pick-location.html) a point that is near, but not on a curve, overriding the built-in object snap.
![images/line-perpendicular-point.png](images/line-perpendicular-point.png)
FromFirstPoint
The FromFirstPoint option forces the line to go through the first picked point on the curve instead of allowing the point to slide along the curve.
2Curves
The 2Curves option restricts the line to be perpendicular to two curves.
![images/line-perp-2crvs.png](images/line-perp-2crvs.png)
{: #tangent}Tangent
The Tangent option draws the line tangent from a curve.
![images/line-tangent.png](images/line-tangent.png)
Tangent steps
 [Pick](pick-location.html) the start of the line on a curve.Pick the end of the line.Tangent options
Point
The Point option allows you to [pick](pick-location.html) a point that is near, but not on a curve, overriding the built-in object snap.
![images/line-tangent-point.png](images/line-tangent-point.png)
FromFirstPoint
The FromFirstPoint option forces the line to go through the first picked point on the curve instead of allowing the point to slide along the curve.
2Curves
The 2Curves option restricts line to be tangent to two curves.
![images/line-tangent-2crv.png](images/line-tangent-2crv.png)
Extension
Extends a curve with a line.
![images/line-extension.png](images/line-extension.png)
Extension steps
 [Select](select-objects.html) a curve (line) near the end you want to extend.Pick the end of the line or type a distance and press [Enter](enter-key.html) .See also
 [Draw lines and curves](sak-curve.html) 
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](line.html) 


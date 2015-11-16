---
---

{: #kanchor2265}
# WireCut
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/wirecut.png](images/wirecut.png) [Solid Editing](solid-editing-toolbar.html)  [Solid Tools](solid-tools-toolbar.html) 
Menus
Solid
Solid Edit Tools![images/menuarrow.gif](images/menuarrow.gif)
Wire Cut
The WireCut command trims a polysurface with a curve similar to cutting foam with a heated wire.
Your browser does not support the video tag.Steps
 [Select](select-objects.html) the cutting curve.Select a surface or polysurface face.Infinite Plane: TypeIPfor [InfinitePlane](infiniteplane.html) options.
 [Pick](pick-location.html) the first cut depth or press [Enter](enter-key.html) to cut through the object.Your browser does not support the video tag.Pick the second cut depth, or press [Enter](enter-key.html) to cut through the object.Select the part to cut away.Command-line options
Line
Draw a cutting line instead of selecting an existing curve.
Direction (first cut)
X/Y/Z
Constrains the direction for the wire curve extrusion to world x, y, or z.
Your browser does not support the video tag.NormalToCurve
Constrains the direction for the wire curve extrusion to the curve plane normal.
Your browser does not support the video tag.CPlaneNormal
Constrains the direction for the wire curve extrusion to the construction plane z&#160;direction.
Your browser does not support the video tag.Pick
Two points establish the direction angle.
Pick steps
 [Pick](pick-location.html) a base point.Pick a second point that establishes the direction angle.Your browser does not support the video tag.AlongCurve (closed curves only)
Constrains the direction for the hole extrusion along a curve.
DeleteInput
Yes
Deletes the original geometry.
No
Retains the original geometry.
BothSides
The BothSides option draws the object on both sides of the start point, creating the object twice as long as you indicate.
![images/line-bothsides.png](images/line-bothsides.png)
The BothSides option demonstrated with the [Line](line.html) command.
Direction (second cut - open curves only)
X/Y/Z
Constrains the direction for the second cut extrusion to world x, y, or z.
NormalToFirstExtrusion
Constrains the direction for the second cut extrusion to the first cut extrusion normal.
Pick
Pick two points to specify the second cut extrusion direction.
Invert
Changes the selected and highlighted part that will be cut away and deleted from the currently highlighted part to the other part.
KeepAll
Keeps all parts of the solid.
See also
 [Split and trim curves and surfaces](sak-splittrim.html) 
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](wirecut.html) 


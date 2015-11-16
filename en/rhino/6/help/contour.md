---
---


# Contour
{: #kanchor431}
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/contour.png](images/contour.png) [Curve From Object](curve-from-object-toolbar.html) 
Menus
Curve
Curve From Objects![images/menuarrow.gif](images/menuarrow.gif)
Contour
The Contour command creates a spaced series of planar curves and points resulting from the intersection of a defined cutting planes through curves, surfaces, [polysurfaces](polysurface.html), or meshes.
Steps
 [Select](select-objects.html) objects for contour creation.Infinite Plane: TypeIPfor [InfinitePlane](infiniteplane.html) options.
 [Pick](pick-location.html) the base point.One of the contour planes will go through this point. The contour curves and points are created from the intersections of a series of invisible parallel planes cutting through the selected object.Pick a direction perpendicular to the contour planes.The contour planes will be generated in both directions from the base point and will be perpendicular to the picked direction. [Specify the distance](distance-pick-2pts.html) between contours and press [Enter](enter-key.html) .This will create contour curves where the contour planes intersect the selected surfaces and polysurfaces and points where the contour planes intersect the selected curves.Your browser does not support the video tag.Command-line options
AssignLayersBy
The AssignLayersBy option specifies the layer for the contour curves and points.
CurrentLayer
The output will be on the current layer.
InputObject
Contour curves and points will be on the same layer as the input objects.
GroupObjectsByContourPlane=Yes/No
The GroupObjectsByContourPlane option specifies whether or not contour on the same contour plane will be [grouped](group.html).
JoinCurves
The JoinCurves option specifies how contour curves created from polysurfaces will be joined.
ByPolysurface
Curves in the same contour plane created from a polysurface will be joined.
ByContourPlane
All curves in the same contour plane will be joined.
None
No curve joining.
Range
Specifies limits for the contours.
Steps
 [Select](select-objects.html) objects for contour creation. [Pick](pick-location.html) the start for the contour curves and points.Pick the end of the contour range perpendicular to the contour planes.The range line determines the direction for the contours curves.The contour planes will be perpendicular to this direction, generated from the base point to the end point. [Specify the distance](distance-pick-2pts.html) between contours and press [Enter](enter-key.html) .Contour curves are created where the contour planes intersect the objects.See also
 [Create curves from other objects](sak-curvefromobject.html) 
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](contour.html) 


---
---

{: #kanchor1915}{: #kanchor1916}{: #kanchor1917}
# Section
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/section.png](images/section.png) [Curve From Object](curve-from-object-toolbar.html) 
Menus
Curve
Curve From Objects![images/menuarrow.gif](images/menuarrow.gif)
Section
The Section command creates a planar curve or points resulting from the intersection of a defined cutting plane through objects.
Steps
 [Select](select-objects.html) objects. [Pick](pick-location.html) the start of the section plane.Infinite Plane: TypeIPfor [InfinitePlane](infiniteplane.html) options.
Pick the end of the section.Section curves and points are created by intersecting the selected objects with the section plane, which is perpendicular to the construction plane.Press [Enter](enter-key.html) when you finish creating sections.Your browser does not support the video tag.Command-line options
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
ExtendSection
TheExtendSectionoption specifies whether or not the section curves will automatically be created for all selected objects as though the drawn section plane extended through them.
See also
 [Create curves from other objects](sak-curvefromobject.html) 
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](section.html) 


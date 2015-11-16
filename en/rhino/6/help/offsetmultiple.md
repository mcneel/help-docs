---
---

{: #kanchor1555}
# OffsetMultiple
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/-no-toolbar-button.png](images/-no-toolbar-button.png) [Not on toolbars.](toolbarwhattodo.html) 
Menus
![images/-no-menu-item.png](images/-no-menu-item.png) [Not on menus.](menuwhattodo.html) 
![images/history-tag.png](images/history-tag.png) [&#160;History enabled](historyenabled.html) 
The OffsetMultiple command copies multiple curves so that all locations on the copied curves are a specified distance from the original curve.
Note
All open curves offset toward the cursor.When offsetting closed curves, if the side-to-offset point is inside a curve, the offsets for other closed curves will also be inside.Islands (closed curves inside other closed curves) are recognized and offset in the opposite direction from the container closed curves.Steps
 [Select](select-objects.html) curves and edges.Click on to specify the side.For best results, use proportionately small offset distances and smooth curves; otherwise, you may get kinks and doubled-back curves.Command-line options
Distance
Sets the offset distance.
Corner
Specifies how offset corner [continuity](continuity-descriptions.html) handled.
The Corner options only apply if the offset direction is to the "outside."
Sharp
The corners of the offset curves will be extended to meet at sharp corners with position (G0) continuity.
![images/offsetcornersharp.png](images/offsetcornersharp.png)
Round
The corners of the offset curves will be filled with arc segments with tangent (G1) continuity.
![images/offsetcornerround.png](images/offsetcornerround.png)
Smooth
The corners of the offset curves will be filled with blend segments with curvature (G2) continuity.
![images/offsetcornersmooth.png](images/offsetcornersmooth.png)
Chamfer
The corners of the offset curves will be filled with a straight line between their endpoints.
![images/offsetcornerchamfer.png](images/offsetcornerchamfer.png)
OffsetCount
Specifies the number of curves that will be offset.
See also
![images/offset.png](images/offset.png) [Offset](offset.html) 
Copy a curve parallel to the original.
![images/offsetmesh.png](images/offsetmesh.png) [OffsetMesh](offsetmesh.html) 
Copy a mesh parallel to the original.
![images/offsetcrvonsrf.png](images/offsetcrvonsrf.png) [OffsetCrvOnSrf](offsetcrvonsrf.html) 
Copy a curve on a surface parallel to the original.
![images/offsetnormal.png](images/offsetnormal.png) [OffsetNormal](offsetnormal.html) 
Copy a curve on a surface parallel to the original in the surface normal direction.
 [Create curves from other objects](sak-curvefromobject.html) 
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](offsetmultiple.html) 


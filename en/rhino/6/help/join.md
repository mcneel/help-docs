---
---

{: #kanchor1272}{: #kanchor1273}{: #kanchor1274}{: #kanchor1275}
# Join
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/join.png](images/join.png) [Curve Drawing](curve-drawing-toolbar.html)  [Geometry Fix](geometry-fix-toolbar.html)  [Main1](main1-toolbar.html)  [Popup](popup-toolbar.html)  [Solids Sidebar](solids-sidebar-toolbar.html)  [STL Tools](stl-tools-toolbar.html)  [Surface Sidebar](surface-sidebar-toolbar.html) 
Menus
Edit
Join
Shortcut
 [Ctrl](ctrl-key.html) +J
The Join command connects objects together to form a single object.
Join turns lines into polylines, curves into [polycurves](polycurve.html), surfaces and [polysurfaces](polysurface.html) into polysurfaces or solids.
Notes
Joindoes not change the surfaces. It is merely a test to see if the surfaces edges are within 2x tolerance. If they are, then they are tagged as joined and not available for further joining.The edge of a surface or mesh face can be joined to curves.You can join curves that touch end-to-end.The order the objects are selected determines the layer of the new joined object.You can join surfaces and polysurfaces that touch at [naked edges](showedges.html) .You can join meshes that do not touch ( [disjoint meshes](splitdisjointmesh.html) ).Joining does not change the underlying surface geometry. It simply "glues" adjacent objects together so meshing, Boolean operations, and intersections can cross seams without gaps.To change a surface's geometry so it fills in a gap, use [MatchSrf](matchsrf.html) or fill the gap with a new surface created by [FilletSrf](filletsrf.html), [BlendSrf](blendsrf.html), [BlendEdge](blendedge.html), [FilletEdge](filletedge.html), [NetworkSrf](networksrf.html), or [Patch](patch.html) .To change two adjacent surfaces into a single surface, use [MergeSrf](mergesrf.html). Pay special attention to the setting of the [Smooth](mergesrf.html#smooth) option to get the geometry you want.Steps
 [Select](select-objects.html) the objects (curves, surfaces, polysurfaces, or meshes) to join.Use [SelChain](selection-commands.html#selchain) to select a string of curves that touch end to end.Your browser does not support the video tag.To select objects one-by-one
 [Select](select-objects.html) an object (curve, surface, polysurface, or mesh).Select the next object.To select a surface edge as a curve to join, see [sub-object selection](selection-commands.html#sub-object-selection) .When you are finished selecting objects to join, press [Enter](enter-key.html) .Command-line options
Undo
The Undo option removes the last selected object from the join operation.
JoinDisjointMeshes
The JoinDisjointMeshes option allows joining meshes that do not touch into one object.
See: [SplitDisjointMesh command](splitdisjointmesh.html).
See also
 [Edit curves](sak-curvetools.html) 
 [Edit surfaces](sak-surfacetools.html) 
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](join.html) 


---
---


# ToNURBS
{: #kanchor2184}
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/-no-toolbar-button.png](images/-no-toolbar-button.png) [Not on toolbars.](toolbarwhattodo.html) 
Menus
![images/-no-menu-item.png](images/-no-menu-item.png) [Not on menus.](menuwhattodo.html) 
The ToNURBS command converts objects like polycurves, extrusions, meshes, SubDs, true circles and arcs, and so on, to NURBS curves, NURBS surfaces, or polysurfaces with NURBS geometry components.
Note
The ToNURBS comm and replaces the [ConvertExtrusion](convertextrusion.html) and [MeshToNURB](meshtonurb.html) command.The ToNURBS command replaces scripts that select a curve or surface, move one [control point](controlpoint.html), and put it back in the same location to convert the original curve or surface to a NURBS curve or surface.The ToNURBS command replaces the "Output=Brep" in the [SubDFromMesh](subdfrommesh.html) command.Command-line options
DeleteInputObjects
Yes
The NURBS object will replace the non-NURBS object.
No
The NURBS object will simply be added on the current layer. Both the old and new objects will be in the same location and it might be hard to pick the new/old one.
MeshOptions
If the input includes mesh objects, then MeshOptions appears on the command line. If you click on this you can set options that are applied only to mesh to NURBS:
TrimTriangularFaces
Yes
Mesh triangles will be trimmed NURBS surfaces.
No
Means mesh triangles will be singular NURBS surfaces.
SubDOptions
If the input includes SubD objects, then SubDOptions appears on the command line. If you click on this you can set options that are applied only to SubD to NURBS:
PatchDensity
The number of subdivisions to perform before creating an approximate patch at extraordinary vertices.
ClampKnots
Individual patches typically have clamped knots.
Set to No, if you need to see the [control-point](controlpoint.html) structure. The ClampKnots option is useful if you will subsequently run custom scripts that combine patches in a custom manner.
SetPatchName
Set to Yes if you want the patch object name to indicate the original face and subdivision path that resulted in the patch.
The SetPathName option is useful for custom scripts that post process the patches, and you need to know what portion of the input SubD generated the patch.
See also
For more information, see [Rhino SubD Project](https://docs.google.com/document/d/18OSiR9tC6UDSh_206nQoUsWELcOhrpLMmGWSxXfnM5Q/edit?usp=sharing).
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](tonurbs.html) 


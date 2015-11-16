---
---

{: #kanchor2289}{: #kanchor2290}{: #kanchor2291}{: #kanchor2292}{: #kanchor2293}
# Extrude curves and surfaces
Extrudes use a base curve or surface to make an open or closed shape. Extrusions can be polysurfaces or lightweight extrusion objects.
![images/extrusion-002.png](images/extrusion-002.png)
Polysurfaces (red); extrusion objects (blue).

## Lightweight extrusion objects
Light-weight extrusion objects use only a profile curve and a length as input instead of the network of isocurves normally needed for [NURBS](http://www.rhino3d.com/nurbs) objects. The [Box](box.html), [Cylinder](cylinder.html), [Tube](tube.html), [ExtrudeCrv](extrudecrv.html), and [ExtrudeSrf](extrudesrf.html) commands create extrusion objects. Extrusion objects can be closed with a planar cap or open. These objects will be converted to polysurfaces by some commands if necessary to add additional information for editing.
Lightweight extrusion objects use less memory, mesh faster, and save smaller than the traditional polysurfaces.
In models containing large numbers of extrusions represented by traditional polysurfaces, performance can be sluggish due to the relatively high demand on resources. If the same objects are made in Rhino as lightweight extrusion objects, these models are more responsive and more memory is available.
The [UseExtrusions](useextrusions.html) command controls the use of lightweight extrusion objects. To make commands that normally create extrusions create traditional polysurfaces, select thePolysurfaceoption.
Commands affected
![images/-no-toolbar-button.png](images/-no-toolbar-button.png) [UseExtrusions](useextrusions.html) 
Specifies whether extrusion objects or polysurfaces are used when extruding straight&#8209;side objects.
The [UseExtrusions](useextrusions.html) command controls the use of extrusion objects.
When [UseExtrusions](useextrusions.html) is turned on, Rhino commands that create simple solids and surfaces will use extrusion objects when possible.When [UseExtrusions](useextrusions.html) is turned off, Rhino will use surface and polysurface objects.Turning off [UseExtrusions](useextrusions.html) does not change existing extrusion objects.![images/-no-toolbar-button.png](images/-no-toolbar-button.png) [ConvertExtrusion](convertextrusion.html) 
Convert extrusion objects to surfaces and polysurfaces.
![images/-no-toolbar-button.png](images/-no-toolbar-button.png) [SelExtrusion](selection-commands.html#selextrusion) 
Select object by its object ID number.
The [SelExtrusion](selection-commands.html#selextrusion) command will not select polysurface or surface objects. Use this command if you want to see which objects are extrusion objects.
![images/-no-toolbar-button.png](images/-no-toolbar-button.png) [SelExtrusion](selection-commands.html#selextrusion) 
Select object by its object ID number.
![images/explode.png](images/explode.png) [Explode](explode.html) 
Break objects down into components.
Exploding an extrusion object results in an exploded a polysurface.
![images/mesh.png](images/mesh.png) [Mesh](mesh.html) 
Create a mesh from a NURBS surface or polysurface.
The walls of extrusion objects are always meshed with quadrangles running the length of the extrusion. The caps are generally meshed with triangles.
![images/saveas.png](images/saveas.png) [SaveAs](save.html#saveas) 
Save the current model with a different name, close the current model, and open the new model.
Extrusion objects are converted to polysurfaces when saving as Rhino 4 or earlier.
![images/-no-toolbar-button.png](images/-no-toolbar-button.png) [ConvertExtrusion](convertextrusion.html) 
Convert extrusion objects to surfaces and polysurfaces.

## Extrude curves
![images/extrudecrv.png](images/extrudecrv.png) [ExtrudeCrv](extrudecrv.html) 
Drive closed planar curves in a straight line.
![images/extrudecrvalongcrv.png](images/extrudecrvalongcrv.png) [ExtrudeCrvAlongCrv](extrudecrvalongcrv.html) 
Drive closed planar curves along a path curve.
![images/extrudecrvtapered.png](images/extrudecrvtapered.png) [ExtrudeCrvTapered](extrudecrvtapered.html) 
Drive closed planar curves in a straight line tapering at an angle.
![images/extrudecrvtopoint.png](images/extrudecrvtopoint.png) [ExtrudeCrvToPoint](extrudecrvtopoint.html) 
Drive closed planar curves tapering to a point.

## Extrude surfaces
![images/extrudesrf.png](images/extrudesrf.png) [ExtrudeSrf](extrudesrf.html) 
Drive surface edges in a straight line to create a solid.
![images/extrudesrfalongcrv.png](images/extrudesrfalongcrv.png) [ExtrudeSrfAlongCrv](extrudesrfalongcrv.html) 
Drive surface edges along a path curve to create a solid.
![images/extrudesrftapered.png](images/extrudesrftapered.png) [ExtrudeSrfTapered](extrudesrftapered.html) 
Drive surface edges in a straight line tapering at an angle to create a solid.
![images/extrudesrftopoint.png](images/extrudesrftopoint.png) [ExtrudeSrfToPoint](extrudesrftopoint.html) 
Drive surface edges tapering to a point to create a solid.

## Draw extrusions
![images/box.png](images/box.png) [Box](box.html) 
Draws a solid box.
![images/cylinder.png](images/cylinder.png) [Cylinder](cylinder.html) 
Draw a cylinder.
![images/pipe.png](images/pipe.png) [Pipe](pipe.html) 
Create a [surface](rhinoobjects.html#surfaces), [polysurface](rhinoobjects.html#polysurfaces), or [extrusion](rhinoobjects.html#lightweightextrusions) object with a circular profile around a curve.
![images/slab.png](images/slab.png) [Slab](slab.html) 
Offset a polyline, and extrude and cap the result to create a solid.

## Special case extrusions
![images/boss.png](images/boss.png) [Boss](boss.html) 
Extrude closed planar curves normal to the curve plane toward a boundary surface where the boundary surface is trimmed and joined to the extruded objects.
![images/fin.png](images/fin.png) [Fin](fin.html) 
Extrude a curve on a surface in the surface normal direction.
![images/pipe.png](images/pipe.png) [Pipe](pipe.html) 
Create a [surface](rhinoobjects.html#surfaces), [polysurface](rhinoobjects.html#polysurfaces), or [extrusion](rhinoobjects.html#lightweightextrusions) object with a circular profile around a curve.
![images/rib.png](images/rib.png) [Rib](rib.html) 
Extrude a curve in two directions to a boundary surface.
![images/ribbon.png](images/ribbon.png) [Ribbon](ribbon.html) 
Offset a curve and create a ruled surface between the curves.
![images/slab.png](images/slab.png) [Slab](slab.html) 
Offset a polyline, and extrude and cap the result to create a solid.
See also
 [Polysurfaces](sak-polysurfaces.html) 
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](sak-extrude.html) 


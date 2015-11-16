---
---


# AcadSchemes
{: #kanchor24}
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/-no-toolbar-button.png](images/-no-toolbar-button.png) [Not on toolbars.](toolbarwhattodo.html) 
Menus
![images/-no-menu-item.png](images/-no-menu-item.png) [Not on menus.](menuwhattodo.html) 
The AcadSchemes command creates AutoCAD export schemes, which determine how various Rhino objects are exported to AutoCAD .dwg and .dxf files.
These options can be saved as schemes for later use. Several schemes that have been determined to give good results are available on the Export Scheme list. You may have to experiment with the options to get the best result from your downstream application.
AutoCAD Export Schemes
Export
Select the export scheme to edit.
Default
2004 Lines
2004 Natural
2004 Polylines
2004 Solids
CAM Imperial
CAM Metric
R12 Lines &amp; Arcs
R12 Natural
General Options
AutoCAD version
When exporting curves to R12 DWG/DXF, curves are approximated with polylines. When exporting to R13/R14/2000 + DWG/DXF, you can export either polyline or spline entities.
Release 12
Release 14
Release 2000
Release 2004
Entities only
AutoCAD Release 12 DXF only.
Export surfaces as
Solids
Simple solids export to AutoCAD as 3DSolids (SAT).
Curves
The wireframe is exported as curves. Use settings on theCurvestab to specify how these and other curves are exported.
Meshes
Surfaces are exported as polyface meshes.
Use the [Create Mesh from NURBS object](mesh.html) dialog box to adjust the mesh settings.
Export meshes as
Meshes
Export meshes without modification.
3DFaces
Each face in a polygon mesh is exported as a separate [3DFace](3dface.html).
Some programs that read DXF files may read 3DFaces, but may not properly read polyface meshes.
Project to plane
Project objects to the active construction plane or the active view plane. Objects will appear on the world xy plane in the DWG/DXF file. Projecting does not automatically include silhouette lines.
For silhouette lines, see the [Silhouette](silhouette.html) and [Make2D](make2d.html) commands.
Do not project
Objects are not projected.
CPlane
Project to the active construction plane.
View
Project to the active view plane.
Export full layer paths (Parent$Child)
Export layer names only (Child)
Color by RGB
Exports colors as red, green, blue (RGB) values.
Color by AutoCAD index
Exports colors to match the AutoCAD color index.
Preserve arc normals
Keeps arc normals in their current orientation.
Flip arc normals to +Z
Flips arc normals to be mostly in the + direction of the closest world xyz coordinate.
Curves options
Rhino&#160;Objects
AutoCAD Objects
Lines
 [Lines](#polylines) 
 [Polylines](#polylines) 
 [3DPolylines](#3dpolylines) 
 [Splines](#splines) 
Arcs
 [Lines](#polylines) 
 [Arcs](#polylines) 
 [Polylines](#polylines) 
 [3DPolylines](#polylines) 
 [Polylines w/bulge arcs](#polylines-w-bulge-arcs) 
 [Splines](#splines) 
Polylines
 [Lines](#polylines) 
 [Polylines](#polylines) 
 [Polylines](#polylines) 
 [3DPolylines](#polylines) 
 [Splines](#splines) 
Curves
 [Lines](#polylines) 
 [Polylines](#polylines) 
 [Polylines](#polylines) 
 [3DPolylines](#polylines) 
 [Splines](#splines) 
Polycurves
 [Lines](#polylines) 
 [Polylines](#polylines) 
 [Polylines](#polylines) 
 [3DPolylines](#polylines) 
 [Polylines w/bulge arcs](#polylines-w-bulge-arcs) 
 [Splines](#splines) 
AutoCAD Objects
{: #polylines}Polylines
All curves are approximated with polylines before exporting. You can adjust the way polylines are created in theCurve tessellation parameters.
{: #3dpolylines}3D Polylines
Each point on the polyline can have a different z&#160;value.
{: #polylines-w-bulge-arcs}Polylines w/bulge arcs
If [polycurves](polycurve.html) with arc segments are saved asPolylinesandSimplify lines and arcsis checked, they are saved as bulge segments in the polyline. Otherwise, they are tessellated to small straight polyline segments.
{: #splines}Splines
Exporting Rhino curves as AutoCAD splines is not an option when the AutoCAD version is Release&#160;12.All curves are exported as AutoCAD spline entities.Rhino curves will be exploded upon export. Rhino polylines will export as multiple separate AutoCAD linear splines. Other Rhino compound curves will translate as separate splines.If you have mostly Rhino polylines, you will probably want to export curves as polylines. If you have mostly non-compound curves and want to have real curvature in AutoCAD, export curves as splines.Curve tessellation parameters
Maximum angle
When exporting curves as polylines, Rhino must approximate each curve with a polyline. TheMaximum anglesetting, combined with theChord heightandSegment lengthsettings, determine how the polylines are created.
TheMaximum angleoption sets the maximum angle between adjacent polyline segments. The larger this number, the farther away the polyline segment midpoints are from the original curve.
Chord height
The distance from the polyline segment midpoint to the curve will be less or equal to this number. Smaller numbers make the polyline fit the curve better, but they also increase the number of polyline segments.
Segment length
The maximum length of a polyline segment. This setting uses current model units and ensures that all polyline segments are shorter than this setting.
The physical size of the model should be taken into consideration when using this setting exporting a boat that is 100,000 units long with a maximum segment length of 0.01 will result in millions of polyline segments and a huge DWG/DXF file.
Explode polycurves
Splits [polycurves](polycurve.html) into separate splines at polycurve segment start/end points.
Split curves at kinks
Splits curves into separate splines at kinks.
Simplify lines &amp; arcs
Circles, arcs, ellipses, and lines export as AutoCAD circle, arc, ellipse, and line entities.Rhino compares each curve with an exact arc, circle, line, and ellipse and determines if it can be exported as a simple entity. If the curve is within the simplify tolerance of one of the simple entities, it is exported as a simple entity.2-D curves are simplified. This means if the curve is just one line, arc, or circle, it is exported as an AutoCAD line, arc, or circle. If there are arcs in the curve with discontinuous curvature at the ends, it is exported as a bulge arc in a polyline.3-D curves are never simplified.If [polycurves](polycurve.html) with arc or line segments are saved as splines, Rhino will save arcs and lines. Otherwise, separate splines are saved.Simplify tolerance
Rhino must evaluate each curve to determine if it is a simple entity. If a curve is within simplify tolerance of an arc, line, circle, or ellipse, it will be exported as such.If the simplify tolerance is too large, some curves may export as simple entities when they should not be.If the simplify tolerance is too small, some curves may export as simple entities when they should be.The default simplify tolerance should work well for most cases. **New** 
Creates a new scheme.
 **Save** 
Saves the currently selected scheme.
 **SaveAs** 
Saves the currently selected scheme with a new name.
 **Delete** 
Deletes the currently selected scheme.
 **Rename** 
Renames the currently selected scheme.
 **Export** 
Exports the settings to a scheme file.
 **Import** 
Imports the settings from a scheme file.
 **Close** 
Closes theAutoCAD Export Schemesdialog box.
See also
 [AutoCAD (.dwg; .dxf; .dwf) Import/Export](autocad-dwg-dxf-import-export.html) 
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](acadschemes.html) 


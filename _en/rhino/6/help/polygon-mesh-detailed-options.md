---
---


## Polygon Mesh Detailed Options
Density
Uses a formula to control how close the polygon edges are to the original surface. Values between 0 and 1. Larger values result in a mesh with a higher polygon count.
Maximum angle
Sets the maximum allowable angle between input surface normals at neighboring mesh vertices. If the angle between surface normals is greater than this setting, the mesh is further refined (more vertices are inserted) and the mesh is made denser. Two vertices are neighbors if they are at the opposite ends of a single facet edge.
The Maximum angle setting will influence the meshing of objects of the same shape in the same way regardless of the size of the objects. It will tend to make meshes denser in areas of high curvature and less dense in flatter areas.
Maximum aspect ratio
Surfaces are initially tessellated with a regular quadrangle mesh and then that mesh is refined. The initial quad mesh is constructed so that on average, the maximum aspect ratio of the quads is less than or equal to Maximum aspect ratio.
Smaller values result in slower meshing and a higher polygon count with more equilateral and nicely shaped polygons. This is approximately the maximum aspect ratio of the quads in theMinimum initial grid quads. Setting Maximum aspect ratio to zero turns off the option. Zero means no limit.
The default value for this option is zero and the suggested range, when not zero, is from 1 to 100.
This setting is scale independent.
Application
When shading long, skinny objects, use 0.0 for the this value. This allows infinite ratios. Control the smoothness of the mesh with other parameters.
Minimum edge length
If any edge is shorter than the Minimum edge length, no further division of the mesh faces occurs. This is also, approximately, the minimum edge length of the quads in the Minimum initial grid quads.
The default value for this option is 0.0001 units and the usable range depends on the size of the model. Bigger values result in faster meshing, less accurate meshes and a lower polygon count. Setting this value to zero turns off the minimum edge length option.
This option is scale dependent.
The value is always in the current unit system.
Maximum edge length
Polygons are further divided until all polygon edges are shorter than this value. This is also, approximately, the maximum edge length of the quads in theMinimum initial grid quads.
Smaller values result in slower meshing and a higher polygon count with more equally sized polygons. Setting this value to zero turns off the option.
The default value is zero and the usable range depends on the size of the model.
This option is scale dependent.
Application
Use for making sure the polygons are approximately the same size.
Maximum distance, edge to surface
Polygons divide until the distance from a polygon edge midpoint to the [NURBS](http://www.rhino3d.com/nurbs) surface is smaller than this value. This distance is also the approximate maximum distance from polygon edge midpoints to the NURBS surface in theMinimum initial grid quads.
Smaller values result in slower meshing, more accurate meshes, and a higher polygon count. Setting this value to zero turns off the option.
The default value is zero and the usable range depends on the size of the model.
Application
Use as a general polygon mesh tolerance setting.
Minimum initial grid quads
Initial mesh grid is a quad mesh Rhino creates on each [NURBS](http://www.rhino3d.com/nurbs) surface in the first stage of meshing. When the initial mesh grid is made, trim curves are ignored. After the initial grid is made, Rhino meshes all trim edges, connects the initial grid to the trim edges and then refines the mesh if theRefine meshoption is selected.
The number of quadrangles per surface in the initial mesh grid. In practice, Rhino will use at least this many polygons on each surface.
Bigger values result in slower meshing, more accurate meshes and a higher polygon count with more evenly distributed polygons. Setting this value to zero turns off the option.
The default value is 16. The suggested range is from 0 to 10000.
This option is scale independent.
Application
Use to make sure that surfaces with very subtle details are meshed with a high enough polygon count.
Refine mesh
After its initial meshing, Rhino uses a recursive process to refine the mesh until it meets the criteria defined byMaximum angle,Minimum edge length,Maximum edge length, andMaximum distance, edge to surfaceoptions.
The mesh is refined until the angle between surface normals along a polygon edge is smaller than this value. The default is 20 degrees and the suggested range is from 5 to 90 degrees. Setting Maximum angle to 0 turns off the option. Scale independent.
No refinement results in faster meshing, less accurate meshes, and lower polygon count. Clearing this checkbox also means untrimmed individual surfaces and surface areas away from trim edges and joined edges are meshed with evenly sized quadrangles.
Jagged seams
All surfaces mesh independently and Rhino does not stitch the edges of joined surface edges together. Meshes for each surface in a polysurface do not necessary meet to form a watertight mesh.
IfJagged seamsis not checked, watertight meshes are created.
This causes faster meshing, a lower polygon count and cracks between joined surfaces in the rendered image.
Application
Rhino does not support watertight quadrangle meshes unless you are meshing a single untrimmed surface. In this case, clearRefine meshand useJagged seamsto generate quadrangle meshes.
Simple planes
All planar surfaces are meshed by meshing the surface edges and then filling the area bounded by the edges with triangles.
Causes a slower meshing and a minimum polygon count on planar surface, especially for complex trimmed surfaces.
IfSimple planesis selected, the settings, exceptJagged seams, are ignored for planar surfaces and the planar surface is meshed with as few polygons as possible.
Pack Textures
 [Packs](packtextures.html) the mesh textures of the selected polysurfaces.
 **Preview** 
Click to display a preview of the output. If you change the settings, click **Preview** again to refresh the display.
 **Simple Controls** 
Opens the [Polygon Mesh Options](polygon-mesh-simple-options.html) dialog box.
 [Open topic with navigation](polygon-mesh-detailed-options.html) 


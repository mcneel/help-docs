---
---


# Create surfaces
A surface is like a rectangular stretchy rubber sheet. The NURBS form can represent simple shapes, such as planes and cylinders, as well as free-form, sculptured surfaces.
All surface creation commands in Rhino result in the same object: a NURBS surface. Rhino has many tools for constructing surfaces directly or from existing curves.
![images/surfaces-001.png](images/surfaces-001.png)
All NURBS surfaces have an inherently rectangular organization.
Even a closed surface such as a cylinder is like a rectangular piece of paper that has been rolled up so two opposite edges are touching. The place where the edges come together is called theseam. If a surface does not have a rectangular shape, either it has been trimmed or the control points on the edges have been moved.
![images/surfaces-002.png](images/surfaces-002.png)

## Closed and open surfaces
A surface can be open or closed. An open cylinder is closed in one direction.
A torus (donut shape) is closed in two directions.
![images/aboutsurfaces-001.png](images/aboutsurfaces-001.png)

## Draw a surface
![images/plane.png](images/plane.png) [Plane](plane.html) 
Draw a rectangular planar surface.
![images/picture.png](images/picture.png) [Picture](picture.html) 
Draw a rectangular planar surface with a bitmap texture.

## Create a surface from points
![images/planethroughpt.png](images/planethroughpt.png) [PlaneThroughPt](planethroughpt.html) 
Fit a rectangular planar surface through points.
![images/-no-toolbar-button.png](images/-no-toolbar-button.png) [SrfControlPtGrid](srfcontrolptgrid.html) 
Draw a surface from a grid of points that represent surface control points.
![images/srfpt.png](images/srfpt.png) [SrfPt](srfpt.html) 
Draw a surface from three or four corner points.
![images/srfptgrid.png](images/srfptgrid.png) [SrfPtGrid](srfptgrid.html) 
Draw a surface from a grid of points that lie on the surface.

## Create a surface from curves
![images/extrudecrv.png](images/extrudecrv.png) [ExtrudeCrv](extrudecrv.html) 
Drive closed planar curves in a straight line.
![images/edgesrf.png](images/edgesrf.png) [EdgeSrf](edgesrf.html) 
Create a surface from two, three, or four curves.
![images/fin.png](images/fin.png) [Fin](fin.html) 
Extrude a curve on a surface in the surface normal direction.
![images/loft.png](images/loft.png) [Loft](loft.html) 
Fit a surface through profile curves that define the surface shape.
![images/networksrf.png](images/networksrf.png) [NetworkSrf](networksrf.html) 
Fit a surface through a network of crossing curves.
![images/patch.png](images/patch.png) [Patch](patch.html) 
Fit a surface through curves and point objects.
![images/planarsrf.png](images/planarsrf.png) [PlanarSrf](planarsrf.html) 
Create a planar surface from planar curves.
![images/railrevolve.png](images/railrevolve.png) [RailRevolve](railrevolve.html) 
Revolve a profile curve around an axis and along a rail curve.
![images/revolve.png](images/revolve.png) [Revolve](revolve.html) 
Create a surface by revolving a profile curve around an axis.
![images/ribbon.png](images/ribbon.png) [Ribbon](ribbon.html) 
Offset a curve and create a ruled surface between the curves.
![images/sweep1.png](images/sweep1.png) [Sweep1](sweep1.html) 
Fit a surface through profile curves and one edge curve.
![images/sweep2.png](images/sweep2.png) [Sweep2](sweep2.html) 
Fit a surface through profile curves and two edge curves.

## Create a surface from other surfaces
![images/cutplane.png](images/cutplane.png) [CutPlane](cutplane.html) 
Create planar surfaces through objects at specified locations.
![images/drape.png](images/drape.png) [Drape](drape.html) 
Create a surface through the intersections of objects and points projected toward the construction plane.
![images/offsetsrf.png](images/offsetsrf.png) [OffsetSrf](offsetsrf.html) 
Copy a surface parallel to the original.
![images/variableoffsetsrf.png](images/variableoffsetsrf.png) [VariableOffsetSrf](variableoffsetsrf.html) 
Copy a surface specified varying distances from the original surface.
![images/unrollsrf.png](images/unrollsrf.png) [UnrollSrf](unrollsrf.html) 
Flatten (develop) a surface or polysurface with curvature in one direction to a planar surface.

## Other methods
![images/heightfield.png](images/heightfield.png) [Heightfield](heightfield.html) 
Create a surface based on gray-scale color values in an image file.
![images/meshtonurb.png](images/meshtonurb.png) [MeshToNURB](meshtonurb.html) 
Duplicate each mesh face with a NURBS surface.
![images/symmetry-crv.png](images/symmetry-crv.png) [Symmetry](symmetry.html) 
Mirror a copy of a curve or surface with continuity.
See also
 [Edit surfaces](sak-surfacetools.html) 
 [Split and trim curves and surfaces](sak-splittrim.html) 
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](sak-surface.html) 


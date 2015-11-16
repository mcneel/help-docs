---
---


# Edit curves
Curves can be edited by changing their control-point structure.

## Turn curve points on
![images/pointson.png](images/pointson.png) [PointsOn](pointson.html) 
Display curve and surface control points.
![images/pointsoff.png](images/pointsoff.png) [PointsOff](pointson.html#pointsoff) 
Turn off [control](pointson.html), [edit](pointson.html#editpton), and [solid](pointson.html#solidpton) points display.
![images/editpton.png](images/editpton.png) [EditPtOn](pointson.html#editpton) 
Display points on the curve evaluated at [knot](knot.html) averages.
![images/solidpton.png](images/solidpton.png) [SolidPtOn](pointson.html#solidpton) 
Turn on pseudo control points for polysurfaces.

## Insert or remove control points
![images/insertcontrolpoint.png](images/insertcontrolpoint.png) [InsertControlPoint](insertcontrolpoint.html) 
Add control points to a curve or a row of control points to a surface.
![images/inserteditpoint.png](images/inserteditpoint.png) [InsertEditPoint](inserteditpoint.html) 
Add edit points to a curve.
![images/insertkink.png](images/insertkink.png) [InsertKink](insertkink.html) 
Add kinks to a curve.
![images/insertknot.png](images/insertknot.png) [InsertKnot](insertknot.html) 
Add knots to curves or surfaces.
![images/removeknot.png](images/removeknot.png) [RemoveKnot](insertknot.html#removeknot) 
Delete specified knots from a curve or surface.
![images/removemultiknot.png](images/removemultiknot.png) [RemoveMultiKnot](insertknot.html#removemultiknot) 
Remove multiple knots from curves and surfaces.
![images/makeperiodic.png](images/makeperiodic.png) [MakePeriodic](makeperiodic.html) 
Remove the kink from the start/end of a curve or surface.
![images/makenonperiodic.png](images/makenonperiodic.png) [MakeNonPeriodic](makeperiodic.html#makenonperiodic) 
Insert a kink at the start/end of a curve or surface.

## Change control point structure
![images/changedegree.png](images/changedegree.png) [ChangeDegree](changedegree.html) 
Change the degree of the polynomial that defines the curve or surface by adding or subtracting control points between knot spans, while maintaining the knot structure.
![images/convert-arcs.png](images/convert-arcs.png) [Convert](convert.html) 
Change a curve to polyline or arc segments.
![images/-no-toolbar-button.png](images/-no-toolbar-button.png) [ConvertToBeziers](convert.html#converttobeziers) 
Change the structure of a NURBS object to a Bézier object.
![images/crvseam.png](images/crvseam.png) [CrvSeam](crvseam.html) 
Change the seam (start/end) location on closed curves.
![images/fair.png](images/fair.png) [Fair](fair.html) 
Remove large curvature variations in a curve while limiting the geometry changes to the specified tolerance.
![images/fitcrv.png](images/fitcrv.png) [FitCrv](fitcrv.html) 
Make a non-rational NURBS curve of a specified degree that matches the input curve to within the specified tolerance.
![images/makenonperiodic.png](images/makenonperiodic.png) [MakeNonPeriodic](makeperiodic.html#makenonperiodic) 
Insert a kink at the start/end of a curve or surface.
![images/makeperiodic.png](images/makeperiodic.png) [MakePeriodic](makeperiodic.html) 
Remove the kink from the start/end of a curve or surface.
![images/makeuniform.png](images/makeuniform.png) [MakeUniform](makeuniform.html) 
Make the object knot vectors uniform without changing the control point locations.
![images/-no-toolbar-button.png](images/-no-toolbar-button.png) [MakeUniformUV](makeuniform.html#makeuniformuv) 
Make the surface knots uniform in u or v&#160;direction.
![images/rebuild.png](images/rebuild.png) [Rebuild](rebuild.html) 
Reconstruct curves, surfaces, and extrusion objects to a specified degree and control point number.
![images/rebuildcrvnonuniform.png](images/rebuildcrvnonuniform.png) [RebuildCrvNonUniform](rebuildcrvnonuniform.html) 
Interactively modify selected curves by non-uniformly re-spacing the control points.
![images/removemultiknot.png](images/removemultiknot.png) [RemoveMultiKnot](insertknot.html#removemultiknot) 
Remove multiple knots from curves and surfaces.
![images/-no-toolbar-button.png](images/-no-toolbar-button.png) [Reparameterize](reparameterize.html) 
Recalculate an object's parameter space to match its 3-D geometry.
![images/simplifycrv.png](images/simplifycrv.png) [SimplifyCrv](simplifycrv.html) 
Replace each curve segment that has the geometry of a line or an arc with a true line or arc.
![images/smooth.png](images/smooth.png) [Smooth](smooth.html) 
Average the positions of curve and surface [control points](controlpoint.html) and mesh vertices in a specified region and evens out the spacing of selected control points in small increments to remove unwanted detail, and loops in curves and surfaces.
![images/weight.png](images/weight.png) [Weight](weight.html) 
Edit the weight of a curve or surface control point.

## Interactive editing
These commands allow interactive curve editing.
![images/fixedlengthcrvedit.png](images/fixedlengthcrvedit.png) [FixedLengthCrvEdit](fixedlengthcrvedit.html) 
Drag points on a curve to change its shape without changing the curve's length.
![images/extractsubcrv.png](images/extractsubcrv.png) [ExtractSubCrv](extractsubcrv.html) 
Separate or duplicate polycurve segments.
![images/hbar.png](images/hbar.png) [HBar](hbar.html) 
Edit a curve or surface with Bézier curve editing handles.
![images/insertcontrolpoint.png](images/insertcontrolpoint.png) [InsertControlPoint](insertcontrolpoint.html) 
Add control points to a curve or a row of control points to a surface.
![images/inserteditpoint.png](images/inserteditpoint.png) [InsertEditPoint](inserteditpoint.html) 
Add edit points to a curve.
![images/insertkink.png](images/insertkink.png) [InsertKink](insertkink.html) 
Add kinks to a curve.
![images/insertknot.png](images/insertknot.png) [InsertKnot](insertknot.html) 
Add knots to curves or surfaces.
![images/insertlineintocrv.png](images/insertlineintocrv.png) [InsertLineIntoCrv](insertlineintocrv.html) 
Flatten the curve segment between picked points.
![images/match.png](images/match.png) [Match](match.html) 
Change a curve end to meet another curve or surface edge with a specified continuity.
![images/matchcurvedir.png](images/matchcurvedir.png) [MatchCrvDir](matchcrvdir.html) 
Change a curve's direction to match another curve's direction.
![images/moveuvn.png](images/moveuvn.png) [MoveUVN](moveuvn.html) 
Move curve or surface control points along the u, v, and normal directions of the object.
![images/rebuildcrvnonuniform.png](images/rebuildcrvnonuniform.png) [RebuildCrvNonUniform](rebuildcrvnonuniform.html) 
Interactively modify selected curves by non-uniformly re-spacing the control points.
![images/removeknot.png](images/removeknot.png) [RemoveKnot](insertknot.html#removeknot) 
Delete specified knots from a curve or surface.
![images/setpt.png](images/setpt.png) [SetPt](setpt.html) 
Move objects to a specified location in the x, y, and/or z&#160;directions.
![images/softeditcrv.png](images/softeditcrv.png) [SoftEditCrv](softeditcrv.html) 
Move the surrounding curve area smoothly relative to the distance.
![images/subcrv.png](images/subcrv.png) [SubCrv](subcrv.html) 
Shorten a curve to the new picked endpoints.

## Curve analysis
These commands gather information about the structure of a curve.
![images/curve deviation.png](images/curve deviation.png) [CrvDeviation](crvdeviation.html) 
Report the maximum and minimum distances between two curves.
![images/crvend-rt.png](images/crvend-rt.png) [CrvEnd](crvstart.html#crvend) 
Place a point object at the end of a curve.
![images/crvseam.png](images/crvseam.png) [CrvSeam](crvseam.html) 
Change the seam (start/end) location on closed curves.
![images/crvstart.png](images/crvstart.png) [CrvStart](crvstart.html) 
Place a point object at the start of a curve.
![images/radius.png](images/radius.png) [Curvature](curvature.html) 
Evaluate the curvature of a curve or surface.
![images/curvaturegraph.png](images/curvaturegraph.png) [CurvatureGraph](curvaturegraph.html) 
Evaluate curve or surface curvature with a graph.
![images/direction.png](images/direction.png) [Dir](dir.html) 
Display and edit an object's normal direction.
![images/domain.png](images/domain.png) [Domain](domain.html) 
Report the domain of a curve or surface.
![images/editpton.png](images/editpton.png) [EditPtOn](pointson.html#editpton) 
Display points on the curve evaluated at [knot](knot.html) averages.
![images/extractpt.png](images/extractpt.png) [ExtractPt](extractpt.html) 
Duplicate curve control or edit points, surface control points, and mesh vertices.
![images/gcon.png](images/gcon.png) [GCon](gcon.html) 
Report the geometric continuity between two curves.
![images/radius.png](images/radius.png) [Radius](radius.html) 
Report the radius of a curve.
See also
 [Edit surfaces](sak-surfacetools.html) 
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](sak-curvetools.html) 


---
---


# FitCrv
{: #kanchor1034}
{: #kanchor1033}
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/fitcrv.png](images/fitcrv.png) [Curve Tools](curve-tools-toolbar.html) 
Menus
Curve
Curve Edit Tools![images/menuarrow.gif](images/menuarrow.gif)
Refit to Tolerance
The FitCrv command makes a non-rational [NURBS](http://www.rhino3d.com/nurbs) curve of a specified [degree](degree.html) that matches the input curve to within the specified tolerance.
Note
Generally, use this command to fit very dense or complex curves to a simpler structure.The [parameterization](parameterization.html) is chosen so that the [domain](domain.html) is approximately from 0 to the curve's length and for a parametertin the domain, the length of the sub-curve from 0 to *t* is approximately equal to *t*. [Knot](knot.html) spacing is based on the [curvature](curvature.html) of the input curve, so knots are closer together in areas of higher curvature.The resulting curve may have fewer [control points](controlpoint.html) than the input, or it may have more points if the input is simple.Steps
 [Select](select-objects.html) curves.Type a new tolerance value or press [Enter](enter-key.html) .You can also pick two points to set the tolerance.Type0(zero) to use the current [absolute tolerance](units.html#absolutetolerance) .Note
When the input to the FitCrv command is a polyline, the FitCrv command treats the polyline vertices as a list of points, and it tries to compute a curve that goes near the points but has a reasonable number of control points. The FitCrv command is meant for polylines with many closely spaced points.When the input to the FitCrv command is a control points wiggly curve with many control points, the FitCrv command tries to compute a curve that has the same general shape but fewer control points.Command-line options
DeleteInput
Yes
Deletes the original geometry.
No
Retains the original geometry.
Degree
Specifies the [degree](degree.html) of the curve (or surface).
When drawing a high-degree curve, the output curve will not be the degree you request unless there is at least one more [control point](controlpoint.html) than the degree.
OutputLayer
Specifies the layer for the results of the command.
Current
Places the results on the current layer.
Input
Places the results on the same layer as the input curve.
TargetObject
Places the results on the same layer as the target surface.
AngleTolerance
When a kink in the input curve is this angle or less from tangent, the kink will be refit smoothly, otherwise the output curve will also have a kink at that location.
See also
 [Edit curves](sak-curvetools.html) 
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](fitcrv.html) 


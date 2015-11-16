---
---


# FitSrf
{: #kanchor1036}
{: #kanchor1035}
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/fitsrf.png](images/fitsrf.png) [Surface Tools](surface-tools-toolbar.html) 
Menus
Surface
Surface Edit Tools![images/menuarrow.gif](images/menuarrow.gif)
Refit to Tolerance
The FitSrf command tries to reduce the number of surface [control points](controlpoint.html) while maintaining the surface's same general shape.
Steps
 [Select](select-objects.html) surfaces.Type a newtolerancevalue or press [Enter](enter-key.html) to accept the default.Type0(zero) to use the current [absolute tolerance](units.html#absolutetolerance) .Note
Use the FitSrf command for replacing surfaces with too many [control points](controlpoint.html) .When the input to the FitSrf command is a wiggly surface with lots of control points, the FitSrf command tries to compute a surface that has the same general shape but fewer control points.Command-line options
DeleteInput
Yes
Deletes the original geometry.
No
Retains the original geometry.
ReTrim
Trims the new fit surface with the original trimming curves.
UDegree/VDegree
The [degree](degree.html) of the surface in the [u or v&#160;direction](curvesurfacedirection.html).
OutputLayer
Specifies the layer for the results of the command.
Current
Places the results on the current layer.
Input
Places the results on the same layer as the input curve.
TargetObject
Places the results on the same layer as the target surface.
See also
 [Edit surfaces](sak-surfacetools.html) 
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](fitsrf.html) 


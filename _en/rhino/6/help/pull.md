---
---

{: #kanchor1800}{: #kanchor1801}{: #kanchor1802}
# Pull
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/pull.png](images/pull.png) [Curve From Object](curve-from-object-toolbar.html) 
Menus
Curve
Curve From Objects![images/menuarrow.gif](images/menuarrow.gif)
Pullback
![images/history-tag.png](images/history-tag.png) [&#160;History enabled](historyenabled.html) 
The Pull command creates curves and points on a surface that are the intersections of curve or points pulled toward a surface in the surface normal direction.
Steps
 [Select](select-objects.html) curves.Infinite Plane: TypeIPfor [InfinitePlane](infiniteplane.html) options.
Select the surface to pull the curves back to.Your browser does not support the video tag.Note
When exiting the command, the newly created curves will be always be selected without regard for [pre-selection](selection-commands.html#preselect) .Use the Pull command to create complex trim curves, such as a curve that goes most of the way around a cylinder.Use the [Project](project.html) command if you know what the trim curve looks like from a single viewport.Use Pull command if you know where on the surface (in 3&#8209;D) the trim path should be. Use curve commands to draw the curve, drag the [control points](controlpoint.html) or [edit points](pointson.html#editpton) to move the curve near the surface. Then, use the Pull command to pull the curve onto the surface. You can also use the [InterpCrvOnSrf](interpcrvonsrf.html) command to create a curve on a surface.When drawing the curves, use the fewest control points possible. This guarantees the smoothest possible trim curve.Command-line options
DeleteInput
Yes
Deletes the original geometry.
No
Retains the original geometry.
Loose
Pulls edit points back to the surface. If any edit point misses the surface, the curve will not be created.
OutputLayer
Specifies the layer for the results of the command.
Current
Places the results on the current layer.
Input
Places the results on the same layer as the input curve.
TargetObject
Places the results on the same layer as the target surface.
See also
 [Create curves from other objects](sak-curvefromobject.html) 
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](pull.html) 


---
---

{: #kanchor1778}{: #kanchor1779}{: #kanchor1780}{: #kanchor1781}
# Project
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/project.png](images/project.png) [Curve From Object](curve-from-object-toolbar.html)  [Main1](main1-toolbar.html) 
Menus
Curve
Curve From Objects![images/menuarrow.gif](images/menuarrow.gif)
Project
![images/history-tag.png](images/history-tag.png) [&#160;History enabled](historyenabled.html) 
The Project command creates curves or points on a surface that are the intersections of the surface and curves or points projected toward the construction plane.
Steps
 [Select](select-objects.html) curves and points to project.Select surfaces and polysurfaces.Infinite Plane: TypeIPfor [InfinitePlane](infiniteplane.html) options.
Your browser does not support the video tag.Note
You can select all the projection objects and target surfaces before starting the command.The curves are projected vertical to the construction plane that is active when the surface selection is completed.If the projection misses the selected surfaces and polysurfaces, a curve will not be created. Make sure the correct construction plane is active when you select the surfaces.The [Pull](pull.html) command will suck the curve back toward the surface by closest points. The Project command will not work in situations where you want to pull a curve onto a cylinder when the curve goes most of the way around the cylinder. Use the [Pull](pull.html) command in this case.TheProjectcommand creates complex curves that can be simplified with the [Rebuild](rebuild.html) command. You will need to be careful with the [Rebuild](rebuild.html) command and use enough points to keep the curve trimmable.TheProjectcommand can be faster than [Extrude](extrudecrv.html) followed by [Trim](trim.html) or [Split](split.html) .Smooth projection curves create smooth trim curves. Basic shapes like ellipses, circles, lines, and free-form curves work well for projection curves.Options
{: #project-loose}Loose
Projects edit points toward the construction plane onto the surface.
DeleteInput
Yes
Deletes the original geometry.
No
Retains the original geometry.
OutputLayer
Specifies the layer for the results of the command.
Current
Places the results on the current layer.
Input
Places the results on the same layer as the input curve.
TargetObject
Places the results on the same layer as the target surface.
Direction
Specifies the direction for the projection. These settings are saved during your editing session.
CPlaneZ
Projects objects in the construction plane z&#160;direction.
View
Projects objects in the view direction.
Custom
Pick two points to specify the projection direction.
See also
 [Create curves from other objects](sak-curvefromobject.html) 
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](project.html) 


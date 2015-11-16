---
---

{: #kanchor1650}{: #kanchor1651}
# Patch
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/patch.png](images/patch.png) [Surface Creation](surface-creation-toolbar.html)  [Surface Sidebar](surface-sidebar-toolbar.html) 
Menus
Surface
Patch
![images/history-tag.png](images/history-tag.png) [&#160;History enabled](historyenabled.html) 
The Patch command fits a surface through selected curves, meshes, point objects, and point clouds.
Steps
 [Select](select-objects.html) point objects, curves, and edges to base the patch on.Specify the options.Your browser does not support the video tag.Patch Surface Options
General
Sample point spacing
The physical distance along the input curve between sample points. The minimum is eight points per curve.
Surface U spans
The u [direction](curvesurfacedirection.html) span count for the automatically generated surface. This value is also used if the starting surface is a 1x1 span plane.
Surface V spans
The v [direction](curvesurfacedirection.html) span count for the automatically generated surface. This value is also used if the starting surface is a 1x1 span plane.
Stiffness
Rhino builds the patch surface by first finding the best fit plane ( [PlaneThroughPt](planethroughpt.html) ) through the selected and sampled points along curves. Then the surface deforms to match the points and sampled points. The Stiffness setting tells how much you allow the best fit plane to deform. The bigger the number, the "stiffer" and more rectangular and planar the resulting surface will be. You can test this setting with small or even very big values (&gt;1000).
Click the **Preview** button to check the result.
Adjust tangency
Match to the tangent direction of surfaces if the input curves are edges of existing surfaces.
Automatic trim
Tries to find an outside curve and trims the surface to it.
Starting surface options
Your browser does not support the video tag. **Select starting surface** 
TheSelect starting surfacebutton lets you select a surface that is similar in shape to the surface you are trying to create.
Starting surface pull
Similar to the Stiffness option, but applies to the starting surface. The greater the pull value, the closer the resulting surface shape will be to the starting surface.
Preserve edges
Clamps the edges of the starting surface in place. This is useful if you are using a curve or points for deforming an existing surface, and you do not want the edges of the starting surface to move.
Delete input
The starting surface is deleted after the new surface is made.
 **Preview** 
Displays a preview of the output.
If you change the settings, click **Preview** again to refresh the display.
Note
Try using the [Sweep2](sweep2.html) command if the Patch command does not give good results.For a trimmed patch, select curves that form a closed shape. Select them in order, so each additional curve touches one you have already selected.Select additional curves to influence the shape of the patch (such as dips or peaks in the middle of the patch). These do not have to be connected.The patch may not pass exactly through all of the input curves.If a starting surface is selected and Delete input is checked, [History](history.html) is not saved.See also
 [Create surfaces](sak-surface.html) 
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](patch.html) 


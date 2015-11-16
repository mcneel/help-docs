---
---


# FilletSrf
{: #kanchor1025}
{: #kanchor1024}
{: #kanchor1023}
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/filletsrf.png](images/filletsrf.png) [Surface Tools](surface-tools-toolbar.html)  [Main2](main2-toolbar.html) 
Menus
Surface
Fillet Surfaces
![images/history-tag.png](images/history-tag.png) [&#160;History enabled](historyenabled.html) 
The FilletSrf command creates a constant-radius round surface between two surfaces.
Steps
 [Select](select-objects.html) the first surface.Infinite Plane: TypeIPfor [InfinitePlane](infiniteplane.html) options.
Click the surface at the side you want to keep after filleting.Component surfaces will be selected and unjoined from their polysurfaces.
Component surfaces will be selected and unjoined from their polysurfaces.Select second surface.Click the surface at the side you want to keep after filleting.Your browser does not support the video tag.Warning
This command works on the analogy of rolling a ball of a defined radius along the edges of the surfaces. If a corner is narrower than the ball radius, the ball cannot negotiate the turn, which can cause the command to fail.
Tips
Always fillet from the largest radius to the smallest radius across a model.Remove any edges you can prior to filleting with [MergeAllFaces](mergeallfaces.html) or by way of surfacing in a simpler manner. Fewer intersected edges = Fewer problems as the fillet rolls along any edges and tries to trim and join with the adjacent surfaces.Make sure there is enough room for the fillet surface to trim and join with adjacent surfaces. The angle relationships between surfaces, sharpness of the bend in the rail around corners and rail type all play a part in any particular case.Command-line options
Radius
 [Specify](distance-pick-2pts.html) the fillet radius.
Extend
When one input surface is longer than the other, the fillet surface is extended to the input surface edges.
Your browser does not support the video tag.Trim
 [History](history.html) only works ifTrim=No.
Yes
Trims the original surfaces to the intersections with the resulting surface.
No
Does not trim.
Split
Splits the original surfaces at the resulting surface edges.
Your browser does not support the video tag.See also
 [Fillet, blend, or chamfer between curves and surfaces](sak-fillet-blend-chamfer.html) 
 [Rhino Wiki: Advanced Filleting](http://wiki.mcneel.com/rhino/advancedfilleting) 
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](filletsrf.html) 


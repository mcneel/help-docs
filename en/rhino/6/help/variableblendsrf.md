---
---

{: #kanchor2230}{: #kanchor2231}{: #kanchor2232}
# VariableBlendSrf
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/variableblendsrf-variablefilletsrf-rt.png](images/variableblendsrf-variablefilletsrf-rt.png) [Surface Tools](surface-tools-toolbar.html) 
Menus
Surface
Variable Fillet/Chamfer/Blend![images/menuarrow.gif](images/menuarrow.gif)
Variable Blend Surfaces
![images/history-tag.png](images/history-tag.png) [&#160;History enabled](historyenabled.html) 
The VariableBlendSrf command creates a blend surface between edges of intersecting surfaces with varying radius values, trims the original surfaces faces, and joins the resulting surfaces.
Steps
 [Select](select-objects.html) two intersecting surfaces for variable radius blend on the surfaces near the edge that will be blended.Surfaces must intersect.Handles will appear on surface edges.Infinite Plane: TypeIPfor [InfinitePlane](infiniteplane.html) options.
Press [Enter](enter-key.html) to use the default radii.Or, type a new radius distance any time theRadiusoption displays on the command line. [Specify a command line option.](specifycommandlineoption.html) OrSelect a handle to edit.Your browser does not support the video tag.Tips for using handle grips
The default handles have one grip that can be dragged to change the radius.Any added or copied handles have two grips.Use the grip on the edge to move the handle along the edge.Use the grip in the center to change the radius at the handle location.Radius/Distance options
TheRadiusandDistanceoptions appear on the command line when you drag a handle grip.
FromCurve
 [Select](select-objects.html) a curve. The radius of the curve at the picked location will be used.
FromTwoPoints
 [Pick](pick-location.html) two points to show the radius distance.
Handle options
AddHandle
Adds a handle along the edges.
CopyHandle
Adds a new handle using the distance from the selected handle.
RemoveHandle
Visible only when at least one handle has been added.
SetAll
Sets the distance or radius for all handles.
LinkHandles
Editing a single handle updates all handles.
Note
Only added handles can be removed.The default handles at the ends of each open edge segment cannot be moved or deleted. This is the minimum information the command needs in order to work.The handle at the end of a single closed edge can be moved but not deleted.RailType options
Three rail types control the intersection.
DistFromEdge
The [distance](distance-pick-2pts.html) from the edge curves determines the intersection.
Your browser does not support the video tag.RollingBall
The radius of a rolling ball determines the intersection.
Your browser does not support the video tag.DistBetweenRails
The [distance](distance-pick-2pts.html) between the edge rails determines the intersection.
Your browser does not support the video tag.TrimAndJoin
Trims and joins the resulting surface to the input surfaces.
 [History](history.html) only works if TrimAndJoin=No.
Preview
Displays a dynamic preview.
You can change the options and the preview will update.
Tips
Always blend from the largest radius to the smallest radius across a model.Remove any edges you can prior to blending with [MergeAllFaces](mergeallfaces.html) or by way of surfacing in a simpler manner. Fewer intersected edges = Fewer problems as the blend rolls along any edges and tries to trim and join with the adjacent surfaces.Make sure there is enough room for the blend surface to trim and join with adjacent surfaces. The angle relationships between surfaces, sharpness of the bend in the rail around corners, and rail type all play a part in any particular case.See also
 [Fillet, blend, or chamfer between curves and surfaces](sak-fillet-blend-chamfer.html) 
 [Rhino Wiki: Advanced Filleting](http://wiki.mcneel.com/rhino/advancedfilleting) 
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](variableblendsrf.html) 


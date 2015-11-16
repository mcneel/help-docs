---
---


# BlendEdge
{: #kanchor148}
{: #kanchor147}
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/blendedge-filletedge-rt.png](images/blendedge-filletedge-rt.png) [Solids](solid-tools-toolbar.html) 
Menus
Solid
Fillet Edge![images/menuarrow.gif](images/menuarrow.gif)
Blend Edge
The BlendEdge command creates a curvature-continuous blend surface between polysurface edges with varying radius values.
The polysurface is trimmed and joined to the blend.
Steps
 [Select](select-objects.html) edges.Select a handle.Your browser does not support the video tag.Command-line options
ShowRadius
Controls the display of the current radius in the viewport.
NextRadius
Specifies the radius for the next handle.
ChainEdges
Automatically selects curves that are touching the selected curve.
 [How to chain select edges.](howtochainselectedges.html) 
PreviousEdgeSelection
In cases where the command is canceled or ended prematurely, thePreviousEdgeSelectionoption re-selects the previously selected edges. Supports multiple sets of previously selected edges for up 20 previous edge sets.
Radius/Distance options
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
Your browser does not support the video tag.Preview
Displays a dynamic preview.
You can change the options and the preview will update.
Tips
Always blend from the largest radius to the smallest radius across a model.Use [MergeAllFaces](mergeallfaces.html) or other modeling method to remove as many edges as possible. Fewer intersected edges = Fewer problems.Make sure there is enough room for the blend surface to trim and join with adjacent surfaces.The success of the blend operation depends on the angle relationships between surfaces, the sharpness of the bend in the rail around corners, and rail type.Edit
Allows changing the radius of existing blends.
See also
 [Fillet, blend, or chamfer between curves and surfaces](sak-fillet-blend-chamfer.html) 
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](blendedge.html) 


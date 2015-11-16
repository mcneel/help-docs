---
---


# ChamferEdge
{: #kanchor264}
{: #kanchor263}
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/chamferedge.png](images/chamferedge.png) [Solid Tools](solid-tools-toolbar.html) 
Menus
Solid
Fillet Edge![images/menuarrow.gif](images/menuarrow.gif)
Chamfer Edge
The ChamferEdge command creates a ruled surface between selected polysurface edges with varying chamfer distances, trims and joins the chamfer surfaces to the surface.
Steps
 [Select](select-objects.html) edges.Select a handle.Your browser does not support the video tag.Command-line options
ShowChamferDistance
Displays the chamfer distance on the object as edges are selected.
NextChamferDistance
Sets the chamfer distance for the next edge selection.
ChainEdges
Selects surface edges that are touching the selected curve.
How to chain select
Select the first segment.ChainEdges options
AutoChain
Selecting a curve or surface edge automatically selects all curve segments connected with the level of [continuity](continuity-descriptions.html) set by the ChainContinuity option.
ChainContinuity
Controls the level of [continuity](continuity-descriptions.html) required between segments to be selected with theAutoChainoption.
Direction
Forward
Selects curves in the positive curve [direction](dir.html#normaldirection).
Backward
Selects curves in the negative curve [direction](dir.html#normaldirection).
Both
Selects curves in both the positive and negative curve [direction](dir.html#normaldirection).
GapTolerance
If the gap between two edges/curves is less than this value, the chain selection will ignore the gap and will select the next segment.
![images/gaptolerance-001.png](images/gaptolerance-001.png)
AngleTolerance
When Continuity is set to Tangency, if the angle between two edges/curves is less than this value, the chain selection will consider the criteria for continuity met and will select the next segment.
![images/angletolerance-001.png](images/angletolerance-001.png)
Undo
Undo last segment selection.
Next
Select next segment.
All
Select all segments.
Preview
Displays a dynamic preview.
You can change the options and the preview will update.
Edit
Allows changing the radius of existing chamfers.
See also
 [Fillet, blend, or chamfer between curves and surfaces](sak-fillet-blend-chamfer.html) 
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](chamferedge.html) 


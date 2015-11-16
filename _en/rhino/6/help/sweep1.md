---
---

{: #kanchor2088}{: #kanchor2089}{: #kanchor2090}
# Sweep1
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/sweep1.png](images/sweep1.png) [Surface Creation](surface-creation-toolbar.html)  [Surface Sidebar](surface-sidebar-toolbar.html) 
Menus
Surface
Sweep 1 Rail
![images/history-tag.png](images/history-tag.png) [&#160;History enabled](historyenabled.html) 
![images/creasesplitting-tag.png](images/creasesplitting-tag.png)&#160; [Crease splitting enabled](creasesplttingenabled.html) 
The Sweep1 command fits a surface through a series of profile curves that define the surface cross-sections and one curve that defines a surface edge.
Your browser does not support the video tag.Steps
 [Select](select-objects.html) a single rail curve.Select cross-section curves in the order that the surface will pass through them.Note
Select open curves near the same ends.For closed curves, adjust the curve seams.Tips
To create a single surface, the cross-section curves need to be compatible. If you use theRefit withinoption, the cross-section curves are refit with compatible cubic splines.If you do not use theRefit withinoption, the cross-section curves are made compatible by [degree](degree.html) elevation and [knot](knot.html) addition. (The original curves are not modified.) You can specify the fitting tolerance for the cross-section curves with theRefit withinoption, but the fitting tolerance for the rail curve is controlled by [Document Properties &gt; Units &gt; Absolute tolerance](units.html#absolutetolerance) .With closed rail curves, the first cross-section curve you select is added to the end of the list if you choose to create a closed surface.Command-line options
ChainEdges(rails only)
Select connected edges based on the curve continuity of the connection between segments.
To chain-select objects
Inside a command that accepts chain selection, typechain. [Select](select-objects.html) first chain segment.Chain options
AutoChain
Selecting a curve or surface edge automatically selects all curve segments connected with the level of [continuity](continuity-descriptions.html) set by theChainContinuityoption.
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
WhenContinuityis set toTangency, if the angle between two edges/curves is less than this value, the chain selection will consider the criteria for continuity met and will select the next segment.
![images/angletolerance-001.png](images/angletolerance-001.png)
Undo
Undo last segment selection.
Next
Select next segment.
All
Select all segments.
Point(cross-sections only)
ThePointoption creates a surface that begins or ends at a point. Use this option only at the start or end of the curve series.
Sweep 1 Rail Options
Frame Style
Freeform
The cross-section curve rotates to maintain its angle to the rail throughout the sweep.
Your browser does not support the video tag.Roadlike
An axis is used for calculating the 3-D rotation for the cross-section. This axis does stay constant, since the result of the calculation depends on the direction of the rail.
The orientation of the propagated shapes changes according to the rail direction.
Frames are calculated along the rail and are used to orient the cross-section curves at those locations. In a simple case with one cross-section, frames are made at the cross-section curve location and where the calculated cross-section is going to go. The 3-D rotation between those two frames determines the rotation of the cross-section curve at its new location.
The frames are made by rail-tangent cross normal of the construction plane.
 **Set axis** 
Sets the axis direction for theRoadlikeoption.
Align with surface(surface edge as rail only)
If the rail is a surface edge, the cross-section curve will twist with the surface edge. If the shapes are tangent to the surface, the new surface should also be tangent.
Your browser does not support the video tag.Align with surface on.
Your browser does not support the video tag.Align with surface off.
Sweep options
Closed sweep
TheClosed sweepoption creates a closed surface, continuing the surface past the last curve around to the first curve.
This option is only available after you select two cross-section curves.
Global shape blending
The sweep is linearly blended from one end to the other, creating sweeps that taper from one cross-section curve to the other. Otherwise, the sweep stays constant at the ends and changes more rapidly in the middle.
Your browser does not support the video tag.Global shape blending on.
Your browser does not support the video tag.Global shape bending off.
Untrimmed miters
If the sweep creates a polysurface with kinks, the component surfaces will be untrimmed.
Your browser does not support the video tag.Untrimmed Miters on.
Your browser does not support the video tag.Untrimmed Miters off.
Curve options
Refit rail
 [Refits](fitcrv.html) the rail curve before creating the sweep.
 **Align cross sections** 
Allows reversing the direction of the cross-section curves.
Do not change cross sections
Creates the sweep without altering the cross-section curves.
Rebuild cross sections with ___ control points
 [Rebuilds](rebuild.html) the cross-section curve's [control points](controlpoint.html) before creating the sweep.
Refit cross sections within ___
 [Refits](fitcrv.html) the cross-section curves before creating the sweep.
Note
To create a single surface, the cross-section curves need to be compatible. If you use theRefit cross sectionsoption, the cross-section curves are refit with compatible cubic splines. If you do not use theRefit cross sectionsoption, the cross-section curves are made compatible by [degree](degree.html) elevation and [knot](knot.html) addition. (The original curves are not modified.)You can specify the fitting tolerance for the cross-section curves with theRefit cross sectionsoption, but the fitting tolerance for the rail curve is controlled by [Document Properties &gt; Units &gt; Absolute tolerance](units.html#absolutetolerance) .With closed rail curves, the first cross-section curve you select is added to the end of the list if you choose to create a closed surface.See also
![images/sweep2.png](images/sweep2.png) [Sweep2](sweep2.html) 
Fit a surface through profile curves and two edge curves.
![images/loft.png](images/loft.png) [Loft](loft.html) 
Fit a surface through profile curves that define the surface shape.
![images/networksrf.png](images/networksrf.png) [NetworkSrf](networksrf.html) 
Fit a surface through a network of crossing curves.
 [Create surfaces](sak-surface.html) 
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](sweep1.html) 


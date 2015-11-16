---
---

{: #kanchor2037}
# SmartTrack
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/smarttrack.png](images/smarttrack.png) [Object Snap](object-snap-toolbar.html) 
Menus
Tools
Object Snaps![images/menuarrow.gif](images/menuarrow.gif)
SmartTrack
The SmartTrack command turns [SmartTrack](modeling-aids-smarttrack.html) on, off, or toggles the current state.
SmartTrack™ is a system of temporary reference lines and points that is drawn in the Rhino viewport using implicit relationships among various 3-D points, other geometry in space, and the coordinate axes' directions.
Temporary infinite lines (tracking lines) and points (smart points) are available to object snaps very much like real lines and points. You can snap to intersections of the tracking lines, perpendiculars, and directly to smart points as well as intersections of tracking lines and real curves. The tracking lines and smart points are displayed for the duration of a command.
You can add or 'capture' new points as needed up to the current maximum after which the oldest smart points disappear as new ones are added. Captured smart points can be cleared at any time if they are not proving useful.
Your browser does not support the video tag.Steps
 [Specify a command line option.](specifycommandlineoption.html) Command-line options
On
Off
Toggle

## Capture smart points
{: #capture}
Automatically
Capture smart points automatically by hovering briefly over an object snap point.Manually
Tap [Ctrl](ctrl-key.html) once to place a manual smart point anywhere in space. This makes it easy to for example to place smart points along curves.Tap [Ctrl](ctrl-key.html) twice to clear all smart points.Your browser does not support the video tag.Note
Captured smart points are drawn in their own color and styles: gray with a cross for captured, but not currently active points (that is they are not sending out any tracking lines), and blue for active smart points.Tracking lines are drawn once a smart point is captured and the cursor is in a predictable relation with the captured point(s).In this case, predictable means that the cursor is along or near an ortho line through the point, at or near the intersection between ortho lines from two smart points. Ortho tracking lines pay attention to the [OrthoAngle](ortho.html#orthoangle) setting.When a single smart point is highlighted and you see the ortho cursor with a distance, type a distance or Enter relative coordinates to place a point relative to the active smart point.See also
 [Use modeling aids](sak-modelingaids.html) 
 [SmartTrack options](modeling-aids-smarttrack.html) 
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](smarttrack.html) 


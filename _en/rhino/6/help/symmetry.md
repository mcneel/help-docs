---
---

{: #kanchor2095}{: #kanchor2096}
# Symmetry
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/symmetry-crv.png](images/symmetry-crv.png) [Curve Tools](curve-tools-toolbar.html) 
![images/symmetry.png](images/symmetry.png) [Surface Tools](surface-tools-toolbar.html) 
Menus
Transform
Symmetry
![images/history-tag.png](images/history-tag.png) [&#160;History enabled](historyenabled.html) 
The Symmetry command mirrors curves and surfaces, makes the mirrored half tangent to the original, and then when the original object is edited, the mirrored half updates to match the original.
 [History recording](history.html) must be on when the command is run.
Steps
 [Select](select-objects.html) a curve or surface.Note:
If you select the curve first, the start of the curve is changed.If you select the curve after you start the command, the end of the curve nearest to where you select is changed. [Pick](pick-location.html) the start of the symmetry plane.This is similar to the [Mirror](mirror.html) command.Pick the end of the symmetry plane.Your browser does not support the video tag.Command-line options
Continuity
Determines how the [continuity](continuity-descriptions.html) between the mirrored objects is handled.
None
No constraint.
Position
The mirrored curve or surface will connect to the original with G0 continuity.
Smooth
The mirrored curve or surface will connect to the original with G2 continuity.
See also
![images/history.png](images/history.png) [History](history.html) 
Store the connection between a command's input geometry and the result, so that when the input geometry changes, the result updates accordingly.
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](symmetry.html) 


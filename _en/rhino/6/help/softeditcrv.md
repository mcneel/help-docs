---
---

{: #kanchor2042}
# SoftEditCrv
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/softeditsrf.png](images/softeditsrf.png) [Move](move-toolbar.html)  [Transform](transform-toolbar.html) 
Menus
Curve
Curve Edit Tools![images/menuarrow.gif](images/menuarrow.gif)
Soft Edit
The SoftEditCrv command moves the curve area surrounding a selected point smoothly relative to the distance from selected point.
Note
Editing is done by moving the selected point. This location on the curve is moved, and the move is smoothly tapered off with increasing distance along the curve from this point.Use this command to fine-tune curves with many [control points](controlpoint.html) .The command takes over the moving of the control points so that the curve stays smooth. This is difficult on curves that are very dense. The falloff distance is adjustable, allowing the changes made to the curve to be more or less local.Steps
 [Select](select-objects.html) a curve. [Pick](pick-location.html) a point on the curve.Pick a point to move to.Press [Enter](enter-key.html) to end the command.Your browser does not support the video tag.Note
The selection point snaps to the closest edit point.Corresponding control points of the curve/surface are moved.Command-line options
Distance
The distance, in model units, along the curve from the editing point over which the strength of the editing falls off smoothly.
Either enter a value or click on the curve to set the distance.
Your browser does not support the video tag.Copy
The Copy option specifies whether or not the objects are copied. A plus sign![images/copyplus.png](images/copyplus.png)appears at the cursor when copy mode is on.
The [RememberCopyOptions](remembercopyoptions.html) command determines whether the selected option is used as the default.
FixEnds
Determines whether or not the position of the curve ends is fixed.
IfNoand theDistancevalue is larger than the distance to one or both ends of the curve, the end of the curve will be allowed to move.
IfYesand theDistancevalue is larger than the distance to one or both ends of the curve, the end of the curve will not be allowed to move.
With theYesoption, all control points are moved as they would be according to the normal falloff except the end control points. This can lead to an abrupt change in the curve near the end on dense curves.
Your browser does not support the video tag.See also
 [Edit curves](sak-curvetools.html) 
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](softeditcrv.html) 


---
---

{: #kanchor1046}{: #kanchor1047}
# Flow
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/flow.png](images/flow.png) [Transform](transform-toolbar.html)  [Deformation Tools](deformation-tools-toolbar.html) 
Menus
Transform
Flow along Curve
![images/history-tag.png](images/history-tag.png) [&#160;History enabled](historyenabled.html) 
The Flow command re-aligns an object or group of objects from a base curve to a target curve.
Use the Flow command to map a flat, straight shape to a curved shape, since it can be easier to draw things when they are lined up than to draw a complex shape around a curve.
Steps
 [Select](select-objects.html) objects.Select the base curve near one end.Select the target curve near the matching end.Your browser does not support the video tag.Command-line options
Copy
The Copy option specifies whether or not the objects are copied. A plus sign![images/copyplus.png](images/copyplus.png)appears at the cursor when copy mode is on.
The [RememberCopyOptions](remembercopyoptions.html) command determines whether the selected option is used as the default.
Rigid
The Rigid option specifies that individual objects will not be deformed as they are transformed.
The illustration shows the Rigid option with the Bend command.
![images/rigid-bend.png](images/rigid-bend.png)
Original objects (left), Rigid=No (center), Rigid=Yes (left).
Yes
Individual objects will not change, only their positions will change.
No
Individual objects are transformed as well as their positions.
Your browser does not support the video tag.Rigid=No.
Your browser does not support the video tag.Rigid=Yes.
Line
Draw a line to be used as the base curve.
Local
Specify circles to define a "tube" of influence around the input curve. Everything inside the tube flows. Everything outside the tube is fixed. Inside the tube wall the flow dies off.
Stretch
TheYesoption stretches or compresses objects in the curve direction so that the relationship to the target curve is the same as it is to the base curve.
TheNooption maintains the length of the objects along the curve directions.
Your browser does not support the video tag.Stretch=Yes.
Your browser does not support the video tag.Stretch=No.
PreserveStructure
Specifies whether the control-point structure of a curve or surface will be maintained after the deformation.
The PreserveStructure option does not apply to polysurfaces, and will not be displayed if polysurfaces are selected for editing.
Yes
The [control point](controlpoint.html) structure of the surface is maintained. Deformation may be less accurate if there are too few control points in on the object.
No
The objects are [refit](fitcrv.html) as needed with more [control points](controlpoint.html) to allow accurate deformation.
![images/bend-preservestructureno.png](images/bend-preservestructureno.png)PreserveStructure=Yes (left); PreserveStructure=No (right).
Your browser does not support the video tag.
PreserveStructure=No.
Your browser does not support the video tag.PreserveStructure=Yes.
See also
 [Use Universal Deformation Technology](sak-udt.html) 
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](flow.html) 


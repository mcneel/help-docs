---
---

{: #kanchor1628}{: #kanchor1629}{: #kanchor1630}{: #kanchor1631}{: #kanchor1632}
# OrientOnSrf
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/orientonsrf.png](images/orientonsrf.png) [Transform](transform-toolbar.html) 
Menus
Transform
Orient![images/menuarrow.gif](images/menuarrow.gif)
On Surface
The OrientOnSrf command moves or copies and rotates objects on a surface using the surface's normal direction for orientation.
Steps
 [Select](select-objects.html) the objects. [Pick](pick-location.html) two reference points.The first reference point defines the new origin of the reference plane.The vector created by second and first reference points defines the reference plane's x&#160;axis.In addition, the distance between the first and second reference points is used as input when scaling the objects.The z&#160;direction of the current construction plane determines the "up" direction for the object. The up direction will then follow the surface normal direction on the target surface.Select the surface.Pick target points on the surface.Infinite Plane: TypeIPfor [InfinitePlane](infiniteplane.html) options.
As you move the cursor over the surface, you will see a dynamic preview image of the transformed objects being reoriented by the varying normal direction of the surface.Your browser does not support the video tag.Command-line options
OnSurface
Sets the initial base point on the surface. This option is useful if the object is already on the target surface but must be copied or moved.
The option uses initial base points on the target surface and uses the surface normal rather construction plane normal to determine the initial orientation of the object.
Flip
Reverses the [direction](dir.html#normaldirection).
Scale
Scales the object as it orients.
Your browser does not support the video tag.Prompt
Prompts to [pick](pick-location.html) a scale a for each copy.
Uniform
Sets the same scale for the x, y, and z&#160;directions.
X/Y/Z
Sets a separate scale for each direction.
Rotation
Your browser does not support the video tag.Prompt
Prompts to [pick](pick-location.html) a rotation angle for each copy.
Angle
Specify an angle of rotation. Rotation is around the surface normal at the target point.
Copy
![images/history-tag.png](images/history-tag.png) [&#160;History enabled](historyenabled.html) 
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
Your browser does not support the video tag.See also
![images/orient.png](images/orient.png) [Orient](orient.html) 
Transform objects using two reference and two target points.
![images/orient3pt-orient-rt.png](images/orient3pt-orient-rt.png) [Orient3Pt](orient3pt.html) 
Transform objects using three reference and three target points.
![images/orientcrvtoedge.png](images/orientcrvtoedge.png) [OrientCrvToEdge](orientcrvtoedge.html) 
Copy and align a curve to a surface edge.
![images/orientoncrv.png](images/orientoncrv.png) [OrientOnCrv](orientoncrv.html) 
Transform objects along a curve normal.
 [Transform objects](sak-transform.html) 
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](orientonsrf.html) 


---
---


# CageEdit
{: #kanchor242}
{: #kanchor241}
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/cageedit.png](images/cageedit.png) [Cage](cage-toolbar.html)  [Deformation Tools](deformation-tools-toolbar.html)  [Transform](transform-toolbar.html) 
Menus
Transform
Cage Editing![images/menuarrow.gif](images/menuarrow.gif)
Cage Edit
The CageEdit command deforms objects smoothly using two-, and three-dimensional [cage](cage.html) objects.
Your browser does not support the video tag.Note
Cage editing allows smooth deformation of surfaces with dense cage [control points](pointson.html) .Polysurfaces are not broken apart at the seams by CageEdit deformation.CageEdit allows both overall deformation and partial deformation of an object.The control object can be made with the [Cage](cage.html) command or can be an existing surface or curve.To use the captive object as its own control, select an edge of same object or a face of a polysurface.History is built in regardless of the [History](history.html) setting.Steps
 [Select](select-objects.html) the captive objects (objects to edit).Select or create a control object, which defines the region to edit.Options for cage control object
BoundingBox{: #kanchor243}
The BoundingBox option uses the object bounding box to determine the box location.
Your browser does not support the video tag.BoundingBox options
See the [BoundingBox](boundingbox.html) command for detailed option descriptions.
CoordinateSystem
The coordinate system for the bounding box.
CPlane
 [Construction plane coordinates.](unit-systems.html#construction-plane-coordinates) 
World
 [World coordinates.](unit-systems.html#world-coordinates) 
3Point
 [Pick](pick-location.html) three points to establish a coordinate system.
Cage Points
TheCage Pointsoption specifies the number of cage [control points](pointson.html) and [degree](degree.html) of the cage in each direction as appropriate for the cage object.
PointCount (UV or XYZ)
Specifies the number of cage [control points](pointson.html) in each direction of the line, rectangle, or box.
Degree (UV or XYZ)
Specifies the [degree](degree.html) in each direction of the line, rectangle, or box.
Line
Draw a line to be used as the control object.
Your browser does not support the video tag.Line Cage Points
Degree
The [degree](degree.html) of the line.
PointCount
The number of cage [control points](pointson.html).
Rectangle
Draw a rectangle to be used as a control object.
Your browser does not support the video tag.Rectangle options
3Point
Draws the rectangle using two adjacent corner locations and a location on the opposite side.
Vertical
Draws the rectangle perpendicular to the construction plane.
Center
Draws the rectangle around a center point.
See the [Rectangle](rectangle.html) command for detailed option descriptions.
Cage Points
UDegree / VDegree
Sets the [degree](degree.html) of the surface in the u and v&#160;directions.
UPointCount / VPointCount
The number of cage control points in the u and v&#160;directions.
Box
Draw a box to be used as a control object.
Your browser does not support the video tag.Box options
Default
The default option draws the base rectangle using two opposite corners.
BoundingBox
Uses the object bounding box to determine the box location.
See the [BoundingBox](boundingbox.html) command for detailed option descriptions.
Diagonal
Draws the base rectangle from two diagonal corners. No option for side length is offered.
3Point
Draws the base rectangle using two adjacent corner locations and a location on the opposite side.
Vertical
Draws the base rectangle perpendicular to the construction plane.
Center
Draws the base rectangle around a center point.
See the [Box](box.html) command for detailed option descriptions.
Cage Points
Specifies the number of cage [control points](pointson.html) and [degree](degree.html) of the cage in each direction as appropriate for the cage object.
PointCount (UV or XYZ)
Specifies the number of cage [control points](pointson.html) in each direction of the line, rectangle, or box.
Degree (UV or XYZ)
Specifies the [degree](degree.html) in each direction of the line, rectangle, or box.
Deformation
Accurate
Makes the deformation slower to update and may result in denser surfaces when deformed objects are refit.
Your browser does not support the video tag.Fast
Creates surfaces that have fewer control points and are therefore less accurate.
Your browser does not support the video tag.PreserveStructure
Specifies whether the control-point structure of a curve or surface will be maintained after the deformation.
The PreserveStructure option does not apply to polysurfaces, and will not be displayed if polysurfaces are selected for editing.
Yes
Preserves the control point structure of the surface. Deformation may be less accurate if there are too few control points in on the object.
No
Refits the objects as needed with more cage control points to allow accurate deformation.
![images/bend-preservestructureno.png](images/bend-preservestructureno.png)
PreserveStructure=Yes (left); PreserveStructure=No (right).
Region to edit
Global
Deforms objects throughout 3-D space. The influence of the control object on the captives is not limited to the region inside cage objects or adjacent to control curves or surfaces. Objects that are only partly contained in cage objects are still deformed throughout. The influence of control objects is greatly magnified the farther captives are outside them.
Your browser does not support the video tag.Local
Specifies a Falloff distance from the control object to surrounding space. Captives or parts of captive objects that fall outside the falloff distance are not deformed.
Your browser does not support the video tag.Local option
Falloff distance
Controls where the cage edit is applied and controls the size of the region between the region with full effect and the region with no effect.
Three regions control editing:
The region where the cage edit has full effect (the same behavior as when no falloff option is specified). This region is the volume inside a cage box, the area in the cage rectangle, or the segment along the cage line.The region where the cage edit has no effect. Nothing is moved in this region.The region between the region of no effect and the region of full effect.Other
Define a sphere, cylinder, or box that limits the influence of the control object over the captives in space.Specify a Falloff distance.
# ReleaseFromCage
{: #releasefromcage}
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/releasefromcage.png](images/releasefromcage.png) [Cage](cage-toolbar.html) 
Menus
![images/-no-menu-item.png](images/-no-menu-item.png) [Not on menus.](menuwhattodo.html) 
The ReleaseFromCage command removes selected objects from the influence of a control object set up by the [CageEdit](#) command.
Steps
 [Select](select-objects.html) objects.Note
The [Explode](explode.html) command will change a control object into normal geometry.The [SelCaptives](selection-commands.html#selcaptives) command selects all of the objects that could be released.See also
![images/selcontrols.png](images/selcontrols.png) [SelControls](selection-commands.html#selcontrols) 
Select all cage controls.
![images/selcaptives.png](images/selcaptives.png) [SelCaptives](selection-commands.html#selcaptives) 
Select captive objects of a specified cage controls.
 [Use Universal Deformation Technology](sak-udt.html) 
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](cageedit.html) 


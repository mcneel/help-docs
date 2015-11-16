---
---

{: #kanchor1157}{: #kanchor1158}{: #kanchor1159}{: #kanchor1160}{: #kanchor1161}{: #kanchor1162}{: #kanchor1163}{: #kanchor1164}{: #kanchor1165}
# Hydrostatics
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/hydrostatics.png](images/hydrostatics.png) [Mass Properties](mass-properties-toolbar.html) 
Menus
Analyze
Mass Properties![images/menuarrow.gif](images/menuarrow.gif)
Hydrostatics
The Hydrostatics command reports hydrostatic values for surfaces and polysurfaces.
Hydrostatic values include wetted surface area, waterline length, maximum waterline beam, water plane area, and center of floatation.
Steps
 [Select](select-objects.html) surfaces or polysurfaces.Command-line options
WaterLineElevation
The water plane must always be horizontal in world coordinates. (This is a limitation of the command, not a statement of a physical principle.) Its location is defined by specifying the depth of the origin in world coordinates.
Symmetric
When only half of the model is given, the calculation results are doubled or adjusted as appropriate to represent the full model.
Longitude
The symmetry plane is either x=0 (when y is longitudinal) or y=0 (when x is longitudinal). The longitudinal direction (from bow to stern or front to back) must be either the direction of the x&#160;axis or the y&#160;axis.
Value
Volume Displacement
Volume under the water.
Center of Buoyancy
Centroid of the volume displacement.
Wetted Surface Area
Surface area under water.
Waterline Length
Length at water line. The longitudinal bounding box{: #kanchor1166}extents of the water plane area.
Maximum Waterline Beam
Maximum beam at water line. The transverse bounding box extents of the water plane section.
Water Plane Area
Area of the cross section at the water plane.
Center of Floatation
Centroid of the water plane section These are the values for the whole model even if only a half model is given.
Save As
Save the information to a file that you can use in spreadsheet programs.
Note
To get displacement information there must be no naked edges below the waterline except in the case ofSymmetric= *Yes*, in which case there can be naked edges on the symmetry plane.If the waterline falls on a singularity (place in the surface where points converge like at a pole of a sphere), the command will fail. Move the singularity point a fraction away from the water line.See also
 [Analyze an object's mass properties](sak-massproperties.html) 
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](hydrostatics.html) 


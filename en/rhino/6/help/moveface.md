---
---

{: #kanchor1495}{: #kanchor1496}
# MoveFace
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/moveface.png](images/moveface.png) [Solid Editing](solid-editing-toolbar.html)  [Solid Tools](solid-tools-toolbar.html) 
Menus
Solid
Solid Edit Tools![images/menuarrow.gif](images/menuarrow.gif)
Faces![images/menuarrow.gif](images/menuarrow.gif)
Move Face
The MoveFace command moves a polysurface face.
The surrounding joined surfaces are adjusted to accommodate the new face orientation.
Faces on relatively simple polysurfaces such as boxy planar shapes can be moved to adjust things like wall locations in a building or planes in a mechanical part.
Steps
 [Select](select-objects.html) a face. [Pick](pick-location.html) a point to move from.Pick a point to move to.Your browser does not support the video tag.Notes
The surrounding joined surfaces are adjusted to accommodate the new face shape and orientation.All adjusted faces must be either planar or easy to stretch (extruded surfaces in the direction of stretch).Holes in the adjusted faces generally do not move or stretch.Command-line options
DirectionConstraint
None
The face can be moved any direction.
Normal
the face can only be moved in the positive or negative [normal](dir.html) direction.
ToBoundary
The face is moved until the side surfaces intersect the boundary object and the face itself is replaced by a trimmed section of the boundary object.
Your browser does not support the video tag.
DeleteBoundary
Determines whether or not the boundary is deleted after the move.
See also
 [Move objects](sak-move.html) 
 [Edit solid objects](sak-solidtools.html) 
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](moveface.html) 


---
---


# Smash
{: #kanchor2040}
{: #kanchor2039}
{: #kanchor2038}
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/smash.png](images/smash.png) [Surface Tools](surface-tools-toolbar.html) 
Menus
Surface
Smash
The Smash command flattens a surface without restriction to single-directional curvature.
Note
Makes an approximate 2-D development of surfaces that have compound curvature.This command can be used to deal with fabrics that have a certain amount of flexibility and stretch.The Smash command is a modified version of the [UnrollSrf](unrollsrf.html) command. With [UnrollSrf](unrollsrf.html), the surface has to be linear in one direction to unroll, and with the Smash command it does not.Since it is not possible to flatten a double-curved object (like a half a coconut shell) to get a paper pattern, the answer is always inaccurate to some degree. This command is useful if the object you are flattening is not extremely curved and you want to make the pattern out of a stretchy material like rubber.Steps
 [Select](select-objects.html) surfaces or polysurfaces.Select curves on the surface.Your browser does not support the video tag.Command-line options
LinearDirection
Natural
Allows the command to choose one direction to be the straight one.
U
Select the surface u&#160; [direction](curvesurfacedirection.html) as the linear (straight) direction.
V
Select the surface v&#160; [direction](curvesurfacedirection.html) as the linear (straight) direction.
Explode
Yes
The resulting surfaces are not joined.
No
The resulting surfaces are joined along the same edges that were joined in the original polysurface.
Your browser does not support the video tag.Labels
Determines whether or not matching numbered dots are placed on the edges of the selected object and the resulting objects.
Your browser does not support the video tag.KeepProperties
Determines whether or not the selected object's [properties](properties.html) are copied to the resulting object.
See also
![images/unrollsrf.png](images/unrollsrf.png) [UnrollSrf](unrollsrf.html) 
Flatten (develop) a surface or polysurface with curvature in one direction to a planar surface.
![images/-no-toolbar-button.png](images/-no-toolbar-button.png) [Squish](squish.html) 
Flatten a non-developable (curved in two directions) 3-D mesh or NURBS surface into a flat 2-D pattern.
 [Flatten curves and surfaces](sak-flatten.html) 
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](smash.html) 


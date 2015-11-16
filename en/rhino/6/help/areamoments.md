---
---


# AreaMoments
{: #kanchor113}
{: #kanchor112}
{: #kanchor111}
{: #kanchor110}
{: #kanchor109}
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/areamoments.png](images/areamoments.png) [Mass Properties](mass-properties-toolbar.html) 
Menus
Analyze
Mass Properties![images/menuarrow.gif](images/menuarrow.gif)
Area Moments
The AreaMoments command reports the [area moments of inertia](http://en.wikipedia.org/wiki/Moment_of_inertia) and corresponding axes of surfaces, polysurfaces, meshes, or closed planar curves with respect to the world coordinate system.
Note
The area moments of inertia compute on the entire collection of objects. For example, if you select a box polysurface, the area moments will compute using all six sides of the box.To analyze the area moments of a surface that is part of the polysurface, either extract the surface from the polysurface using the [ExtractSrf](extractsrf.html) command or use the [sub-object selection](selection-commands.html#sub-object-selection) when selecting the surface.For mass properties analysis, it is frequently convenient to model a real-world solid, like a boat hull made from thin steel plate with a surface or open polysurface. TheAreaMomentscommand can estimate the volume moments of this shell without having to actually create the boat hull as a complete thin-walled solid.Steps
 [Select](select-objects.html) curves, surfaces, or polysurfaces.See also
 [Measure objects](sak-measure.html) 
 [Analyze an object's mass properties](sak-massproperties.html) 
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](areamoments.html) 


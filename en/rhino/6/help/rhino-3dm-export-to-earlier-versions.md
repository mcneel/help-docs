---
---

{: #kanchor3012}{: #kanchor3013}{: #kanchor3014}{: #kanchor3015}
# Rhino (.3dm) Export to Earlier Versions
Opening Rhino files
The current version of Rhino will open files from any previous Rhino version and Rhino backup files (.3dm.bak and .3dmbak).
To save a model as an earlier Rhino file:
From theFilemenu, clickExport SelectedorSave As.In the dialog box, in theSave as typebox, select the Rhino version.In theFilename box, type a file name.Saving as Rhino 5
Saving as Rhino 4
When saving to Rhino 4 files, the following changes take place:
 [Extrusion objects](sak-extrude.html) are saved as polysurfaces (but not lost).Some of the annotation objects lose enhanced V5 information.Minor things like display order, Gumball user data, and so on.Saving as Rhino 3
When saving as Rhino 3, the following changes take place:
Layers, materials, and object attributes are saved in simpler V3 formats.The following data is not saved:
History information.Advanced texture mapping information.Custom display information.User data.Saving as Rhino 2
When saving as Rhino 2, the following changes take place:
Objects that contain non- [NURBS](http://www.rhino3d.com/nurbs) geometry (spheres, cylinders, arcs, circles, etc.) are converted into NURBS objects. Sometimes this results in some less precise trimming curves. In particular, some geometry does not round trip to Rhino 2 and back.Layers, materials, and object attributes are saved in simpler V2 formats.Point clouds are exploded into single points.Blocks are exploded into their component geometry.The following data is not saved:Annotation.Render meshes and analysis meshes.History informationAdvanced texture mapping information.Custom display information.User data.&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](rhino-3dm-export-to-earlier-versions.html) 


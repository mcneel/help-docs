---
---


# CullDegenerateMeshFaces
{: #kanchor495}
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/culldegeneratemeshfaces.png](images/culldegeneratemeshfaces.png) [Mesh Tools](mesh-tools-toolbar.html) 
Menus
Mesh
Mesh Edit Tools![images/menuarrow.gif](images/menuarrow.gif)
Cull Degenerate Mesh Faces
The CullDegenerateMeshFaces command deletes mesh faces that have 0 area.
Note
Some STL/SLA printers have problems if meshes contain many long, thin facets. These can slow the printer's slicing process down, produce odd printed results, and run the printer out of memory.The [MeshRepair](meshrepair.html) command may be useful when tuning up meshes for STL/SLA printing.Steps
 [Select](select-objects.html) mesh objects.If any vertices are orphaned in the process, they are also removedSee also
 [Edit mesh objects](sak-meshtools.html) 
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](culldegeneratemeshfaces.html) 


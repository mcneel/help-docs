---
---


# Collapse mesh faces and vertices
These commands assist in repairing mesh objects to make them watertight.
Note
Some STL/SLA printers have problems if meshes contain many long, thin facets. These can slow the printer's slicing process down, produce odd printed results, and run the printer out of memory.The [MeshRepair](meshrepair.html) command may be useful when tuning up meshes for STL/SLA printing.![images/collapsemeshedge.png](images/collapsemeshedge.png) [CollapseMeshEdge](collapsemeshedge.html) 
Move mesh edge [vertices](meshvertex.html) to a single vertex.
![images/collapsemeshface.png](images/collapsemeshface.png) [CollapseMeshFace](collapsemeshface-commands.html) 
Move all mesh face [vertices](meshvertex.html) to a single vertex.
![images/collapsemeshfacesbyarea.png](images/collapsemeshfacesbyarea.png) [CollapseMeshFacesByArea](collapsemeshface-commands.html#collapsemeshfacesbyarea) 
Move all mesh face [vertices](meshvertex.html) to a single vertex based on face area.
![images/collapsemeshfacesbyaspectratio.png](images/collapsemeshfacesbyaspectratio.png) [CollapseMeshFacesByAspectRatio](collapsemeshface-commands.html#collapsemeshfacesbyaspectratio) 
Move all mesh face [vertices](meshvertex.html) to a single vertex based on face aspect ratio.
![images/collapsemeshfacesbyedgelength.png](images/collapsemeshfacesbyedgelength.png) [CollapseMeshFacesByEdgeLength](collapsemeshface-commands.html#collapsemeshfacesbyedgelength) 
Move all [mesh face vertices](meshvertex.html) to a single vertex based on face edge length.
![images/collapsemeshvertex.png](images/collapsemeshvertex.png) [CollapseMeshVertex](collapsemeshvertex.html) 
Move a [mesh vertex](meshvertex.html) to an adjacent mesh vertex.
See also
 [Extract object sub-elements](sak-extract.html) 
 [Edit mesh objects](sak-meshtools.html) 
 [White paper: Scan, Cleanup, Remodel](http://download.rhino3d.com/download.asp?id=ScanCleanupRemodel) 
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](sak-collapsemesh.html) 


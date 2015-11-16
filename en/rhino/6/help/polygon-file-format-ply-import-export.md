---
---

{: #kanchor3047}
# Polygon (.ply) import/export
Stores data from 3-D scanners as a list of nominally flat polygons.

## Import
To open, import, insert, and attach a file as a worksession
From theFilemenu, click [Open](open.html) or [Import](import.html) .In theOpendialog box, select the supported file type.If the import can be configured, click **Options** to specify import settings.ClickOpen, or press [Enter](enter-key.html) .When Rhino opens a non-3dm model, the title bar reflects the name of the model that was opened. When the model is saved for the first time, this model name is entered as the file name.
## Export
To save as or export a Rhino model
From theFilemenu, click [Export Selected](export.html) or [Save As](save.html#saveas) .In the dialog box, theFiles of typelist displays the currently supported file types for export.In theFiles of typebox, select the supported file type.In theFile namebox, select or type a file name.Specify what is to be saved.Save small
Though clearing the render meshes makes the file smaller, it will shade and render more slowly the next time you open the file.
Save geometry only
Saves geometry objects only. No layers, materials, properties, notes, or units settings are saved.
This is similar to exporting the objects. A new file is made, but it does not become your active Rhino model.
Save Textures
Embeds external textures used by materials, environments and decals into the model.
Save plugin data
Saves data attached to objects or the document by plug-in applications.
If the export can be configured, click **Options** to specify export settings.If the file type creates only mesh objects, in the [Polygon Mesh Objects](polygon-mesh-simple-options.html) dialog box, specify the mesh settings.PLY Export Options
ASCII/Binary
Export vertex normals
Vertex normals are the normalized average of the normals of the faces that contain that [vertex](meshvertex.html). The average can be weighted by the area of the face or it can be unweighted. Vertex normals are used in Gouraud shading, Phong shading, and other lighting models.
Export vertex colors
Exports color data assigned to a mesh vertex.
Export object material
Exports the [material](material.html) name assigned to the object.
Mesh vertex
The location where the edges of the mesh faces meet. The [mesh vertex](meshvertex.html) (plural *vertices* ) contains x, y, and z&#160;coordinates and may contain a vector normal, a color value, and texture coordinates.
Always use these settings. Do not show this dialog again.
Saves the current settings and turns off the dialog display.
To turn the message back on
Click **Options** in the appropriate [Save](save.html), [Export](export.html), [Open](open.html), [Import](import.html), or [Insert](insert.html) dialog box.See also
 [Wikipedia: PLY (file format)](http://en.wikipedia.org/wiki/PLY_(file_format)) 
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](polygon-file-format-ply-import-export.html) 


---
---

{: #kanchor3068}{: #kanchor3069}
# VRML (.vrml, .wrl) import/export
VRML (Virtual Reality Modeling Language) is a standard file format for representing 3-D interactive vector graphics, designed particularly with the World Wide Web in mind. It has been superseded by X3D.

## Import
To open, import, insert, and attach a file as a worksession
From theFilemenu, click [Open](open.html) or [Import](import.html) .In theOpendialog box, select the supported file type.If the import can be configured, click **Options** to specify import settings.ClickOpen, or press [Enter](enter-key.html) .When Rhino opens a non-3dm model, the title bar reflects the name of the model that was opened. When the model is saved for the first time, this model name is entered as the file name.Note
Only VRML 2 files can be imported.Spotlights, point lights and directional lights import.
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
If the export can be configured, click **Options** to specify export settings.If the file type creates only mesh objects, in the [Polygon Mesh Objects](polygon-mesh-simple-options.html) dialog box, specify the mesh settings.VRML Export Options
Version
Try 2.0 first. If it does not work with your VRML viewer, try 1.0.
1.0
2.0
Options
Vertex normals
Only the polygon mesh vertex normals calculated from the [NURBS](http://www.rhino3d.com/nurbs) surfaces export to the VRML file. This may improve the appearance of the objects in the viewer, and it will make the file much larger.
Texture coordinates
The uv texture mapping coordinates are exported to the VRML file.
Vertex colors
In order to get vertex colors to export select a mesh with vertex colors such as a mesh imported from VRML or an mesh with the [ExtractAnalysisMesh](extractanalysismesh.html) command.
Always use these settings. Do not show this dialog again.
Saves the current settings and turns off the dialog display.
To turn the message back on
Click **Options** in the appropriate [Save](save.html), [Export](export.html), [Open](open.html), [Import](import.html), or [Insert](insert.html) dialog box.Note
The default Top view is exported.Render color, shine, and transparency determine the render material properties exported to the VRML file.The render background color exports as a background color to VMRL2.Spotlights, point lights and directional lights export.Material names assigned to objects in [Material Properties](material.html) export.Some VRML clients are incompatible with the material shininess (specularity) set to zero. Using Cortona and Cosmo Player, objects with shininess set to zero shade completely white. If the shininess is zero, Rhino sets the shininess to something bigger than zero (we used 1, but the value does not matter) and the specular color to black. The Black specular color results in a matte surface in the VRML viewer.Texture assignments are not exported.See also
 [Wikipedia: VRML](http://en.wikipedia.org/wiki/VRML) 
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](vrml-vrml-import-export.html) 


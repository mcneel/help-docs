---
---

{: #kanchor2984}
# 3D Studio (.3ds) import/export
Import and export to the .3ds format, one of the file formats used by the [Autodesk 3ds Max](http://en.wikipedia.org/wiki/Autodesk_3ds_Max) 3-D modeling, animation and rendering software.
Rhino does not support files with the extension .max.
The specification of the .max format is not public. Since the content of the file is heavily dependent on the plug-in data used to build the scene, parsing the file outside of 3ds Max makes little sense.
See [CG Society 3ds Max File Formats](http://wiki.cgsociety.org/index.php/3ds_Max_File_Formats).

## Import
To open, import, insert, and attach a file as a worksession
From theFilemenu, click [Open](open.html) or [Import](import.html) .In theOpendialog box, select the supported file type.If the import can be configured, click **Options** to specify import settings.ClickOpen, or press [Enter](enter-key.html) .When Rhino opens a non-3dm model, the title bar reflects the name of the model that was opened. When the model is saved for the first time, this model name is entered as the file name.3DS Import Options
Unweld ___ degrees
The minimum angle between mesh polygon normals where unwelding of points should occur.
Always use these settings. Do not show this dialog again.
Saves the current settings and turns off the dialog display.
To turn the message back on
Click **Options** in the appropriate [Save](save.html), [Export](export.html), [Open](open.html), [Import](import.html), or [Insert](insert.html) dialog box.Import notes
3DS files contain polygon mesh objects. Polygon mesh objects import into Rhino as polygon mesh objects. They do not convert to [NURBS](http://www.rhino3d.com/nurbs) .Rhino can read [texture mapping coordinates](texturemapping.html) from 3DS files.
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
If the export can be configured, click **Options** to specify export settings.If the file type creates only mesh objects, in the [Polygon Mesh Objects](polygon-mesh-simple-options.html) dialog box, specify the mesh settings.Export notes
3DStudio export uses exact object names whenever possible.If the object name in Rhino is: *RhinoObjectName*, 3DS export uses the first 10 characters of the name, because MAX and 3DS only support object names up to 10 characters. The result of this example is:RhinoObjecRhino then checks whether or not the object name has already been used. If so, the object name is truncated to 6 characters and a 3- digit index is added, like this: *RhinoO_010* The index is the last three digits from the mesh counter used in the exporter.If no object name is defined, Rhino uses a generic name: *Obj_000010.* In this case, the index is the last six digits from the mesh counter.See also
 [Wikipedia: .3DS](http://en.wikipedia.org/wiki/.3DS) 
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](3dstudio-3dsimportexport.html) 


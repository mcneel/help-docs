---
---

{: #kanchor3020}{: #kanchor3021}{: #kanchor3022}{: #kanchor3023}{: #kanchor3024}
# MotionBuilder (.fbx) import/export
Autodesk FBX asset exchange technology used for Autodesk content creation packages—Autodesk 3ds Max, Autodesk Maya, Autodesk MotionBuilder, Autodesk Mudbox, and Autodesk Softimage software.

## Import
To open, import, insert, and attach a file as a worksession
From theFilemenu, click [Open](open.html) or [Import](import.html) .In theOpendialog box, select the supported file type.If the import can be configured, click **Options** to specify import settings.ClickOpen, or press [Enter](enter-key.html) .When Rhino opens a non-3dm model, the title bar reflects the name of the model that was opened. When the model is saved for the first time, this model name is entered as the file name.FBX Import Options
Submit a bug report if unsupported objects are detected in the file
Unsupported objects may appear. If you would be willing to submit a bug report when these objects are detected, check this box.
Import Notes
Reads polygon meshes with associated materials and textures.Limited support for NURBS curves and surfaces.Poses, skeletons, and takes are not read because Rhino doesn't have any way to represent them. [NURBS](http://www.rhino3d.com/nurbs) objects and patches are currently not imported.
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
If the export can be configured, click **Options** to specify export settings.If the file type creates only mesh objects, in the [Polygon Mesh Objects](polygon-mesh-simple-options.html) dialog box, specify the mesh settings.FBX Export Options
Export NURBS objects as
NURBS
Meshes only
Export materials as
Lambert
Phong
Export file as
Version 7 binary
Version 7 ascii
Version 6 binary
Version 6 ascii
Always use these settings. Do not show this dialog again.
Saves the current settings and turns off the dialog display.
To turn the message back on
Click **Options** in the appropriate [Save](save.html), [Export](export.html), [Open](open.html), [Import](import.html), or [Insert](insert.html) dialog box.Export Notes
Exports meshes with materials and textures.Limited support for [NURBS](http://www.rhino3d.com/nurbs) curves and surfaces.See also
 [Autodesk FBX](http://www.autodesk.com/products/motionbuilder/overview) 
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](motionbuilder-fbx-import-export.html) 


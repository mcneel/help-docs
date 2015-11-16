---
---

{: #kanchor3016}
# LightWave (.lwo) import/export
LightWave is used for rendering animated and static 3-D images.
Note
Rhino imports line and point objects from LightWave.Rhino breaks apart objects into separate meshes and sorts them into layers by surface type.LightWave files contain polygon mesh objects. They are not converted to [NURBS](http://www.rhino3d.com/nurbs).
## Import
To open, import, insert, and attach a file as a worksession
From theFilemenu, click [Open](open.html) or [Import](import.html) .In theOpendialog box, select the supported file type.If the import can be configured, click **Options** to specify import settings.ClickOpen, or press [Enter](enter-key.html) .When Rhino opens a non-3dm model, the title bar reflects the name of the model that was opened. When the model is saved for the first time, this model name is entered as the file name.LWO Import Options
Unweld ___ degrees
The minimum angle between mesh polygon normals where unwelding of points should occur.
Always use these settings. Do not show this dialog again.
Saves the current settings and turns off the dialog display.
To turn the message back on
Click **Options** in the appropriate [Save](save.html), [Export](export.html), [Open](open.html), [Import](import.html), or [Insert](insert.html) dialog box.
## Export
Export Notes
LWO only exports mesh or meshable (surfaces, polysurfaces, etc.) objects, NOT curves, polylines, points, etc.Use the [ExtractControlPolygon](extractcontrolpolygon.html) command to convert smooth Rhino surfaces into polygon meshes that you can convert into MetaNURBS objects in LightWave.Object names will be used when exporting the LightWave file instead of a generic name.To save as or export a Rhino model
From theFilemenu, click [Export Selected](export.html) or [Save As](save.html#saveas) .In the dialog box, theFiles of typelist displays the currently supported file types for export.In theFiles of typebox, select the supported file type.In theFile namebox, select or type a file name.Specify what is to be saved.Save small
Though clearing the render meshes makes the file smaller, it will shade and render more slowly the next time you open the file.
Save geometry only
Saves geometry objects only. No layers, materials, properties, notes, or units settings are saved.
This is similar to exporting the objects. A new file is made, but it does not become your active Rhino model.
Save Textures
Embeds external textures used by materials, environments and decals into the model.
Save plugin data
Saves data attached to objects or the document by plug-in applications.
If the export can be configured, click **Options** to specify export settings.If the file type creates only mesh objects, in the [Polygon Mesh Objects](polygon-mesh-simple-options.html) dialog box, specify the mesh settings.LWO Export Options
Version 5 or earlier (65535 points maximum)
If exporting to a version of LightWave version 5 or earlier, the LightWave file is limited to 65,535 points for the entire file. Export large Rhino models in pieces or export as [OBJ file format](wavefront-obj-import-export.html), which does not have the 65,000 polygon limitation.
Version 6 or later
No point limitation.
Always use these settings. Do not show this dialog again.
Saves the current settings and turns off the dialog display.
To turn the message back on
Click **Options** in the appropriate [Save](save.html), [Export](export.html), [Open](open.html), [Import](import.html), or [Insert](insert.html) dialog box.See also
 [LightWave 3D](http://en.wikipedia.org/wiki/LightWave) 
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](lightwave-lwo-import-export.html) 


---
---

{: #kanchor2988}
# AMF (.amf) Import/Export
Additive Manufacturing File Format (AMF) is an open standard for describing objects for additive manufacturing processes such as 3&#8209;D printing. The official standard is an XML-based format designed to allow any computer-aided design software to describe any 3&#8209;D object to be fabricated on any 3&#8209;D printer. Unlike its predecessor [STL](stereolithography-stl-import-export.html) format, AMF has native support for color and materials.

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
If the export can be configured, click **Options** to specify export settings.If the file type creates only mesh objects, in the [Polygon Mesh Objects](polygon-mesh-simple-options.html) dialog box, specify the mesh settings.See also
 [Wikipedia: Additive Manufacturing File Format](http://en.wikipedia.org/wiki/Additive_Manufacturing_File_Format) 
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](amf-import-export.html) 


---
---

{: #kanchor3074}{: #kanchor3075}
# Windows Metafile (.wmf/.emf) export
Windows Metafile (WMF) is a graphics file format intended to be portable between applications and may contain both vector graphics and bitmap components.
{: #enhanced-metafile}Enhanced Metafile (EMF), a newer version with additional commands is a 32-bit format that can contain both vector information and bitmap information.
This format is an improvement over the Windows Metafile Format and contains extended features, such as the following:
Built-in scaling informationBuilt-in descriptions that are saved with the fileImprovements in color palettes and device independenceThe EMF format is an extensible format, which means that a programmer can modify the original specification to add functionality or to meet specific needs. This modification can lead to incompatibilities between different types of EMF pictures.To save as or export a Rhino model
From theFilemenu, click [Export Selected](export.html) or [Save As](save.html#saveas) .In the dialog box, theFiles of typelist displays the currently supported file types for export.In theFiles of typebox, select the supported file type.In theFile namebox, select or type a file name.Specify what is to be saved.Save small
Though clearing the render meshes makes the file smaller, it will shade and render more slowly the next time you open the file.
Save geometry only
Saves geometry objects only. No layers, materials, properties, notes, or units settings are saved.
This is similar to exporting the objects. A new file is made, but it does not become your active Rhino model.
Save Textures
Embeds external textures used by materials, environments and decals into the model.
Save plugin data
Saves data attached to objects or the document by plug-in applications.
If the export can be configured, click **Options** to specify export settings.If the file type creates only mesh objects, in the [Polygon Mesh Objects](polygon-mesh-simple-options.html) dialog box, specify the mesh settings.In theOptionsdialog box, specify the [print settings](print.html) .Note
Curves are exported as a 2-D snapshot from the active viewport.Surfaces and solids are exported as a polyline wireframe and curves as polylines.See also
 [Wikipedia: Windows Metafile](http://en.wikipedia.org/wiki/Windows_Metafile).
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](windows-metafile-wmf-emf-export.html) 


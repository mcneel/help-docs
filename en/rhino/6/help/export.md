---
---


# Export
{: #kanchor938}
{: #kanchor937}
{: #kanchor936}
{: #kanchor935}
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/export.png](images/export.png) [File](file-toolbar.html)  [Popup](popup-toolbar.html)  [Standard](standard-toolbar.html) 
Menus
File
Export Selected
The Export command saves selected objects to a new Rhino (or other supported format) file.
Steps
 [Select](select-objects.html) objects to export.Type a file name.ClickSave.
## Export to a different file type
To save as or export a Rhino model
From theFilemenu, click [Export Selected](#) or [Save As](save.html#saveas) .In the dialog box, theFiles of typelist displays the currently supported file types for export.In theFiles of typebox, select the supported file type.In theFile namebox, select or type a file name.Specify what is to be saved.Save small
Though clearing the render meshes makes the file smaller, it will shade and render more slowly the next time you open the file.
Save geometry only
Saves geometry objects only. No layers, materials, properties, notes, or units settings are saved.
This is similar to exporting the objects. A new file is made, but it does not become your active Rhino model.
Save Textures
Embeds external textures used by materials, environments and decals into the model.
Save plugin data
Saves data attached to objects or the document by plug-in applications.
If the export can be configured, click **Options** to specify export settings.If the file type creates only mesh objects, in the [Polygon Mesh Objects](polygon-mesh-simple-options.html) dialog box, specify the mesh settings.Command-line options
Save small
Though clearing the render meshes makes the file smaller, it will shade and render more slowly the next time you open the file.
Save geometry only
Saves geometry objects only. No layers, materials, properties, notes, or units settings are saved.
This is similar to exporting the objects. A new file is made, but it does not become your active Rhino model.
Save Textures
Embeds external textures used by materials, environments and decals into the model.
Save plugin data
Saves data attached to objects or the document by plug-in applications.

# Related commands

## ExportWithOrigin
{: #kanchor941}
{: #kanchor940}
{: #kanchor939}
{: #exportwithorigin}
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/exportwithorigin.png](images/exportwithorigin.png) [File](file-toolbar.html) and [Block](block-toolbar.html) 
Menus
File
Export With Origin
TheExportWithOrigincommand saves selected objects to a new Rhino .3dm file with a specified origin and construction plane.
Steps
 [Pick](pick-location.html) an insertion base point on the model that will become the world origin of the new file, or press [Enter](enter-key.html) to use the current model world origin (0,0,0).In theExportdialog box, type a file name.ClickSave.The objects in the resulting file have the same relationship to the world top construction plane as the original objects had to their original construction plane active during the export.Command-line options
Save small
Though clearing the render meshes makes the file smaller, it will shade and render more slowly the next time you open the file.
Save geometry only
Saves geometry objects only. No layers, materials, properties, notes, or units settings are saved.
This is similar to exporting the objects. A new file is made, but it does not become your active Rhino model.
Save Textures
Embeds external textures used by materials, environments and decals into the model.
Save plugin data
Saves data attached to objects or the document by plug-in applications.
See also
 [Import and export objects](sak-importexport.html) 
 [Index of import/export file types](-index-of-import-export-file-types.html) 
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](export.html) 


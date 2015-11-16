---
---

{: #kanchor3026}{: #kanchor3027}{: #kanchor3028}{: #kanchor3029}{: #kanchor3030}{: #kanchor3031}
# Object Properties (.csv) export
Creates a comma-delimited text file in CSV (comma-separated value) that contains a tabulation of various [object properties](properties.html) including layer name, layer color, object name, object render color and selected mass properties. The text file is created in a way that makes it easy to import information into spreadsheet programs.
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
If the export can be configured, click **Options** to specify export settings.If the file type creates only mesh objects, in the [Polygon Mesh Objects](polygon-mesh-simple-options.html) dialog box, specify the mesh settings.CSV Export Options
General
Include header line
When exporting to a spreadsheet, a column heading line will be created.
Layer information
 [Layer name](layer.html#name) 
 [Layer color](layer.html#current) 
Layer index
The creation order number of the layer.
Include hierarchy
Exclude the parent layer name and use only the short layer name.
Object information
 [Object name](properties.html#name) 
 [Object ID](properties.html#details) 
 [Object description](properties.html#object-type) 
 [Object color](properties.html#displaycolor) 
 [Object material](material.html) 
Note: A render material of –1 means the object or layer has not been assigned a render material and therefore uses Rhino’s default render material.
Surround point coordinates with double-quotes
Mass properties
 [Length](length.html) 
 [Area](area.html) 
 [Area centroid](areacentroid.html) 
 [Area moments](areamoments.html) 
Perimeter
 [Volume](volume.html) 
 [Volume centroid](volumecentroid.html) 
 [Volume moments](volumemoments.html) 
 [Cumulative mass properties](massproperties.html) 
User text
 [Attributes Keys](rhinoscripting.html#setusertext-toattributes) 
 [Attributes Texts](rhinoscripting.html#setusertext-toattributes) 
 [Object Keys](rhinoscripting.html#setusertext-toobject) 
 [Object Texts](rhinoscripting.html#setusertext-toobject) 
Always use these settings. Do not show this dialog again.
Saves the current settings and turns off the dialog display.
To turn the message back on
Click **Options** in the appropriate [Save](save.html), [Export](export.html), [Open](open.html), [Import](import.html), or [Insert](insert.html) dialog box.&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](object-properties-csv-export.html) 


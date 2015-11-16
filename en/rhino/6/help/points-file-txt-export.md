---
---

{: #kanchor3041}{: #kanchor3042}{: #kanchor3043}{: #kanchor3044}{: #kanchor3045}{: #kanchor3046}
# Points File (.txt) Export
Saves points to a delimited text file.
Note
Both point coordinates and RGB color values (x,y,z,r,g,b) are exported.For point objects, the color is taken from the point object's color.For point cloud objects, if the point cloud has point colors, these colors are used. Otherwise, all points use the point cloud object's color.To save as or export a Rhino model
From theFilemenu, click [Export Selected](export.html) or [Save As](save.html#saveas) .In the dialog box, theFiles of typelist displays the currently supported file types for export.In theFiles of typebox, select the supported file type.In theFile namebox, select or type a file name.Specify what is to be saved.Save small
Though clearing the render meshes makes the file smaller, it will shade and render more slowly the next time you open the file.
Save geometry only
Saves geometry objects only. No layers, materials, properties, notes, or units settings are saved.
This is similar to exporting the objects. A new file is made, but it does not become your active Rhino model.
Save Textures
Embeds external textures used by materials, environments and decals into the model.
Save plugin data
Saves data attached to objects or the document by plug-in applications.
If the export can be configured, click **Options** to specify export settings.If the file type creates only mesh objects, in the [Polygon Mesh Objects](polygon-mesh-simple-options.html) dialog box, specify the mesh settings.TXT Export Options
Delimiter
Comma
Uses commas as delimiters.
Semicolon
Uses semicolons as delimiters.
Space
Uses spaces as delimiters.
Tab
Uses tab characters as delimiters.
Other
Uses characters you specify as delimiters.
General
___ Significant digits
Rounds values to the number of significant digits you specify.
Surround values with double-quotes
Places double-quote marks around each value.
Always use these settings. Do not show this dialog again.
Saves the current settings and turns off the dialog display.
To turn the message back on
Click **Options** in the appropriate [Save](save.html), [Export](export.html), [Open](open.html), [Import](import.html), or [Insert](insert.html) dialog box.&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](points-file-txt-export.html) 


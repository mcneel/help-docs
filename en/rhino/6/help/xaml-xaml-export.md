---
---

{: #kanchor3077}
# Extensible Application Markup Language (.xaml) export
Exports 3-D meshes a to an xaml (Extensible Application Markup Language) file for web applications that use [SilverLight](http://www.microsoft.com/silverlight/).
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
If the export can be configured, click **Options** to specify export settings.If the file type creates only mesh objects, in the [Polygon Mesh Objects](polygon-mesh-simple-options.html) dialog box, specify the mesh settings.XAML Export Options
Use render meshes
Uses the [render mesh](extractrendermesh.html) if one exists in the model.
Add rotation scrollbars
Adds slider bars to rotate the model.
Use origin for rotation center
Rotates the model around 0,0,0.
Add rotation animation
X Axis / Y Axis / Z Axis
Rotates the model about the x, y, or z axis.
Always use these settings. Do not show this dialog again.
Saves the current settings and turns off the dialog display.
To turn the message back on
Click **Options** in the appropriate [Save](save.html), [Export](export.html), [Open](open.html), [Import](import.html), or [Insert](insert.html) dialog box.See also
 [Wikipedia: Extensible Application Markup Language](http://en.wikipedia.org/wiki/Extensible_Application_Markup_Language).
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](xaml-xaml-export.html) 


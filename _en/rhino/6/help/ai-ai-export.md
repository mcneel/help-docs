---
---

{: #kanchor2987}
# Adobe Illustrator (.ai) Export
Exports or saves to Adobe Illustrator (.ai) format.
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
If the export can be configured, click **Options** to specify export settings.If the file type creates only mesh objects, in the [Polygon Mesh Objects](polygon-mesh-simple-options.html) dialog box, specify the mesh settings.AI Export Options
Scale
You cannot preserve the scale and units from a perspective viewport.
Snapshot of current view
Rhino exports the curves as a 2-D snapshot from the active viewport.
Preserve model scale
Sets the scale factor and units you want to use.
Color
RGB
Red, Green, Blue color system.
CMYK
Cyan, Magenta, Yellow, Black color system.
Options
Export viewport boundary
Exports a rectangle that corresponds to the current viewport boundary. It is useful for registering curves to renderings or screen captures taken in the same view.
Hatches exported as solid fills
If checked, hatches export to as solid fills.
If unchecked, hatches export as lines.
Always use these settings. Do not show this dialog again.
Saves the current settings and turns off the dialog display.
To turn the message back on
Click **Options** in the appropriate [Save](save.html), [Export](export.html), [Open](open.html), [Import](import.html), or [Insert](insert.html) dialog box.Note
Before exporting, position the objects in the active viewport the way you want them to fit the page in the illustration program.Rhino exports text and dimensions to AI files.Rhino exports [NURBS](http://www.rhino3d.com/nurbs) geometry and polygon meshes as wireframe curves.Curves have fewer [control points](controlpoint.html) than the original because the Adobe Illustrator file format only supports non-rational cubic Bézier curves. Rational curves or curves higher than degree 3 are approximated with a cubic Bézier.If you draw curves using the free-form curve tools degree 3 or lower and export them from the top view, they won't get refit and will look exactly the same in Adobe Illustrator.Hatches export into AI as closed paths with standard solid fills.See also
 [Wikipedia: Adobe Illustrator Artwork](http://en.wikipedia.org/wiki/Adobe_Illustrator_Artwork) 
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](ai-ai-export.html) 


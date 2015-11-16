---
---

{: #kanchor2985}{: #kanchor2986}
# ACIS (.sat) Export
Exports solids-based geometry to [Spatial's](http://www.spatial.com/) ACIS .sat native file format.
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
If the export can be configured, click **Options** to specify export settings.If the file type creates only mesh objects, in the [Polygon Mesh Objects](polygon-mesh-simple-options.html) dialog box, specify the mesh settings.Always use these settings. Do not show this dialog again.
Saves the current settings and turns off the dialog display.
To turn the message back on
Click **Options** in the appropriate [Save](save.html), [Export](export.html), [Open](open.html), [Import](import.html), or [Insert](insert.html) dialog box.ACIS Export Type
Default
ACIS version: 4.0Curves are not exportedCurve knots and surface knots are clampedClosed surfaces are split
ACIS Version 1.5
ACIS Version: 1.5Exports curvesCurve knots and surface knots are clampedClosed surfaces are split
ACIS Version 2.0
ACIS Version: 2.0Exports curvesCurve knots and surface knots are clampedClosed surfaces are split
ACIS Version 3.0
ACIS Version: 3.0Exports curvesCurve knots and surface knots are clampedClosed surfaces are split
ACIS Version 4.0
ACIS Version: 4.0Exports curvesCurve knots and surface knots are clampedClosed surfaces are split
AutoCAD
ACIS Version: 4.0Exports curvesCurve knots and surface knots are clampedClosed surfaces are split
Mechanical Desktop
ACIS Version: 4.0Exports curvesCurve knots and surface knots are clampedClosed surfaces are split
Inventor
ACIS Version: 4.0Does not export curvesCurve knots and surface knots are clampedClosed surfaces are split
Inventor does not read any ACIS object that is not a legitimate solid.
SOLIDWORKS
ACIS Version: 4.0Does not export curvesCurve knots and surface knots are clampedClosed surfaces are split
SOLIDWORKS ignores anything that is not a surface or a solid.
Note
There are various file types that save Rhino files as SAT files. All of the version types can export curves, but not all programs based on ACIS can import curves.Hidden geometry is skipped.See also
 [Wikipedia: ACIS](http://en.wikipedia.org/wiki/ACIS) 
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](acis-sat-export.html) 


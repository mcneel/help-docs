---
---

{: #kanchor3033}{: #kanchor3034}{: #kanchor3035}{: #kanchor3036}
# Parasolid (.x_t) Export
Parasolid is a geometric modeling kernel.
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
If the export can be configured, click **Options** to specify export settings.If the file type creates only mesh objects, in the [Polygon Mesh Objects](polygon-mesh-simple-options.html) dialog box, specify the mesh settings.X_T Export Options
Default
 [Edgecam](http://www.edgecam.com/) 
 [Mastercam](http://www.mastercam.com/) 
 [Solid Edge](http://www.plm.automation.siemens.com/en_us/products/velocity/solidedge/overview/index.shtml) 
 [SOLIDWORKS](http://www.solidworks.com/) 
Always use these settings. Do not show this dialog again.
Saves the current settings and turns off the dialog display.
To turn the message back on
Click **Options** in the appropriate [Save](save.html), [Export](export.html), [Open](open.html), [Import](import.html), or [Insert](insert.html) dialog box.Note
Parasolid files are always in meters. If Rhino units are set to a real-world unit other than meters, the exported geometry will be scaled by the appropriate factor.In general, your model's objects should be joined solids that have no naked edges. Use the [Properties](properties.html) command to ensure your models are closed solids, and the [ShowEdges](showedges.html) command to ensure there are no naked edges.Simple planes are supported as Parasolid primitives. A simple plane is one that is defined in Rhino as four [control points](controlpoint.html) arranged in a rectangle. Planes are important primitives. Many feature-based modelers (SOLIDWORKS in particular) only allow sketching on planar surfaces defined by a plane primitive.See also
 [Wikipedia: Parasolid](http://en.wikipedia.org/wiki/Parasolid).
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](parasolid-x-t-export.html) 


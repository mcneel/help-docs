---
---

{: #kanchor3056}{: #kanchor3057}{: #kanchor3058}
# RenderMan (.rib) Export
A .rib file consists of Pixar RenderMan ASCII language commands.
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
If the export can be configured, click **Options** to specify export settings.If the file type creates only mesh objects, in the [Polygon Mesh Objects](polygon-mesh-simple-options.html) dialog box, specify the mesh settings.Note
Rhino uses the active view for the RIB export. Make sure the correct view is active when you export.Rhino spotlights are exported to RIB. The intensity is always set to 1, the beam distribution to 2 (these are shader defaults).Assign a material name to an object in [Material Properties](material.html). Rhino exports this material name for use by the renderer.Object names are exported to make it easier to identify surfaces in the RIB file. Use the [Properties](properties.html) command to set the object names.A name attribute definition is inserted before each light.The transparency color is the color of the object.When rendered with default settings, a Rhino-compliant spotlight shader makes the RIB scenes look very close to Rhino scenes.Rhino writes the surface, color, and opacity statement for each object. This makes it easier to parse the RIB file and replace the settings if necessary.Exporting to the RIB file format does not replace the Rhino search paths, but rather appends the existing paths. This makes it possible to define custom search paths in .rendribrc.Export to RIB file format supports render background color.See also
 [Pixar's RenderMan](https://renderman.pixar.com/view/renderman) 
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](renderman-rib-export.html) 


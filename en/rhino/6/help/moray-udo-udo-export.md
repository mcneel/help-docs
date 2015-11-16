---
---

{: #kanchor3019}
# Moray UDO (.udo) export
Moray is an interactive shareware wireframe modeler for the PC platform, supporting [POV-Ray](pov-ray-pov-export.html) 3.5.
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
Moray supports object names. Moray UDO export uses the first 40 characters of a stringlayer_name_object_name. The 40-character limitation is defined in the POV-Ray specifications. If multiple objects share one name, Moray UDO automatically numbers the objects.Use this format if you want to define POV-Ray textures, and if you want to set other POV -Ray specific information in Moray UDO.When you export to Moray UDO, Rhino creates a .udo file and a .inc file. Exporting the .udo file to &amp;/Moray For Windows/PovScn/ folder seems to help you avoid the hassle of having to move the .inc file before rendering.To import the object into Moray UDO, from the MorayCreatemenu, clickUser Defined.The wireframe view in Moray UDO is a line approximation of the wireframe you see in Rhino.See also
 [Moray](http://www.stmuc.com/moray/) 
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](moray-udo-udo-export.html) 


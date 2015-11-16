---
---

{: #kanchor3065}{: #kanchor3066}{: #kanchor3067}
# Stereolithography (.stl) import/export
STL files describe only the surface geometry of a three dimensional object without any representation of color, texture or other common CAD model attributes.
STL files contain polygon mesh objects. Polygon mesh objects import into Rhino as polygon mesh objects. They are not converted to [NURBS](http://www.rhino3d.com/nurbs).

## Import
To open, import, insert, and attach a file as a worksession
From theFilemenu, click [Open](open.html) or [Import](import.html) .In theOpendialog box, select the supported file type.If the import can be configured, click **Options** to specify import settings.ClickOpen, or press [Enter](enter-key.html) .When Rhino opens a non-3dm model, the title bar reflects the name of the model that was opened. When the model is saved for the first time, this model name is entered as the file name.STL Import Options
Weld angle ___ degrees
The angle at which the automatic weld will be performed.
Split disjoint meshes
Determines whether disjoint pieces of a mesh will be automatically split up on import.
See: [SplitDisjointMesh](splitdisjointmesh.html).
STL model units
If the STL file has units saved, they will be displayed.
Current Rhino units
Displays the units in the current file. This applies only to the [Import](import.html) and [Insert](insert.html) commands. The [Open](open.html) command displays Rhino units asNone.
If the Rhino file and the file being imported have different units, the imported model geometry will be scaled accordingly.
Always use these settings. Do not show this dialog again.
Saves the current settings and turns off the dialog display.
To turn the message back on
Click **Options** in the appropriate [Save](save.html), [Export](export.html), [Open](open.html), [Import](import.html), or [Insert](insert.html) dialog box.
## Export
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
If the export can be configured, click **Options** to specify export settings.If the file type creates only mesh objects, in the [Polygon Mesh Objects](polygon-mesh-simple-options.html) dialog box, specify the mesh settings.{: #stl-mesh-export-options}STL Mesh Export Options
Tolerance
The maximum distance between the original object and the polygon mesh created for the STL file.
 **Preview** 
Displays a preview of the output.
If you change the settings, click **Preview** again to refresh the display.
 ** [Detailed Controls](polygon-mesh-detailed-options.html) ** 
STL Export Options
File type
Binary
Ascii
Export open objects
 ** [Adjust Mesh](#stl-mesh-export-options) ** 
STL Export Warning
If the STL mesh is not closed, a warning dialog appears.
 **Export Anyway** 
Saves the open mesh.

### STL mesh export diagnostics
For some rapid prototyping machines, STL files must contain completely closed (watertight) polygon mesh objects.
You might want to do this to ensure that the meshes really do fit together before exporting them for use in an expensive STL job.
To test for watertightness
 [Join](join.html) the mesh objects.Conceptually, this command gets all the triangles into one bag, but it doesn't glue the edges together. (The situation is similar to having surfaces that all fit together but have not been joined into a solid.) [Weld](weld.html) the new mesh object.At theAngle toleranceprompt type180.An angle tolerance of 180 tells the [Weld](weld.html) command to glue adjacent triangle points together no matter what. [UnifyMeshNormals](unifymeshnormals.html) .This changes all the triangles so they are oriented the same way, that is, if two triangles share an edge, then they have the same idea of up.To see if the result has any holes or gaps, type [SelNakedMeshEdgePt](selection-commands.html#selnakedmeshedgept) .If a mesh point is highlighted, then it is part of a "naked" triangle edge.To avoid generating very large mesh files
Start with the [Mesh](mesh.html) command, which has the same controls as the render mesh controls found in [Mesh Document Properties](mesh.html). The difference is that the [Mesh](mesh.html) command, however, produces a polygon mesh you can export. You would get the same controls by exporting the Rhino geometry to STL, but in general it is preferable to make the mesh object as a separate operation and export that.The settings that work best for STL will vary, but a good place to start is to go to clear theMaximum Anglesetting and theMaximum Aspect Ratiosetting completely. Set theMaximum distance edge to surfacesetting (which is the desired maximum distance between the midpoint of any edge of a polygon and the true surface) to something around the resolution of the rapid prototyping machine. About .005 inch (.125mm) might be a good number to start with. It may be that once you have determined which are the best settings for your projects and rapid prototyping machine, this procedure may become superfluous. Instead you may just want to export the [NURBS](http://www.rhino3d.com/nurbs) objects directly and use your proven mesh settings when the object is converted to polygons during export.Once the mesh is generated, you can hide the [NURBS](http://www.rhino3d.com/nurbs) object and inspect the mesh using the [FlatShade](flatshade.html) command. This will show you a shaded view of the polygons without the smoothing tricks used by normal shaded views. If the mesh looks good, export the mesh to the STL file. If not, delete the mesh and try different mesh settings.It is best to only change one setting at a time to see the effects of that setting. It is best to only change one setting at a time to see the effects of that setting. If the mesh is fine enough but some areas do not work, tryMaximum aspect ratioto something between 4 and 7. It is generally not worth settingMaximum distance edge to surfaceto much below the resolution of the rapid prototyping machine.See also
 [Wikipedia: STL (file format)](http://en.wikipedia.org/wiki/STL_(file_format)) 
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](stereolithography-stl-import-export.html) 


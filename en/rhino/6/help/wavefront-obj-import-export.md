---
---

{: #kanchor3071}{: #kanchor3072}{: #kanchor3073}
# OBJ (.obj) import/export
The OBJ file format is a simple data-format that represents 3-D geometry alone include only the position of each vertex, the UV position of each texture coordinate vertex, normals, and the faces that make each polygon defined as a list of vertices, and texture vertices. Vertices are stored in a counter-clockwise order by default, making explicit declaration of normals unnecessary.

## Import
To open, import, insert, and attach a file as a worksession
From theFilemenu, click [Open](open.html) or [Import](import.html) .In theOpendialog box, select the supported file type.If the import can be configured, click **Options** to specify import settings.ClickOpen, or press [Enter](enter-key.html) .When Rhino opens a non-3dm model, the title bar reflects the name of the model that was opened. When the model is saved for the first time, this model name is entered as the file name.OBJ Import Options
Import OBJ groups as
Nothing
Groups
Layers
Object names
Import OBJ objects
Import as morph target only
Reverse group order
Ignore textures
Map OBJ Y to Rhino Z
Split 32-bit textures into separate files
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
If the export can be configured, click **Options** to specify export settings.If the file type creates only mesh objects, in the [Polygon Mesh Objects](polygon-mesh-simple-options.html) dialog box, specify the mesh settings.OBJ Export Options
Save objects as
NURBS
Rhino curves and surfaces export as [NURBS](http://www.rhino3d.com/nurbs) curves and surfaces.
Polygon mesh
Surfaces are approximated with polygon mesh objects. In the [Create mesh from [NURBS](http://www.rhino3d.com/nurbs) object](mesh.html) dialog box, set the way Rhino creates a polygon mesh from the NURBS geometry. Curves do not export.
Save surface trim curves as
Polylines
When exporting [NURBS](http://www.rhino3d.com/nurbs) surfaces, polylines approximate the trimming curves. The geometry does not match the accuracy of exporting trims as curves. This option was originally included for exporting to Alias. Now you should be able to use IGES for exporting to Alias instead.
Curves
When exporting [NURBS](http://www.rhino3d.com/nurbs) surfaces, the trim curves are NURBS. NURBS trim curves provide more accuracy than exporting trims as polylines.
End-of-line character
Windows (CRLF)
Return + line feed.
Mac OS X, Unix (LF)
Line feed only.
Mac OS 9 (CR)
Return only.
Export Rhino object names
Exports object names.
Do not export object names
As OBJ groups (Use for export to 3dsMax)
As OBJ objects
Export Rhino layer/group names
Exports layer names.
These settings make it possible to export data to programs that do not support nested grouping. The OBJ import plug-in for 3ds max is one example. To export to 3ds max, selectDo not export layer/group names.
Do not export layer/group names
Layers as OBJ groups
Groups as OBJ groups
Sort by OBJ groups
Vertex welding
Unmodified
Completely unwelded
Unwelds the entire mesh before exporting it
Welded
Exports a single [vertex](meshvertex.html) for any given location (i.e., the topological vertex) but exports all of the normals and texture coordinates associated with the mesh vertex.
__ Significant digits
Export mesh texture coordinates
Export mesh vertex normals
Export material definitions
Creates an .mtl file with the same name as the .obj file. The .mtl file contains one material definition per object. There are also references to these materials added to the .obj file.
Map Rhino Z to OBJ Y
Translates the exported model from a z&#160;up orientation to a y&#160;up orientation.
Wrap long lines
OBJ Export Options

### Geometry
Save objects as
NURBS
Rhino curves and surfaces export as [NURBS](http://www.rhino3d.com/nurbs) curves and surfaces.
Polygon mesh
Surfaces are approximated with polygon mesh objects. In the [Create mesh from [NURBS](http://www.rhino3d.com/nurbs) object](mesh.html) dialog box, set the way Rhino creates a polygon mesh from the NURBS geometry. Curves do not export.
Save surface trim curves as
Polylines
When exporting [NURBS](http://www.rhino3d.com/nurbs) surfaces, polylines approximate the trimming curves. The geometry does not match the accuracy of exporting trims as curves. This option was originally included for exporting to Alias. Now you should be able to use IGES for exporting to Alias instead.
Curves
When exporting [NURBS](http://www.rhino3d.com/nurbs) surfaces, the trim curves are NURBS. NURBS trim curves provide more accuracy than exporting trims as polylines.

### Formatting
End-of-line character
Windows (CRLF)
Return + line feed.
Mac OS X, Unix (LF)
Line feed only.
Mac OS 9 (CR)
Return only.
__ Significant digits
Export material definitions
Creates an .mtl file with the same name as the .obj file. The .mtl file contains one material definition per object. There are also references to these materials added to the .obj file.
This option sets OBJ diffuse material to the object's display material if there is no render material assigned.
Convert white space in material names to underscores
Export mesh texture coordinates
Map Rhino Z to OBJ Y
Translates the exported model from a z&#160;up orientation to a y-up orientation.
Wrap long lines

### Naming
Export Rhino object names
Exports object names.
Do not export object names
As OBJ groups (Use for export to 3dsMax)
As OBJ objects
Export Rhino layer/group names
Exports layer names.
These settings make it possible to export data to programs that do not support nested grouping. The OBJ import plug-in for 3ds max is one example. To export to 3ds max, selectDo not export layer/group names.
Do not export layer/group names
Layers as OBJ groups
Groups as OBJ groups
Sort by OBJ groups

### Mesh
Vertex welding
Unmodified
Welded
Exports a single vertex for any given location (i.e., the topological vertex) but exports all of the normals and texture coordinates associated with the mesh vertex.
Completely unwelded
Unwelds the entire mesh before exporting it
NGons
Create NGons
___Minimum face count
Include unwelded edges
Cull unnecessary vertexes
Export texture coordinates
Export vertex normals
Export open meshes
Always use these settings. Do not show this dialog again.
Saves the current settings and turns off the dialog display.
To turn the message back on
Click **Options** in the appropriate [Save](save.html), [Export](export.html), [Open](open.html), [Import](import.html), or [Insert](insert.html) dialog box.Export notes
Attempting to export invalid objects will cause the export to fail. Use the [SelBadObjects](selection-commands.html#selbadobjects) command to find invalid objects before exporting.Assign a material name to an object in [Material Properties](material.html). This material name is exportedin a .mtl filefor use by the renderer.Layer names and object names export into the OBJ file as OBJ group names. Spaces in the layer or object names are converted into underbar (_) characters.See also
 [Wikipedia: Wavefront OBJ](http://en.wikipedia.org/wiki/Wavefront_OBJ).
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](wavefront-obj-import-export.html) 


---
---

{: #kanchor2989}{: #kanchor2990}{: #kanchor2991}
# AutoCAD (.dwg, .dxf) import/export
A binary file format used for storing two and three-dimensional design data and metadata. It is the native format for several CAD packages including [AutoCAD](http://www.autodesk.com/products/dwg/viewers).

## Import
To open, import, insert, and attach a file as a worksession
From theFilemenu, click [Open](open.html) or [Import](import.html) .In theOpendialog box, select the supported file type.If the import can be configured, click **Options** to specify import settings.ClickOpen, or press [Enter](enter-key.html) .When Rhino opens a non-3dm model, the title bar reflects the name of the model that was opened. When the model is saved for the first time, this model name is entered as the file name.DWG/DXF Import Options
Import unreferenced layers
Imports empty layers.
Import unreferenced blocks
Imports unused block definitions.
Import unreferenced linetypes
Imports unused linetype definitions.
Convert wide polylines to surfaces
Ignore thickness
Convert regions to curves
Mesh precision
Automatic
If the mesh imported from DWG/DXF is too big or too far from the origin to work properly as a single-precision mesh, Rhino will import the mesh as double precision.
Double precision
Single precision
 [Model units](units.html) 
 [Layout units](units.html) 
Set layer material to layer color
Assigns a material to each layer that matches the layer color.
Always use these settings. Do not show this dialog again.
Saves the current settings and turns off the dialog display.
To turn the message back on
Click **Options** in the appropriate [Save](save.html), [Export](export.html), [Open](open.html), [Import](import.html), or [Insert](insert.html) dialog box.Import notes
Polyface mesh and 3DFace entities import as polygon mesh objects. They do not convert to [NURBS](http://www.rhino3d.com/nurbs) .Wide polylines import as surfaces. If the polylines are narrower than Rhino's current tolerance setting, wide polylines import as polylines. Graphics, rays, regions, or OLE objects do not import.Line widths by layer and by object import as print widths by layer and by object.Block attributes import as text.Attribute definitions that are not included in blocks are skipped.Hatches may not import in the same position relative to objects since Rhino does not support varying the origin.Off and frozen layers import as off layers.XREFs are imported. XREF layers with the same names as the base drawing layers are merged. If any of the layers contributing to a merged layer is off or frozen in AutoCAD, the combined layer will be off in Rhino.If objects in a block definition are on AutoCAD layer 0, their properties will be set to [ByParent](properties.html#by-parent) .AutoCAD Dimension Style scale (dimscale) is now imported and assigned to the [Model space scale](dimensions-style.html#model-space-scale) in the [dimension style](dimensions-style.html) that is generated on import.Images are imported as Rhino [Picture](picture.html) objects.
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
If the export can be configured, click **Options** to specify export settings.If the file type creates only mesh objects, in the [Polygon Mesh Objects](polygon-mesh-simple-options.html) dialog box, specify the mesh settings.DWG/DXF Export Options
Export Scheme
Select the export scheme to use.
Default
2004 Lines
2004 Natural
2004 Polylines
2004 Solids
CAM Imperial
CAM Metric
R12 Lines &amp; Arcs
R12 Natural
Always use these settings. Do not show this dialog again.
Saves the current settings and turns off the dialog display.
To turn the message back on
Click **Options** in the appropriate [Save](save.html), [Export](export.html), [Open](open.html), [Import](import.html), or [Insert](insert.html) dialog box. **Edit Schemes** 
Opens the [AutoCAD Export Schemes](acadschemes.html) dialog box.
Export notes
Characters that are unsupported by AutoCAD in Layout names are replaced with underscore characters.AutoCAD supports NURBS geometry and Rhino exports NURBS surfaces as such if your export scheme is set toExport Surfaces as Solids. In AutoCAD, the objects will list as Solid or Surface.PictureFrame and [Picture](picture.html) objects are exported as AutoCAD images.Import and Export Notes
Block definitions and instances import and export.Paperspace objects import as [Layouts](layout.html) .Layer names and colors import and export.Use IGES with the IGES import/export module to exchange [NURBS](http://www.rhino3d.com/nurbs) geometry with AutoCAD.The ACIS SAT file format can be used to export solids to AutoCAD 2000 and above; AutoCAD 2000 ACIS objects are imported.ByBlock and ByLayer properties settings are translated as ByParent and ByLayer in Rhino.AutoCAD blocks with attributes are now imported into Rhino as user text. This can be manipulated with the [GetUserText](rhinoscripting.html#getusertext) and [SetUserText](rhinoscripting.html#setusertext) commands.See also
![images/-no-toolbar-button.png](images/-no-toolbar-button.png) [AcadSchemes](acadschemes.html) 
Edit AutoCAD export schemes.
 [Wikipedia: .DWG](http://en.wikipedia.org/wiki/.dwg) 
 [Wikipedia: .DXF](http://en.wikipedia.org/wiki/DXF) 
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](autocad-dwg-dxf-import-export.html) 


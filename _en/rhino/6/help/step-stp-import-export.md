---
---

{: #kanchor2074}{: #kanchor2075}
# STEP (.stp; .step) import/export
STEP (Standard for the Exchange of Product Data) is an ISO standard exchange format used for representing three-dimensional data in a format that can be recognized by multiple programs.

## Import
To open, import, insert, and attach a file as a worksession
From theFilemenu, click [Open](open.html) or [Import](import.html) .In theOpendialog box, select the supported file type.If the import can be configured, click **Options** to specify import settings.ClickOpen, or press [Enter](enter-key.html) .When Rhino opens a non-3dm model, the title bar reflects the name of the model that was opened. When the model is saved for the first time, this model name is entered as the file name.STP Import Options
Note
Importing a .step file in a format that supports units and tolerances does not adjust the units and tolerances in Rhino. A dialog box will warn you if the units do not match.When reading .step files where not all objects have the same unit system, all units are converted to match the Rhino file [unit](units.html) system, and objects are scaled appropriately.Join surfaces (Uncheck to retain per-face colors)
Joins surfaces with shared edges.
ifJoin Surfacesis unchecked, face colors come from the face entities rather than the solid entities.
Do not join polysurfaces with more than ___ faces
Restricts the number of faces allowed in the resulting polysurface.
Display nested block warning
If nested blocks occur, display a warning dialog box.
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
If the export can be configured, click **Options** to specify export settings.If the file type creates only mesh objects, in the [Polygon Mesh Objects](polygon-mesh-simple-options.html) dialog box, specify the mesh settings.STP Export Options
STEP schema
Your company standards determine which STEP schema you should use. If you have no standard, choose the default. The STEP schema number makes no difference to the data exported.
AP203ConfigControlDesign
AP214AutomotiveDesign
AP214AutomotiveDesignCC2
Export parameter space curves
Some (not most, and not Rhino) importing applications can make use of the 2-D trimming curves to get a more accurate and faster import. The size of the step file will be larger.
Let importing application set color for black objects
If a Rhino object has color black, no color is assigned to the object in the step file. This will cause the importing application to give the object its default color. This is desirable because black objects look like ink blots in some applications. This option is grayed out if the schema option is AP203ControConfigDesign since that schema does not include color entities.
Always use these settings. Do not show this dialog again.
Saves the current settings and turns off the dialog display.
To turn the message back on
Click **Options** in the appropriate [Save](save.html), [Export](export.html), [Open](open.html), [Import](import.html), or [Insert](insert.html) dialog box.
# Related command

## STEPTree
{: #steptree}
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/-no-toolbar-button.png](images/-no-toolbar-button.png) [Not on toolbars.](toolbarwhattodo.html) 
Menus
![images/-no-menu-item.png](images/-no-menu-item.png) [Not on menus.](menuwhattodo.html) 
TheStepTREEcommand browses the structure of a STEP file.
Steps
Select a file.See also
 [Wikipedia: ISO 10303](http://en.wikipedia.org/wiki/ISO_10303).
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](step-stp-import-export.html) 


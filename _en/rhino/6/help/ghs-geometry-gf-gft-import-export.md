---
---

{: #kanchor2995}{: #kanchor2996}{: #kanchor2997}
# GHS Geometry (.gf, .gft) import/export
GHS geometry (.gf and .gft) files are used to analyze floating vessels (boats, ships, docks).

## Import
To open, import, insert, and attach a file as a worksession
From theFilemenu, click [Open](open.html) or [Import](import.html) .In theOpendialog box, select the supported file type.If the import can be configured, click **Options** to specify import settings.ClickOpen, or press [Enter](enter-key.html) .When Rhino opens a non-3dm model, the title bar reflects the name of the model that was opened. When the model is saved for the first time, this model name is entered as the file name.GHS Import Options
Style
Mesh
Import the data in the geometry file as a set of meshes
Body View
Generate 2-D body sections
Plan View
Generate a 2-D plan (top down) view
Profile View
Generate a 2-D profile (from side) view
Wire Frame
Generate 3-D polylines from data in the geometry file
Attach GHS Data to Meshes
Add GHS geometry file information to the meshes generated on import. This includes all of the hull and tank information (contents, permeability, sounding tubes). This is the same information embedded with the [AttachGHSData](attachghsdata.html) command.
This is an option only available with the Mesh import option. Using the other modes will contain only the geometry, not the GHS data.
Remove collinear points
Simplify imported polylines by removing collinear points. If three point along a station all lay on the same line, the middle point will be removed.
When a GHS file is imported using the mesh option, it is possible that the mesh may not have the exactly correct join information. You can edit the mesh with the mesh editing commands.
Always use these settings. Do not show this dialog again.
Saves the current settings and turns off the dialog display.
To turn the message back on
Click **Options** in the appropriate [Save](save.html), [Export](export.html), [Open](open.html), [Import](import.html), or [Insert](insert.html) dialog box.
## Export
Creating a GHS file is a two-step process
Use the [AttachGHSData](attachghsdata.html) command to define portions of the hull.Save or export the data to a GHS file format.To save a GHS Geometry file
From theFilemenu, click [Export Selected](export.html) or [Save As](save.html#saveas) .Note: Before saving a GHS Geometry file, GHS data needs to be associated the surfaces or meshes through the [AttachGHSData](attachghsdata.html) command.
In theFiles of typebox, selectGHS Geometry File (*.gf).In theFile namebox, select or type a file name.Specify what is to be saved. [Save Small](save.html#savesmall) 
 [Save geometry only](save.html#save-geometry-only) 
{: #ghs-part-maker-file-pm-export}GHS Part Maker File (PM)
A GHS Part Maker file is a script that is processed by the Part Maker application to create or modify a GHS geometry file. In many cases this is a better alternative than the straight GHS Geometry File export because the script can be modified with a plain text editor such as Notepad to include additional geometric information.
To save GHS Part Maker Files (PM)
In theSavedialog box, selectGHS Part Maker File (*.pm).See also
 [Creative Systems, Inc](http://www.ghsport.com/home.htm).
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](ghs-geometry-gf-gft-import-export.html) 


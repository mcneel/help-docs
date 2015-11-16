---
---

{: #kanchor3001}{: #kanchor3002}{: #kanchor3003}{: #kanchor3004}{: #kanchor3005}{: #kanchor3006}{: #kanchor3007}{: #kanchor3008}{: #kanchor3009}{: #kanchor3010}
# Initial Graphics Exchange Specifications (.iges) import/export
Initial Graphics Exchange Specification (.iges) defines a vendor-neutral data format that allows the digital exchange of information.

## Import
To open, import, insert, and attach a file as a worksession
From theFilemenu, click [Open](open.html) or [Import](import.html) .In theOpendialog box, select the supported file type.If the import can be configured, click **Options** to specify import settings.ClickOpen, or press [Enter](enter-key.html) .When Rhino opens a non-3dm model, the title bar reflects the name of the model that was opened. When the model is saved for the first time, this model name is entered as the file name.
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
If the export can be configured, click **Options** to specify export settings.If the file type creates only mesh objects, in the [Polygon Mesh Objects](polygon-mesh-simple-options.html) dialog box, specify the mesh settings.Import notes
When Rhino reads an IGES file using the [Open](open.html) command, the Rhino units are set to those in the IGES file and the Rhino system tolerance is set to the IGES file tolerance, with some adjustments made to keep Rhino from setting a too small/big tolerance based on a bogus IGES file tolerance.When Rhino reads an IGES file using the [Import](import.html) command, the Rhino system tolerance is not changed. The tolerance used in rebuilding incorrect IGES trims is automatically computed and is always smaller than or equal to the Rhino system tolerance. If the IGES units do not match the Rhino units, you are given the option of scaling the imported IGES geometry so that it matches the current Rhino unit system.Polygon meshes are not exported to IGES file.IGES supports only the printable subset of ASCII characters from character 32 to 127. This causes layer names to be truncated at the first occurrence of a non US character (like é).Unnecessary knots are removed from imported curves if the curve has identical geometry and [parameterization](parameterization.html) .IGES Export Options
 [IGES type](#iges-type) 
Always use these settings. Do not show this dialog again.
Saves the current settings and turns off the dialog display.
To turn the message back on
Click **Options** in the appropriate [Save](save.html), [Export](export.html), [Open](open.html), [Import](import.html), or [Insert](insert.html) dialog box.IGES Export Detailed Options
{: #iges-type}IGES type
Specifies a pre-defined IGES type that attempts to match requirements in target software.
 ** [Edit Types](#iges-export-types) ** 
Click to customize existing IGES types or to create new IGES export types.
Author / Organization / Sender's product ID / Receiver's product ID
These are text fields in the IGES file that can be used for identification purposes.
IGES tolerance
In general, the IGES tolerance should match the absolute tolerance setting in Rhino, taking account the possible unit conversion.
The IGES tolerance does not affect the accuracy of the geometry.
IGES units
The units used for the IGES export.
Include Rhino notes in the IGES file
Check to save notes in IGES start section. Otherwise, the IGES start section is a blank line.
Render color as IGES entity color
Check to use the render color of objects as the IGES entity color. Otherwise, Rhino uses the layer color of the object as the IGES entity color.
Always use these settings. Do not show this dialog again.
Saves the current settings and turns off the dialog display.
To turn the message back on
Click **Options** in the appropriate [Save](save.html), [Export](export.html), [Open](open.html), [Import](import.html), or [Insert](insert.html) dialog box.Export note
There are two types of solids modelers: *surfaces* and *solids*. Use the "surfaces" type when exporting a single surface to those products. Use the "solids" type when exporting anything you want to be able to join back together.{: #iges-type-details}IGES Type Details
General
Name
Type a name for the IGES type.
IGES version
Choose between IGES version 5.2 and 5.3.
The difference is 5.2 stores years if you use two digits and 5.3 if you use four digits.
Text file type
Choose among MS-DOS, Unix, and MacOS style line endings.
Windows (CRLF)
Mac OS X Unix (LF)
Mac OS 9 (CR)
Scale
Set the default scale factor for the IGES type. The number must be bigger than zero. In most cases, this number should be 1.
Points and Curves
Point Objects
116 (Separate points)
Exports points as separate IGES point entities
106-2 (Layer set points)
Exports points on a single layer as a single point set.
Max degree
No limit
No limit to the degree is applied.
3
All [NURBS](http://www.rhino3d.com/nurbs) curves with any degree higher than three are approximated with non-rational cubics to the specified IGES tolerance.
5
All [NURBS](http://www.rhino3d.com/nurbs) curves with degree higher than five are approximated, in non-rational quintics to the specified IGES tolerance.
Composite curves as single B-spline
Curve made from two or more B-splines can be exported as an IGES 102 (composite curve) entity or as IGES 126 entities.
Use simple entities when possible
Use this setting to export [NURBS](http://www.rhino3d.com/nurbs) curves that are lines, arcs, or circles (within the IGES tolerance) as IGES lines, IGES arcs, or IGES circles.
Fit rational curves
With this setting all rational curves (curve objects and trim curves) are approximated, in non-rational cubics, to the tolerance specified as the IGES tolerance.
Clamp end knots
With this setting periodic [NURBS](http://www.rhino3d.com/nurbs) curves are exported as NURBS curves with clamped end knots.
Surfaces
Solids
Separate surfaces
184
186 (Manifold BRep)
402-7 (Unordered group)
Polysurfaces
Separate surfaces
402-7 (Unordered group)
Surfaces
143
144
128 + 3D Trim curves
IGES 128 means all trimmed surfaces are exported as untrimmed surfaces.
Use simple entities when possible
With this setting [NURBS](http://www.rhino3d.com/nurbs) surfaces that are planar (within the tolerance specified as the IGES tolerance) export as IGES planes or IGES trimmed planes.
Fit rational surfaces
With this setting, when possible, rational [NURBS](http://www.rhino3d.com/nurbs) surfaces are be approximated with non-rational cubics to the tolerance specified as the IGES tolerance.
Clamp end knots
With this setting periodic [NURBS](http://www.rhino3d.com/nurbs) surfaces are exported as NURBS surfaces with clamped end knots.
Split closed surfaces
If a surface is closed (like a cylinder), the surface will be split into two halves in the IGES file. If a surface is closed in both directions (like a torus), the surface will be split into four quarters in the IGES file.
Split bipolar surfaces
If a surface has poles at both ends (like a sphere), the surface is split so each half has just one pole.
{: #iges-export-types}IGES Export Types
IGES Type
Lists the currently defined IGES types.
 **New** 
Opens the [IGES Type Details](#iges-type-details) dialog box.
 **Copy Type** 
Opens the [IGES Type Details](#iges-type-details) dialog box with settings from the currently selected IGES type.
 **Edit** 
Opens the [IGES Type Details](#iges-type-details) dialog box to edit settings from the currently selected IGES type.
 **Delete** 
Deletes the currently selected IGES type.

# Related commands

## ReadEveryIGESEntity
{: #readeveryigesentity}
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/-no-toolbar-button.png](images/-no-toolbar-button.png) [Not on toolbars.](toolbarwhattodo.html) 
Menus
![images/-no-menu-item.png](images/-no-menu-item.png)
TheReadEveryIGESEntitycommand imports all IGES entities, regardless of type.
Steps
Open the questionable IGES file.If there is any geometry at all in the IGES file, It will be read. You might, however, get lots of geometry you didn't want and have to dig through the pile to find the items you need.TheReadEveryIGESEntitycommand only effects the next IGES file that is read. If you do something like:
open alpha.igsReadEveryIgesEntityopen beta.igsopen gamma.igs
Rhino attempts to read every entity only from beta.igs.
Rhino reads alpha.igs and gamma.igs normally, accepting only entities marked as geometry.

## IGESStudy
{: #igesstudy}
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/-no-toolbar-button.png](images/-no-toolbar-button.png) [Not on toolbars.](toolbarwhattodo.html) 
Menus
![images/-no-menu-item.png](images/-no-menu-item.png) [Not on menus.](menuwhattodo.html) 
The IGESStudy command examines specific entities in an IGES file by limiting which portions of the IGES folder are parsed.
Warning
This command is for users familiar with the structure of IGES data files.No technical supportis available for this command. TheIGESStudycommand is for expert users who need to dig through large IGES files on piece at a time. Again, expert knowledge of IGES file structure is required.
Background
Every entry into an IGES file also has folder entry (DE). The information that a DE stores determines if the corresponding IGES entity (curve, surface, solid, color, layer name, etc.) gets read. To further understand the importance of not blindly reading every entity in an IGES file as a top level piece of geometry, do this test:
Steps
Use the [BooleanUnion](booleanunion.html) command to make a multi-faced solid from a box, torus, and sphere.Export the solid to an IGES file.Read the IGES file back in. You will get an exploded version of what you started with.Delete all the stuff you just read in.Run the [ReadEveryIGESEntity](#readeveryigesentity) command.Read the IGES file again. You will get lots of extra curves and surfaces.The extra curves and surfaces you got in step 6 provide the information you need to create trimmed surfaces. These curves and surfaces were imported in step 6 because the IGES reader ignored to DE information that flags the corresponding entity as a part of some "top" level object. The [ReadEveryIGESEntity](#readeveryigesentity) command is used as a last resort to get information out of IGES files that have "top" level objects that have been flagged as parts.Basic scenario:
You read an IGES file and it looks like some information is coming in damaged. The first thing you need to find out is the DE of the damaged objects. Run theIGESStudycommand and turn theLabeloption on.
IGES debugging options(DEtest=OffFirstDE= *1* LastDE=0ReadEveryEntity= *Off* Label=On)
Read the file again. This time, every object you read has its Rhino name set to "DE N", where "N" is an odd number. The folder entries in an IGES file are labeled 1, 3, 5, 7, and so on. Select the bad objects and make a list of the DE's that are troublesome. Let us say 13, 137, and 9025 were coming in as bad objects.
Now you use theIGESStudycommand to read just the problem entitles, one at a time.
IGES debugging options(DEtest=OnFirstDE= *13* LastDE=13ReadEveryEntity= *Off* Label=On)
You verify that DE 13 is coming in as junk. Then, look at the IGES file (in a text editor or a program like IGESure) and see what DE 13 is supposed to be. If you understand the entity, you can use theIGESStudycommand to read in the parts that are used to make the entity. For example, you can look at the base surface and trimming curves to see what might be going on. As you do this, you will find blocks of entities you need to read. In those cases, you can use theIGESStudycommand to read chunks of the file. For example:
IGES debugging options(DEtest=OnFirstDE= *123* LastDE=199ReadEveryEntity= *On* Label=On)
will read every entry with DE number between 123 and 199. If you only want to read top level entities you setReadEveryEntity=Off.

## SetIGESLayerLevelMap
{: #setigeslayerlevelmap}
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/-no-toolbar-button.png](images/-no-toolbar-button.png) [Not on toolbars.](toolbarwhattodo.html) 
Menus
![images/-no-menu-item.png](images/-no-menu-item.png) [Not on menus.](menuwhattodo.html) 
The SetIGESLayerLevelMap command controls the correspondence between Rhino layers and IGES levels on IGES import and export from the command line or a script.
IGES "levels" are like Rhino layers, except they use a number as an identifier instead of a text name. If you have layer standards for products that use IGES to exchange data, you will need a way to define a correspondence between Rhino layer names and IGES level numbers. Rhino has a layer to level function.
To set up correspondence between Rhino layers and IGES levels:
Create a text file like the following example:;IGES level translation rules[3Stooges]"Default" = 0"Larry" = 13"Curley" = 7"Moe" = 32000[FruitStand]"Default" = 0"Orange" = 9876"Apple - Delicious" = 13"Apple - Granny Smith" = 7232"Grape" = 1This file defines rules for mapping Rhino layers to IGES level numbers that will be used during IGES export and for mapping IGES level numbers to Rhino layers that will be used during IGES import.This example file defines two sets of Rhino layer-IGES level correspondence rules (flavors) named "3Stooges" and "FruitStand."Steps
Select the map file you created.Select theflavoroption.For example, if your file is called "iges_level_mapping.txt" and you want to use the "FruitStand" type, set theFlavoroption toFruitStand.Flavor Options
LayerMapping
Flavor
File
Note
In general, it is a good idea for Rhino's "Default" layer to correspond to IGES's level 0, but this is not required.This file can contain multiple flavors. A flavor has a name enclosed in square brackets [] followed by lines that look like:"&lt;RhinoLayerName&gt;" = Nwhere N is a non-negative integer (0, 1, 2, 3, ... ).The Rhino layer name appears between the quotation marks.A flavor is terminated by a blank line.The converter/map program ignores spaces and tabs.The converter/map program ignores lines that begin with semi-colon (;).If an imported IGES file contains a level number that is not listed in the set of rules and does have a IGES level name, that level will automatically import to a layer called "IGES_LEVEL_N".If an exported Rhino layer name is not listed in the set of rules, an IGES level number is automatically selected.See also
 [Import and export objects](sak-importexport.html) 
 [Troubleshooting IGES Files with Rhinoceros](http://wiki.mcneel.com/rhino/troubleshootingiges).
 [Wikipedia: IGES](http://en.wikipedia.org/wiki/IGES) 
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](iges-iges-import-export.html) 


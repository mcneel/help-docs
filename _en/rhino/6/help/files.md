---
---

{: #kanchor2705}{: #kanchor2706}{: #kanchor2707}{: #kanchor2708}{: #kanchor2709}{: #kanchor2710}{: #kanchor2711}{: #kanchor2712}{: #kanchor2713}{: #kanchor2714}{: #kanchor2715}
# Files
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/options.png](images/options.png) [Properties](properties-toolbar.html)  [Standard](standard-toolbar.html)  [Tools](tools-toolbar.html) 
Menus
Tools
Options
TheFilesoptions manage templates, backup files, file saving and locking.
Template files
Location
Specifies the location of the template files.
Default
Defines the name of the template file Rhino uses when it starts. If a file is specified, this template is used when Rhino starts. If no template file is specified, a template list appears each time Rhino starts.
{: #save-bak}Save
Create backup (*.3DMBAK) files when saving
When enabled and a Rhino model is saved to a .3dm filename that already exists, the original is renamed .3dmbak. This backup file can be opened from the RhinoFile &gt; Openmenu.
AutoSave
Save every ___ minutes
Turns on the Autosave feature and defines the save interval. When Autosave activates, a copy of the model you are working on automatically saves to the Autosave file.
Autosave file
Defines the name and location of the Autosave file. If a model has been saved, the Autosave file name will include the model name.
Always save before
Sets a list of commands that will save the file before the command starts.
Save render and analysis meshes in autosave file
If this setting is off, the model will save without meshes.
File Locking
Enable file locking. Creates *.RHL files
Rhino lock files *&lt;filename&gt;.3dm.rhl* are created to let other instances of Rhino know that a file is in use. Lock files are created when a .3dm file is opened or when an unnamed file is saved as a .3dm file.
Display read-only warning
Displays in a warning message to a second user who tries to access a locked .3dm file with Rhino.
Note
Lock filesdo notprevent the file from being opened; they are only used to get information about who is using the file.This information can display in a warning message to a second user who tries to access the .3dm file with Rhino.If a lock file exists, Rhino lets other users open the related .3dm file only in read-only mode.The lock file is automatically deleted when Rhino successfully closes the .3dm file.If the Rhino file does not close successfully, abandoned .rhl files may prevent re-opening the associated Rhino file.Abandoned .rhl files can be deleted.Imported file layers
Controls how Rhino manages layer names when Rhino imports an external model into an existing model.
Ways to "import" an external model into the existing model include:
 [Import](import.html)  [Paste](paste.html)  [Insert](insert.html) Example
Current model = ThreeStooges.3dm
Import models named CurlyHoward.3dm, LarryFine.3dm, and MoeHoward.3dm with the following layer structures.
ThreeStooges.3dm
CurlyHoward.3dm
LarryFine.3dm
MoeHoward.3dm
Layers
Layers
Layers
Layers
Name
![images/layerminus.png](images/layerminus.png)Stooges
Curly
Larry
Moe
Name
![images/layerminus.png](images/layerminus.png)Faces
Curly
Name
![images/layerminus.png](images/layerminus.png)Faces
Larry
Name
![images/layerminus.png](images/layerminus.png)Faces
Moe
Use complete layer tree from source file
Rhino will create a copy of the imported model's layer tree in the existing model.
Result
The imported layersCurly,Larry, andMoeare merged into the same-named layers in the current model. The layer Faces is not merged.
ThreeStooges.3dm
Layers
Name
![images/layerminus.png](images/layerminus.png)Stooges
Curly
Larry
Moe
![images/layerminus.png](images/layerminus.png)Faces
Curly
Larry
Moe
Use existing layers with matching name
If a layer in the existing model has the same name as a layer in the external model, Rhino will add everything on the external layer to the existing layer.
Result
The imported layerFaces, with sub-layersCurly,Larry, andMoebelow it, is imported without merging.
ThreeStooges.3dm
Layers
Name
![images/layerminus.png](images/layerminus.png)Stooges
Curly
Larry
Moe
Faces
Clipboard
Allow copy and paste to version 4.0
On exit
Specifies action to take when a large amount of data is in the Clipboard when Rhino closes.
Keep
Keeps data in the Clipboard for use in another application.
Delete
Clears the Clipboard.
Prompt
Prompts to keep or delete Clipboard data.
Recent files list
 **Clear Recent Files List** 
Removes file names from the list of recently-used files.
To save options for use on other computers
![images/optionsexport.png](images/optionsexport.png) [OptionsExport](optionsexport.html) 
Save [Options](options.html) settings to a file.
![images/optionsimport.png](images/optionsimport.png) [OptionsImport](optionsexport.html#optionsimport) 
Restore [Options](options.html) settings from a file.
See also
 [Rhino Wiki: Imported and linked block layer names](http://wiki.mcneel.com/rhino/rhinov5status_layernames#examplelinked_block_layer_names) 
![images/options.png](images/options.png) [Options](options.html) 
Manage global options: [3D mouse](3dconnexion.html), [alerter](alerter.html), [aliases](aliases.html), [appearance](appearance.html), [context menu](context-menu.html), [display modes](view-displaymode-options.html), [files](#), [general](general.html), [idle processor](idleprocessor.html), [keyboard](keyboard.html), [libraries](libraries.html), [licenses](licenses.html), [modeling aids](modeling-aids.html), [mouse](mouse.html), [plug-ins](plug-ins.html), [render](rendering.html), [RhinoScript](rhinoscript.html), [selection menu](selection-menu.html), [toolbars](toolbars.html), [updates and statistics](updates-and-statistics.html), [view](view.html).
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](files.html) 


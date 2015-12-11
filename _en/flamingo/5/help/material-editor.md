---
title: Materials Editor Panel
---

# ![images/paint.svg](images/paint.svg) {{page.title}}
Materials contain the specification for color, reflectivity, transparency, textures, and bump-maps of a surface finish. All materials have basic settings. The default material is white and matte, with no reflectivity or transparency. For the best results use Flamingo specific materials.

Materials can be assigned to layers, objects, and blocks. Assignments can be made by dragging and dropping on to objects or various controls. See [Material Assignments](material_assignment.html) for more information.

Once assigned, materials are stored in the model. The material, textures, and all support files for rendering can be stored within the Rhino model with properly set [Rendering Options](http://docs.mcneel.com/rhino/5/help/en-us/index.htm#options/rendering.htm).

Materials, environments, and textures are stored in the model, but rendering content can also be saved to files that can be shared between models. Content can be dragged between Rhino sessions and into a folder. Color swatches can be dragged and dropped in the same way. The [Libraries Panel](libraries.html) displays the default content folder. Use this to drag and drop content into the model or to drag and drop model content to an external file.

![images/material_editor_panel.svg](images/material_editor_panel.svg){:  #panel_map .float-img-right}

##### Where can I find this command?
There are several options to find the Materials tab.

* ![images/materialtab.png](images/materialtab.png)Materials tab
* ![images/icon-render.png](images/icon-render.png)Render Tools toolbar > ![images/materialtab.png](images/materialtab.png) Material Editor
* Menus > Render Pulldown > Materials Editor
* On the Command line type MaterialEditor

The Material Editor Panel is split into discrete sections.  Based on the material type, the advanced panels may vary.

You can drag colors and textures from the color swatch and drop onto any other color swatch or control in the Material Editor, [Texture Palette](texturepalette.html), or [Environment Editor](environmenteditor.html).

##### Materials Panel

 1. [Settings Bar](#settings)
 1. [Material List](#material_list)
 1. [Window Divider](#divider)
 1. [Material Properties Section](#properties)
 1. [Name](#name)
 1. [Material Properties Panels](#panels)

## [Settings Bar](#panel_map) ![images/callout_1.svg](images/callout_1.svg)
{: #settings .clear-img}
Use this bar to navigate the material during its development.

#### ![images/met_leftarrow.png](images/met-leftarrow.png) Back Arrow
Walks back though the current material or the previously selected materials.  For instance, materials with textures have multiple layers.  Use this arrow to return to the parent material from the texture details.

####  ![images/met_rightarrow.png](images/met-rightarrow.png) Forward Arrow
Walks forward though the current material or the previously selected materials.  For instance materials with textures have multiple layers.  Use this arrow to return to the recently used texture from the parent material.


#### ![images/material_editor.png](images/material_editor.png)![images/texture-2dchecker.png](images/texture-2dchecker.png) Currently selected material name
Displays the current material name and level.  For instance, if there is a texture or a material procedural level the ">" will show. A good place to see where the editor is in a material.

#### ![images/library_default.png](images/library_default.png) Tools menu
Displays the [Tools menu](#tools-menu).  This is an extensive menu of commands, settings and utilities related to materials.


## [Materials List](#panel_map) ![images/callout_2.svg](images/callout_2.svg)
{: #material_list}
This lists all the materials contained in the model. From this list:

* Scroll up and down in the list to see all the materials in the model.
* Drag and drop a material from this list onto a layer in the [Layer Panel](http://docs.mcneel.com/rhino/5/help/en-us/index.htm#commands/layer.htm) or directly onto an Object to assign it to an Object. See [Material Assignments](material_assignment.html) for more information.
* Add a new Material using the Add New Button ![images/add_material.png](images/add_material.png) at the bottom of the list.


* Click on each material to select it. Once selected the material's properties will show in the panels below. See [Render Materials Properties](#properties) for more information.
* Right-click a thumbnail to display the Material context menu.
* Right-click the blank area to display the New Material Context Menu.

###  ![images/add_material.png](images/add_material.png) Add new material
{: #add_material}
Scroll down to the bottom of the Material list to see the add icon.

Opens the Render Content [library](libraries.html) of materials.
The materials in the library act as templates for creating materials in the model.

### Material Context Menu
{: material_context}
This menu is available by right-clicking on a material listing.  See the [Tools Menu](#tools_menu) for details on the many options in this menu.

### New Material Context Menu
{: new_material_context}
This menu is available by right-clicking on a blank area of the Material List.

#### ![images/toolbarlus.png](images/toolbarplus.png) Create New Material
Creates a new basic matte white material.


#### ![images/paste.png](images/paste.png) Paste
Creates a new material based on the Clipboard contents.

#### ![images/pasteasinstance.png](images/pasteasinstance.png) Paste as Instance
Creates a new material based on the Clipboard contents that is linked to the original through instancing.

#### ![images/grid.png](images/grid.png) Grid
Displays the previews as a grid of thumbnails.

#### ![images/list.png](images/list.png) List
Displays the previews as a list of thumbnails.

#### ![images/tree.png](images/tree.png) Tree
Displays the previews as a tree showing nesting.

#### ![images/horizontal.png](images/horizontal.png) Horizontal Layout
Displays the previews to the left of the controls.

#### ![images/showpreview.png](images/showpreview.png) Show Preview Pane
Displays the preview properties for the currently-selected thumbnail. Set the preview geometry, size, background, rotation behavior.

#### ![images/floatthumbnail.png](images/floatthumbnail.png) Float
Floats the preview image in a resizable window.

#### Thumbnails

##### ![images/small.png](images/small.png) Small
Sets the thumbnail size to the smallest size.

##### ![images/medium.png](images/medium.png) Medium
Sets the thumbnail size to medium size.

##### ![images/large.png](images/large.png) Large
Sets the thumbnail size to large size.

##### ![images/showlabels.png](images/showlabels.png) Show Labels
Displays thumbnail name labels when in Grid mode.
List mode always displays labels.

##### ![images/showunits.png](images/showunits.png) Show Units
Displays size in model units.

##### ![images/autoupdatethumbnail.png](images/autoupdatethumbnail.png) Auto-Update Preview
Automatically updates all previews as settings change.

##### ![images/updateallpreviews.png](images/updateallpreviews.png) Update All Previews
Update previews manually when Auto-Update Preview is off.

## [Window Divider](#panel_map) ![images/callout_3.svg](images/callout_3.svg)
{: #divider}
Drag on this divider to change the length of the Material List. If you lengthen the Material List, the Material Properties Section shortens.

## [Material Properties Section](#panel_map) ![images/callout_4.svg](images/callout_4.svg)
{: #properties}

#### [Material Name](#panel_map) ![images/callout_5.svg](images/callout_5.svg)
{: #name}
This is the name of the material. The material name is also saved as the file name when exporting the material to the library. Note: Materials are stored in the Rhino model. Unique materials can have the same name in different Rhino models.

#### [Material Panels](material-editor.html#panel_map) ![images/callout_6.svg](images/callout_6.svg)
{: #panels}
The Materials Properties section is filled with several direct Material panels. Clicking on the grey title bar will roll up the material panel, hiding the contents of that panel.  Click on the title bar again to show contents.

Material Panels will vary based on the type of material and the current active material level. For more information on specific material panels see [Flamingo Materials](material-type-simple.html).

## Tools menu ![images/library_default.png](images/library_default.png)
{: #tools-menu}
<!-- This comes from the page http://docs.mcneel.com/rhino/5/help/en-us/popup_moreinformation/materialthumbnail_contextmenu.htm -->
These settings also appear on right-click context menus for the thumbnail previews and the thumbnail backgrounds.

#### ![images/assigntoobjects.png](images/assigntoobjects.png) Assign to Selection
Assigns the current material to selected objects.

##### To assign a material to objects
 1. Click Assign to Selection.
 1. In the Rhino viewport, select the target objects.

##### To preselect objects
 1. In the Rhino viewport, select the target objects.
 1. Click Assign to Selection.
The target objects can be selected either before or after clicking Assign to Selection.

##### To drag and drop materials to objects
 * Drag the material from the thumbnails or list onto the target objects.
Drag and drop works for only one object at a time.

#### ![images/assigntolayers.png](images/assigntolayers.png) Assign to Layers
Assigns the current material to layers.

##### To assign a material to layers
 1. Click Assign to Layers.
 1. In the Choose Layers dialog box, check the boxes for the material assignment.

##### To assign materials from the Layers panel
 1. In the  [Layer](http://docs.mcneel.com/rhino/5/help/en-us/index.htm#commands/layer.htm)  panel, select one or more layers and click the  [Material](http://docs.mcneel.com/rhino/5/help/en-us/commands/layer.htm#Material)  column.
 1. In the Layer Material dialog box, select the material to assign.


##### To drag and drop materials to objects
 * Drag the material from the thumbnails or list onto the target layer.
Drag and drop works for only one layer at a time.

#### ![images/materials_selectobjects.png](images/materials_selectobjects.png) Select Objects
Select objects in the model for material assignment.

#### ![images/toolbarplus.png](images/toolbarplus.png) Create New Material
Opens the Render Content [library](libraries.html) of materials.
The materials in the library act as templates for creating materials in the model.

#### ![images/import.png](images/import.png) Import Material from File
Imports materials from a saved Rhino .rmtl file.

#### ![images/savetofile.png](images/savetofile.png) Save to File
Saves a material to a Rhino .rmtl file.

#### ![images/changetype.png](images/changetype.png) Change Type
Changes the material to a different type.

#### ![images/changetype.png](images/changetype.png) Change Type (Copy Similar Settings)
Changes the material to a different type.
The default behavior depends on the current state of the [Rendering Options](http://docs.mcneel.com/rhino/5/help/en-us/index.htm#popup_moreinformation/materialpanel_toolsmenu.htm) &gt;  [Copy similar settings when content type is changed](http://docs.mcneel.com/rhino/5/help/en-us/index.htm#popup_moreinformation/materialpanel_toolsmenu.htm)  box. If checked, compatible settings from the old content will be copied to the new one.

#### ![images/reset.png](images/reset.png) Reset to Defaults
Changes all the material settings to the default white, matte, non-reflective, untextured material.

#### ![images/copy.png](images/copy.png) Copy
Copies the selected material to the Windows Clipboard. The Clipboard can then be pasted into the editor to create a new material or pasted directly into a folder to create a [library](libraries.html) file.

#### ![images/paste.png](images/paste.png) Paste
Creates a new material based on the Clipboard contents.

#### ![images/pasteasinstance.png](images/pasteasinstance.png) Paste as Instance
Creates a new material based on the Clipboard contents that is linked to the original through instancing.

#### ![images/delete.png](images/delete.png) Delete
Deletes the selected material.

#### ![images/rename.png](images/rename.png) Rename...
Renames the selected material.

#### ![images/duplicate.png](images/duplicate.png) Duplicate
Copies the selected material to a new material with the same settings.

#### ![images/removeinstancing.png](images/removeinstancing.png) Remove Instancing
Removes the connection between [instanced](http://docs.mcneel.com/rhino/5/help/en-us/index.htm#popup_moreinformation/materialpanel_toolsmenu.htm) materials.
{% include_relative snippets/snippet-contenteditorpreviewoptions.md %}


#### ![images/contentfilter.png](images/contentfilter.png) Content Filter
Opens the [Content Filters](content_filters.html) dialog box.

#### ![images/rename.png](images/rename.png) Properties
Opens the [Preview Properties](http://docs.mcneel.com/rhino/5/help/en-us/index.htm#popup_moreinformation/materialpanel_toolsmenu.htm) dialog box.

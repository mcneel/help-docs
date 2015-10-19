---
---

# Material Editor Panel ![images/materialtab.png](images/materialtab.png)
Materials contain the specification of color, reflectivity, transparency, textures, and bump-maps of a surface finish. For best result use Flamingo specific materials.

#### Where can I find this command?
 1. ![images/materialtab.png](images/materialtab.png)Materials Tab
 1. ![images/icon-render.png](images/icon-render.png)Render Tools Toolbars > ![images/materialtab.png](images/materialtab.png) Material Editor
 1. ![images/menuicon.png](images/menuicon.png)Menus > Render Pulldown > Materials Editor
 1. Command > MaterialEditor


{% include_relative snippets/snippet-savingrendercontent.md %}
<!-- TODO: The snippet above and the paragraph below need to be combined?  Not sure this is the right place for this snippet-->
Materials can be assign to layer, objects and blocks. Assignments can be made by dragged and dropped onto objects or various controls. Any number of materials can be stored in the model.

![images/material_editor_panel.svg](images/material_editor_panel.svg){:  #panel_map height="600px" style="float: right"}

The Material Editor Panel is split into discrete sections.  Based on the material type, the advanced panels may vary.

Colors and textures can be dragged from the color swatch and dropped onto any other color swatch or control in the Material Editor, [Texture Palette](texturepalette.html), or [Environment Editor](environmenteditor.html).
Materials Panel

 1. [Settings Bar](material-editor.html#settings)
 1. [Material List](material-editor.html#material_list)
 1. [Name](material-editor.html#name)
 1. [Basic Settings](material-editor.html#basic)
 1. [Texture Panels](material-editor.html#texture)
 1. [Advanced Settings](material-editor.html#advanced)

## [Settings Bar](material-editor.html#panel_map) ![images/callout_1.svg](images/callout_1.svg)
{: #settings}
Opening a floating preview allows visualization of the texture during its development.
<!-- TODO: This content is from the old source.  It needs heavy editing-->

#### Back Arrow
<!-- TODO: Add a back button image-->
Walks back though the current material or the previously selected materials.  For instance materials with textures have multiple layers.  Use this arrow to get back to the parent material from the texture details.

#### Forward Arrow
<!-- TODO: Add a forward button image-->
Walks back though the current material or the previously selected materials.  For instance materials with textures have multiple layers.  Use this arrow to get back to the recently used texture from the parent material.

#### Currently selected material name ![images/material_editor.png](images/material_editor.png)
<!-- TODO: Add a texture image image and a procedural icon-->
Displays the current material name and level.  For instance, if there is a texture or a material procedural level the ">" will be shown. A good place to see where the editor is in a material.

#### Tools Menu ![images/library_default.png](images/library_default.png)
Displays the [Tools menu](material_editor.html#tools-menu).  This is an extensive menu of commands, settings and utilities related to materials.

#### Help ![images/help_topics.png](images/help_topics.png)

## Materials List ![images/callout_2.svg](images/callout_2.svg)
{: #material_list}


Previews
Displays the preview thumbnail.

##### To display context menus

>Right-click a thumbnail to display the [id="a5" style="position: relative;">material context menu]().
>Right-click the blank area to display the [id="a28" style="position: relative;">new material context menu]().

###  [Add new](materialeditor.html#create-new)![images/add.png](images/add.png)
Opens the Render Content [library](libraries.html) of materials.
The materials in the library act as templates for creating materials in the model.

### Window blind control
Closes the editor.
Name
Names the material.
 **Note** : When a texture or image file is dragged to a Rhino object, a material with that image is assigned to the object.
Basic Settings
All materials have basic settings. The default material is white and matte, with no reflectivity or transparency.

## [Material Name](material-editor.html#panel_map) ![images/callout_3.svg](images/callout_3.svg)
{: #name}

## [Basic Material Panel](material-editor.html#panel_map) ![images/callout_4.svg](images/callout_4.svg)
{: #basic}

## [Texture Material Panel](material-editor.html#panel_map) ![images/callout_5.svg](images/callout_5.svg)
{: #texture}

## [Advanced Material Panels](material-editor.html#panel_map) ![images/callout_6.svg](images/callout_6.svg)
{: #advanced}

## Tools menu ![images/library_default.png](images/library_default.png)
{: #tools_menu}
These settings also appear on right-click context menus for the thumbnail previews and the thumbnail background.

### Assign to Selection
Assigns the current material to selected objects.

#### To assign a material to objects

>![images/number-1.png](images/number-1.png)Click **Assign to Selection**.
>![images/number-2.png](images/number-2.png)In the Rhino viewport, select the target objects.

#### To pre-select objects

>![images/number-1.png](images/number-1.png)In the Rhino viewport, select the target objects.
>![images/number-2.png](images/number-2.png)Click **Assign to Selection**.

 **Note** : The target objects can be selected either before or after clicking Assign to Selection.

#### To drag and drop materials to objects

>Drag the material from the thumbnails or list onto the target objects.

 **Note** : Drag and drop works for only one object at a time.

### Assign to Layers
Assigns the current material to layers.

#### To assign a material to layers

>![images/number-1.png](images/number-1.png)Click **Assign to Layers**.
>![images/number-2.png](images/number-2.png)In the **Choose Layers** dialog box, check the boxes for the material assignment.

#### To assign materials from the Layers panel

>![images/number-1.png](images/number-1.png)In the ** [Layer](layer.html) ** panel, select one or more layers and click the ** [Material](layer.html#material) ** column.
>![images/number-2.png](images/number-2.png)In the **Layer Material** dialog box, select the material to assign.

#### To drag and drop materials to objects

>Drag the material from the thumbnails or list onto the target layer.

 **Note** : Drag and drop works for only one layer at a time.

### Select Objects
Select objects in the model for material assignment.

### Create New Material
Opens the Render Content [library](libraries.html) of materials.
The materials in the library act as templates for creating materials in the model.

### Import Material from File
Imports materials from a saved Rhino .rmtl file.

### Save to File
Saves a material to a Rhino .rmtl file.

### Change Type
Changes the material to a different type.
Types

### Start from scratch
Provides templates for materials.

#### Import from file
Imports materials from a saved Rhino .rmtl file.

####  [Basic Material](materialeditor.html#basic-settings)

####  [Blend Material](materialeditor.html#material-blend)

####  [Composite Material](materialeditor.html#material-composite)

### Start from existing
Displays the materials in the model to use as templates.

### Change Type (Copy Similar Settings)
Changes the material to a different type.
The default behavior depends on the current state of the [Rendering Options](rendering.html) &gt; ** [Copy similar settings when content type is changed](rendering.html#copy-similar-settings-when-content-type-is-changed) ** box. If checked, compatible settings from the old content will be copied to the new one.

### Reset to Defaults
Changes all of the material settings to the default white, matte, non-reflective, untextured material.

### Copy
Copies the selected material to the Windows Clipboard. The Clipboard can then be pasted into the editor to create a new material or pasted directly into a folder to create a [library](libraries.html) file.

### Paste
Creates a new material based on the contents of the Clipboard.

### Paste as Instance
Creates a new material based on the contents of the Clipboard that is linked to the original through instancing.

### Delete
Deletes the selected material.

### Rename
Renames the selected material.

### Duplicate
Copies the selected material to a new material with the same settings.

### Remove Instancing
Removes the connection between [instanced](#paste-as-instance) materials.
{% include_relative snippets/snippet-contenteditorpreviewoptions.md %}
### Content Filter
Opens the **Content Filters** dialog box.
{% include_relative snippets/snippet-contentfilters.md %}
### Properties
Opens the **Preview Properties** dialog box.
{% include_relative snippets/snippet-previewthumbnails.md %}&#160;

## See Also
{% include_relative snippets/alsosee-materialsandtextures.md %}

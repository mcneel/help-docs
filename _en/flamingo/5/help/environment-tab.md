---
title: Environment Panel
---

# ![images/environment.svg](images/environment.svg) {{page.title}}
{: #environment-tab}
Environments are not only what can be seen in the background of a rendering, but control an infinite sphere surrounding the model. Objects within the scene will reflect and refract the environment. The environment sphere is not an object that you can select, but a reference surface for background effects.

The Environment affects the visible part of the background and reflections.  For effects that affect lighting the scene, see the [Sky](sun-and-sky.html) help topic.

Flamingo comes with a special environment called *[Default Flamingo Environment](environment.html)*.  This environment will sync to the current [Lighting Preset](lighting-tab.html). By using [Lighting presets](lighting-tab.html), both the Lighting and environment will be set to appropriate scene defaults.

![images/environment-editor-panel.svg](images/environment-editor-panel.svg){:  #panel_map height="600px" style="float: right"}

##### Where can I find this command?
 1. ![images/environments.png](images/environments.png)Environment Tab
 1. ![images/icon-render.png](images/icon-render.png)Render Tools Toolbars > ![images/environments.png](images/environments.png) Environment Editor
 1. ![images/menuicon.png](images/menuicon.png)Menus > Render Pulldown > Environments Editor
 1. Command > EnvironmentEditor

The Environment Editor Panel is split into discrete sections.  Based on the environment type, the advanced panels may vary.

Colors and textures can be dragged from the color swatch and dropped onto any other color swatch or control in the Material Editor, [Texture Palette](texturepalette.html), or [Environment Editor](environmenteditor.html).
Environment Panel

 1. [Background Type](#type)
 1. [Settings Bar](#settings)
 1. [Environment List](#environment_list)
 1. [Window Divider](#divider)
 1. [Environment Properties Section](#properties)
 1. [Name](#name)
 1. [Environment Property Panels](#panels)

## [Background Type](#panel_map) ![images/callout_1.svg](images/callout_1.svg)
{: #type style="clear: both;"}
Select the type of background for the model.  [Environment](#flamingo-environment) is an all inclusive rendering environment and should be the default setting for Flamingo.  The other three settings present a much more simplified set of settings that reflect older ways of defining backgrounds. For more information see the [Rhinoceros Simple Background](http://docs.mcneel.com/rhino/5/help/en-us/commands/environmenteditor.htm#Basic_settings) topic

The reset of this help topic covers the Environment type.

## [Settings Bar](#panel_map) ![images/callout_2.svg](images/callout_2.svg)
{: #settings}
Use this bar to help navigate the Environment list.

#### ![images/met_leftarrow.png](images/met-leftarrow.png) Back Arrow
Walks back through the current environment or the previously selected environments.  For instance an environment with reflective or refractive layers.  Use this arrow to get back to the parent environment from the reflection or refraction details.

####  ![images/met_rightarrow.png](images/met-rightarrow.png) Forward Arrow
Walks forward through the previously selected environments.  For instance an environment with reflective or refractive layers.  Use this arrow to get forward to the parent environment from the reflection or refraction details.

#### ![images/material_editor.png](images/material_editor.png)![images/texture-2dchecker.png](images/texture-2dchecker.png) Currently selected environment name
Displays the current environment name and edit level.  For instance, if there is a reflective or refractive level a ">" is shown. A good place to see where the environment is current.

#### ![images/library_default.png](images/library_default.png) Tools Menu
Displays the [Tools menu](#tools-menu).  This is an extensive menu of commands, settings and utilities related to environments.

#### ![images/help_topics.png](images/help_topics.png) Help

## [Environment List](#panel_map) ![images/callout_3.svg](images/callout_3.svg)
{: #environment_list}
This lists all the environments contained in the model. One Environment will be selected as the current environment. The current environment is used in the rendering. Yellow corners will show up surrounding the current Environment.

From this list:

* Click on an Environment to make it current. Once selected the environment's properties will show in the panels below. See [Render Materials Properties](#properties) for more information
* Scroll up and down in the list to see all the environments in the model.
* Drag and drop an environment from this list onto any viewport to set it current.
* Add a new Environment using the Add New Button ![images/add_material.png](images/add_material.png) at the bottom of the list.
* Right-click a thumbnail to display the Environment context menu
* Right-click the blank area to display the New Environment Context Menu

###  ![images/add_material.png](images/add_material.png) Add new environment
{: #add_environment}
Scroll down to the bottom of the Environment list to see the add icon.

Opens the Render Content [library](libraries.html) of environments.
The environments in the library act as templates for creating environments in the model.

### Environment Context Menu
{: environment_context}
This menu is available by right click on a environment listing.  See the [Tools Menu](#tools_menu) for details on the many options in this menu.

### New Environment Context Menu
{: new_envrionment_context}
This menu is available by right-clicking on a blank area of the Environment List.

#### ![images/toolbarlus.png](images/toolbarplus.png) Create New Environment
Creates a new Flamingo Environment.

#### ![images/import.png](images/import.png) Import Environment from File...
Use this command to select a previously exported Environment.

#### ![images/paste.png](images/paste.png) Paste
Creates a new environment based on the contents of the Clipboard.

#### ![images/pasteasinstance.png](images/pasteasinstance.png) Paste as Instance
Creates a new environment based on the contents of the Clipboard that is linked to the original through instancing.

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
Floats the preview image in a re-sizable window.

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

## [Window Divider](#panel_map) ![images/callout_4.svg](images/callout_4.svg)
{: #divider}
Drag on this divider to change the length of the Environment List versus the length of the Environment Properties Section.

## [Environment Properties Section](#panel_map) ![images/callout_5.svg](images/callout_5.svg)
{: #properties}

### [Environment Name](#panel_map) ![images/callout_6.svg](images/callout_6.svg)
{: #name}
This is the name of the environment. The environment name is also saved as the file name when exporting the environment to the library. **Note:** Environments are stored in the Rhino model, unique environments can have the same name in different Rhino models.

### [Environment Panels](l#panel_map) ![images/callout_7.svg](images/callout_7.svg)
{: #panels}
The Environment Properties section is filled with a number of direct Environment panels. Clicking on the grey title bar will rollup the environment panel, hiding the contents of that panel.  Click on the title bar again to show contents.

Environment Panels will vary based on the type of environment and the current active environment level. For more information on specific environment panels see [Flamingo Environment](environment.html)

## Tools Menu ![images/library_default.png](images/library_default.png)
{: tools_menu}
These settings also appear on right-click context menus for the thumbnail previews and the thumbnail background.

#### ![images/currentenvironment.png](images/currentenvironment.png) Set as Current Environment
This sets the target environment current.  The current environment will be used in the next rendering.

#### ![images/toolbarlus.png](images/toolbarplus.png) Create New Environment
Creates a new Flamingo Environment.
<!-- This comes from the page http://docs.mcneel.com/rhino/5/help/en-us/popup_moreinformation/materialthumbnail_contextmenu.htm -->
These settings also appear on right-click context menus for the thumbnail previews and the thumbnail background.

#### ![images/import.png](images/import.png) Import Environment from File
Imports environments from a saved Rhino .renv file.

#### ![images/savetofile.png](images/savetofile.png) Save to File
Saves an environment to a Rhino .renv file.

#### ![images/changetype.png](images/changetype.png) Change Type
Changes the environment to a different type.

#### ![images/changetype.png](images/changetype.png) Change Type (Copy Similar Settings)
Changes the environment to a different type.
The default behavior depends on the current state of the [Rendering Options](http://docs.mcneel.com/rhino/5/help/en-us/options/rendering.htm) >  [Copy similar settings when content type is changed](http://docs.mcneel.com/rhino/5/help/en-us/options/rendering.htm#Copy_similar_settings_when_content_type_is_changed)  box. If checked, compatible settings from the old content will be copied to the new one.

#### ![images/reset.png](images/reset.png) Reset to Defaults
Changes all the environment settings to the default Solid color background (Black), reflected background, Sky and Refracted Background visible.

#### ![images/copy.png](images/copy.png) Copy
Copies the selected environment to the Windows Clipboard. The Clipboard can then be pasted into the editor to create a new environment or pasted directly into a folder to create a [library](libraries.html) file.

#### ![images/paste.png](images/paste.png) Paste
Creates a new environment based on the contents of the Clipboard.

#### ![images/pasteasinstance.png](images/pasteasinstance.png) Paste as Instance
Creates a new environment based on the contents of the Clipboard that is linked to the original through instancing.

#### ![images/delete.png](images/delete.png) Delete
Deletes the selected environment.

#### ![images/rename.png](images/rename.png) Rename...
Renames the selected environment.

#### ![images/duplicate.png](images/duplicate.png) Duplicate
Copies the selected environment to a new environment with the same settings.

#### ![images/removeinstancing.png](images/removeinstancing.png) Remove Instancing
Removes the connection between [instanced](#paste-as-instance) environments.

{% include_relative snippets/snippet-contenteditorpreviewoptions.md %}

#### ![images/contentfilter.png](images/contentfilter.png) Content Filter
Opens the [Content Filters](content_filters.html) dialog box.

#### ![images/rename.png](images/rename.png) Properties
Opens the [Preview Properties](previewproperties.html) dialog box.

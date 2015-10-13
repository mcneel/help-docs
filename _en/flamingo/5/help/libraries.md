---
---

# Library Panel
The Libraries command opens the Libraries panel, to manage libraries of materials, textures, and environments.
Render content can be saved to files creating external libraries that can be shared between models. Content can also be dragged between Rhino sessions and into a folder.

Color swatches can be dragged and dropped in the same way.

The Libraries panel displays a view into the content folders you have set up. Use this to drag and drop content into the model or to store document content to a location outside the model.

Materials are simply files on your hard driver.  Library folders are simply Windows folders.  You can copy and paste and move around folders just as you would any Windows file or folder.

Use the address bar at the top of the Libraries tab to navigate to any folder on your computer.

Quickly navigate back to the Default Library locations using the wrench icon at the upper right. ![images/library_defaults.png](images/library_defaults.png)

## Material Library
{: #material}
Materials in libraries are files on the hard drive.  Once assigned to the model, the material is then stored and saved in the model.  Any changes to the assigned material will not change to original material on the hard drive.

Drag and drop materials to assign materials to the model. Materials can be assigned to:

#### Layer Assignment
Drag a material directly onto the layer name in the Layer Panel. This is the recommended method as by default any object on the layer will adopt the material assignment. Later changes to the material can be quite quick by simply dropping anither material on the layer.

#### Object Assignment
Drag a material directly onto an object in any viewport. This will override the By Layer material to a By Object assignment. 

#### Block Assignment
Drag onto a block and any ByParent objects in the block will adopt that material.  Any object wihin the block that has a ByParent material source will pickup the blocks material.

## Plant Library
{: #plant}
Plants in libraries are Rhino files on the hard drive.  Once placed in the model, the plant is then stored and saved in the model.  Any changes to the assigned material will not change to original material on the hard drive.

Drag and drop plants into a viewport to place plants into the model. 

## Environment Library
{: #environment}
This is the Environment Library
<!-- TODO: This needs to be filled out -->

## Library Settings
{: #settings}
Set up content libraries in Options > Libraries.

![images/options.png](images/options.png)Libraries Options
&#160;

### Where can I find this command?
![images/options.png](images/options.png)Toolbars
 [id="a6" style="position: relative;">Properties]() 
 [id="a7" style="position: relative;">Standard]() 
 [id="a8" style="position: relative;">Tools]() 
![images/menuicon.png](images/menuicon.png)Menus
 [id="a9" style="position: relative;">Tools]() 
Options
![images/ctrlplus.png](images/ctrlplus.png)Shortcut
Libraries


### Show render content
Changes the default location of [content libraries](libraries.html) for this computer.

#### Use default library location (My Documents)
By default, the [content libraries](libraries.html) are a subfolder of the *My Documents* folder.

#### Custom
Sets a custom [library](libraries.html) location.

####  **Browse** 
Open file browser to specify file.

### Show &quot;Documents&quot; folder
In the [Libraries panel](libraries.html), the designated Documents folder will display in the menu.

### Show custom folders
In the [Libraries panel](libraries.html), designated custom folders will display in the menu.



### Organizing Libraries
{: Orgainzing Libraries}
Libraries are simply files.  You can copy and paste and move around folders.
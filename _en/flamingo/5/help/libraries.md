---
---

# Library Panel
The Libraries command opens the Libraries panel, to manage libraries of materials, textures, and environments.
Render content can be saved to files creating external libraries that can be shared between models. Content can also be dragged between Rhino sessions and into a folder.

Color swatches can be dragged and dropped in the same way.

The Libraries panel displays a view into the content folders you have set up. Use this to drag and drop content into the model or to store document content to a location outside the model.

Materials are simply files on your hard driver.  Library folders are simply Windows folders.  You can copy and paste and move around folders just as you would any Windows file or folder.

Use the address bar at the top of the Libraries tab to navigate to any folder on your computer.

Quickly navigate back to the Default Library locations using the wrench icon at the upper right. ![images/library_default.png](images/library_default.png)

#### Organizing Libraries
{: organizing_libraries}
Libraries are simply files.  You can copy and paste and move around folders. Use Windows Explorer to edit the folders and documents.


## Material Library
{: #material}
Materials in libraries are files on the hard drive.  Once assigned to the model, the material is then stored and saved in the model.  Any changes to the assigned material will not change to original material on the hard drive.

Drag and drop materials to assign materials to the model. Materials can be assigned to:

#### Layer Assignment
Drag a material directly onto the layer name in the Layer Panel. This is the recommended method as by default any object on the layer will adopt the material assignment. Later changes to the material can be quite quick by simply dropping another material on the layer.

#### Object Assignment
Drag a material directly onto an object in any viewport. This will override the By Layer material to a By Object assignment. 

#### Block Assignment
Drag onto a block and any ByParent objects in the block will adopt that material.  Any object within the block that has a ByParent material source will pickup the blocks material.

## Plant Library
{: #plant}
Plants in libraries are Rhino files on the hard drive.  Once placed in the model, the plant is then stored and saved in the model.  Any changes to the assigned material will not change to original material on the hard drive.

Drag and drop plants into a viewport to place plants into the model. 

<!-- TODO: Where do we explain plants and what you can do with them? -->

## Environment Library
{: #environment}
Environments can be saved in the library.  This allows Environment settings to be passed from one model to another.  For more details, got to [Environments](environment-tab.html)

## Library Settings
{: #settings}
![images/options.png](images/options.png)Libraries Options are used to change the library defaults shown under the ![images/library_default.png](images/library_default.png) menu.

#### Where can I find this command?
 1. Libraries Tab > ![images/library_default.png](images/library_default.png) in the upper right of the Libraries panel > Settings...
 1. ![images/options.png](images/options.png)Toolbars >![images/icon-properties.png](images/icon-properties.png)Properties Toolbar > ![images/documentpropertiesbutton.png](images/documentpropertiesbutton.png)Document Properties > Libraries
 1. ![images/menuicon.png](images/menuicon.png)Menus > Tools Pulldown > Options > Libraries.

### Show render content
Use this to show or hide the default render content location.

#### Use default library location (My Documents)
By default, the [content libraries](libraries.html) are a subfolder of the *My Documents* folder.

#### Custom
Sets a custom [library](libraries.html) location.  Changes the default location of [content libraries](libraries.html) for this computer.

##### Browse Button 
Open file browser to specify file.

#### Show "Documents" folder
In the [Libraries panel](libraries.html), the designated Documents folder will display in the menu.

#### Show custom folders
In the [Libraries panel](libraries.html), designated custom folders will display in the menu.

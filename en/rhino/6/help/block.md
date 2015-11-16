---
---


# Block
{: #kanchor155}
{: #kanchor154}
{: #kanchor153}
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/block.png](images/block.png) [Block](block-toolbar.html)  [Main](main-sidebar-toolbar.html)  [Main1](main1-toolbar.html) 
Menus
Edit
Blocks![images/menuarrow.gif](images/menuarrow.gif)
Create Block Definition
Shortcut
 [Ctrl](ctrl-key.html) +B
The Block command defines a block object from the selected objects and replaces the selected objects with an instance of the block.
Using blocks lets you
Create parts libraries.Update all instances by modifying the block definition.Keep a smaller model size by using block instances instead of copying identical geometry.Use the [BlockManager](blockmanager.html) command to view information about the blocks defined in the model.Use the [Insert](insert.html) command to place block instances into your model, which scales and rotates the instance.Define a block in a model
 [Select](select-objects.html) the objects. [Pick](pick-location.html) a base point for the block.This is the point around which the instance will be located, scaled, and rotated when it is inserted.A block control point is placed at the base point of the block.Type a name for the block definition.Block Definition Properties
Name
The name of the block definition.
Description
Optional descriptive information.
Hyperlink
Adds hyperlink information to a block definition. This information can be retrieved with the [Hyperlink](hyperlink.html) command.
Description
A description of the URL.
URL
A web address. Click the address to open the page in the default browser.
Define a block by inserting another file into a model
Use the [Insert](insert.html) command with theInsert asoption set toBlock Instance.A block definition will be added to the model.Define a block by dragging another file onto a model
 [Drag and drop](drag-and-drop-file.html) a supported file from Windows Explorer onto the model.Specify theInsert fileoption.A block definition will be added to the model.To redefine a block
Follow the steps for defining a block and re-use the same block name.Note
Do not create blocks in a model that are named the same as the model itself.When inserting a file with the [Insert](insert.html) command, the file's [ModelBasepoint](modelbasepoint.html) will determine how the geometry is being located in the new file.Block Instances and Layers
The properties of the *geometry* (curves, surfaces, etc.) that are contained in the block instance are controlled either by the layer properties or object properties of the geometry itself. Block instances that you insert to the model insert onto the current layer and can be moved to any other layer. There is no relationship between the block instance's layer and the geometry contained in the block. For example, the block geometry does not change to match the layer color onto which the block instance is inserted.
When the block contains objects on a specific layer, turning that layer off will turn off only the objects on that layer. However, if the layer the block instance is inserted on is turned off, all of the objects will disappear.
Locking Layers
When you lock a layer, only the layer that contains the *insertion point* of the block instance is locked. If a block has objects that are on the locked layer, but the block instance insertion point is not on that layer, the object itself is not locked because the controlling factor is the layer of the block insertion point.
Groups
 [Grouped](group.html) objects will not maintain their grouped status inside a block.
Properties By Parent
This option is only useful when creating [blocks](#).
Before you make a block, assign objects color toBy parent, then make the block and include the object.
The layer that is current when the block is inserted will control the color and visibility of the objects that were set toBy parent.
If color is setBy layerorBy object, that color is maintained regardless of which layer was current when the block was inserted or the block reference layer.
Assign the object color to "by parent" in Properties has to happen before the block is made or after in the BlockEdit command.
If an object's properties areBy Parent, the object will continue to draw as if set toBy Layer. However, when the object is part of a block, it takes on the properties of the block instance (layer or property).
Linetypes are not supported in theBy parentsetting.
Example using Parent material
Set the material for Layer 1.Draw a Sphere on Layer 1.Select the sphere, and set its material property toParent.Use the [Block](#) command to turn the sphere into a block.Set the material for Layer 2 to a different material.Insert the block from step 4 on Layer 2.The sphere will display the material assigned to Layer 2 because the block instance is on Layer&#160;2, and the objects in the block are assigned their materialBy Parent.Select the block instance, and set its material property to object.The sphere will change to the object material.For nested blocks: Blocks made of nested blocks that include objects set to the Parent material are not affected by further nesting.
See also
 [Work with blocks, groups, and worksessions](sak-blocksgroups.html) 
 [McNeel Wiki: Using blocks](http://wiki.mcneel.com/rhino/usingblocks) 
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](block.html) 


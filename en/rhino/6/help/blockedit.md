---
---


# BlockEdit
{: #kanchor156}
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/blockedit.png](images/blockedit.png) [Block](block-toolbar.html) 
Menus
Edit
Blocks![images/menuarrow.gif](images/menuarrow.gif)
Edit Block In Place
The BlockEdit command allows selecting a block instance to change the block geometry and update the block definition.
Steps
Select a block instance to edit.Or, double-click a block instance.The block geometry opens in the Rhino window. All other objects are locked.You can now edit the geometry in the block using any editing techniques.When all changes are complete, clickOK.Command-line options
PromptToEditLinkedBlocks
 [Linked blocks](insert.html#link) are not stored in the Rhino file, but are a connection to an external model. To edit linked blocks, Rhino opens the external model in a separate instance of Rhino. The current editing session is paused until the external file is locked.
Yes
TheYesoption prompts to open a [linked](insert.html#link) block.
No
TheNooption opens the linked block without prompting.
In theEdit Linked Blockdialog box, checking theDon't ask this question again...box automatically sets thePromptToEditLinkedBlockstoNo.
Block Edit options
TheBlock Editdialog box displays the block name and a list of any blocks nested in it.
 **Add Object** 
Adds selected objects to the block definition. If the selected object is a block, this becomes a nested block and will display in the tree the next time theBlockEditcommand is run.
The object added is copied to the block definition and the original object remains in the model.
 **Remove Object** 
Removes selected objects from the block definition.
When the block is updated, the removed objects are added to the model as separate individual objects.
 **Set Base Point** 
Repositions the block insertion point.
When the block is updated, the block instance will shift so the new insertion point is placed at the block insertion location.
Notes
Hidden or locked objects are not supported in block definitions. therefore, a warning dialog will appear if you have locked or hidden objects giving you the option to leave objects hidden or locked and remove them from the block definition or to show and or unlock the objects to make further edits.Linked blocks in use by another user cannot be edited.See also
 [Work with blocks, groups, and worksessions](sak-blocksgroups.html) 
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](blockedit.html) 


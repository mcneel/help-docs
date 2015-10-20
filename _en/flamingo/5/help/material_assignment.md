---
---

# Material Assignment ![images/materialtab.png](images/materialtab.png)


### Assign material by
Using a plug-in library, rendering properties can be assigned to layers, or to objects that will be used with the basic Rhino renderer.

#### Layer
The object inherits the render material assigned to the layer. To change the material assignment of the layer, use the [ **Layers** ](layer.html) dialog box.
 **Note** : Deleting a material from the ** [Material Editor](materialeditor.html) **, returns all objects that had the deleted material assigned to assignment by layer.

#### Parent
The object inherits the render material from its parent object.

#### Object
Render materials are assigned to individual objects and are used by Rhino's built-in renderer.
See ** [MaterialEditor](materialeditor.html) **.


To assign a material to objects
1.	On the Tools menu, click Assign to Selection.
2.	In the Rhino viewport, select the target objects.
To pre-select objects
1.	In the Rhino viewport, select the target objects.
2.	On the Tools menu, click Assign to Selection.
To drag and drop materials to objects
Drag the material from the thumbnails or list onto the target objects.

# Materials
Materials can be assigned to layers or individual objects from materials either saved in the current model or from material libraries.
Assigning materials by layer is the recommended method. Assign materials by object if you have only a few objects that you do not want on separate layers.

## Assign materials to layers
{: #bylayer}
{: #assign-materials}
Assigning materials by layer assigns a material to all objects on a layer.

##### Assign a material to a layer
1. In Rhino, open the **Layers** dialog box.
1. Select one or more layer names, and click the **Material** column.
1. In the **Material Editor** dialog box, under **Assign By**, click **Plug-in**.
1. Click the **Browse** button.
1. In the **Flamingo Materials** dialog box, select a material either from the **Materials in Model** palette or from the **Material Libraries**, and click **OK**.

##### Drag a material to a layer
{: #drag-dropmaterialtolayer}
1. In Rhino, open the **Layers** dialog box.
1. In the **Flamingo nXt [Control Panel](welcome.html#control-panel) **, on the **Materials** tab, drag a material either from the **Materials in Model** palette or from the **Material Libraries** on to a layer name.

##### Remove a material from a layer
{: #detachmaterialfromlayer}
1. In Rhino, open the **Layers** dialog box.
1. Select one or more layer names, and click the **Material** column.
1. In the **Material Properties** dialog box, under **Assign By**, click **Basic**.
1. If desired, reset the material color.

## Assign material to objects
{: #byobject}
You can assign materials from the material libraries to a layer or object.
Assigning materials by layer is the recommended method. Assign materials by object if you have only a few objects that you do not want on separate layers.

##### Assign a material through object properties
1. Select objects.
1. On the **Edit** menu, click **Object Properties** command to edit the object.
1. In the ** [Properties](properties-object.html) ** dialog box, on the **Material** page, under **Assign By**, click **Plug-in**, and then click the **Browse** button.
1. In the **Flamingo Materials** dialog box, select a material either from the **Materials in Model** palette or from the **Material Libraries**, and click **OK**.

##### Drag a material onto a single object
{: #drag-dropmaterialtoobject}

>In the **Flamingo nXt [Control Panel](welcome.html#control-panel) **, on the **Materials tab**, drag a material either from the **Materials in Model** palette or from the material library onto an object.

##### Assign a material to selected objects
1. Select objects.
1. In the **Flamingo nXt [Control Panel](welcome.html#control-panel) **, on the **Materials** tab, right-click a material from the **Materials in Model** palette.
1. On the menu, click **Assign to Selected Objects**.

## Select objects with material assignment
{: #select-objects-with-material-assignment}
1. In the **Flamingo nXt [Control Panel](welcome.html#control-panel) **, on the **Materials** tab, right-click a material from the **Materials in Model** palette.
1. On the menu, click **Select Objects with this Material**.

## Remove a by-object material assignment
{: #removematerialfromobject}
1. Select objects.
1. On the **Edit** menu, click **Object Properties**.
1. In the ** [Properties](properties-object.html) ** dialog box, on the **Material** page, under **Assign by**, select **Layer**.

## Manage Materials
{: #manage-materials}
1. On the **Flamingo nXt** menu, click **Control Panel**.
1. In the **Control Panel**, click the **Materials** tab.
&#160;
![images/materialtab-001.png](images/materialtab-001.png)

>![images/01.png](images/01.png)New material menu
>![images/02.png](images/02.png)Assign to object
>![images/03.png](images/03.png)Assign to layer
>![images/04.png](images/04.png)View menu
>![images/05.png](images/05.png)Materials in Model palette
>![images/06.png](images/06.png)Material library name
>![images/07.png](images/07.png)Material Library folders

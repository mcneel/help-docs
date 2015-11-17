---
title: 재질 적용
---

# ![images/paint.svg](images/paint.svg) {{page.title}}
Objects in the scene have a material source. This is the place where they adopt their rendering material.  Materials can be assigned in different ways. The method used to assign materials has a great effect on the how easy the model is to change and maintain in the future.

Materials can be assigned in three ways. The three are a hierarchy, so an assignment lower on the list will overwrite an assignment above. The three ways are:

 1. [Layers](#bylayer) - All objects on the layer will adopt this material, unless they are in a block or have a specific object assignment.
 2. [Parent](#byparent) - This is used for objects within blocks.  Objects with a By Parent assignment will look to the block insert for the material.
 3. [Individual objects](#byobject) - Materials can be assigned directly to an object, overwriting any other material assignments.

Assigning materials by layer is the recommended method. Using By layer makes it very easy to change the material of all the objects on a layer. Use By object assignment if you have only a few objects that you do not want on separate layers.

Imported files may have any one of these three assignments. Many imported files will have By Object assignments.  It may take a lot of work to convert the model to By Layer assignments, but it can be beneficial if there is a lot of editing to the render materials planned.

Once materials are assigned, the material will be saved in the current model.  Editing the material will not effect that material in other models.

## Assign materials to layers
{: #bylayer}
Assigning materials by layer assigns a material to all objects on that layer. This is the default method of assignment. To change the material assignment of the layer, use the [Layers](http://docs.mcneel.com/rhino/5/help/en-us/commands/layer.htm) dialog box.
Note: Deleting a material from the [Material Editor](material-editor.html) returns all objects that had the deleted material assigned to assignment by layer.

##### Drag a material to a layer
{: #drag-dropmaterialtolayer}
1. In Rhino, open the [Layers](http://docs.mcneel.com/rhino/5/help/en-us/commands/layer.htm) dialog box.
1. In the [Materials List](material-editor.html#material_list), on the Library tab or the Material Editor tab, drag a material on to a layer name in the [Layers](http://docs.mcneel.com/rhino/5/help/en-us/commands/layer.htm) dialog.

##### To assign a material to a layer
1. In Rhino, open the [Layers](http://docs.mcneel.com/rhino/5/help/en-us/commands/layer.htm) dialog box.
1. Select one or more layer names, and click the Material column.
1. In the Layer Material dialog box, select a material from the Material drop-down list.

##### 레이어에서 재질 제거
{: #detachmaterialfromlayer}
1. In Rhino, open the [Layers](http://docs.mcneel.com/rhino/5/help/en-us/commands/layer.htm) dialog box.
1. Select one or more layer names, and click the Material column.
1. In the Layer Material dialog box, select the Default Material Material drop-down list.

## Assign material to Parent
{: #byparent}
By parent is a seldom used, but useful, assignment. Objects within a Block instance will retain their By Layer or By Object assignments.  Objects that are using By Parent assignment will adopt the material of the block insertion.  This way objects within a block instance can adopt the material of the parent block.

As an example, a car model might have tires on the tires layer and wheels on the wheel layer. But for rendering the body of the car might vary between individual block instances.  Assign By Parent to the car body.  Then a material can be assigned to the block insert and only the body will adopt that material.

##### To assign a material through object properties
1. 개체를 선택합니다.
1. On the Edit menu, click Object Properties ![images/properties.png](images/properties.png) command to edit the object.
1. In the [Properties](properties-object.html) dialog box, on the Material page ![images/materialtab.png](images/materialtab.png) under Assign By, click By Parent.

## Assign material to objects
{: #byobject}
You can assign materials from the material libraries to a layer or object. Rendering materials are assigned to individual objects and are used by Rhino's built-in renderer.
[재질 편집기](material-editor.html)를 참조하세요.

레이어에 따라 재질을 적용하는 방법을 권장합니다. 별도의 레이어에서 작업하지 않고, 소수의 개체만으로 작업하는 경우에는 개체마다 재질을 적용하십시오.

##### 개체 속성을 통해 재질 적용
1. 개체를 선택합니다.
1. 편집 메뉴에서 개체 속성 ![images/properties.png](images/properties.png)을 클릭하여 개체를 편집합니다.
1. In the  [Properties](properties-object.html)  dialog box, on the Materials page ![images/materialtab.png](images/materialtab.png) under Assign By, click By Object, and then click the Material from the list.

##### Drag a material onto a single object
{: #drag-dropmaterialtoobject}

 * In the [Materials List](material-editor.html#material_list), on the Library tab or the Material Editor tab, drag a material onto an object. The object will highlight when the cursor is in the correct place to drop.

##### Assign a material to selected objects
1. 개체를 선택합니다.
1. In the [Material List](material-editor.html#material_list), on the Library tab or the Material Editor tab, right-click a material from the Materials in Model palette.
1. On the menu, click Assign to Selected Objects.

##### Select objects with material assignment
{: #select-objects-with-material-assignment}
1. In the [Materials List](material-editor.html#material_list), on the Library tab or the Material Editor tab, right-click a material from the Materials in Model palette.
1. On the menu, click Select Objects with this Material.

##### Remove a by-object material assignment
{: #removematerialfromobject}
1. 개체를 선택합니다.
1. 편집 메뉴에서 개체 속성을 클릭합니다.
1. [속성](properties-object.html) 대화상자 재질 페이지의 할당 옵션 아래에서 레이어를 선택합니다.

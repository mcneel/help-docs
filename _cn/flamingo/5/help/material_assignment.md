---
title: 赋予材质
---

# ![images/paint.svg](images/paint.svg) {{page.title}}
场景中的物件都可以有一个材质来源，物件可以用不同途径获得渲染材质，通过正确的材质来源为物件赋予材质，将能够简化赋予材质的过程。

可以通过以下三种材质来源赋予材质，这三种来源具有优先级关系，越后面的优先级越高，通过优先级高的来源赋予的材质将覆盖优先级低的来源赋予的材质。

 1. [图层](#bylayer) - 该图层中所有物件将获得该材质，除非物件本身被赋予了材质或通过图块赋予了材质。
 2. [父物件](#byparent) - 此方法适用于图块中的物件，物件的材质来源如果是“父物件”将获得赋予给图块的材质。
 3. [物件](#byobject) - 材质可以直接赋予给物件，将覆盖物件由其他途径获取的材质。

推荐使用图层为物件赋予材质，通过图层可以为图层中所有的物件赋予材质，即使您想为该图层中某个物件单独赋予材质，也不需要将该物件从图层中分离出来。

导入物件的材质来源有可能是三种来源中的任何一种，许多导入物件来源都是“物件”，将它们的来源都设置为“图层”可能需要耗费一些功夫，但是如果渲染材质需要做很多调整测试的话，这可以为之后的渲染带来方便。

一旦赋予了材质，材质就保存到了当前模型当中，编辑一个模型中的材质不会影响其他模型中的材质。

## 将材质赋予给图层
{: #bylayer}
将材质赋予到图层中的每个物件。这是物件默认的材质来源，在[图层](http://docs.mcneel.com/rhino/5/help/en-us/commands/layer.htm)对话框中可以更改图层的材质。
附注: 从[材质编辑器](material-editor.html)中删除材质，使用了该材质的物件的材质来源将会重新设置为“图层”。

##### 将材质拖放到图层
{: #drag-dropmaterialtolayer}
1. 打开 Rhino 的[图层](http://docs.mcneel.com/rhino/5/help/en-us/commands/layer.htm)对话框。
1. 打开材质库标签页或材质编辑器，从[材质列表](material-editor.html#material_list)中将材质拖放到[图层](http://docs.mcneel.com/rhino/5/help/en-us/commands/layer.htm)对话框中的的图层名称上。

##### 将材质赋予给图层
1. 打开 Rhino 的[图层](http://docs.mcneel.com/rhino/5/help/en-us/commands/layer.htm)对话框。
1. 选取一个或多个图层，点击材质栏。
1. 在图层材质对话框中，从材质下拉列表中选取一个材质。

##### 移除图层的材质
{: #detachmaterialfromlayer}
1. 打开 Rhino 的[图层](http://docs.mcneel.com/rhino/5/help/en-us/commands/layer.htm)对话框。
1. 选取一个或多个图层，点击材质栏。
1. 在图层材质对话框中，选取默认材质。

## 将材质赋予给父物件
{: #byparent}
虽然很少用到以父物件赋予材质的方式，但是这是一种很有用的方式，图块中物件的材质来源为父物件时它依然可以从图层及物件自身获得材质。使用此种材质来源，物件可以获得赋予给父图块引例的材质。

例如，汽车图块中有车身、轮胎、轮毂等，汽车模型的轮胎在轮胎图层，而轮毂在轮毂图层，渲染时需要渲染几种车身材质不同的图块引例，这时就可以只把车身的材质来源设置为父物件，将材质赋予给整个图块时，就只改变车身的材质而不改变轮胎和轮毂的材质。

##### 在物件属性中指定材质来源
1. 选取物件。
1. 在编辑功能表中，点击物件属性 ![images/properties.png](images/properties.png) 编辑物件。
1. 在[属性](properties-object.html)对话框中的材质页面 ![images/materialtab.png](images/materialtab.png) 将材质赋予方式选为父物件。

## 将材质赋予给物件
{: #byobject}
您可以将材质库中的材质赋予给图层或物件， 赋予给物件的渲染材质可以用 Rhino 内置渲染器渲染。
请参考[材质编辑器](material-editor.html)。

推荐使用以图层的方式赋予材质，如果要渲染的物件较少，而且您不想分图层的情况下可以通过以物件的方式赋予材质。

##### 在物件属性中指定材质来源
1. 选取物件。
1. 在编辑功能表中，点击物件属性 ![images/properties.png](images/properties.png) 编辑物件。
1. 在[属性](properties-object.html)对话框中的材质页面 ![images/materialtab.png](images/materialtab.png) 中，从“材质赋予方式”后的下拉菜单中选取“物件”，然后从材质列表中选取一个材质。

##### 拖放材质到单个物件
{: #drag-dropmaterialtoobject}

 * 打开材质库或材质编辑器，从[材质列表](material-editor.html#material_list)中将材质拖动到物件上，将接受材质的物件会呈现高亮显示状态，选取正确的物件然后松开鼠标完成拖放。

##### 将材质赋予给选取的物件
1. 选取物件。
1. 打开材质库或材质编辑器，右键点击[材质列表](material-editor.html#material_list)中要操作的材质。
1. 在弹出的菜单中，点击“赋予给选取的物件”。

##### 以材质选取物件
{: #select-objects-with-material-assignment}
1. 打开材质库或材质编辑器，右键点击[材质列表](material-editor.html#material_list)中要操作的材质。
1. 在弹出的菜单中，点击“选取物件”。

##### 移除物件的材质
{: #removematerialfromobject}
1. 选取物件。
1. 从编辑菜单选择物件属性。
1. 在[属性](properties-object.html)对话框中的材质页面，将材质赋予方式选为“图层”。

---
title: 植物
---

<!-- TODO: Is this  about trees or plants? I can see some confusion on the page. Lots of mentions of "trees" where I think we actually want to say "plant". -->

# ![images/plants.svg](images/plants.svg) {{page.title}}
Flamingo nXt 内建植物创建功能，可以在渲染时快速创建复杂的植物模型，这些植物在模型里是以点云表示，所以不会让模型变大。

![images/plants-001.png](images/plants-001.png)
*Flamingo nXt 的树。*

### 插入 nXt 植物
{: #insert:}
Flamingo 植物是以图块的方式插入的，这些图块包含了构成织物形状的点。

1. 从 Flamingo nXt 菜单选择植物 > 插入植物。
1. 在 Flamingo nXt 植物对话框选取一种植物名称，点击打开。
1. 在命令提示下，指定放置植物的位置。

附注:

* 请确定模型的单位设置是否正确。 
* 植物可以做缩放、复制、旋转等操作。

### 编辑植物
{: #edit}
植物插入后，您可以执行移动、复制与缩放操作。植物将会根据您的操作进行调整。要对植物进行更进一步的编辑，请使用编辑织物相关的指令，对植物进行一些小的修改会计算的很快，当调整较大时程序算法的计算量会很大。

1. 在 Flamingo nXt 菜单，点击 植物 > 编辑植物。
1. 选取要编辑的植物。
1. 对植物进行正确的编辑。
1. 保存并关闭编辑器，Rhino 中的植物将自动更新。

### 使用 Flamingo 2 植物
{: #using-flamingo-2-plants}
1. 从 Flamingo nXt 菜单选择植物 > 插入 Flamingo 2 植物。
1. 在 Flamingo nXt 植物对话框选取一种植物名称，点击打开。
1. 在命令提示下，指定放置植物的位置。

附注:

* 已插入模型里的 Flamingo 2 植物虽然也可以用，但会有一些限制。
* Flamingo 2 的植物与 Flamingo nXt 的植物不一样，而且 Flamingo 2 的植物无法转化成 Flamingo nXt 的植物。

### 植物编辑器
{: tree-editor}
Flamingo 有一个植物编辑器可以创建自定义的树，可以通过现有的几种树的基本模板来创建新的植物。更多详情请参考[植物编辑器](tree-editor.html)主题。

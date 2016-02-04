---
title: Flamingo 入门
---


# ![images/flamingotab.svg](images/flamingotab.svg) Flamingo nXt® 入门
Flamingo nXt 可以在 Rhinoceros ® 内部将模型渲染为高质量、照片级的静态与动画图片文件，Flamingo nXt 5 是 Flamingo 的升级版，并集合了 Rhino 5 内置渲染的功能，此版本仍是开发中的版本（WIP）。

您可以在 [Flamingo nXt 5 下载](http://www.rhino3d.com/download/flamingo/5/beta)页面下载并安装 Flamingo。

参与技术讨论，请访问 [Flamingo Discourse 论坛](http://discourse.mcneel.com/c/rendering/flamingo)。

## 安装

* 安装 Flamingo 5 Beta 测试版必须先安装有先前版本的 Flamingo nXt 。
* 运行  Flamingo nXt 5 需要 Rhino 5 SR12。

下载后通过 RHI 安装器安装完成以后，启动 Rhino 就可以载入了。

获得技术支持、教学、案例以及入门 **Flamingo nXt** 的相关信息，请访问 [Flamingo nXt web site](http://nxt.flamingo3d.com/)。

> [教学](http://nxt.flamingo3d.com/page/tutorials-and-documentation)
> [作品](http://nxt.flamingo3d.com/photo)
> [技术支持](http://nxt.flamingo3d.com/forum)

## Flamingo nXt 控制面板
{: #control-panel}
Flamingo 渲染工具与 Rhino 5 渲染工具整合在一起，Flamingo nXt 控制面板提供了用于模型渲染的设置，包括：

> [材质](materials-tab.html)
> [照明](lighting-tab.html)
> [环境](environment-tab.html)
> [渲染](render-tab.html)

## 进入 Flamingo 控制面板
* 在 Flamingo nXt 5.0 菜单中，点击控制面板。

## 渲染基础
{: #rendering-basics}
要渲染出最终的模型，需要完成下列四个步骤：

 1. [设置材质](material-editor.html)
 1. [设置照明](lighting-tab.html)
 1. [设置环境](environment-tab.html)
 1. [设置渲染条件](render-tab.html)

##### 开始渲染
* 在“渲染”或“Flamingo nXt ”菜单中，点击“渲染”。
* 或在标准工具列中，点击渲染按钮。

### 停止渲染
默认情况下，在您点击停止渲染 按钮之前，图像会在渲染过程中被一遍一遍的逐步精细化，这让您可以在渲染质量和时间消耗之间做一个权衡，渲染时间越久，渲染越接近 &quot;正确&quot 的结果，您可以随时停止渲染。

###  恢复渲染
点击停止渲染按钮在完成当前队列后暂停渲染。
随后按钮变为恢复渲染按钮，I如果当前渲染的队列还没有达到设置的队列数或没有达到设置的渲染时间，点击恢复渲染按钮继续渲染。

通过[渲染窗口](render-window.html)或[文件属性 &gt; Flamingo nXt](documentproperties-flamingo.html) 中的[队列数](render-window.html#number-of-passes)或[时间](render-window.html#time)来设置停止渲染的条件。

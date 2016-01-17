---
title: Flamingo 入门
---


# ![images/flamingotab.svg](http://help.mcneel.com/en/flamingo/5/website/images/flamingotab.svg)Flamingo nXt® 入门
Flamingo nXt 可以在 Rhinoceros ® 内部将模型渲染为高质量、照片级的静态与动画图片文件，Flamingo nXt 5 是 Flamingo 的升级版，并集合了 Rhino 5 内置渲染的功能，此版本仍是开发中的版本（WIP）。

您可以在 [Flamingo nXt 5 下载](http://www.rhino3d.com/download/flamingo/5/beta)页面下载并安装 Flamingo。

参与技术讨论，请访问 [Flamingo Discourse 论坛](http://discourse.mcneel.com/c/rendering/flamingo)。

## 安装

* Flamingo 5 Beta requires a previous version of Flamingo nXt to be installed.
* Rhino 5 Service Release 12 is required to run Flamingo nXt 5.

After downloading and running the RHI installer, start up Rhino.

For technical support, tutorials, examples, and information about how to get started using **Flamingo nXt**, go to the [Flamingo nXt web site](http://nxt.flamingo3d.com/).

>[教学](http://nxt.flamingo3d.com/page/tutorials-and-documentation)
>[作品](http://nxt.flamingo3d.com/photo)
>[技术支持](http://nxt.flamingo3d.com/forum)

## Flamingo nXt 控制面板
{: #control-panel}
This version of Flamingo features an interface integrated with the Rhino 5 rendering tools. The Flamingo nXt Control Panel provides tabs for setting up the model for rendering, including:

>[材质](materials-tab.html)
>[照明](lighting-tab.html)
>[环境](environment-tab.html)
>[渲染](render-tab.html)

## 进入 Flamingo 控制面板
* On the Flamingo nXt 5.0 menu, click Control Panel.

## 渲染基础
{: #rendering-basics}
要渲染出最终的模型，需要完成下列四个步骤：

 1. [设置材质](material-editor.html)
 1. [设置照明](lighting-tab.html)
 1. [设置环境](environment-tab.html)
 1. [设置渲染条件](render-tab.html)

##### 开始渲染
* On the Render or Flamingo nXt menu, click Render.
* Or, on the Standard toolbar, click the Render button.

### 停止渲染
By default, the rendering process will continue refining the image, pass by pass, until you click the Stop Rendering button. This lets you manage the trade-off between time and quality. The longer the rendering continues, the more closely it resembles its fully converged result. You can stop a rendering at any time.

### Resume Rendering
Clicking the Stop Rendering button suspends the rendering process after the current pass completes.
The button then changes to Resume Rendering. If you stop the rendering before reaching the number of passes or the time constraints, you can click the Resume Rendering button to continue.

Use the [Number of passes](render-window.html#number-of-passes) or [Time](render-window.html#time) settings on the [Render Window](render-window.html) or in [Document Properties Flamingo nXt](documentproperties-flamingo.html) to set an automatic stopping point.

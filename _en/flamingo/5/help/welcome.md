---
title: Getting Started with Flamingo
---

<!-- TODO: This page mentions "Work in Progress" and "Flamingo Beta" and has to be updated once Flamingo has been released -->
# ![images/flamingotab.svg](images/flamingotab.svg) Getting Started with Flamingo nXt®
Flamingo nXt creates high quality, photorealistic, still, and animation image files from 3-D models inside Rhinoceros ®. Flamingo nXt 5 is an update to Flamingo which integrates with the built-in rendering features in Rhino 5. This is currently a work in progress version.

Download and install Flamingo from the [Flamingo nXt 5 Download](http://www.rhino3d.com/download/flamingo/5/beta).

You can join the technical discussion on the [Flamingo Discourse Forum](http://discourse.mcneel.com/c/rendering/flamingo).

## Installation

* Flamingo 5 Beta requires a previous version of Flamingo nXt to be installed.
* Rhino 5 Service Release 12 is required to run Flamingo nXt 5.

After downloading and running the RHI installer, start up Rhino.

For technical support, tutorials, examples, and information about how to get started using **Flamingo nXt**, go to the [Flamingo nXt web site](http://nxt.flamingo3d.com/).

> [Tutorials](http://nxt.flamingo3d.com/page/tutorials-and-documentation)
> [Gallery](http://nxt.flamingo3d.com/photo)
> [Technical Support](http://nxt.flamingo3d.com/forum)

## The Flamingo nXt Control Panel
{: #control-panel}
This version of Flamingo features an interface integrated with the Rhino 5 rendering tools. The Flamingo nXt Control Panel provides tabs for setting up the model for rendering, including:

> [Materials](materials-tab.html)
> [Lighting](lighting-tab.html)
> [Environment](environment-tab.html)
> [Render](render-tab.html)

## To access the Flamingo control panel
* On the Flamingo nXt 5.0 menu, click Control Panel.

## Rendering Basics
{: #rendering-basics}
Rendering your finished model comprises four basic steps:

 1. [Set up materials](material-editor.html)
 1. [Set up lighting](lighting-tab.html)
 1. [Set up an environment](environment-tab.html)
 1. [Set up rendering conditions](render-tab.html)

##### To start a rendering
* On the Render or Flamingo nXt menu, click Render.
* Or, on the Standard toolbar, click the Render button.

### Stop Rendering
By default, the rendering process will continue refining the image, pass by pass, until you click the Stop Rendering button. This lets you manage the trade-off between time and quality. The longer the rendering continues, the more closely it resembles its fully converged result. You can stop a rendering at any time.

###  Resume Rendering
Clicking the Stop Rendering button suspends the rendering process after the current pass completes.
The button then changes to Resume Rendering. If you stop the rendering before reaching the number of passes or the time constraints, you can click the Resume Rendering button to continue.

Use the [Number of passes](render-window.html#number-of-passes) or [Time](render-window.html#time) settings on the [Render Window](render-window.html) or in [Document Properties Flamingo nXt](documentproperties-flamingo.html) to set an automatic stopping point.

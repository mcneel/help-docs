---
layout: fullwidth-page
---

# Getting Started with Flamingo nXt 5®
 
## Installation

Flamingo 5 Beta requires a previous version of Flamingo nXt to be installed.
Rhino 5 Service Release 12 is required to run Flamingo nXt 5.
After downloading and running the RHI installer, start up Rhino.
Startup notes

This version of Flamingo features an interface which is integrated with the Rhino 5 rendering tools. This made several necessary changes to the rendering interface. At this time it is important to find the Flamingo interface when first starting up Flamingo:

The Flamingo control panel can be found under the Render Pulldown > Flamingo nXt 5 > Show Control Panel
The Flamingo nXt tab contains Flamingo specific controls:
Sky
Lighting Manager
Custom Lighting controls
Render Options
Once in the control panel, Right-click in the tab area and select the panels:
Libraries
Environment
Groundplane
Etc…
 
## To access the Flamingo control panel
  * On the **Flamingo nXt** menu, click **Control Panel**.

  ## The Flamingo nXt Control Panel
The **Flamingo nXt**  **Control Panel** provides tabs for setting up the model for rendering, including:

 *  [Materials](..\materials\materials-tab.html) 
 *  [Lighting](../lighting/lighting-tab.html) 
 *  [Environment](../environment/environment-tab.html) 
 *  [Render](../render/render-tab.html) 

## Rendering Basics
 
Rendering your finished model comprises four basic steps:

 *  [Set up materials](..\materials\materials-tab.html) 
 *  [Set up lighting](../lighting/lighting-tab.html) 
 *  [Set up an environment](../environment/environment-tab.html) 
 *  [Set up rendering conditions](../render/render-tab.html) 

#### To start a rendering

 * On the **Render** or **Flamingo nXt** menu, click **Render**.
- Or -

 * On the **Standard** toolbar, click the **Render** button.

### Stop Rendering
 

By default, the rendering process will continue refining the image, pass by pass, until you click the **Stop Rendering** button. This allows you to manage the trade-off between time and quality. The longer you allow the rendering to continue, the more closely it will resemble its fully converged &quot;correct&quot; result. You can stop a rendering at any time.


###  <kbd>Resume Rendering</kbd> 
 

Clicking the **Stop Rendering** button suspends the rendering process after the current pass is completed.

The button then changes to **Resume Rendering**. If you have stopped the rendering before the number of passes or the time constraints have been reached, you can click the **Resume Rendering** button to continue.

Use the [Number of passes](..\render\render-window.html#number-of-passes) or [Time](..\render\render-window.html#time) settings on the [Render Window](..\render\render-window.html) or in [Document Properties &gt; Flamingo nXt](..\render\documentproperties-flamingo.html) to set an automatic stopping point.

&#160;

Revised: 22-Dec-2011 14:45

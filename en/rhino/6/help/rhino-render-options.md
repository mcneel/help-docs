---
---

{: #kanchor2771}{: #kanchor2772}
# Rhino Render
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/options.png](images/options.png) [Properties](properties-toolbar.html)  [Standard](standard-toolbar.html)  [Tools](tools-toolbar.html) 
Menus
Tools
Options
The Rhino Render options manage settings for the built-in rendering engine.
General
Two-stage render
 [Render](render.html) and [RenderPreview](render.html#renderpreview) commands render the scene in two stages. Render the most important detail first to make sure it looks right. If it does, wait for the image to finish. If not, cancel the render and continue editing.
Select a rectangular area to render first.Press [Enter](enter-key.html) to use previous rectangle.Press [Esc](esc-key.html) for no rectangle.The rest of the image is rendered automatically right after rendering and displaying the selected area.Multithreading
Number of render threads
Controls the number of threads used for rendering. If you have a dual core or dual or quad CPU computer, you can speed up rendering by using multiple simultaneous render threads. There is very little overhead in setting up the multiple threads.
Auto
The render automatically uses as many threads as there are cores in the CPU.
Thread priority
Controls the relative priority of the rendering compared to other processes. The lower the priority, the more responsive your computer will be while rendering, at the expense of rendering speed, and vice versa.
To save options for use on other computers
![images/optionsexport.png](images/optionsexport.png) [OptionsExport](optionsexport.html) 
Save [Options](options.html) settings to a file.
![images/optionsimport.png](images/optionsimport.png) [OptionsImport](optionsexport.html#optionsimport) 
Restore [Options](options.html) settings from a file.
See also
 [Render your model scene](sak-render.html) 
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](rhino-render-options.html) 


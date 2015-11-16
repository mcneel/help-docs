---
---

{: #kanchor2754}{: #kanchor2755}{: #kanchor2756}
# Rendering
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/options.png](images/options.png) [Properties](properties-toolbar.html)  [Standard](standard-toolbar.html)  [Tools](tools-toolbar.html) 
Menus
Tools
Options
Rendering options control settings that apply to all renderers and all documents.
Rendering
Renderer support options
Preview custom render meshes in viewport
Controls whether custom render meshes produced by certain plug-ins display in the viewport.
Copy similar settings when content type is changed
Determines whether, by default, settings from the previous material, environment, or texture are copied to the new material, environment, or texture when a content type is changed using the Change button in the Content Editor dialog box.
{: #check-for-missing-textures-when-rendering}Check for missing textures when rendering
If there are textures referred to in the model, that are not on your system, a dialog box with a list of the missing textures displays.
Auto-save renderings
The saved renderings are stored in a temp folder. They are accessible from the [Render window File &gt; Recent](render.html) list.
Renderings to keep ___
The number of auto-saved renderings that will be kept. When this number is reached, older files are deleted without warning.
 **Restore All "Do Not Show Me This" Dialog Boxes** 
Revives display of all warning dialog boxes used by rendering processes.
For example:
When saving a material to an RMTL file:Do you want to embed support files...?When changing a texture on a material or environment:Would you like to preserve &lt;material-x&gt; as a child of &lt;material-y&gt;?When copying/deleting multiply selected materials, textures, etc.:Are you sure you want to duplicate/delete these &lt;number&gt; items?When opening floating previews of multiply selected materials, textures, etc.:Are you sure you want to open &lt;value&gt; floating previews?When embedding a large number of support files into a .3dm file: You are attempting to embed &lt;number&gt; of support files.Are you sure you really want to do this?When stopping a rendering:Are you sure you want to stop rendering?Previews
Prefer native renderer
By default, material, texture and environment previews are rendered using the renderer they are designed for, even if that renderer is not current. Clear the check box to always render previews with the current renderer.
Use quick initial preview
Troubleshooting-only setting.
Use preview cache
Troubleshooting-only setting.
Show details panel (requires restart of Rhino)
Developers-only setting.
Texture size
When a procedural texture is displayed in the viewport, it is created as a bitmap on the disk. This setting determines the size of the image on the disk. Using larger textures can improve the viewport display, but may slow down certain operations.
128
256
512
1024
2048
To save options for use on other computers
![images/optionsexport.png](images/optionsexport.png) [OptionsExport](optionsexport.html) 
Save [Options](options.html) settings to a file.
![images/optionsimport.png](images/optionsimport.png) [OptionsImport](optionsexport.html#optionsimport) 
Restore [Options](options.html) settings from a file.
See also
![images/options.png](images/options.png) [Options](options.html) 
Manage global options: [3D mouse](3dconnexion.html), [alerter](alerter.html), [aliases](aliases.html), [appearance](appearance.html), [context menu](context-menu.html), [display modes](view-displaymode-options.html), [files](files.html), [general](general.html), [idle processor](idleprocessor.html), [keyboard](keyboard.html), [libraries](libraries.html), [licenses](licenses.html), [modeling aids](modeling-aids.html), [mouse](mouse.html), [plug-ins](plug-ins.html), [render](#), [RhinoScript](rhinoscript.html), [selection menu](selection-menu.html), [toolbars](toolbars.html), [updates and statistics](updates-and-statistics.html), [view](view.html).
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](rendering.html) 


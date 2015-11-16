---
---


# View
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/options.png](images/options.png) [Properties](properties-toolbar.html)  [Standard](standard-toolbar.html)  [Tools](tools-toolbar.html) 
Menus
Tools
Options
TheViewoptions manage view controls.
Pan
These options control keyboard pan behavior.
Screen fraction ___
When you pan with the keyboard, Rhino pans in steps. The pan step is defined as the screen fraction value multiplied by the smaller of the two viewport dimensions (height or width) in pixels.
Reverse keyboard action
By default, Rhino pans the camera in the direction of the arrow key you press. Select this check box to make Rhino pan the scene instead.
Always pan parallel views
If the view is not looking straight at the construction plane, sets parallel viewports so they will not rotate.
Note
The parallel views always pan with right-mouse button even if the view has been rotated. [Ctrl](ctrl-key.html) + [Shift](shift-key.html) &#160;+ [right-mouse button](mouse-buttons.html) does not rotate a plan parallel view.Auto adjust camera target after Pan and Zoom
Tries to keep the view rotation target where the objects are. If a pan or zoom operation moves the target point very close to the camera, or very far beyond the objects in the scene, the target point is automatically moved back into the scene.
Zoom
{: #zoom-scale-factor}Scale factor ___
Defines the step size for zooming with a wheeled mouse or the Page Up and Page Down keys.
To reverse the default zoom direction of the mouse scroll wheel and the Page Up and Page Down keys, set this number higher than 1.
Named views
Named views set CPlane
Restoring a named view causes the construction plane saved with that view to also restore.
Named views set projection
Restoring a named view causes the viewport projection saved with the view to also restore.
Named views set clipping planes
Restoring a named view causes the clipping planes saved with the view to also restore.
Rotate
These options control view rotation. Some options affect both keyboard and mouse rotation, some only the keyboard rotation.
Increment in divisions of a circle ___
When you [rotate a view with the keyboard](rotateview.html), Rhino rotates the view in steps. The default step is 1/60th of a circle, which equals six degrees.
Reverse keyboard action
Make Rhino rotate the scene instead of rotating the camera around the scene. Reversing the keyboard pan and keyboard rotation makes them in sync with the mouse controls.
Rotate around world axes
Makes the views rotate relative to the world axes. You can use the tilt keys to rotate the view around the view depth axis.
Rotate relative to view
Makes the views rotate relative to the view axes rather than the model x, y, and z axes.
Classic V2 style rotate relative to view
The view rotation is always relative to the previous dynamic view.
Dynamic redraw
Frames per second ___
The number of frames per second Rhino will attempt to redraw when zooming or rotating a view.
When you pan, zoom, or rotate a view, the scene is redrawn dynamically. With large models, the dynamic redraw can be very slow.
By default, to make sure the feedback is reasonably fast, Rhino cancels the redraw if necessary. Use these options to control the speed and responsiveness of the views.
Viewport properties
{: #linkedviewports}Linked viewport
Enables real-time view synchronization. When a standard view is manipulated, the camera lens length of all parallel projection viewports are set to match the current viewport. See: [SynchronizeViews](synchronizeviews.html).
Note
This setting does not affect layout viewports.Zooming in a [perspective](viewport.html#projection-parallel-perspective) viewport does not affect [parallel](viewport.html#projection-parallel-perspective) viewports.Zooming in a [parallel](viewport.html#projection-parallel-perspective) viewport does not affect [perspective](viewport.html#projection-parallel-perspective) viewports.Single-click maximize
Maximizes a viewport with a single click on the [viewport title](rhino-window.html#viewport-title-menu) rather than a double-click.
Wrap cursor at viewport borders
Causes the cursor to wrap at viewport borders during view manipulations (pan, rotate).
When unchecked, the cursor does not wrap. Use this option for absolute pointing devices like Wacom tablets.
Default 35mm camera lens length ___
Sets the viewport camera lens length when the viewport projection is changed from [parallel](viewport.html#projection-parallel-perspective) to [perspective](viewport.html#projection-parallel-perspective).
To save options for use on other computers
![images/optionsexport.png](images/optionsexport.png) [OptionsExport](optionsexport.html) 
Save [Options](options.html) settings to a file.
![images/optionsimport.png](images/optionsimport.png) [OptionsImport](optionsexport.html#optionsimport) 
Restore [Options](options.html) settings from a file.
See also
![images/options.png](images/options.png) [Options](options.html) 
Manage global options: [3D mouse](3dconnexion.html), [alerter](alerter.html), [aliases](aliases.html), [appearance](appearance.html), [context menu](context-menu.html), [display modes](view-displaymode-options.html), [files](files.html), [general](general.html), [idle processor](idleprocessor.html), [keyboard](keyboard.html), [libraries](libraries.html), [licenses](licenses.html), [modeling aids](modeling-aids.html), [mouse](mouse.html), [plug-ins](plug-ins.html), [render](rendering.html), [RhinoScript](rhinoscript.html), [selection menu](selection-menu.html), [toolbars](toolbars.html), [updates and statistics](updates-and-statistics.html), [view](#).
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](view.html) 


---
---

{: #kanchor2731}{: #kanchor2732}{: #kanchor2733}
# Idle Processor
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/options.png](images/options.png) [Properties](properties-toolbar.html)  [Standard](standard-toolbar.html)  [Tools](tools-toolbar.html) 
Menus
Tools
Options
TheIdle Processoroptions schedule commands to be run when Rhino has been inactive for a user-specified period.
For example, you could have Rhino automatically save your current document or start a time-consuming rendering.
General
Enable idle processing
Turns idle processing on.
Elapsed time in seconds
The amount of inactive time in seconds required to begin processing commands.
Commands to run
Specifies the commands to run.
Note
Idle processor only listens to command inactivity. That is, if you have not run a command for the specified period, it will run the idle process commands. Panning, zooming or rotating a view will not reset the idle timer.The idle process commands are only run once. If your elapsed time is set for 300 seconds (5 minutes) and you have been away from your system for 30 minutes, the idle process commands will be run one time (after the first 5 minutes), not six times. To reset the idle timer, run another command.To save options for use on other computers
![images/optionsexport.png](images/optionsexport.png) [OptionsExport](optionsexport.html) 
Save [Options](options.html) settings to a file.
![images/optionsimport.png](images/optionsimport.png) [OptionsImport](optionsexport.html#optionsimport) 
Restore [Options](options.html) settings from a file.
See also
![images/options.png](images/options.png) [Options](options.html) 
Manage global options: [3D mouse](3dconnexion.html), [alerter](alerter.html), [aliases](aliases.html), [appearance](appearance.html), [context menu](context-menu.html), [display modes](view-displaymode-options.html), [files](files.html), [general](general.html), [idle processor](#), [keyboard](keyboard.html), [libraries](libraries.html), [licenses](licenses.html), [modeling aids](modeling-aids.html), [mouse](mouse.html), [plug-ins](plug-ins.html), [render](rendering.html), [RhinoScript](rhinoscript.html), [selection menu](selection-menu.html), [toolbars](toolbars.html), [updates and statistics](updates-and-statistics.html), [view](view.html).
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](idleprocessor.html) 


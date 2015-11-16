---
---

{: #kanchor1147}{: #kanchor1148}{: #kanchor1149}{: #kanchor1150}{: #kanchor1151}{: #kanchor1152}{: #kanchor1153}{: #kanchor1154}{: #kanchor1155}{: #kanchor1156}
# History
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/history.png](images/history.png) [History](history-toolbar.html)  [Main2](main2-toolbar.html)  [Tools](tools-toolbar.html) 
Menus
![images/-no-menu-item.png](images/-no-menu-item.png) [Not on menus.](menuwhattodo.html) 
 [Status bar![images/menuarrow.gif](images/menuarrow.gif)](rhino-window.html#statusbarpanes) 
Record History
(Right&#8209;click Record History pane.)![images/menuarrow.gif](images/menuarrow.gif)
Always Record History
Update Children
Lock Children
History Break Warning
The History command stores the connection between a command's input geometry and the result so that when the input geometry changes, the result updates accordingly.
For example, with History recording and Update turned on, a lofted surface can be changed by editing the input curves.
Steps
In the [status bar](rhino-window.html#appwindow-statusbar), click the [Record History](rhino-window.html#recordhistory) pane.Use a history-enabled command such as the [Loft](loft.html) command to make a surface from input curves.Edit the input curves.The surface updates.Your browser does not support the video tag.Command-line options
{: #history-record}Record
Controls the defaultRecord Historysetting.
In general, it is best to leave theRecordoption set toNoand use theRecord Historystatus bar pane to selectively record history. Recording history uses computer resources and makes saved files larger.
{: #update}Update
Allows output to automatically update when input is edited. This may be slow or may interfere with your workflow.
If the option is set toNo, use the [HistoryUpdate](#historyupdate) command to manually update the objects.
{: #lock-yes}Lock
Locks child objects created with History to discourage direct geometry editing of the child object. Editing the child object directly will break the history link to the parent object.
History locked objects are selectable to use as input and edit properties, but not change geometry. If full locking is needed, children can be selected and locked with [Lock](lock.html) command.
BrokenHistoryWarning
Displays a warning dialog when an action is taken that breaks the link between the output and input objects. To get back, use theUndocommand.
Cautions
The connection between the input objects and the output object is easily broken. The basic rules for preserving history are:
Do not [purge](#historypurge) the history from the child (output) surfaces.Do not delete the parent geometry (input objects - curves, surfaces, etc.) that was used to create the child surface.Do not control-point edit or move the child surface.Do not move parents and children together. [Joining](join.html) objects breaks history on the objects.History stored in previous versions of Rhino will not carry over to a later version.Overriding History Options
The status bar [Record History](rhino-window.html#recordhistory) pane reflects the current state of history recording. Click the pane to toggle the global setting for the duration of one command. If the text in the pane is bold, then recording is active, if it is not bold, recording is not active.
Change the option using the History command. This command can be run inside another command. It can also be included in a macro. This setting does not quit after one command. It must be explicitly changed.
History can be recorded without the output geometry being updated when inputs are edited.
{: #commandprefixes}Command prefixes for turning history on and off
Type these shortcut symbols before a command name to enable/disable history recording
# (hash)
Enables history recording.
For example:#ArcBlend
% (percent)
Disables history recording.
For example: **%ArcBlend** 
Commands with history enabled
Commands with the following notation pay attention to history recording.
![images/history-tag.png](images/history-tag.png) [&#160;History enabled](historyenabled.html) 
These commands can make use of history recording.
 [ArcBlend](arcblend.html)  [Array](array.html)  [ArrayCrv](arraycrv.html)  [ArrayCrvOnSrf](arraycrvonsrf.html)  [ArrayPolar](arraypolar.html)  [ArraySrf](arraysrf.html)  [Bend](bend.html) (Copy only)Blend [BlendCrv](blendcrv.html)  [BlendSrf](blendsrf.html)  [ChamferSrf](chamfersrf.html)  [Copy](copy.html)  [Crv2View](crv2view.html)  [CSec](csec.html)  [CurveThroughPolyline](curvethroughpolyline.html)  [CurveThroughPt](curvethroughpt.html)  [Dim](dim.html)  [DimAligned](dimaligned.html)  [DimAngle](dimangle.html)  [DimArea](dimarea.html)  [DimCurveLength](dimcurvelength.html)  [DimDiameter](dimdiameter.html)  [DimOrdinate](dimordinate.html)  [DimRadius](dimradius.html)  [DimRotated](dimrotated.html)  [Divide](divide.html)  [EdgeSrf](edgesrf.html)  [ExtrudeCrv](extrudecrv.html)  [ExtrudeCrvAlongCrv](extrudecrvalongcrv.html)  [ExtrudeCrvTapered](extrudecrvtapered.html)  [ExtrudeCrvToPoint](extrudecrvtopoint.html)  [ExtrudeSrf](extrudesrf.html)  [ExtrudeSrfAlongCrv](extrudesrfalongcrv.html)  [ExtrudeSrfTapered](extrudesrftapered.html)  [ExtrudeSrfToPoint](extrudesrftopoint.html)  [FilletSrf](filletsrf.html)  [Flow](flow.html)  [Hatch](hatch.html)  [Helix](helix.html) (AroundCurve only) [Intersect](intersect.html)  [Loft](loft.html)  [MatchSrf](matchsrf.html)  [Mirror](mirror.html) (Copy only) [NetworkSrf](networksrf.html)  [Offset](offset.html)  [OffsetSrf](offsetsrf.html)  [Orient](orient.html) (Copy only) [OrientCrvToEdge](orientcrvtoedge.html) (Copy only) [OrientOnCrv](orientoncrv.html) (Copy only) [OrientOnSrf](orientonsrf.html) (Copy only) [Patch](patch.html)  [Pipe](pipe.html)  [PlanarSrf](planarsrf.html)  [Project](project.html)  [ProjectToCPlane](projecttocplane.html)  [Pull](pull.html)  [RailRevolve](railrevolve.html)  [RemapCPlane](remapcplane.html) (Copy only) [Revolve](revolve.html)  [Ribbon](ribbon.html)  [Rotate](rotate.html) (Copy only) [Rotate3D](rotate3d.html) (Copy only) [Scale](scale.html) (Copy only) [Scale1D](scale1d.html) (Copy only) [Scale2D](scale2d.html) (Copy only) [ScaleByPlane](scalebyplane.html) (Copy only) [ScaleNU](scalenu.html) (Copy only) [SetPt](setpt.html)  [Shear](shear.html) (Copy only) [Slab](slab.html)  [Spiral](spiral.html) (AroundCurve only) [Stretch](stretch.html)  [Sweep1](sweep1.html)  [Sweep2](sweep2.html)  [Symmetry](symmetry.html)  [Taper](taper.html) (Copy only) [TweenCurves](tweencurves.html)  [TweenSurfaces](tweensurfaces.html)  [Twist](twist.html) (Copy only) [VariableBlendSrf](variableblendsrf.html)  [VariableChamferSrf](variablechamfersrf.html)  [VariableFilletSrf](variablefilletsrf.html) 
# Related commands

## HistoryUpdate
{: #historyupdate}
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/historyupdate.png](images/historyupdate.png) [History](history-toolbar.html) 
Menus
![images/-no-menu-item.png](images/-no-menu-item.png) [Not on menus.](menuwhattodo.html) 
 [Status bar![images/menuarrow.gif](images/menuarrow.gif)](rhino-window.html#statusbarpanes) 
Record History
(Right-click Record History pane.)![images/menuarrow.gif](images/menuarrow.gif)
Update Children
The HistoryUpdate command redefines the object based on editing its parents.
Steps
 [Select](select-objects.html) the objects.Command-line options
{: #historyupdate-all}All
Updates all objects.

## HistoryPurge
{: #historypurge}
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/historypurge.png](images/historypurge.png) [History](history-toolbar.html) 
Menus
![images/-no-menu-item.png](images/-no-menu-item.png) [Not on menus.](menuwhattodo.html) 
The HistoryPurge command removes history from an object and its children.
History records can add to the file size so purging unneeded history may a good idea at times.
Warning: HistoryPurge cannot be undone.
Steps
 [Select](select-objects.html) the objects.See also
 [Edit objects using history](sak-history.html) 
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](history.html) 


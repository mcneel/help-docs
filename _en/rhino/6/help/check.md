---
---


# Check
{: #kanchor315}
{: #kanchor314}
{: #kanchor313}
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/check.png](images/check.png) [Analyze](analyze-toolbar.html)  [Diagnostics](diagnostics-toolbar.html)  [Main2](main2-toolbar.html)  [Mesh Tools](mesh-tools-toolbar.html) 
Menus
Analyze
Diagnostics![images/menuarrow.gif](images/menuarrow.gif)
Check
The Check command reports errors in the selected object's data structure.
Steps
 [Select](select-objects.html) objects.A report on the correctness of the object will display.This is primarily a tool for diagnosing potential geometry errors.Delete or remodel objects that have errors.
# CheckNewObjects
{: #kanchor317}
{: #kanchor316}
{: #checknewobjects}
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/checknewobjects.png](images/checknewobjects.png) [Analyze](analyze-toolbar.html)  [Diagnostics](diagnostics-toolbar.html)  [Diagnostics](diagnostics-toolbar.html)  [Main2](main2-toolbar.html)  [Mesh Tools](mesh-tools-toolbar.html) 
Menus
![images/-no-menu-item.png](images/-no-menu-item.png) [Not on menus.](menuwhattodo.html) 
The CheckNewObjects command reports errors in the data structure of objects as they are created or imported.
Details
Rhino reports the addition of bad objects to a model in three situations.
Reading .3dm files
If bad objects are added to the model while Rhino is reading a Rhino .3dm file, after the file is read a message is printed in the command history window," *N* bad objects were created while reading *model.3dm* ."
Reading other model files
If bad objects are added to the model while file import plug-in is reading a file, after the file is read a message is printed in the command history window, " *N* bad objects were created while reading *model.3dm* ." No dialogs are shown.
If Rhino creates a bad object while opening any file not 3DM:
If you are reading an IGES, STEP, or other file that is not a Rhino .3dm file, and Rhino creates a bad object, please email the file you are importing to [tech@mcneel.com](mailto:tech@mcneel.com) .Running Rhino commands
If bad objects are added to the model while a command is running, after the command finishes, a message is printed in the command window, "The *CommandName* command created N bad objects." and a modal dialog is shown.
If Rhino creates a bad object while modeling:
If you are working normally and theCheck New Objectsdialog box appears, then you have found a bug in Rhino.
Please report this bug as follows:
Make a note of the command that was running when the message box appeared. [Undo](undo.html) .Select all of the objects that were used in the command and [Export](export.html) these to a new file.Email the file to [tech@mcneel.com](mailto:tech@mcneel.com) .Tell us what command you were using and any options that were enabled at the time.
## NURBS Diagnostics
Sometimes a model can become damaged. These damaged areas can cause problems.
It is possible to build bad models using Rhino tools. For instance, Rhino will let you create a planar surface from a self-intersecting curve, but the result will be a poorly defined object that will cause problems later.
Another potential problem is a tiny trimming edge joining to a larger trim curve on an adjacent surface. If Rhino matches the large edges, sometimes the tiny trim curve edge compresses even further so that it is really just a point. That compressed edge no longer has meaningful orientation and causes problems.
There are modeling techniques you can use to increase the overall robustness of your models.
Drawing tiny little lines to connect pieces of a trim curve instead of moving the two endpoints of the curves together generally interferes with other objects joining together and tends to cause problems.
Sometimes the microscopic edges can be generated through other means, such as Boolean operations, where the objects are just off from each other by just a little bit.
Trimming edges that are very small or curved back on themselves are the biggest cause of problems in models.
There are Rhino tools you can use to examine your model for these defects.
The first one to try is theCheckcommand. If your model doesn't passCheck, then it will list some specific problems. You can just use the list to indicate that you might need to tune up the model. If a model passesCheck, it doesn't automatically mean that it is 100 percent properly structured, though. Some bad model parts, like having surfaces that fold back on themselves or self-intersect, are very time consuming and difficult to automatically detect, andCheckdoes not check for those things. But it can check the general overall structure of the object.
The work-around is to [Explode](explode.html), [Untrim](trim.html#untrim), [Trim](trim.html) again, and [Join](join.html). If there are lots of tiny edges, then you may have to use the [SplitEdge](splitedge.html) command to split all edges so they have a compatible structure, and then use [JoinEdge](joinedge.html) to manually mate the proper pairs.
When there are long things and tiny things adjacent to each other, the [Join](join.html) command can get confused - when that happens, the low level manual [JoinEdge](joinedge.html) can work as a replacement.
These tools are on theAnalyzemenu underEdge Tools. You may need to use several of these tools to fix difficult broken models as well.
Avoiding Modeling Errors
In general, avoid creating tiny edges in models.Do not use curves where there is a tiny line in the middle of the curve that joins two pieces together.Try to make sure that adjacent parts mate cleanly with a good, simple edge-to-edge matching.Tools for analysis include:
 [List data structure of an object](list.html)  [Check objects](#)  [Select all objects that do not pass Check](selection-commands.html#selbadobjects) Mesh Diagnostics
Note
Some STL/SLA printers have problems if meshes contain many long, thin facets. These can slow the printer's slicing process down, produce odd printed results, and run the printer out of memory.The [MeshRepair](meshrepair.html) command may be useful when tuning up meshes for STL/SLA printing.Degenerate faces
Fix with the [CullDegenerateMeshFaces](culldegeneratemeshfaces.html) command.
Zero length edges
Zero-length edges typically are the result of degenerate faces. Fix with the [CullDegenerateMeshFaces](culldegeneratemeshfaces.html) command.
Non manifold edges
Use the [CullDegenerateMeshFaces](culldegeneratemeshfaces.html) command and then fix with the [ExtractNonManifoldMeshEdges](extractmeshedges.html#extractnonmanifoldmeshedges) command.
Naked edges
Naked edges are allowed, but cause problems with rapid prototyping. Use the [ShowEdges](showedges.html) command to help find them. Try the [FillMeshHole](fillmeshhole.html), [FillMeshHoles](fillmeshholes.html), or [MatchMeshEdge](matchmeshedge.html) commands to remove naked edges.
Duplicate faces
Fix with the [ExtractDuplicateMeshFaces](extractmeshfaces-commands.html#extractduplicatemeshfaces) command.
Faces that could make it better if their directions were flipped
Fix with the [UnifyMeshNormals](unifymeshnormals.html) command.
Disjoint pieces
Fix with the [SplitDisjointMesh](splitdisjointmesh.html) command.
Unused vertices
Unused vertices do not usually cause a problem, and there are no commands to for removing them.

### Text window
Right-click for options.
Undo
Cut
Copy
Paste
Select All
 **Copy All** 
Copies all text in the window to the Clipboard.
 **Save As** 
Saves the contents of the window to a text file.
 **Close** 
Closes the window.
See also
 [Analyze objects](sak-analysis.html) 
 [Rhino Wiki: Bad objects](http://wiki.mcneel.com/rhino/badobjects) 
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](check.html) 


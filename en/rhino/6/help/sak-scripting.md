---
---


# Use scripting
Scripting extends Rhino functionality.
All Rhino commands can be used in command macros. Command macros can be run by typing the command at the command prompt, from toolbar buttons, [shortcut keys](keyboard.html), [command aliases](aliases.html), from the [ReadCommandFile](rhinoscripting.html#readcommandfile) command, or using the [Paste](paste.html) command into Rhino's command stream.
Some commands are provided to facilitate scripting actions usually performed through the Rhino interface.

# Specialized commands for scripting

## Action
![images/cancel.png](images/cancel.png) [Cancel](cancel.html) 
Cancel the current command and deselects objects.
![images/-no-toolbar-button.png](images/-no-toolbar-button.png) [Delete](delete.html) 
Erase objects.
![images/-no-toolbar-button.png](images/-no-toolbar-button.png) [Echo](rhinoscripting.html#echo) 
Turn on echoing of script commands to the command history window.
![images/-no-toolbar-button.png](images/-no-toolbar-button.png) [EditPythonScript](rhinoscripting.html#editpythonscript) 
Edit a Python script.
![images/-no-toolbar-button.png](images/-no-toolbar-button.png) [EditScript](rhinoscripting.html#editscript) 
Open a text editor utility for editing RhinoScript files.
![images/-no-toolbar-button.png](images/-no-toolbar-button.png) [Enter](rhinoscripting.html#enter) 
Simulate the Enter key in a script.
![images/-no-toolbar-button.png](images/-no-toolbar-button.png) [EnterEnd](rhinoscripting.html#enterend) 
Simulate the Enter key to complete a command string in a script.
![images/-no-toolbar-button.png](images/-no-toolbar-button.png) [GetDocumentUserText](rhinoscripting.html#getdocumentusertext) 
Retrieve text information attached to a file with the [SetDocumentUserText](rhinoscripting.html#setdocumentusertext) command.
![images/-no-toolbar-button.png](images/-no-toolbar-button.png) [GetUserText](rhinoscripting.html#getusertext) 
Retrieve text information attached to an object using the [SetUserText](rhinoscripting.html#setusertext) command.
![images/macroeditor.png](images/macroeditor.png) [MacroEditor](rhinoscripting.html#macroeditor) 
Open an edit window for script creation and testing.
![images/-no-toolbar-button.png](images/-no-toolbar-button.png) [NoEcho](rhinoscripting.html#noecho) 
Turn off echoing of script commands to the command history window.
![images/-no-toolbar-button.png](images/-no-toolbar-button.png) [Pause](rhinoscripting.html#pause) 
Stop a script for user input.
![images/readcommandfile.png](images/readcommandfile.png) [ReadCommandFile](rhinoscripting.html#readcommandfile) 
Read and execute a command script from a text file.
![images/-no-toolbar-button.png](images/-no-toolbar-button.png) [Run](rhinoscripting.html#run) 
Run another application from inside Rhino.
![images/-no-toolbar-button.png](images/-no-toolbar-button.png) [RunPythonScript](rhinoscripting.html#runpythonscript) 
Run a Python script.
![images/-no-toolbar-button.png](images/-no-toolbar-button.png) [RunScript](rhinoscripting.html#runscript) 
Run a RhinoScript.
![images/-no-toolbar-button.png](images/-no-toolbar-button.png) [SetCurrentRenderPlugIn](render.html#setcurrentrenderplugin) 
Specify a rendering plug-in.
![images/-no-toolbar-button.png](images/-no-toolbar-button.png) [SetDisplayMode](setdisplaymode.html) 
Specify a viewport display mode.
![images/-no-toolbar-button.png](images/-no-toolbar-button.png) [SetDocumentUserText](rhinoscripting.html#setdocumentusertext) 
Attach text information to the file.
![images/-no-toolbar-button.png](images/-no-toolbar-button.png) [SetObjectName](setobjectname.html) 
Assign a name to an object.
![images/setredrawoff.png](images/setredrawoff.png) [SetRedrawOff](rhinoscripting.html#setredrawoff) 
Disable screen redraw, construction plane, and view changes during scripts.
![images/setredrawon.png](images/setredrawon.png) [SetRedrawOn](rhinoscripting.html#setredrawon) 
Enable screen redraw, construction plane, and view changes during scripts.
![images/-no-toolbar-button.png](images/-no-toolbar-button.png) [SetUserText](rhinoscripting.html#setusertext) 
Attach text information to an object.
![images/setworkingfolder.png](images/setworkingfolder.png) [SetWorkingFolder](setworkingfolder.html) 
Specify the default folder for saving and opening files.

## Interface
![images/-no-toolbar-button.png](images/-no-toolbar-button.png) [BringViewportToTop](viewport-arrangement.html#bringviewporttotop) 
Bring a viewport to the front.
![images/clearundo.png](images/clearundo.png) [ClearUndo](clearundo.html) 
Clear the undo buffer to free memory.
![images/-no-toolbar-button.png](images/-no-toolbar-button.png) [CloseRenderWindow](render.html#closerenderwindow) 
Close the render display window.
![images/closeviewport-newviewport-rt.png](images/closeviewport-newviewport-rt.png) [CloseViewport](new-viewport-arrangements.html#closeviewport) 
Close the active viewport.
![images/-no-toolbar-button.png](images/-no-toolbar-button.png) [CommandPrompt](commandprompt.html) 
Manage the display of the command prompt window.
![images/-no-toolbar-button.png](images/-no-toolbar-button.png) [CopyRenderWindowToClipboard](render.html#copyrenderwindowtoclipboard) 
Copy the image in the render window to the Clipboard.
![images/-no-toolbar-button.png](images/-no-toolbar-button.png) [DocumentPropertiesPage](documentpropertiespage.html) 
Open the Document Properties dialog box at the specified page.
![images/-no-toolbar-button.png](images/-no-toolbar-button.png) [Exit](rhinoscripting.html#exit) 
Close Rhino.
![images/-no-toolbar-button.png](images/-no-toolbar-button.png) [Maximize](sizeapplicationwindow-commands.html#maximize) 
Maximize the Rhino application window.
![images/maxviewport.png](images/maxviewport.png) [MaxViewport](maxviewport.html) 
Maximize the active viewport.
![images/newfloatingviewport.png](images/newfloatingviewport.png) [NewFloatingViewport](new-viewport-arrangements.html#newfloatingviewport) 
Create a new free-floating viewport.
![images/newviewport.png](images/newviewport.png) [NewViewport](new-viewport-arrangements.html#newviewport) 
Create a new viewport.
![images/-no-toolbar-button.png](images/-no-toolbar-button.png) [NextOrthoViewport](nextviewport.html#nextorthoviewport) 
Activate the next viewport with an orthogonal projection.
![images/-no-toolbar-button.png](images/-no-toolbar-button.png) [NextPerspectiveViewport](nextviewport.html#nextperspectiveviewport) 
Activate the next viewport with a perspective projection.
![images/-no-toolbar-button.png](images/-no-toolbar-button.png) [NextViewport](nextviewport.html) 
Activate the next viewport.
![images/-no-toolbar-button.png](images/-no-toolbar-button.png) [NextViewportToTop](viewport-arrangement.html#nextviewporttotop) 
Display the next viewport in front of all other viewports.
![images/ortho.png](images/ortho.png) [Ortho](ortho.html) 
Restrict cursor movement to an angle.
![images/orthoangle.png](images/orthoangle.png) [OrthoAngle](ortho.html#orthoangle) 
Set the angle for cursor ortho movement.
![images/-no-toolbar-button.png](images/-no-toolbar-button.png) [OptionsPage](optionspage.html) 
Open the Options dialog box at a specified page.
![images/-no-toolbar-button.png](images/-no-toolbar-button.png) [PrevViewport](nextviewport.html#prevviewport) 
Activate the previous viewport.
![images/-no-toolbar-button.png](images/-no-toolbar-button.png) [PushViewportToBack](viewport-arrangement.html#pushviewporttoback) 
Send a named viewport behind all viewports.
![images/-no-toolbar-button.png](images/-no-toolbar-button.png) [PropertiesPage](propertiespage.html) 
Open the Properties dialog box at a specified page.
![images/-no-toolbar-button.png](images/-no-toolbar-button.png) [SetActiveViewport](setactiveviewport.html) 
Activate a named viewport.
![images/-no-toolbar-button.png](images/-no-toolbar-button.png) [SetMaximizedViewport](setmaximizedviewport.html) 
Maximize a named viewport inside the application window.
![images/-no-toolbar-button.png](images/-no-toolbar-button.png) [SetOrtho](ortho.html#setortho) 
Turn ortho mode on, off, or toggle the current state.
![images/-no-toolbar-button.png](images/-no-toolbar-button.png) [SetPlanar](planar.html#setplanar) 
Turn Planar mode on, off, or toggle the current state.
![images/-no-toolbar-button.png](images/-no-toolbar-button.png) [SetSnap](snap.html#setsnap) 
Turn grid snap on, off, or toggle the current state.
![images/showosnap.png](images/showosnap.png) [ShowOsnap](object-snaps.html#showosnap) 
Turn the Osnap control on.
![images/-no-toolbar-button.png](images/-no-toolbar-button.png) [Snap](snap.html) 
Toggle the current snap mode state.
![images/snapsize.png](images/snapsize.png) [SnapSize](snap.html#snapsize) 
Specify the grid snap spacing.

## Import/Export
![images/-no-toolbar-button.png](images/-no-toolbar-button.png) [AssignBlankTexture](assignblanktexture.html) 
Assign texture names to objects.
![images/-no-toolbar-button.png](images/-no-toolbar-button.png) [ComputeVertexColors](computevertexcolors.html) 
Evaluate texture coordinates and set [vertex](meshvertex.html) colors.
See also
 [Command Macros and Scripting](rhinoscripting.html) 
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](sak-scripting.html) 


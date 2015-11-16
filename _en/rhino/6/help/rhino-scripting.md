---
---


# Command macros and scripting
All Rhino commands can be used in command macros. Command macros can be run by typing the command at the command prompt, from toolbar buttons, [shortcut keys](keyboard.html), [command aliases](aliases.html), from the [ReadCommandFile](#readcommandfile) command, or using the [Paste](paste.html) command into Rhino's command stream.

### Writing Command Macros
Write command macros just as you would type the command sequence at the command line. A space between characters or a new line act like pressing [Enter](enter-key.html) at the command line.
Special characters{: #kanchor3105}
Character
Meaning in macro
*(asterisk){: #kanchor3106}{: #kanchor3107}
Causes the command to repeat automatically without pressing [Enter](enter-key.html) to restart.
!(exclamation point){: #kanchor3108}{: #kanchor3109}
Cancels the previous command.
An exclamation point (!) and a space in the beginning of a macro cancels any previous command. At other locations, it cancels the macro. If necessary, the exclamation point can be used at the end of the macro.
_(underscore){: #kanchor3110}
Runs command as English command name.
Rhino can be localized in many languages. The non-English versions will have commands, prompts, command options, dialog boxes, menus, etc., translated into their respective languages. English commands will not work in these versions.
For scripts written in English to work on all computers (regardless of the language of Rhino), the scripts need to force Rhino to interpret all commands as English command names.
For example: In the English version of Rhino, the following macro works:
Circle 3Point 0,0,0 1,1,0 0,3,0
But in the French version of Rhino, this won't work. Instead you need one of these macros:
Cercle 3Point 0,0,0 1,1,0 0,3,0_Circle _3Point 0,0,0 1,1,0 0,3,0
To make sure macros work worldwide, write them in English and put _ in front of all command names and options.
-(hyphen){: #kanchor3111}{: #kanchor3112}
Suppress dialog box.
All commands can be made into macros at the command line (even commands that have dialog boxes by default). To suppress the dialog box and use command-line options, prefix the command name with a hyphen (-).
'(apostrophe){: #kanchor3113}{: #kanchor3114}
The next command is a nestable command.
View and construction plane manipulation and object snaps are nestable. Geometry creation commands are not nestable.
 [One-shot object snaps](object-snaps.html) and sub-object picking filters are automatically nestable and do not require an apostrophe.
/(backslash){: #kanchor3115}{: #kanchor3116}
If the first character in a toolbar macro is not "!" and the last character is" /", the script runs on the command line without [Enter](enter-key.html), so more information can be added.
This feature is useful for building a command string out of parts like digits, decimal points, angles (such as "&lt;45") that are on buttons, making a "numeric keypad" on the screen.
~(tilde){: #kanchor3117}
Suppresses command options for clutter free command feedback. The options still work as usual.
;
(semicolon){: #kanchor3118}{: #kanchor3119}
Comment.
Lines beginning with a semicolon (;) are not part of the macro, but let you document the macro or try alternative input.
For example:
; This is a test macro_Circle 0,0,0 15_Line 0,0,0 pause ;15,0,0; Line 0,0,0 0,15,0_Line 0,0,0 -15,0,0
Examples
Draw a circle
This macro creates a circle centered at 5,5 with a radius of 10:
! _-Circle 5,5 10
The spaces between the entries are the same places you would press [Enter](enter-key.html) when typing the command by hand.
Deselect objects and start the Move command
This macro starts the [Move](move.html) command, but makes sure no objects are selected before asking you to select objects to move:
! _SelNone _Move
Create a curve through points
This macro creates a set of three points, selects them all, and fits a polyline through the points:
! _SelAll _Points _Pause _Pause _Pause _Enter _Invert _CurveThroughPt _EnterEnd
How this script works:
! _SelAll
Cancels all previous commands and selects all the objects currently in the model.
_Points
Runs the [Points](points.html) command.
_Pause
_Pause
_Pause
Allows picking three point locations.
_Enter
Simulates pressing [Enter](enter-key.html), which stops the creation of point objects.
_Invert
 [Inverts](selection-commands.html#invert) the selection. All visible objects in the scene were selected at the beginning of the script, so after Invert only the newly created point objects are selected.
_CurveThroughPt
Creates a polyline through the point objects.
_EnterEnd
Completes the command.
Bypass a dialog box
! -_Rebuild _Pause _Points=10 _Degree=3 _Enter
Select a curve, then run this macro. All options will be set by the macro.
To try these scripts
Select the macro right from this Help topic.Press [Ctrl](ctrl-key.html) +Cto copy it to the Clipboard.Click in the Rhino command prompt, and press [Ctrl](ctrl-key.html) +Vto paste the macro.Special scripting commands
Pause
Stops for user input in a macro.
Example
! _Circle _Pause 50
This macro asks for a point and then draws a circle with a 50 unit radius centered there.
Enter
Simulates pressing [Enter](enter-key.html) inside a macro.
This command does not repeat the previous command like pressing [Enter](enter-key.html) does.
EnterEnd
Completes the command.
SetRedrawOff
Prevents screen redraw, construction plane or camera changes during macros.
SetRedrawOn
Turns screen redraw back on afterSetRedrawOff.
NoEcho
Turns off echoing of macro commands to the command history window.
Echo
Turns on echoing of macro commands to the command history window.
If you do not know what to type in a macro, run the hyphenated version of the command. Highlight and copy the command sequence and paste it into your macro text as a starting point.

# MacroEditor
{: #kanchor3120}
{: #macroeditor-command}
{: #macroeditor}
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/macroeditor.png](images/macroeditor.png) [Utilities](utilities-toolbar.html) 
Menus
Tools
Commands![images/menuarrow.gif](images/menuarrow.gif)
Macro Editor
The MacroEditor command opens an edit window for macro creation and testing.
Macro Editor Panel
![images/paneloptions.png](images/paneloptions.png) [Panel options](panel-options.html) 
Steps
Type commands in theMacro Editorwindow.To test, clickRun.To delete the macro, clickDelete.Notes
Selecting some text and clickingRunwill run only that selected part of the macro.There is a right click context menu for selecting all, copy, paste, delete, run, etc.
# ReadCommandFile
{: #kanchor3124}
{: #kanchor3123}
{: #kanchor3122}
{: #kanchor3121}
{: #readcommandfile-command}
{: #readcommandfile}
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/readcommandfile.png](images/readcommandfile.png) [Tools](tools-toolbar.html) 
Menus
Tools
Commands![images/menuarrow.gif](images/menuarrow.gif)
Read from File
The ReadCommandFile command reads and executes a command macro from a text file.
Steps
In theOpen Text Filedialog box, select the file to read.The file contents are copied into the command line, and the lines of the command file are interpreted as if they were typed into the command line.Notes
When building command files, use the [Enter](#enter) command, which is equivalent to pressing [Enter](enter-key.html) to execute commands.If you read in a particular file often, assignReadCommandFileto a toolbar button along with a filename. For example:-ReadCommandFile myfile.txtIf the file name has spaces, surround the text with quote marks. For example: -ReadCommandFile "my file.txt".Example
Make a text file like the following example that has commands for creating all your curves in it, and then create the curves all at once withReadCommandFile.
! _interpcrv23,5,023.2,5,023.7,5.2,1_Enter_interpcrv26.1,4.9,1.126.8,4.9,1.027.1,4.8,0.9_Enter
etc&amp;.

# Echo
{: #kanchor3127}
{: #kanchor3126}
{: #kanchor3125}
{: #echo-command}
{: #echo}
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/-no-toolbar-button.png](images/-no-toolbar-button.png) [Not on toolbars.](toolbarwhattodo.html) 
Menus
![images/-no-menu-item.png](images/-no-menu-item.png) [Not on menus.](menuwhattodo.html) 
The Echo command turns on echoing of macro commands to the command history window.
To turn echoing off, use the [NoEcho](#noecho) command.

# NoEcho
{: #kanchor3128}
{: #noecho-command}
{: #noecho}
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/-no-toolbar-button.png](images/-no-toolbar-button.png) [Not on toolbars.](toolbarwhattodo.html) 
Menus
![images/-no-menu-item.png](images/-no-menu-item.png) [Not on menus.](menuwhattodo.html) 
The NoEcho command turns off display of macro commands in the command history window.
To turn echoing on use the [Echo](#echo) command.NoEcho or _NoEcho needs to be the very first word in the macro for it to work properly. Everything, including the exclamation point should follow, separated by a single space.

# Enter
{: #kanchor3130}
{: #kanchor3129}
{: #enter-command}
{: #enter}
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/-no-toolbar-button.png](images/-no-toolbar-button.png) [Not on toolbars.](toolbarwhattodo.html) 
Menus
![images/-no-menu-item.png](images/-no-menu-item.png) [Not on menus.](menuwhattodo.html) 
The Enter command functions as pressing [Enter](enter-key.html) for use in scripts or toolbar button programming.
Example
This script sets a construction plane by three picked points:
'_CPlane _3Point
_Pause _Pause _Pause _Enter
The Enter command does not repeat the previous command like pressing the [Enter](enter-key.html) key does.

# EnterEnd
{: #kanchor3131}
{: #enterend-command}
{: #enterend}
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/-no-toolbar-button.png](images/-no-toolbar-button.png) [Not on toolbars.](toolbarwhattodo.html) 
Menus
![images/-no-menu-item.png](images/-no-menu-item.png) [Not on menus.](menuwhattodo.html) 
The EnterEnd command functions as pressing the Enter key to complete a command string for use in macros or toolbar button programming.
EnterEnd is handy when a command is deep, in terms of command options such as Options or DocumentProperties, and you want to exit after one of these without counting how many Enters you need to get back to a blank command prompt. For example:
! _-DocumentProperties _Mesh _Custom _MaxEdgeSrf .01
would require at least two or three enters to exit the command. With EnterEnd, the command exits as soon as you want it to.
Example
! _-DocumentProperties _Mesh _Custom _MaxEdgeSrf .01 _EnterEnd

# Exit
{: #kanchor3133}
{: #kanchor3132}
{: #exit-command}
{: #exit}
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/-no-toolbar-button.png](images/-no-toolbar-button.png) [Not on toolbars.](toolbarwhattodo.html) 
Menus
File
Exit
The Exit command closes the current Rhino session.
To access command-line options
Type a hyphen in front of the command name-Exit.Command-line options
Yes
No
Cancel

# Pause
{: #kanchor3135}
{: #kanchor3134}
{: #pause-command}
{: #pause}
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/-no-toolbar-button.png](images/-no-toolbar-button.png) [Not on toolbars.](toolbarwhattodo.html) 
Menus
![images/-no-menu-item.png](images/-no-menu-item.png) [Not on menus.](menuwhattodo.html) 
Example
This macro asks for a point and then draws a circle with a 50 unit radius centered there.
! _Circle _Pause 50
The Pause command stops a macro for user input.

# Run
{: #kanchor3138}
{: #kanchor3137}
{: #kanchor3136}
{: #run-command}
{: #run}
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/-no-toolbar-button.png](images/-no-toolbar-button.png) [Not on toolbars.](toolbarwhattodo.html) 
Menus
![images/-no-menu-item.png](images/-no-menu-item.png) [Not on menus.](menuwhattodo.html) 
The Run command runs another application from inside Rhino.
Steps
Type the name and path of the file to run.
# SetRedrawOff
{: #kanchor3140}
{: #kanchor3139}
{: #setredrawoff-command}
{: #setredrawoff}
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/setredrawoff.png](images/setredrawoff.png) [View](view-toolbar.html) 
Menus
![images/-no-menu-item.png](images/-no-menu-item.png) [Not on menus.](menuwhattodo.html) 
The SetRedrawOff command disables screen redraw, construction plane, or camera changes during scripts.
To turn screen redraw back on
Use the [SetRedrawOn](#setredrawon) command.
# SetRedrawOn
{: #kanchor3141}
{: #setredrawon-command}
{: #setredrawon}
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/setredrawon.png](images/setredrawon.png) [View](view-toolbar.html) 
Menus
![images/-no-menu-item.png](images/-no-menu-item.png) [Not on menus.](menuwhattodo.html) 
The SetRedrawOn command enables screen redraw, construction plane, or camera changes during scripts.
To turn screen redraw off
Use the [SetRedrawOff](#setredrawoff) command.
# Scripting
{: #kanchor3143}
{: #kanchor3142}
RhinoScriptis a plug-in for running scripts. Scripting languages allow loops, variable names, browsing for files, queries, and other
The commands to use:
 [LoadScript](#loadscript) 
 [RunScript](#runscript) 
 [EditScript](#editscript) 
The basic steps are
Write a script function.RhinoScripts use the file extension .rvb.Run the [LoadScript](#loadscript) command to load a script into memory.Use the [RunScript](#runscript) command to run the function name.Dragging a .rvb file onto the Rhino window will load and run the script.
For more help on scripts
From the RhinoHelpmenu, clickPlug-insand then clickRhinoScript.For more information on Rhino-specific scripting, see: [http://wiki.mcneel.com/rhino/basicmacros](http://wiki.mcneel.com/rhino/basicmacros).

# LoadScript
{: #kanchor3145}
{: #kanchor3144}
{: #loadscript-command}
{: #loadscript}
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/-no-toolbar-button.png](images/-no-toolbar-button.png) [Not on toolbars.](toolbarwhattodo.html) 
Menus
Tools menu
Rhino Script![images/menuarrow.gif](images/menuarrow.gif)
Load
The LoadScript command reads a script file from disk, loads it into the script interpreter, and runs it.
Dragging a .rvb file onto the Rhino window will load and run the script.
Steps
In theLoad Script Filedialog box, click theHelpmenu.For the on-line RhinoScript programmers reference, see: [http://www.rhino3d.com/5/rhinoscript/index.html](http://www.rhino3d.com/5/rhinoscript/index.html).

# RunScript
{: #kanchor3147}
{: #kanchor3146}
{: #runscript-command}
{: #runscript}
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/-no-toolbar-button.png](images/-no-toolbar-button.png) [Not on toolbars.](toolbarwhattodo.html) 
Menus
Tools menu
Rhino Script![images/menuarrow.gif](images/menuarrow.gif)
Run
The RunScript command runs a previously loaded script.
Dragging a .rvb file onto the Rhino window will load and run the script.
Steps
In theRun Script Subroutinedialog box, click theHelpmenu.
# EditScript
{: #kanchor3149}
{: #kanchor3148}
{: #editscript-command}
{: #editscript}
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/-no-toolbar-button.png](images/-no-toolbar-button.png) [Not on toolbars.](toolbarwhattodo.html) 
Menus
Tools
Rhino Script![images/menuarrow.gif](images/menuarrow.gif)
Edit
TheEditScriptcommand opens a text editor utility for editing RhinoScript files.
Steps
In theEdit Scriptdialog box, click theHelpmenu.
# RunPythonScript
{: #kanchor3150}
{: #runpythonscript-command}
{: #runpythonscript}
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/-no-toolbar-button.png](images/-no-toolbar-button.png) [Not on toolbars.](toolbarwhattodo.html) 
Menus
Tools
Python Script![images/menuarrow.gif](images/menuarrow.gif)
Run
The RunPythonScript command runs a Python script.
For the on-line Rhino.Python programmers reference, see: [http://www.rhino3d.com/5/ironpython/index.html](http://www.rhino3d.com/5/ironpython/index.html).
-RunPythonScript
Options
ResetEngine
Forces the python engine to re-initialize. This is only useful while python scripts that span multiple files are being written and tested.

# EditPythonScript
{: #kanchor3151}
{: #editpythonscript-command}
{: #editpythonscript}
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/-no-toolbar-button.png](images/-no-toolbar-button.png) [Not on toolbars.](toolbarwhattodo.html) 
Menus
Tools
Python Script![images/menuarrow.gif](images/menuarrow.gif)
Edit
The EditPythonScript command edits a Python script.
For more information on Rhino-specific scripting, see: [http://wiki.mcneel.com/developer/python](http://wiki.mcneel.com/developer/python).

# SetUserText
{: #kanchor3152}
{: #setusertext-command}
{: #setusertext}
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/-no-toolbar-button.png](images/-no-toolbar-button.png) [Not on toolbars.](toolbarwhattodo.html) 
Menus
![images/-no-menu-item.png](images/-no-menu-item.png) [Not on menus.](menuwhattodo.html) 
The SetUserText command attaches text information to an object.
The information is stored in a key/value format.
Retrieve the information with the [GetUserText](#getusertext) command. This information can also be attached by .NET plug-ins and VisualBasic scripts.
This information is easily accessed in .NET and Visual Basic scripts.
Example
Text key = Weight
Text = Kilograms
Steps
 [Select](select-objects.html) objects.Type a text key.Type the text.To remove a key
 [Select](select-objects.html) objects.Type a text key.Type "" (double quotes).Options
AttachTo
{: #setusertext-toobject}Object
Attaches text information to the object geometry.
If the information is closely associated with the geometry, attach it to the geometry. For example, a circle's radius should be attached to the geometry because the information will be invalid if the circle is control-point edited and changed into a [NURBS](http://www.rhino3d.com/nurbs) curve.
{: #setusertext-toattributes}Attributes
Attaches text information to the attributes of an object.
If the information is higher-level attribute information, like color, then it should be attached to the object's attributes. Attribute information will persist when an object is control-point edited, trimmed, copied, and so on.

# GetUserText
{: #kanchor3153}
{: #getusertext-command}
{: #getusertext}
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/-no-toolbar-button.png](images/-no-toolbar-button.png) [Not on toolbars.](toolbarwhattodo.html) 
Menus
![images/-no-menu-item.png](images/-no-menu-item.png) [Not on menus.](menuwhattodo.html) 
The GetUserText command retrieves text information attached to an object using the [SetUserText](#setusertext) command. This information can also be retrieved by .NET plug-ins and VisualBasic scripts.
Steps
 [Select](select-objects.html) an object.Type a text key or press [Enter](enter-key.html) for all keys.
# SetDocumentUserText
{: #kanchor3154}
{: #setdocumentusertext-command}
{: #setdocumentusertext}
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/-no-toolbar-button.png](images/-no-toolbar-button.png) [Not on toolbars.](toolbarwhattodo.html) 
Menus
![images/-no-menu-item.png](images/-no-menu-item.png) [Not on menus.](menuwhattodo.html) 
The SetDocumentUserText command attaches text information to a Rhino .3dm file.
The information is stored in a key/value format.
Retrieve the information with the [GetDocumentUserText](#getdocumentusertext) command. This information can also be attached by .NET plug-ins and VisualBasic scripts.
This information is easily accessed in .NET and Visual Basic scripts.
Steps
Type a text key.Type the text.
# GetDocumentUserText
{: #kanchor3155}
{: #getdocumentusertext-command}
{: #getdocumentusertext}
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/-no-toolbar-button.png](images/-no-toolbar-button.png) [Not on toolbars.](toolbarwhattodo.html) 
Menus
![images/-no-menu-item.png](images/-no-menu-item.png) [Not on menus.](menuwhattodo.html) 
The GetDocumentUserText command retrieves text information attached using the [SetDocumentUserText](#setdocumentusertext) command. This information can also be retrieved by .NET plug-ins and VisualBasic scripts.
Steps
Type a text key or press [Enter](enter-key.html) for all keys.&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](rhino-scripting.html) 


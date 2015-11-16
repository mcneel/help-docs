---
---


# Autosave
{: #kanchor142}
{: #kanchor141}
{: #kanchor140}
{: #kanchor139}
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/autosave.png](images/autosave.png) [File](file-toolbar.html) 
Menus
 [![images/-no-menu-item.png](images/-no-menu-item.png) [Not on menus.](menuwhattodo.html) ](workspace-editor.html) 
The Autosave command saves the current file to the designated AutoSave(Number) file.
The automatic autosave mechanism periodically saves a copy of your current model. This saved file is removed when you successfully close your model. If Rhino is not successfully closed, either because it crashed or because you turned off your computer while your file was open, the autosave file remains on your hard drive.
When you run Rhino and Rhino detected an autosaved file, Rhino prompts to save the recovered model.
Warning
This is the only opportunity to recover the model. If you choose not to save, the autosaved file will be removed.
To turn automatic Autosave on
In [Files Options](files.html), underAutosave, check theSave everybox and type a number of minutes.To set the name and folder of the Autosave file
In [Files Options](files.html), underAutosave, set the folder and file name.To set a list of commands that trigger Autosave automatically
In [Files Options](files.html), underAutosave, in theAlways save beforebox, type the command names.Running commands in this list will trigger an autosave even if Autosave is not turned on.Note
A timer is used to fire an autosave event. If no command is running, Rhino saves immediately. If a command is running, Rhino autosaves at the end of the command/script that is running.Rhino starts the timer only when the document is modified. [Save](save.html) (but not [Export](export.html), nor [SaveAs](save.html#saveas) ) resets the autosave timer. [Save](save.html) also deletes the existing Autosave file and clears the registry flag indicating the last autosaved file because the real file is more current than the Autosave file.If the active model is named, the Autosave file will be placed in the default Autosave folder and be named as follows:&lt;auto save folder&gt;//&lt;file name&gt;_RhinoAutoSave(&lt;thread_id&gt;).3dmIf the active model is not named, autosave file is written to the default Autosave file.See also
 [Work with files](sak-file.html) 
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](autosave.html) 


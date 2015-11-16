---
---

{: #kanchor1566}{: #kanchor1567}{: #kanchor1568}{: #kanchor1569}{: #kanchor1570}{: #kanchor1571}{: #kanchor1572}{: #kanchor1573}{: #kanchor1574}{: #kanchor1575}{: #kanchor1576}{: #kanchor1577}{: #kanchor1578}{: #kanchor1579}{: #kanchor1580}{: #kanchor1581}{: #kanchor1582}{: #kanchor1583}{: #kanchor1584}{: #kanchor1585}{: #kanchor1586}{: #kanchor1587}{: #kanchor1588}{: #kanchor1589}{: #kanchor1590}{: #kanchor1591}{: #kanchor1592}{: #kanchor1593}{: #kanchor1594}{: #kanchor1595}{: #kanchor1596}{: #kanchor1597}{: #kanchor1598}{: #kanchor1599}{: #kanchor1600}{: #kanchor1601}{: #kanchor1602}{: #kanchor1603}{: #kanchor1604}{: #kanchor1605}{: #kanchor1606}{: #kanchor1607}{: #kanchor1608}{: #kanchor1609}
# Open
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/open.png](images/open.png) [File](file-toolbar.html)  [Standard](standard-toolbar.html)  [STL Tools](stl-tools-toolbar.html) 
Menus
File
Open
Shortcut
 [Ctrl](ctrl-key.html) +O
The Open command opens an existing Rhino or other supported format file.
Steps
Specify a file type.Select or type a file name.Click **Open** .Note
When Rhino opens a non-3dm model, the title bar reflects the name of the model that was opened. When the model is saved for the first time, this model name is entered as the file name.When Rhino reads polygon mesh formats, the polygon mesh objects in the original file are not converted to [NURBS](http://www.rhino3d.com/nurbs) objects; they remain polygon meshes in Rhino; they are not converted to [NURBS](http://www.rhino3d.com/nurbs) objects.{: #openrhinowithshortcut}Open Rhino With Shortcut
Using shortcuts, you can open Rhino using a number of options.
Options
/&lt;schemename&gt;
Opens with the saved scheme.
/nosplash
Suppress splash screen. View the splash screen with theAboutcommand.
/safemode
Starts Rhino in [safe mode](startingrhino.html#start-rhino-in-safe-mode) without OpenGL or third-party plug-ins.
/notemplate
Start Rhino with a default model based on hard-coded defaults.
/language=&lt;langid&gt;
Set the language. For example, /language=1041 starts in Japanese, /language=1033 starts in English, etc.
LCID
NAME
ABBR
CODEPAGE
1028
Chinese - Taiwan
zh-tw
950
2052
Chinese - China
zh-cn
936
1029
Czech
cs-cz
1250
1033
English - United States
en-us
1252
1036
French - France
fr-fr
1252
1031
German - Germany
de-de
1252
1040
Italian - Italy
it-it
1252
1041
Japanese
ja-jp
932
1042
Korean
ko-kr
949
1045
Polish
pl-pl
1250
1034
Spanish - Spain
es-es
1252
/runscript="&lt;script&gt;"
Run a script at startup.
modelname.3dm
The path and name of a model to open.
{: #schemes}Schemes
Save and restore Rhino workspace settings. The scheme saves the following settings:
Command defaultsDialog box positionsAll settings in the Rhino Options pages such as aliases, appearance and colors settings, mouse settings, render settings, shortcut keysRecently-used file listToolbar layoutTo save schemes
Make a Windows desktop shortcut to Rhino like this:"C:/Program Files/Rhino.exe" /scheme="WhiteBackground"
Set up Rhino with your white background colors and exit.Start Rhino from this shortcut.Rhino will find and store all it's settings in:HKEY_CURRENT_USER/Software/McNeel/Rhinoceros/5.0/Scheme:WhiteBackground/...Make another shortcut:"C:/Program Files/Rhino.exe" /scheme="BlackBackground"Set up Rhino with your black background colors and exit.Start Rhino from this shortcut.Rhino will find and store all it's settings in:HKEY_CURRENT_USER/Software/McNeel/Rhinoceros/5.0/Scheme:BlackBackground/...See also
 [Work with files](sak-file.html) 
 [Index of import/export file types](-index-of-import-export-file-types.html) 
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](open.html) 


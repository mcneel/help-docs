---
---

{: #kanchor2407}{: #kanchor2408}{: #kanchor2409}{: #kanchor2410}{: #kanchor2411}{: #kanchor2412}{: #kanchor2413}{: #kanchor2414}{: #kanchor2415}{: #kanchor2416}{: #kanchor2417}{: #kanchor2418}{: #kanchor2419}{: #kanchor2420}{: #kanchor2421}{: #kanchor2422}{: #kanchor2423}{: #kanchor2424}{: #kanchor2425}{: #kanchor2426}{: #kanchor2427}{: #kanchor2428}{: #kanchor2429}{: #kanchor2430}{: #kanchor2431}{: #kanchor2432}{: #kanchor2433}{: #kanchor2434}{: #kanchor2435}{: #kanchor2436}{: #kanchor2437}{: #kanchor2438}{: #kanchor2439}{: #kanchor2440}{: #kanchor2441}{: #kanchor2442}{: #kanchor2443}{: #kanchor2444}{: #kanchor2445}{: #kanchor2446}{: #kanchor2447}{: #kanchor2448}{: #kanchor2449}{: #kanchor2450}
# Starting Rhino
When Rhino installs, a shortcut icon is saved to your desktop. Other options for opening Rhino involve customizing or creating new shortcuts, using schemes, and starting Rhino in safe mode.

## Start Rhino with a Windows shortcut
{: #openrhinowithshortcut}
Using Windows shortcuts, you can open Rhino using a number of options.
Options
 */scheme="Scheme Name"* 
Opens with the saved scheme.
/nosplash
Suppress splash screen. View the splash screen with theAboutcommand.
/safemode
Starts Rhino in [safe mode](#start-rhino-in-safe-mode) without OpenGL or third-party plug-ins.
/notemplate
Start Rhino with a default model based on hard-coded defaults.
/language=&lt; *langid* &gt;
Set the language. For example, /language=1041 starts in Japanese, /language=1033 starts in English, etc.
NAME
ABBR
LCID
CODEPAGE
Chinese - Taiwan
zh-tw
1028
950
Chinese - China
zh-cn
2052
936
Czech
cs-cz
1029
1250
English - United States
en-us
1033
1252
French - France
fr-fr
1036
1252
German - Germany
de-de
1031
1252
Italian - Italy
it-it
1040
1252
Japanese
ja-jp
1041
932
Korean
ko-kr
1042
949
Polish
pl-pl
1045
1250
Spanish - Spain
es-es
1034
1252
/runscript=" *&lt;script&gt;* "
Run a script at startup.
modelname.3dm
The path and name of a model to open.

## Schemes
{: #schemes}
Save and restore Rhino workspace settings. The scheme saves the following settings:
Command defaultsDialog box positionsAll settings in the Rhino Options pages such as aliases, appearance and colors settings, mouse settings, render settings, shortcut keysRecently-used file listToolbar layoutTo save schemes
Make a Windows desktop shortcut to Rhino like this:"C:/Program Files/Rhino.exe" /scheme="WhiteBackground"Set up Rhino with your white background colors and exit.Start Rhino from this shortcut.Rhino will find and store all it's settings in:HKEY_CURRENT_USER/Software/McNeel/Rhinoceros/5.0/Scheme:WhiteBackground/...Make another shortcut:"C:/Program Files/Rhino.exe" /scheme="BlackBackground"Set up Rhino with your black background colors and exit.Start Rhino from this shortcut.Rhino will find and store all it's settings in:HKEY_CURRENT_USER/Software/McNeel/Rhinoceros/5.0/Scheme:BlackBackground/...
## Start Rhino in safe mode
{: #start-rhino-in-safe-mode}
Safe modeis a method of opening Rhino with features disabled that might be the cause of crashing.
Safe mode is not designed to be a working mode – it is a troubleshooting, problem solving mode.
Use safe mode if Rhino crashes immediately on starting, crashes when shading, or crashes when running commands that are part of a plug-in. Please report all problems crashing Rhino to the Rhino development team.
If you launch Rhino in safe mode, the following items will be disabled:
Any start-up commands listed in [General Options](general.html) .Command line scripts specified by the "/runscript" argument.All plug-ins.Templates.OpenGL shading.To open Rhino in safe mode
On the WindowsStartbutton, underPrograms, selectRhinoceros in Safe Mode.Get technical support:
 [Technical support](http://discourse.mcneel.com/)  [Rhino Web Site](http://www.rhino3d.com) See also
![images/open.png](images/open.png) [Open](open.html) 
Open an existing model file.
 [Work with files](sak-file.html) 
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](startingrhino.html) 


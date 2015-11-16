---
---

{: #kanchor1735}{: #kanchor1736}
# PointDeviation
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/pointdeviation.png](images/pointdeviation.png) [Surface Analysis](surface-analysis-toolbar.html) 
Menus
Analyze
Surface![images/menuarrow.gif](images/menuarrow.gif)
Point Set Deviation
The PointDeviation command reports the distance between selected [point objects](points.html), [control points](controlpoint.html), [mesh vertices](meshvertex.html), and a surface.
Steps
 [Select](select-objects.html) the objects from which to measure, and press [Enter](enter-key.html) .In the Point / Surface Deviation dialog box you can change the color of the selected point objects and mark them with indicator lines.Point / Surface Deviation options
Options
Proximity angle
Points qualify for display if the hair line is this close to the normal direction on either the curve or the surface. Default is 1 degree. No points disqualify at 180.
Hair scale
The hair is exaggerated by this factor from the actual distance to the curve or surface. Default is 10.
Display hair
Display the hair line for each qualifying point.
Make hair permanent
Create a line object when the command terminates. Line objects are created on layers with names "Point Test *&lt;color&gt;* ".
Statistics
Point count
The number of points.
Mean distance
The [mean](http://en.wikipedia.org/wiki/Mean) distance between the selected points and the selected surface.
Median distance
The [median](http://en.wikipedia.org/wiki/Median) distance between the selected points and the selected surface.
Standard deviation
The [standard deviation](http://en.wikipedia.org/wiki/Standard_deviation) distance between the selected points and the selected surface.
Ignore
Points beyond this distance are ignored.
Bad point
Points beyond this distance are colored red or ignored.
Good point
Points closer than this distance are colored blue.
On surface
Points on the surface are colored blue.
 **Apply** 
After changing settings in the dialog box, clickApplyto recalculate the display.
See also
 [Analyze objects](sak-analysis.html) 
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](pointdeviation.html) 


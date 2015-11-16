---
---


# Curve
{: #kanchor521}
{: #kanchor520}
{: #kanchor519}
{: #kanchor518}
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/curve.png](images/curve.png) [Curve Drawing](curve-drawing-toolbar.html)  [Curve](curve-toolbar.html)  [Main2](main2-toolbar.html) 
Menus
Curve
Free-Form![images/menuarrow.gif](images/menuarrow.gif)
Control Points
The Curve command draws a curve from [control point](controlpoint.html) locations.
Steps
 [Pick](pick-location.html) the start of the curve.Pick the next points.Press [Enter](enter-key.html) to end the curve.The Curve command makes a curve of degree &lt;number of points&gt; -1 as long as the number of [control points](controlpoint.html) is less than or equal to the degree setting.Your browser does not support the video tag.Command-line options
AutoClose
Closes the curve when the cursor moves close to the curve's start point.
AutoClose steps
Move the cursor close to the start point of the curve, and pick.The curve will close.Press the [Alt](alt-key.html) key to suspend automatic closing.Degree
Specifies the [degree](degree.html) of the curve (or surface).
When drawing a high-degree curve, the output curve will not be the degree you request unless there is at least one more [control point](controlpoint.html) than the degree.
PersistentClose
The PersistentClose option closes the curve as soon as there are two points placed.
If you continue to pick points, the curve updates the shape while remaining closed.
Close
Closes the curve smoothly, creating a [periodic curve](makeperiodic.html).
Sharp
Closes the curve with a kink, creating a [non-periodic curve](makeperiodic.html#makenonperiodic).
Undo
The Undo option reverses the last action.
See also
 [Draw lines and curves](sak-curve.html) 
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](curve.html) 


---
---


# Convert
{: #kanchor436}
{: #kanchor435}
{: #kanchor434}
{: #kanchor433}
{: #kanchor432}
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/convert-polyline.png](images/convert-polyline.png) [Arc](arc-toolbar.html)  [Curve Tools](curve-tools-toolbar.html)  [Lines](lines-toolbar.html) 
Menus
Curve
Convert
The Convert command changes the structure of a curve to polyline or arc segments.
Steps
 [Select](select-objects.html) curves to convert.Select options.Command-line options
Output
{: #arcs}Arcs
Converts the curve to arc segments. Sections of curves that are nearly straight are converted to straight-line segments.
{: #lines}Lines
Converts the curve to polyline segments.
SimplifyInput
TheYesoption combines co-linear line segments and co-circular arc segments.
Simplifying ensures that [NURBS](http://www.rhino3d.com/nurbs) curves that consist of arc and line segments are split into proper arc and line segments making the conversion to arcs and lines more accurate.
The simplification step is done using the [absolute](units.html#absolutetolerance) and [angle](units.html#angletolerance) tolerance, not the custom tolerance settings set in the command.
Use theNooption in cases where simplifying is too aggressive and converts normal [NURBS](http://www.rhino3d.com/nurbs) curves into arcs or lines to get a more accurate answer.
DeleteInput
Yes
Deletes the original geometry.
No
Retains the original geometry.
AngleTolerance
The maximum angle between segments at endpoints, overriding the [system tolerance](units.html#absolutetolerance) setting.
Specify 0 (zero) to allow non-tangent arcs. The output will have kinks, but since it consists of arc segments, there will be fewer segments than if theLinesoption was used. This is useful for approximating a curve with the smallest number of segments.
Tolerance
The tolerance at segment midpoints, overriding the [system tolerance](units.html#absolutetolerance) setting.
MinLength
The minimum segment length. Specify 0 (zero) for no minimum limit.
MaxLength
The maximum segment length. Specify 0 (zero) for no maximum limit.Options
OutputLayer
Specifies the layer for the results of the command.
Current
Places the results on the current layer.
Input
Places the results on the same layer as the input curve.
TargetObject
Places the results on the same layer as the target surface.

# ConvertToBeziers
{: #kanchor439}
{: #kanchor438}
{: #kanchor437}
{: #converttobeziers}
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/-no-toolbar-button.png](images/-no-toolbar-button.png) [Not on toolbars.](toolbarwhattodo.html) 
Menus
![images/-no-menu-item.png](images/-no-menu-item.png) [Not on menus.](menuwhattodo.html) 
The ConvertToBeziers command changes the structure of a [NURBS](http://www.rhino3d.com/nurbs) curve or surface to a Bézier curve or surface.
Steps
 [Select](select-objects.html) the objects.Choose either to keep or to delete the input objects.See also
 [Edit curves](sak-curvetools.html) 
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](convert.html) 


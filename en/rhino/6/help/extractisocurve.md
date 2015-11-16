---
---


# ExtractIsocurve
{: #kanchor974}
{: #kanchor973}
{: #kanchor972}
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/extractisocurve.png](images/extractisocurve.png) [Curve From Object](curve-from-object-toolbar.html) 
Menus
Curve
Curve From Objects![images/menuarrow.gif](images/menuarrow.gif)
Extract Isocurve
The ExtractIsocurve command creates curves that duplicate surface [isoparametric curves](isocurve.html) at specified locations on the surface.
Steps
 [Select](select-objects.html) a surface.The [cursor](cursor-tracking-line.html) is constrained to the surface, and [isoparametric curves](isocurve.html) display at cursor.The [draft angle](draftangleanalysis.html) of the surface displays at the status bar. [Pick](pick-location.html) to create the curve(s).Use theIntobject snap for snapping to [isoparametric curves](isocurve.html) intersections.Your browser does not support the video tag.Command-line options
Direction(Surfaces only)
Specify the u, v, or both [directions](curvesurfacedirection.html).
ExtractAll
Extracts all isocurves in u, v, or both directions depending on theDirectionoption.
Toggle(Surfaces only)
Toggles the [direction](curvesurfacedirection.html) between u and v.
IgnoreTrims
Determines whether surface trims are ignored or taken into consideration. When the marker misses the untrimmed surface, the *no-access cursor* is shown.
![images/noaccesscursor.png](images/noaccesscursor.png)
No access cursor.
Note
TheExtractIsocurvecommand creates the simplest possible curve exactly on the surface in u, v or both [directions](curvesurfacedirection.html) .TheExtractIsocurvecommand is useful for creating trimming curves on surfaces. You can make surfaces trimmed along [isoparametric curves](isocurve.html) into untrimmed surfaces with [ShrinkTrimmedSrf](shrinktrimmedsrf.html) .You can use [isoparametric curves](isocurve.html) to recreate an existing surface with different [parameterization](parameterization.html). To do this, extract several isoparametric curves, and [Loft](loft.html) a surface through them.If you need to put angled cross sections along a surface, use the [Section](section.html) command instead of theExtractIsocurvecommand. If you need curved cross sections, use the [Project](project.html) or [Intersect](intersect.html) commands.The [Knot](object-snaps.html#osnap-knot) object snap can be used to create [isoparametric curves](isocurve.html) at exact [knot](knot.html) locations.In contrast to the [InsertKnot](insertknot.html) command, theExtractIsocurvecommand creates separate curves that are not attached to the surface.If you need to place an object on a surface, use theExtractIsocurvecommand to add visual cues or locations that can be snapped to on the surface area and help position the object. Using theExtractIsocurvecommand does not change the surface in any way.See also
 [Extract object sub-elements](sak-extract.html) 
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](extractisocurve.html) 


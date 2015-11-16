---
---

{: #kanchor1557}{: #kanchor1558}{: #kanchor1559}
# OffsetSrf
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/offsetsrf.png](images/offsetsrf.png) [Surface Tools](surface-tools-toolbar.html) 
Menus
Solid
Offset
Surface
Offset Surface
![images/history-tag.png](images/history-tag.png) [&#160;History enabled](historyenabled.html) 
The OffsetSrf command copies a surface or polysurface so that locations on the copied surface are the same specified distance from the original surface.
Steps
 [Select](select-objects.html) a surface or polysurface.Infinite Plane: TypeIPfor [InfinitePlane](infiniteplane.html) options.
Type the offset distance, and press [Enter](enter-key.html) .Your browser does not support the video tag.Options
Distance
Specifies a distance for the offset.
Corner
Round
Creates a fillet at sharp corners in the original surface.
Sharp
Maintains the sharp corner when the original surface has a sharp corner.
FlipAll
Flips the offset direction of all selected surfaces. Arrows indicate the positive offset direction.
Your browser does not support the video tag.Solid
Makes a closed solid from the input and offset surfaces by lofting a ruled surface between all of the matching edges.
Your browser does not support the video tag.Loose *(Surfaces only)* 
The resulting surface point structure is identical to the original surface.
Your browser does not support the video tag.Tolerance
Sets the tolerance for the offset surface. Type 0 to use the default tolerance.
BothSides
Draws the offset on both sides of the original.
Your browser does not support the video tag.DeleteInput
Yes
Deletes the original geometry.
No
Retains the original geometry.
Note
Positive values offset in the direction the arrows. Negative values offset the other way.When a plane, torus, sphere, open cylinder, or open cone surface is offset, the resulting surface is exact. Free-form surfaces are offset to within the value of theToleranceoption.When offsetting surfaces are joined that are part of a polysurface, there is no guarantee that the offset surfaces will also join into another polysurface. For example, offsetting the six sides of a box will not result in a larger closed box. It will return six separate surfaces with gaps between the edges.TheOffsetSrfcommand does not maintain the overall structure of the starting polysurface in the offsets. Each surface offsets as an individual object.
### Troubleshoot shelling
 [Shell](shell.html) and [OffsetSrf](#) for polysurfaces are works in progress. There are several known problem areas:
Singular surfaces can cause problems, especially when the offset of the surface must be extended at the singularity. The extensions are done in [OffsetSrf](#) (Corner= *Sharp* ) and shelling, which always uses sharp corners. These extensions happen when the offsets of adjacent surfaces come apart. Also, cone-like singularities cause problems in all cases.Complex vertices (ones with more than three edges) can be problematic, especially in shelling and sharp corner offsets and where some, but not all, of the surfaces at the vertex offset apart.![images/shellthreecorner.png](images/shellthreecorner.png) [OffsetSrf](#) on polysurfaces with naked edges, where the naked edges make concave boundaries will not work correctly.![images/shellnakedconcave.png](images/shellnakedconcave.png)If faces adjacent to the removed faces offset in such a way that the removed face must be extended to fill in the gap, it will fail.![images/shelloffsetaway.png](images/shelloffsetaway.png)Any surface whose offset self-intersects will cause a problem.See also
 [Create surfaces](sak-surface.html) 
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](offsetsrf.html) 


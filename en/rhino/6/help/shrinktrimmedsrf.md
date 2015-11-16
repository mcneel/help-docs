---
---

{: #kanchor2026}{: #kanchor2027}{: #kanchor2028}{: #kanchor2029}{: #kanchor2030}
# ShrinkTrimmedSrf
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/shrinktrimmedsrf.png](images/shrinktrimmedsrf.png) [Geometry Fix](geometry-fix-toolbar.html)  [Surface Tools](surface-tools-toolbar.html) 
Menus
Surface
Surface Edit Tools![images/menuarrow.gif](images/menuarrow.gif)
Shrink Trimmed Surface
The ShrinkTrimmedSrf command contracts the underlying untrimmed surface close to trimming boundaries.
Shrinking a surface is like [extending](extendsrf.html) smoothly, only backwards. [knot](knot.html) of full multiplicity are added where you want the surface to be cut off. Then the remaining [control points](controlpoint.html) are thrown away.
Steps
 [Select](select-objects.html) trimmed surfaces. [Trimmed surfaces](trim.html) are represented by an untrimmed surface with trimming boundaries. When textures are applied to surfaces, the textures map to the underlying untrimmed surface. Sometimes the underlying untrimmed surface is much larger than the trimmed surface, resulting in only a small portion of the texture showing up in the rendering.To fix this, the ShrinkTrimmedSrf command shrinks the underlying untrimmed surface in order to make it as small as possible, resulting in the maximum amount of the texture map displaying in the rendering.You will see no visible change in the surface. Only the underlying untrimmed surface alters.Your browser does not support the video tag.
# ShrinkTrimmedSrfToEdge
{: #shrinktrimmedsrftoedge}
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) ![images/shrinktrimmedsrftoedge.png](images/shrinktrimmedsrftoedge.png)Toolbars
 [Surface Tools](surface-tools-toolbar.html) 
Menus
![images/-no-menu-item.png](images/-no-menu-item.png) [Not on menus.](menuwhattodo.html) 
The ShrinkTrimmedSrfToEdge command contracts the underlying untrimmed surface right to the to the trimming boundaries.
Shrinking the trimmed surface can sometimes cause problems later since having the edges so close to the trimming boundaries can cause commands that use the surface edges as input to fail.
Compare the video with ShrinkTrimmedSrf. Notice in the close-ups that there is a tiny margin between the control points and the trimmed surface. This margin is eliminated with ShrinkTrimmedSrfToEdge.
Steps
 [Select](select-objects.html) trimmed surfaces.Your browser does not support the video tag.See also
 [Edit surfaces](sak-surfacetools.html) 
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](shrinktrimmedsrf.html) 


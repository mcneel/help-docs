---
---


# Explode
{: #kanchor933}
{: #kanchor932}
{: #kanchor931}
{: #kanchor930}
{: #kanchor929}
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/explode.png](images/explode.png) [Curve Drawing](curve-drawing-toolbar.html)  [Geometry Fix](geometry-fix-toolbar.html)  [Main2](main2-toolbar.html)  [Popup](popup-toolbar.html)  [Solids Sidebar](solids-sidebar-toolbar.html)  [Surface Sidebar](surface-sidebar-toolbar.html) 
Menus
Edit
Explode
The Explode command breaks objects down into components.
Steps
 [Select](select-objects.html) objects.Your browser does not support the video tag.
## Explode results
Explode breaks down objects as follows:
Object
Result
 [Blocks](block.html) 
Explodes blocks into component curves, surfaces, meshes, text, blocks, etc.
When linked blocks are exploded, a layer tree for the objects is created.
 [Dimensions](dim.html) 
Curves and text.
 [Groups](group.html) 
Explodes objects contained in the group, but leaves the objects grouped.
 [Hatch](hatch.html) 
Single segment lines and planar surfaces.
 [Mesh](mesh.html) 
Mesh parts and mesh faces based on unwelded edges. If a mesh is completely [unwelded](weld.html#unweld), then it will explode to its individual faces. ( [Unweld](weld.html#unweld) &gt; 0 degrees).
Note
When Rhino creates a seamless (closed) mesh from a complex closed polysurface [NURBS](http://www.rhino3d.com/nurbs) object, the resulting mesh, when exported, can make a mesh that is too large to be imported into other programs. The simple meshes that result from exploding the joined mesh may be small enough.Completely unwelded meshes such as imported *.stl files will explode into individual mesh faces, resulting in a separate mesh in the current file for each mesh face. The overhead required for this can greatly increase the amount of memory used and potentially crash. Welding a mesh completely ( [Weld](weld.html) command, 180 degrees) then unwelding ( [Unweld](weld.html#unweld) command) at some reasonable angle such as 20-30 degrees may allow the mesh to explode into a more manageable number of meshes containing multiple polygon faces. [Cage&#160;controls](cage.html) 
Curves, surfaces, cages.
 [Polysurface](polysurface.html) 
Surfaces.
 [Polycurve](polycurve.html) 
Single segment curves.
 [Polyline](polyline.html) 
Single segment lines/curves.
 [Text](text.html) 
Curves.

# ExplodeBlock
{: #kanchor934}
{: #explodeblock}
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/explodeblock.png](images/explodeblock.png) [Block](block-toolbar.html) 
Menus
Edit
Explode Block
TheExplodeBlockcommand reduces blocks into component objects (including any nested blocks).
Steps
 [Select](select-objects.html) blocks to explode.Command-line options
AllBlocks
Explodes all of the blocks in the file.
GroupOutput
 [Groups](group.html) the resulting objects.
See also
 [Split and trim curves and surfaces](sak-splittrim.html) 
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](explode.html) 


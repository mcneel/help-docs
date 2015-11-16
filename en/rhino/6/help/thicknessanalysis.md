---
---

{: #kanchor2179}{: #kanchor2180}{: #kanchor2181}{: #kanchor2182}
# ThicknessAnalysis
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/thicknessanalysis.png](images/thicknessanalysis.png) [Surface Analysis](surface-analysis-toolbar.html) 
Menus
![images/-no-menu-item.png](images/-no-menu-item.png) [Not on menus.](menuwhattodo.html) 
The ThicknessAnalysis command uses false-color display to evaluate the thickness of a solid.
Notes:
The ThicknessAnalysis command is not designed to evaluate the distance between two independent surfaces.To evaluate the distance between two surfaces compare the points on the first surface to the second surface using the [PointDeviation](pointdeviation.html) command.The easiest way to generate a set of points on a surface is to create a mesh using the [Mesh](mesh.html) command and then use [PointDeviation](pointdeviation.html) on the resulting mesh object and the second surface.For every vertex in the mesh the distance from the vertex to the "other side" of the mesh is calculated. Then a color is assigned to the vertex based on that distance. If the distance is less than or equal to the minimum distance the color is red. If the distance is greater than the maximum distance, the color is white. If the distance is between the minimum and maximum distances, a color between red and blue is assigned. Distance close to the minimum distance are more red than blue and distances close to the maximum distance are more blue than red. A report is printed in the command prompt window that lists the number of vertices tested and the percentage of vertices with distances less than or equal to the minimum distance, between the minimum and maximum distances, and beyond the maximum distance.The distance from a vertex to the "other side" of the mesh is calculated as follows.A = a set of triangles that touch the vertex.A triangle, T, is on the "other side" of the mesh if there is some triangle in set A where the angle between the normals is greater than 91 degrees.B = a set of triangles that are on the "other side" of the mesh from the vertex.For every triangle in B, the distance from the vertex to the closest point on the triangle is calculated. The smallest one of these distances is the distance from the vertex to the other side of the mesh.Steps
Type the minimum or maximum acceptable thickness.Command-line options
If the analysis takes a long time, a prompt to continue appears.
Do you want to continue for another 6 minutes
Yes
Continues the analysis for an additional six minutes.
No
Stops the analysis.
ForAsLongAsItTakes
Continues the analysis no matter how long it takes.
Warning
Once you commit to allowing the analysis to continue, you cannot stop the command with [Esc](esc-key.html).
Example
The thickness analysis dialog box has a range of values.
Blue = B; Red = R
Assume 0 &lt; R &lt; B.
For each analysis [mesh vertex](meshvertex.html) V, Rhino searches for a point P on "the other side".
d = the distance from P to V.
If d &lt;= R, the vertex V is red.
If d &gt; B, the vertex is white.
If R &lt;= d &lt;= B, the vertex is the appropriate color in the range from red to blue.
The percentage reported is the percentage of analysis [mesh vertices](meshvertex.html) that are not white. In this example, it is the percentage of the analysis mesh vertices whose distance to the "other side" point is &lt;= B.

# ThicknessAnalysisOff
{: #thicknessanalysisoff}
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/thicknessanalysisoff.png](images/thicknessanalysisoff.png) [Surface Analysis](surface-analysis-toolbar.html) 
Menus
![images/-no-menu-item.png](images/-no-menu-item.png) [Not on menus.](menuwhattodo.html) 
The ThicknessAnalysisOff command turns off thickness analysis display.
See also
 [Analyze objects](sak-analysis.html) 
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](thicknessanalysis.html) 


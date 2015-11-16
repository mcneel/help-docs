---
---

{: #kanchor2195}
# TriangulateNonPlanarQuads
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/triangulatenonplanarquads-triangulatemesh-rt.png](images/triangulatenonplanarquads-triangulatemesh-rt.png) [Mesh Tools](mesh-tools-toolbar.html) 
Menus
Mesh
Mesh Edit Tools![images/menuarrow.gif](images/menuarrow.gif)
Triangulate Non Planar Quads
The TriangulateNonPlanarQuads command splits all non-planar quadrangular polygon mesh faces into two triangular mesh faces.
Options
Distance
Any quadrangle where the distance of the quad's fourth point from the plane defined by the quad's first three points is greater than or equal to theDistancevalue will be triangulated.
Angle
Any quadrangle where the angle between the plane normals of the face triangles if it were triangulated is greater than or equal to theAnglevalue will be triangulated.
Increment
The value by which theDistanceandAngleedit boxes are increased or decreased with the spinner controls.
Select Face
Select a mesh face to set theDistanceandAnglevalues.
See also
 [Edit mesh objects](sak-meshtools.html) 
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](triangulatenonplanarquads.html) 


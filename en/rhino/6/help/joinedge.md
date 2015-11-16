---
---

{: #kanchor1276}{: #kanchor1277}{: #kanchor1278}{: #kanchor1279}{: #kanchor1280}
# JoinEdge
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/joinedge.png](images/joinedge.png) [Geometry Fix](geometry-fix-toolbar.html)  [Edge Tools](edge-tools-toolbar.html) 
Menus
Surface and Analyze
Edge Tools![images/menuarrow.gif](images/menuarrow.gif)
Join 2 Naked Edges
The JoinEdge command joins two naked edges that are out of tolerance.
Steps
 [Select](select-objects.html) two naked surface or polysurface edges that are coincident or close together.If the edges overlap (run somewhat parallel) along at least part of their length (an interval), but are not coincident, theEdge Joiningdialog box reports, "Joining these edges requires a join tolerance of *&lt;distance&gt;*. Do you want to join these edges?". The surfaces will extend to join along the intervals.Warning
JoinEdgedoes not fill any gaps between surfaces. When surfaces won't [Join](join.html), that's an indication that more time should be spent fixing the gap/overlap/other problem so they WILL join.If the surface edges are not close to each other, you may have problems later on, depending on what you do with the model.If you cannot join surfaces using the [Join](join.html) command, you should make the surfaces more accurate.If you useJoinEdge, you should learn what it does and use good judgment. Try to think of it as a shortcut for changing your tolerance to a bigger value, doing a [Join](join.html), and resetting the tolerance.
# UnjoinEdge
{: #unjoinedge}
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/-no-toolbar-button.png](images/-no-toolbar-button.png) [Not on toolbars.](toolbarwhattodo.html) 
Menus
![images/-no-menu-item.png](images/-no-menu-item.png) [Not on menus.](menuwhattodo.html) 
The UnjoinEdge command separates selected polysurface edges.
Seams in closed surfaces will not separate.
Your browser does not support the video tag.
See also
 [Edit surfaces](sak-surfacetools.html) 
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](joinedge.html) 


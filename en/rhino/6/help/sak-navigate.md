---
---


# Navigate in viewports
Navigation is accomplished using a camera and target metaphor. The camera and target can be visualized with the [Camera](camera.html) command.
The viewport title has some special functions for manipulating the viewport.
Click the title to make the viewport active without disturbing the view.Drag the viewport title to move the viewport.Double-click the viewport title to maximize the viewport. Double-click again to restore the size to normal.
## Viewport projection
Viewports can have one of three projections: parallel, perspective or two-point perspective.
Right mouse navigation works differently in the two viewport styles. In parallel views, right mouse dragging pans the view. In perspective views, right-mouse dragging rotates the view. In the usual four-viewport layout, there are three parallel viewports and one perspective viewport.
Parallel
Parallel views are also called orthogonal views in some systems. In a parallel view, all the grid lines are parallel to each other, and identical objects look the same size, regardless of where they are in space.
![images/parallelprojection.png](images/parallelprojection.png)
Parallel projection.
Perspective
In a perspective view, grid lines converge to a vanishing point. This provides the illusion of depth in the viewport. Perspective projection makes objects farther away look smaller.
![images/perspectiveprojection.png](images/perspectiveprojection.png)
Perspective projection.

## Viewport navigation
Rhino’s easy navigation helps you to visualize your model.
The simplest way to change the view is to drag the mouse with right button held down. This pans the view in parallel views and rotates the view in perspective views.
You can change your view in the middle of a command to see precisely where you want to select an object or choose a point.
![images/-no-toolbar-button.png](images/-no-toolbar-button.png) [Camera](camera.html) 
Show, hide, or toggle the visibility of the viewport camera.
![images/undoview.png](images/undoview.png) [UndoView](undoview.html) 
Undo the last view change.

## Pan and Rotate
![images/pan.png](images/pan.png) [Pan](pan.html) 
Shift the location of the view camera and target parallel to the view plane.
![images/rotatecamera-rotateview-rt.png](images/rotatecamera-rotateview-rt.png) [RotateCamera](rotatecamera.html) 
Rotate the view target around the camera.
![images/rotateview.png](images/rotateview.png) [RotateView](rotateview.html) 
Rotate the view camera around the target.
![images/tilt view.png](images/tilt view.png) [TiltView](tiltview.html) 
Rotate the view around the view axis.

## Zoom
![images/dollyzoom.png](images/dollyzoom.png) [DollyZoom](dollyzoom.html) 
Move the camera location and change the lens length at the same time.
![images/zoom.png](images/zoom.png) [Zoom](zoom.html) 
Move the viewport camera so the area defined by a window selection fills the viewport.
![images/zoom1to1calibrate.png](images/zoom1to1calibrate.png) [Zoom1To1Calibrate](zoom.html#zoom1to1calibrate) 
Calibrate the screen for the Zoom command, 1To1 option.
![images/zoomlens.png](images/zoomlens.png) [ZoomLens](zoom.html#zoomlens) 
Adjust the lens length of the viewport camera in a perspective view.
![images/-no-toolbar-button.png](images/-no-toolbar-button.png) [ZoomNaked](zoomnaked.html) 
Zooms to include all naked edges on selected objects with naked edges.
![images/-no-toolbar-button.png](images/-no-toolbar-button.png) [ZoomNonManifold](zoomnonmanifold.html) 
Zooms to include all non-manifold edges on selected objects with [non-manifold](non-manifold-edges.html) edges.

## Set a view
![images/movetargettoobjects.png](images/movetargettoobjects.png) [MoveTargetToObjects](movetargettoobjects.html) 
Move the target to the center of selected objects.
![images/namedview.png](images/namedview.png) [NamedView](namedview.html) 
Manage the named views.
![images/-no-toolbar-button.png](images/-no-toolbar-button.png) [OneView](oneview.html) 
Sets the active construction plane according to the current view direction to accommodate single-window modeling.
![images/orientcameratosrf.png](images/orientcameratosrf.png) [OrientCameraToSrf](orientcameratosrf.html) 
Align the view to a surface normal.
![images/perspectiveangle.png](images/perspectiveangle.png) [PerspectiveAngle](perspectiveangle.html) 
Set the viewport field-of-view angle.
![images/perspectivematch.png](images/perspectivematch.png) [PerspectiveMatch](perspectivematch.html) 
Allow matching the view to the Wallpaper image.
![images/plan.png](images/plan.png) [Plan](setview.html#plan) 
Set the viewport to a parallel plan view.
![images/setview-top.png](images/setview-top.png) [SetView](setview.html) 
Change the view to a standard construction plane view.
![images/setviewtospotlight.png](images/setviewtospotlight.png) [SetViewToSpotlight](setviewtospotlight.html) 
Match the view to a spotlight direction.
![images/-no-toolbar-button.png](images/-no-toolbar-button.png) [SwapView](swapview.html) 
Exchange the views in two viewports with one another.
See also
![images/synchronizeviews.png](images/synchronizeviews.png) [SynchronizeViews](synchronizeviews.html) 
Set the scale and center of all viewports to match the active viewport.
![images/turntable.png](images/turntable.png) [Turntable](turntable.html) 
Rotate a view around the target.
![images/walkabout.png](images/walkabout.png) [WalkAbout](walkabout.html) 
Toggle between WalkAbout and normal navigation modes.
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](sak-navigate.html) 


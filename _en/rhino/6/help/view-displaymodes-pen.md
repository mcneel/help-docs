---
---


# Pen display mode
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/options.png](images/options.png) [Properties](properties-toolbar.html)  [Standard](standard-toolbar.html)  [Tools](tools-toolbar.html) 
Menus
Tools
Options![images/menuarrow.gif](images/menuarrow.gif)
View![images/menuarrow.gif](images/menuarrow.gif)
Display Modes![images/menuarrow.gif](images/menuarrow.gif)
ThePendisplay mode uses white with black lines to simulate a pen drawing.
![images/pen-002.png](images/pen-002.png)

### Display Mode Options
{: #name}Name
Name of display mode.

### Viewport settings
For Artistic and Pen display modes, the background is automatically set to a specified image file.
To use a custom background
 [Copy](view-displaymode-options.html#copy) an Artistic or Pen mode.The background setting will be available in the copy.Background{: #kanchor2851}
For Pen and Artistic modes, the background is automatically set.
Image file
Specifies an image for the viewport background.
Image file name
Type or browse for the file name. [![images/transparent.gif](images/transparent.gif)Shading settings](javascript:void(0);) Shade objects
Sets the viewport to opaque shaded mode.
![images/displaymode-shadedviewport.png](images/displaymode-shadedviewport.png)
Flat shading
Shades the current viewport with no smoothing so the individual render mesh faces are visible.
See: [FlatShade](flatshade.html).
![images/flatshade-001.png](images/flatshade-001.png)
Color and material usage
Object's color
Use the color specified in the object's [properties](properties.html#displaycolor).
![images/advanceddisplay-012.png](images/advanceddisplay-012.png)
Gloss
Sets the [gloss](materialeditor.html#glossfinish) for the backface material. This can be different from the front face material.
Transparency
Sets the [transparency](materialeditor.html#transparency) for the backface material. This can be different from the front face material.
Single color for all objects
Ignores object colors and uses a single color for the shading.
![images/advanceddisplay-013.png](images/advanceddisplay-013.png)
Gloss
Sets the [gloss](materialeditor.html#glossfinish) for the backface material. This can be different from the front face material.
Transparency
Sets the [transparency](materialeditor.html#transparency) for the backface material. This can be different from the front face material.
Single object color
To select a color
Click the color swatch.Rendering material
Shades using rendering [material](materialeditor.html).
Custom material for all objects
Click **Customize** to specify the custom material.
 **Customize** 
Opens the [Custom Object Attributes Settings](view-displaymode-custom-object-attributes.html) dialog box.
Backface settings
Changes the color of the backface (the side opposite of the [surface normal](dir.html#normaldirection) ).
Use front face settings
No color change.
![images/advanceddisplay-018.png](images/advanceddisplay-018.png)
Cull backfaces
Surfaces viewed from the back will be transparent.
![images/advanceddisplay-019.png](images/advanceddisplay-019.png)
Use object's color
Surfaces viewed from the back use the color specified in the object's [Properties](properties.html#displaycolor).
Gloss
Sets the [gloss](materialeditor.html#glossfinish) for the backface material. This can be different from the front face material.
Transparency
Sets the [transparency](materialeditor.html#transparency) for the backface material. This can be different from the front face material.
Single color for all backfaces
All backfaces display a specified color regardless of the object color.
![images/advanceddisplay-020.png](images/advanceddisplay-020.png)
Gloss
Sets the [gloss](materialeditor.html#glossfinish) for the backface material. This can be different from the front face material.
Transparency
Sets the [transparency](materialeditor.html#transparency) for the backface material. This can be different from the front face material.
Single backface color
To select a color
Click the color swatch.Rendering material
Shades using rendering [material](materialeditor.html).
Custom material for all backfaces
Click **Customize** to specify the custom material.
 **Customize** 
Opens the [Custom Object Attributes Settings](view-displaymode-custom-object-attributes.html) dialog box.
Shading effects
Standard shading
Uses normal solid shading.
Parallel lines
Uses parallel lines for shading.
![images/sepl1.png](images/sepl1.png)
Width (in pixels)
Width of the lines.
Separation (in lines)
Distance between lines.
Rotation (in degrees)
Rotation angle of lines.

### Visibility
{: #visibility}
Specifies which elements will be visible in the display mode.
Show curves
Shows [curves](sak-curve.html) objects.
Show hidden lines
Displays hidden lines as [dashed lines](properties.html#linetype).
Show edges
Displays surface and polysurface [clipping planes](clippingplane.html).
Show silhouettes
Shows surface [silhouettes](silhouette.html).
Show creases
Displays [creases](creasesplitting.html) in surfaces.
Show seams
Displays surface [seams](srfseam.html).
Show intersections
Displays [intersections](intersect.html) between surfaces.
Show lights
Shows [lights](lights.html) objects
Show text
Shows [text](sak-textanddimensions.html) blocks.
Show annotations
Shows [annotations](sak-textanddimensions.html) objects.
Show points
Shows [points](sak-point.html) objects.
Show pointclouds
Shows [pointclouds](sak-point.html) objects

### Lighting scheme
The lighting used by the display mode.
Lighting method
No lighting
No shading occurs when there is no light sources added to the scene.
![images/lightingnolights.png](images/lightingnolights.png)
Scene lighting (left), No lighting (right).
Default lighting
Uses a single "head lamp" light.
Scene lighting
Uses the light objects that exist in the current model/scene.
Custom lighting
Sets up to eight custom lights.
 **Customize** 
Set an x, y, and z&#160;direction and color for each light.

### Custom Lighting Setup
Light #
Up to eight lights are available.
Direction
Setting the directional value to 0,0,0 disables the light.
Color
The color the light shines on objects.
Specular
The highlight color the light creates on glossy objects.
 **Use current scene lights** 
Identifies any lights in the scene that are [Directional](directionallight.html) lights, and uses up to eight lights to populate the fields in the dialog.
Note
This option deletes all current values in the dialog, even if there were no directional lights found in the scene.The directional lights are converted to camera-directional lights using world coordinates. **Apply** 
Applies the lighting to the model.
Ambient color
To select a color
Click the color swatch.Use advanced GPU lighting
With normal, per-vertex lighting, calculations only occur for each vertex in a mesh. Everything else in between is interpolated (invented).
This has major limitations for shading, lighting, and texturing, especially when a mesh has very few vertices. For example, a plane with four vertices, has nothing to interpolate over the plane surface. When only vertices are used, there is very little data.
With Advanced GPU (per-pixel) lighting, calculations occur for every pixel within the viewport, no matter how many vertices there are. This gives more data, and the larger the frame buffer, the more detail and data you get. The result is that you can now light the entire plane and see how light falls across the entire surface independent of how many vertices there are.
In order to display [bump mapping](materialeditor.html#bump) in Rendered mode, the [Use Advanced GPU lighting setting](#use-per-pixel-lighting) must be checked.H
![images/perpixellightng-001.png](images/perpixellightng-001.png)
Advanced GPU lighting on (left) and off (right).
See: [Wikipedia: Per-pixel lighting](http://en.wikipedia.org/wiki/Per-pixel_lighting).

# Grid

### Grid settings
Grid usage{: #kanchor2852}{: #kanchor2853}{: #kanchor2854}
Use document settings
Use settings specified in [Grid Document Properties](grid.html).
Use mode-specific settings
Specify the settings in individual modes.
Show [grid](grid.html#grid-visibility) 
Show [grid axes](grid.html#grid-axes-visibility) 
Show [world axis icon](grid.html#world-icon-visibility) 

### World axes settings
World axis icon color usage{: #kanchor2855}
Application settings
Use default setting.
Same as grid axis colors
Set colors for grid axes in [Appearance: Colors Options](appearance-colors.html).
Use specified custom colors
To select a color
Click the color swatch.
### Advanced Grid Settings
Show z&#160;axis{: #kanchor2856}
Display construction plane z&#160;axis.
Axes size (grid extent %)
Set size of axes as a percentage of the grid extents.
Grid appearance
Show grid behind / on top of all objects
Shows the grid behind all objects or allows the grid to pass through objects.
![images/gridbehindno.png](images/gridbehindno.png)
Grid behind (left) and on top of objects (right).
Use transparent grid{: #kanchor2857}
Displays the grid lines with transparency.
Transparency is not available when the [Pipeline](#pipeline) setting isWindows.
![images/gridtransparent.png](images/gridtransparent.png)
Transparency %
Grid plane usage{: #kanchor2858}
Do not use / use transparent plane
Displays the grid as lines or as a transparent plane with lines.
![images/gridtransparentplane.png](images/gridtransparentplane.png)
Do not use transparent plane (left) and Use transparent plane (right).
Transparency is not available when the [Pipeline](#pipeline) setting isWindows.
Plane color
To select a color
Click the color swatch.![images/gridtransparentplanecolor.png](images/gridtransparentplanecolor.png)
Plane transparency %
Plane visibility
Show only when grid is on
Show always

## Objects

### Selection
Shaded modes only
Shade-highlight selected surfaces and polysurfaces{: #kanchor2859}{: #kanchor2860}
Shades entire object with highlight color.
![images/shadehighlightsrfoff.png](images/shadehighlightsrfoff.png)
Shade highlight on (left) and off (right).
Shade-highlight selected meshes{: #kanchor2861}{: #kanchor2862}
Shades entire object with highlight color.
![images/shadehighlightmeshoff.png](images/shadehighlightmeshoff.png)
Shade highlight mesh on (left) and off (right).

### Control points
Control polygon usage{: #kanchor2863}{: #kanchor2864}
Use dotted / solid lines
![images/advanceddisplay-022.png](images/advanceddisplay-022.png)
Dotted (left) and solid control polygon ( right).
Line thickness{: #kanchor2865}{: #kanchor2866}
The width of the control polygon in pixels.
Control polygon color
Specifies a color for the control polygon.
Use object color
Use the color specified in the object's [Properties](properties.html#displaycolor).
![images/advanceddisplay-021.png](images/advanceddisplay-021.png)
Use fixed color
Use a specified color for all control polygons.
![images/advanceddisplay-025.png](images/advanceddisplay-025.png)
Polygon color
To select a color
Click the color swatch.Visibility
Hide control points
Hides the control points while the control polygon is displayed.
![images/advanceddisplay-023.png](images/advanceddisplay-023.png)
Hide object
Hides the object while the control polygon is displayed.
![images/advanceddisplay-024.png](images/advanceddisplay-024.png)
Hide control polygon
Hides the control polygon and only shows the control points.
![images/displaycontrolpolygon-001.png](images/displaycontrolpolygon-001.png)
Hide control polygon on (left) and off (right).
Highlight control polygon
Highlights the segments of the control polygon on either side of the control points.
![images/displaycontrolpolygon-003.png](images/displaycontrolpolygon-003.png)
Highlight control polygon on (left) and off (right).
Control point style
Square with white center
![images/controlptstyle-sqwhite.png](images/controlptstyle-sqwhite.png)
Round with white center
![images/controlptstyle-roundwht.png](images/controlptstyle-roundwht.png)
Solid square
![images/controlptstyle-solidsq.png](images/controlptstyle-solidsq.png)
Solid circle
![images/controlptstyle-solidcircle.png](images/controlptstyle-solidcircle.png)
Control point size
The control point size in pixels.
![images/controlpointsize3.png](images/controlpointsize3.png)
Size = 2 (left), size = 3 (right).

### Locked objects
Locked object usage
Use application settings
Use settings specified in [Appearance: Colors Options](appearance-colors.html).
Use specified lock color
To select a color
Click the color swatch.Use object's display attributes
Uses the [object's specified attributes](view-displaymode-custom-object-attributes.html).
Locked object appearance
Locked objects appear solid
Locked objects appear transparent
![images/advanceddisplay-008.png](images/advanceddisplay-008.png)
Gray locked object transparent.
Transparency %
Sets the amount of transparency as a percentage.
Draw objects behind all others
Draws locked objects behind all other objects.
![images/advanceddisplay-030.png](images/advanceddisplay-030.png)
Gray locked object displayed behind others.
Apply these settings to layers
Applies the settings for locked objects to locked layers.

### Dynamic display
Dynamic display usage
Sets the appearance of objects in the display
Use application settings
Use system default settings.
Display object's bounding box
Reduces the display of objects to their bounding boxes. This can speed up the display on large models.
![images/display-boundingbox.png](images/display-boundingbox.png)
Bounding box display off (left) and on (right).
Always display
Always display objects as bounding boxes.
Only display during view changes
Change objects to bounding boxes only when zooming or panning.

## Points

### Point object settings
Point style
Specifies the appearance of [point](points.html) objects.
Square with white center
Displays point objects as squares with a white center.
![images/pointstylewhitecenter.png](images/pointstylewhitecenter.png)
Size
Point object size in pixels.
Solid square
Displays point objects as a solid squares.
![images/pointstylesolid.png](images/pointstylesolid.png)
Size
Point size in pixels.

### PointCloud object settings
PointCloud style
Specifies the appearance of [point cloud](pointcloud.html) objects.
Square with white center
Displays point cloud objects as squares with a white center.
![images/pointstylewhitecenter.png](images/pointstylewhitecenter.png)
Size
Point cloud point size in pixels.
Solid square
Displays point cloud objects as a solid squares.
![images/pointstylesolid.png](images/pointstylesolid.png)
Size
Point cloud point size in pixels.
PointCloud control point style
Specifies the appearance of [point cloud](pointcloud.html)  [control points](pointson.html).
Square with white center
Displays point cloud control points as squares with a white center.
![images/pointstylewhitecenter.png](images/pointstylewhitecenter.png)
Size
Point cloud point control point size in pixels.
Solid square
Displays point cloud control points as a solid squares.
![images/pointstylesolid.png](images/pointstylesolid.png)
Size
Point cloud point size in pixels.

## Curves

### Curve settings
Curve color usage
Specifies a color for all curves.
Use object's color
Use the color specified in the curve's [Properties](properties.html#displaycolor).
Use single color for all curves
Use the specified [color](select-color.html) for all curves.
Curve color
To select a color
Click the color swatch.Curve width
Specify the curve width in pixels.

## Lines

### Technical line type settings
Hidden line color usage
Specifies a color for all hidden lines.
Use object's color
Use the color specified in the hidden line's [Properties](properties.html#displaycolor).
Use single color for all hidden lines
To select a color
Click the color swatch.Hidden line width
Specify the hidden line width in pixels.
Edge line color usage
Specifies a color for all edge lines.
Use object's color
Use the color specified in the edge line's [Properties](properties.html#displaycolor).
Use single color for all edge lines
To select a color
Click the color swatch.Edge line width
Specify the edge line width in pixels.
Silhouette line color usage
Specifies a color for all silhouette lines.
Use object's color
Use the color specified in the silhouette line's [Properties](properties.html#displaycolor).
Use single color for all silhouette lines
To select a color
Click the color swatch.Silhouette line width
Specify the silhouette line width in pixels.
Intersection line color usage
Specifies a color for all intersection lines.
Use object's color
Use the color specified in the intersection line's [Properties](properties.html#displaycolor).
Use single color for all intersection lines
To select a color
Click the color swatch.Intersection line width
Specify the intersection line width in pixels.

## Shadows

### Shadows
Shadows On
Video memory usage / shadow size
Minimum (grainy shadows)![images/arrow.png](images/arrow.png)Maximum (sharper shadows)
Soft edge quality / speed
None / faster![images/arrow.png](images/arrow.png)Softer / slower
Edge blurring
No blurring![images/arrow.png](images/arrow.png)Maximum blurring
Self shadowing artifacts
Dirty![images/arrow.png](images/arrow.png)Cleaner
Transparent objects
Never cast shadows![images/arrow.png](images/arrow.png)Always cast shadows
Camera based clipping bubble
None![images/arrow.png](images/arrow.png)Maximum radius
Shadow color
To select a color
Click the color swatch.Shadows ignore user-defined clipping planes

## Other Settings
 [![images/transparent.gif](images/transparent.gif)User interface options](javascript:void(0);) Include in View's display menu
Displays the custom display mode in the [viewport title](rhino-window.html#viewport-title-menu) and View menus.
Include in Shade command modes
Offers the custom display mode as an option for the [Shade](shade.html) command.
Allow assignment to individual objects
Allows applying this display mode to objects with the [SetObjectDisplayMode](setobjectdisplaymode.html) command.

### View Scaling
Horizontal scale
Expands the view and grid horizontally.
![images/gridscale-002.png](images/gridscale-002.png)
Vertical scale
Expands the view and grid vertically.
![images/gridscale-001.png](images/gridscale-001.png)

### Display pipeline assignment
{: #pipeline}Pipeline
The display pipeline handles all the drawing of viewports - wireframe, shaded, ghosted, etc. The drawing is either handled by Windows or by OpenGL graphics cards.
Windows(Wireframe modes only)
OpenGL

### Stereo mode settings
Stereo viewing is display-mode specific. Once a display mode is configured to operate in stereo mode, all views that are in that mode will also be viewed in stereo.
![images/stereomode.png](images/stereomode.png)
Stereo modes use what is called *asymmetry* stereo.
It is best to make a copy of an Advanced Display mode and turn on the Stereo mode settings for this copied view.
Note
To see if a system supports 3-D shutter glasses, select a stereo display mode.This should cause your view to have two rapidly flickering images. The view will appear almost blurry because of the two slightly offset copies of the viewport image. If you do not see this, and the view looks the same as any other view, then either the refresh rate is not set high enough or the video card does not support it.Video cards designed for games may support hardware stereo mode in DirectX, but not in OpenGL.Stereo usage
Stereo mode disabled
Use hardware 3D shutter glasses
Requires three forms of special hardware:
A video card and drivers that support OpenGL stereo modesA monitor that can support a refresh rate of 100hz or higherA pair of 3-D shutter glasses that can plug in to the back of your special video card.Separation
Parallax
Use anaglyph glasses
A pair of red/blue anaglyph glasses like those that you get at a 3-D movie is required.
Separation
Parallax
Color usage
Use black and white imaging
Use full-color imaging
Glasses configuration
Red and Cyan glasses
Red and Blue glasses
Red and Green glasses
Amber and Blue glasses
Flip left and right lenses
To save options for use on other computers
![images/optionsexport.png](images/optionsexport.png) [OptionsExport](optionsexport.html) 
Save [Options](options.html) settings to a file.
![images/optionsimport.png](images/optionsimport.png) [OptionsImport](optionsexport.html#optionsimport) 
Restore [Options](options.html) settings from a file.
See also
 [Viewport display modes](sak-displaymodes.html) 
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](view-displaymodes-pen.html) 


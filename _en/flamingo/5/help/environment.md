---
---

# ![images/environment.svg](images/environment.svg){:height="75px" width="75px"} Flamingo Environment
There are many types of environments in Rhino, this topic will address the Flamingo Default Environment.

The Environment effects the visible part of the background and reflections.  For effects that effect lighting the scene, see the [Sky](sun-and-sky.html) help topic.

Flamingo comes with a special environment called *[Default Flamingo Environment](environment.html)*.  This environment will sync to the current [Lighting Pre-set](lighting-tab.html). By using [Lighting pre-sets](lighting-tab.html), both the Lighting and environment will be set to appropriate scene defaults.

The complete set of property groups in the Flamingo Environment are:

> [Name](#name)
> [Material Procedure](#proceedures)
> [Advanced Material Properties](#advanced)
> [Reflective Finish](#reflective)
> [Transparency Properties](#transparent)
> [Procedural Textures](#texture_procedural)
> [Bitmap Textures](#texture_bitmap)
> [Notes](#notes)

## Environment Name
{: #name}
This is the name of the environment in the Rhino model.  Environments are stored in the Rhino model. That means a with the same name in the library or a different model will not be affected by edits to the environment in the current model. To use any environment in another model it must be exported to the [Library](libraries.html) first. The Name of the environment will also serve as its exported file name.

## Flamingo Environment
{: environment}
There are three major effects an environment effects in a rendering:

>Visible Background
>[Reflective Background](#advanced-background-reflected-sky)
>[Refractive Background](#advanced-background-refracted-sky)

The Visible Background is the basic general properties panels and is the visible environment. The [Reflective](#advanced-background-reflected-sky) and [Refractive](#advanced-background-refracted-sky) backgrounds can differ and are available in the Advanced Background section.

#### Intensity
{: #background-intensity}
Modifies the relative brightness of the background. The Intensity value is used to multiply the colors in the background and result in a lighting value.  Colors can range from 0 - 256 per channel. Intensity will multiply those values.  This becomes important if the background looks very dark compared to the rendered model.

#### Background type
{: #background-type}
Specifies the color scheme that will fill the background of the rendered image. Backgrounds can be of the following types:

> [Sky](#environment-sky)
> [Solid and gradient color](#color-backgrounds)
> [Image](#environment-image)
> [HDR and planar HDR images](#hdr-and-planar-hdr-backgrounds)

## Sky Background
{: #environment-sky}
The Sky environment uses the sun and sky settings from the [Lighting](lighting-tab.html) tabs for settings.  It is the default setting for the renderings that see the sky in the renderings.

![images/background-sky-001.png](images/background-sky-001.png)
*Automatic (left) and HDR image and sun (right).*

## Color Background
{: #color-backgrounds}
A background color controls are always present. There is always a color background even if the color is completely obscured by and image, HDRI or Sky background.

#### Solid Color
{: #solid-color}
A solid color background consists of a single color that fills the background.

![images/background-color-001.png](images/background-color-001.png)
*Solid-color background.*
See [Color Controls](#enviroment-sky-color-controls) below for more details on editing the Solid Color.

#### Two-Color Gradient
{: #two-color-gradient}
Two- and three-color gradient backgrounds only apply to perspective views. Two-color gradient backgrounds interpolate the background color between two selected colors.

![images/background-color-002.png](images/background-color-002.png)
*Two-color gradient background: blue and yellow.*
See [Color Controls](#enviroment-sky-color-controls) below for more details on editing the Two-color Gradient.

#### Three-Color Gradient
{: #three-color-gradient}
Three-color gradient backgrounds interpolate the background color between three selected colors.
![images/background-color-003.png](images/background-color-003.png)
*Three-color gradient background: blue, white, yellow.*
See [Color Controls](#enviroment-sky-color-controls) below for more details on editing the Three-color Gradient.

### Color controls
{: #enviroment-sky-color-controls}
The number of controls available  may change based on the Color Background type that is currently selected.

{% include_relative snippets/snippet-material-color-select.md %}
Gradient Backgrounds will have up to 3 color selectors that may include a top, middle and bottom color.

#### Swap Colors
Use this button to rearrange the color in the gradient from top to bottom

#### Gradient Mapping control
{: #gradient-mapping}
The colors in a gradient color background need to be mapped to the environment sphere. The Gradient mapper is used to do this.  The Gradient mapping controls will activate only when a Two or Three color gradient is selected. Gradients can only be mapped to perspective views.

#### Angles from views
{: #angle-from-views}
If Angles from View are checked in, the current color gradient will sync with the current rendered perspective view.  The top color will map to the top of the view and the bottom color will map to the bottom of the view.  All other colors will evenly distribute between those extremes.

#### View Altitude Mapper
{: #colorrange}
If the current viewport is a perspective projection, the top and bottom colors and the extents of the gradient relative to the view can be controlled. By controlling the angles above and below the horizon that each of the top, middle and bottom colors occurs.

![images/background-color-004.png](images/background-color-004.png)
*Color Gradient Mapper*

* The control shows the environment in section view.  The 90 degree marker is the Z-up coordinate. The 0 coordinate represents the horizontal ground plane. The -90 Degree marker is the Z-down coordinate.
* The grey cone of vision shows the last coordinates of the current perspective view.
* The Red arrow represents the location of the top color. At this angle and above will be the top color.
* The Green double-arrow represents the middle of the gradient blend between the top and bottom colors.  If it is a three color gradient this is also the location of the middle color.
* The Blue arrow represents the location of the bottom color.  Below this angle there will only be bottom color.

####  Get angles from View Button
Use this button to reset the Gradient mapping control to the current perspective view coordinates.

#### Top/Middle/Bottom Angles
These are angle readouts of the Top, Middle and Bottom colors in the current gradients.  They correspond the the location of the Red, Green and Blue arrows in the View altitude mapper.

## Image Background
{: #environment-image}
A background image is projected onto the background.
You can use a digital photograph, a scanned artwork, or an image created with an electronic paint program. For best results, use high-resolution images for background images. It is also a good idea to blur and lighten sharp images to simulate natural focus and aerial perspective.

>Place the model into an existing context.
>Add panoramic city or mountain skylines.
>Add surrealistic effects.

The image can be mapped to a planar, cylindrical, or spherical shape or offset using coordinates or the visual graphic.
![images/background-image-001.png](images/background-image-001.png)

### Image Properties
{: #image-properties}

>Click the **Click here to assign** button to select an image.

{% include_relative snippets/snippet-clearbitmapcache.md %}

### Projection
{: #backgroud-image-projection}
Three types of background image projections are supported: [Planar](environment-tab.html#planar), [Cylindrical](environment-tab.html#cylindrical), and [Spherical](environment-tab.html#spherical). Each projection method has its own set of controls for positioning the image.

#### Planar
{: #backgroud-image-planar}
Projects the image to a flat background.

![images/projectiontypesplanar.png](images/projectiontypesplanar.png)
Drag the pink rectangle or use the numerical controls to move or scale the background image.

![images/background-image-003.png](images/background-image-003.png) *Background area (1), image size and shape (2).*

#### Planar Options

##### XScale / YScale
Specifies the size of the background image.

##### XOffset / YOffset
Specifies the offset of the background image from the lower left corner of the viewport.

#### Cylindrical
{: #cylindrical}
Cylindrical projection maps the image to an imaginary cylinder that surrounds the model. While this projection works best with true cylindrical images, it can also be used effectively with standard panoramas built from photographs.
Specify the size and position of the image map in height and width angles. Use the graphical tools and the mouse to position and size the image. The current cone of vision is displayed in the graphic as a light gray shaded region.
![images/projectiontypescylindrical.png](images/projectiontypescylindrical.png)

#### Cylindrical Options
{: #cylindricalprojectionoptions}

#####  [Background color](environment-tab.html#backgroundcolors)

##### Width
Specifies the angular width of the image map. Enter an angle or drag the flags in the control widget to set the width. The blue area indicates the extents of the angular width.

##### Top / Bottom
Specifies the vertical extents of the image. Enter an angle or drag the flags in the control widget to set the top and bottom angles. The cylindrical projection is limited to 45&#160;degrees above or below the horizon.
![images/background-cylinder-001.png](images/background-cylinder-001.png)

##### Rotation
Specifies the image rotation and extents. Enter an angle or drag the control widget to set the rotation. The red dot indicates the center of the image. The gray area indicates the view.
![images/cylindricalcontrol-001.png](images/cylindricalcontrol-001.png)

#####  **Angles From View**
Sets the **Width** and **Top/Bottom** angles to match the viewport.

#### Spherical
{: #spherical}
Spherical projection maps the image to a complete sphere. This method generally produces good results only if with an equirectangular spherical image.

#### Spherical Options
{: #sphericalprojectionoptions}

##### Rotation
Specifies the image rotation. The red dot indicates the center of the image.

#####  **Angles From View**
Sets the rotation angle to match the viewport.

## HDR and Planar HDR Background
{: #hdr-and-planar-hdr-backgrounds}
High-dynamic-range images provide lighting from luminance information stored in the image.
Using an HDR image as an environment allows more control over the relationship between the light in the background and other light in the image. This is especially useful for depicting an interior space with a bright exterior space showing through a window.
An HDR environment image has more range of light than a normal bitmap image and can be assigned a channel so the contrast can be managed in a [multi-channel](lights-tab.html#channel) rendering.

## HDR options
{: #background-hdr-options}

>Click the **Click here to assign** button to select an image.

{% include_relative snippets/snippet-rotatehdrimage.md %}{% include_relative snippets/snippet-mirrorimage.md %}{% include_relative snippets/snippet-sunchannel.md %}{% include_relative snippets/snippet-skychannel.md %}
## Planar HDR options
{: #planar-hdr-options}
Planar high-dynamic-range images provide both an image background and lighting. These are often used outside windows in architectural renderings where light from the exterior is required.

>Click the **Click here to assign** button to select an image.

###
*Background image (left) and Planar HDR (right) shows subtle lighting difference in background.*
{% include_relative snippets/snippet-sunchannel.md %}{% include_relative snippets/snippet-skychannel.md %}
## Advanced Background
{: #advanced-background}
The **Advanced Background** settings control environments that are not visible in the rendering, but show in reflections and refractions for the objects.
In the illustration, the background is black, but the reflected environment is an HDR image of a building interior.

## Reflected
{: #advanced-background-reflected-sky}
A reflected environment is not visible in the rendered image, but it reflects in shiny objects.
![images/reflectedbackground-002.png](images/reflectedbackground-002.png)
*Normal environment (left) and reflected HDR sky environment (right).*

### Sky
Objects reflect the sky as specified in the [Lighting: Sun and Sky](sun-and-sky-tabs.html) settings.

### Custom
Objects reflect a [Color or gradient](environment-tab.html#color-and-gradient-backgrounds), [Image](environment-tab.html#image), or [HDR](environment-tab.html#hdr-and-planar-hdr-backgrounds) background.

### Visible Background
Objects reflect the visible background as specified in the [Environment](environment-tab.html) settings.

## Refracted
{: #advanced-background-refracted-sky}

### Sky
Objects refract the sky as specified in the [Lighting: Sun and Sky](sun-and-sky-tabs.html) settings.

### Custom
Objects refract a [Color or gradient](environment-tab.html#color-and-gradient-backgrounds), [Image](environment-tab.html#image), or [HDR](environment-tab.html#hdr-and-planar-hdr-backgrounds) background.

### Visible Background
Objects refract the visible background as specified in the [Environment](environment-tab.html) settings.

### No Transparent Object Alpha
{: #no-transparent-alpha-objects}
Prevents seeing alpha channel through transparent objects and will prevent alpha channel compositing through transparent objects.
If images will be pasted into the alpha channel, turn this setting off.

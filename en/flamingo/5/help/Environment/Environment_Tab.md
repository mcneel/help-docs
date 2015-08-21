---
layout: toc-page
---


# <img src="../Image/icon-environment.png"/>Environment
{: toc-title }

Environments include elements of the rendering that are not part of the actual model geometry, but only appear when rendering.

You can think of the background as an infinite sphere surrounding the model. Backgrounds are projected onto this sphere. The background sphere is not an object that you can select, but a reference surface for the background effects.

The ground plane provides an infinite horizontal platform for the image that stretches to the horizon in all directions positioned at a defined elevation. The ground plane renders much faster than using a large planar surface as a base.


## Ground plane
{: .toc-header }


### Enabled
{: .toc-header }

Turns the ground plane on.

<img src="GroundPlane-002a.png"/>


 *Ground plane disabled (left) and enabled (right).* 

### Alpha
{: .toc-header }

Applies a transparent alpha channel to the ground plane so the image can be composited with the cast shadow into another image. See: [Wikipedia article: Alpha compositing](http://en.wikipedia.org/wiki/Alpha_compositing).

<img src="GroundPlane-004a.png"/>

 *Ground plane shows shadow, but is otherwise transparent in the image.* 


### Elevation
{: .toc-header }

Specifies the ground plane's height above zero.

<img src="GroundPlane-005a.png"/>


 *Ground plane elevation above zero.* 

### Material
{: .toc-header }

Assigns a [material](..\Materials\Simple_Material_Properties.html) to the ground plane.

<img src="GroundPlane-003a.png"/>


 *Ground plane with raised elevation and water material.* 

## Background
{: .toc-header }

 **Note** : A color background is always turned on, but it may be hidden behind an image or other background.


### Intensity
{: .toc-header }

Modifies the relative brightness of the background.


## Background type
{: .toc-header }

Specifies the color scheme that will fill the background of the rendered image. Backgrounds can be of the following types:

 *  [Sky](Environment_Tab.htm#Environment_Sky) 
 *  [Solid and gradient color](Environment_Tab.htm#Color_and_Gradient_Backgrounds) 
 *  [Image](#Environment_Image) 
 *  [HDR and planar HDR images](Environment_Tab.htm#HDR_and_Planar_HDR_Backgrounds) 

## Sky
{: toc-header }

The Sky environment uses the sun and sky settings from the [Lighting](../Lighting/Lighting_Tab.html) tabs for settings.

<img src="Background-Sky-001.png"/>


 *Automatic (left) and HDR image and sun (right).* 

## Color and Gradient Color
{: toc-header }

A background color is always present, but may be obscured by images.


### Solid Color
{: .toc-header }

A solid color background consists of a single color that fills the background.

<img src="Background-Color-001.png"/>


 *Solid-color background.* 

### Two-Color Gradient
{: .toc-header }

 **Note** : Two- and three-color gradient backgrounds only apply to perspective views.

Two-color gradient backgrounds interpolate the background color between two selected colors.

<img src="Background-Color-002.png"/>


 *Two-color gradient background: blue and yellow.* 

### Three-Color Gradient
{: .toc-header }

Three-color gradient backgrounds interpolate the background color between three selected colors.

<img src="Background-Color-003.png"/>


 *Three-color gradient background: blue, white, yellow.* 

## Color controls
{: .toc-header }

Clicking a color swatch opens the [Select Color](..\General\select_color.html) dialog box.

The edit boxes indicate the angle where the color will be the most saturated.


#### To change the gradient color

 * Click the color swatches to set the colors in the [Select Color](..\General\select_color.html) dialog box.

#### To change the range of the gradient color

If the current viewport is a perspective projection, the top and bottom colors and the extents of the gradient relative to the view can be controlled.

 * Enter an angle in degrees above and below the horizon in the Top, Middle, or Bottom boxes.
Or, drag the angle markers in the angle graphic.

A cone of vision is displayed in the graphic as a light gray shaded region.

The angle filled by the background is displayed in the graphic as a light gray shaded region.

The red flag indicates the angle where the Top color will be the most saturated.

The blue flag indicates where the Bottom color&#160;will be the most saturated.

For three-color gradients, the green flag indicates the angle where the Middle color is most saturated.

<img src="Background-Color-004.png"/>


###  <kbd>Swap top and bottom colors</kbd> 
{: .toc-header }

Reverses the color order for the gradient.


###  <kbd>Get angles from view</kbd> 
{: .toc-header }

Sets the angles of the gradient extents to match the viewport.


## Image
{: toc-header }

A background image is projected onto the background.

You can use a digital photograph, a scanned artwork, or an image created with an electronic paint program. For best results, use high-resolution images for background images. It is also a good idea to blur and lighten sharp images to simulate natural focus and aerial perspective.

 * Place the model into an existing context.
 * Add panoramic city or mountain skylines.
 * Add surrealistic effects.
The image can be mapped to a planar, cylindrical, or spherical shape or offset using coordinates or the visual graphic.

<img src="Background-Image-001.png"/>


## Image Properties
{: .toc-header }

 * Click the <kbd>Click here to assign</kbd> button to select an image.

### Projection
{: .toc-header }

Three types of background image projections are supported: [Planar](Environment_Tab.htm#Planar), [Cylindrical](Environment_Tab.htm#Cylindrical), and [Spherical](Environment_Tab.htm#Spherical). Each projection method has its own set of controls for positioning the image.


#### Planar

Projects the image to a flat background.

<img src="ProjectionTypesPlanar.png"/>

 * Drag the pink rectangle or use the numerical controls to move or scale the background image.

<img src="Background-Image-003.png"/> *Background area (1), image size and shape (2).* 


##### Planar Options


###### XScale / YScale

Specifies the size of the background image.


###### XOffset / YOffset

Specifies the offset of the background image from the lower left corner of the viewport.


#### Cylindrical

Cylindrical projection maps the image to an imaginary cylinder that surrounds the model. While this projection works best with true cylindrical images, it can also be used effectively with standard panoramas built from photographs.

Specify the size and position of the image map in height and width angles. Use the graphical tools and the mouse to position and size the image. The current cone of vision is displayed in the graphic as a light gray shaded region.

<img src="ProjectionTypesCylindrical.png"/>


##### Cylindrical Options


######  [Background color](Environment_Tab.htm#BackgroundColors) 


###### Width

Specifies the angular width of the image map. Enter an angle or drag the flags in the control widget to set the width. The blue area indicates the extents of the angular width.


###### Top / Bottom

Specifies the vertical extents of the image. Enter an angle or drag the flags in the control widget to set the top and bottom angles. The cylindrical projection is limited to 45&#160;degrees above or below the horizon.

<img src="Background-Cylinder-001.png"/>


###### Rotation

Specifies the image rotation and extents. Enter an angle or drag the control widget to set the rotation. The red dot indicates the center of the image. The gray area indicates the view.

<img src="CylindricalControl-001.png"/>


######  <kbd>Angles From View</kbd> 

Sets the **Width** and **Top/Bottom** angles to match the viewport.


#### Spherical

Spherical projection maps the image to a complete sphere. This method generally produces good results only if with an equirectangular spherical image.


##### Spherical Options


###### Rotation

Specifies the image rotation. The red dot indicates the center of the image.


######  <kbd>Angles From View</kbd> 

Sets the rotation angle to match the viewport.


## HDR and Planar HDR Backgrounds
{: toc-header }

High-dynamic-range images provide lighting from luminance information stored in the image.

Using an HDR image as an environment allows more control over the relationship between the light in the background and other light in the image. This is especially useful for depicting an interior space with a bright exterior space showing through a window.

An HDR environment image has more range of light than a normal bitmap image and can be assigned a channel so the contrast can be managed in a [multi-channel](..\Lighting\Lights_Tab.htm#Channel) rendering.


## HDR options
{: .toc-header }

 * Click the <kbd>Click here to assign</kbd> button to select an image.

## Planar HDR options
{: .toc-header }

Planar high-dynamic-range images provide both an image background and lighting. These are often used outside windows in architectural renderings where light from the exterior is required.

 * Click the <kbd>Click here to assign</kbd> button to select an image.

### <img src="PlanarImageBeach.png"/>
{: .toc-header }


 *Background image (left) and Planar HDR (right) shows subtle lighting difference in background.* 

## Advanced Background
{: .toc-header }

The **Advanced Background** settings control environments that are not visible in the rendering, but show in reflections and refractions for the objects.

In the illustration, the background is black, but the reflected environment is an HDR image of a building interior.


## Reflected
{: .toc-header }

A reflected environment is not visible in the rendered image, but it reflects in shiny objects.

<img src="../image/ReflectedBackground-002.png"/>


 *Normal environment (left) and reflected HDR sky environment (right).* 

### Sky
{: .toc-header }

Objects reflect the sky as specified in the [Lighting: Sun and Sky](../Lighting/Sun_and_Sky_Tabs.html) settings.


### Custom
{: .toc-header }

Objects reflect a [Color or gradient](Environment_Tab.htm#Color_and_Gradient_Backgrounds), [Image](Environment_Tab.htm#Image), or [HDR](Environment_Tab.htm#HDR_and_Planar_HDR_Backgrounds) background.


### Visible Background
{: .toc-header }

Objects reflect the visible background as specified in the [Environment](Environment_Tab.html) settings.


## Refracted
{: .toc-header }


### Sky
{: .toc-header }

Objects refract the sky as specified in the [Lighting: Sun and Sky](../Lighting/Sun_and_Sky_Tabs.html) settings.


### Custom
{: .toc-header }

Objects refract a [Color or gradient](Environment_Tab.htm#Color_and_Gradient_Backgrounds), [Image](Environment_Tab.htm#Image), or [HDR](Environment_Tab.htm#HDR_and_Planar_HDR_Backgrounds) background.


### Visible Background
{: .toc-header }

Objects refract the visible background as specified in the [Environment](Environment_Tab.html) settings.


### No Transparent Object Alpha
{: .toc-header }

Prevents seeing alpha channel through transparent objects and will prevent alpha channel compositing through transparent objects.

If images will be pasted into the alpha channel, turn this setting off.


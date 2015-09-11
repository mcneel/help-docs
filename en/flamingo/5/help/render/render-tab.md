---
layout: toc-page
---


# <img src="../image/icon-render.png"/>Render
{: .toc-title }


## Viewport to render
{: .toc-header }


#### Active view


#### List of available viewports

Includes named views.


## Rendering resolution
{: .toc-header }

The image size and resolution are saved in the Rhino file.


### Total pixels
{: .toc-subheader }

Sets the number of total pixels in the rendered image.


### Viewport Resolution
{: .toc-subheader }

Uses the viewport size in pixels to determine the rendered image size.


### Image size
{: .toc-subheader }


#### Pixels

Sets the page units to pixels.


#### Inches

Sets page units to inches.


#### Millimeters

Sets the page units to millimeters.


#### Width

Printed image width in current size units.


#### Height

Printed image height in current size units.


#### Resolution


#### Display

The image is rendered using the pixel size of the viewport.


#### Custom

The image is rendered using a custom resolution. Type the custom width and height resolution in pixels.


#### Printer, draft quality

100 pixels per inch or 4 pixels per mm.


#### Printer, normal quality

150 pixels per inch or 6 pixels per mm.


#### Printer, high quality

300 pixels per inch or 12 pixels per mm.


#### Pixels per ___

Displays the current resolution.


## Depth of field
{: .toc-header }

This effect creates a depth of field blur that mimics a photographer's lens. A lens can only focus precisely at exactly one distance, but the decrease in sharpness is gradual around the focal distance.


### Enabled
{: .toc-subheader }

Turns on the depth-of-field effect.


### Strength
{: .toc-subheader }

Controls the size of the focus area. Setting **Strength** to zero makes the entire image is sharp. Increasing the **Strength** makes the areas outside the focal distance more blurry and makes the area in focus smaller.


### Focal distance
{: .toc-subheader }

Sets the distance for the depth of field. The distance around the depth of field point at which objects will be in focus. If theFocal distanceis set to ten units, objects about seven units behind the depth of field point and about three units in front of the depth of field point will be in focus.


### Pick
{: .toc-subheader }

Pick a point in the model for the focal distance.


## Render Engine
{: .toc-header }


### Default
{: .toc-subheader }

The default algorithm produces a very high-quality simulation. The difference in quality between the default method and the path tracer can be very subtle, particularly if indirect lighting is enabled. The difference in quality may not be worth the extra processing time.


### Path Tracer
{: .toc-subheader }

The path tracer begins by displaying a very grainy image that gradually refines and becomes smooth. This process is known as *convergence*. The path tracer can provide a better quality finished product for many models (with a simpler setup), but does so at the expense of a more complex and time-consuming calculation.

 **Note** : Using the path tracer can cause bright spot or speckle artifacts to occur during the rendering process. These artifacts are normal to the path tracer and will resolve over time.


### Advantages of using the path tracer

 * Certain advanced effects, such as caustics or blurry transmission, can be calculated with better accuracy using the path tracer.
 * Images rendered with instancing, plants, and displacement maps can converge faster.
 * The path tracer is usually easier to set up than the default method. advanced settings such as reflection shaders, daylight portals, and ambient lighting, are not used when the path tracer engine is selected.

### Disadvantages of using the path tracer

 * Images rendered using the path tracer will generally take longer to converge than images rendered using the default method. Interior daylight simulations, particularly those scenes where the windows are relatively small, may take much longer.

###  <kbd>Advanced</kbd> 
{: .toc-subheader }

Opens the Document Properties dialog box at the [Flamingo nXt](documentproperties-flamingo.html) page.


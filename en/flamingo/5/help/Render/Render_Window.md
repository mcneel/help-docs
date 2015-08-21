---
layout: toc-page
---


# Render Window
{: toc-title }

The render window provides options for exposure adjustment and adding post-processing effects.


## <img src="SaveImageAs.png"/>File menu
{: .toc-header }


### <img src="SaveImageAs.png"/>Save
{: .toc-header }

Saves the image to file including alpha channel if the image format supports it. Does not save other rendered channels or [exposure](#Adjust_Image).

The Save button allows you to save your rendering to several different image formats.


#### JPEG Bitmap (.jpeg, .jpg)

Saves JPEG compressed (lossy) 24-bit RGB with no alpha channel.


#### Portable Network Graphics (.png)

Saves non-lossy compressed 24-bit RGB with no alpha channel.


#### Tagged Image File Format (.tif, .tiff)

Saves uncompressed 24-bit RGB with no [alpha](../Environment/Environment_Tab.html#Alpha) channel.


#### Windows Bitmap (.bmp)

Saves uncompressed 24-bit RGB color with no alpha channel.


### <img src="SaveImageAs.png"/>Save with background alpha channel
{: .toc-header }

Saves image 32-bit PNG, TIF, and BMP including alpha channel background. The Alpha channel versions of the file formats are used for high-quality compositing. Backgrounds will appear black when the rendering is saved with Alpha channel.


### <img src="PrintRenderedImage.png"/>Print
{: .toc-header }

Opens the **Print Preview** dialog box.


#### Print

Opens the Print dialog box.


#### Landscape

Prints the image horizontally on the paper.


#### Portrait

Prints the image vertically on the paper.


#### Close

Closes the Print Preview dialog box.


### <img src="ExportImage.png"/>Export to native Flamingo nXt file (.nXtImage)
{: .toc-header }

Saves uncompressed luminance and color information. Saves all rendered channels including [alpha](../Environment/Environment_Tab.html#Alpha). The nXtImage files can be opened in the [Image Editor](Image_Editor.html) where [exposure](#Adjust_Image) and [post-processing effects](#Effects) can be applied and the image re-saved to another bitmap format.

The .nXtImage format is the native image format of the nXt renderers. It is the recommended format for storing your renderings, since it preserves the most information about your rendering. Images stored in this format can be manipulated in the [nXt Image Editor](Image_Editor.html) and special effects can be added. From this editor, you can save to many popular standard formats, including all of the formats supported in nXt. You can also save to [Piranesi EPix file (.epx)](http://www.piranesi.co.uk/) format.


### <img src="ExportImage.png"/>Export to HDR file
{: .toc-header }

Saves uncompressed luminance and color information. The .hdr format stores luminance data directly in a High Dynamic Range format. Non-luminance backgrounds, such as normal photographs, will appear black when saved in one of these formats.


### <img src="ExportImage.png"/>Export to EXR file
{: .toc-header }

A&#160;high-dynamic-range image file format, released as an&#160;open standard&#160;along with a set of software tools created by&#160;Industrial Light and Magic (ILM), released under a&#160;free software license. This file format supports 16-bits-per-channel&#160;floating-point&#160;values (half precision) with a sign bit, five bits of exponent, and a ten-bit&#160;mantissa. This allows a dynamic range of over thirty&#160;stops&#160;of exposure. See: [Wikipedia article: OpenEXR](http://en.wikipedia.org/wiki/OpenEXR).

The .exr format stores luminance data directly in a High Dynamic Range format. Non-luminance backgrounds, such as normal photographs, will appear black when saved in one of these formats.


## Exit
{: .toc-header }

Closes the render window.


## <img src="CopyToClipboard.png"/>Edit menu
{: .toc-header }


### <img src="CopyToClipboard.png"/>Copy
{: .toc-header }

Places a copy of the image in the Windows Clipboard.


## <img src="ZoomToActualSize.png"/>View menu
{: .toc-header }


### <img src="ZoomToActualSize.png"/>Zoom
{: .toc-header }

Magnifies the view of the image.


#### <img src="ZoomToActualSize.png"/>Actual Size


#### <img src="ZoomIn.png"/>Zoom In


#### <img src="ZoomOut.png"/>Zoom Out


#### <img src="ZoomExtents.png"/>Zoom Extents


### Rendered Display
{: .toc-header }

Displays the original rendered image.

<img src="FX-001.png"/>


### Alpha Mask
{: .toc-header }

Displays the [alpha mask](Image_Editor.html#Alpha_Channel).

<img src="AlphaChannel.png"/>


### Distance Mask
{: .toc-header }

Displays the [distance mask](Image_Editor.html#Distance_Channel).

<img src="DistanceChannel.png"/>


### <img src="HideToolbar.png"/>Hide toolbar
{: .toc-header }

Closes the toolbar.


### <img src="Help.png"/>Help
{: .toc-header }

Displays the Flamingo Help.


## <img src="ResumeRendering.png"/>Stop/Resume Rendering
{: .toc-header }

Stops/continues rendering the image.


## Toolbar
{: .toc-header }


###  [<img src="SaveImageAs.png"/>Save](Render_Window.html#Save) 
{: .toc-header }


###  [<img src="SaveImageAs.png"/>Save with background alpha channel](Render_Window.html#Save_with_alpha_channel) 
{: .toc-header }


###  [<img src="PrintRenderedImage.png"/> [Print](Render_Window.html#RenderWindowPrint) ](Render_Window.html#Print_Preview) 
{: .toc-header }


###  [<img src="ExportImage.png"/>Export to native Flamingo nXt file (.nXtImage)](Render_Window.html#Export_to_nXtImage) 
{: .toc-header }


###  [<img src="ExportImage.png"/>Export to HDR file](Render_Window.html#Export_to_HDR) 
{: .toc-header }


###  [<img src="ExportImage.png"/>Export to EXR file](Render_Window.html#Export_to_EXR) 
{: .toc-header }


###  [<img src="CopyToClipboard.png"/>Copy to clipboard](Render_Window.html#Copy) 
{: .toc-header }


###  [<img src="ZoomToActualSize.png"/>Zoom to actual image size](Render_Window.html#Zoom) 
{: .toc-header }


###  [Rendered Display](Render_Window.html#Rendered_Display) 
{: .toc-header }


###  [Alpha Mask](Render_Window.html#Alpha_Mask) 
{: .toc-header }


###  [Distance Mask](Render_Window.html#Distance_Mask) 
{: .toc-header }


### Options
{: .toc-header }


#### Pan increment

Specifies how many pixels a pan moves the image in the render window when using the arrow keys to pan.


#### Zoom increment

Specifies the ratio of the image in the render window a mouse wheel step or pressing the + or - keys moves the view in or out.


### Show/Hide menu
{: .toc-header }


###  [<img src="Help.png"/>Help](Render_Window.html#Help) 
{: .toc-header }


## Progress
{: .toc-header }


### Action
{: .toc-header }


### Pass
{: .toc-header }


### Scan line
{: .toc-header }


### Elapsed time
{: .toc-header }


### Rays / second
{: .toc-header }


### Pixels / second
{: .toc-header }


## Render Constraints
{: .toc-header }


## Adjust Image
{: .toc-header }

The settings that control the screen display also control any image file made from that display. Multiple image files with different exposure settings can be saved from a single rendering. The exposure settings for one rendered image will be applied to the next.

This adjustment process is called *tone mapping.* Tone mapping is the process of converting the luminance data used by Flamingo nXt into&#160;Red, Green, and Blue (RGB) pixels that can be displayed or printed.


### Brightness
{: .toc-header }

Adjusts the overall brightness of the image. For example, if a white surface in the model is rendering gray, increase the brightness until the surface appears white. Or, if the exterior scene seems overexposed, decrease the brightness until the scene appears more correct.

<img src="BrightnessDefault.png"/>


 *Brightness at default (left) and increased.* 

### Burn
{: .toc-header }

Adjusts the image white point. This is the brightest white color in the image. Burn can add drama, life,&#160;and sharpness to a rendering by adding more areas of white to contrast with the dark areas.

See [Wikipedia article: White point](http://en.wikipedia.org/wiki/White_point).

<img src="Burn-001.png"/>


 *Burn at the default setting (left) and increased.* 

### Saturation
{: .toc-header }

Saturation controls the amount of color in the image. A saturation of 0.00 will result in a grayscale image. Values above 1.00 can make colors richer.

<img src="SaturationDefault.png"/>


 *Saturation at the default (left) and increased by about 3 (right).* 

### Histogram
{: .toc-header }

Graphically displays the distribution of the light and dark areas in the image.

See: [Wikipedia article: Histogram](http://en.wikipedia.org/wiki/Histogram). The internet has many articles about using histograms to evaluate exposure in digital photography. The principles are the same for rendering.

<img src="Histogram.png"/>


 *Histogram.* 

#### Histogram options

 * Right-click the histogram image for options

#### Fit


#### Median


#### Mean


#### Show Sorted Graph


#### Show Scale


#### Graph Color


#### Show Luminance Values


### Lock exposure
{: .toc-header }

When the exposure settings are locked, changing the lighting will not adjust the exposure to compensate.


## Information
{: .toc-header }


### Resolution
{: .toc-header }

Displays the [render resolution](Render_Tab.html#Resolution).


### Faces
{: .toc-header }

Displays the number of mesh faces used to render the model.


### Apparent faces
{: .toc-header }

When there are blocks in the model, Flamingo nXt is able to use the block definition to render block instances without remeshing each instance. The **Apparent faces** display shows how many additional temporary faces are generated.


## Pixel information
{: .toc-header }

Window point

Image point

Image Y-Up

Pixel color

Luminance

Distance


## Lighting information
{: .toc-header }


###  [Presets](../Lighting/Lighting_Tab.html) 
{: .toc-header }


###  [Sun](../Lighting/Sun_and_Sky_Tabs.html#Sun) 
{: .toc-header }


###  [Sky](../Lighting/Sun_and_Sky_Tabs.html#Sky) 
{: .toc-header }


###  [Lights](../Lighting/Lights_Tab.html) 
{: .toc-header }


###  [Indirect](../Lighting/Lighting_Advanced_Tab.html#Indirect) 
{: .toc-header }


###  [Ambient On/Off](../Lighting/Lighting_Advanced_Tab.html#Ambient) 
{: .toc-header }


## Channels
{: .toc-header }

Displays the status of the lighting channels.


## Effects
{: .toc-header }

Post-processing effects are applied after the image is rendered. These can be turned on and off and re-ordered in the list. Each effect has its own settings.


## Effects Options
{: .toc-header }

These options are also available from a context menu.

 * Right-click an effect to display the context menu.
<img src="ToggleEffect.png"/>Toggle the on/off state of the selected effect.

<img src="MoveUp.png"/>Move the selected effect up in the list.

<img src="MoveDown.png"/>Move the selected effect down in the list.

<img src="EffectProperties.png"/>Selected effect properties.

<img src="SaveListOrderAsDefault.png"/>Save the current effects list order and properties as default.

<img src="SaveCurrentEffectsList.png"/>Save the current effects list as named list.

<img src="ImportNamedEffectsList.png"/>Import named effects list.


## Depth of Field
{: toc-header }

The Depth of Field effect blurs the image depending on the distance from the camera.

<img src="../Image/PostProcessing_DOF.png"/>


## Depth of Field Properties
{: .toc-header }


### Visual Properties


#### Blurring strength

Determines the amount of blurring. This is an arbitrary value and different values will work better with different images.


#### Max blurring

Determines the maximum blurring radius used. Since extremely blurred areas can cause the effect to be slow, this limits the effect.


### Area of Effect


#### Focal distance

The distance from the camera at which the image is in focus (not blurry).


#### Pick

Pick a location on the image to set the focal distance.


#### Blur background

Determines whether the background is blurry. The background will be blurred at the maximum effect.


## Fog
{: toc-header }

The fog effect adds depth-dependent coloration in the image. This effect can be used to add a thick fog effect or a subtle depth cue.

<img src="../Image/PostProcessing_NoFog.png"/>


 *No post processing effects.* 

### Fog as Gradient Background
{: .toc-header }

Fog can be used to create a gradient background.

In this case the settings to create the background are as follows:

Strength = 1Noise = .1Fog Color = BlackEnd distance = approximately 110Start distance = approximately 90Fog Background = OnFeathering = 80

<img src="../Image/PostProcessing_FogAsGradient.png"/>


 *Fog as gradient background.* 

## Fog Properties
{: .toc-header }


### Visual properties

Determines the appearance of the fog effect.


#### Strength

Determines the maximum amount of fogginess. Setting Strength to 0.0 turns the effect off; setting Strength to 1.0 represents total fog. Values higher than 1.0 can be used but only make sense when used with the **Noise**.


#### Noise

Adds a random variation to Fog **Strength**.


#### Color

Specifies the fog color.

 * Click the color swatch to select a color from the [Select color](../General/select_color.html) dialog box.
 * Click the **Pick** button to select the color from the rendered image.

### Area of effect

Determines the area encompassed by the fog effect.


#### Start distance

Specifies the distance from the camera at which the fog begins to appear.

 * Click the **Pick** button to pick the depth from the rendered image.

#### End distance

Specifies the distance from the camera at which the maximum amount of fogginess is achieved.

 * Click the **Pick** button to pick the depth from the rendered image.

### Bounds (Left, Right, Top, Bottom)

Specifies the area of the image affected by the fog. This can be used to create a low-lying mist effect.

 * Click the **Pick Area** button to pick bounding area from the rendered image.


### Fog


#### Fog background

Determines whether the background image is also made foggy. The background will be fogged at the maximum strength.


#### Feathering

Determines the number of pixels outside the bounding area to “fade in” the fogginess.


### Preview
{: .toc-header }

Preview the effect on the image as you change the values.


## Glare
{: toc-header }

Glare and Glow are very similar. Whereas Glow uses a selected color, Glare pushes the color to white. Glare makes extremely bright parts of the image appear to glare. It does this by making the area surrounding the bright area brighter. This very subtle effect is usually used for night scenes where it will make the lights seem much more realistic.

<img src="../Image/PostProcessing_NoGlare.png"/>


 *Glare off (left) and on (right).* 

## Glare Properties
{: .toc-header }


### White point bound
{: .toc-header }

Determines where in the tonal range the glare will begin. The value is represented on the histogram and can be adjusted graphically. Pixels lighter than the **White Point Bound** (in either luminance or the grey-scale value) will glare.


### Glare size
{: .toc-header }

The radius of the glare around the bright pixel.


### Gain
{: .toc-header }

Multiplier for the lightness of the glare. The default value of 1.0 should result in normal glare effects. Use higher values for extremely bright glare.


### Use photometric information
{: .toc-header }

When using photometric information, the amount of glare is controlled by how &quot;whiter than white&quot; the pixel is. Otherwise, the effect uses the whitest pixels in the image.


### Histogram
{: .toc-header }

Graphically displays the distribution of the light and dark.


#### Histogram options

 * Right-click the histogram image for options

#### Fit


#### Median


#### Mean


#### Show Sorted Graph


### Preview
{: .toc-header }

Preview the effect on the image as you change the values.


## Glow
{: toc-header }

The Glow effect produces a bright area around specific colors. It can be used to make colored lights or objects like neon lights appear to glow. Select up to 10 colors to affect in the image.

In the illustration, a red color from the ruby is used with the gain set so that the color becomes close to white.

<img src="../Image/PostProcessing_GlowAsSparkle.png"/>


 *Glow as sparkle.* 
<img src="../Image/PostProcessing_GlowOn.png"/>


 *Glow off (left) and on (right).* 

## Glow Properties
{: .toc-header }


### On
{: .toc-header }

Turns glow for the corresponding color on.


### Color
{: .toc-header }

Specifies the glow color.

 * Click the color swatch to select a color from the [Select color](../General/select_color.html) dialog box.
 * Click the **Pick** button to select the color from the rendered image.

### Sensitivity
{: .toc-header }

Controls how much variation on the selected color is permitted when calculating glow on pixels close to that color.


### Glow Size
{: .toc-header }

The radius of the glow around the bright pixel.


### Gain
{: .toc-header }

Multiplier for the lightness of the glow. The default value of 1.0 should result in normal glow effects. Use higher values for extremely bright glow.


### Preview
{: .toc-header }

Preview the effect on the image as you change the values.


## Wires &amp; Text
{: toc-header }

Overlays curves, text, dimensions, isocurves, mesh edges, and point objects over the rendered image.

<img src="PostEffectWires-001.png"/>


 *With (left) and without Wires &amp; Text (right).* 

## Wires and Text Properties
{: .toc-header }


### Curves
{: .toc-header }

Displays curve objects.


### Dimensions and text
{: .toc-header }

Displays dimension and text objects.


### Isocurves
{: .toc-header }

Displays surface isoparametric curves.


### Mesh edges
{: .toc-header }

Displays mesh edges.


### Points
{: .toc-header }

Displays point objects.


### Preview
{: .toc-header }

Preview the effect on the image as you change the values.


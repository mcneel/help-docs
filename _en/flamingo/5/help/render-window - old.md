﻿---
---

<!-- TODO: This is a combination of the old information here and the Rhino render Windows.  These two still need to be combined. -->

# Render Window
The render window provides options for exposure adjustment and adding post-processing effects. The mainframe of the render windows is part of Rhino's rednering frameowrk.  For details on the rederwindow menus and icons see the [Render Windows topic](http://docs.mcneel.com/rhino/5/help/en-us/index.htm#information/renderwindowpostprocess.htm)

### Pulldown Menus
For details on the rederwindow menus and icons see the [Render Windows topic](http://docs.mcneel.com/rhino/5/help/en-us/index.htm#information/renderwindowpostprocess.htm)


### Toolbars


### Save with background alpha channel
{: #save-with-alpha-channel}
Saves image 32-bit PNG, TIF, and BMP including alpha channel background. The Alpha channel versions of the file formats are used for high-quality compositing. Backgrounds will appear black when the rendering is saved with Alpha channel.

### Export to native Flamingo nXt file (.nXtImage)
{: #export-to-nxtimage}
Saves uncompressed luminance and color information. Saves all rendered channels including [alpha](environment-tab.html#alpha). The nXtImage files can be opened in the [Image Editor](image-editor.html) where [exposure](#adjust-image) and [post-processing effects](#effects) can be applied and the image re-saved to another bitmap format.
The .nXtImage format is the native image format of the nXt renderers. It is the recommended format for storing your renderings, since it preserves the most information about your rendering. Images stored in this format can be manipulated in the [nXt Image Editor](image-editor.html) and special effects can be added. From this editor, you can save to many popular standard formats, including all of the formats supported in nXt. You can also save to [Piranesi EPix file (.epx)](http://www.piranesi.co.uk/) format.

### Export to HDR file
{: #export-to-hdr}
Saves uncompressed luminance and color information. The .hdr format stores luminance data directly in a High Dynamic Range format. Non-luminance backgrounds, such as normal photographs, will appear black when saved in one of these formats.

### Export to EXR file
{: #export-to-exr}
A&#160;high-dynamic-range image file format, released as an&#160;open standard&#160;along with a set of software tools created by&#160;Industrial Light and Magic (ILM), released under a&#160;free software license. This file format supports 16-bits-per-channel&#160;floating-point&#160;values (half precision) with a sign bit, five bits of exponent, and a ten-bit&#160;mantissa. This allows a dynamic range of over thirty&#160;stops&#160;of exposure. See: [Wikipedia article: OpenEXR](http://en.wikipedia.org/wiki/OpenEXR).
The .exr format stores luminance data directly in a High Dynamic Range format. Non-luminance backgrounds, such as normal photographs, will appear black when saved in one of these formats.

## Exit
Closes the render window.

##  [Flamingo Tab Render Window](render-window.html#help)

## Progress
{: #progress}

### Action

### Pass

### Scan line

### Elapsed time

### Rays / second

### Pixels / second

## Render Constraints
{: #number-of-passes}
{: #time}
{: #render-constraints}
{% include_relative snippets/snippet-renderconstraints.md %}
## Adjust Image
{: #adjust-image}
The settings that control the screen display also control any image file made from that display. Multiple image files with different exposure settings can be saved from a single rendering. The exposure settings for one rendered image will be applied to the next.
This adjustment process is called *tone mapping.* Tone mapping is the process of converting the luminance data used by Flamingo nXt into&#160;Red, Green, and Blue (RGB) pixels that can be displayed or printed.

### Brightness
{: #brightness}
Adjusts the overall brightness of the image. For example, if a white surface in the model is rendering gray, increase the brightness until the surface appears white. Or, if the exterior scene seems overexposed, decrease the brightness until the scene appears more correct.
![images/brightnessdefault.png](images/brightnessdefault.png)
*Brightness at default (left) and increased.*
{% include_relative snippets/snippet-brightness.md %}
### Burn
{: #burn}
Adjusts the image white point. This is the brightest white color in the image. Burn can add drama, life,&#160;and sharpness to a rendering by adding more areas of white to contrast with the dark areas.
See [Wikipedia article: White point](http://en.wikipedia.org/wiki/White_point).
![images/burn-001.png](images/burn-001.png)
*Burn at the default setting (left) and increased.*

### Saturation
{: #saturation}
Saturation controls the amount of color in the image. A saturation of 0.00 will result in a grayscale image. Values above 1.00 can make colors richer.
![images/saturationdefault.png](images/saturationdefault.png)
*Saturation at the default (left) and increased by about 3 (right).*

### Histogram
{: #histogram}
Graphically displays the distribution of the light and dark areas in the image.
See: [Wikipedia article: Histogram](http://en.wikipedia.org/wiki/Histogram). The internet has many articles about using histograms to evaluate exposure in digital photography. The principles are the same for rendering.
![images/histogram.png](images/histogram.png)
*Histogram.*

#### Histogram options

>Right-click the histogram image for options

#### Fit

#### Median

#### Mean

#### Show Sorted Graph

#### Show Scale

#### Graph Color

#### Show Luminance Values

### Lock exposure
{: #lock-exposure}
When the exposure settings are locked, changing the lighting will not adjust the exposure to compensate.

## Information
{: #information}

### Resolution
Displays the [render resolution](render-tab.html#resolution).

### Faces
Displays the number of mesh faces used to render the model.

### Apparent faces
When there are blocks in the model, Flamingo nXt is able to use the block definition to render block instances without remeshing each instance. The **Apparent faces** display shows how many additional temporary faces are generated.

## Pixel information
Window point
Image point
Image Y-Up
Pixel color
Luminance
Distance

## Lighting information

###  [Presets](lighting-tab.html)

###  [Sun](sun-and-sky-tabs.html#sun)

###  [Sky](sun-and-sky-tabs.html#sky)

###  [Lights](lights-tab.html)

###  [Indirect](lighting-advanced-tab.html#indirect)

###  [Ambient On/Off](lighting-advanced-tab.html#ambient)

## Channels
{: #channels}
Displays the status of the lighting channels.

## Effects
{: #post-process-effects}
{: #effects}
Post-processing effects are applied after the image is rendered. These can be turned on and off and re-ordered in the list. Each effect has its own settings.

## Effects Options
These options are also available from a context menu.

>Right-click an effect to display the context menu.

![images/toggleeffect.png](images/toggleeffect.png)Toggle the on/off state of the selected effect.
![images/moveup.png](images/moveup.png)Move the selected effect up in the list.
![images/movedown.png](images/movedown.png)Move the selected effect down in the list.
![images/effectproperties.png](images/effectproperties.png)Selected effect properties.
![images/savelistorderasdefault.png](images/savelistorderasdefault.png)Save the current effects list order and properties as default.
![images/savecurrenteffectslist.png](images/savecurrenteffectslist.png)Save the current effects list as named list.
![images/importnamedeffectslist.png](images/importnamedeffectslist.png)Import named effects list.

## Depth of Field
{: #postprocessingdof}
The Depth of Field effect blurs the image depending on the distance from the camera.
![images/postprocessing-dof.png](images/postprocessing-dof.png)

## Depth of Field Properties
{: #depth-of-field-properties}

### Visual Properties
{: #dofvisualproperties}

#### Blurring strength
{: #dofblurringstrength}
Determines the amount of blurring. This is an arbitrary value and different values will work better with different images.

#### Max blurring
{: #dofmaxblurring}
Determines the maximum blurring radius used. Since extremely blurred areas can cause the effect to be slow, this limits the effect.

### Area of Effect
{: #dofareaofeffect}

#### Focal distance
{: #dofocaldistance}
The distance from the camera at which the image is in focus (not blurry).

#### Pick
Pick a location on the image to set the focal distance.

#### Blur background
{: #dofblurbackground}
Determines whether the background is blurry. The background will be blurred at the maximum effect.

## Fog
{: #postprocessingfog}
The fog effect adds depth-dependent coloration in the image. This effect can be used to add a thick fog effect or a subtle depth cue.
![images/postprocessing-nofog.png](images/postprocessing-nofog.png)
*No post processing effects.*

### Fog as Gradient Background
Fog can be used to create a gradient background.
In this case the settings to create the background are as follows:
Strength = 1Noise = .1Fog Color = BlackEnd distance = approximately 110Start distance = approximately 90Fog Background = OnFeathering = 80
![images/postprocessing-fogasgradient.png](images/postprocessing-fogasgradient.png)
*Fog as gradient background.*

## Fog Properties
{: #fogsettings}

### Visual properties
{: #fogvisualproperties}
Determines the appearance of the fog effect.

#### Strength
{: #fogstrength}
Determines the maximum amount of fogginess. Setting Strength to 0.0 turns the effect off; setting Strength to 1.0 represents total fog. Values higher than 1.0 can be used but only make sense when used with the **Noise**.

#### Noise
{: #fognoise}
Adds a random variation to Fog **Strength**.

#### Color
{: #fogcolor}
Specifies the fog color.

>Click the color swatch to select a color from the [Select color](select-color.html) dialog box.
>Click the **Pick** button to select the color from the rendered image.

### Area of effect
Determines the area encompassed by the fog effect.

#### Start distance
{: #fogstartdistance}
Specifies the distance from the camera at which the fog begins to appear.

>Click the **Pick** button to pick the depth from the rendered image.

#### End distance
{: #fogenddistance}
Specifies the distance from the camera at which the maximum amount of fogginess is achieved.

>Click the **Pick** button to pick the depth from the rendered image.

### Bounds (Left, Right, Top, Bottom)
{: #fogbounds}
Specifies the area of the image affected by the fog. This can be used to create a low-lying mist effect.
Click the **Pick Area** button to pick bounding area from the rendered image.

### Fog

#### Fog background
Determines whether the background image is also made foggy. The background will be fogged at the maximum strength.

#### Feathering
{: #fogfeathering}
Determines the number of pixels outside the bounding area to “fade in” the fogginess.

### Preview
Preview the effect on the image as you change the values.

## Glare
{: #postprocessingglare}
Glare and Glow are very similar. Whereas Glow uses a selected color, Glare pushes the color to white. Glare makes extremely bright parts of the image appear to glare. It does this by making the area surrounding the bright area brighter. This very subtle effect is usually used for night scenes where it will make the lights seem much more realistic.
![images/postprocessing-noglare.png](images/postprocessing-noglare.png)
*Glare off (left) and on (right).*

## Glare Properties
{: #glaresettings}

### White point bound
{: #glarewhitepointbound}
Determines where in the tonal range the glare will begin. The value is represented on the histogram and can be adjusted graphically. Pixels lighter than the **White Point Bound** (in either luminance or the grey-scale value) will glare.

### Glare size
{: #glaresize}
The radius of the glare around the bright pixel.

### Gain
{: #glaregain}
Multiplier for the lightness of the glare. The default value of 1.0 should result in normal glare effects. Use higher values for extremely bright glare.

### Use photometric information
{: #glareusephotometric}
When using photometric information, the amount of glare is controlled by how &quot;whiter than white&quot; the pixel is. Otherwise, the effect uses the whitest pixels in the image.

### Histogram
{: #glarehistogram}
Graphically displays the distribution of the light and dark.

#### Histogram options

>Right-click the histogram image for options

#### Fit

#### Median

#### Mean

#### Show Sorted Graph

### Preview
Preview the effect on the image as you change the values.

## Glow
{: #postprocessingglow}
The Glow effect produces a bright area around specific colors. It can be used to make colored lights or objects like neon lights appear to glow. Select up to 10 colors to affect in the image.
In the illustration, a red color from the ruby is used with the gain set so that the color becomes close to white.
![images/postprocessing-glowassparkle.png](images/postprocessing-glowassparkle.png)
*Glow as sparkle.*
![images/postprocessing-glowon.png](images/postprocessing-glowon.png)
*Glow off (left) and on (right).*

## Glow Properties
{: #glowsettings}

### On
Turns glow for the corresponding color on.

### Color
{: #glowcolor}
Specifies the glow color.

>Click the color swatch to select a color from the [Select color](select-color.html) dialog box.
>Click the **Pick** button to select the color from the rendered image.

### Sensitivity
{: #glowsensitivity}
Controls how much variation on the selected color is permitted when calculating glow on pixels close to that color.

### Glow Size
{: #glowsize}
The radius of the glow around the bright pixel.

### Gain
{: #glowgain}
Multiplier for the lightness of the glow. The default value of 1.0 should result in normal glow effects. Use higher values for extremely bright glow.

### Preview
Preview the effect on the image as you change the values.

## Wires &amp; Text
{: #postprocessingwireframe}
Overlays curves, text, dimensions, isocurves, mesh edges, and point objects over the rendered image.
![images/posteffectwires-001.png](images/posteffectwires-001.png)
*With (left) and without Wires &amp; Text (right).*

## Wires and Text Properties

### Curves
Displays curve objects.

### Dimensions and text
Displays dimension and text objects.

### Isocurves
Displays surface isoparametric curves.

### Mesh edges
Displays mesh edges.

### Points
Displays point objects.

### Preview
Preview the effect on the image as you change the values.

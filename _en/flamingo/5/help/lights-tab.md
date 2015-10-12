---
---


# Lights
Artificial light sources use normal Rhino lights with added properties to control the light distribution. When using light sources, choose the type that most closely represents the real-world lamp being modeled.

## Note

>![images/directionallightbutton.png](images/directionallightbutton.png)Rhino **Directional Lights** are not supported. They do not appear in the list of lights and cannot carry Flamingo nXt properties.

### LinearLight
{: #linearlight}
{: #rhino-light-commands}
Distributes light in a cylindrical pattern that imitates a fluorescent tube.
![images/linearlight.png](images/linearlight.png)

### PointLight
{: #pointlight}
Distributes light equally in all directions.
![images/pointlight.png](images/pointlight.png)

### RectangularLight
{: #rectangularlight}
Provides an approximation of a recessed light with a diffuser or baffles.
![images/rectangular light.png](images/rectangular light.png)

### Spotlight
{: #spotlight}
Provides a beam angle and direction.
![images/spotlight.png](images/spotlight.png)

### Tag objects as lights
{: #tag-objects-as-lights}
Any renderable object (surface, solid, etc.) can be tagged as a light and given light properties.
Objects tagged as lights display a preview widget of how the light is pointed and were its location is.

##### To control the visibility of light widget

>On the **Flamingo nXt menu &gt; Lights &gt;** check **Show light widgets on tagged objects** or use the [FlamingoNXtDrawLightsForObjectsTaggedAsLights](flamingo-command-list.html#flamingonxtdrawlightsforobjectstaggedaslights) command

## Light Properties
{: #light-properties}
When Flamingo is the current rendering application in Rhino, additional properties can be set for lights. Lights have some but not all properties in common.
Some light properties are displayed on the Lights tab as a matrix: [On/Off](lights-tab.html#on), [Name](lights-tab.html#name), [Distribution](lights-tab.html#light-distribution), [Aim](lights-tab.html#aim-light), [Watts](lights-tab.html#watts), and [Channel](lights-tab.html#channel).

### Name
{: #name}
The name of the light object.

### On
{: #on}
Toggles the light on and off.

### Visible
{: #visible}
The light object itself will be visible in the rendered image.

### Light distribution *( [Tagged objects only](#tag-objects-as-lights) )* 
{: #light-distribution}
Specifies the light distribution pattern.

#### All Directions
Simulates a point light.

#### Diffuse
Simulates a rectangular light.

#### Spot
Simulates a spotlight.

### Aim light *( [Tagged objects only](#tag-objects-as-lights) )* 
{: #aim-light}
Drag the light target into position.

### Watts
{: #watts}
Specifies the electrical power usage.

### Beam angle *( [Spotlights only](lights-tab.html#spotlight) )* 
{: #beam-angle}
The degree of width that light emanates from a light source.

### Radius *( [Spotlights only](lights-tab.html#spotlight) )* 
{: #radius}
The size of the light. Smaller lights cast sharper shadows.

### Color
{: #color}
The color for the light.

#### Use material color *( [Tagged objects only](#tag-objects-as-lights) )* 
Uses the color of the material assigned to the light object for the light it produces.

### Channel
{: #channel}
Specifies one of eight channels for the light.
This controls the number of channels for multi-channel rendering.
This feature lets you adjust the lighting in your rendered image in real time, after the rendering has been produced. Each light source in the drawing, including the sun and sky, can be assigned to a channel. Once this image is rendered, each channel can be individually scaled either in the Render Window before saving or it can be saved to an .nXtImage file for later editing. Using this capability, you can produce day and night interiors with a single rendering.
Click to play video clip.
The following conditions are necessary to produce and manipulate a multi-channel image:

>All participating lights must be on.
>Each light source must be assigned a channel. By default, Sun and Sky are set to channel 0.
>The only saved format that preserves this channel information is the .nXtImage format. Lighting can be adjusted there and then the image saved to a bitmap format.

## Additional options
{: #additional-options}

> [id="a13" style="position: relative;">Right-click]() a light in the **Lights** tab for additional options

####  [On](lights-tab.html#on) 

#### Delete
Deletes the selected light.

#### Remove light tag
Removes the [tag](lights-tab.html#tag-objects-as-lights) that makes an object a light.

####  [Properties](lights-tab.html#light-properties) 

#### Select objects and matching items
Selects the light in the viewport.

## IES File
{: #iesfile}
IES (Illuminating Engineering Society) files are photometry files that define the distribution of light from a light source. Light fixture manufacturers often provide these files. By using the IES file to define your distribution, you can more accurately depict your light source. The geometry of the tagged light object has no relationship to the distribution of light. The definition of the light distribution comes from the photometry file alone.

## Notes:

>Flamingo nXt supports Type C goniometry files, which includes the majority of IES files. Type A, which are occasionally used by the automobile industry to define headlights, and Type B files, which are sometimes used to define floodlighting, are not supported.
>IES distributions include the effects of light fixture elements such as baffles, reflectors, and diffusers.
>IES distributions are often asymmetrical, so the process of aiming the source includes not just a target, but a rotation angle as well.

### Brightness from file
Use the intensity stored in the IES file. If this is not checked, the ** [Watts](lights-tab.html#watts) ** setting is used.


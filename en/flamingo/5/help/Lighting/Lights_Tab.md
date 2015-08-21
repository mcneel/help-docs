---
layout: toc-page
---


# <img src="../Image/PropertiesButton.png"/>Lights
{: toc-title }

Artificial light sources use normal Rhino lights with added properties to control the light distribution. When using light sources, choose the type that most closely represents the real-world lamp being modeled.


## Note
{: .toc-header }

 1. <img src="../image/directionallightButton.png"/>Rhino **Directional Lights** are not supported. They do not appear in the list of lights and cannot carry Flamingo nXt properties.

### <img src="LinearLight-01.png"/>LinearLight
{: .toc-header }

Distributes light in a cylindrical pattern that imitates a fluorescent tube.

<img src="LinearLight.png"/>


### <img src="PointLight-01.png"/>PointLight
{: .toc-header }

Distributes light equally in all directions.

<img src="PointLight.png"/>


### <img src="RectangularLight-01.png"/>RectangularLight
{: .toc-header }

Provides an approximation of a recessed light with a diffuser or baffles.

<img src="Rectangular Light.png"/>


### <img src="SpotLight-01.png"/>Spotlight
{: .toc-header }

Provides a beam angle and direction.

<img src="Spotlight.png"/>


### <img src="TagObjectsAsLights.png"/>Tag objects as lights
{: .toc-header }

Any renderable object (surface, solid, etc.) can be tagged as a light and given light properties.

Objects tagged as lights display a preview widget of how the light is pointed and were its location is.


#### To control the visibility of light widget

 * On the **Flamingo nXt menu &gt; Lights &gt;** check **Show light widgets on tagged objects** or use the [FlamingoNXtDrawLightsForObjectsTaggedAsLights](../General/flamingo_command_list.html#FlamingoNXtDrawLightsForObjectsTaggedAsLights) command

## Light Properties
{: .toc-header }

When Flamingo is the current rendering application in Rhino, additional properties can be set for lights. Lights have some but not all properties in common.

Some light properties are displayed on the Lights tab as a matrix: [On/Off](Lights_Tab.html#On), [Name](Lights_Tab.html#Name), [Distribution](Lights_Tab.html#Light_distribution), [Aim](Lights_Tab.html#Aim_light), [Watts](Lights_Tab.html#Watts), and [Channel](Lights_Tab.html#Channel).


### Name
{: .toc-header }

The name of the light object.


### On
{: .toc-header }

Toggles the light on and off.


### Visible
{: .toc-header }

The light object itself will be visible in the rendered image.


### Light distribution *( [Tagged objects only](#Tag_objects_as_lights) )* 
{: .toc-header }

Specifies the light distribution pattern.


#### All Directions

Simulates a point light.


#### Diffuse

Simulates a rectangular light.


#### Spot

Simulates a spotlight.


### Aim light *( [Tagged objects only](#Tag_objects_as_lights) )* 
{: .toc-header }

Drag the light target into position.


### Watts
{: .toc-header }

Specifies the electrical power usage.


### Beam angle *( [Spotlights only](Lights_Tab.html#Spotlight) )* 
{: .toc-header }

The degree of width that light emanates from a light source.


### Radius *( [Spotlights only](Lights_Tab.html#Spotlight) )* 
{: .toc-header }

The size of the light. Smaller lights cast sharper shadows.


### Color
{: .toc-header }

The color for the light.


#### Use material color *( [Tagged objects only](#Tag_objects_as_lights) )* 

Uses the color of the material assigned to the light object for the light it produces.


### Channel
{: .toc-header }

Specifies one of eight channels for the light.

This controls the number of channels for multi-channel rendering.

This feature lets you adjust the lighting in your rendered image in real time, after the rendering has been produced. Each light source in the drawing, including the sun and sky, can be assigned to a channel. Once this image is rendered, each channel can be individually scaled either in the Render Window before saving or it can be saved to an .nXtImage file for later editing. Using this capability, you can produce day and night interiors with a single rendering.

Click to play video clip.

The following conditions are necessary to produce and manipulate a multi-channel image:

 * All participating lights must be on.
 * Each light source must be assigned a channel. By default, Sun and Sky are set to channel 0.
 * The only saved format that preserves this channel information is the .nXtImage format. Lighting can be adjusted there and then the image saved to a bitmap format.

## Additional options
{: .toc-header }

 *  **/mouse_button_right.htm');" id="a13" style="position: relative;">Right-click** a light in the **Lights** tab for additional options

####  [On](Lights_Tab.html#On) 


#### Delete

Deletes the selected light.


#### Remove light tag

Removes the [tag](Lights_Tab.html#Tag_objects_as_lights) that makes an object a light.


####  [Properties](Lights_Tab.html#Light_Properties) 


#### Select objects and matching items

Selects the light in the viewport.


## IES File
{: .toc-header }

IES (Illuminating Engineering Society) files are photometry files that define the distribution of light from a light source. Light fixture manufacturers often provide these files. By using the IES file to define your distribution, you can more accurately depict your light source. The geometry of the tagged light object has no relationship to the distribution of light. The definition of the light distribution comes from the photometry file alone.


## Notes:
{: .toc-header }

 * Flamingo nXt supports Type C goniometry files, which includes the majority of IES files. Type A, which are occasionally used by the automobile industry to define headlights, and Type B files, which are sometimes used to define floodlighting, are not supported.
 * IES distributions include the effects of light fixture elements such as baffles, reflectors, and diffusers.
 * IES distributions are often asymmetrical, so the process of aiming the source includes not just a target, but a rotation angle as well.

### Brightness from file
{: .toc-header }

Use the intensity stored in the IES file. If this is not checked, the ** [Watts](Lights_Tab.html#Watts) ** setting is used.


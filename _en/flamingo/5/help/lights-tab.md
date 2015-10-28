---
---

# ![images/lights-tab.png](images/lights-tab.png){:height="75px" width="75px"} Lights
Artificial light sources use normal Rhino lights with added Flamingo properties to control the light distribution. When using light sources, choose the type that most closely represents the real-world lamp being modeled.


## Lights Tab
{: #light-tab}
The Lights tab will list all the artificial lights in the scene. This topic covers the Flamingo specific Lights tab.  There is also a [Rhino Lights Tab](http://docs.mcneel.com/rhino/5/help/en-us/index.htm#commands/lights.htm).  Flamingo and Rhino will keep the lights settings in sync between the two tabs.  The Flamingo Lights tab is a bit more flexible through additional [Light Properties](#light-properties)

#### Where can I find Flamingo Lighting control?
The Lights tab must be activated through the [Lighting Pre-set](lighting-tab.html#lighting-presets) or the [Custom Lighting settings](lighting-tab.html#sun).

 1. ![images/options.png](images/options.png)Toolbars >![images/flamingo-icon.png](images/flamingo-icon.png)Flamingo nXt Toolbar
 1. ![images/menuicon.png](images/menuicon.png)Menus > Flamingo nXt 5.0 Pulldown > Show Control Panel > Flamingo Tab > Lights

From the Lights tab lights can be inserted, turned off/on, changed the strength and channel of each light.

##### Flamingo supports these light types:

> [Tag objects as Lights](#tag-objects-as-lights)
> [Spotlight](#spotlight)
> [Point light](#pointlight)
> [Rectangular Light](#rectangularlight)
> [Linear Light](#linearlight)

**Note:** Rhino Directional Lights ![images/directionallightbutton.png](images/directionallightbutton.png) are not supported. They do not appear in the list of lights and cannot carry Flamingo nXt properties.

Some light properties are displayed on the Lights tab table for quick editing of common properties.

##### Properties contained in the table are:

 >[On/Off](#on)
 >[Name](#name)
 >[Distribution](#light-distribution)
 >[Aim](#aim-light)
 >[Watts](#watts)
 >[Channel](#channel)

Right-clicking on the lights tab table will open the [Additional Options](#additional-options) menu.

[Light Properties](#light-properties) can also be accessed by picking on the light and accessing the Light Properties icon ![images/spotlightbutton.png](images/spotlightbutton.png) on the [Object Properties Panel](http://docs.mcneel.com/rhino/5/help/en-us/commands/properties.htm)

## Light Types
{: #light-types}
Lights can be inserted from the Rhino toolbars or the Flamingo Lights Tab. Objects can be tagged as lights with Flamingo.

#### ![images/tagobjectsaslights.png](images/tagobjectsaslights.png) Tag objects as lights
{: #tag-objects-as-lights}
<!-- TODO: Add the distribution types on this page?-->
Any renderable object (surface, solid, etc.) can be tagged as a light source and given light properties. Additional properties such as distribution, direction and strength can be assigned. Objects tagged as lights may display a preview widget showing direction of the light and were its center is location.

![images/tag-object-as-light-r85.png](images/tag-object-as-light-r85.png)
*LED driving lights and headlights tagged as light sources*

#### ![images/spotlight-01.png](images/spotlight-01.png) Spotlight
{: #spotlight}
SpotLight is a conical light distribution with a specific direction.  The light properties include a [source radius](#radius), [beam angle](#beam-angle), falloff radius and direction. The larger the source radius, the softer the shadows will be from the light. By default there is a visible disk at the light location. For information on editing the location, direction, beam angle on the screen using grips can be found in the [Rhinoceros Spotlight](http://docs.mcneel.com/rhino/5/help/en-us/commands/spotlight.htm) help topic.

![images/spotlight.png](images/spotlight.png)
*A Spotlight pointed at the red box.*

#### ![images/pointlight-01.png](images/pointlight-01.png) PointLight
{: #pointlight}
Point lights are a small sphere that distributes light equally in all directions. Light properties for this light include [source radius](#radius). The larger the radius, the softer the shadows it will cast from the light. By default there is a visible light sphere at the light location when rendering. Note that unusual effects can happen if the pointlight is partially obscured by an object that intersects the light.

![images/pointlight.png](images/pointlight.png)
*A small pointlight close to the right wall.*

#### ![images/rectangularlight-01.png](images/rectangularlight-01.png) RectangularLight
{: #rectangularlight}
Provides an approximation of a recessed light with a diffuser or baffles. The light distributes light in a diffuse pattern based on the orientation of the rectangle. An direction arrow is drawn at the center point of the light. Directly in front of the rectangle is full strength.  Then the light falls off as the objects are at an angle to the rectangle. By default a white rectangle will be visible when rendering. A common mistake is to insert these rectangles at exactly the same height as a ceiling plane. For consistent results, make sure the lights are slightly below the ceiling. For information on editing the location, direction, beam angle on the screen using grips can be found in the [Rhinoceros Rectangular Light](http://docs.mcneel.com/rhino/5/help/en-us/commands/rectangularlight.htm) help topic.

![images/rectangular light.png](images/rectangular light.png)
*A rectangular light just below the ceiling*

#### ![images/linearlight-01.png](images/linearlight-01.png) LinearLight
{: #linearlight}
Distributes light in a cylindrical pattern that imitates a fluorescent tube. Light properties for this light include [source radius](#radius) and length. The larger the radius, the softer the shadows it will cast from the light. By default there is a visible light cylinder at the light location when rendering. Note that unusual effects can happen if the cylindrical light is partially obscured by an object that intersects the light. Use Rhino Control points to activate the grips on the light to edit on the screen.

![images/linearlight.png](images/linearlight.png)

## Light Properties
{: #light-properties}
When Flamingo is the current rendering application in Rhino, additional properties can be set for lights. Lights have some but not all properties in common.

#### Name
{: #name}
The name of the light object. This is an easy way to differentiate lights which are the same type in the model.

#### ![images/lightbulbon.png](images/lightbulbon.png) On/Off
{: #on}
Toggles the light on and off. In the Light table,  the lightbulb icon is yellow, the light is on. If the lightbulb icon is gray, the light will be off in the rendering. Double-click on the icon to toggle On/Off. In the properties dialog, there is a On/Off Checkbox.

#### Visible
{: #visible}
By default lights will show themselves as a bright light source in the rendering.  By unchecking the Viibile property, the light object itself will be invisible in the rendering.  Although, the light will project its light into the scene.

#### Light distribution *( [Tagged objects only](#tag-objects-as-lights) )*
{: #light-distribution}
When tagging an object as a light, us Distribution to specify the pattern the light projects into the scene. In the light panel, double-click on the distribution cell to get options drop-down. Distribution types include: [All Directions](#point), [Spot](#spot) and [Diffuse](#diffuse). Both Spot and Diffuse require a [direction](#aim-light) to be specified.

#### Aim light *( [Tagged objects only](#tag-objects-as-lights) )*
{: #aim-light}
For tagged light which have a distribution of Spot or Diffuse, a direction must be specified.  Double-click on the "Aim >>" option and follow the command line prompts.

#### Watts
{: #watts}
Specifies the electrical power of the light.  It is recommended to start with realistic values for the scene. In the light table, double-click on the cell to change the value.

#### Beam angle *( [Spotlights only](lights-tab.html#spotlight) )*
{: #beam-angle}
The angle in degrees controlling the width that light emanates from a light source. This also can be changed by using grips on the screen.  Details on grip editing can be found in the [Rhinoceros Spotlight](http://docs.mcneel.com/rhino/5/help/en-us/commands/spotlight.htm) help topic.

#### Radius
{: #radius}
The size of the visible light source. Smaller lights cast sharper shadows.

#### Color
{: #color}
The color for the light the source emanates.

#### Use material color *( [Tagged objects only](#tag-objects-as-lights) )*
Uses the color of the material assigned to the light object for the light it produces.

#### Channel
{: #channel}
Lights can be assigned to one of eight channels. This feature lets you adjust the lighting in your rendered image in real time, after the rendering has been produced. This is a very powerful feature when working to balance multiple light sources in a rendering. For more details see the [Rendering Channels](render-channel.htnl) topic.

#### IES File
{: #iesfile}
IES (Illuminating Engineering Society) files are photometry files that define the distribution of light from a light source. Light fixture manufacturers often provide these files. By using the IES file to define your distribution, you can more accurately depict your light source. The geometry of the tagged light object has no relationship to the distribution of light. The definition of the light distribution comes from the photometry file alone.

Notes:

* Flamingo nXt supports Type C goniometry files, which includes the majority of IES files. Type A, which are occasionally used by the automobile industry to define headlights, and Type B files, which are sometimes used to define floodlighting, are not supported.
* IES distributions include the effects of light fixture elements such as baffles, reflectors, and diffusers.
* IES distributions are often asymmetrical, so the process of aiming the source includes not just a target, but a rotation angle as well.

#### Brightness from file
Use the intensity stored in the IES file. If this is not checked, the  [Watts](lights-tab.html#watts)  setting is used.


## Additional Options Menu
{: #additional-options}
Additional options for lights can be accessed by right-clicking on the light in the Light table.

####  On
Toggles the light [ON/Off](#on)

#### Delete
Deletes the selected light.

#### Remove light tag
Removes the [tag](#tag-objects-as-lights) that makes an object a light.

#### Properties
Access the [Light Properties](#light-properties) for that light.

#### Select objects and matching items
Selects the light in the viewport.

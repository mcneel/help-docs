---
layout: toc-page
---


# <img src="../Image/Icon-spotlight.png"/>Lighting
{: .toc-title }

Lighting is the most important and most neglected consideration when creating images. It is not just a way to illuminate the model. Lighting sets the mood and is a key ingredient in determining the composition.

<img src="ChristopherSotoGutierrez.png"/>


 *Image by Christopher Soto Gutiérrez.* 
Use the following guidelines when lighting your model:

 * Provide accurate information whenever possible.
 * Avoid using unrealistic intensity levels for light sources.
 * Set the units correctly for your model. The lighting will not be correct unless the units are correct. For example, if your model is in millimeters, set the model units to millimeters.
 * Adjust the overall brightness of your rendering by using the [Brightness](..\Render\Render_Window.html#Brightness) control on the rendering display. Do not attempt to adjust the overall scene brightness by changing the intensity of all of the light sources; the automatic [exposure](../Render/Render_Window.html#Brightness) adjustment will defeat this.
Since Flamingo nXt simulates real-world lighting, it includes presets that correspond to real-world lighting situations. Lighting in Flamingo nXt uses four broad methods:

 *  [Studio lighting](Lighting_Tab.html#Studio_lighting) 
 *  [Exterior daylight](Lighting_Tab.html#Exterior_daylight) 
 *  [Interior daylight](Lighting_Tab.html#Interior_daylight) 
 *  [Artificial lighting](Lighting_Tab.html#Artificial_lighting) 
The lighting tabs that control the settings are visible depending on which preset you choose.

To improve lighting techniques, be aware of the light and how it affects various surfaces. Materials can mask some of the effects of shadows and reflections, so some rendering experts apply lighting to their models before applying materials. Try to see light objectively, the way a camera does.


### <img src="SaveSchemeIcon.png"/>Save lighting scheme
{: .toc-subheader }

Saves the current lighting scheme.


### <img src="OpenSchemeIcon.png"/>Open lighting scheme
{: .toc-subheader }

Opens a saved lighting scheme.


## Lighting Presets
{: .toc-header }

Flamingo nXt provides lighting presets that can help get you started lighting your model. There are many more lighting options available, but the presets are often sufficient for many different renderings.

Indirect lighting, the lighting reflected off surfaces, is on when one of the two interior presets are selected and off for studio and exterior. This type of lighting is a very significant component of an interior simulation. For exteriors and studio models the effects of indirect lighting is more subtle and is therefore turned off by default.

Choose the Preset scheme that most closely resembles your scene.


## <img src="StudioLightingIcon.png"/>Studio lighting
{: .toc-header }

<img src="StudioLighting-001.png"/>

This scheme mimics the lighting found in a photographer's studio. It is most useful for rendering small-to-medium-sized objects in isolation. A high-dynamic-range (HDR) image file provides the primary lighting. The light from the HDR image resembles the interior lighting levels of the studio. The HDR settings are on the [Sky tab](Lighting_Advanced_Tab.html#Sky). You can also add artificial lights to your scene using the Lights tab. The visible background in the Studio preset is black.

Studio lighting is optimized for tabletop setups for small design articles such as jewelry and product designs.

In the preset scheme, the sun is off and an HDR image sky provides something for shiny objects to reflect.

For greater control, use light sources to light the scene. When lighting a studio setup, dramatic lighting is important. Create dramatic ligshting by producing a lot of contrast. This means that dark areas are just as important as light areas. Dramatic lighting requires a number of light sources placed in a way to create very light and very dark areas.

Lighting techniques for photography are generally the same as lighting for rendering, so a good place to start learning is one of the many books on the subject of photographic lighting. For more information about setting up studio lighting, see: [Studio Lighting Basics](Studio_Lighting_Basics.html).


## <img src="ExteriorLightingIcon.png"/>Exterior daylight
{: .toc-header }

<img src="ExteriorLighting-001.png"/>

This scheme simulates daylight for architectural exteriors using a natural sun and sky.

Specify settings on the [Sun](Sun_and_Sky_Tabs.html#Sun) and [Sky](Sun_and_Sky_Tabs.html#Sky) tabs. Set [sun angles](Sun_and_Sky_Tabs.html#Set_azimuth_and_altitude) directly or use [geographical location](Sun_and_Sky_Tabs.html#Set_location_on_Earth), date, and time. The default visible background for this preset is the simulated sky.

Lighting a building exterior is the most straightforward lighting model. Most exterior lighting will need no more than the default [Sun](Sun_and_Sky_Tabs.html#Sun) light source.

When the [Sun](Sun_and_Sky_Tabs.html#Sun) is turned on, the scene must be designated as an [interior](Lighting_Advanced_Tab.html#Interior) or an [exterior](Lighting_Advanced_Tab.html#Exterior). This is because the contribution of the sky light, reflected light from the ground, and light reflected off other surfaces is much different when inside as opposed to outside. Using the correct [Interior/Exterior](Lighting_Advanced_Tab.html#Indirect) setting results in effective and realistic lighting.

Sometimes it is easy to determine if a scene is an interior or an exterior. If the viewpoint is outside a building, it is an exterior scene. If the viewpoint is inside a room, it is an interior. Some kinds of scenes are not so clear. This includes courtyards, gazebos, exploded views, and sections. If a courtyard is much wider than it is tall, thereby letting in a lot of skylight, try lighting it as an exterior scene. If it is taller than it is wide, try lighting the scene as an interior. In this case, one of the tricks is to add daylight portals at the top of the courtyard to help direct the skylight into the scene.

Lights can also simulate landscape lighting. Use spotlights to highlight architectural features and trees. This works well for night or twilight scenes. During the day, the sun normally will overpower any artificial lighting in an outdoor scene, just as it will in the real world.

Exploded views, sections, and axonometric drawings from above also pose a special challenge. The decision depends on the desired results. For an exterior scene with the quickest rendering, use the exterior rendering method. If this method is not producing an interesting enough image, try using an interior rendering. This may make the interior more interesting, but it takes more time to set up the lighting.


## <img src="InteriorDaylightIcon.png"/>Interior daylight
{: .toc-header }

<img src="InteriorDaylightNoPortals.png"/>

This scheme simulates an interior lit by natural light. It consists of two components: direct sunlight transmitted from the [Sun](Sun_and_Sky_Tabs.html#Sun) and indirect sunlight transmitted via the [Sky](Sun_and_Sky_Tabs.html#Sky), the ground, and other exterior objects.

The [Sun](Sun_and_Sky_Tabs.html#Sun) and [Sky](Sun_and_Sky_Tabs.html#Sky) settings are similar to the [Exterior](Lighting_Tab.html#Exterior_daylight) preset.

The direct sunlight component of day lighting involves a straightforward calculation -- normally simply specify the time, date, and location to ensure accuracy.


## Notes
{: .toc-header }

 * Use accurate values for your [lights](Lights_Tab.html), [sky settings](Sun_and_Sky_Tabs.html#Sky), and window glass materials if possible.
 * Because the sun and sky are much brighter than other lights, you may not see much effect from adding artificial lighting when the sun is on. This is normal. Avoid artificially boosting the power of your light sources.
 * You can set the [Sun](Sun_and_Sky_Tabs.html#Sun_intensity) or [Sky](Sun_and_Sky_Tabs.html#Sky_intensity) intensity to a lower value. Since these settings simulate a clear sky, reducing their intensity will simulate cloudy or darker day lighting conditions.
 * A [multi-channel](Lights_Tab.html#Channel) rendering may help you get the picture you want, while still preserving accurate data.

## <img src="ArtificialLightingIcon.png"/>Artificial lighting
{: .toc-header }

This scheme provides a simulation of an architectural interior at night, lit by lamps. Use the [Lights tab](Lights_Tab.html) or [Rhino light commands](Lights_Tab.html#Rhino_Light_commands) to insert and manage light objects in your model.

<img src="ArtificialLight-001.png"/>


## <img src="CustomLighting.png"/>Custom
{: .toc-header }

When the values on the [Advanced tab](Lighting_Advanced_Tab.html) change from the defaults for the presets, the scheme becomes a custom scheme.


## Lighting controls
{: .toc-header }


###  [Sky](Sun_and_Sky_Tabs.html#Sky) 
{: .toc-subheader }

The [Sky tab](Sun_and_Sky_Tabs.html#Sky) has one mode for HDR image sky (studio lighting) and one for daylight lighting modes.


###  [Sun](Sun_and_Sky_Tabs.html#Sun) 
{: .toc-subheader }

The [Sun tab](Sun_and_Sky_Tabs.html#Sun) contains the controls for altering the parameters of the automatic sky. The sun is a very bright directional light source infinitely far from the model. The controls for the sun specify its direction using spherical coordinates.


###  [Advanced](Lighting_Advanced_Tab.html) 
{: .toc-subheader }

The [Advanced tab](Lighting_Advanced_Tab.html) lets you override all of the preset scheme settings to create custom lighting conditions.


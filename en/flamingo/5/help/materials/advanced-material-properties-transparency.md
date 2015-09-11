---
layout: toc-page
---


# Advanced Material Properties: Transparency
{: .toc-title }

The Transparency settings control&#160;properties associated with light passing through a material.

<img src="transparentmaterials.png"/>


### Transparency
{: .toc-subheader }

Changes the material from opaque to transparent. Transparent materials increase rendering time.

<img src="transparency.png"/>


### Index of Refraction
{: .toc-subheader }

Determines how much refraction occurs when looking through the material at objects beyond.

<img src="transparencyior.png"/>

The following table shows some examples of index of refraction:


### Material
{: .toc-subheader }


### IOR
{: .toc-subheader }

Vacuum

1.0

Air

1.00029

Ice

1.309

Water

1.33

Glass

1.52 to 1.8

Emerald

1.57

Ruby/Sapphire

1.77

Diamond

2.417


### Translucency
{: .toc-subheader }

A measure of diffusion. High translucency produces a “sandblasted” effect, since more light is scattered randomly through the material.

<img src="transparencytl.png"/>


### Scattering
{: .toc-subheader }

Controls the probability of the light encountering a particle per unit length.

 **Note** : The&#160; [Path Tracer](../render/render-tab.html#path-tracer) &#160;is required for this effect.

Subsurface scattering permits light to penetrate the object's surface and scatter in any direction. Many translucent materials can be modeled using this effect. Certain surfaces, such as stone or skin can be realistically “softened” by allowing the light to penetrate a short distance.

The material must have some transparency in order for sub-surface scattering to take place. This is a volumetric effect. The objects with this material attached must be solid or “space enclosing” for this to work properly.

<img src="scattering.png"/>


### Attenuation
{: .toc-subheader }

Determines how much light is absorbed as it passes through the object— greater values produce a more cloudy appearance. Use **Attenuation** to model liquids. Clear liquids have low **Attenuation** ; murky liquids have higher **Attenuation** values.

<img src="attenuation.png"/>


### Dispersion
{: .toc-subheader }

Controls how much light is split into its component wavelengths.

<img src="dispersion.png"/>


### Saturation
{: .toc-subheader }

Determines the amount of dispersion.

<img src="saturation.png"/>


### Blurry Transparency
{: .toc-subheader }

When a material is partially transparent, a little noise is introduced into the transparency, to make the material look more natural.


#### Blurriness

Controls the amount of noise added.

<img src="blurrytransparency.png"/>


### Glow
{: .toc-subheader }

Creates the illusion of illumination.

<img src="glow.png"/>


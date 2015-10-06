---
---


# Advanced Material Properties: Transparency
The Transparency settings control&#160;properties associated with light passing through a material.
![images/transparentmaterials.png](images/transparentmaterials.png)

### Transparency
Changes the material from opaque to transparent. Transparent materials increase rendering time.
![images/transparency.png](images/transparency.png)

### Index of Refraction
Determines how much refraction occurs when looking through the material at objects beyond.
![images/transparencyior.png](images/transparencyior.png)
The following table shows some examples of index of refraction:

### Material

### IOR
Vacuum
1. Air
1. Ice
1. Water
1. Glass
1. Emerald
1. Ruby/Sapphire
1. Diamond
1. 
### Translucency
A measure of diffusion. High translucency produces a “sandblasted” effect, since more light is scattered randomly through the material.
![images/transparencytl.png](images/transparencytl.png)

### Scattering
Controls the probability of the light encountering a particle per unit length.
 **Note** : The&#160; [Path Tracer](render-tab.html#path-tracer) &#160;is required for this effect.
Subsurface scattering permits light to penetrate the object's surface and scatter in any direction. Many translucent materials can be modeled using this effect. Certain surfaces, such as stone or skin can be realistically “softened” by allowing the light to penetrate a short distance.
The material must have some transparency in order for sub-surface scattering to take place. This is a volumetric effect. The objects with this material attached must be solid or “space enclosing” for this to work properly.
![images/scattering.png](images/scattering.png)

### Attenuation
Determines how much light is absorbed as it passes through the object— greater values produce a more cloudy appearance. Use **Attenuation** to model liquids. Clear liquids have low **Attenuation** ; murky liquids have higher **Attenuation** values.
![images/attenuation.png](images/attenuation.png)

### Dispersion
Controls how much light is split into its component wavelengths.
![images/dispersion.png](images/dispersion.png)

### Saturation
Determines the amount of dispersion.
![images/saturation.png](images/saturation.png)

### Blurry Transparency
When a material is partially transparent, a little noise is introduced into the transparency, to make the material look more natural.

#### Blurriness
Controls the amount of noise added.
![images/blurrytransparency.png](images/blurrytransparency.png)

### Glow
Creates the illusion of illumination.
![images/glow.png](images/glow.png)


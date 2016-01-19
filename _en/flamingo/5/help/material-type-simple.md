---
title: Basic Material Properties
---
# ![images/paint.svg](images/paint.svg) {{page.title}}
Flamingo materials are defined by a series of property groups. These are a series of Simple Material Types of commonly used materials.  These materials present a very simple set of controls. This gives easy access to the properties you can change to make a material look different without the complexity of extra controls. For most simple materials, changing the color is all that is needed to get a different look.

#### Simple Material Types:

> ![images/newsolidcolormaterial.png](images/newsolidcolormaterial.png)[Solid Color](#solid-color)
> ![images/newplasticmaterial.png](images/newplasticmaterial.png)[Plastic](#plastic)
> ![images/newmetalmaterial.png](images/newmetalmaterial.png)[Metal](#metal)
> ![images/newglassmaterial.png](images/newglassmaterial.png)[Glass](#glass)
> ![images/newglossymaterial.png](images/newglossymaterial.png)[Glossy](#glossy)
> ![images/newclearfinishmaterial.png](images/newclearfinishmaterial.png)[ClearFinish](#clearfinish)
> ![images/newtexturedmaterial.png](images/newtexturedmaterial.png)[Flamingo Textured](#flamingo-textured)
> ![images/newtexturesetmaterial.png](images/newtexturesetmaterial.png)[Texture Set](#texture-set)

Any material can be converted to an advanced material.  Advanced materials present all the possible controls to edit a material in Flamingo nXt.  For the most extensive control of a material, use Advanced Materials or convert your existing material to an advanced material.

#### Advanced Materials are comprised of these property groups:

> [Name](material-type-advanced.html#name)
> [Material Procedure](material-type-advanced.html#procedures)
> [Advanced Material Properties](material-type-advanced.html#advanced-materials-properties)
> [Reflective Finish](material-type-advanced.html#reflective-finish-and-highlight)
> [Transparency Properties](material-type-advanced.html#transparency)
> [Procedural Textures](material-type-advanced.html#bump-patterns)
> [Bitmap Textures](material-type-advanced.html#textures)
> [Notes](material-type-advanced.html#notes)

Materials are saved and stored in the Rhino model. Unique materials can have the same name in different Rhino models.

## Solid Color
{: #solid-color}
Solid Color materials have only a [name](material-type-advanced.html#name) and a [color](material-type-advanced.html#color).

![images/solidcolors.png](images/3-solidcolor.png)

{% include_relative snippets/snippet-material-name.md %}
{% include_relative snippets/snippet-material-color-select.md %}
{% include_relative snippets/snippet-material-advanced-editor.md %}

## Plastic
{: #plastic}
Plastic materials are slightly reflective with a white [highlight](material-type-advanced.html#highlight-color).

![images/solidcolors.png](images/3-plastic.png)

{% include_relative snippets/snippet-material-name.md %}
{% include_relative snippets/snippet-material-color-select.md %}
{% include_relative snippets/snippet-material-advanced-editor.md %} Use the Advanced Editor to overwrite the presets of [Highlight color](material-type-advanced.html#highlight-color), [Intensity](material-type-advanced.html#intensity), [Fresnel](material-type-advanced.html#fresnel), and [Sharpness](material-type-advanced.html#sharpness).

## Metal
{: #metal}
Metal materials have a highlight whose color matches the [color](material-type-advanced.html#color). You can also control the [Sharpness](material-type-advanced.html#sharpness) of the reflection.

![images/solidcolors.png](images/3-metal.png)

{% include_relative snippets/snippet-material-name.md %}
{% include_relative snippets/snippet-material-color-select.md %}
#### Sharpness
Controls the sharpness vs blurriness of the reflection. See Advanced [Sharpness](material-type-advanced.html#sharpness) topic for more details.

{% include_relative snippets/snippet-material-advanced-editor.md %} Use the Advanced Editor to overwrite the pre-sets of [Highlight color](material-type-advanced.html#highlight-color), [Intensity](material-type-advanced.html#intensity), [Fresnel](material-type-advanced.html#fresnel) and [Type](material-type-advanced.html#type).

## Glass
{: #glass}
Glass materials have a [color](material-type-advanced.html#color) and an [Index of Refraction](advanced-material-properties-main.html#index-of-refraction) (IOR).

![images/solidcolors.png](images/3-glass.png)

{% include_relative snippets/snippet-material-name.md %}
{% include_relative snippets/snippet-material-color-select.md %}
#### Index of Refraction
Controls the amount light bends through the material. See Advanced [Index of Refraction](advanced-material-properties-main.html#index-of-refraction) topic for more details.

{% include_relative snippets/snippet-material-advanced-editor.md %} Use the Advanced Editor to overwrite the pre-sets of [Highlight color](material-type-advanced.html#highlight-color), [Intensity](material-type-advanced.html#intensity), [Fresnel](material-type-advanced.html#fresnel), [Sharpness](material-type-advanced.html#sharpness) and [Transparency](material-type-advanced.html#transparency).

## Glossy
{: #glossy}
Glossy materials generally have a low Highlight [Intensity](material-type-advanced.html#intensity) and [Sharpness](material-type-advanced.html#sharpness).

![images/solidcolors.png](images/3-glossy.png)

{% include_relative snippets/snippet-material-name.md %}
{% include_relative snippets/snippet-material-color-select.md %}
#### Intensity
Controls strength of the highlight from lights on the surface. See Advanced [Intensity](material-type-advanced.html#intensity) topic for more details.

#### Highlight Sharpness
Controls sharpness vs blurriness of the highlight spot from lights on the surface. See Advanced [Highlight sharpness](material-type-advanced.html#sharpness) topic for more details.

{% include_relative snippets/snippet-material-advanced-editor.md %} Use the Advanced Editor to overwrite the presets of [Fresnel](material-type-advanced.html#fresnel) and [Type](material-type-advanced.html#type).

## ClearFinish
{: #clearfinish}
The ClearFinish material simulates car paint, porcelain, ceramics, varnished woods, or any material with a plastic or clear-coat layer. ClearFinish uses the [Fresnel](material-type-advanced.html#fresnel) setting to change the material color based on angle to the view. These materials tend to be a deep color when looked at straight on, but as the surface curves away from the view, they become more and more reflective. Car paints with a clear-coat or clear lacquer finishes are good examples.

![images/solidcolors.png](images/3-clearfinish.png)

{% include_relative snippets/snippet-material-name.md %}
{% include_relative snippets/snippet-material-color-select.md %}
{% include_relative snippets/snippet-material-advanced-editor.md %} Use the Advanced Editor to overwrite the presets of [Highlight color](material-type-advanced.html#highlight-color), [Intensity](material-type-advanced.html#intensity), [Fresnel](material-type-advanced.html#fresnel) and [Sharpness](material-type-advanced.html#sharpness).

## Flamingo Textured
{: #flamingo-textured}
Textured materials use images to create colors and patterns. The image name, resolution, tile size, and highlight intensity and sharpness are controllable from this simple material.

![images/solidcolors.png](images/3-texture.png)

{% include_relative snippets/snippet-material-name.md %}
{% include_relative snippets/snippet-material-color-select.md %}
#### Intensity
Controls strength of the mirror-like reflection of the surface. See Advanced [Intensity](material-type-advanced.html#intensity) topic for more details.

#### Sharpness
Controls the sharpness vs blurriness of the reflection. See Advanced [Sharpness](material-type-advanced.html#sharpness) topic for more details.

#### Image
Set the image map and properties of the material. There are many options here. See the Advanced [Images](material-type-advanced.html#texture) topic for more details.

{% include_relative snippets/snippet-material-image-add-edit.md %}
{% include_relative snippets/snippet-material-advanced-editor.md %} Use the Advanced Editor to overwrite the presets on this material.

## Texture Set
{: #texture-set}
<!-- TODO: The following link doesn't work -->
[Texture set materials](material-type-texture-set.html) are a coordinated set of texture which defines a material.  These coordinated sets can the created through texture maps that contain information such as displacement, normal, or bump maps. Displacement maps give the material depth. Combining these texture maps as a set can create very realistic materials. The [PixPlant software](http://www.pixplant.com/) is a product that can take a standard bitmap and create these sets of textures.

![images/solidcolors.png](images/textureset.png)

{% include_relative snippets/snippet-material-name.md %}
#### Width and Height
Controls size of all the textures in the set.  Use this control to keep all the bitmaps sized and aligned together.

#### Intensity
Controls strength of the mirror-like reflection of the surface. See Advanced [Intensity](material-type-advanced.html#intensity) topic for more details.

#### Sharpness
Controls the sharpness vs blurriness of the reflection. See Advanced [Sharpness](material-type-advanced.html#sharpness) topic for more details.

#### Types
This controls the type of reflection on the surface.  See Advanced [Type](material-type-advanced.html#type) topic for more details.

### Texture maps
Within the Texture Map table will be listed the textures that are part of the texture set.  Right-click on the table to add, remove or change the textures in the set.

#### Add Maps...
Use this command in the right-click menu to add new textures to the list.  More then one texture can be added at one time. If the textures names include suffixes for one of the mapping types, then the map type will be automatically added.  For instance, if a map has *-normal* in the name it will automatically be tagged as a normal map type.

#### Remove Map
This right-click command will remove a texture map from the table.

#### Color
This right-click mapping type will contribute the the visible color of the texture. For more details see [Standard Mapping Type](material-image-properties.html#standard)

#### Bump
The bump map will use the greyscale of the texture to simulate a change in height or bump in the material. For more details see [Bump Map Advanced](material-image-properties.html#bump)

#### Normal
Normal maps are special bump maps that use the red, green and blue channel of the bitmap to adjust the bump direction at each pixels.  Because the blue channel is the the Z direction of the bump, the images tend to take on a blue hue. For more details see [Normal Map Advanced](material-image-properties.html#normal)

#### Specular
A Specular map will use the greyscaled colors in the material to control the amount of reflection in the image at that spot. For more details see [Transparency Map Advanced](material-image-properties.html#transparency)

#### Opacity
An opacity map will control the transparency of a material at each pixel based on the greyscale of the image. For more details see [Normal Map Advanced](material-image-properties.html#normal)

#### Displacement
A displacement map will actually displace the rendering mesh based on the greyscale color of the map. For more details see [Displacement Map Advanced](material-image-properties.html#displacement)

### Advanced Material
The [Flamingo Advanced](material-type-advanced) material contains a complete set of properties for a Flamingo Material.  If none of these simple materials work, use the [Flamingo Advanced](material-type-advanced) Material to create a material and have the greatest flexibility in creating materials.

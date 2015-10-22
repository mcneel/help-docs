---
---

# ![images/paint.svg](images/paint.svg){:height="75px" width="75px"} Material Properties
The Flamingo material is defined by a series of property groups. There are a series of Simple Material Types of commonly used materials.  These material present very a very simple set of controls. This give easy access to the properties you will usually want to change to make a material look different without the complexity of extra controls. For most simple materials, changing the color is all that is necessary to get a different look.

#### Simple Material Types:

> ![images/newsolidcolormaterial.png](images/newsolidcolormaterial.png)[Solid Color](#solid-color)
> ![images/newplasticmaterial.png](images/newplasticmaterial.png)[Plastic](#plastic)
> ![images/newmetalmaterial.png](images/newmetalmaterial.png)[Metal](#metal)
> ![images/newglassmaterial.png](images/newglassmaterial.png)[Glass](#glass)
> ![images/newglossymaterial.png](images/newglossymaterial.png)[Glossy](#glossy)
> ![images/newclearfinishmaterial.png](images/newclearfinishmaterial.png)[Clear Finish](#clear-finish)
> ![images/newtexturedmaterial.png](images/newtexturedmaterial.png)[Flamingo Textured](#flamingo-textured)
> ![images/newtexturesetmaterial.png](images/newtexturesetmaterial.png)[Texture Set](#texture-set)

Any material can be converted to an advanced material.  Advanced material present all the possible controls to edit a material in Flamingo NXT.  For the most extensive control of a material, use Advanced Materials or convert your existing material to an advanced material.

#### Advanced Materials are comprised of these property groups:

> [Name](material-type-advanced.html#name)
> [Procedural Material](material-type-advanced.html#name)
> [Advanced Material](material-type-advanced.html#name)
> [Transparency](material-type-advanced.html#name)
> [Textures](material-type-advanced.html#name)
> [Textures Summary](material-type-advanced.html#name)
> [Notes](material-type-advanced.html#name)

Materials are saved in the Rhino Model. A materials are stored in the Rhino model, unique materials can have the same name in different Rhino models.
<!-- TODO: All the links and anchors need to be tested on this page.  They were created before the Advanced page they reference.-->

## Solid Color
{: #solid-color}
Solid Color materials have only a [name](advanced-material-properties-main.html#name) and a [color](advanced-material-properties-main.html#color).

![images/solidcolors.png](images/3-solidcolor.png)

{% include_relative snippets/snippet-material-name.md %}
{% include_relative snippets/snippet-material-color-select.md %}
{% include_relative snippets/snippet-material-advanced-editor.md %}

## Plastic
{: #plastic}
Plastic materials are slightly reflective with a white [highlight](advanced-material-properties-main.html#highlight-color).

![images/solidcolors.png](images/3-plastic.png)

{% include_relative snippets/snippet-material-name.md %}
{% include_relative snippets/snippet-material-color-select.md %}
{% include_relative snippets/snippet-material-advanced-editor.md %} Use the Advanced Editor to overwrite the pre-sets of [Highlight color](advanced-material-properties-main.html#highlight-color), [Intensity](advanced-material-properties-main.html#intensity), [Fresnel](advanced-material-properties-main.html#fresnel), and [Sharpness](advanced-material-properties-main.html#sharpness).

## Metal
{: #metal}
Metal materials have a highlight whose color matches the [color](advanced-material-properties-main.html#color). You can also control the [Sharpness](advanced-material-properties-main.html#sharpness) of the reflection.

![images/solidcolors.png](images/3-metal.png)

{% include_relative snippets/snippet-material-name.md %}
{% include_relative snippets/snippet-material-color-select.md %}
#### Sharpness
Controls the sharpness vs blurriness of the reflection. See Advanced [Sharpness](advanced-material-properties-main.html#sharpness) topic for more details.

{% include_relative snippets/snippet-material-advanced-editor.md %} Use the Advanced Editor to overwrite the pre-sets of [Highlight color](advanced-material-properties-main.html#highlight-color), [Intensity](advanced-material-properties-main.html#intensity), [Fresnel](advanced-material-properties-main.html#fresnel) and [Type](advanced-material-properties-main.html#type)

## Glass
{: #glass}
Glass materials have a [color](advanced-material-properties-main.html#color) and an [Index of Refraction](advanced-material-properties-transparency.html#index-of-refraction) (IOR).

![images/solidcolors.png](images/3-glass.png)

{% include_relative snippets/snippet-material-name.md %}
{% include_relative snippets/snippet-material-color-select.md %}
#### Index of Refraction
Controls the amount light bends through the material. See Advanced [Index of Refraction](advanced-material-properties-transparency.html#index-of-refraction) topic for more details.

{% include_relative snippets/snippet-material-advanced-editor.md %} Use the Advanced Editor to overwrite the pre-sets of [Highlight color](advanced-material-properties-main.html#highlight-color), [Intensity](advanced-material-properties-main.html#intensity), [Fresnel](advanced-material-properties-main.html#fresnel), [Sharpness](advanced-material-properties-main.html#sharpness) and [Transparency](advanced-material-properties-transparency.html)

## Glossy
{: #glossy}
Glossy materials gernally have a low Highlight [Intensity](advanced-material-properties-main.html#intensity) and [Sharpness](advanced-material-properties-main.html#sharpness).

![images/solidcolors.png](images/3-glossy.png)

{% include_relative snippets/snippet-material-name.md %}
{% include_relative snippets/snippet-material-color-select.md %}
#### Intensity
Controls strength of the highlight from lights on the surface. See Advanced [Intensity](advanced-material-properties-main.html#intensity) topic for more details.

#### Highlight Sharpness
Controls sharpenss vs blurriness of the highlight spot from lights on the surface. See Advanced [Highlight sharpness](advanced-material-properties-main.html#sharpness) topic for more details.

{% include_relative snippets/snippet-material-advanced-editor.md %} Use the Advanced Editor to overwrite the pre-sets of [Fresnel](advanced-material-properties-main.html#fresnel) and [Type](advanced-material-properties-main.html#type)

## ClearFinish
{: #clearfinish}
The ClearFinish material simulates car paint, porcelain, ceramics, varnished woods, or any material with a plastic or clear-coat layer. ClearFinish uses the [Fresnel](advanced-material-properties-main.html#fresnel) setting to change the material color based on angle to the view. These materials tend to be a deep color when looked at straight on, but as the surface curves away from the view, they become more and more reflective. Car paints with a clear-coat or clear lacquer finishes are good examples.

![images/solidcolors.png](images/3-clearfinish.png)

{% include_relative snippets/snippet-material-name.md %}
{% include_relative snippets/snippet-material-color-select.md %}
{% include_relative snippets/snippet-material-advanced-editor.md %} Use the Advanced Editor to overwrite the pre-sets of[Highlight color](advanced-material-properties-main.html#highlight-color), [Intensity](advanced-material-properties-main.html#intensity), [Fresnel](advanced-material-properties-main.html#fresnel) and [Sharpness](advanced-material-properties-main.html#sharpness).

## Flamingo Textured
{: #textured}
Textured materials use images to create colored and patterns. The image name, resolution, tile size, and highlight intensity and sharpness are controllable from this simple material.

![images/solidcolors.png](images/3-texture.png)

{% include_relative snippets/snippet-material-name.md %}
{% include_relative snippets/snippet-material-color-select.md %}
#### Intensity
Controls strength of the mirror-like reflection of the surface. See Advanced [Intensity](advanced-material-properties-main.html#intensity) topic for more details.

#### Sharpness
Controls the sharpness vs blurriness of the reflection. See Advanced [Sharpness](advanced-material-properties-main.html#sharpness) topic for more details.

#### Texture
Set the texture map and properties of the material. There are many options here, see the Advanced [Texture](material-type-advanced.html#texture) topic for more details.

{% include_relative snippets/snippet-material-advanced-editor.md %} Use the Advanced Editor to overwrite the pre-sets on this material.

## Texture Set
{: #texture-set}
[Texture set materials](texture-set-materials.html) support third-party texture maps that contain information such as displacement, normal, or bump maps. Displacement maps cause the material to have depth. Combining these texture maps as a set can create very realistic materials. The [PixPlant software](http://www.pixplant.com/) is a product that can take a standard bitmap and create these set of textures.
<!-- TODO: This dialog at this time is all messed up.  Please check at a later date to see if it works better. There are the wrong controls in the panel-->
![images/solidcolors.png](images/textureset.png)

{% include_relative snippets/snippet-material-name.md %}
#### Width and Height
Controls size of all the textures in the set.  Use this control to keep all the bitmaps sized and aligned together.

#### Intensity
Controls strength of the mirror-like reflection of the surface. See Advanced [Intensity](advanced-material-properties-main.html#intensity) topic for more details.

#### Sharpness
Controls the sharpness vs blurriness of the reflection. See Advanced [Sharpness](advanced-material-properties-main.html#sharpness) topic for more details.

#### Types
This controls the type of reflection on the surface.  See Advanced [Type](material-type-advanced#type) topic for more details.

{% include_relative snippets/snippet-material-advanced-editor.md %} Use the Advanced Editor to overwrite the pre-sets on this material. Note: This is a complex material that uses many overlaid textures set with various defaults.  Using the using the advanced editor will not keep all the properties in sync.

## Advanced Material
The [Flamingo Advanced](material-type-advanced) material contains a complete set of properties for a Flamingo Material.  If none of these simple materials will work, use the [Flamingo Advanced](material-type-advanced) Material to create a material and have the greatest flexibility in creating materials.

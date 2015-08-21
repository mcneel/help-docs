---
layout: toc-page
---


# <img src="../Image/Icon-Materials.png"/>Advanced Material Properties: Textures
{: toc-title }

Two types of maps can be added to a material: image maps and bump patterns. Image mapping uses bitmap images to add detail to the material. Images can alter many attributes of the materials surface including its color and apparent three-dimensional surface quality (bump). Bumps add a random roughness or knurled quality to the surface.

<img src="Textures.png"/>

Image maps are two-dimensional patterns created using raster-based paint programs or by scanning photographs or other materials. Image maps can be used many ways. A common method is to use a picture of a real-world material as the materials color.


## Textures
{: .toc-header }

Buttons display previews of the specified image files.

 * Click a button with an image to edit its [texture properties](Texture_Properties_Main.html). Click a blank image button to apply a new image.
Textures can consist of more than one image. Sometimes one image controls the color and another controls the bump properties of the texture.


## Bump Patterns
{: .toc-header }

Bumps create the appearance of a specific kind of surface without using displacement maps or requiring additional maps. When one of the bump maps is checked, additional controls become available. Bumps use mathematical rules to provide the illusion of surface bumpiness in the material. More than one bump pattern can be added to a material.

Materials like stucco, concrete, and clay have a fine texture. It is probably not worth scanning a piece of the material to make a bitmap for it unless it will be viewed at close range. Using a **Sandpaper** procedural bump on a ** [Base Color](Advanced_Material_Properties_Main.htm#Color) ** emulates this kind of fine pattern. Create a ** [Base Color](Advanced_Material_Properties_Main.htm#Color) ** that is the color of the material. Then add a procedural bump to the material. Use **Sandpaper** for a fine texture and **Rubble** for a coarser texture.


### Sandpaper
{: .toc-header }

Provides a random, finely textured appearance.

<img src="Sandpaper.png"/>


### Rubble
{: .toc-header }

Gives the appearance of a lumpy, pitted surface. It can be scaled up and used for water, dirt, and smudges on surfaces. **Rubble** bump has a larger size range than **Sandpaper**.

<img src="Rubble.png"/>


### Pyramid
{: .toc-header }

Gives the appearance of small pyramidal protrusions like a knurl pattern.

<img src="Pyramid.png"/>


### Wrinkled
{: .toc-header }

Gives a wrinkled appearance.

<img src="Wrinkled.png"/>


### Marbled
{: .toc-header }

Gives a marbled appearance

<img src="Marbled.png"/>


## Scale
{: .toc-header }

Scale controls the proportional size of the bumps.


#### X/Y/Z

Specifies scale in each direction separately.

<img src="TextureScaleXY.png"/>


#### <img src="Lock.png"/>Lock

Maintains the aspect ratio.


## Properties
{: .toc-header }


#### Strength

Controls the appearance of depth.

<img src="TextureStrength.png"/>


#### Rotation

Sets the rotation angle for the pattern.

Changes to the orientation are normally apparent only if the procedural map has an obvious pattern or if the bump map has been scaled with different x, y and z components to produce a directional pattern.

<img src="TextureRotated.png"/>


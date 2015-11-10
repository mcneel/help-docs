---
---


# ![images/images.svg](images/images.svg){:height="75px" width="75px"} Material Image Properties

![images/3-texture.png](images/3-texture.png)
![images/textures.png](images/textures.png)
![images/solidcolors.png](images/textureset.png)

Materials can be created from images. Scan photographs and real materials like wallpaper and carpet, create patterns in a paint program, or use images from other bitmap sources.
재질이 모든 방향에서 무한대로 늘어난다고 상상해보십시오. 개체가 이를 통과하는 지점에서만 재질이 보이게 됩니다. 패턴은 지정된 비율로 네 방향에서 끝없이 반복 (타일) 됩니다.
작은 이미지는 타일처럼 사용하기 가장 좋습니다. 비트맵으로 타일 처리가 잘 되지 않으면 타일을 미러(거울) 실행하는 옵션을 사용합니다. 이 옵션은 가장자리 일치를 보장합니다.

**Note:** To make a bitmap image cover only part of the object (like a label on a wine bottle or a logo on a product), use the [Decal](properties-decal.html) feature instead.

이미지 맵은 다양한 방식으로 사용될 수 있습니다. 일반적인 방식은 실제 재질의 사진을 재질색으로 사용하는 것입니다.

## Name
Image Textures can be named.  This name is used by the Texture library of the RDK and has no real impact on Flamingo.

## Flamingo Image

### Image preview
{: #image-preview}
Displays a preview of the selected image file. Hold the mouse over the image to see a pop-up of the image file name.  Click on the image to select a different image.

#### Image resolution
{: #image-resolution}
Displays the resolution in pixels of the current image file.

### Tiles
{: #tiles}
재질 정의에 사용되는 이미지 맵은 항상 반복됩니다 (타일 처리). 이 설정은 각 인스턴스(타일)의 크기가 현재 모델 단위에서 얼마나 큰지를 지정합니다.

#### Width/Height
{: #width-height}
Sets the tile size in model units.
{% include_relative snippets/snippet-lock-widthheight.md %}

{% include_relative snippets/snippet-masking.md %}

### Mapping type
{: #mapping-type}
Images normally apply to the color channel. But there are other ways to use images.  Images can be set as:

> [Standard](#standard)
> [Normal](#normal)
> [Displacement](#displacement)

### Standard
{: standard}
The image provides color and visual bump to the material. Use the Strength and Bump values to control how the bitmap will influence the material.

#### Color Strength
{: #color}
Determines how much the image map influences the material appearance. In the example below, the underlying material is magenta colored. The color strength increases until the underlying color is completely masked by the black and white texture.

![images/brik-b14.png](images/brik-b14.png)![images/strength.png](images/strength.png)
*Color strength 0.2, 0.5, 1.0.*

#### Bump Strength
{: #bump}
Simulates bumps and wrinkles on the surface of an object by perturbing the surface normals of the object. The underlying object is not changed. In the illustration, the material on the left uses displacement mapping, while the material on the right uses bump mapping set at its highest value. Using negative bump numbers will reverse the effect. The edge and shadow are smooth for the bump-mapped material. See: [Wikipedia article: Bump mapping](http://en.wikipedia.org/wiki/Bump_mapping).

![images/bumpvsdisplacement.png](images/bumpvsdisplacement.png)
*Bump strength, 0.5 (left) and 1.0 (right).*

### Normal
{: #normal}
Fakes the lighting of bumps and dents without using more polygons to the render mesh. See: [Wikipedia article: Normal mapping](http://en.wikipedia.org/wiki/Normal_mapping).

Normal maps work very similar to bump maps, in that they modify the normal of the surface. The effect is essentially the same as bump, but normal maps allow more control over the normal than a bump. A bump map uses the grey average of the RGB in a bitmap. The RGB of a normal map corresponds to the modification of the XYZ of the normal. Because the blue channel of the image controls the Z-direction of the normal. Normal maps have a considerable blue color to them.

### Displacement
{: #displacement}
This image map displaces the surface render mesh based on the color values in the image. The effect is a change in the actual geometric position of the surface. The displacement is often along the local surface normal. See: [Wikipedia article: Displacement mapping](http://en.wikipedia.org/wiki/Displacement_mapping).

 **Note:** Use displacement mapping sparingly for small objects. Displacement increases rendering time considerably.

![images/displacement.png](images/displacement.png)

#### Height
{: #height}
변위의 가장 높은 지점의 높이.

![images/displacementheight.png](images/displacementheight.png)

#### Offset
{: #offset}
Sets the starting point of the displacement with reference to the surface normal. The displacement can take place completely outside, inside, or some ratio inside and outside the part.

![images/displacementz-001.png](images/displacementz-001.png)
*Z-offset = -1.0*

![images/displacementz-002.png](images/displacementz-002.png)
*Z-offset = -0.5*

![images/displacementz-003.png](images/displacementz-003.png)
*Z-offset = 0.0*

#### Facet size
{: #facet-size}
The size of the facets of the displacement mesh. This will increase the detail in the displacement, but also will increase rendering size and memory usage.

![images/facetsize.png](images/facetsize.png)

## Flamingo Image Advanced
{: #advanced}
Normally a Flamingo Image will apply to the main color channel of a material. The Flamingo Advanced dialog specifies other channels that the bitmap can effect.  These are used for very special effects.

####  Base color
This is the default setting.  An image will effect the [color](advanced-material-properties-main.html#color) of a material.

####  Specular color
This will effect the color of [reflection channel](advanced-material-properties-main.html#highlight-color) based on the image color at that point.

####  Specular intensity
This will change the [amount of reflection](advanced-material-properties-main.html#intensity) based on the grayscale of the image at that point.  This is used often in Texture Sets as a Specular Map.

####  Highlight sharpness
This will adjust the sharpness vs blurriness of the [highlight](advanced-material-properties-main.html#intensity) based on the grayscale value of the map at that point.

#### Highlight shape
{: #advanced-highlight-shape}
하이라이트 형태에 영향을 줍니다.

####  Transparency
This will effect the amount of [transparency](advanced-material-properties-main.html#intensity) in the material based on the grayscale of the image.

####  Translucency
This will effect the amount of [transparency](advanced-material-properties-transparency.html#translucency) in the material based on the grayscale of the image.

####  Attenuation
This will effect the amount of [attenuation](advanced-material-properties-transparency.html#attenuation) in the material based on the grayscale of the image.

#### Offsets X/Y
{: #advanced-x-y-offset}
재질과 X축, Y축과의 간격을 띄웁니다.

####  Rotation
This will rotate the image map.  Use to rotate the image 90 or 180 degrees if needed to reorient the image from its default rotation.

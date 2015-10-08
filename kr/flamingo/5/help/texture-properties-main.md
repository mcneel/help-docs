---
---


# Texture Properties: Main
![images/3-texture.png](images/3-texture.png)
이미지를 가지고 재질을 만들 수 있습니다. 사진과 실제 재질(벽지, 카펫 등)을 스캔하여 페인트 프로그램에서 패턴을 만들거나 다른 비트맵을 소스로 이미지를 사용합니다.
재질이 모든 방향에서 무한대로 늘어난다고 상상해보십시오. 개체가 이를 통과하는 지점에서만 재질이 보이게 됩니다. 패턴은 지정된 비율로 네 방향에서 끝없이 반복 (타일) 됩니다.
작은 이미지는 타일처럼 사용하기 가장 좋습니다. 비트맵으로 타일 처리가 잘 되지 않으면 타일을 미러(거울) 실행하는 옵션을 사용합니다. 이 옵션은 가장자리 일치를 보장합니다.
 **Note** : To make a bitmap image cover only part on the object (like a label on a wine bottle or a logo on a product), use the [Decal](properties-decal.html) feature instead.
이미지 맵은 다양한 방식으로 사용될 수 있습니다. 일반적인 방식은 실제 재질의 사진을 재질색으로 사용하는 것입니다.

### File name
{: #file-name}
The name of the image file.{: #clearbitmapcache}
{% include_relative snippets/snippet-clearbitmapcache.md %}
### Image preview
{: #image-preview}
선택된 이미지 파일의 미리보기를 표시합니다.

### Image resolution
{: #image-resolution}
이미지 파일의 해상도(픽셀 단위)를 표시합니다.

### Tiles
{: #tiles}
재질 정의에 사용되는 이미지 맵은 항상 반복됩니다 (타일 처리). 이 설정은 각 인스턴스(타일)의 크기가 현재 모델 단위에서 얼마나 큰지를 지정합니다.

#### Width/Height
{: #width-height}
타일 크기를 설정합니다.
{% include_relative snippets/snippet-lock-widthheight.md %}
#### Mirror tiles
{: #mirror-tiles}
Mirrors the map in both directions as it is tiled. This can sometimes produce adequate results using bitmaps that do not tile correctly by guaranteeing that the tile edges are continuous.{: #linking}
{% include_relative snippets/snippet-linking.md %}{: #masking}
{% include_relative snippets/snippet-masking.md %}
### Show masked colors
Graphically displays the effects of masking as the parameters change. Use the [ehlpsource="robohelp classic" class="hcp1" id="a169" style="position: relative;">color swatch]() provided to select the display color of the masked pixels. Changing this color or the setting of the checkbox does not change the masked color. This is simply a graphical tool for editing the mask.
![images/masking-008.png](images/masking-008.png)

## Mapping type
{: #mapping-type}

### Standard
이미지는 재질에 색과 시각적 범프를 제공합니다.

### Strength

#### Color
{: #color}
이미지 맵이 얼마나 재질 표현에 영향을 미치는지를 결정합니다. 다음의 예에서 아래에 있는 재질은 자홍색입니다. 아래에 있는 색이 완전히 검정색과 흰색 텍스처로 마스크 처리될 때까지 색의 세기가 증가합니다.
![images/brik-b14.png](images/brik-b14.png)![images/strength.png](images/strength.png) *Color strength 0.2, 0.5, 1.0.* 

#### Bump
{: #bump}
Simulates bumps and wrinkles on the surface of an object by perturbing the&#160;surface normals&#160;of the object. The underlying object is not changed.&#160;In the illustration, the material on the left uses displacement mapping, while the material on the right uses bump mapping set at its highest value. The edge and shadow are smooth for the bump-mapped material. See: [Wikipedia article: Bump mapping](http://en.wikipedia.org/wiki/Bump_mapping).
![images/bumpvsdisplacement.png](images/bumpvsdisplacement.png) *Bump strength, 0.5 (left) and 1.0 (right).* 

### Normal
{: #normal}
Fakes the lighting of bumps and dents without using more&#160;polygons to the render mesh. See: [Wikipedia article: Normal mapping](http://en.wikipedia.org/wiki/Normal_mapping).
법선 맵(Normal Map)은 범프 맵과 유사하지만, 법선 맵의 경우 서피스의 법선을 수정합니다. 효과는 범프와 기본적으로 동일합니다. 그러나 법선 맵은 범프보다 법선을 훨씬 제어하기 쉽습니다. 범프 맵은 비트맵에서 RGB의 회색 평균을 사용합니다. 법선 맵의 RGB는 법선의 XYZ 수정에 대응합니다.

### Displacement
{: #displacement}
Causes an effect where the actual geometric position of the surface isdisplaced, often along the&#160;local&#160;surface normal. See: [Wikipedia article: Displacement mapping](http://en.wikipedia.org/wiki/Displacement_mapping).
렌더링 메쉬에서 점을 이동시키기 위해 색상값을 사용하여 재질의 위치를 바꿉니다(변위:變位).
 **Note** : Use displacement mapping sparingly for small objects. Displacement increases rendering time considerably.
![images/displacement.png](images/displacement.png)

#### Height
{: #height}
변위의 가장 높은 지점의 높이.
![images/displacementheight.png](images/displacementheight.png)

#### Offset
{: #offset}
서피스 법선에 대하여 변위가 시작하는 지점을 설정합니다.
![images/displacementz-001.png](images/displacementz-001.png)
Z 간격띄우기 = -1.0
![images/displacementz-002.png](images/displacementz-002.png)
Z 간격띄우기 = -0.5
![images/displacementz-003.png](images/displacementz-003.png)
Z 간격띄우기 = 0.0

#### Facet size
{: #facet-size}
변위 메쉬의 패싯 크기.
![images/facetsize.png](images/facetsize.png)

## Advanced
{: #advanced}
비트맵의 영향을 받는 재질의 색 구성 요소를 선택합니다.

## Surface Component Altered by Map

###  [Base color](advanced-material-properties-main.html#color) 

###  [Specular color](advanced-material-properties-main.html#highlight-color) 

###  [Specular intensity](advanced-material-properties-main.html#intensity) 

###  [Highlight sharpness](advanced-material-properties-main.html#sharpness) 

### Highlight shape
{: #advanced-highlight-shape}
하이라이트 형태에 영향을 줍니다.

###  [Transparency](advanced-material-properties-transparency.html) 

###  [Translucency](advanced-material-properties-transparency.html#translucency) 

###  [감쇠](advanced-material-properties-transparency.html#attenuation) 

### Normal
{: #advanced-normal}
서피스 법선의 방향에 영향을 줍니다.

## Orientation
{: #advanced-orientation}

### X/Y Offset
{: #advanced-x-y-offset}
재질과 X축, Y축과의 간격을 띄웁니다.

###  [Rotation](advanced-material-properties-textures.html#rotation) 

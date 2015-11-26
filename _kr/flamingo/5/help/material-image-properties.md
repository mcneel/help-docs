---
title: 재질 이미지 속성
---


# ![images/images.svg](images/images.svg) {{page.title}}

![images/3-texture.png](images/3-texture.png)
![images/textures.png](images/textures.png)
![images/solidcolors.png](images/textureset.png)

이미지를 가지고 재질을 만들 수 있습니다. 사진과 실제 재질(벽지, 카펫 등)을 스캔하여 페인트 프로그램에서 패턴을 만들거나 다른 비트맵 소스로 이미지를 사용합니다.

재질이 모든 방향에서 무한대로 늘어난다고 상상해보십시오. 개체가 이를 통과하는 지점에서만 재질이 보이게 됩니다. 패턴은 지정된 비율로 네 방향에서 끝없이 반복 (타일) 됩니다.

작은 이미지는 타일처럼 사용하기 가장 좋습니다. 비트맵으로 타일 처리가 잘 되지 않으면 타일을 미러(거울) 실행하는 옵션을 사용합니다. 이 옵션은 가장자리 일치를 보장합니다.

**안내:** 비트맵 이미지가 개체의 일부에서만 보이게 하려면(와인병의 레이블 또는 제품 로고의 경우), 이 기능 대신 [데칼](properties-decal.html)을 사용하세요.

이미지 맵은 다양한 방식으로 사용될 수 있습니다. 일반적인 방식은 실제 재질의 사진을 재질색으로 사용하는 것입니다.

## 이름
이미지 텍스처는 이름을 지정할 수 있습니다. 이 이름은 RDK의 텍스처 라이브러리에서 사용되며, Flamingo 자체에 실제로 미치는 영향은 없습니다.

## Flamingo 이미지

### 이미지 미리보기
{: #image-preview}
선택된 이미지 파일의 미리보기를 표시합니다. 이미지 위에 마우스를 잠시 두면 이미지 파일 이름이 팝업으로 표시됩니다. 다른 이미지를 선택하려면 해당 이미지를 클릭합니다.

#### 이미지 해상도
{: #image-resolution}
현재 이미지 파일의 해상도(픽셀 단위)를 표시합니다.

### 타일
{: #tiles}
재질 정의에 사용되는 이미지 맵은 항상 반복됩니다 (타일 처리). 이 설정은 각 인스턴스(타일)의 크기가 현재 모델 단위에서 얼마나 큰지를 지정합니다.

#### 너비/높이
{: #width-height}
타일 크기를 모델 단위로 설정합니다.
{% include_relative snippets/snippet-lock-widthheight.md %}

{% include_relative snippets/snippet-masking.md %}

### 매핑 유형
{: #mapping-type}
색 채널에 적용되는 이미지입니다. 이미지를 사용하는 다른 방법도 있습니다. 이미지는 다음과 같이 설정할 수 있습니다:

> [표준](#standard)
> [법선](#normal)
> [변위](#displacement)

### 표준
{: standard}
The image provides color and visual bump to the material. Use the Strength and Bump values to control how the bitmap will influence the material.

#### 색 세기
{: #color}
이미지 맵이 얼마나 재질 표현에 영향을 미치는지를 결정합니다. 다음의 예에서 아래에 있는 재질은 자홍색입니다. 아래에 있는 색이 완전히 검정색과 흰색 텍스처로 마스크 처리될 때까지 색의 세기가 증가합니다.

![images/brik-b14.png](images/brik-b14.png)![images/strength.png](images/strength.png)
*색의 세기는 0.2, 0.5, 1.0 입니다.*

#### 범프 세기
{: #bump}
개체의 서피스 법선을 흔들어 개체 표면의 범프와 주름을 시뮬레이션합니다. 기본 개체는 바뀌지 않습니다. 그림에서 왼쪽의 재질은 변위 맵핑이 사용되였고, 오른쪽 재질은 가장 높은 값으로 설정된 범프 매핑이 사용되었습니다. 음의 범프 값을 사용하면 효과가 반전됩니다. 범프 맵핑된 재질에서 가장자리와 그림자는 부드럽게 처리됩니다. 참조: [Wikipedia 항목: Bump mapping](http://en.wikipedia.org/wiki/Bump_mapping).

![images/bumpvsdisplacement.png](images/bumpvsdisplacement.png)
*범프의 세기는 0.5 (왼쪽), 1.0 (오른쪽)입니다.*

### 법선
{: #normal}
렌더링 메쉬에 더 많은 다각형을 사용하지 않고도 범프와 움푹 들어간 부분의 음영을 가짜로 만들어냅니다. 참조: [Wikipedia 항목: Normal mapping](http://en.wikipedia.org/wiki/Normal_mapping).

Normal maps work very similar to bump maps, in that they modify the normal of the surface. The effect is essentially the same as bump, but normal maps allow more control over the normal than a bump. A bump map uses the grey average of the RGB in a bitmap. The RGB of a normal map corresponds to the modification of the XYZ of the normal. Because the blue channel of the image controls the Z-direction of the normal. Normal maps have a considerable blue color to them.

### 변위
{: #displacement}
This image map displaces the surface render mesh based on the color values in the image. The effect is a change in the actual geometric position of the surface. The displacement is often along the local surface normal. See: [Wikipedia article: Displacement mapping](http://en.wikipedia.org/wiki/Displacement_mapping).

 **Note:** Use displacement mapping sparingly for small objects. Displacement increases rendering time considerably.

![images/displacement.png](images/displacement.png)

#### 높이
{: #height}
변위의 가장 높은 지점의 높이.

![images/displacementheight.png](images/displacementheight.png)

#### 간격띄우기
{: #offset}
Sets the starting point of the displacement with reference to the surface normal. The displacement can take place completely outside, inside, or some ratio inside and outside the part.

![images/displacementz-001.png](images/displacementz-001.png)
*Z간격띄우기 = -1.0*

![images/displacementz-002.png](images/displacementz-002.png)
*Z간격띄우기 = -0.5*

![images/displacementz-003.png](images/displacementz-003.png)
*Z간격띄우기 = 0.0*

#### 패싯 크기
{: #facet-size}
The size of the facets of the displacement mesh. This will increase the detail in the displacement, but also will increase rendering size and memory usage.

![images/facetsize.png](images/facetsize.png)

## Flamingo 이미지 고급
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

####  투명도
This will effect the amount of [transparency](advanced-material-properties-main.html#intensity) in the material based on the grayscale of the image.

####  반투명도
This will effect the amount of [transparency](advanced-material-properties-transparency.html#translucency) in the material based on the grayscale of the image.

####  감쇠
This will effect the amount of [attenuation](advanced-material-properties-transparency.html#attenuation) in the material based on the grayscale of the image.

#### Offsets X/Y
{: #advanced-x-y-offset}
재질과 X축, Y축과의 간격을 띄웁니다.

####  회전
This will rotate the image map.  Use to rotate the image 90 or 180 degrees if needed to reorient the image from its default rotation.

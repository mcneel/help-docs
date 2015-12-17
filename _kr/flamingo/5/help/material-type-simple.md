---
title: 기본 재질 속성
---
# ![images/paint.svg](images/paint.svg) {{page.title}}
Flamingo 재질은 속성 그룹 시리즈로 정의됩니다. 자주 사용되는 재질로 구성된 간단한 재질 속성 시리즈가 있습니다. 이들 재질에는 아주 간단한 제어로 변경이 가능하며, 복잡하게 많은 설정을 변경할 필요 없이 간단한 제어만으로도 원하는 대로 설정을 변경하여 재질을 다르게 표현할 수 있습니다. 가장 간단한 재질의 경우, 재질의 색만 바꾸면 다르게 표현이 됩니다.

#### 간단한 재질 속성:

> ![images/newsolidcolormaterial.png](images/newsolidcolormaterial.png)[단색](#solid-color)
> ![images/newplasticmaterial.png](images/newplasticmaterial.png)[플라스틱](#plastic)
> ![images/newmetalmaterial.png](images/newmetalmaterial.png)[금속](#metal)
> ![images/newglassmaterial.png](images/newglassmaterial.png)[유리](#glass)
> ![images/newglossymaterial.png](images/newglossymaterial.png)[광택](#glossy)
> ![images/newclearfinishmaterial.png](images/newclearfinishmaterial.png)[클리어_피니시](#clearfinish)
> ![images/newtexturedmaterial.png](images/newtexturedmaterial.png)[Flamingo 텍스처](#flamingo-textured)
> ![images/newtexturesetmaterial.png](images/newtexturesetmaterial.png)[텍스처 세트](#texture-set)

어떤 재질도 고급 재질로 변환할 수 있습니다. 고급 재질에서는 Flamingo nXt 재질을 편집하는 모든 사용 가능한 제어가 표시됩니다. 재질을 최대한의 설정으로 제어하려면, 고급 재질을 사용하거나, 기존 재질을 고급 재질로 변환합니다.

#### 고급 재질은 다음 속성 그룹으로 구성되어 있습니다:

> [이름](material-type-advanced.html#name)
> [재질 절차](material-type-advanced.html#procedures)
> [고급 재질 속성](material-type-advanced.html#advanced-materials-properties)
> [반사 마무리](material-type-advanced.html#reflective-finish-and-highlight)
> [투명도 속성](material-type-advanced.html#transparency)
> [절차적 텍스처](material-type-advanced.html#bump-patterns)
> [비트맵 텍스처](material-type-advanced.html#textures)
> [노트](material-type-advanced.html#notes)

재질은 Rhino 모델에 저장되고 보관됩니다. Rhino 모델이 서로 다르더라도, 고유한 재질의 이름은 동일할 수 있습니다.

## 단색
{: #solid-color}
단색 재질에는 [이름](material-type-advanced.html#name)과 [색](material-type-advanced.html#color) 속성만 있습니다.

![images/solidcolors.png](images/3-solidcolor.png)

{% include_relative snippets/snippet-material-name.md %}
{% include_relative snippets/snippet-material-color-select.md %}
{% include_relative snippets/snippet-material-advanced-editor.md %}

## 플라스틱
{: #plastic}
플라스틱 재질은 흰색 [하이라이트](material-type-advanced.html#highlight-color)와 함께 적은 반사가 표시됩니다.

![images/solidcolors.png](images/3-plastic.png)

{% include_relative snippets/snippet-material-name.md %}
{% include_relative snippets/snippet-material-color-select.md %}
{% include_relative snippets/snippet-material-advanced-editor.md %} [하이라이트 색](material-type-advanced.html#highlight-color), [강도](material-type-advanced.html#intensity), [프레넬](material-type-advanced.html#fresnel), [선명도](material-type-advanced.html#sharpness)의 기본 설정을 덮어쓰려면 고급 편집기를 사용합니다.

## 금속
{: #metal}
금속 재질에는 [색](material-type-advanced.html#color)과 일치하는 하이라이트가 있습니다. 반사의 [선명도](material-type-advanced.html#sharpness)를 제어할 수 있습니다.

![images/solidcolors.png](images/3-metal.png)

{% include_relative snippets/snippet-material-name.md %}
{% include_relative snippets/snippet-material-color-select.md %}
#### 선명도
반사의 선명도와 흐린 정도를 제어합니다. 자세한 정보는 [선명도](material-type-advanced.html#sharpness) 항목을 참조하세요.

{% include_relative snippets/snippet-material-advanced-editor.md %} [하이라이트 색](material-type-advanced.html#highlight-color), [강도](material-type-advanced.html#intensity), [프레넬](material-type-advanced.html#fresnel), [유형](material-type-advanced.html#type)의 기본 설정을 덮어쓰려면 고급 편집기를 사용합니다.

## 유리
{: #glass}
유리 재질에는 [색](material-type-advanced.html#color), [굴절률](advanced-material-properties-main.html#index-of-refraction) (IOR) 이 있습니다.

![images/solidcolors.png](images/3-glass.png)

{% include_relative snippets/snippet-material-name.md %}
{% include_relative snippets/snippet-material-color-select.md %}
#### 굴절률(IOR)
재질을 통해 구부러지는 빛의 양을 제어합니다. 자세한 정보는 고급 [굴절률](advanced-material-properties-main.html#index-of-refraction) 항목을 참조하세요.

{% include_relative snippets/snippet-material-advanced-editor.md %} [하이라이트 색](material-type-advanced.html#highlight-color), [강도](material-type-advanced.html#intensity), [프레넬](material-type-advanced.html#fresnel), [선명도](material-type-advanced.html#sharpness), [투명도](material-type-advanced.html#transparency)의 기본 설정을 덮어쓰려면 고급 편집기를 사용합니다.

## 광택
{: #glossy}
광택 재질은 일반적으로 낮은 하이라이트 [강도](material-type-advanced.html#intensity)와 [선명도](material-type-advanced.html#sharpness)를 갖습니다.

![images/solidcolors.png](images/3-glossy.png)

{% include_relative snippets/snippet-material-name.md %}
{% include_relative snippets/snippet-material-color-select.md %}
#### 강도
표면에서, 빛으로 인한 하이라이트의 세기를 제어합니다. 자세한 정보는 [강도](material-type-advanced.html#intensity) 항목을 참조하세요.

#### 하이라이트 선명도
표면에서, 빛으로 인한 하이라이트 부분의 선명도와 흐린 정도를 제어합니다. 자세한 정보는 고급 [하이라이트 선명도](material-type-advanced.html#sharpness) 항목을 참조하세요.

{% include_relative snippets/snippet-material-advanced-editor.md %} [프레넬](material-type-advanced.html#fresnel)과 [유형](material-type-advanced.html#type) 기본 설정을 덮어쓰려면 고급 편집기를 사용합니다.

## 클리어_피니시
{: #clearfinish}
클리어_피니시 재질은 자동차 페인트, 자기, 도자기, 유광 처리된 목재, 그 밖에 플라스틱이 있거나 투명 코팅된 레이어가 있는 재질들을 시뮬레이션합니다. 클리어_피니시는 [프레넬](material-type-advanced.html#fresnel) 설정을 사용하여 뷰에 대한 각도를 기준으로 재질색을 변경합니다. 이러한 재질은 직접 보면 짙은 색으로 보이는 경향이 있지만, 뷰에서는 표면이 곡면을 이루므로 더욱 더 반사적이 됩니다. 투명 코팅된 자동차 페인트 또는 투명 락카 마무리가 그 좋은 예입니다.

![images/solidcolors.png](images/3-clearfinish.png)

{% include_relative snippets/snippet-material-name.md %}
{% include_relative snippets/snippet-material-color-select.md %}
{% include_relative snippets/snippet-material-advanced-editor.md %} [하이라이트 색](material-type-advanced.html#highlight-color), [강도](material-type-advanced.html#intensity), [프레넬](material-type-advanced.html#fresnel), [선명도](material-type-advanced.html#sharpness)의 기본 설정을 덮어쓰려면 고급 편집기를 사용합니다.

## Flamingo 텍스처
{: #flamingo-textured}
텍스처 재질은 이미지를 사용하여 색과 패턴을 만듭니다. 이미지 이름, 해상도, 타일 크기, 하이라이트 강도, 선명도는 간단한 재질 속성에서 제어 가능합니다.

![images/solidcolors.png](images/3-texture.png)

{% include_relative snippets/snippet-material-name.md %}
{% include_relative snippets/snippet-material-color-select.md %}
#### 강도
표면에서 거울과 같은 반사 세기를 제어합니다. 자세한 정보는 [강도](material-type-advanced.html#intensity) 항목을 참조하세요.

#### 선명도
반사의 선명도와 흐린 정도를 제어합니다. 자세한 정보는 [선명도](material-type-advanced.html#sharpness) 항목을 참조하세요.

#### 이미지
이미지 맵과 재질의 속성을 설정합니다. 여기에는 많은 옵션이 있습니다. 자세한 정보는 고급 [이미지](material-type-advanced.html#texture) 항목을 참조하세요.

{% include_relative snippets/snippet-material-image-add-edit.md %}
{% include_relative snippets/snippet-material-advanced-editor.md %} 이 재질의 기본 설정을 덮어쓰려면 고급 편집기를 사용합니다.

## 텍스처 세트
{: #texture-set}
[텍스처 세트 재질](texture-set-materials.html)은 변위, 법선, 범프 맵 정보가 있는 타사(third-party)의 텍스처 맵을 지원합니다. 변위 맵은 재질의 깊이를 더합니다. 이 텍스처 맵을 하나의 세트로 병합하면 매우 사실적인 재질을 만들 수 있습니다. [PixPlant 소프트웨어](http://www.pixplant.com/)는 일반적인 비트맵을 가지고 이러한 텍스처 세트를 만드는 제품입니다.
<!-- TODO: This dialog Needs a page.-->
![images/solidcolors.png](images/textureset.png)

{% include_relative snippets/snippet-material-name.md %}
#### 너비와 높이
세트에서 모든 텍스처의 크기를 제어합니다. 이 제어를 사용하여 모든 비트맵의 크기와 정렬을 함께 유지할 수 있습니다.

#### 강도
표면에서 거울과 같은 반사 세기를 제어합니다. 자세한 정보는 [강도](material-type-advanced.html#intensity) 항목을 참조하세요.

#### 선명도
반사의 선명도와 흐린 정도를 제어합니다. 자세한 정보는 [선명도](material-type-advanced.html#sharpness) 항목을 참조하세요.

#### 유형
표면에서의 반사 유형을 제어합니다. 자세한 정보는 [유형](material-type-advanced.html#type) 항목을 참조하세요.

{% include_relative snippets/snippet-material-advanced-editor.md %} 고급 편집기를 사용하여 이 재질의 기본 설정을 덮어 씁니다. **안내:** 많이 겹쳐진 텍스처 세트와 다양한 기본값을 사용하는 복잡한 재질입니다. 고급 편집기를 사용해도 모든 속성이 동기화되지는 않습니다.

## 고급 재질
[Flamingo 고급](material-type-advanced) 재질에는 Flamingo 재질의 완전한 속성 세트가 포함되어 있습니다. 간단한 재질만으로는 부족할 때 [Flamingo 고급](material-type-advanced) 재질을 사용하여, 보다 자유롭게 재질을 만들 수 있습니다.

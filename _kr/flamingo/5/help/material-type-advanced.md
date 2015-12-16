---
title: 고급 재질 속성
---

# ![images/paint.svg](images/paint.svg) {{page.title}}

![images/bunchofmaterials.png](images/bunchofmaterials.png)

Flamingo에는 [간단한 재질](material-type-simple.html)과 고급 재질 유형이 있습니다.  고급 재질에는 재질의 속성 그룹 시리즈 전체가 포함되어 있습니다. 재질을 최대한 활용하고 제어하려면 고급 재질 유형을 사용하세요.

고급 재질의 속성 그룹 전체 세트:

> [이름](#name)
> [재질 절차](#procedures)
> [고급 재질 속성](#advanced-materials-properties)
> [반사 마무리](#reflective-finish-and-highlight)
> [투명도 속성](#transparency)
> [절차적 텍스처](#bump-patterns)
> [비트맵 텍스처](#textures)
> [노트](#notes)

## 재질 이름
{: #name}
Rhino 모델의 재질 이름입니다. 재질은 Rhino 모델에 저장됩니다. 즉, 현재 모델에서 재질을 편집한다고 해도 다른 모델 또는 라이브러리의 이름이 같은 재질에 영향을 미치지 않음을 뜻합니다. 다른 모델의 재질을 사용하려면 해당 재질은 [라이브러리](libraries.html)로 먼저 내보내야 합니다. 내보낸 파일 이름으로는 해당 재질의 이름이 사용됩니다.

## 재질 절차
{: #procedures}
절차 트리는 재질들이 서로 상호 작용하는 방법을 정하는 규칙을 사용하여 하나 이상의 재질을 결합합니다. 트리에는 재질을 만드는 데 사용된 구성 요소가 표시되며, 직접 구성 요소를 추가할수도 있습니다. 표준 재질은 베이스 구성 요소만 목록에 표시됩니다.

각각의 절차는 두 개의 하위 재질을 특정한 방식을 사용하여 결합합니다. 두 하위 재질이 차례차례 절차가 되어 두 하위 재질 자체를 결합합니다. 이 방식을 사용하여 더욱 간단한 구성 요소를 가지고 매우 정교한 재질을 만들 수 있습니다. 재질을 결합하는 절차에는 [각도 블렌드](procedural-materials.html#angular-blend), [블렌드](procedural-materials.html#blend), [대리석](procedural-materials.html#marble), [화강암](procedural-materials.html#granite), [타일](procedural-materials.html#tile), [나무](procedural-materials.html#wood) 가 있습니다.

예를 들어, [대리석](procedural-materials.html#marble) 절차는 베이스 재질과 결 재질을 소용돌이 패턴으로 합칩니다.


##### 절차를 추가하려면
1. 베이스 절차 창에서 오른쪽 클릭합니다.
1. 메뉴에서 절차 유형을 클릭합니다.
  * [베이스](procedural-materials.html#base)
  * [각도 블렌드](procedural-materials.html#angular-blend)
  * [블렌드](procedural-materials.html#blend)
  * [화강암](procedural-materials.html#granite)
  * [대리석](procedural-materials.html#marble)
  * [타일](procedural-materials.html#tile)
  * [나무](procedural-materials.html#wood)

##### 절차를 제거하려면
 1. 절차 창에서 절차의 이름을 오른쪽 클릭합니다.
 2. 메뉴에서 제거를 클릭합니다.

## 고급 재질 속성
{: #advanced-materials-properties}

{% include_relative snippets/snippet-material-color-select.md %}

#### 반사 마무리와 하이라이트
{: #reflective-finish-and-highlight}
이 설정은 재질과 개체가 빛을 반사하는 방식에 변화를 줍니다. 하이라이트 효과는 일반적으로 빛이 광택 재질에 닿아 빛나는 부분과 관계가 있습니다. 반사 효과는 일반적으로 장면의 나머지 개체를 반사하는 거울과 같은 반사로 정의됩니다. 반사되어 보이는 개체가 없다면 크롬과 기타 반사 재질로 흥미로운 이미지를 만들 수 없다는 점을 기억해야 합니다. 반사 재질로 작업할 때에는 반사 재질에서 반사될 흥미로운 환경과 개체를 염두에 두시기 바랍니다.
 안내: 이 설정이 활성화되려면 강도값이 0보다 커야 합니다.

#### 하이라이트 색
{: #highlight-color}
하이라이트 색은 재질에서 반사에 더해지는 색입니다. 흰색, 금속, 사용자 지정과 같은 세 가지 제어가 있습니다.

#### 흰색
하이라이트가 흰색인 재질은 반사에 다른 색을 추가하지 않습니다. 흰색 하이라이트를 가진 재질이 주로 사용되며, 일반적인 그림, 플라스틱, 거울 마무리와 같은 효과를 나타냅니다.

![images/3-plastic.png](images/3-plastic.png)

#### 금속
{: #metallic}
베이스 색에 일치하는 하이라이트 색을 설정합니다. 많은 금속 마무리에서 일반적으로 베이스 색을 반사 색으로 사용합니다. 이 금속 옵션은 재질의 베이스 색을 반사 색으로 사용합니다.

![images/highlightcolormetallic.png](images/highlightcolormetallic.png)

#### 사용자 지정
일부 특수한 마무리의 경우, 개체의 반사는 재질의 베이스 색과 다른 색일 수 있습니다. 여러 개의 재질로 만들어진 재질이 일반적으로 여기에 속합니다. 사용자 지정을 사용하여 하이라이트 색을 지정합니다. [색 선택](select-color.html) ![images/colorswatch-001.png](images/colorswatch-001.png)을 사용하여 반사 색을 선택합니다.

![images/highlightcolorcustom.png](images/highlightcolorcustom.png)

#### 강도
{: #intensity}
하이라이트의 세기를 조정합니다. 값이 낮을수록 주변 개체가 아닌, 빛을 반사하는 광택 있는 개체로 표현됩니다. 큰 값은 하이라이트와 반사의 크기와 세기를 증가시킵니다. 가장 높은 값을 사용하면 재질이 거울처럼 표현되므로 장면의 다른 개체와 환경이 반사됩니다.

![images/highlightintensity.png](images/highlightintensity.png)

#### 프레넬
{: #fresnel}
프레넬(Fresnel)은 전도체의 [프레넬 반사, Fresnel reflection of conductors](http://en.wikipedia.org/wiki/Fresnel_equations)로 알려진 현상인, 불투명한 재질의 반사를 제어합니다. 프레넬 설정은 특정한 화각(畵角)에서 무광 속성이 고정된 상태로, 조사각(照射角)에서는 많은 재질이 더욱 더 정반사 (거울 반사) 경향을 보이게 합니다.

지나친 반사를 방지하려면 아주 어두운 재질의 값을 줄입니다. 프레넬 반사가 더욱 확연한, 광택제가 칠해진 나무 재질 등의 값은 올립니다.

![images/highlightfresnel.png](images/highlightfresnel.png)

#### 선명도
{: #sharpness}
하이라이트의 크기를 설정합니다. 낮은 숫자를 사용하면 하이라이트가 넓게 표현되며, 높은 숫자를 사용할수록 하이라이트의 초점이 더 작게 표시됩니다. 더 높은 강도의 반사에 적용되면, 반사가 흐리게 (초점에서 벗어나게) 또는 아주 선명하게 (초점이 맞춰져) 보입니다.

![images/highlightsharpness.png](images/highlightsharpness.png)

#### 유형
{: #type}
인공 광원이 반사될 때의 반사가 계산되는 방식을 변경합니다. 반사는 2가지 방식 즉, *레이캐스팅(ray casting)*과 *하이라이트*로 계산됩니다. 이 두 가지 방식은 결국 동일한 결과를 만듭니다. 그러나, 특정한 경우에 한 가지 방식이 다른 하나보다 더 좋은 결과를 더 빠르게 만들어내는 것을 알게 될 것입니다. 예를 들어, 광원 반사로 인해 재질이 잘 보이지 않아 개체를 잘 표현할 수 없을 수도 있습니다.

아래 그림에서 균형 유형의 경우, 왼쪽 개체의 반사가 밝고 하얗기 때문에 재질이 잘 표현되지 않았습니다.

때때로, 광원이 작은 실내 렌더링의 일부 경우에 서피스에 마치 점과 같은 아티팩트가 있을 수 있습니다. 아티팩트가 보이는 서피스는 특히 흐리게 반사됩니다. 유형을 [광택](advanced-material-properties-main.html#glossy), [광원 반사 없음](advanced-material-properties-main.html#no-light-source-reflection), 또는 [몬테카를로](advanced-material-properties-main.html#monte-carlo) 반사로 변경하면 이 문제를 완화시키는 데 도움이 됩니다.

#### 균형
{: #balanced}
자동으로 선명도 설정에 맞춰 레이캐스팅과 하이라이트의 균형을 유지합니다. 광원의 실제 반사와 인공적인 하이라이트가 모두 계산됩니다.

![images/highlightbalanced.png](images/highlightbalanced.png)

#### 광택
{: #glossy}
하이라이트의 흐린 정도를 증가시키고 레이캐스팅을 방지합니다. 개체 또는 빛의 반사가 계산되지 않으므로 따라서 성능이 향상되고 매우 흐리게 반사되는 재질의 아티팩트도 방지됩니다. 은은한 반사는 일부 손실될 수 있습니다.

![images/highlightglossy.png](images/highlightglossy.png)

#### 몬테카를로
{: #monte-carlo}
오직 레이캐스팅만이 광원 반사 계산에 사용됩니다. 레이캐스팅 초기에는 매우 노이즈가 많으며 점차 올바르게 수렴됩니다. 하이라이트가 흐리지 않을 때 가장 유용합니다.

![images/highlightmontecarlo.png](images/highlightmontecarlo.png)

#### 하이라이트 없음
{: #no-highlight}
오직 레이캐스팅만이 광원 반사 계산에 사용됩니다. 광원이 크고 재질이 흐리지 않아 하이라이트 계산에 시간이 오래 걸릴 수 있을 때 유용한 방식입니다. 광원 반사는 점차적으로 수렴됩니다.

![images/highlightnohighlight.png](images/highlightnohighlight.png)

#### 광원 반사 또는 하이라이트 없음
{: #no-light-source-reflection-and-no-highlight}
인공 광원의 모든 반사와 인공 하이라이트 효과가 제외됩니다. 개체 반사는 여전히 계산됩니다.

![images/highlightnohighlightreflection.png](images/highlightnohighlightreflection.png)

#### 광원 반사 없음
{: #no-light-source-reflection}
광원의 레이캐스트 반사가 제외되고, 하이라이트만 사용됩니다. 재질이 흐리고, 장면에 작고 밝은 광원이 있을 경우, 스펙클 아티팩트를 방지하는 데 종종 유용하게 사용됩니다.

![images/highlightnoreflection.png](images/highlightnoreflection.png)

## 투명도
{: #transparency}
투명도 설정은 재질을 투과하는 빛의 속성과 연관된 속성을 제어합니다.

![images/transparentmaterials.png](images/transparentmaterials.png)

#### 투명도 강도
불투명한 재질을 투명한 재질로 변경합니다. 투명한 재질은 렌더링 시간을 증가시킵니다.

![images/transparency.png](images/transparency.png)

#### 굴절률(IOR)
{: #index-of-refraction}
재질을 통해 그 너머에 있는 개체를 볼 때 굴절이 얼마나 발생하는지를 결정합니다.

![images/transparencyior.png](images/transparencyior.png)

다음 표는 굴절률의 일부 예를 나타냅니다.

 | 재질      |     | IOR         |
 |:--------------|:---:|:------------|
 | 진공        |     | 1.0         |
 | 공기           |     | 1.0029      |
 | 얼음           |     | 1.309       |
 | 물         |     | 1.33        |
 | 유리         |     | 1.52 to 1.8 |
 | 에메랄드       |     | 1.57        |
 | 루비/사파이어 |     | 1.77        |
 | 다이아몬드       |     | 2.417       |
{: .grided-table}

#### 반투명도
{: #translucency}
확산의 정도입니다. 높은 반투명도는 더 많은 빛이 재질을 통과하면서 불규칙하게 산란되므로, “샌드블라스트(sandblasted)” 효과를 만들어냅니다. 이는 매우 민감한 효과입니다. 세밀하게 조정해도 결과에 크게 차이를 만들 수 있습니다.

![images/transparencytl.png](images/transparencytl.png)

#### 산란
{: #scattering}
단위 길이당 입자와 빛이 만나는 확률을 제어합니다. 이 효과에는 [경로 추적기](render-tab.html#path-tracer)가 필요합니다.

표면하 확산(Subsurface scattering)은 빛이 개체의 표면을 관통하고 어떤 방향으로든 확산되는 것을 가능하게 합니다. 많은 반투명 재질들은 이 효과를 사용하여 모델링될 수 있습니다. 빛이 짧은 거리를 통과하도록 설정하면, 돌이나 피부같은 특정한 표면을 현실성 있게 “부드럽게 처리”할 수 있습니다.

재질이 어느 정도 반투명해야 표면하 확산이 발생할 수 있습니다. 이것은 체적을 나타내는 효과(volumetric effect)입니다. 이 효과가 올바르게 실행되려면 이 재질이 적용되는 개체가 솔리드 또는 "폐쇄된 공간"이어야 합니다.

![images/scattering.png](images/scattering.png)

#### 감쇠
{: #attenuation}
빛이 개체를 통과하면서 얼마나 빛이 흡수되는지를 결정합니다. 값이 클수록 더욱 탁하게 표현됩니다. 액체를 모델링할 때 감쇠를 사용하세요. 맑은 액체는 감쇠가 낮고, 탁한 액체는 감쇠 값이 더 높습니다.

![images/attenuation.png](images/attenuation.png)

#### 굴절 분산
{: #dispersion}
빛이 얼마나 많이 구성 요소 파장으로 분할되는지를 제어합니다.

![images/dispersion.png](images/dispersion.png)

#### 채도
{: #saturation}
굴절 분산의 양을 결정합니다.

![images/saturation.png](images/saturation.png)

#### 흐린 투명도
{: #blurry-transparency}
재질이 부분적으로 투명할 때 재질이 더욱 자연스럽게 보이도록 적은 양의 노이즈가 투명도에 더해집니다.

#### 흐린 정도
노이즈가 추가되는 정도를 제어합니다.

![images/blurrytransparency.png](images/blurrytransparency.png)

#### 글로우
{: #glow}
마치 빛이 비추고 있는 것과 같은 착각을 불러일으킵니다.

![images/glow.png](images/glow.png)

## 텍스처
{: #textures}
이미지 텍스처와 범프 패턴, 이렇게 두 가지 유형의 텍스처를 재질에 추가할 수 있습니다. 이미지 텍스처는 비트맵, 사진, 스캔 이미지 등을 기준으로 합니다. 범프 패턴은, Flamingo가 생성하는 불특정한 또는 반복되는 패턴입니다.

![images/textures.png](images/textures.png)

### 이미지
{: #images}
최대 4개의 비트맵 이미지를 사용하여 재질에 디테일을 추가할 수 있습니다. 이미지 맵은 서피스 색, 입체처럼 표현하는 서피스을 나타내는 데 사용할 수 있습니다. 이미지 맵은 래스터 기반 페인트 프로그램이나 스캔한 사진, 또는 다른 재질을 가지고 만든 2차원 패턴입니다. 이미지 맵은 다양한 방식으로 사용할 수 있습니다. 실제 재질의 사진을 재질 색으로 사용하는 것이 일반적인 방식입니다. 이미지 맵은 최대 4개의 이미지로 구성이 가능합니다. 경우에 따라, 한 이미지는 색을 제어하고 다른 이미지로는 텍스처의 범프 속성을 제어합니다. 이미지가 재질에 영향을 주는 방식을 제어하려면 [이미지 속성](material-image-properties.html) 대화상자로 갑니다.

![images/solidcolors.png](images/3-texture.png)

{% include_relative snippets/snippet-material-image-add-edit.md %}

### 범프 패턴
{: #bump-patterns}
범프 패턴은 변위 맵이나 다른 맵을 사용하지 않아도 표면의 질감을 특정하게 표현합니다. 범프는 수학적인 규칙을 사용하여 마치 표면이 울퉁불퉁한 것처럼 보이게 재질을 표현합니다. 다음과 같은 패턴이 포함됩니다: 

> [사포](#sandpaper)
> [자갈](#rubble)
> [각뿔](#pyramid)
> [주름](#wrinkled)
> [대리석](#marbled)

치장 벽토, 콘크리트, 점토의 텍스처는 아주 곱습니다. 가까운 범위에서 보이는 것이 아니라면 굳이 재질을 스캔하여 비트맵을 만들 필요는 아마도 없을 것입니다. 사포 절차 범프맵을 [기본색](advanced-material-properties-main.html#color)에 사용하면 이와 같은 고운 패턴을 비슷하게 표현합니다. 재질의 색인 [기본색](advanced-material-properties-main.html#color)을 만듭니다. 그 후 재질에 절차적 범프를 추가합니다. 고운 텍스처에 사포를 사용하고, 거친 텍스처에 자갈을 사용합니다.

범프 맵 중 하나를 체크하면 다른 제어도 사용할 수 있습니다. 하나보다 많은 범프 패턴을 재질에 추가할 수 있습니다.

#### 사포
{: #sandpaper}
랜덤하고 세밀하게 텍스처 처리된 모습으로 표현됩니다. 사포를 편집하려면 [크기](#scale), [세기](#strength), [회전](#rotation)을 변경합니다.

![images/sandpaper.png](images/sandpaper.png)
*작은 [크기](#scale)와 [세기](#strength)에서 큰 크기와 세기로 처리되는 사포* 

#### 자갈
{: #rubble}
울퉁불퉁하고 구멍난 표면을 표현합니다. 크기 조정하여 물, 흙, 표면의 얼룩을 나타낼 수 있습니다. 얼룩은 자갈을 사용하여, 큰 [크기](#scale)와 아주 작은 [강도](#strength)로 만들 수 있습니다. 자갈 범프는 사포보다 크기 범위가 더 큽니다.

![images/rubble.png](images/rubble.png)
*작은 [크기](#scale)와 [세기](#strength)에서 큰 크기와 세기로 처리되는 자갈*

#### 각뿔
{: #pyramid}
널링(knurling) 패턴처럼, 작은 피라미드 형태의 돌기를 표현합니다. [크기](#scale)는  X와 Y 각뿔의 기본 크기만을 제어합니다. [세기](#strength)는 각뿔의 "높이" 효과에 영향을 줍니다.

![images/pyramid.png](images/pyramid.png)
*크고 더 큰 [크기](#scale)를 나타내는 각뿔*

#### 주름
{: #wrinkled}
주름과 같은 모습으로 표현됩니다. 주름을 편집하려면 [크기](#scale), [세기](#strength), [회전](#rotation)을 변경합니다.

![images/wrinkled.png](images/wrinkled.png)
*크고 더 큰 [크기](#scale)를 나타내는 주름. [세기](#strength)는 일정합니다.*

#### 대리석
{: #marbled}
대리석처럼 표현하는 소용돌이 패턴입니다. 대리석을 편집하려면 [크기](#scale), [세기](#strength), [회전](#rotation)을 변경합니다.

![images/marbled.png](images/marbled.png)
*크고 더 큰 [크기](#scale)를 나타내는 대리석. [세기](#strength)는 일정합니다.*

### 비율
{: #scale}
비율은 범프의 비례적 크기를 제어합니다.

#### X/Y/Z
각 방향에서의 비율을 별도로 지정합니다.
![images/texturescalexy.png](images/texturescalexy.png)

#### 잠금
종횡비를 유지합니다.

### 강도
{: #strength}
깊이 표시를 제어합니다.
![images/texturestrength.png](images/texturestrength.png)

### 회전
{: #rotation}
패턴의 회전 각도를 설정합니다. 절차적 맵에 분명한 패턴이 있거나, 범프맵이 방향성 패턴을 만들기 위해 서로 다른 X, Y, Z 구성 요소를 기준으로 크기 조정된 경우에만 방향을 바꾸는 것이 분명하게 보입니다.
![images/texturerotated.png](images/texturerotated.png)

---
title: 조명 기본 설정
---

# ![images/flamingotab.svg](images/flamingotab.svg) {{page.title}}
조명은 이미지를 만들 때 가장 중요하지만 도외시된 부분입니다. 조명은 단순하게 모델을 비추는 한 방법이 아닙니다. 조명 설정은 분위기를 설정하고, 이미지 작업하는 데 가장 중요한 요소입니다.

![images/christophersotogutierrez.png](images/christophersotogutierrez.png)
*이미지 제공: Christopher Soto Gutiérrez.*

#### Flamingo 조명 제어는 어디에 있습니까?

* ![images/menuicon.png](images/menuicon.png)메뉴 > Flamingo nXt 5.0 메뉴 > 제어 패널 표시 > Flamingo nXt.
* 어느 한 탭을 오른쪽 클릭하고 Flamingo nXt를 선택합니다.


모델의 조명을 설정할 때 다음의 가이드라인을 사용하세요:

* 조명 기본 설정값으로 시작합니다.
* Since Flamingo nXt simulates real-world lighting, provide accurate information whenever possible.
* Avoid using unrealistic intensity levels for light sources.
* Set the units correctly for your model. The lighting will not be correct unless the units are correct. For example, if your model is in millimeters, set the model units to millimeters.
* Adjust the overall brightness of your rendering by using the [Brightness](render-window.html#brightness) control on the rendering display. Do not attempt to adjust the overall scene brightness by changing the intensity of all the light sources; the automatic [exposure](render-window.html#brightness) adjustment will defeat this.

조명 능력을 향상시키려면 빛을 이해하고 빛이 다양한 표면에 어떤 영향을 미치는지 알아야 합니다. 재질로 인해 그림자와 반사 효과가 가려질 수 있으므로, 일부 렌더링 전문가들은 재질을 적용하기 전에 모델의 조명을 설정합니다. 카메라에서 처리되는 방식처럼 객관적으로 조명을 보도록 노력하십시오.

## 조명 기본 설정
{: #lighting-presets}
A great starting place for lighting is the included Lighting presets that correspond to real-world lighting situations. Flamingo nXt provides lighting presets that can help get you started lighting your model. There are many more lighting options available, but the presets are often sufficient for many different renderings. Choose the Preset scheme that most closely resembles your scene.

Lighting in Flamingo nXt uses four preset methods categories:

> [스튜디오 조명](lighting-tab.html#studio-lighting)
> [실외 주광](lighting-tab.html#exterior-daylight)
> [실내 주광](lighting-tab.html#interior-daylight)
> [인공 조명](lighting-tab.html#artificial-lighting)

### 스튜디오 조명
{: #studio-lighting}
This scheme mimics the lighting found in a photographer's studio. It is most useful for rendering small-to-medium-sized objects in isolation.  It can also be used for any scene that is well lit through an HDRI environment.

![images/studiolighting-001.png](images/studiolighting-001.png){: .float-img-left} A high-dynamic-range (HDR) image file provides the primary lighting. The light from the HDR image resembles the interior lighting levels of the studio. The HDR settings are on the [Sky tab](sun-and-sky-tabs.html#sky). You can also add artificial lights to your scene using the Lights tab. The visible background in the Studio preset is black.

Studio lighting is optimized for tabletop setups for small design articles such as jewelry and product designs. In the preset scheme, the sun is off and an HDR image sky provides something for shiny objects to reflect.

For greater control, use light sources to light the scene. When lighting a studio setup, dramatic lighting is important. Create dramatic lighting by producing a lot of contrast. This means that dark areas are just as important as light areas. Dramatic lighting requires several light sources placed to create very light and very dark areas.

Lighting techniques for photography are generally the same as lighting for rendering. So a good place to start learning is one of the many books on the subject of photographic lighting. For more information about setting up studio lighting, see: [Studio Lighting Basics](../guides/studio-lighting-basics.html).

### 실외 주광
{: #exterior-daylight .clear-img}
이 기본 설정은 자연적인 태양과 하늘을 사용한 건축물 외부를 위한 주광(daylight)을 표현합니다.

![images/exteriorlighting-001.png](images/exteriorlighting-001.png){: .float-img-right} Specify settings on the [Sun](sun-and-sky-tabs.html#sun) and [Sky](sun-and-sky-tabs.html#sky) tabs. Set [sun angles](sun-and-sky-tabs.html#set-azimuth-and-altitude) directly or use [geographical location](sun-and-sky-tabs.html#set-location-on-earth), date, and time. The default visible background for this preset is the simulated sky.

Lighting a building exterior is the most straightforward lighting model. Most exterior lighting will need no more than the default [Sun](sun-and-sky-tabs.html#sun) light source.

When the [Sun](sun-and-sky-tabs.html#sun) is turned on, the scene must be designated as an [interior](#interior) or an [exterior](#exterior). This is because the contribution of the sky light, reflected light from the ground, and light reflected off other surfaces is much different when inside as opposed to outside. Using the correct [Interior/Exterior](#indirect) setting results in effective and realistic lighting.

때로는 장면이 실내인지 실외인지 쉽게 알 수 있습니다. 시점이 건물 바깥에 있다면, 실외 장면입니다. 시점이 방 안이라면 실내입니다. 어떤 장면들은 그렇게 명확하지 않기도 합니다. 건물에 둘러싸인 안뜰, 정원의 정자, 분해도, 단면이 여기에 속합니다. 안뜰의 높이보다 너비가 더 넓다면 많은 천공광이 들어오게 되므로, 실외 장면으로 조명을 설정해 보세요. 너비보다 높이가 더 높다면 실내 조명 설정을 시도해 보세요. 이 경우, 한 가지 트릭은 안뜰의 높은 곳에 데이라이트 포털을 추가하여 직사일광이 장면을 비추게 하는 것입니다.

조명은 경관 조명도 시뮬레이션할 수 있습니다. 집중 조명으로 건축물과 나무에 하이라이트를 줍니다. 이것은 야간이나  황혼 무렵의 장면에 적합한 방법입니다. 주간 야외 장면에서는, 현실 세계와 마찬가지로 어떤 인공 조명보다 태양빛이 압도적인 조건이 됩니다.

분해도, 단면, 위에서 아래 방향을 보는 엑소노메트릭 도면도 쉬운 대상이 아닙니다. 어떤 결과를 원하는가에 따라 결정이 달라집니다. 실외 장면을 속성으로 렌더링하려면 실외 렌더링 방법을 사용합니다. 이 방법으로 흥미로운 이미지를 얻지 못했다면 실내 조명을 사용해 보세요. 실내를 더 흥미롭게 표현할 수 있으나, 조명을 설정하는 데 시간이 더 많이 걸립니다.

### 실내 주광
{: #interior-daylight .clear-img}
이 기본 설정은 자연광이 비춰진 실내를 시뮬레이션합니다.

![images/interiordaylightnoportals.png](images/interiordaylightnoportals.png){: .float-img-left} 두 가지 구성 요소로 이루어져 있습니다. [태양](sun-and-sky-tabs.html#sun)의 직사일광과 지면, 실외 개체, [하늘](sun-and-sky-tabs.html#sky)을 통해 전달된 간접 태양광이 그 두 가지입니다.

The [Sun](sun-and-sky-tabs.html#sun) and [Sky](sun-and-sky-tabs.html#sky) settings are similar to the [Exterior](lighting-tab.html#exterior-daylight) preset.
주광의 직사일광 구성 요소 계산법은 간단합니다. 단순히 시간, 날짜, 장소를 지정하는 것만으로 충분히 정확한 결과를 얻을 수 있습니다.

실내 렌더링에 대한 안내:
{: .clear-img}

* Use accurate values for your [lights](lights-tab.html), [sky settings](sun-and-sky-tabs.html#sky), and window glass materials if possible.
* Because the sun and sky are much brighter than other lights, you may not see much effect from adding artificial lighting when the sun is on. This is normal. Avoid artificially boosting the power of your light sources.
* You can set the [Sun](sun-and-sky-tabs.html#sun-intensity) or [Sky](sun-and-sky-tabs.html#sky-intensity) intensity to a lower value. Since these settings simulate a clear sky, reducing their intensity will simulate cloudy or darker day lighting conditions.
* A [multi-channel](lights-tab.html#channel) rendering may help you get the picture you want, while still preserving accurate data.

### 인공 조명
{: #artificial-lighting}
![images/artificiallight-001.png](images/artificiallight-001.png){: style="float: right; padding-left: 25px;"} This scheme provides a simulation of an architectural interior at night, lit by lamps. Use the [Lights tab](lights-tab.html) or [Rhino light commands](lights-tab.html#rhino-light-commands) to insert and manage light objects in your model.

Indirect lighting, the lighting reflected off surfaces, is on when one of the two interior presets is selected and off for studio and exterior. This type of lighting is a significant component of an interior simulation. For exteriors and studio models the effects of indirect lighting is more subtle and is therefore turned off by default.

### 사용자 지정 조명
{: #custom  style="clear:both;"}
Custom is the tab to mix and match parts of the lighting prelights together.  For instance, if the scene is Exterior daylight, but lit with the addition of an HDRI environment, use the Custom tab to turn off and on parts of the lighting model.  When the values change from the defaults for the presets, the scheme becomes a custom scheme.

####  [태양](sun-and-sky-tabs.html#sun)
{: #sun}
Turn on and off the Sun tab in the drop down. The [Sun tab](sun-and-sky-tabs.html#sun) contains the controls for altering the parameters of the sun position.

![images/lightsunon.png](images/lightsunon.png)
*태양이 켜진 상태, 꺼진 상태.*
The sun is a very bright directional light source infinitely far from the model. The controls for the sun specify its direction using spherical coordinates. For more details, see the [Sun tab](sun-and-sky-tabs.html#sun) topic.

####  [태양](sun-and-sky-tabs.html#sky)
{: #sky}
Set the Sky channel to one of four options:

> 자동
> HDRI
> 색
> 이미지

For details, see the [Sky tab](sun-and-sky-tabs.html#sky) topic.
모델로부터 끝없이 떨어져 있는 반구형의 광원을 정의합니다.

#### 끄기
{: #off}
하늘을 끕니다.
![images/chromenosky.png](images/chromenosky.png)

#### 자동
{: #auto}
Provides an analytical model based on real-world sky conditions. The settings on the [Sun](sun-and-sky-tabs.html) tab control the appearance and light qualities of the sky.
![images/chromeautosky.png](images/chromeautosky.png)

#### HDRi
{: #hdri}
HDR 이미지는 반짝거리는 이미지에 반사되는 형상을 제공합니다.
![images/chromehdrbackground.png](images/chromehdrbackground.png)

#### 색
{: #color}
Sets the sky to a solid color or a two- or three-color gradient using controls similar to [Environment: Color and Gradient Backgrounds](environment-tab.html#color-and-gradient-backgrounds).
![images/colorsky.png](images/colorsky.png)

#### 이미지
{: #image}
Uses an image background with a planar, cylindrical, or spherical projection similar to [Environment: Image](environment-tab.html#image).
![images/chromeimagesky.png](images/chromeimagesky.png)


### 스튜디오 밝기
{: #studio-brightness}
Reduces the brightness of the [sun](sun-and-sky-tabs.html) and sky to mimic the interior lighting levels of a photographer's studio.
![images/studiobrightnessoffandon.png](images/studiobrightnessoffandon.png)
*스튜디오 밝기를 끈 상태 (왼쪽), 켠 상태 (오른쪽).*

### 조명
{: #lights}
인공 조명을 켜거나 끕니다.

![images/lightsonandoff.png](images/lightsonandoff.png)
*조명이 켜진 상태 (왼쪽), 꺼진 상태 (오른쪽).*

### 간접
{: #indirect}
서피스로부터 반사된 조명을 정의합니다. 기본적으로 실내 조명에는 켜져 있는 상태이며, 실외 및 스튜디오 조명 기본 설정에서는 꺼져 있는 상태입니다. 실외 렌더링에 간접 조명을 켜고 사용할 수 있습니다.

#### 방식
간접 조명의 계산 방식을 설정합니다.

#### 끄기
간접 조명 계산을 끕니다.

#### 실내
{: #interior}
실내 상황에 맞는 간접 조명으로 최적화합니다.

#### 실외
{: #exterior}
실외 상황에 맞는 간접 조명으로 최적화합니다.

다른 표면에서 반사된 간접 조명은 실외 렌더링에 보다 섬세하고 사실적인 느낌을 부여합니다. 특히, 간접 조명과 함께, 지붕의 처마, 발코니처럼 돌출된 부분의 아래쪽을 더욱 정확하게 렌더링할 수 있습니다.

#### 바운스
{: #bounces}
간접 조명으로 인해 반사되는 횟수를 지정합니다.

### 주변광
{: #ambient}
주변광은 렌더링에 더해지는 일정한 빛입니다. 이 설정은 장면에서 예상되는 총 주변광을 퍼센트로 지정하여 주변광의 강도를 제어합니다.
주변광의 양을 줄이면 이미지의 명암이 더욱 짙어집니다. 주변광을 지나치게 높이면 렌더링된 이미지가 단순하고 재미없어 보일 수 있습니다. 주변광이 너무 낮으면 명암이 과도하게 표현됩니다.

#### 없음
주변광 없음.

#### 실외
주변광을 실외 설정에 맞춰 최적화합니다.

#### 실내
주변광을 실내 설정에 맞춰 최적화합니다.

#### 스튜디오
주변광을 스튜디오 설정에 맞춰 최적화합니다.

## 사용자 지정 조명 저장

### 조명 구성표 저장
{: #save-lighting-scheme}
![images/saveschemeicon.png](images/saveschemeicon.png) 현재 조명의 구성표를 저장합니다.

### 조명 구성표 열기
{: #open-lighting-scheme}
![images/importfromfile.png](images/importfromfile.png) 저장된 조명 구성표를 엽니다.

---
---


# Lighting
조명은 이미지를 만들 때 가장 중요하지만 도외시된 부분입니다. 조명은 단순하게 모델을 비추는 한 방법이 아닙니다. 조명 설정은 분위기를 설정하고, 이미지 작업하는 데 가장 중요한 요소입니다.
![images/christophersotogutierrez.png](images/christophersotogutierrez.png)
*Image by Christopher Soto Gutiérrez.*
모델의 조명을 설정할 때 다음의 가이드라인을 사용하세요:

>Provide accurate information whenever possible.
>Avoid using unrealistic intensity levels for light sources.
>Set the units correctly for your model. The lighting will not be correct unless the units are correct. For example, if your model is in millimeters, set the model units to millimeters.
>Adjust the overall brightness of your rendering by using the [Brightness](render-window.html#brightness) control on the rendering display. Do not attempt to adjust the overall scene brightness by changing the intensity of all of the light sources; the automatic [exposure](render-window.html#brightness) adjustment will defeat this.

Flamingo nXt는 실제 조명을 시뮬레이션하므로 실제 조명 상황에 해당하는 기본 설정이 탑재되어 있습니다. Flamingo nXt의 조명에는 네 가지 기본 방식이 있습니다.

> [Studio lighting](lighting-tab.html#studio-lighting) 
> [Exterior daylight](lighting-tab.html#exterior-daylight) 
> [Interior daylight](lighting-tab.html#interior-daylight) 
> [인공 조명](lighting-tab.html#artificial-lighting) 

사용자가 선택하는 기본 설정에 따라 그에 맞는 제어 설정이 조명 탭에 표시됩니다.
조명 능력을 향상시키려면 빛을 이해하고 빛이 다양한 표면에 어떤 영향을 미치는지 알아야 합니다. 재질로 인해 그림자와 반사 효과가 가려질 수 있으므로, 일부 렌더링 전문가들은 재질을 적용하기 전에 모델의 조명을 설정합니다. 카메라에서 처리되는 방식처럼 객관적으로 조명을 보도록 노력하십시오.

### Save lighting scheme
{: #save-lighting-scheme}
현재 조명의 구성표를 저장합니다.

### Open lighting scheme
{: #open-lighting-scheme}
저장된 조명 구성표를 엽니다.

## Lighting Presets
{: #lighting-presets}
Flamingo nXt에는 모델의 조명 설정에 도움이 되는 조명 기본 설정이 있습니다. 많은 조명 옵션이 있지만, 다양한 렌더링에 기본 설정만으로도 충분한 경우가 많습니다.
두 가지 실내 기본 설정 중 하나를 선택하면 간접 조명과 표면에 반사된 조명이 켜지고, 스튜디오와 실외 조명에서는 꺼집니다. 이러한 조명 유형은 실내 시뮬레이션에서 매우 중요한 구성요소입니다. 실외와 스튜디오 모델의 경우, 간접 조명 효과가 좀 더 은은하게 표현되므로, 기본적으로 꺼짐 상태가 됩니다.
사용자가 원하는 장면과 가장 비슷한 기본 설정 구성표를 선택하십시오.

## Studio lighting
{: #studio-lighting}
![images/studiolighting-001.png](images/studiolighting-001.png)
This scheme mimics the lighting found in a photographer's studio. It is most useful for rendering small-to-medium-sized objects in isolation. A high-dynamic-range (HDR) image file provides the primary lighting. The light from the HDR image resembles the interior lighting levels of the studio. The HDR settings are on the [Sky tab](lighting-advanced-tab.html#sky). You can also add artificial lights to your scene using the Lights tab. The visible background in the Studio preset is black.
스튜디오 조명은 주얼리와 제품 디자인과 같은 작은 디자인 물품용 테이블탑 설정에 최적화되어 있습니다.
이 기본 설정에서 태양은 꺼진 상태이며, HDR 이미지 하늘은 반짝거리는 개체에 반사되는 형상을 제공합니다.
전체적으로 제어하기 위해 광원을 사용하여 장면을 비춥니다.   스튜디오 설정 조명에서는 극적인 조명이 중요합니다. 명암을 짙게 만들면 조명을 극적으로 만들 수 있습니다. 이것은 어두운 부분도 밝은 부분만큼 중요하다는 것을 의미합니다. 극적인 조명에는 아주 밝고 아주 어두운 부분을 만드는 방식으로 설치된 일정 수의 조명이 필요합니다.
Lighting techniques for photography are generally the same as lighting for rendering, so a good place to start learning is one of the many books on the subject of photographic lighting. For more information about setting up studio lighting, see: [Studio Lighting Basics](studio-lighting-basics.html).

## Exterior daylight
{: #exterior-daylight}
![images/exteriorlighting-001.png](images/exteriorlighting-001.png)
이 기본 설정은 자연적인 태양과 하늘을 사용한 건축물 외부를 위한 주광(daylight)을 표현합니다.
Specify settings on the [Sun](sun-and-sky-tabs.html#sun) and [Sky](sun-and-sky-tabs.html#sky) tabs. Set [sun angles](sun-and-sky-tabs.html#set-azimuth-and-altitude) directly or use [geographical location](sun-and-sky-tabs.html#set-location-on-earth), date, and time. The default visible background for this preset is the simulated sky.
Lighting a building exterior is the most straightforward lighting model. Most exterior lighting will need no more than the default [Sun](sun-and-sky-tabs.html#sun) light source.
When the [Sun](sun-and-sky-tabs.html#sun) is turned on, the scene must be designated as an [interior](lighting-advanced-tab.html#interior) or an [exterior](lighting-advanced-tab.html#exterior). This is because the contribution of the sky light, reflected light from the ground, and light reflected off other surfaces is much different when inside as opposed to outside. Using the correct [Interior/Exterior](lighting-advanced-tab.html#indirect) setting results in effective and realistic lighting.
때로는 장면이 실내인지 실외인지 쉽게 알 수 있습니다. 시점이 건물 바깥에 있다면, 실외 장면입니다. 시점이 방 안이라면 실내입니다. 어떤 장면들은 그렇게 명확하지 않기도 합니다. 건물에 둘러싸인 안뜰, 정원의 정자, 분해도, 단면이 여기에 속합니다. 안뜰의 높이보다 너비가 더 넓다면 많은 천공광이 들어오게 되므로, 실외 장면으로 조명을 설정해 보세요. 너비보다 높이가 더 높다면 실내 조명 설정을 시도해 보세요. 이 경우, 한 가지 트릭은 안뜰의 높은 곳에 데이라이트 포털을 추가하여 직사일광이 장면을 비추게 하는 것입니다.
조명은 경관 조명도 시뮬레이션할 수 있습니다. 집중 조명으로 건축물과 나무에 하이라이트를 줍니다. 이것은 야간이나  황혼 무렵의 장면에 적합한 방법입니다. 주간 야외 장면에서는, 현실 세계와 마찬가지로 어떤 인공 조명보다 태양빛이 압도적인 조건이 됩니다.
분해도, 단면, 위에서 아래 방향을 보는 엑소노메트릭 도면도 쉬운 대상이 아닙니다. 어떤 결과를 원하는가에 따라 결정이 달라집니다. 실외 장면을 속성으로 렌더링하려면 실외 렌더링 방법을 사용합니다. 이 방법으로 흥미로운 이미지를 얻지 못했다면 실내 조명을 사용해 보세요. 실내를 더 흥미롭게 표현할 수 있으나, 조명을 설정하는 데 시간이 더 많이 걸립니다.

## Interior daylight
{: #interior-daylight}
![images/interiordaylightnoportals.png](images/interiordaylightnoportals.png)
This scheme simulates an interior lit by natural light. It consists of two components: direct sunlight transmitted from the [Sun](sun-and-sky-tabs.html#sun) and indirect sunlight transmitted via the [Sky](sun-and-sky-tabs.html#sky), the ground, and other exterior objects.
The [Sun](sun-and-sky-tabs.html#sun) and [Sky](sun-and-sky-tabs.html#sky) settings are similar to the [Exterior](lighting-tab.html#exterior-daylight) preset.
주광의 직사일광 구성 요소 계산법은 간단합니다. 단순히 시간, 날짜, 장소를 지정하는 것만으로 충분히 정확한 결과를 얻을 수 있습니다.

## Notes

>Use accurate values for your [lights](lights-tab.html), [sky settings](sun-and-sky-tabs.html#sky), and window glass materials if possible.
>Because the sun and sky are much brighter than other lights, you may not see much effect from adding artificial lighting when the sun is on. This is normal. Avoid artificially boosting the power of your light sources.
>You can set the [Sun](sun-and-sky-tabs.html#sun-intensity) or [Sky](sun-and-sky-tabs.html#sky-intensity) intensity to a lower value. Since these settings simulate a clear sky, reducing their intensity will simulate cloudy or darker day lighting conditions.
>A [multi-channel](lights-tab.html#channel) rendering may help you get the picture you want, while still preserving accurate data.

## Artificial lighting
{: #artificial-lighting}
This scheme provides a simulation of an architectural interior at night, lit by lamps. Use the [Lights tab](lights-tab.html) or [Rhino light commands](lights-tab.html#rhino-light-commands) to insert and manage light objects in your model.
![images/artificiallight-001.png](images/artificiallight-001.png)

## Custom
{: #custom-lighting}
When the values on the [Advanced tab](lighting-advanced-tab.html) change from the defaults for the presets, the scheme becomes a custom scheme.

## Lighting controls

###  [Sky](sun-and-sky-tabs.html#sky) 
The [Sky tab](sun-and-sky-tabs.html#sky) has one mode for HDR image sky (studio lighting) and one for daylight lighting modes.

###  [태양](sun-and-sky-tabs.html#sun) 
The [Sun tab](sun-and-sky-tabs.html#sun) contains the controls for altering the parameters of the automatic sky. The sun is a very bright directional light source infinitely far from the model. The controls for the sun specify its direction using spherical coordinates.

###  [Advanced](lighting-advanced-tab.html) 
The [Advanced tab](lighting-advanced-tab.html) lets you override all of the preset scheme settings to create custom lighting conditions.

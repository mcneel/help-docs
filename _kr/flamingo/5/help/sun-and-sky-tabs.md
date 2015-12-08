---
title: 태양과 하늘
---

# ![imagessun.svg](images/sun.svg) {{page.title}}
[태양](#sun)과 [하늘](#sky)은 서로 밀접하게 연관되어 있습니다. 자동 모드에서 태양은 하늘의 밝기를 변경시킬 수 있습니다. 태양이 켜져 있고 하늘이 HDRI 일 때, 그 강도의 균형을 맞추는 것이 중요합니다.

## 태양
{: #sun}
태양은 보이지 않는 강력한 평행광입니다. 위도, 경도, 시간, 계절과 같은 실제 세계 조건을 시뮬레이션하는 요소가 태양의 방향과 밝기를 제어합니다.

이 도움말 항목은 Flamingo 태양 제어에 대해 설명합니다. [Rhinoceros 태양](http://docs.mcneel.com/rhino/5/help/ko-kr/commands/sun.htm) 제어를 사용하여 태양을 배치할 수 있습니다. Flamingo에서 두 태양 제어를 동기화합니다.

##### Flamingo 태양 제어는 어디에 있습니까?

태양은 [조명 기본 설정](lighting-tab.html#lighting-presets) 또는 [사용자 지정 조명 설정](lighting-tab.html#sun)에서 활성화해야 합니다.

* ![images/options.png](images/options.png)도구모음 >![images/flamingo-icon.png](images/flamingo-icon.png)Flamingo nXt 도구모음
* ![images/menuicon.png](images/menuicon.png)메뉴 > Flamingo nXt 5.0 메뉴 > 제어 패널 표시 > Flamingo nXt 탭 > 태양

**안내:** 조명 기본 설정에서 태양이 활성화된 경우에만 태양 탭이 표시됩니다.

태양빛을 계산하려면 태양 각도가 필요합니다. 태양의 방향을 지정하는 방법에는 2 가지가 있습니다. 날짜/시간/장소로 결정하는 방법과 직사광선의 각도로 지정하는 방법이 그것입니다. 날짜, 시간, 장소를 사용하여 모델이 위치한 부지에서 실제 태양을 시뮬레이션합니다. 태양 직사광선의 각도는 실제 태양을 참조하지 않고 빛의 각도를 제어합니다. 직사광선 각도를 사용하여 조명 효과를 시험해 보세요.

![images/sydneymorning.png](images/sydneymorning.png)  ![images/stockholmmorning.png](images/stockholmmorning.png)
*호주, 시드니, 6월 21일, 09:30 (왼쪽). 스웨덴, 스톡홀름, 6월 21일, 09:30 (오른쪽).*

### 방위각과 고도 설정
{: #set-azimuth-and-altitude}
태양의 방향을 직접 설정하려면 태양의 각도를 사용합니다. [방위각](#azimuth)과 [고도](#altitude) 제어를 사용합니다.

#### 방위각
{: #azimuth}
가로 평면에서 북쪽(0)을 기준, 도 단위의 각도로 태양 방향을 설정합니다. 원형 지도에서 전세계를 평면뷰로 표시합니다.

#### 고도
{: #altitude}
Sets the sun's height in the sky in angle degrees from the Equator (0).  The half circle map simulates a section through the vertical direction of the world coordinates.

### 지구상의 위치 설정
{: #set-location-on-earth}
Use the sun angle calculator to place the sun based on Date, Time, Location.  **Note:** As with all Sun calculators, the Sun position accuracy may vary. If absolute accuracy is required it is recommended to verify the sun location.  

#### 날짜
{: #date}
날짜를 지정합니다.

#### 시간
{: #time}
현지 시각을 지정합니다.

#### 일광 시간 절약제
{: #daylight-savings-time}
시간을 한 시간 앞당깁니다.

#### 위도/경도
{: #latitude-longitude}
위도와 경도를 입력하거나 지도에서 위치를 지정합니다.
The numbers will also update to display the latitude and longitude of a location picked on the map with the mouse cursor.

#### 시간대
{: #time-zone}
Displays the time zone based on Latitude and Longitude for the current location.

#### 도시 목록
{: #city-list}
Use this to select a major city to set the location.

#### 지도
{: #map}
Click the map to specify a location. Drag with the left mouse button to pan the map.

### 태양광 강도
{: #sun-intensity}
Modifies the brightness of the sun (direct) daylight component. The intensity of sun is automatically calculated based on solar angles and sky conditions, but can be modified to balance with other lights.

### 태양 하이라이트
{: #sun-highlight}
태양 하이라이트의 선명도입니다.

![images/sunhighlight-0.png](images/sunhighlight-0.png)
* 태양 하이라이트=0 (왼쪽), 1 (오른쪽).*

**안내:** 태양 하이라이트 설정을 사용하면 때때로 실외 렌더링에 태양의 하이라이트 아티팩트가 보일 수 있습니다. 이 아티팩트를 완화시키거나 없애려면 태양 하이라이트를 작은 값으로 설정하세요.
{: #speckle-artifacts}

{% include_relative snippets/snippet-sunchannel.md %}

#### 북쪽 방향
{: #north}
**안내:** 북쪽은 절대좌표 Y 방향입니다.

## 하늘
{: #sky}
The Sky is a large sphere around the rendering that can be used for lighting. The Sky is very different from environment.  Sky controls lighting. Environment controls what is reflected and visible in the background. There are many situations where the Sky and Environment might be set differently.

#### Flamingo 하늘 제어는 어디에 있습니까?
The Sky must be activated through the [Lighting Preset](lighting-tab.html#lighting-presets) or the [Custom Lighting settings](lighting-tab.html#sky).

 1. ![images/options.png](images/options.png)Toolbars >![images/flamingo-icon.png](images/flamingo-icon.png)Flamingo nXt 도구모음
 1. ![images/menuicon.png](images/menuicon.png)메뉴 > Flamingo nXt 5.0 메뉴 > 제어 패널 표시 > Flamingo nXt 탭 > 하늘

[실외](lighting-tab.html#exterior-daylight)와 [실내](lighting-tab.html#interior-daylight) 주광의 기본 설정에서는 기본적으로 자동 하늘을 사용합니다. [스튜디오](lighting-tab.html#studio-lighting) 조명 기본 설정에서는 HDR 이미지 조명을 기본적으로 사용합니다.

하늘은 다음의 5가지 방법으로 설정할 수 있습니다:

>[끄기](lighting-tab.html#off)
>[자동 하늘](#automatic-sky)
>[하이 다이내믹 레인지 (HDRI)](#high-dynamic-range-image-sky)
>[색](#color-sky)
>[이미지](#image-sky)

The two best settings for sky lighting types are [HDR image](#high-dynamic-range-image-sky) sky and [Automatic sky](#automatic-sky). HDR image sky uses an image with lighting values stored on each pixel to provide light and reflection. Automatic sky uses a real-world sun location and cloudiness to simulate a sky.  These settings will produce the most dynamic renderings.

### 자동 하늘
{: #automatic-sky}
Automatic sky uses settings from the [Sun tab](sun-and-sky-tabs.html) to specify the color range and intensity of the skylight.  For instance, when the sun is high in the sky, the lighting and colors of the sky are very different than when the sun is low in the sky.

![images/sky-002.png](images/sky-002.png)
*자동 하늘: 하늘의 태양이 높을 떄 (왼쪽), 낮을 때 (오른쪽).*

#### 운량
{: #sky-cloudiness}
When Cloudiness is turned off, the sky is considered clear and strong shadows are created. The greater the cloudiness, the less contrast there will be between the light and shadows. Greater cloudiness will create lighter shadows and a more even lighting effect. The Cloudiness setting affects many aspects of the daylight calculation, including the relative amounts of direct vs. indirect lighting, the way indirect lighting is calculated, and the background color if Automatic Sky mode has been selected. The Cloudiness setting varies from 0 (clear) to 1 (completely overcast). The cloudiness settings around 0.35 - 0.50 is a very sensitive and dynamic range.

![images/cloudiness0.png](images/cloudiness0.png)
*운량 0 (왼쪽), 1 (오른쪽).*

#### 하늘 강도
{: #sky-intensity}
Modifies the brightness of the sky (indirect) daylight component. The intensity of skylight is automatically calculated based on solar angles and sky conditions, but can be modified. **Note:** This setting only matters if there are other lights in the scene that have to be compensated for. If there are no other lights, the tone operator will compensate the exposure and the rendered image will not be brighter or dimmer based on this setting.

{% include_relative snippets/snippet-skychannel.md %}

### HDRI(High-Dynamic-Range Image) 하늘
{: #high-dynamic-range-image-sky}
[하이 다이내믹 레인지 (HDR 또는 HDRi)](https://en.wikipedia.org/wiki/High-dynamic-range_imaging) 이미지는 2D 이미지 파일입니다. 이 이미지는 일반적인 이미지 파일 (jpg, png 등) 보다 훨씬 광범위한 값을 포함하고 있습니다. 이러한 추가적인 데이터를 사용하여 모델에 조명을 설정할 수 있습니다. HDR에 포함된 값이 정확하다면 조명도 정확하게 설정됩니다. 스튜디오 조명 기본 설정에서는 HDR 이미지를 하늘로 사용합니다. 스튜디오 조명을 실내 환경이라고 생각한다면, HDR 이미지를 해당 이미지에 있는 색을 기반으로 빛을 발산하는 천장이라고 생각할 수 있습니다.

![images/lighting-001.png](images/lighting-001.png)
*HDRi 조명*

HDR 이미지에는 와트 단위로 표시된 방사휘도(radiance value)가 있습니다. 만약 방사휘도가 없다면 적절한 조명 수준을 얻기 위해서 HDR 이미지의 강도를 조정해야 할 수도 있습니다.

In addition to the Sky, a different HDR image can be used for each of the three visible backgrounds: [Visible](environment-tab.html#advanced-background), [Reflected](environment-tab.html#advanced-background), and [Refracted](environment-tab.html#advanced-background) background.

#### HDRI 이미지
Specifies the HDR (HDR and HDRI are the same file type) image file. Click on the image to select a different HDRI.

![images/hdrimage-001.png](images/hdrimage-001.png)
* 등장방향 투영*

HDR images come in two projection types which let the image to properly wrap around the sky sphere. The most popular is equirectangular.  These images are rectangular with an aspect ratio of 2:1. Equirectangular images will have similar resolution over the whole image. The second projection is spherical. Spherical HDRI images are square in aspect ratio and the image will show great curvature. Spherical projections have less resolution at the seam.

#### 강도
Modifies the brightness of the HDR image light. This setting only matters if there are other lights in the scene that have to be compensated for. If there are no other lights, the tone operator will compensate the exposure and the rendered image will not be brighter or dimmer based on this setting.

![images/hdrlightintensitylow.png](images/hdrlightintensitylow.png)
* 낮고 높은 HDR 강도*

{% include_relative snippets/snippet-rotatehdrimage.md %}In the illustration, the image has been rotated so the reflection of the sun appears on the object. Enter rotation degrees or interactively move the rotation widget indicator.
![images/hdrlightrotation2.png](images/hdrlightrotation2.png)
* 태양이 개체에 나타나도록 이미지가 회전되었습니다.*

#### 채도
빛의 채도입니다. HDR 이미지의 빛은 이미지에 있는 픽셀의 색이므로 때때로 원치 않는 효과를 얻을 수도 있습니다. 이미지에서 색이 아니라 빛을 얻으려면 채도를 낮게 설정하십시오.

![images/hdrlightsaturation0.png](images/hdrlightsaturation0.png)
* 낮은 채도(왼쪽), 높은 채도(오른쪽)*

{% include_relative snippets/snippet-mirrorimage.md %}

{% include_relative snippets/snippet-skychannel.md %}

### 색
{: #color-sky}
It is possible to use a color or gradient of color to light the scene. The colors in the sky are multiplied by the intensity value to give the colors a lighting value.

#### 강도
The Intensity value is used to multiply the colors in the Sky and result in a lighting value.  Colors can range from 0 - 256 per channel. Intensity will multiply those values.

#### 색 유형
There are three ways to control the color of the sky.  These are similar to the Color Environment controls.  See [Color Background](environment-tab.html#environment-color-and-gradient-backgrounds) controls for more information.

### 이미지
{: #image-sky}
It is possible to use an image to light the scene. The colors in the image are multiplied by the intensity value to give the colors a lighting value.

#### 강도
The Intensity value is used to multiply the colors in the Sky and result in a lighting value.  Colors can range from 0 - 256 per channel. Intensity will multiply those values.

#### 이미지 투영
There are many ways to control how an image is mapped to the sky.  These are similar to the Image Background controls.  See [Image Background](environment-tab.html#environment-image) controls for more information.

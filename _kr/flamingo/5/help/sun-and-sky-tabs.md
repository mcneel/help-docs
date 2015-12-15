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
적도(0)를 기준으로 도 단위의 각도로, 하늘에서의 태양 고도를 설정합니다. 반원 맵은 절대좌표의 수직 방향을 기준으로 하는 섹션을 나타냅니다.

### 지구상의 위치 설정
{: #set-location-on-earth}
날짜, 시간, 위치를 기준으로 태양을 배치하려면 태양 각도 계산기를 사용합니다.  **안내:** 모든 태양 계산기와 마찬가지로, 태양 위치의 정확도는 다양할 수 있습니다. 절대적인 정확도가 필요하다면 태양 위치를 지정하는 것을 권장합니다.  

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
마우스 커서로 지도상에서 지정된 위치의 위도와 경도를 나타내는 숫자도 업데이트됩니다.

#### 시간대
{: #time-zone}
현재 위치의 위도와 경도를 기준으로 시간대를 표시합니다.

#### 도시 목록
{: #city-list}
이 목록에서 주요 도시를 선택하여 위치를 설정합니다.

#### 지도
{: #map}
지도를 클릭하여 위치를 지정합니다. 왼쪽 마우스 단추로 끌어 지도에서 초점 이동합니다.

### 태양광 강도
{: #sun-intensity}
태양 (직사광선) 일광 구성 요소의 밝기를 수정합니다. 태양의 강도는 태양 각도와 하늘 조건을 기반으로 자동으로 계산되지만 다른 조명과의 균형을 맞추기 위해 수정할 수 있습니다.

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
하늘은 렌더링을 중심으로 하는 큰 구이며 조명에 사용될 수 있습니다. 하늘은 환경과 매우 다릅니다. 하늘은 빛을 제어합니다. 환경은 배경에 무엇이 반사되고, 보이는지를 제어합니다. 하늘과 환경이 다르게 설정되는 경우가 많이 있습니다.

#### Flamingo 하늘 제어는 어디에 있습니까?
하늘은 [조명 기본 설정](lighting-tab.html#lighting-presets) 또는 [사용자 지정 조명 설정](lighting-tab.html#sky)에서 활성화해야 합니다.

 1. ![images/options.png](images/options.png)Toolbars >![images/flamingo-icon.png](images/flamingo-icon.png)Flamingo nXt 도구모음
 1. ![images/menuicon.png](images/menuicon.png)메뉴 > Flamingo nXt 5.0 메뉴 > 제어 패널 표시 > Flamingo nXt 탭 > 하늘

[실외](lighting-tab.html#exterior-daylight)와 [실내](lighting-tab.html#interior-daylight) 주광의 기본 설정에서는 기본적으로 자동 하늘을 사용합니다. [스튜디오](lighting-tab.html#studio-lighting) 조명 기본 설정에서는 HDR 이미지 조명을 기본적으로 사용합니다.

하늘은 다음의 5가지 방법으로 설정할 수 있습니다:

>[끄기](lighting-tab.html#off)
>[자동 하늘](#automatic-sky)
>[하이 다이내믹 레인지 (HDRI)](#high-dynamic-range-image-sky)
>[색](#color-sky)
>[이미지](#image-sky)

천공광(天空光)에 사용하는 가장 좋은 두 가지 설정은 [HDR 이미지](#high-dynamic-range-image-sky) 하늘과 [자동 하늘](#automatic-sky)입니다. HDR 이미지 하늘은 빛과 반사를 나타내도록 각 픽셀에 저장된 라이트밸류(Light Value)가 있는 이미지를 사용합니다. 자동 하늘은 실제 태양 위치와 운량을 사용하여 하늘을 시뮬레이션합니다. 이 설정은 가장 생생한 렌더링을 만들어냅니다.

### 자동 하늘
{: #automatic-sky}
자동 하늘은 색의 범위와 천공광의 강도 지정에 [태양 탭](sun-and-sky-tabs.html)의 설정을 사용합니다. 예를 들어, 태양이 하늘 높이 있을 때와 낮게 있을 때를 비교하면 하늘의 빛과 색은 매우 다릅니다.

![images/sky-002.png](images/sky-002.png)
*자동 하늘: 하늘의 태양이 높을 떄 (왼쪽), 낮을 때 (오른쪽).*

#### 운량
{: #sky-cloudiness}
이 운량 설정이 꺼져 있으면 하늘이 맑은 상태이므로 강한 그림자가 만들어집니다. 운량이 많을수록, 빛과 그림자 사이에 명암이 더 적게 만들어집니다. 직접 조명과 간접 조명 사이의 상대적인 정도, 간접 조명이 계산되는 방법, 자동 하늘이 선택된 상태에서 배경색 지정 등, 다양한 주광 계산에 운량 설정이 영향을 줍니다.  운량 설정은 0 (맑음)에서 1 (완전히 구름으로 뒤덮인 상태) 사이의 값으로 달라집니다. 0.35 ~ 0.50 정도의 운량 설정은 매우 민감하면서도 다이내믹한 범위입니다. 

![images/cloudiness0.png](images/cloudiness0.png)
*운량 0 (왼쪽), 1 (오른쪽).*

#### 하늘 강도
{: #sky-intensity}
하늘 (간접) 주광 구성 요소의 밝기를 수정합니다. 천공광(skylight)의 강도는 태양 각도와 하늘 조건을 기반으로 자동으로 계산되지만 수정할 수 있습니다. **안내:** 장면에 보정되어야 하는 다른 조명이 있는 경우에만 이 설정이 해당됩니다. 다른 조명이 없는 경우, 톤 연산자가 노출을 보정하고 렌더링된 이미지는 이 설정을 바탕으로 더 밝아지거나 더 어두워지지 않게 됩니다.

{% include_relative snippets/snippet-skychannel.md %}

### HDRI(High-Dynamic-Range Image) 하늘
{: #high-dynamic-range-image-sky}
[하이 다이내믹 레인지 (HDR 또는 HDRi)](https://en.wikipedia.org/wiki/High-dynamic-range_imaging) 이미지는 2D 이미지 파일입니다. 이 이미지는 일반적인 이미지 파일 (jpg, png 등) 보다 훨씬 광범위한 값을 포함하고 있습니다. 이러한 추가적인 데이터를 사용하여 모델에 조명을 설정할 수 있습니다. HDR에 포함된 값이 정확하다면 조명도 정확하게 설정됩니다. 스튜디오 조명 기본 설정에서는 HDR 이미지를 하늘로 사용합니다. 스튜디오 조명을 실내 환경이라고 생각한다면, HDR 이미지를 해당 이미지에 있는 색을 기반으로 빛을 발산하는 천장이라고 생각할 수 있습니다.

![images/lighting-001.png](images/lighting-001.png)
*HDRi 조명*

HDR 이미지에는 와트 단위로 표시된 방사휘도(radiance value)가 있습니다. 만약 방사휘도가 없다면 적절한 조명 수준을 얻기 위해서 HDR 이미지의 강도를 조정해야 할 수도 있습니다.

하늘 외에도, 다른 HDR 이미지를 세 가지 배경 채널 ( [보이는 배경](environment-tab.html#advanced-background), [반사된 배경](environment-tab.html#advanced-background), [굴절된 배경](environment-tab.html#advanced-background) )로 사용할 수 있습니다.

#### HDRI 이미지
HDR (HDR과 HDRi는 동일한 파일 유형입니다) 이미지 파일을 지정합니다. 다른 HDRi를 선택하려면 원하는 이미지를 클릭합니다.

![images/hdrimage-001.png](images/hdrimage-001.png)
* 등장방향 투영*

HDR 이미지에는 하늘 구를 제대로 둘러싸게 하는 두 가지 투영 유형이 있습니다. 가장 많이 사용되는 유형은 등장방형(equirectangular)입니다. 이 이미지는 종횡비가 2:1인 직사각형입니다. 등장방향 이미지는 이미지 전체에 걸쳐 해상도가 비슷합니다. 두 번째 투영은 구(球) 투영입니다. 구 형태 HDR 이미지는 종횡비가 정사각형이며 이미지의 곡률이 잘 표현됩니다. 구 투영은 심 위치에서 해상도가 더 낮습니다.

#### 강도
HDR 이미지 조명의 밝기를 수정합니다. 장면에 보정되어야 하는 다른 조명이 있는 경우에만 이 설정이 해당됩니다. 다른 조명이 없는 경우, 톤 연산자가 노출을 보정하고 렌더링된 이미지는 이 설정을 바탕으로 더 밝아지거나 더 어두워지지 않게 됩니다.

![images/hdrlightintensitylow.png](images/hdrlightintensitylow.png)
* 낮고 높은 HDR 강도*

{% include_relative snippets/snippet-rotatehdrimage.md %}그림의 경우, 이미지가 회전되었으므로 개체에 태양이 반사되어 보입니다. 회전 각도를 입력하거나 회전 위젯 표시기에서 직접 회전을 지정합니다.
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
장면에 빛을 비추는 데 색 또는 색의 그라데이션을 사용할 수 있습니다. 하늘의 색은 색에 라이트밸류(Light Value)를 주기 위해 강도 값으로 곱합니다. 

#### 강도
강도 값은 하늘의 색과 라이브 밸류의 결과를 곱하는 데 사용됩니다. 색의 범위는 채널당 0에서 256까지입니다. 강도는 이 값을 증가시킵니다. 

#### 색 유형
하늘의 색을 제어하는 방법에는 세 가지가 있습니다. 이 설정은 색 환경 제어와 비슷합니다. 자세한 정보는 [색 배경](environment-tab.html#environment-color-and-gradient-backgrounds) 제어를 참조하세요.

### 이미지
{: #image-sky}
장면에 빛을 비추는 데 이미지를 사용할 수 있습니다. 이미지의 색은 색에 라이트밸류(Light Value)를 주기 위해 강도 값으로 곱합니다.

#### 강도
강도 값은 하늘의 색과 라이브 밸류의 결과를 곱하는 데 사용됩니다. 색의 범위는 채널당 0에서 256까지입니다. 강도는 이 값을 증가시킵니다.

#### 이미지 투영
하늘에 이미지를 매핑하는 방법은 다양합니다. 이 설정은 이미지 배경 제어와 비슷합니다. 자세한 정보는 [이미지 배경](environment-tab.html#environment-image) 제어를 참조하세요.

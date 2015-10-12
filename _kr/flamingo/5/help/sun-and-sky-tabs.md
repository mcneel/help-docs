---
---


# Sun
{: #sun}
The **Sun** is a powerful invisible parallel light. Factors simulating real-world conditions such as latitude and longitude, time of day, and season control the Sun's direction and brightness.
태양빛을 계산하려면 태양 각도가 필요합니다. 태양의 방향을 지정하는 방법에는 2 가지가 있습니다. 날짜/시간/장소로 결정하는 방법과 직사광선의 각도로 지정하는 방법이 그것입니다. 날짜, 시간, 장소를 사용하여 모델이 위치한 부지에서 실제 태양을 시뮬레이션합니다. 태양 직사광선의 각도는 실제 태양을 참조하지 않고 빛의 각도를 제어합니다. 직사광선 각도를 사용하여 조명 효과를 시험해 보세요.
 *![images/sydneymorning.png](images/sydneymorning.png)* 
*Sydney, Australia, 21-June, 09:30.*
 *![images/stockholmmorning.png](images/stockholmmorning.png)* 
*Stockholm, Sweden, 21-June, 09:30.*

## Set azimuth and altitude
{: #set-azimuth-and-altitude}
Use solar angles to set the sun's direction. Enables **Azimuth** and **Altitude** controls.

#### Azimuth
{: #azimuth}
북쪽(0)을 기준으로 도 단위의 각도로 태양 방향을 설정합니다.

#### Altitude
{: #altitude}
적도(0)를 기준으로 도 단위의 각도로, 하늘에서의 태양 고도를 설정합니다.

## Set location on Earth
{: #set-location-on-earth}
 **{: #north}Note** : **North** is the World Y direction.

### Date
{: #date}
날짜를 지정합니다.

### Time
{: #time}
현지 시각을 지정합니다.

### Daylight savings time
{: #daylight-savings-time}
시간을 한 시간 앞당깁니다.

### Latitude/Longitude
{: #latitude-longitude}
위도와 경도를 입력하거나 지도에서 위치를 지정합니다.
지도상에서 지정된 위치의 위도와 경도를 나타내는 숫자도 업데이트됩니다.

### 시간대
{: #time-zone}

>Displays the time zone for the specified location.

### City list
{: #city-list}

>Select a city to set the location.

### Map
{: #map}
지도를 클릭하여 위치를 지정합니다.
 **Note** : Drag with the left mouse button to pan the map.

### Sun intensity
{: #sun-intensity}
태양 (직사광선) 일광 구성 요소의 밝기를 수정합니다. 태양의 강도는 태양 각도와 하늘 조건을 기반으로 자동으로 계산되지만 다른 조명과의 균형을 맞추기 위해 수정할 수 있습니다.

### Sun highlight
{: #sun-highlight}
태양 하이라이트의 선명도입니다.
![images/sunhighlight-0.png](images/sunhighlight-0.png)
*Sun highlight=0 (left) and 1 (right).*
 **{: #speckle-artifacts}Note** : Solar highlight artifacts can sometimes be seen on exterior renderings when the **Sun highlight** setting is used. To mitigate or eliminate this artifact, set the **Sun highlight** to a smaller value.{: #sun-channel}
{% include_relative snippets/snippet-sunchannel.md %}
## 하늘
{: #sky}
Two kinds of built-in sky lighting are provided: [HDR image](lighting-advanced-tab.html#hdri) sky and [Automatic sky](#automatic-sky). HDR image sky uses an image with lighting values stored on each pixel to provide light and reflection. Automatic sky uses a real-world sun location and cloudiness to simulate a sky.
The lighting preset schemes for [Exterior](lighting-tab.html#exterior-daylight) and [Interior](lighting-tab.html#interior-daylight) daylight use the Automatic sky by default. The [Studio](lighting-tab.html#studio-lighting) lighting preset scheme uses HDR image lighting by default.

## High-Dynamic-Range Image Sky
{: #high-dynamic-range-image-sky}
하이 다이내믹 레인지 (HDR) 이미지는 2D 이미지 파일입니다. 이 이미지는 일반적인 이미지 파일 (jpg, png 등) 보다 훨씬 광범위한 값을 포함하고 있습니다. 이러한 추가적인 데이터를 사용하여 모델에 조명을 설정할 수 있습니다. HDR에 포함된 값이 정확하다면 조명도 정확하게 설정됩니다.
![images/lighting-001.png](images/lighting-001.png)
*HDRi lighting.*
HDR 이미지에는 와트 단위로 표시된 방사휘도(radiance value)가 있습니다. 만약 방사휘도가 없다면 적절한 조명 수준을 얻기 위해서 HDR 이미지의 강도를 조정해야 할 수도 있습니다.
In addition to the Sky, a different HDR image can be used for each of the three background channels: [Visible](environment-tab.html#advanced-background), [Reflected](environment-tab.html#advanced-background), and [Refracted](environment-tab.html#advanced-background) background.
스튜디오 조명 기본 설정에서는 HDR 이미지를 하늘로 사용합니다. 스튜디오 조명을 실내 환경이라고 생각한다면, HDR 이미지를 해당 이미지에 있는 색을 기반으로 빛을 발산하는 천장이라고 생각할 수 있습니다.

### 이미지
HDR 이미지 파일을 지정합니다.
![images/hdrimage-001.png](images/hdrimage-001.png)

### 강도
HDR 이미지 조명의 밝기를 수정합니다.
 **Note** : This setting only matters if there are other lights in the scene that have to be compensated for. If there are no other lights, the tone operator will compensate the exposure and the rendered image will not be brighter or dimmer based on this setting.
![images/hdrlightintensitylow.png](images/hdrlightintensitylow.png)
*Low and high HDR intensity.*
{% include_relative snippets/snippet-rotatehdrimage.md %}In the illustration, the image has been rotated so the reflection of the sun appears on the object. Enter rotation degrees or interactively move the rotation widget indicator.
![images/hdrlightrotation2.png](images/hdrlightrotation2.png)
*Image rotated so the sun appears on the object.*

### Saturation
빛의 채도입니다. HDR 이미지의 빛은 이미지에 있는 픽셀의 색이므로 때때로 원치 않는 효과를 얻을 수도 있습니다. 이미지에서 색이 아니라 빛을 얻으려면 채도를 낮게 설정하십시오.
![images/hdrlightsaturation0.png](images/hdrlightsaturation0.png)
*Low (left) and high (right) saturation.*
{% include_relative snippets/snippet-mirrorimage.md %}{% include_relative snippets/snippet-skychannel.md %}
## Automatic Sky
{: #automatic-sky}
Automatic sky uses settings from the [Sun tab](sun-and-sky-tabs.html) to specify the location of the sun and its intensity.
![images/sky-002.png](images/sky-002.png)
*Automatic sky: sun high (left) and low (right) in the sky.*

### Cloudiness
{: #sky-cloudiness}
When **Cloudiness** is turned off, strong shadows are created. The greater the cloudiness, the less contrast there will be between the light and shadows.
The **Cloudiness** setting affects many aspects of the daylight calculation, including the relative amounts of direct vs. indirect lighting, the way indirect lighting is calculated, and the background color if **Automatic Sky** mode has been selected. The **Cloudiness** setting varies from 0 (clear) to 1 (completely overcast).
![images/cloudiness0.png](images/cloudiness0.png)
*Cloudiness 0 (left) and 1 (right).*

### Sky intensity
{: #sky-intensity}
하늘 (간접) 주광 구성 요소의 밝기를 수정합니다. 천공광(skylight)의 강도는 태양 각도와 하늘 조건을 기반으로 자동으로 계산되지만 수정할 수 있습니다.
 **Note** : This setting only matters if there are other lights in the scene that have to be compensated for. If there are no other lights, the tone operator will compensate the exposure and the rendered image will not be brighter or dimmer based on this setting.
{% include_relative snippets/snippet-skychannel.md %}&#160;

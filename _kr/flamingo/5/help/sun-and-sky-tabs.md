---
title: Sun and Sky
---

# ![imagessun.svg](images/sun.svg) {{page.title}}
The [Sun](#sun) and [Sky](#sky) are closely related to each other. The Sun can change the brightness of the Sky in Automode. If the Sun is on and the Sky is an HDRI balancing their strengths is important.

## 태양
{: #sun}
The Sun is a powerful invisible parallel light. Factors simulating real-world conditions such as latitude and longitude, time of day, and season control the Sun's direction and brightness.

This help topic reviews the Flamingo Sun control.  The [Rhinoceros Sun](http://docs.mcneel.com/rhino/5/help/en-us/commands/sun.htm) control may also be used to place the sun.  Flamingo will keep the two sun controls in sync.

##### Where can I find Flamingo Sun control?

The Sun must be activated through the [Lighting Preset](lighting-tab.html#lighting-presets) or the [Custom Lighting settings](lighting-tab.html#sun).

* ![images/options.png](images/options.png)Toolbars >![images/flamingo-icon.png](images/flamingo-icon.png)Flamingo nXt Toolbar
* ![images/menuicon.png](images/menuicon.png)Menus > Flamingo nXt 5.0 Pulldown > Show Control Panel > Flamingo nXt Tab > Sun

**안내:** 조명 기본 설정에서 태양이 활성화된 경우에만 태양 탭이 표시됩니다.

태양빛을 계산하려면 태양 각도가 필요합니다. 태양의 방향을 지정하는 방법에는 2 가지가 있습니다. 날짜/시간/장소로 결정하는 방법과 직사광선의 각도로 지정하는 방법이 그것입니다. 날짜, 시간, 장소를 사용하여 모델이 위치한 부지에서 실제 태양을 시뮬레이션합니다. 태양 직사광선의 각도는 실제 태양을 참조하지 않고 빛의 각도를 제어합니다. 직사광선 각도를 사용하여 조명 효과를 시험해 보세요.

![images/sydneymorning.png](images/sydneymorning.png)  ![images/stockholmmorning.png](images/stockholmmorning.png)
*Sydney, Australia, 21-June, 09:30 (on the left). Stockholm, Sweden, 21-June, 09:30 (on the right).*

### Set azimuth and altitude
{: #set-azimuth-and-altitude}
Use solar angles to manually set the sun's direction. Enables [Azimuth](#azimuth) and [Altitude](#altitude) controls.

#### 방위각
{: #azimuth}
Sets the sun's direction in angle degrees from North (0) in the horizontal plane.  The circular map shows the world in a plan view.

#### 고도
{: #altitude}
Sets the sun's height in the sky in angle degrees from the Equator (0).  The half circle map simulates a section through the vertical direction of the world coordinates.

### Set location on Earth
{: #set-location-on-earth}
Use the sun angle calculator to place the sun based on Date, Time, Location.  **Note:** As with all Sun calculators, the Sun position accuracy may vary. If absolute accuracy is required it is recommended to verify the sun location.  

#### Date
{: #date}
날짜를 지정합니다.

#### 시간
{: #time}
현지 시각을 지정합니다.

#### Daylight savings time
{: #daylight-savings-time}
시간을 한 시간 앞당깁니다.

#### Latitude/Longitude
{: #latitude-longitude}
위도와 경도를 입력하거나 지도에서 위치를 지정합니다.
The numbers will also update to display the latitude and longitude of a location picked on the map with the mouse cursor.

#### Time zone
{: #time-zone}
Displays the time zone based on Latitude and Longitude for the current location.

#### City list
{: #city-list}
Use this to select a major city to set the location.

#### Map
{: #map}
Click the map to specify a location. Drag with the left mouse button to pan the map.

### Sun intensity
{: #sun-intensity}
Modifies the brightness of the sun (direct) daylight component. The intensity of sun is automatically calculated based on solar angles and sky conditions, but can be modified to balance with other lights.

### Sun highlight
{: #sun-highlight}
태양 하이라이트의 선명도입니다.

![images/sunhighlight-0.png](images/sunhighlight-0.png)
*Sun highlight=0 (left) and 1 (right).*

**Note:** Solar highlight artifacts can sometimes be seen on exterior renderings when the Sun highlight setting is used. To mitigate or eliminate this artifact, set the Sun highlight to a smaller value.
{: #speckle-artifacts}

{% include_relative snippets/snippet-sunchannel.md %}

#### North Direction
{: #north}
**안내:** 북쪽은 절대좌표 Y 방향입니다.

## 하늘
{: #sky}
The Sky is a large sphere around the rendering that can be used for lighting. The Sky is very different from environment.  Sky controls lighting. Environment controls what is reflected and visible in the background. There are many situations where the Sky and Environment might be set differently.

#### Flamingo 하늘 제어는 어디에 있습니까?
The Sky must be activated through the [Lighting Preset](lighting-tab.html#lighting-presets) or the [Custom Lighting settings](lighting-tab.html#sky).

 1. ![images/options.png](images/options.png)Toolbars >![images/flamingo-icon.png](images/flamingo-icon.png)Flamingo nXt 도구모음
 1. ![images/menuicon.png](images/menuicon.png)Menus > Flamingo nXt 5.0 Pulldown > Show Control Panel > Flamingo nXt Tab > Sky

The lighting preset schemes for [Exterior](lighting-tab.html#exterior-daylight) and [Interior](lighting-tab.html#interior-daylight) daylight use the Automatic sky by default. The [Studio](lighting-tab.html#studio-lighting) lighting preset scheme uses HDR image lighting by default.

Sky can be set five ways:

>[Off](lighting-tab.html#off)
>[Automatic Sky](#automatic-sky)
>[High Dynamic Range Image (HDRI)](#high-dynamic-range-image-sky)
>[Color](#color-sky)
>[Image](#image-sky)

The two best settings for sky lighting types are [HDR image](#high-dynamic-range-image-sky) sky and [Automatic sky](#automatic-sky). HDR image sky uses an image with lighting values stored on each pixel to provide light and reflection. Automatic sky uses a real-world sun location and cloudiness to simulate a sky.  These settings will produce the most dynamic renderings.

### Automatic Sky
{: #automatic-sky}
Automatic sky uses settings from the [Sun tab](sun-and-sky-tabs.html) to specify the color range and intensity of the skylight.  For instance, when the sun is high in the sky, the lighting and colors of the sky are very different than when the sun is low in the sky.

![images/sky-002.png](images/sky-002.png)
*Automatic sky: sun high (left) and low (right) in the sky.*

#### Cloudiness
{: #sky-cloudiness}
When Cloudiness is turned off, the sky is considered clear and strong shadows are created. The greater the cloudiness, the less contrast there will be between the light and shadows. Greater cloudiness will create lighter shadows and a more even lighting effect. The Cloudiness setting affects many aspects of the daylight calculation, including the relative amounts of direct vs. indirect lighting, the way indirect lighting is calculated, and the background color if Automatic Sky mode has been selected. The Cloudiness setting varies from 0 (clear) to 1 (completely overcast). The cloudiness settings around 0.35 - 0.50 is a very sensitive and dynamic range.

![images/cloudiness0.png](images/cloudiness0.png)
*Cloudiness 0 (left) and 1 (right).*

#### Sky intensity
{: #sky-intensity}
Modifies the brightness of the sky (indirect) daylight component. The intensity of skylight is automatically calculated based on solar angles and sky conditions, but can be modified. **Note:** This setting only matters if there are other lights in the scene that have to be compensated for. If there are no other lights, the tone operator will compensate the exposure and the rendered image will not be brighter or dimmer based on this setting.

{% include_relative snippets/snippet-skychannel.md %}

### High-Dynamic-Range Image Sky
{: #high-dynamic-range-image-sky}
A [high-dynamic-range (HDR or HDRI)](https://en.wikipedia.org/wiki/High-dynamic-range_imaging) image is a special 2-D image file. These images contain a much broader range of values at each pixel then standard image files, such as a .jpg or .png. This extra data can be used to light models. If the values contained in the HDR are accurate, then the lighting will be accurate. This can produce very dynamic lighting in a scene. The preset Studio Lighting scheme uses HDR images for the sky. If you are thinking of studio lighting as an indoor activity, think of the HDR image as a ceiling that emits light based on the colors in the image.

![images/lighting-001.png](images/lighting-001.png)
*HDRi lighting.*

It is assumed that HDR images contain radiance values expressed in watts units. If this is not the case, the intensity of these HDR images may need to be adjusted in order to achieve proper illumination levels.

In addition to the Sky, a different HDR image can be used for each of the three visible backgrounds: [Visible](environment-tab.html#advanced-background), [Reflected](environment-tab.html#advanced-background), and [Refracted](environment-tab.html#advanced-background) background.

#### HDRI 이미지
Specifies the HDR (HDR and HDRI are the same file type) image file. Click on the image to select a different HDRI.

![images/hdrimage-001.png](images/hdrimage-001.png)
*Equarectangular projection.*

HDR images come in two projection types which let the image to properly wrap around the sky sphere. The most popular is equirectangular.  These images are rectangular with an aspect ratio of 2:1. Equirectangular images will have similar resolution over the whole image. The second projection is spherical. Spherical HDRI images are square in aspect ratio and the image will show great curvature. Spherical projections have less resolution at the seam.

#### Intensity
Modifies the brightness of the HDR image light. This setting only matters if there are other lights in the scene that have to be compensated for. If there are no other lights, the tone operator will compensate the exposure and the rendered image will not be brighter or dimmer based on this setting.

![images/hdrlightintensitylow.png](images/hdrlightintensitylow.png)
*Low and high HDR intensity.*

{% include_relative snippets/snippet-rotatehdrimage.md %}In the illustration, the image has been rotated so the reflection of the sun appears on the object. Enter rotation degrees or interactively move the rotation widget indicator.
![images/hdrlightrotation2.png](images/hdrlightrotation2.png)
*Image rotated so the sun appears on the object.*

#### Saturation
빛의 채도입니다. HDR 이미지의 빛은 이미지에 있는 픽셀의 색이므로 때때로 원치 않는 효과를 얻을 수도 있습니다. 이미지에서 색이 아니라 빛을 얻으려면 채도를 낮게 설정하십시오.

![images/hdrlightsaturation0.png](images/hdrlightsaturation0.png)
*Low (left) and high (right) saturation.*

{% include_relative snippets/snippet-mirrorimage.md %}

{% include_relative snippets/snippet-skychannel.md %}

### 색
{: #color-sky}
It is possible to use a color or gradient of color to light the scene. The colors in the sky are multiplied by the intensity value to give the colors a lighting value.

#### Intensity
The Intensity value is used to multiply the colors in the Sky and result in a lighting value.  Colors can range from 0 - 256 per channel. Intensity will multiply those values.

#### Color type
There are three ways to control the color of the sky.  These are similar to the Color Environment controls.  See [Color Background](environment-tab.html#environment-color-and-gradient-backgrounds) controls for more information.

### 이미지
{: #image-sky}
It is possible to use an image to light the scene. The colors in the image are multiplied by the intensity value to give the colors a lighting value.

#### Intensity
The Intensity value is used to multiply the colors in the Sky and result in a lighting value.  Colors can range from 0 - 256 per channel. Intensity will multiply those values.

#### Image Projection
There are many ways to control how an image is mapped to the sky.  These are similar to the Image Background controls.  See [Image Background](environment-tab.html#environment-image) controls for more information.

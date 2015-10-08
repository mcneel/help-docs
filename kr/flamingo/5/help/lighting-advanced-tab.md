---
---


# Lighting: Advanced

### Sun
{: #sun}
태양은 모델로부터 무한히 떨어져 있는 매우 밝은 방향성 광원입니다.

#### On/Off
태양을 켜고 끕니다.
![images/lightsunon.png](images/lightsunon.png)Sun on and off.

### 하늘
{: #sky}
모델로부터 끝없이 떨어져 있는 반구형의 광원을 정의합니다.

#### Off
하늘을 끕니다.
![images/chromenosky.png](images/chromenosky.png)

#### Auto
{: #auto}
Provides an analytical model based on real-world sky conditions. The settings on the [Sun](sun-and-sky-tabs.html) tab control the appearance and light qualities of the sky.
![images/chromeautosky.png](images/chromeautosky.png)

#### HDRi
{: #hdri}
HDR 이미지는 반짝거리는 이미지에 반사되는 형상을 제공합니다.
![images/chromehdrbackground.png](images/chromehdrbackground.png)

#### Color
{: #color}
Sets the sky to a solid color or a two- or three-color gradient using controls similar to [Environment: Color and Gradient Backgrounds](environment-tab.html#color-and-gradient-backgrounds).
![images/colorsky.png](images/colorsky.png)

#### 이미지
{: #image}
Uses an image background with a planar, cylindrical, or spherical projection similar to [Environment: Image](environment-tab.html#image).
![images/chromeimagesky.png](images/chromeimagesky.png)

### Studio Brightness
{: #studio-brightness}
Reduces the brightness of the [sun](sun-and-sky-tabs.html) and sky to mimic the interior lighting levels of a photographer's studio.
![images/studiobrightnessoffandon.png](images/studiobrightnessoffandon.png)Studio Brightness off (left) and on (right).

### Lights
{: #lights}

#### On/Off
인공 조명을 켜거나 끕니다.
![images/lightsonandoff.png](images/lightsonandoff.png)Lights on (left) and off (right).

## Indirect
{: #indirect}
서피스로부터 반사된 조명을 정의합니다. 기본적으로 실내 조명에는 켜져 있는 상태이며, 실외 및 스튜디오 조명 기본 설정에서는 꺼져 있는 상태입니다. 실외 렌더링에 간접 조명을 켜고 사용할 수 있습니다.

#### Method
간접 조명의 계산 방식을 설정합니다.

#### Off
간접 조명 계산을 끕니다.

#### Interior
{: #interior}
실내 상황에 맞는 간접 조명으로 최적화합니다.

#### Exterior
{: #exterior}
실외 상황에 맞는 간접 조명으로 최적화합니다.
다른 표면에서 반사된 간접 조명은 실외 렌더링에 보다 섬세하고 사실적인 느낌을 부여합니다. 특히, 간접 조명을 사용하여 지붕의 처마, 발코니처럼 돌출된 부분의 아래쪽을 더욱 정확하게 렌더링할 수 있습니다.

#### Bounces
{: #bounces}
간접 조명으로 인해 반사되는 횟수를 지정합니다.

#### Color Bleed
{: #color-bleed}
각각의 간접 바운스와 연관된 색이 변환되는 양을 지정합니다.

### Ambient
{: #ambient}
Ambient light is a constant light added to the rendering. These settings control&#160;the intensity of the ambient light as a percentage of the total estimated ambient light in the scene.
주변광의 양을 줄이면 이미지의 명암이 더욱 짙어집니다. 주변광을 지나치게 높이면 렌더링된 이미지가 단순하고 재미없어 보일 수 있습니다. 주변광이 너무 낮으면 명암이 과도하게 표현됩니다.

#### None
주변광 없음.

#### Exterior
주변광을 실외 설정에 맞춰 최적화합니다.

#### Interior
주변광을 실내 설정에 맞춰 최적화합니다.

#### Studio
주변광을 스튜디오 설정에 맞춰 최적화합니다.

### Monte Carlo reflections
{: #monte-carlo-reflections}
Tries to resolve blurry reflections containing small, bright areas. This is normally slower than the standard reflection algorithm. See: [Wikipedia article: Monte Carlo method](http://en.wikipedia.org/wiki/Monte_Carlo_method).

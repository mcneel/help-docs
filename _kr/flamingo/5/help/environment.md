---
title: Flamingo 환경
---

# ![images/environment.svg](images/environment.svg) {{page.title}}
<!-- TODO: Is it "... environments in Rhino" or "in Flamingo" in the following sentence? -->
Rhino에는 다양한 유형의 환경이 있습니다. 이 항목에서는 Flamingo의 기본 환경에 대해 설명합니다.

The Environment effects the visible part of the background and reflections.  For effects that effect lighting the scene, see the [Sky](sun-and-sky-tabs.html) help topic.

Flamingo comes with a special environment called **Default Flamingo Environment**.  This environment will sync to the current [Lighting Preset](lighting-tab.html). By using [lighting presets](lighting-tab.html), both the Lighting and Environment will be set to appropriate scene defaults.

The complete set of property groups in the Flamingo Environment are:

> [이름](#name)
> [Flamingo 환경](#environment)
> [배경색](#color-backgrounds)
> [고급 배경](#advanced-background-reflected-sky)


## 환경 이름
{: #name}
This is the name of the environment in the Rhino model.  Environments are stored in the Rhino model. That means that the same name in the library or a different model will not be affected by edits to the environment in the current model. To use any environment in another model it must be exported to the [Library](libraries.html) first. The Name of the environment will also serve as its exported file name.

## Flamingo 환경
{: #environment}
There are three major effects of environment in a rendering:

>보이는 배경
>[반사된 배경](#advanced-background-reflected-sky)
>[굴절된 배경](#advanced-background-refracted-sky)

<!-- TODO: Does the following sentence make sense? Is there something missing? -->
The Visible Background is the basic general properties panels and is the visible environment. The [Reflective](#advanced-background-reflected-sky) and [Refractive](#advanced-background-refracted-sky) backgrounds can differ and are available in the Advanced Background section.

#### Intensity
{: #background-intensity}
<!-- TODO: Color range normally is from 0-255... -->
Modifies the relative brightness of the background. The Intensity value is used to multiply the colors in the background and result in a lighting value.  Colors can range from 0 - 256 per channel. Intensity will multiply those values.  This becomes important if the background looks very dark compared to the rendered model.

#### 배경 유형
{: #background-type}
Specifies the color scheme that will fill the background of the rendered image. Backgrounds can be the following types:

> [하늘](#environment-sky)
> [단색과 그라데이션](#color-backgrounds)
> [이미지](#environment-image)
> [HDR과 평면형 HDR 이미지](#hdr-background)


## 하늘 배경
{: #environment-sky}
The Sky environment uses the sun and sky settings from the [Lighting](lighting-tab.html) tabs for settings.  It is the default setting for the renderings that see the sky in the renderings.

![images/background-sky-001.png](images/background-sky-001.png)
*자동 (왼쪽), HDR 이미지와 태양 (오른쪽).*

## 컬러 배경
{: #color-backgrounds}
Background color controls are always present. There is always a color background even if the color is completely obscured by an image, HDRI, or Sky background.

#### 단색
{: #solid-color}
단색 배경은 배경이 하나의 색으로 채워져 있습니다.

![images/background-color-001.png](images/background-color-001.png)
*단색 배경.*
See [Color Controls](#enviroment-sky-color-controls) below for more details on editing the Solid Color.

#### 2색 그라데이션
{: #two-color-gradient}
Two- and three-color gradient backgrounds only apply to perspective views. Two-color gradient backgrounds interpolate the background color between two selected colors.

![images/background-color-002.png](images/background-color-002.png)
*2색 그라데이션 배경: 파랑과 노랑.*
See [Color Controls](#enviroment-sky-color-controls) below for more details on editing a two-color gradient.

#### 3색 그라데이션
{: #three-color-gradient}
3색 그라데이션 배경은 선택된 3색의 단계적 변화로 배경을 표시합니다.
![images/background-color-003.png](images/background-color-003.png)
*3색 그라데이션 배경: 파랑, 흰색, 노랑.*
See [Color Controls](#enviroment-sky-color-controls) below for more details on editing the Three-color Gradient.

### 색 제어
{: #enviroment-sky-color-controls}
The number of controls available  may change based on the Color Background type that is currently selected. Gradient backgrounds will have up to three color selectors that may include a top, middle, and bottom color.

{% include_relative snippets/snippet-material-color-select.md %}

#### 색 바꾸기
Use this button to rearrange the color in the gradient from top to bottom

#### 그라데이션 매핑 제어
{: #gradient-mapping}
The colors in a gradient color background need to be mapped to the environment sphere. The Gradient mapper is used to do this.  The Gradient mapping controls will activate only when a two- or three-color gradient is selected. Gradients can only be mapped to perspective views.

#### 뷰로부터의 각도
{: #angle-from-views}
If Angles from View are checked, the current color gradient will sync with the current rendered perspective view.  The top color will map to the top of the view and the bottom color will map to the bottom of the view.  All other colors will evenly distribute between those extremes.

#### View Altitude Mapper
{: #colorrange}
현재 뷰포트가 투시 투영인 경우, 위 아래 색과 뷰와 관련된 그라데이션의 범위는 제어할 수 있습니다.

![images/background-color-004.png](images/background-color-004.png){: style="float: left; padding-right: 25px;padding-bottom: 15px;padding-top:15px;"}

* The control shows the environment in section view.  The 90 degree marker is the Z-up coordinate. The 0 coordinate represents the horizontal ground plane. The -90 degree marker is the Z-down coordinate.
* The grey cone of vision shows the last coordinates of the current perspective view.
* The Red arrow represents the location of the top color. At this angle and above will be the top color.
* The Green double-arrow represents the middle of the gradient blend between the top and bottom colors.  If it is a three color gradient this is also the location of the middle color.
* The Blue arrow represents the location of the bottom color.  Below this angle there will only be bottom color.

####  Get angles from View Button
Use this button to reset the Gradient mapping control to the current perspective view coordinates.

#### Top/Middle/Bottom Angles
These are angle readouts of the Top, Middle, and Bottom colors in the current gradients.  They correspond to the location of the Red, Green, and Blue arrows in the View altitude mapper.

## Image Background
{: #environment-image}
<!-- TODO: "A digital photograph, a scanned artwork, or an image created with an electronic paint program may be used as the image." doesn't sound very 2015-ish... -->
A background image is projected onto the background. Many times this is used to place a model in an existing context or set a view out some windows. A digital photograph, a scanned artwork, or an image created with an electronic paint program may be used as the image. For best results, use high-resolution images for background images. It is also a good idea to blur and lighten sharp images to simulate natural focus and aerial perspective. The background image can be mapped to the background in a planar, cylindrical, or spherical projection into the scene.

![images/background-image-001.png](images/background-image-001.png)
*A planar image set as a background.*

### 이미지 파일
{: #image-properties}
Set the background image by clicking on the large button that reads *(empty - click here to assign)*, then select a bitmap.  To assign a different image, click on the button thumbnail image.

### 투영
{: #backgroud-image-projection}
Select one of three image projections from the drop-down control:

>[평면형](#planar)
>[원통형](#cylindrical)
>[구형태](#spherical)

Each projection method has its own set of controls for positioning the image.

<!-- TODO: The hierarchy of the following section is inconsistent. "Planar Projection", "Cylindrical Projection" and "Spherical Projection" should be parent elements of the  respective following topics like "Angle from View", "Image Placement Control" etc. -->

#### Planar Projection
{: #planar}
Projects the image to a flat background in the current view. The planar projection coordinates are always relative to the current view.

![images/projectiontypesplanar.png](images/projectiontypesplanar.png)

#### 뷰로부터의 각도
The angle from view checkbox will keep the image in sync with the current view.  This will stretch the image to fit the current view.

#### 이미지 배치 제어
Use the placement control to place the image relative to the current view. The viewport shape shows up as a dark grey rectangle. Drag the pink rectangle or use the numerical controls to move or scale the background image relative the view.

![images/background-image-003.png](images/background-image-003.png)
*현재 뷰포트 영역 (1), 이미지 크기와 형태 (2).*

#### X 방향 크기 / Y 방향 크기
Specifies the size of the background image in the 0 - 1.0 scale of the view width and height. For instance a value of 1.0 is 100% of the view size, a value of 0.5 is 50 % of the view width, etc...

#### X 간격띄우기 / Y 간격띄우기
Specifies the offset of the background image from the lower left corner of the viewport in a 0 - 1.0 scale of the view width and height. For instance a value of 0.25 is offset 25% of the view size, a value of 0.5 is 50 % of the view width, etc...

#### 이미지 배치 제어
Use the placement control to place the image relative the to current view. The viewport shape shows up as a dark grey rectangle. Drag the pink rectangle or use the numerical controls to move or scale the background image relative the view.

![images/background-image-003.png](images/background-image-003.png)
*현재 뷰포트 영역 (1), 이미지 크기와 형태 (2).*

#### X 방향 크기 / Y 방향 크기
Specifies the size of the background image in the 0 - 1.0 scale of the view width and height. For instance a value of 1.0 is 100% of the view size, a value of 0.5 is 50 % of the view width, etc...

#### X 간격띄우기 / Y 간격띄우기
Specifies the offset of the background image from the lower left corner of the viewport in a 0 - 1.0 scale of the view width and height. For instance a value of 0.25 is offset 25% of the view size, a value of 0.5 is 50 % of the view width, etc...

#### 원통형 투영
{: #cylindrical}
원통형 투영은 모델을 둘러싸고 있는 상상 속의 원통에 이미지를 매핑합니다. 이 투영 방법은 실제로 원통형인 이미지에 가장 적합하지만, 사진을 기반으로 구성된 일반적인 파노라마에도 잘 적용됩니다.

![images/projectiontypescylindrical.png](images/projectiontypescylindrical.png)
이미지 맵의 높이와 너비 각도의 크기 및 위치를 지정합니다. 그래픽 도구와 마우스를 사용하여 이미지의 위치와 크기를 지정합니다. 현재 원뿔형 표시기는 옅은 회색으로 음영 처리된 영역으로 표시됩니다.

#### 뷰로부터의 각도
The angle from view checkbox will keep the image in sync with the current view.  This will stretch the image to fit the current view.

#### 평면 제어
이미지 맵의 각도 너비를 지정합니다. 각도를 입력하거나, 제어 위젯에서 플래그를 끌어 너비를 지정합니다. 파란색 영역은 각도 너비 범위를 나타냅니다.

![images/cylindricalcontrol-001.png](images/cylindricalcontrol-001.png){: .float-img-left}

* The control shows the environment in plan view.
* The dark grey cone of vision shows the last coordinates in the current perspective view.
* The blue cone shows the range of angles the image will be visible.
* The blue arrow represents the left coordinate of the image map.
* The red dot represents the middle of the background image.
* The purple arrow represents the right coordinate of the image map.

#### Vertical control
{: .clear-img}
Specifies the vertical extents of the cylindrical projection. Enter an angle or drag the flags in the control widget to set the top and bottom angles. The cylindrical projection is limited to 45 degrees above or below the horizon.

![images/background-cylinder-001.png](images/background-cylinder-001.png){: .float-img-left}

* The control shows the cylinder in section view.
* The grey cone of vision shows the last coordinates in the current perspective view.
* The blue arrow represents the bottom border of the image map.
* The red arrow represents the top border of the image map.

#### 회전
{: .clear-img}
이미지의 회전을 지정합니다. 빨간 점은 이미지의 중심을 나타냅니다.

#### 너비
Specifies the width of the image in degrees relative the the plan view.

#### 위/아래
Specifies the vertical angles of the image based on horizontal groundplane direction in the model

####  뷰와 일치하는 각도 설정 단추
Sets the rotation angle to match the current perspective viewport.  Good for resetting the values of the projection.

#### 구형태 투영
{: #spherical}
구(球) 형태 투영은 이미지를 완전한 구체로 매핑합니다. 이 방식은 일반적으로 등장방형인 구 형태 이미지를 사용할 때 좋은 결과물을 만들어냅니다. 등장방향 이미지는 2:1 직사각형 종횡비를 갖습니다.

#### 뷰로부터의 각도
The angle from view checkbox will keep the image in sync with the current view.  This will stretch the image to fit the current view.

#### Spherical control
Specifies the direction of the image map. Enter an angle or drag the flag in the control widget to set the width. The red dot represents the middle of the background image.

#### 회전
{: .clear-img}
이미지의 회전을 지정합니다. 빨간 점은 이미지의 중심을 나타냅니다.

####  뷰와 일치하는 각도 설정 단추
Sets the rotation angle to match the current perspective viewport.  Good for resetting the values of the projection.

## HDRI 배경
{: #hdr-background}
HDR 이미지를 환경으로 사용하면 조명과 배경의 관계 그리고 이미지에 있는 다른 조명을 보다 상세하게 설정할 수 있습니다. 이 옵션은 밝은 실외가 창으로 보이는 실내 공간을 표현할 때 특히 유용합니다. HDR 환경 이미지는 일반적인 비트맵 이미지보다 훨씬 넓은 범위의 빛 정보를 가지고 있으며, 채널을 적용할 수 있어 [다중 채널](lights-tab.html#channel) 렌더링에서 명암을 관리할 수 있습니다.

#### 이미지 파일
{: #hdri-image}
Set the background HDRI image by clicking on the large button that reads *(empty - click here to assign)*, then select a bitmap.  To assign a different image, click on the button thumbnail image.

{% include_relative snippets/snippet-rotatehdrimage.md %}
{% include_relative snippets/snippet-mirrorimage.md %}
{% include_relative snippets/snippet-sunchannel.md %}
{% include_relative snippets/snippet-skychannel.md %}

## 평면형 HDRI 옵션
{: #planar-hdr-options}

Planar high-dynamic-range images are seldom used, but can be very useful.  And HDRI provides a wider range of color possibilities. A good use of planar HDRI files is used outside windows in architectural renderings where the background may be too light or too dark.  Planer HDRI files are always mapped planar.


![images/planarimagebeach.png](images/planarimagebeach.png)
*배경 이미지 (왼쪽)와 평면형 HDR (오른쪽)을 비교하면 배경에서의 은은한 조명의 차이를 알 수 있습니다.*

#### 이미지 파일
{: #hdri-planar-image}
Set the background HDRI image by clicking on the large button that reads *(empty - click here to assign)*, then select a bitmap.  To assign a different image, click on the button thumbnail image.
{% include_relative snippets/snippet-sunchannel.md %}
{% include_relative snippets/snippet-skychannel.md %}

## 고급 배경
{: #advanced-background}
The Advanced Background settings control environments that are not visible in the rendering, but show in reflections and refractions for the objects. This lets the visible environment look one way, while reflections and refractions might be reacting to a different environment.  For instance, in the illustration below the background is black, but the reflected environment is an HDR image of a building interior.

![images/reflectedbackground-002.png](images/reflectedbackground-002.png)
*보통 환경 (왼쪽), 반사된 HDR 하늘 환경 (오른쪽).*

### 반사됨
{: #advanced-background-reflected-sky}
반사된 환경은 렌더링된 이미지에는 보이지 않으나 반짝거리는 개체에 반사되어 보입니다.

#### 하늘
[조명: 태양과 하늘](sun-and-sky-tabs.html) 설정에서 지정된 대로 개체에 하늘이 비춰집니다.

#### 사용자 지정
Objects reflect a [Color or gradient](#color-backgrounds), [Image](#environment-image), or [HDR](#hdr-background) background.

#### 보이는 배경
[환경](environment-tab.html) 설정에서 지정된 상태로 보이는 배경이 개체에 비춰집니다.

### 굴절됨
{: #advanced-background-refracted-sky}

#### 하늘
[조명: 태양과 하늘](sun-and-sky-tabs.html) 설정에서 지정된 대로 개체가 하늘을 굴절시킵니다.

#### 사용자 지정
Objects refract a [Color or gradient](#color-and-gradient-backgrounds), [Image](#image), or [HDR](#hdr-background) background.

#### 보이는 배경
[환경](environment-tab.html) 설정에서 지정된 상태로 보이는 배경이 개체에 굴절됩니다.

#### 투명한 개체 알파 없음
{: #no-transparent-alpha-objects}
투명한 개체를 통해 알파 채널이 보이는 것을 방지하고, 투명한 개체를 통해 알파 채널이 합성되는 것도 방지합니다.
이미지가 알파 채널로 붙여넣기 실행이 된다면 이 설정을 끕니다.

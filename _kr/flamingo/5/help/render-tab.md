---
title: 렌더링 옵션
---

# ![images/flamingotab.svg](images/flamingotab.svg) {{page.title}}
렌더링 탭은 최종 렌더링의 주요 속성을 제어합니다. 이 탭을 사용하여 렌더링에 소요되는 시간과 화질을 제어합니다. 최종 이미지의 해상도는 전반적인 렌더링 시간에 가장 큰 영향을 미치는 요인 중 하나입니다.

안내: 초안 렌더링 단계에서 렌더링 해상도를 낮게 설정하는 것이 좋습니다. 최종 렌더링일 때만 고해상도 렌더링을 사용하세요.

#### Flamingo 조명 제어는 어디에 있습니까?

 1. ![images/options.png](images/options.png)도구모음 >![images/flamingo-icon.png](images/flamingo-icon.png)Flamingo nXt 도구모음 > 렌더링 옵션 탭
 1. ![images/menuicon.png](images/menuicon.png)Menus > Flamingo nXt 5.0 메뉴 > 제어 패널 표시 > Flamingo nXt > 렌더링 옵션 탭


## 렌더링할 뷰포트
{: #viewtorender}
Flamingo nXt 5가 렌더링하는 뷰를 설정합니다. 모델을 작업하며 렌더링할 때 매우 유용한 설정이지만, 특정한 한 뷰를 항상 렌더링해야 합니다. 예를 들어 많은 경우에 Perspective 뷰가 렌더링 대상이 됩니다. 이 드롭다운 메뉴를 설정하면 렌더링을 시작하기 전에 해당 뷰가 현재 뷰로 설정되어 있는지 매번 확인하지 않아도 됩니다.

#### 활성 뷰
현재 활성 뷰를 렌더링하려면 이 옵션을 사용합니다. 이것은 기본 설정입니다.

#### 사용 가능한 뷰포트 목록
모델에 있는 모든 명명된 뷰가 포함된 목록입니다. 항상 렌더링되는 뷰 이름을 선택합니다.

## 렌더링 해상도
{: #resolution}
렌더링 해상도는 가장 중요한 렌더링 설정 중 하나입니다. 이 설정은 이미지 크기와 Rhino 파일에 저장될 해상도를 지정합니다. 해상도를 올리면 기하급수적으로 렌더링 시간이 길어집니다. 따라서 이 설정을 신중하게 지정하는 것이 중요합니다.

#### 전체 픽셀의 수
{: #resolutionimagepixels}
현재 뷰의 높이와 너비 비율을 사용한 최종 렌더링의 전체 픽셀의 수를 설정합니다. 렌더링 작업에 유용한 설정입니다. 현재 뷰를 렌더링에 일치시키기에 가장 좋은 설정입니다. 픽셀의 전체 수를 변경하는 것만으로 쉽게 이미지 해상도를 올리거나 낮출 수 있습니다.

### 뷰포트 해상도
렌더링된 이미지 크기를 결정하기 위해, 픽셀 단위의 뷰포트 크기를 사용합니다. 이것은 뷰포트 종횡비와 해상도의 1대1 재현입니다. 이는 유용한 모드이지만, 전체 화면 뷰포트를 렌더링하는 경우, Rhino 표준 4뷰 설정에서의 화면 1/4 크기의 뷰포트를 렌더링할 때보다 처리 속도가 느려질 수 있습니다.

### 이미지 크기
{: #resolutionprintedsize}
몇 가지 다른 변수를 기준으로 이미지 크기가 최종 해상도를 설정합니다. 이것은 최종 이미지의 정확한 크기와 해상도를 일치시키는 가장 좋은 방법입니다. 최종 렌더링의 높이와 너비가, 렌더링되고 있는 뷰의 종횡비와 일치하지 않는다면 뷰의 위, 아래 또는 옆이 일부 잘릴 수 있습니다. 안내: 이 제어를 사용하여 아주 오랜 시간이 소요될 수 있는 초고해상도 렌더링을 생성할 수 있습니다. 이 제어를 최종 고해상도 렌더링에 사용하세요.

다음과 같은 4개의 단위 유형을 사용할 수 있습니다:

>픽셀
>인치
>밀리미터
>센티미터

#### 픽셀
Sets the render image units to pixels.  Use this setting to simply set the final width and height of the final rendering by the number of pixels.

#### 인치
Sets page units to inches. Inches are used in combination with resolution settings to determine the final resolution of the rendered image.  To determine final resolution, multiple the number of inches in width and height by the resolution DPI value.

#### 밀리미터
Sets the page units to millimeters. Use millimeters in combination with resolution settings to determine the final resolution of the rendered image.  To determine final resolution, multiply the number of millimeters in width and height by the resolution dots per millimeter value.

#### 센티미터
Sets the page units to centimeters. Use centimeters in combination with resolution settings to determine the final resolution of the rendered image.  To determine final resolution, multiply the number of centimeters in width and height by the resolution dots per centimeter value.

#### 뷰 종횡비 적용
Use this setting to keep the width and height setting in the same aspect ratio to the current view.  This will assure the complete view is rendered in the final image.

#### 너비
Printed image width in current unit size.  Multiply this setting by the resolution setting to reach the final image size in total number of pixels.

#### 높이
Printed image height in current size units.  Multiply this setting by the resolution setting to reach the final image size in total number of pixels.

### 해상도
{: #printsizepixelsperunit}
{: #printsizedpi}
{: #printsizeresolution}

#### 표시
The image is rendered using the DPI resolution of the viewport. This is the density of pixels on a devise.  Normally it is expressing the [dots pre inch (DPI)](https://en.wikipedia.org/wiki/Dots_per_inch)

#### 사용자 지정
The image is rendered using a custom resolution. Type the custom width and height resolution in **Pixels per: control**.

#### 프린터, 간단하게 인쇄
해상도를 100 픽셀/인치 또는 4 픽셀/mm로 설정합니다.

#### 프린터, 보통 품질
해상도를 150 픽셀/인치 또는 6 픽셀/mm로 설정합니다.

#### 프린터, 고품질
Set the resolution to 300 pixels per inch or 12 pixels per mm. This is quite a high resolution for rendering.  This works well for smaller renderings, but for large poster or wall size renderings, the overall resolution can get very high with this setting. High resolutions can lead to long rendering times.

#### 단위당 픽셀
When Resolution control is set to Custom, use this control to set the resolution per selected unit. When a preset resolution is selected, this control displays the current resolution.

## 피사계 심도(DOF)
{: #depthoffieldoption}
이 효과는 포토그래퍼의 렌즈를 흉내내는, 피사계 심도(Depth of Field) 흐림 효과를 만듭니다. 렌주는 정확하게 하나의 거리에서만 정확하게 초점을 맞출 수 있으나, 초점 거리 주변의 선명도는 점차 떨어집니다.

#### Enabled
피사계 심도(DOF) 효과를 켭니다.

#### 세기
Controls the size of the focus area. Setting Strength to zero makes the entire image is sharp. Increasing the Strength makes the areas outside the focal distance more blurry and makes the area in focus smaller.

#### 초점 거리
{: #focaldistance}
Sets the distance for the depth of field. The distance around the depth of field point at which objects will be in focus. If the Focal distance is set to ten units, objects about seven units behind the depth of field point and about three units in front of the depth of field point will be in focus.

#### 지정 >>
초점 거리가 되는 한 지점을 모델에서 지정합니다.

## 렌더링 엔진
{: #render-engine}
There are three different render engines within Flamingo.  Each render engine will produce slightly different results in normal rendering conditions.

Flamingo use progressive, multi-step rendering techniques to create renderings.  With progressive steps, as Flamingo does, there can be unfinished artifacts in the rendering at each step. Artifacts are render effects that leave unusual uncompleted effects in a rendering.  Technically all three render engines will result in the the same rendering, given enough time.  But realistically time is always a limiting factor. So, the trick is to select a render engine that will best render the current scene in the least number of steps.

It is very easy to simply select a different render engine and then render to see the results.

### 기본값
The default algorithm produces a very high-quality simulation. The default engine is a good render engine for a wide variety of scenes.  While the other two engines have greater strengths, they also have greater weaknesses.  The Default engine is a good starting point.

The default render engine has a very noticeable artifact in the renderings in the early passes.  The artifact is hard overlapping shadows.  As passes progress these shadows will soften up.  This allows the default engine to return a result quickly, but may take more passes to actually soften the shadows out.

The difference in quality between the default method and the path tracer can be very subtle, particularly if indirect lighting is enabled. The difference in quality may not be worth the extra processing time.

### 경로 추적기
{: #path-tracer}
The path tracer begins by displaying a grainy image that gradually refines and becomes smooth. This process is known as *convergence*. The path tracer can provide a better quality finished product for many models (with a simpler setup), but does so at the expense of a more complex and time-consuming calculation. **Note:** Using the path tracer can cause bright spot or speckle artifacts to occur during the rendering process. These artifacts are normal to the path tracer and will resolve over time.

Certain advanced effects, such as caustics or blurry transmission, can be calculated with better accuracy using the path tracer. Images rendered with instancing, plants, and displacement maps can converge faster. The path tracer is usually easier to set up than the default method. Advanced settings such as reflection shaders, daylight portals, and ambient lighting are not used when the path tracer engine is selected.

Images rendered using the path tracer will generally take longer to converge than images rendered using the default method. Interior daylight simulations, particularly those scenes where the windows are relatively small, may take much longer to finish.

### 하이브리드
The Hybrid engine is an attempt to use the best between the Default engine and the Path Tracer engine.  It uses effects from both.  The hybrid engine will always calculate indirect light.  The artifact of the hybrid is an extensive dot pattern that will reduce over multiple passes. in some situations it may take many passes to remove that dot pattern. For many renderings this may be the best engine to use.

###  **고급**
Opens the Document Properties dialog box at the [Flamingo nXt](documentproperties-flamingo.html) page. There are several advanced rendering properties that can be set here to further customize the final rendering quality.

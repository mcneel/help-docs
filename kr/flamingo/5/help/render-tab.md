---
---


# Render

## Viewport to render
{: #viewtorender}

#### 활성 뷰

#### List of available viewports
명명된 뷰를 포함합니다.

## Rendering resolution
{: #resolution}
이미지의 크기와 해상도는 Rhino 파일에 저장됩니다.

### Total pixels
{: #resolutionimagepixels}
렌더링된 이미지의 전체 픽셀 수를 설정합니다.

### 뷰포트 해상도
렌더링된 이미지 크기를 결정하는 뷰포트 크기를 픽셀 단위로 사용합니다.

### Image size
{: #resolutionprintedsize}

#### Pixels
페이지 단위를 픽셀로 설정합니다.

#### Inches
페이지 단위를 인치로 설정합니다.

#### Millimeters
페이지 단위를 밀리미터로 설정합니다.

#### Width
현재 크기 단위로 인쇄되는 이미지 너비.

#### Height
현재 크기 단위로 인쇄되는 이미지 높이.

#### Resolution
{: #printsizepixelsperunit}
{: #printsizedpi}
{: #printsizeresolution}

#### Display
뷰포트의 픽셀 크기로 이미지가 렌더링됩니다.

#### Custom
사용자 지정 해상도로 이미지가 렌더링됩니다. 사용자 지정 너비와 높이 해상도를 픽셀 단위로 입력합니다.

#### Printer, draft quality
100 픽셀/인치 또는 4 픽셀/mm.

#### Printer, normal quality
150 픽셀/인치 또는 6 픽셀/mm.

#### Printer, high quality
300 픽셀/인치 또는 12 픽셀/mm.

#### Pixels per ___
현재 해상도를 표시합니다.

## 피사계 심도(DOF)
{: #depthoffieldoption}
이 효과는 포토그래퍼의 렌즈를 흉내내는, 피사계 심도(Depth of Field) 흐림 효과를 만듭니다. 렌주는 정확하게 하나의 거리에서만 정확하게 초점을 맞출 수 있으나, 초점 거리 주변의 선명도는 점차 떨어집니다.

### 사용
피사계 심도(DOF) 효과를 켭니다.

### Strength
Controls the size of the focus area. Setting **Strength** to zero makes the entire image is sharp. Increasing the **Strength** makes the areas outside the focal distance more blurry and makes the area in focus smaller.

### Focal distance
{: #focaldistance}
Sets the distance for the depth of field. The distance around the depth of field point at which objects will be in focus. If theFocal distanceis set to ten units, objects about seven units behind the depth of field point and about three units in front of the depth of field point will be in focus.

### Pick
초점 거리가 되는 한 지점을 모델에서 지정합니다.

## Render Engine
{: #render-engine}

### 기본값
기본값 알고리즘으로 매우 높은 퀄리티의 시뮬레이션이 만들어집니다. 기본 방식과 경로 추적기 방식 간의 퀄리티 차이는 매우 미미하며, 특히 간접 조명이 사용 설정되어 있는 경우 그러합니다. 그 차이는 오랜 렌더링 처리 시간을 감수할 만큼은 아니라고 할 수 있습니다.

### Path Tracer
{: #path-tracer}
The path tracer begins by displaying a very grainy image that gradually refines and becomes smooth. This process is known as *convergence*. The path tracer can provide a better quality finished product for many models (with a simpler setup), but does so at the expense of a more complex and time-consuming calculation.
 **Note** : Using the path tracer can cause bright spot or speckle artifacts to occur during the rendering process. These artifacts are normal to the path tracer and will resolve over time.

### Advantages of using the path tracer

>Certain advanced effects, such as caustics or blurry transmission, can be calculated with better accuracy using the path tracer.
>Images rendered with instancing, plants, and displacement maps can converge faster.
>The path tracer is usually easier to set up than the default method. advanced settings such as reflection shaders, daylight portals, and ambient lighting, are not used when the path tracer engine is selected.

### Disadvantages of using the path tracer

>Images rendered using the path tracer will generally take longer to converge than images rendered using the default method. Interior daylight simulations, particularly those scenes where the windows are relatively small, may take much longer.

###  **고급** 
Opens the Document Properties dialog box at the [Flamingo nXt](documentproperties-flamingo.html) page.

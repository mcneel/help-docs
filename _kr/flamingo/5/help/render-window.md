---
title: 렌더링 창
---

# ![images/render.svg](images/render.svg) {{page.title}}
렌더링 창에는 노출을 조정하고 후처리 효과를 더하는 옵션이 있습니다. 렌더링 창의 메인프레임은 Rhino 렌더링 프레임워크의 일부입니다. 렌더링 창 메뉴와 아이콘에 대한 정보는 [렌더링 창 항목](http://docs.mcneel.com/rhino/5/help/ko-kr/index.htm#information/renderwindowpostprocess.htm) 을 참조하세요. 이 항목은 렌더링 과정에서의 Flamingo 설정을 다룹니다.

## 활성 렌더링의 관리
Once the rendering starts, the [Render Windows topic](http://docs.mcneel.com/rhino/5/help/en-us/index.htm#information/renderwindowpostprocess.htm) starts up and the rendering will proceed.  Flamingo is a multi-pass system that updates the rendered image in stages. Flamingo first looks for any changes to its internal model, then starts an initialization process.  This process can take a few seconds or a few minutes.  This is when the model is imported, material bitmaps are collected from the hard drive, and the render image buffer is created. There are some key steps to the process to managing the rendering:

>[다중 패스 렌더링](#multi-pass)
>[렌더링 중지](#stop-render)
>[이미지 조정](#adjusting)
>[이미지 저장](#saving)

### 다중 패스 렌더링
{: #multi-pass}
Flamingo nXt is a completely new rendering engine. Using a method of multi-pass refinement allows more advanced rendering effects without the overhead of a complicated interface. In the first few rendering passes, there will be unusual artifacts.  For instance you will see shadows start out very sharp and linear. With each pass, the shadows will get softer as they blend together. There are many other effects that will also improve with each rendering pass.  Use the [Flamingo Tab](#flamingo-tab) to track the rendering process.

In this way, an nXt rendering is never "finished"; you merely decide when it is good enough to stop. You can let images that look good continue to improve. But, if you want to change or save something, you can also stop an image at any time.

![images/passes-wide-1.gif](images/passes-wide-1.gif)

패스를 향상시키는 효과 중 일부는 다음과 같습니다:

>조명 (전역 발광을 사용할 때)
>부드러운 그림자
>반사 (흐림)
>굴절
>앤티앨리어싱
>피사계 심도(DOF)

### 렌더링을 중단할 때
{: #stop-render}
렌더링을 중단하는 방법에는 몇 가지가 있습니다:

![images/close-x.png](images/close-x.png) Click the “X” button in the upper right of the render window to stop the rendering immediately and close the render window. This is the best method for quickly getting back to the model to make changes.

![images/stop.png](images/stop.png) Click the Stop Raytrace button to stop the rendering at the end of the current pass. This is the best option before saving and image.

![images/stop.png](images/stop.png) Double-click the Stop Raytrace to stop the rendering immediately and leave the render window open.

### 렌더링 조정
{: #adjusting}
After stopping and image, use the controls in the [Flamingo Tab](#flamingo-tab) to quickly adjust the image and lighting. This is a very important set of tools when producing high end images.

이미지 조정에 사용되는 제어:

>[이미지 조정](#adjust-image)
>[채널](#channels)
>[후처리 효과](#post-process-effects)


### 이미지 저장
{: #saving}
There are many ways to save an image depending on the plans for the image.  Normally saving as a JPG or PNG image file is the recommended process for most images.  But there are other options.

#### ![images/saveimageas.png](images/saveimageas.png) 이미지 저장
Saving a JPG or PNG image file is the normal process after adjusting the image.  

A JPG image is a very efficient, small file format.  This is good for images placed on the web or emailed around.  But that efficiency comes at a small price, as some colors are removed from the image.

PNG is a compressed format that contains 100% of the color information and alpha channel information. This is a good format for high quality images.

#### 배경 알파 채널과 함께 저장
{: #save-with-alpha-channel}
Saves image as a 32-bit PNG, TIF, and BMP including alpha channel background. Use the Alpha channel versions of the file formats for high-quality compositing. Backgrounds will appear black when the rendering is saved with Alpha channel.  There is a checkbox on the [Flamingo Tab](#flamingo-tab) and the [Save dialog](#saving) box to successfully save the alpha channel. The PNG file format is the proper format to use to capture the alpha information.

#### 네이티브 Flamingo nXt 파일 (.nXtImage)로 내보내기
{: #export-to-nxtimage}
Saves uncompressed luminance and color information. Saves all rendered channels including [alpha](environment-tab.html#alpha). The nXt Image files can be opened in the [Image Editor](image-editor.html) where [exposure](#adjust-image) and [post-processing effects](#effects) can be applied and the image resaved to another bitmap format.

.nXtImage 형식은 nXt 렌더러의 원시(기본) 이미지 형식입니다. 이 형식을 사용하면 렌더링과 관련된 가장 많은 정보가 저장되므로, 렌더링을 저장 시 권장되는 형식입니다. 이 형식으로 저장된 이미지는 [nXt 이미지 편집기(image-editor.html)(image-editor.html) 에서 조작할 수 있으며, 특수 효과도 추가할 수 있습니다. 또한 nXt에서 지원되는 모든 형식을 비롯한 많은 표준 형식으로 이미지를 저장할 수 있습니다. [Piranesi EPix 파일 (.epx)](http://www.piranesi.co.uk/) 형식으로도 저장할 수 있습니다.

#### HDR 파일로 내보내기
{: #export-to-hdr}
압축되지 않은 휘도와 색 정보를 저장합니다. hdr 형식은 High Dynamic Range 형식에 있는 휘도 데이터를 직접 저장합니다. 일반 사진처럼 휘도가 없는 배경을 이러한 형식으로 저장하면 검정색으로 나타납니다.

#### EXR 파일로 내보내기
{: #export-to-exr}
HDR (high-dynamic-range) 이미지 형식은 Industrial Light and Magic (ILM)에서 무료 소프트웨어 라이선스로 개발한 소프트웨어 툴과 함께 오픈 스탠다드로 릴리스되었습니다. 이 파일 형식은 1 비트 부호, 5 비트 지수(指數), 10 비트 가수(假數)로 채널당 16비트 부동 소수점 값 (절반의 정밀도: half precision)을 지원합니다.  30 스톱 노출의 동적 범위(dynamic range)가 허용됩니다. [Wikipedia 항목: OpenEXR](http://en.wikipedia.org/wiki/OpenEXR)을 참조하세요.
exr 형식은 High Dynamic Range 형식에 있는 휘도 데이터를 직접 저장합니다. 일반 사진처럼 휘도가 없는 배경을 이러한 형식으로 저장하면 검정색으로 나타납니다.

#### ![images/close-x.png](images/close-x.png) 끝내기
렌더링 창을 닫습니다.

#### 메뉴
렌더링 창 메뉴와 아이콘에 대한 자세한 안내는 [렌더링 창 항목](http://docs.mcneel.com/rhino/5/help/ko-kr/index.htm#information/renderwindowpostprocess.htm) 을 참조하세요.

## Flamingo 탭
{: #flamingo-tab}
The Flamingo Tab in the Render window adds many controls specific to the Flamingo render engine.  Understanding these controls is key to managing the active Flamigno renderings.

#### 알파 채널과 함께 저장
Saves 32-bit PNG, TIF, and BMP images including alpha channel background. The Alpha channel versions of the file formats are used for high-quality compositing. Backgrounds will appear black when the rendering is saved with Alpha channel.  Use this checkbox and the [Save dialog](#saving) box to successfully save the alpha channel. The PNG file format is the proper format to use to capture the alpha information.

## 진행률
{: #progress}
Use the Progress information to check the status and progress of a Flamingo rendering.

#### 액션
Shows the current status of the rendering as is works through the model.

상태 안내 메시지는 다음과 같습니다:

* 렌더링이 시작되었습니다 - 일단 렌더링이 시작된 후에는 렌더링을 하기 위해 모델을 전환하고 메모리를 지정하는 일부 설정이 있습니다. 
* 액션 완료 - 중지 단추를 클릭하면 렌더링 엔진이 패스를 완료하고 액션 중지가 실행됩니다.
* Pass Complete - This message posts each time a pass is complete.
* 렌더링 다시 시작 - 다시 시작이 가능한 경우, 이 메시지가 표시됩니다.
* 업데이트하는 중 - 렌더링 엔진이 패스를 처리 중이며, 현재 렌더링을 업데이트하는 중입니다.

#### 패스
This is the current pass Flamingo is rendering.  Flamingo is a multi-pass render engine.  Each pass will refine add lighting effects and refine the complex rendering effects.

#### 스캔 라인
A pass progresses along a stretch of horizontal pixels.  Each row of pixels is a scanline.  This reports the current scanline returned from the render engine.

#### 경과 시간
This is the time that has passed from the beginning of the rendering.  This does not include the setup time for the rendering.

#### 광선 / 초
The number of rays resolved into the scene per second.

#### 픽셀 / 초
The number of pixels resolved in the image per second.

## 이미지 조정
{: #adjust-image}
This is one of the most important controls in Flamingo. Just like a camera, you can adjust image exposure.  This is the best way to make renderings brighter, darker, add contrast, or increase color saturation. This adjustment process is called [tone mapping](https://en.wikipedia.org/wiki/Tone_mapping). Flamingo works in luminance space, a much broader range of colors and brightness than can be shown on a screen or printer.  Tone mapping is the process of converting the luminance data into Red, Green, and Blue (RGB) pixels that can be displayed on a screen or printed. The settings also control how images are saved.

![images/tonefinals-nocorrection.png](images/tonefinals-nocorrection.png)  ![images/tonefinals-correction.png](images/tonefinals-correction.png)
*The default image on the left. The corrected image after applying brightness (0.20), burn (0.16) and saturation (1.20).*
Use this process to quickly adjust the brightness of an image and overall color of an image without needing to re-render.

### 밝기
{: #brightness}
이미지의 전체 밝기를 조정합니다. 예를 들어, 모델에서 하얀 서피스가 회색으로 렌더링되면 서피스가 하얗게 보일 때까지 밝기를 증가시킵니다. 또는, 실외 장면에서 노출이 지나치면 장면이 올바르게 보일 때까지 밝기를 낮춥니다.

![images/brightnessdefault.png](images/brightnessdefault.png)
*기본 밝기 (왼쪽), 밝기 값을 올린 상태.*

{% include_relative snippets/snippet-brightness.md %}

### 번
{: #burn}
Adjusts the image white point. This is the brightest white color in the image. A little burn can add drama, life, and sharpness to a rendering by adding more areas of white to contrast with the dark areas.
[Wikipedia 항목: White point](http://en.wikipedia.org/wiki/White_point)을 참조하세요.

![images/burn-001.png](images/burn-001.png)
*기본 설정 상태의 번 효과 (왼쪽), 증가된 상태.*

### 채도
{: #saturation}
채도는 이미지에서 색의 양(量)를 제어합니다. 채도가 0.00이면 회색조 이미지가 됩니다. 1.00을 초과하는 값은 색을 진하게 만듭니다.

![images/saturationdefault.png](images/saturationdefault.png)
*채도가 기본값일 때 (왼쪽), 약 3으로 증가되었을 때 (오른쪽).*

### 히스토그램
{: #histogram}
Graphically displays the distribution of the light and dark areas in the image after the Adjust images controls are applied. The left edge of the chart are the darks to black.  The right edge shows the amount of light colors to white. This is a great way to determine the important parts of the image. A good goal is to adjust the image to have a full range of values in the image.  For instance, if the histogram stops before getting to the far right of the graph, use more brightness or burn will stretch the values toward the right or bright edge. See: [Wikipedia article: Histogram](http://en.wikipedia.org/wiki/Histogram). The internet has many articles about using histograms to evaluate exposure in digital photography. The principles are the same for rendering.
<!--'Use more brightness or burn will stretch the values' - This needs rewritten.-->

![images/histogram.png](images/histogram.png)
*An example histogram with few dark areas and a large range of light colors.  Although there a few completely white pixels because the graph falls off before the right edge.*

#### 히스토그램 옵션
Right-click the histogram image for the following options.  These options simply change the way the histogram displays the information. They do not actually change the values in the histogram.

* **Fit** - This fits the highest verticals into the chart.
* **Median** - This fits the median value in the vertical. This is a good way to see the details at the edges of the chart.
* **Mean** - This fits the mean value in the vertical direction.
* **Show Sorted Graph** - This sorts all the values based on the amount they exist in the image.
* **Show Scale** - Shows the corresponding values along the bottom of the chart.
* **Graph Color...** - Sets the graph color.

### 노출 잠금
{: #lock-exposure}
노출 설정이 잠겨 있으면, 조명을 변경해도 이에 맞춰 보정되도록 노출이 조정되지 않습니다.

## 렌더링 제한 조건
{: #number-of-passes}
{: #time}
{: #render-constraints}
{% include_relative snippets/snippet-renderconstraints.md %}

## 정보
{: #information}

#### 해상도
현재 [렌더링 해상도](render-tab.html#resolution)를 표시합니다.

#### 면
Displays the number of mesh faces used to render the model.  This a a good value to compare various [render mesh settings](http://docs.mcneel.com/rhino/5/help/en-us/index.htm#documentproperties/mesh.htm) in Rhino.

#### 보이는 면
When there are blocks in the model, Flamingo nXt is able to use the block definition to render block instances without remeshing each instance. The Apparent faces display shows how many more temporary faces would be generated if the block instances did not exist.

#### 조명 정보
This is some information on the current lighting setup of the rendering.  Here is a list of lighting information listed:

>[기본 설정](lighting-tab.html)
>[태양](sun-and-sky-tabs.html#sun)
>[하늘](sun-and-sky-tabs.html#sky)
>[조명](lights-tab.html)
>[간접](lighting-tab.html#indirect)
>[주변광 켜기/끄기](lighting-tab.html#ambient)

## 채널
{: #channels}
Use these controls to change the lights channels in real time. Assign lights to one of eight channels. After you produce the rendering, adjust the lighting in the rendered image. This is a powerful feature when working to balance multiple light sources in a rendering. For more details see the [Rendering Channels](render-channel.html#adjustng-channels) topic.

## 후처리 효과
{: #post-process-effects}
Apply post-processing effects after rendering the image. Turn post-processing effects on and off and reorder in the list. Each effect has its own settings. Effects include:

>안개
>글로우
>글레어
>피사계 심도(DOF)
>Points
>커브
>아이소커브
>주석

특정 필터에 대한 자세한 정보는 [이미지 후처리](http://docs.mcneel.com/rhino/5/help/ko-kr/index.htm#information/renderwindowpostprocess.htm) 항목을 참조하세요.

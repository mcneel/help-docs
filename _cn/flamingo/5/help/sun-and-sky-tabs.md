---
title: 太阳与天光
---

# ![imagessun.svg](images/sun.svg){{page.title}}
[太阳](#sun)和[天光](#sky)之间有非常密切的关系， 如果天光设置为自动，太阳就能够影响天光的亮度，如果太阳打开的情况下，天光设置成了 HDRI，这时就要注意调节它们之间的平衡。

## 太阳
{: #sun}
太阳是一个亮度极高的平行光源，它的设置模拟真实世界的情形，以经纬度、时间、季节等设置控制太阳的方向与照明的亮度。

本主题是对 Flamingo 太阳相关控制的一个综述。也可以使用 [Rhinoceros 太阳](http://docs.mcneel.com/rhino/5/help/en-us/commands/sun.htm)设置日光，Flamingo 会将这两个太阳的设置进行同步。

##### 在哪里可以找到 Flamingo 太阳的控制设置？

太阳必须通过载入[照明预设](lighting-tab.html#lighting-presets)来开启或在[自定义照明设置](lighting-tab.html#sun)中开启。

* ![images/options.png](images/options.png)工具列 >![images/flamingo-icon.png](images/flamingo-icon.png)Flamingo nXt 工具列
* ![images/menuicon.png](images/menuicon.png)功能表 > Flamingo nXt 5.0 下拉菜单 > 显示控制面板 > Flamingo nXt 选项卡 > 太阳

**附注:** 只有在灯光预设中开启太阳后，才能开启太阳选项卡。

太阳的角度是计算太阳照明的必要因素，有两种方法可以设置太阳的角度：一是日期、时间与地点间接设置，也可以用来分析模型在地球的某个位置太阳光的照射情形；一是以方位与高度直接设置，这个方式较为直观，不考虑日期、时间与地点的因素。

![images/sydneymorning.png](images/sydneymorning.png)![images/stockholmmorning.png](images/stockholmmorning.png)
*澳大利悉尼，6月21日早上 9：30
(左图)。瑞典斯德哥尔摩，6月21日早上 9：30(右图)。*

### 设置方位与高度
{: #set-azimuth-and-altitude}
启用[方位](#azimuth)与[高度](#altitude)设置，以手动设置太阳的角度。

#### 方位
{: #azimuth}
设置太阳的方向，北方为0度。选项卡中的圆形图示将地球表示为平面图。

#### 高度
{: #altitude}
设置太阳的仰角，赤道为0度。半圆形图示和指向圆心的向量表示太阳相对于世界坐标垂直方向（地轴）的入射角度。

### 设置地球上的位置
{: #set-location-on-earth}
通过设置地球上的地理位置、时间和日期来计算太阳的角度。**附注:** 和所有的太阳计算器一样，计算出的太阳位置可能有误差。如果要求绝对精确，建议您通过其他途径进一步验证太阳的位置是否准确。  

#### 日期
{: #date}
设置日期。

#### 时间
{: #time}
设置当地的时间。

#### 夏令时
{: #daylight-savings-time}
将时间提前一小时。

#### 经度/纬度
{: #latitude-longitude}
在这两栏输入经度与纬度，或直接在地球上指定位置。
在地球上指定位置时经度与纬度的数值会更新。

#### 时区
{: #time-zone}
显示指定地点的时区。

#### 城市列表
{: #city-list}
选择世界上主要的城市来设置位置。

#### 地图
{: #map}
在地图上点击以设置位置，使用鼠标左键拖动，可以平移地图。

### 日光强度
{: #sun-intensity}
调整太阳的直接照明亮度，太阳对场景的照明是从太阳的角度与天空的状况计算而来，但可以做调整，与其他光源做调和。

### 太阳高光
{: #sun-highlight}
反射材质上太阳高光的锐利度。

![images/sunhighlight-0.png](images/sunhighlight-0.png)
*太阳高光为0（左）与1（右）。*

**附注:** 在户外场景中如果您不想让物件上的太阳高光太明显，可以降低太阳高光的数值
{: #speckle-artifacts}

{% include_relative snippets/snippet-sunchannel.md %}

#### 北方
{: #north}
**附注:** 北方为世界坐标 Y 方向。

## 天光
{: #sky}
The Sky is a large sphere around the rendering that can be used for lighting. The Sky is very different from environment.  Sky controls lighting. Environment controls what is reflected and visible in the background. There are many situations where the Sky and Environment might be set differently.

#### 在哪里可以找到 Flamingo 天光的控制设置？
天光必须通过载入[照明预设](lighting-tab.html#lighting-presets)来开启或在[自定义照明设置](lighting-tab.html#sky)中开启。

 1. ![images/options.png](images/options.png)工具列 >![images/flamingo-icon.png](images/flamingo-icon.png)Flamingo nXt 工具列
 1. ![images/menuicon.png](images/menuicon.png)功能表 > Flamingo nXt 5.0 下拉菜单 > 显示控制面板 > Flamingo nXt 选项卡 > 天光

The lighting preset schemes for [Exterior](lighting-tab.html#exterior-daylight) and [Interior](lighting-tab.html#interior-daylight) daylight use the Automatic sky by default. The [Studio](lighting-tab.html#studio-lighting) lighting preset scheme uses HDR image lighting by default.

天光有下列五种设置：

>[关闭](lighting-tab.html#off)
>[自动天光](#automatic-sky)
>[高动态范围贴图](#high-dynamic-range-image-sky)
>[颜色](#color-sky)
>[图像](#image-sky)

The two best settings for sky lighting types are [HDR image](#high-dynamic-range-image-sky) sky and [Automatic sky](#automatic-sky). HDR image sky uses an image with lighting values stored on each pixel to provide light and reflection. Automatic sky uses a real-world sun location and cloudiness to simulate a sky.  These settings will produce the most dynamic renderings.

### 自动天光
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

### 高动态范围图片天空
{: #high-dynamic-range-image-sky}
[高动态范围（HDR）图片](https://en.wikipedia.org/wiki/High-dynamic-range_imaging)是一种2D图片，常见的图片格式(JPG、 PNG...) 的像素可以储存最亮的颜色为白色，这也是计算机屏幕能显示最亮的颜色，但自然界的光源亮度远高过白色可以描述的范围，HDR格式的像素可以描述比白色更高的亮度值，所以称为高动态范围图，可以用来照明场景。如果HDR图片所含有的亮度信息是精准的，照明效果也会是精准的。This can produce very dynamic lighting in a scene. The preset Studio Lighting scheme uses HDR images for the sky. If you are thinking of studio lighting as an indoor activity, think of the HDR image as a ceiling that emits light based on the colors in the image.

![images/lighting-001.png](images/lighting-001.png)
*HDRi 照明。*

HDR 图片里的亮度值会被当做以瓦特为单位，如果不是，您必需对 HDR 图片的亮度做调整，以达到适当的照明效果。

HDR 图片除了可以用在天空的设置以外，也可以用在[环境背景](environment-tab.html#advanced-background)、[反射背景](environment-tab.html#advanced-background)及[折射背景](environment-tab.html#advanced-background)。

#### HDRI 图片
Specifies the HDR (HDR and HDRI are the same file type) image file. Click on the image to select a different HDRI.

![images/hdrimage-001.png](images/hdrimage-001.png)
*Equirectangular projection.*

HDR images come in two projection types which let the image to properly wrap around the sky sphere. The most popular is equirectangular.  These images are rectangular with an aspect ratio of 2:1. Equirectangular images will have similar resolution over the whole image. The second projection is spherical. Spherical HDRI images are square in aspect ratio and the image will show great curvature. Spherical projections have less resolution at the seam.

#### 强度
Modifies the brightness of the HDR image light. This setting only matters if there are other lights in the scene that have to be compensated for. If there are no other lights, the tone operator will compensate the exposure and the rendered image will not be brighter or dimmer based on this setting.

![images/hdrlightintensitylow.png](images/hdrlightintensitylow.png)
*Low and high HDR intensity.*

{% include_relative snippets/snippet-rotatehdrimage.md %}In the illustration, the image has been rotated so the reflection of the sun appears on the object. Enter rotation degrees or interactively move the rotation widget indicator.
![images/hdrlightrotation2.png](images/hdrlightrotation2.png)
*Image rotated so the sun appears on the object.*

#### 饱和度
The color saturation for the light. Since the light from an HDR image is the color of the pixels in the image, this sometimes produces unwanted color effects. Set the saturation low if you want the light from the image, but not the color.

![images/hdrlightsaturation0.png](images/hdrlightsaturation0.png)
*Low (left) and high (right) saturation.*

{% include_relative snippets/snippet-mirrorimage.md %}

{% include_relative snippets/snippet-skychannel.md %}

### 颜色
{: #color-sky}
It is possible to use a color or gradient of color to light the scene. The colors in the sky are multiplied by the intensity value to give the colors a lighting value.

#### 强度
The Intensity value is used to multiply the colors in the Sky and result in a lighting value.  Colors can range from 0 - 256 per channel. Intensity will multiply those values.

#### Color type
There are three ways to control the color of the sky.  These are similar to the Color Environment controls.  See [Color Background](environment-tab.html#environment-color-and-gradient-backgrounds) controls for more information.

### 图像
{: #image-sky}
It is possible to use an image to light the scene. The colors in the image are multiplied by the intensity value to give the colors a lighting value.

#### 强度
The Intensity value is used to multiply the colors in the Sky and result in a lighting value.  Colors can range from 0 - 256 per channel. Intensity will multiply those values.

#### Image Projection
There are many ways to control how an image is mapped to the sky.  These are similar to the Image Background controls.  See [Image Background](environment-tab.html#environment-image) controls for more information.

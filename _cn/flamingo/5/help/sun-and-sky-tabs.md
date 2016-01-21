---
title: 太阳与天光
---

# ![imagessun.svg](images/sun.svg) {{page.title}}
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

![images/sydneymorning.png](images/sydneymorning.png)  ![images/stockholmmorning.png](images/stockholmmorning.png)
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
天光是包裹着整个渲染场景的一个巨大球体，用于照明。天光与环境非常不同，天光用于照明而环境控制着物件表面所反射的内容以及可见背景。天光与环境的设置也有所不同。

#### 在哪里可以找到 Flamingo 天光的控制设置？
天光必须通过载入[照明预设](lighting-tab.html#lighting-presets)来开启或在[自定义照明设置](lighting-tab.html#sky)中开启。

 1. ![images/options.png](images/options.png)工具列 >![images/flamingo-icon.png](images/flamingo-icon.png)Flamingo nXt 工具列
 1. ![images/menuicon.png](images/menuicon.png)功能表 > Flamingo nXt 5.0 下拉菜单 > 显示控制面板 > Flamingo nXt 选项卡 > 天光

在[户外日光](lighting-tab.html#exterior-daylight)和[室内日光](lighting-tab.html#interior-daylight)照明预设配置中，默认使用自动天光，[摄影棚](lighting-tab.html#studio-lighting)照明预设配置中的天光默认使用 HDR 图像。

天光有下列五种设置：

>[关闭](lighting-tab.html#off)
>[自动天光](#automatic-sky)
>[高动态范围贴图](#high-dynamic-range-image-sky)
>[颜色](#color-sky)
>[图像](#image-sky)

最好的两种天光类型是 [HDR 贴图](#high-dynamic-range-image-sky)以及[自动天光](#automatic-sky)。 HDR 贴图天光中的每个像素都记录了照明信息，可以用于照明和反射。自动天光通过真实世界中太阳的位置和云量模拟出天空效果，这些设置能够产生很好的渲染效果。

### 自动天光
{: #automatic-sky}
将天空设置为自动时，可以使用[太阳选项卡](sun-and-sky-tabs.html)设置太阳的位置与强度，太阳很高和很低时，渲染出的照明与颜色也非常不同。

![images/sky-002.png](images/sky-002.png)
*自动天空：太阳高角度（左）与低角度（右）。*

#### 云量
{: #sky-cloudiness}
当云量为 0 时，模型会有比较锐利的阴影，云量设置值越大，阴影就越模糊。云量的设置会影响日光计算的许多面相，包括：直接照明与间接光的相对量、间接光的计算方式与使用自动天空时天空的颜色。云量的设置值０为晴朗无云，１为多云，数值在 0.35 - 0.50 之间非常敏感，微小的数值变化也产生不同的效果。

![images/cloudiness0.png](images/cloudiness0.png)
*云量0（左）与1（右）。*

#### 天光强度
{: #sky-intensity}
调整天空的间接光亮度，天空对场景的照明是从太阳的角度与天空的状况计算而来，但可以做调整。**附注:** 这个设置只有在场景中有需要补偿的人造光时才有作用。场景中没有人造光时，渲染图片不会因为这个设置自动调亮或调暗。

{% include_relative snippets/snippet-skychannel.md %}

### 高动态范围图片天空
{: #high-dynamic-range-image-sky}
[高动态范围（HDR）图片](https://en.wikipedia.org/wiki/High-dynamic-range_imaging)是一种2D图片，常见的图片格式(JPG、 PNG...) 的像素可以储存最亮的颜色为白色，这也是计算机屏幕能显示最亮的颜色，但自然界的光源亮度远高过白色可以描述的范围，HDR格式的像素可以描述比白色更高的亮度值，所以称为高动态范围图，可以用来照明场景。如果HDR图片所含有的亮度信息是精准的，照明效果也会是精准的。使用此选项可以为场景提供高动态照明。摄影棚照明预设配置默认使用 HDR 贴图作为天光，您可以将 HDR 图片视为室内场景来自墙体或天花板的间接光，HDR图片上的色彩会影响照明的色调。

![images/lighting-001.png](images/lighting-001.png)
*HDRi 照明。*

HDR 图片里的亮度值会被当做以瓦特为单位，如果不是，您必需对 HDR 图片的亮度做调整，以达到适当的照明效果。

HDR 图片除了可以用在天空的设置以外，也可以用在[环境背景](environment-tab.html#advanced-background)、[反射背景](environment-tab.html#advanced-background)及[折射背景](environment-tab.html#advanced-background)。

#### HDRI 图片
设置 HDR (HDR 和 HDRI 是相同的文件类型) 贴图文件。点击图像可以选择一张不同的 HDRI 贴图。

![images/hdrimage-001.png](images/hdrimage-001.png)
*等量矩形投影*

HDR 贴图可以通过两种投影方式包裹在天光球体上，最流行的一直是等量矩形投影，这种贴图的长宽比为 2:1。等量矩形投影贴图也的分辨率也接近 2:1。第二种投影方式是球面投影，球面 HDRI 贴图具有正方形分辨率，图像的曲率显得非常大， 球面投影的接缝处分辨率较小。

#### 强度
修改 HDR 贴图的照明亮度。这个设置只有场景中有需要补偿的人造光时才有作用。场景中没有人造光时，渲染图片不会因为这个设置自动调亮或调暗。

![images/hdrlightintensitylow.png](images/hdrlightintensitylow.png)
*低与高 HDR 强度。*

{% include_relative snippets/snippet-rotatehdrimage.md %}旋转 HDR 图片，让该图片的某一部分出现在物件的反射里，您可以使用图形化界面调整，或直接输入角度数值。
![images/hdrlightrotation2.png](images/hdrlightrotation2.png)
*旋转图片的位置，使太阳可以出现在物件的反射里。*

#### 饱和度
照明颜色饱和度。 以 HDR 图片照明场景时，图片的颜色即光源的颜色，在某些情形下可能产生非预期的效果。如果您不想让 HDR 图片的颜色影响照明，可以将饱和度调低。

![images/hdrlightsaturation0.png](images/hdrlightsaturation0.png)
*低（左）与高（右）饱和度。*

{% include_relative snippets/snippet-mirrorimage.md %}

{% include_relative snippets/snippet-skychannel.md %}

### 颜色
{: #color-sky}
使用单色或渐变的颜色照亮场景，颜色照亮场景的亮度值是颜色数值乘以强度值。

#### 强度
强度值用于乘以颜色值得到照明场景的亮度值。颜色每个通道的取值范围都是 0 - 256 。强度值将于这些值相乘。

#### 颜色类型
有三种方法控制天光的颜色，与环境颜色的控制设置类似，更多信息请参考[颜色背景](environment-tab.html#environment-color-and-gradient-backgrounds) 。

### 图片
{: #image-sky}
允许使用图像照亮场景，图像中的颜色值乘以强度值得到照亮场景的亮度值。

#### 强度
强度值用于乘以颜色值得到照明场景的亮度值。颜色每个通道的取值范围都是 0 - 256 。强度值将于这些值相乘。

#### 图像投影
有很多种将图像投影到天光的方式，与背景中图像的投影方式类似，更多信息请参考[图像背景](environment-tab.html#environment-image)。

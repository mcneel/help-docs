---
Title: Flamingo nXt 文件属性
---


# ![images/options.svg](images/options.svg) {{page.title}}
这些设置仅应用于当前的模型，可以让您在渲染品质与速度之间取舍。

#### 在哪里可以找到这个指令？
<!-- These locations are not correct.  They need to be updated. -->

 1. ![images/icon-render.png](images/icon-render.png)渲染工具工具列 > ![images/environments.png](images/environments.png) 材质编辑器
 1. ![images/menuicon.png](images/menuicon.png)功能表 > 渲染下拉菜单 > 环境编辑器
 1. 指令 > EnvironmentEditor

## 材质
{: #materials}
使用这些设置快速更改 Flamingo 渲染时的特性。这些设置不会更改物件和图层上被赋予的材质，但是将会决定 Flamingo 渲染每个面生成颜色的方式。

#### 使用材质
{: #use-materials}
以赋予给物件的 Flamingo nXt 或 Rhino 材质渲染，未赋予材质的物件以白色渲染。

#### 使用物件颜色
{: #use-object-color}
使用物件属性设置的显示颜色渲染。附注：使用材质与使用物件颜色可以同时启用，让有赋予材质的物件以材质渲染，未赋予材质的物件以物件属性的显示颜色渲染。

#### 光晕通道
{: #channel}
材质上可以产生很亮的光晕，但是光晕不能照亮其他物件。(将物件标记为灯光物件可以照亮其他物件。)  将光晕设置到一个通道上，这样在渲染完成后就可以直接在图像上实时调节光晕的亮度而不用重新进行渲染。

## 反弹数
{: #bounces}
当每束光线从光源发出进入场景后，照到物件上会反弹到其他物件上，这里设置的是允许反弹的最大次数，反弹达到这个数量就不再反弹。但如果反弹数设置的太少，会丢失反射效果或场景中有些地方呈现出黑色，默认设置在大多数情况下都有很好的表现，只有个别情况下才需要修改。

#### 反射
{: #reflective-bounces}
设置渲染时一条射线反射的最大次数，达到设置的次数反射计算即停止，设置为 0 代表不计算反射，数值越大渲染需要的时间越长。当场景中出现本应该反射出相邻的物件但却呈现出黑色的情况，就需要调高此值。

#### 折射
{: #refractive-bounces}
设置渲染时一条射线折射的最大次数，达到设置的次数折射计算即停止，设置为 0 代表不计算折射，数值越大渲染需要的时间越长。场景中本应该折射出的影像呈现出黑色时需要调高此项。

#### 间接照明
{: #indirect-bounces}
设置渲染时间光源自物件表面反弹的最大次数，达到设置的次数间接光计算即停止，设置为0代表不计算间接光源，数值越大渲染需要的时间越长。

## 间接照明
{: #indirect-settings}
间接照明设置只对照射在物件上反弹出来照射在另一个面上的光照有效果。

#### 溢色
{: #color-bleed}
溢色控制光线从一个面反射到另一个面时随之传播的颜色总量。默认设置中溢色为最大值，随反射携带的颜色在最大程度上对渲染产生影响。  

#### 蒙特卡洛反射
{: #monte-carlo}
蒙特卡洛控制 Flamingo 如何对间接照明进行采样。启用时，渲染初期画面会出现很多噪点，但随着渲染的进行，蒙特卡洛能够展现出间接照明的细节，将间接照明表现的很生动，对间接照明非常依赖的场景，启用蒙特卡洛反射会有不错的效果。

## 其他

#### 使用隐藏的灯光
{: #uselightsonlayersthatareoff}
使用隐藏图层中的灯光和被隐藏的灯光。

### 渲染约束
{: #number-of-passes}
{: #time}
{: #render-constraints}
{% include_relative snippets/snippet-renderconstraints.md %}

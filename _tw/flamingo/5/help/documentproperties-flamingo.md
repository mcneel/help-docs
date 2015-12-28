---
title: Flamingo nXt 文件內容
---


# ![images/options.svg](images/options.svg) {{page.title}}
這裡的設定只會影響目前的模型，可以讓您在彩現品質與速度之間取捨。

#### 可以在哪找到這個指令?
<!-- These locations are not correct.  They need to be updated. -->

 1. ![images/icon-render.png](images/icon-render.png)彩現工具工具列 > ![images/environments.png](images/environments.png) 材質編輯器
 1. ![images/menuicon.png](images/menuicon.png)功能表 > 彩現功能表 > 環境編輯器
 1. 指令 > EnvironmentEditor

## 材質
{: #materials}
Use these controls to quickly change how Flamingo renders the surfaces in a rendering.  These settings will not change the material assignments on the objects and layers, but will change how Flamingo produces the color of each surface.

#### 使用材質
{: #use-materials}
以賦予給物件的 Flamingo nXt 或 Rhino 材質彩現，未賦予材質的物件以白色彩現。如果**使用材質**與**使用物件顏**色皆未勾選，所有的物件以白色彩現。

#### 使用物件顏色
{: #use-object-color}
使用物件內容設定的顯示顏色彩現。附註：使用材質與使用物件顏色可以同時啟用，讓有賦予材質的物件以材質彩現，未賦予材質的物件以物件內容的顯示顏色彩現。

#### 光暈通道
{: #channel}
光暈可使材質在彩現影像裡產生發亮的效果，但無法照亮其它物件，標記為燈光的物件才能照亮其它物件)。光暈通道可在彩現完成後調整光暈的亮度，無需重新彩現整個場景。

## Bounces
{: #bounces}
當一條射線進入場景後經過某個次數的反彈後即停止，限制反彈次數可減少完成彩現需要的時間，但反彈次數設定過低時彩現影像的某些部分可能會出現黑色。預設的反彈次數適用於大部分的場景，少數的場景可能需要適度調高反彈次數。

#### 反射
{: #reflective-bounces}
設定彩現時一條射線反射的最大次數，達到設定的次數時反射計算即停止。設為 0 代表不計算反射，數值越大彩現需要的時間越長。當彩現影像裡的反射影像出現黑色時請調高此數值。

#### 折射
{: #refractive-bounces}
設定彩現時一條射線折射的最大次數，達到設定的次數時折射計算即停止。設為 0 代表不計算折射，數值越大彩現需要的時間越長。當彩現影像裡的透明物件後方的影像出現黑色時請調高此數值。

#### 間接照明
{: #indirect-bounces}
設定彩現時間接光源自物件表面反彈的最大次數，達到設定的次數時間接照明的計算即停止，設為 0 代表不計算間接光源，數值越大彩現需要的時間越長。

## 間接照明
{: #indirect-settings}
The indirect lighting settings only affect the rays that bounce off one surface and carry light to another surface.

#### 溢色
{: #color-bleed}
溢色控制光線從一個物件反彈時，光線顏色受物件顏色的影響程度。預設為最大值，將物件顏色對間接光源的影響最大化。  

#### 蒙地卡羅反射
{: #monte-carlo}
Monte Carlo in indirect lighting controls how Flamingo samples indirect light. When activated, the indirect light will become very noisy in the early passes.  But over all, as the passes progress, the overall effect of Monte Carlo indirect will be a more subtle and potentially more detail indirect effect. Scenes that rely heavily on indirect light may benefit from Mote Carlo indirection reflections.

## 其它

#### 使用隱藏的燈光
{: #uselightsonlayersthatareoff}
使用被隱藏的燈光與被隱藏的圖層上的燈光。

### 彩現限制
{: #number-of-passes}
{: #time}
{: #render-constraints}
{% include_relative snippets/snippet-renderconstraints.md %}

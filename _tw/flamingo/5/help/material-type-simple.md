---
title: 簡易材質內容
---
# ![images/paint.svg](images/paint.svg) {{page.title}}
Flamingo 的材質有許多類型，不同類型的材質有不同的簡易設定，讓您可以輕易編輯一個材質類型常用的選項，通常您只要變更材質的顏色即可。

#### 簡易材質類型：

> ![images/newsolidcolormaterial.png](images/newsolidcolormaterial.png)[純顏色](#solid-color)
> ![images/newplasticmaterial.png](images/newplasticmaterial.png)[塑膠](#plastic)
> ![images/newmetalmaterial.png](images/newmetalmaterial.png)[金屬](#metal)
> ![images/newglassmaterial.png](images/newglassmaterial.png)[玻璃](#glass)
> ![images/newglossymaterial.png](images/newglossymaterial.png)[模糊](#glossy)
> ![images/newclearfinishmaterial.png](images/newclearfinishmaterial.png)[亮光漆面](#clearfinish)
> ![images/newtexturedmaterial.png](images/newtexturedmaterial.png)[貼圖](#flamingo-textured)
> ![images/newtexturesetmaterial.png](images/newtexturesetmaterial.png)[貼圖組](#texture-set)

每種貼圖類型都有相同的進階材質設定，需要使用進階材質設定可以選擇建立 **Flamingo 進階**材質，或是在其它類型的材質裡切換到**進階編輯器**。

#### 材質的進階設定群組有：

> [名稱](material-type-advanced.html#name)
> [材質程序](material-type-advanced.html#procedures)
> [進階材質內容](material-type-advanced.html#advanced-materials-properties)
> [反射度](material-type-advanced.html#reflective-finish-and-highlight)
> [透明內容](material-type-advanced.html#transparency)
> [程序貼圖](material-type-advanced.html#bump-patterns)
> [圖片貼圖](material-type-advanced.html#textures)
> [附註](material-type-advanced.html#notes)

材質是儲存在 Rhino 模型裡，不同模型裡相同名稱的材質不會相互影響。

## 純顏色
{: #solid-color}
純顏色材質只有[名稱](material-type-advanced.html#name)與[顏色](material-type-advanced.html#color)。

![images/solidcolors.png](images/3-solidcolor.png)

{% include_relative snippets/snippet-material-name.md %}
{% include_relative snippets/snippet-material-color-select.md %}
{% include_relative snippets/snippet-material-advanced-editor.md %}

## 塑膠
{: #plastic}
塑膠是低反射度，[反光](material-type-advanced.html#highlight-color)為白色的材質。

![images/solidcolors.png](images/3-plastic.png)

{% include_relative snippets/snippet-material-name.md %}
{% include_relative snippets/snippet-material-color-select.md %}
{% include_relative snippets/snippet-material-advanced-editor.md %} 進階編輯器裡可以修改預設的[反光顏色](material-type-advanced.html#highlight-color)、[強度](material-type-advanced.html#intensity)、[Fresnel](material-type-advanced.html#fresnel) 與[銳利度](material-type-advanced.html#sharpness)。

## 金屬
{: #metal}
金屬材質的反光顏色與金屬的[顏色](material-type-advanced.html#color)一致，並可控制反射與反光[銳利度](material-type-advanced.html#sharpness)。

![images/solidcolors.png](images/3-metal.png)

{% include_relative snippets/snippet-material-name.md %}
{% include_relative snippets/snippet-material-color-select.md %}
#### 銳利度
控制反射與反光的銳利與模糊，請參考[銳利度](material-type-advanced.html#sharpness)的說明。

{% include_relative snippets/snippet-material-advanced-editor.md %} 進階編輯器裡可以修改預設的[反光顏色](material-type-advanced.html#highlight-color)、[強度](material-type-advanced.html#intensity)、[Fresnel](material-type-advanced.html#fresnel) 與[型式](material-type-advanced.html#type)。

## 玻璃
{: #glass}
玻璃材質有[顏色](material-type-advanced.html#color)與[折射率](advanced-material-properties-main.html#index-of-refraction) (Index of Refraction, IOR) 設定。

![images/solidcolors.png](images/3-glass.png)

{% include_relative snippets/snippet-material-name.md %}
{% include_relative snippets/snippet-material-color-select.md %}
#### 折射率
控制光線進入透明材質時的轉折特性，請參考[折射率](advanced-material-properties-main.html#index-of-refraction)的說明。

{% include_relative snippets/snippet-material-advanced-editor.md %} 進階編輯器裡可以修改預設的[反光顏色](material-type-advanced.html#highlight-color)、[強度](material-type-advanced.html#intensity)、[Fresnel](material-type-advanced.html#fresnel)、[銳利度](material-type-advanced.html#sharpness)與[透明度](material-type-advanced.html#transparency)。

## 模糊
{: #glossy}
模糊反射材質通常有較低的反光[強度](material-type-advanced.html#intensity)與[銳利度](material-type-advanced.html#sharpness)。

![images/solidcolors.png](images/3-glossy.png)

{% include_relative snippets/snippet-material-name.md %}
{% include_relative snippets/snippet-material-color-select.md %}
#### 強度
控制反射與反光的銳利與模糊，請參考[銳利度](material-type-advanced.html#intensity)的說明。

#### 反光銳利度
Controls sharpness vs blurriness of the highlight spot from lights on the surface. See Advanced [Highlight sharpness](material-type-advanced.html#sharpness) topic for more details.

{% include_relative snippets/snippet-material-advanced-editor.md %} Use the Advanced Editor to overwrite the presets of [Fresnel](material-type-advanced.html#fresnel) and [Type](material-type-advanced.html#type).

## 亮光漆面
{: #clearfinish}
亮光漆面材質模擬汽車烤漆、瓷器、陶瓷、上了亮光漆的木頭或任何表面有透明塗層的物件，亮光漆面材質使用 [Fresnel](material-type-advanced.html#fresnel) 設定依據物件表面的法線方向與視圖方向的夾角改變材質的顏色，物件正對視圖的部分的材質顏色比較深，徧離視圖方向的部分的反射度會提高，汽車烤漆就是很好的例子。

![images/solidcolors.png](images/3-clearfinish.png)

{% include_relative snippets/snippet-material-name.md %}
{% include_relative snippets/snippet-material-color-select.md %}
{% include_relative snippets/snippet-material-advanced-editor.md %} 進階編輯器裡可以修改預設的[反光顏色](material-type-advanced.html#highlight-color)、[強度](material-type-advanced.html#intensity)、[Fresnel](material-type-advanced.html#fresnel) 與[銳利度](material-type-advanced.html#sharpness)。

## Flamingo 貼圖
{: #flamingo-textured}
貼圖材質以圖片取代材質的顏色，貼圖材質的簡易材質內容裡有使用的圖片的名稱與解析度資訊及調整拼貼、反光強度與銳利度的設定。

![images/solidcolors.png](images/3-texture.png)

{% include_relative snippets/snippet-material-name.md %}
{% include_relative snippets/snippet-material-color-select.md %}
#### 強度
控制反射與反光的強度，請參考[強度](material-type-advanced.html#intensity)的說明。

#### 銳利度
控制反射與反光的銳利與模糊，請參考[銳利度](material-type-advanced.html#sharpness)的說明。

#### 圖片
設定材質使用的貼圖與內容，這裡有許多選項，請參[圖片](material-type-advanced.html#texture)的說明。

{% include_relative snippets/snippet-material-image-add-edit.md %}
{% include_relative snippets/snippet-material-advanced-editor.md %} 進階編輯器裡可修改材質的許多預設值。

## 貼圖組
{: #texture-set}
[貼圖組材質](texture-set-materials.html)可用不同的貼圖控制材質的顏色、置換、法線向量、凹凸，建立效果逼真的材質，[PixPlant](http://www.pixplant.com/) 可將一般的圖片轉換為置換、法線向量、凹凸需要的圖片。
<!-- TODO: This dialog Needs a page.-->
![images/solidcolors.png](images/textureset.png)

{% include_relative snippets/snippet-material-name.md %}
#### 寬度與高度
設定貼圖每一個拼貼單位的尺寸。

#### 強度
控制反射與反光的強度，請參考[強度](material-type-advanced.html#intensity)的說明。

#### 銳利度
控制反射與反光的銳利與模糊，請參考[銳利度](material-type-advanced.html#sharpness)的說明。

#### 型式
控制反射與反光的型式，請參考[型式](material-type-advanced.html#type)的說明。

{% include_relative snippets/snippet-material-advanced-editor.md %} 進階編輯器裡可修改材質的許多預設值。**附註：** This is a complex material that uses many overlaid textures set with various defaults.  Using the advanced editor will not keep all the properties in sync.

## 進階材質
Flamingo 材質的[進階編輯器](material-type-advanced)有材質的所有設定，如果內建的材質類型無法符合您的需要，可以選擇建立 [Flamingo 進階](material-type-advanced)材質，以便直接使用所有的設定。

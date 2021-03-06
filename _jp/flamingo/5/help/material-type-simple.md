---
title: マテリアルの基本プロパティ
---
# ![images/paint.svg](images/paint.svg){: .inline} {{page.title}}
Flamingoのマテリアルは、一連のプロパティのグループで定義されます。これらは一般的に使用されるシンプルなマテリアルのタイプの数々です。これらのマテリアルは、非常にシンプルなコントロールセットを提供します。それによって、多数の複雑なコントロールを設定することなく、プロパティを簡単に編集して、マテリアルの外見を変えることができます。ほとんどのシンプルなマテリアルは、単に色を変更するだけで希望する効果が得られます。

#### シンプルなマテリアルのタイプ

> ![images/newsolidcolormaterial.png](images/newsolidcolormaterial.png){: .inline} [単色](#solid-color)
> ![images/newplasticmaterial.png](images/newplasticmaterial.png){: .inline} [プラスチック](#plastic)
> ![images/newmetalmaterial.png](images/newmetalmaterial.png){: .inline} [金属](#metal)
> ![images/newglassmaterial.png](images/newglassmaterial.png){: .inline} [ガラス](#glass)
> ![images/newglossymaterial.png](images/newglossymaterial.png){: .inline} [光沢](#glossy)
> ![images/newclearfinishmaterial.png](images/newclearfinishmaterial.png){: .inline} [クリアフィニッシュ](#clearfinish)
> ![images/newtexturedmaterial.png](images/newtexturedmaterial.png){: .inline} [Flamingoテクスチャ](#flamingo-textured)
> ![images/newtexturesetmaterial.png](images/newtexturesetmaterial.png){: .inline} [テクスチャセット](#texture-set)

マテリアルはすべて詳細マテリアルに変換することができます。詳細マテリアルは、Flamingo nXtでマテリアルの編集を行うためのすべての可能なコントロールを提供します。マテリアルの幅広いコントロールを利用するには、詳細マテリアルを使うか、既存のマテリアルを詳細マテリアルに変換してください。

#### 詳細マテリアルは、これらのプロパティグループから構成されています:

> [名前](material-type-advanced.html#name)
> [マテリアルプロシージャ](material-type-advanced.html#procedures)
> [詳細マテリアルプロパティ](material-type-advanced.html#advanced-materials-properties)
> [反射仕上げ](material-type-advanced.html#reflective-finish-and-highlight)
> [透明度のプロパティ](material-type-advanced.html#transparency)
> [プロシージャルテクスチャ](material-type-advanced.html#bump-patterns)
> [ビットマップテクスチャ](material-type-advanced.html#textures)
> [注記](material-type-advanced.html#notes)

マテリアルはRhinoのモデルに保存、格納されます。異なるマテリアルが別々のRhinoのモデルで同じ名前を持つことができます。

## 単色
{: #solid-color}
単色マテリアルは、[名前](material-type-advanced.html#name)と[色](material-type-advanced.html#color)だけを所有します。

![images/solidcolors.png](images/3-solidcolor.png)

{% include_relative snippets/snippet-material-name.md %}
{% include_relative snippets/snippet-material-color-select.md %}
{% include_relative snippets/snippet-material-advanced-editor.md %}

## プラスチック
{: #plastic}
プラスチックマテリアルには、白い[ハイライト](material-type-advanced.html#highlight-color)、わずかな反射性があります。

![images/solidcolors.png](images/3-plastic.png)

{% include_relative snippets/snippet-material-name.md %}
{% include_relative snippets/snippet-material-color-select.md %}
{% include_relative snippets/snippet-material-advanced-editor.md %} 予め設定されている[ハイライト色](material-type-advanced.html#highlight-color)、[強度](material-type-advanced.html#intensity)、[フレネル](material-type-advanced.html#fresnel)、[シャープネス](material-type-advanced.html#sharpness)を変更したい場合は、詳細エディタを使用します。

## 金属
{: #metal}
金属マテリアルには、[色](material-type-advanced.html#color)の設定と一致する色でハイライトが設定されています。反射の[シャープネス](material-type-advanced.html#sharpness)をコントロールすることもできます。

![images/solidcolors.png](images/3-metal.png)

{% include_relative snippets/snippet-material-name.md %}
{% include_relative snippets/snippet-material-color-select.md %}
#### シャープネス
反射のシャープネス対ブラーの度合をコントロールします。詳細については、詳細プロパティの[シャープネス](material-type-advanced.html#sharpness)のトピックを参照してください。

{% include_relative snippets/snippet-material-advanced-editor.md %} 予め設定されている[ハイライト色](material-type-advanced.html#highlight-color)、[強度](material-type-advanced.html#intensity)、[フレネル](material-type-advanced.html#fresnel)、[タイプ](material-type-advanced.html#type)を変更したい場合は、詳細エディタを使用します。

## ガラス
{: #glass}
ガラスマテリアルは、[色](material-type-advanced.html#color)と[屈折率](advanced-material-properties-main.html#index-of-refraction)（IOR）があります。

![images/solidcolors.png](images/3-glass.png)

{% include_relative snippets/snippet-material-name.md %}
{% include_relative snippets/snippet-material-color-select.md %}
#### IOR
マテリアルを通過する際の光の屈折量をコントロールします。詳細については、詳細プロパティの[屈折率](advanced-material-properties-main.html#index-of-refraction)を参照してください。

{% include_relative snippets/snippet-material-advanced-editor.md %} 予め設定されている[ハイライト色](material-type-advanced.html#highlight-color)、[強度](material-type-advanced.html#intensity)、[フレネル](material-type-advanced.html#fresnel)、[シャープネス](material-type-advanced.html#sharpness)、[透明度](material-type-advanced.html#transparency)を変更したい場合は、詳細エディタを使用します。

## 光沢
{: #glossy}
光沢マテリアルには通常ハイライト[強度](material-type-advanced.html#intensity)と[シャープネス](material-type-advanced.html#sharpness)が低く設定されています。

![images/solidcolors.png](images/3-glossy.png)

{% include_relative snippets/snippet-material-name.md %}
{% include_relative snippets/snippet-material-color-select.md %}
#### 強度
サーフェス上の光源からのハイライトの強度をコントロールします。詳細については、詳細プロパティの[強度](material-type-advanced.html#intensity)のトピックを参照してください。

#### ハイライトシャープネス
サーフェス上の光源からのハイライトスポットのシャープネス対ブラーの度合コントロールします。詳細については、詳細プロパティの[ハイライトシャープネス](material-type-advanced.html#sharpness)のトピックを参照してください。

{% include_relative snippets/snippet-material-advanced-editor.md %} 予め設定されている[フレネル](material-type-advanced.html#fresnel)と[タイプ](material-type-advanced.html#type)を変更したい場合は、詳細エディタを使用します。

## クリアフィニッシュ
{: #clearfinish}
クリアフィニッシュマテリアルは、車の塗料（ペイント）、磁器（ポーセリン）、陶磁器（セラミック）、ニスを塗った木材、その他のプラスチックまたはクリアコーティング層のあるマテリアルをシミュレートします。クリアフィニッシュは、視点に基づいたマテリアルの色の変化に[フレネル](material-type-advanced.html#fresnel)設定を用います。これらのマテリアルの色は、正面から見た場合、濃くなる傾向があります。しかし、サーフェスの曲面に沿って視点をずらしていくと、反射が強くなっていきます。クリアコーティング、またはクリアラッカー仕上げのあるカーペイントが、よい例です。

![images/solidcolors.png](images/3-clearfinish.png)

{% include_relative snippets/snippet-material-name.md %}
{% include_relative snippets/snippet-material-color-select.md %}
{% include_relative snippets/snippet-material-advanced-editor.md %} 予め設定されている[ハイライト色](material-type-advanced.html#highlight-color)、[強度](material-type-advanced.html#intensity)、[フレネル](material-type-advanced.html#fresnel)、[シャープネス](material-type-advanced.html#sharpness)を変更したい場合は、詳細エディタを使用します。

## Flamingoテクスチャ
{: #flamingo-textured}
テクスチャマテリアルは、画像を用いて色やパターンを作成します。このシンプルなマテリアルからは、画像名、解像度、タイルのサイズ、そしてハイライトの強度とシャープネスをコントロールすることができます。

![images/solidcolors.png](images/3-texture.png)

{% include_relative snippets/snippet-material-name.md %}
{% include_relative snippets/snippet-material-color-select.md %}
#### 強度
サーフェスの鏡のような反射の強度をコントロールします。詳細については、詳細プロパティの[強度](material-type-advanced.html#intensity)のトピックを参照してください。

#### シャープネス
反射のシャープネス対ブラーの度合をコントロールします。詳細については、詳細プロパティの[シャープネス](material-type-advanced.html#sharpness)のトピックを参照してください。

#### 画像
マテリアルの画像マップとプロパティを設定します。多くのオプションがあります。詳細については、詳細プロパティの[画像](material-type-advanced.html#texture)を参照してください。

{% include_relative snippets/snippet-material-image-add-edit.md %}
{% include_relative snippets/snippet-material-advanced-editor.md %} マテリアルに予め設定されている内容を変更したい場合は、詳細エディタを使用します。

## テクスチャセット
{: #texture-set}

テクスチャセットマテリアルは、マテリアルを連係して定義する一連のセットのテクスチャです。これらのセットは、ディスプレイスメント、法線、バンプマップなどの情報を含むテクスチャマップから作成できます。ディスプレイスメントマップは、マテリアルに深さを与えます。これらのテクスチャマップをセットとして組み合わせると、非常にリアルなマテリアルを作成することができます。[PixPlantソフトウェア](http://www.pixplant.com/)は、標準ビットマップを使って、これらのテクスチャのセットを作成できる製品です。

![images/solidcolors.png](images/textureset.png)

{% include_relative snippets/snippet-material-name.md %}
#### 幅と高さ
セットのすべてのテクスチャのサイズをコントロールします。すべてのビットマップのサイズを同じに、整列するようにするには、このコントロールを使用します。

#### 強度
サーフェスの鏡のような反射の強度をコントロールします。詳細については、詳細プロパティの[強度](material-type-advanced.html#intensity)のトピックを参照してください。

#### シャープネス
反射のシャープネス対ブラーの度合をコントロールします。詳細については、詳細プロパティの[シャープネス](material-type-advanced.html#sharpness)のトピックを参照してください。

#### タイプ
これは、サーフェス上の反射のタイプをコントロールします。詳細については、詳細プロパティの[タイプ](material-type-advanced.html#type)のトピックを参照してください。

### テクスチャマップ
テクスチャマップテーブルにテクスチャセットのテクスチャが表示されます。テーブルを右クリックして、セットのテクスチャを追加、削除、変更できます。

#### マップを追加...
右クリックメニューのこのコマンドを使用して、リストに新規テクスチャを追加することができます。1度に複数のテクスチャを追加できます。テクスチャ名にマッピングタイプの1つがサフィックス（接尾辞）として含まれていた場合、マッピングタイプが自動的に追加されます。例えば、マップに*-normal*とあった場合、それは自動的に法線マップタイプとしてタグ付けされます。

#### マップを削除
この右クリックコマンドは、テーブルからテクスチャを削除します。

#### 色
この右クリックで指定できるマッピングタイプは、テクスチャの目に見える色に使用されます。詳細については、[標準マッピングタイプ](material-image-properties.html#standard)を参照してください。

#### バンプ
バンプマップはテクスチャのグレースケールを使用して、マテリアルのバンプ（高さ）の変化をシミュレートします。詳細については、[詳細コントロールのバンプマップの強弱](material-image-properties.html#bump)を参照してください。

#### 法線
法線マップは、ビットマップの赤、緑、青チャンネルを使用してそれぞれのピクセルでのバンプの方向を調整する特殊なバンプマップです。青チャンネルはバンプのZ方向なので、画像は青い色彩を帯びる傾向があります。詳細については、[詳細コントロールの法線](material-image-properties.html#normal)を参照してください。

#### 鏡面反射
鏡面反射マップは、マテリアルのグレースケール色を使用して、その場所での画像の反射の量をコントロールします。詳細については、[詳細コントロールの透明度](material-image-properties.html#transparency)を参照してください。

#### 不透明
不透明マップは、画像のグレースケールに基づいてそれぞれのピクセルでのマテリアルの透明度をコントロールします。詳細については、[詳細のコントロールの法線マップ](material-image-properties.html#normal)を参照してください。

#### ディスプレイスメント
ディスプレイスメントマップは、マップのグレースケール色に基づいてレンダリングメッシュを実際に移し（ディスプレイスし）ます。詳細については、[詳細コントロールのディスプレイスメントマップ](material-image-properties.html#displacement)を参照してください。

### 詳細マテリアル
[Flamingo 詳細](material-type-advanced)マテリアルは、Flamingoのマテリアルのすべてのプロパティのセットを含んでいます。シンプルなマテリアルが用途に合わない場合、この[Flamingo 詳細](material-type-advanced)マテリアルを使用して、フレキシブルにマテリアルを作成することができます。

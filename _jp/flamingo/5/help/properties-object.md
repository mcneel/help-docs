---
title: オブジェクトのプロパティ
---


#  ![images/properties.svg](images/properties.svg) {{page.title}}
Flamingo nXtのオブジェクトのプロパティは、Flamingo nXtでのオブジェクトのレンダリング方法のみに影響します。

### ![images/materialtab.png](images/materialtab.png) マテリアルソース
{: #material-source}
マテリアルは、レイヤ、オブジェクト、そしてブロックに割り当てることができます。マテリアルの割り当てについてに詳細は、[マテリアルの割り当て](material_assignment.html)のトピックを参照してください。マテリアルがオブジェクトの設定になっている場合、マテリアルのプロパティもこのダイアログに表示されます。マテリアルの編集についての詳細は、[マテリアルのプロパティ](material-type-simple.html)を参照してください。

### ![images/apply-cylindrical-mapping.png](images/apply-cylindrical-mapping.png) テクスチャマッピング
{: #texture-mapping}
マッピングは、マテリアルの特定のオブジェクトへの配置（マップ）方法をコントロールします。マテリアルをレイヤに割り当てるのに使用される方法、またはオブジェクトに割り当てるのに使用される方法は、マッピングに影響しません。目立ったパターンがないマテリアルの場合は、通常マッピングをコントロールする必要はありません。マテリアルに方向がある場合、またはマテリアルにはっきりとしたパターンがある部分にマッピングを使用してください。このような場合でも、デフォルトのマッピングで十分な時があります。マッピングは、オブジェクトに付随し、オブジェクトを移動、回転、サイズ変更すると、それに従います。マッピングタイプの詳細については、[テクスチャマッピング](http://docs.mcneel.com/rhino/5/help/en-us/index.htm#properties/texturemapping.htm)とトピックを参照してください。

![images/mapping-cube.png](images/mapping-cube.png) ![images/mapping-planar.png](images/mapping-planar.png)
*2つの異なるマッピング方向*

### ![images/decalproperties.png](images/decalproperties.png) デカール
{: #decals}
デカールは、オブジェクトにマテリアルを用いて間接的にではなく直接適用できるタイリングしない画像マップです。デカールは、オブジェクトの色、反射、またはバンプの一部に変更を加えるのに用います。デカールの作成、配置についての詳細は、[Rhinoのデカール](http://docs.mcneel.com/rhino/5/help/en-us/index.htm#properties/decal.htm)を参照してください。

![images/freshmilk.png](images/freshmilk.png) ![images/decal-planar-001.png](images/decal-planar-001.png)
![images/cylindricaldecal-002.png](images/cylindricaldecal-002.png) ![images/uvmapdecal-00.png](images/uvmapdecal-00.png)
*4つの異なるデカールの例*

### ![images/apply-edge-softening.png](images/apply-edge-softening.png) カスタムメッシュ
{: #custom-meshes}
いくつかのカスタムメッシュのモディファイアーがRhinoでレンダリングモデルの詳細化に使用できます。これらのモディファイアーを用いると、エッジを丸めたり、パネルのシャットラインを加えたり、曲線からケーブル線を作成することができます。

詳細については、次のトピックを参照してください。

>[ソフトエッジ](http://docs.mcneel.com/rhino/5/help/en-us/index.htm#commands/applyedgesoftening.htm)
>[曲線パイプ](http://docs.mcneel.com/rhino/5/help/en-us/index.htm#commands/applycurvepiping.htm)
>[シャットライン](http://docs.mcneel.com/rhino/5/help/en-us/index.htm#commands/applyshutlining.htm)
>[ディスプレイスメント](http://docs.mcneel.com/rhino/5/help/en-us/index.htm#commands/applydisplacement.htm)

### ![images/object-flamingo.PNG](images/object-flamingo.PNG) Flamingoのプロパティ
{: #flamingo-properties}

#### アルファチャンネル
{: #alpha-channel}
オブジェクトを非表示にします。オブジェクトによって付けられた影、そしてオブジェクト上の影はレンダリングされます。そのイメージを他のイメージに重ねると、合成イメージに影を表示することができます。

![images/building.png](images/building.png)
上の例では、イメージにぴったりと合ういくつかの単純な平面サーフェスを作成し、「木」によって建物に投じられた影を「捕まえ」ました。平面はアルファチャンネルプロパティがオンにされているので、レンダリングの際に表示されず、影だけが表示されました。この部分的に透明なイメージが建物のイメージに重ねられ、右のイメージが完成しました。

#### コースティックス
{: #caustics}
曲面によって反射または屈折された光線、またはこれらの他のサーフェス上への投影です。コースティックスは、非常に特殊な状況に用います。コースティックスは、[パストレーサー](render-tab.html#path-tracer)エンジン、または[ハイブリッド](render-tab.html#hybrid)レンダリングエンジンのみを用いでレンダリングされます。コースティックスの計算は、収束するのに多くのパスを用います。詳細については、[Wikipediaの記事: Caustic (optics)](http://en.wikipedia.org/wiki/Caustic_(optics))を参照してください。

![images/kaustik.png](images/kaustik.png)
*ガラスのコップに入った水によるコースティックス*

![images/caustics-001.png](images/caustics-001.png)
*コースティックスなし（左）、コースティックスあり（右）*

#### 薄面
{: #thin}
空間を包括した透明なオブジェクトは屈折の際に通常、ソリッドとして扱われます。薄面プロパティを設定すると、屈折の際にそれぞれのサーフェスが2面のオブジェクトとして扱われます。これは、ガラスなど、一枚のサーフェスが建築モデルに用いられる際に使用する設定です。

![images/thin.png](images/thin.png) ![images/thinoff.png](images/thinoff.png)
*ベースのRhinoモデル（左）、通常（中）、薄面（右）*

#### 昼光ポータル
{: #daylight-portal}
昼光ポータルは、屋内レンダリングの[太陽と空の照明](lighting-tab.html#interior-daylight)の入口です。昼光ポータルは、太陽、空、そして地面の光を自然な形で屋内空間に引き込みます。昼光ポータルは、[太陽](sun-and-sky-tabs.html#sun)がオンの場合のみに効果があります。照明スキームが[屋内昼光](lighting-tab.html#interior-daylight)に設定されている場合、すべての透明なサーフェスは自動的に昼光ポータルとして機能します。照明スキームがスタジオまたは屋外昼光に設定されている場合のみ、外の太陽や空の光を屋内空間に取り入れたい場合は、手動で窓に昼光ポータルを設定しなければなりません。

![images/daylightportal-001.png](images/daylightportal-001.png)
*昼光ポータルがオン（左）、昼光ポータルがオフ（右）*

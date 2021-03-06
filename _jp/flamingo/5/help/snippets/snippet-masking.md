
### マスキング
画像に保存された色値またはアルファチャンネルに基づいて画像の指定部分を覆い隠します。このことによって、テクスチャの境界を複雑な形状にすることが可能になり、サーフェスの穴など、複雑な効果を作成することができるようになります。

この例では、長方形のサーフェスにアルファチャンネル背景のある画像がデカールとして配置されています。マテリアルのマスキングも同じ要領で行えます。

![images/airplane.png](images/airplane.png)  ![images/masking-004.png](images/masking-004.png)
*元のデカール画像。グレーのチェッカーの部分は、画像のアルファチャンネルを表しています。*

マスキング情報は、ビットマップの下の情報を指定して取得できます。

> [なし](#nomask)
> [アルファチャンネル](#alphamask)
> [色](#colormask)

#### なし
{: #nomask}
マスキングが設定されていない場合、画像は下のマテリアルを覆い隠します。マスキングを設定すると、アルファチャンネルまたはマスキング色がある部分では、マテリアルがイメージを通して見えるようになります。この例では、平面サーフェスに割り当てられたマテリアルに赤いベース色が用いられています。

![images/masking-002.png](images/masking-002.png)
*マスキングが設定されていない（左）場合は画像がサーフェスを隠します。マスキングが設定されている（右）場合は赤いマテリアルが透けて見えます。*

#### アルファチャンネル
{: #alphamask}
（アルファチャンネルがある場合、）画像の[アルファチャンネル](environment-tab.html#alpha)を用いてマスク領域を定義します。

![images/airplane.png](images/airplane.png)  ![images/masking-004.png](images/masking-004.png)
*左が元の画像。グレーのチェッカーの部分は、画像のアルファチャンネルを表しています。右は、画像を水のサーフェス上に配置したものです。*

アルファチャンネルは、透明度情報のために用いられるそれぞれのピクセルデータの一部です。アルファチャンネルは、色の変更、フィルタ、その他の効果を画像に適用する際に画像の一部を隔離して保護できるマスクを作成、保存します。画像の各ピクセルは、赤、緑、青（RGB）の混合を定義する複数のデータチャンネルで表現されます。 アルファチャンネルは、下にあるピクセルの色をマスクする、画像の8ビット（256階調）のグレースケール表現です。アルファマスクの値がピクセル色の強度を決定します。アルファチャンネルが100%の場合、画像のピクセルは完全に透明になります。そうでない場合、画像のピクセルは透明度とブレンドされます。

#### 色
{: #colormask}
画像にアルファチャンネルがない場合、画像の色をマスクとして指定することができます。感度設定を使用すると、マスク色としての1つの指定色へのマスク感度を設定することもできます。色オプションを選択すると、スポイト、カラーセレクタ、感度コントロールが使用できるようになります。

#### スポイト
クリックしてビットマップからマスク色を選択します。スポイトをクリックしてから、ビットマップをクリックして色をピックします。このコントロールは、色オプションが選択されている場合のみに使用可能です。

{% include_relative snippets/snippet-material-color-select.md %}

#### 感度
値は、色の周囲の（一緒にマスクされる）領域のサイズを示します。カラーマスキングを行うには、この設定が0.0より大きくなければなりません。このコントロールは、色オプションが選択されている場合のみに使用可能です。

#### ブラー
部分的にピクセルをマスクします。値は、マスクされる色周囲の部分的マスクの度合いを決定します。このコントロールは、色オプションが選択されている場合のみに使用可能です。

#### 反転
マスクを反転します。マスクされていたピクセルが含まれ、含まれていたピクセルがマスクされます。

![images/masking-007.png](images/masking-007.png)  

#### 透明
下にあるオブジェクトのマスクされた部分を透明にし、オブジェクトの背後の背景や他のオブジェクトをオブジェクトを透かして見えるようにします。通常、その部分のオブジェクトのマテリアルが見えるようになります。

透明なマスキングは、影をより自然に見えるようにし、また背景オブジェクトが見えるようにします。 下にあるマテリアルを透明にすることもできますが、時にはサーフェスの他の部分は不透明にしたままで、デカールの後ろのサーフェスを透明にすると便利です。

![images/masking-003.png](images/masking-003.png)    ![images/masking-004.png](images/masking-004.png)

#### マスクされる色を表示
パラメータを変更すると、そのマスキング効果が表示されます。マスクされるピクセルの表示色を選択するには、[カラーセレクタ](select-color.html) ![images/colorswatch-001.png](images/colorswatch-001.png)を使用します。 この色やチェックボックスの設定を変更しても、マスクの色は変わりません。 これは、単にマスクを編集する際に使用するグラフィカルツールです。

![images/masking-008.png](images/masking-008.png)

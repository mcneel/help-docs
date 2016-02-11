---
title: マテリアルエディタパネル
---

# ![images/paint.svg](images/paint.svg){: .inline} {{page.title}}
マテリアルは、サーフェス仕上げの色、反射、透明度、テクスチャ、そしてバンプマップの仕様を含んでいます。すべてのマテリアルには、基本設定があります。デフォルトのマテリアルは、白で艶がなく、反射や透明度もありません。最良の結果を得るには、Flamingo特有のマテリアルを使用してください。

マテリアルは、レイヤ、オブジェクト、そしてブロックに割り当てることができます。割り当ては、オブジェクトへドラッグアンドドロップすることで、またいろいろなコントロールを使用して行えます。詳細については、[マテリアルの割り当て](material_assignment.html)を参照してください。

マテリアルは割り当てると、モデルに格納されます。 マテリアル、テクスチャ、そしてレンダリングのすべてのサポートファイルは、Rhinoのモデルに正しく設定した[レンダリングのオプション](http://docs.mcneel.com/rhino/5/help/ja-jp/index.htm#options/rendering.htm)と共に格納することができます。

マテリアル、環境、そしてテクスチャはモデルに格納されますが、レンダリングコンテンツはモデル間で共有できるファイルに保存することもできます。コンテンツはRhinoのセッション間で、そしてフォルダにドラッグできます。色見本も同じようにドラッグアンドドロップできます。[ライブラリパネル](libraries.html)はデフォルトのコンテンツフォルダを表示します。これを、モデルにコンテンツをドラッグアンドドロップするのに、またはモデルコンテンツを外部ファイルにドラッグアンドドロップするのに使用してください。

![images/material_editor_panel.svg](images/material_editor_panel.svg){:  #panel_map .float-img-right}

##### コマンドの位置
マテリアルをタブを表示する方法には、いくつかのオプションがあります。

* ![images/materialtab.png](images/materialtab.png){: .inline} マテリアルタブ
* ![images/icon-render.png](images/icon-render.png){: .inline} レンダリングツールツールバー > ![images/materialtab.png](images/materialtab.png){: .inline} マテリアルエディタ
* メニュー > レンダリングプルダウン > マテリアルエディタ
* コマンドラインでMaterialEditorと入力

マテリアルエディタパネルは、複数のセクションに分かれています。選択されたマテリアルのタイプに応じて、マテリアルプロパティは異なることがあります。

色やテクスチャは色見本からドラッグして、どのような他の色見本、またはマテリアルエディタ、[テクスチャパレット](texturepalette.html)、または[環境エディタ](environmenteditor.html)にもドロップすることができます。

##### マテリアルパネル

 1. [設定バー](#settings)
 1. [マテリアルリスト](#material_list)
 1. [ウィンドウ区切り線](#divider)
 1. [マテリアルのプロパティセクション](#properties)
 1. [名前](#name)
 1. [マテリアルのプロパティパネル](#panels)

## [設定バー](#panel_map) ![images/callout_1.svg](images/callout_1.svg){: .inline}
{: #settings .clear-img}
このバーを使用すると、マテリアルのリストを順番に表示することができます。

#### ![images/met_leftarrow.png](images/met-leftarrow.png){: .inline} 戻る矢印
現在のマテリアルまたは以前に選択されたマテリアルに戻ります。例えば、テクスチャのあるマテリアルには複数の層があります。テクスチャの詳細から親マテリアルに戻るのにこの矢印を使用してください。

####  ![images/met_rightarrow.png](images/met-rightarrow.png){: .inline} 進む矢印
現在のマテリアルまたは以前に選択されたマテリアルから戻ります。例えば、テクスチャのあるマテリアルには複数の層があります。親マテリアルから最近使用したテクスチャに戻るのにこの矢印を使用してください。


#### ![images/material_editor.png](images/material_editor.png){: .inline} ![images/texture-2dchecker.png](images/texture-2dchecker.png){: .inline} 現在選択されているマテリアル名
現在のマテリアル名とレベルを表示します。例えば、テクスチャまたはマテリアルプロシージャルレベルがある場合、「>」が表示されます。どのマテリアル、またはマテリアルのどのレベルを編集しているのかを確認できる場所です。

#### ![images/library_default.png](images/library_default.png){: .inline} ツールメニュー
[ツールメニュー](#tools-menu)を表示します。マテリアルに関するコマンド、設定、ユーティリティの包括的なメニューです。


## [マテリアルリスト](#panel_map) ![images/callout_2.svg](images/callout_2.svg){: .inline}
{: #material_list}
ここにはモデルに含まれるすべてのマテリアルが表示されます。リストを使って次のことが行えます。

* リストを上下にスクロールして、モデルのすべてのマテリアルを見ることができます。
* このリストから[レイヤパネル](http://docs.mcneel.com/rhino/5/help/ja-jp/index.htm#commands/layer.htm)のレイヤに、またはオブジェクトにマテリアルを直接ドラッグアンドドロップしてオブジェクトに割り当てることができます。詳細については、[マテリアルの割り当て](material_assignment.html)を参照してください。
* 新規マテリアル追加ボタン ![images/add_material.png](images/add_material.png){: .inline} を使用して、リストの一番最後に新規マテリアルを追加することができます。


* それぞれのマテリアルをクリックして選択できます。選択されると、マテリアルのプロパティが下のパネルに表示されます。詳細については、[レンダリングマテリアルのプロパティ](#properties) を参照してください。
* サムネイルを右クリックすると、マテリアルコンテクストメニューを表示できます。
* 何も表示されていない部分を右クリックすると、新規マテリアルのコンテクストメニューを表示することができます。

###  ![images/add_material.png](images/add_material.png){: .inline} 新規マテリアルを追加
{: #add_material}
追加アイコンは、マテリアルリストを一番下までスクロールしたところに表示されます。

マテリアルのレンダリングコンテクスト[ライブラリ](libraries.html)を開きます。
ライブラリのマテリアルは、モデルのマテリアルを作成するためのテンプレートしての役割をします。

### マテリアルのコンテクストメニュー
{: material_context}
このメニューは、マテリアルリストを右クリックすると表示されます。このメニューに表示される多くのオプションの詳細については、[ツールメニュー](#tools_menu)を参照してください。

### 新規マテリアルのコンテクストメニュー
{: new_material_context}
このメニューは、マテリアルリストの何も表示されていない部分を右クリックすると表示されます。

#### ![images/toolbarlus.png](images/toolbarplus.png){: .inline} 新規マテリアルを作成
新規の基本の艶なしで白のマテリアルを作成します。


#### ![images/paste.png](images/paste.png){: .inline} ペースト
クリップボードの内容に基づいて新規マテリアルを作成します。

#### ![images/pasteasinstance.png](images/pasteasinstance.png){: .inline} インスタンスとしてペースト
クリップボードの内容に基づいて、インスタンシングによって元のマテリアルにリンクされている新規マテリアルを作成します。

#### ![images/grid.png](images/grid.png){: .inline} グリッド
プレビューをサムネイルのグリッドとして表示します。

#### ![images/list.png](images/list.png){: .inline} 一覧
プレビューをサムネイルの一覧として表示します。

#### ![images/tree.png](images/tree.png){: .inline} ツリー
プレビューをツリー表示します。（ネストを表示します。）

#### ![images/horizontal.png](images/horizontal.png){: .inline} 水平レイアウト
プレビューをコントロールの左側に表示します。

#### ![images/showpreview.png](images/showpreview.png){: .inline} プレビューペインを表示
現在選択されているサムネイルのプレビューのプロパティを表示します。プレビューの形状、サイズ、背景、回転動作を設定します。

#### ![images/floatthumbnail.png](images/floatthumbnail.png){: .inline} フロート
サイズ変更できるウィンドウにプレビューイメージをフロートします。

#### サムネイル

##### ![images/small.png](images/small.png){: .inline} 小
サムネイルを一番小さいサイズで表示します。

##### ![images/medium.png](images/medium.png){: .inline} 中
サムネイルを一番中ぐらいのサイズで表示します。

##### ![images/large.png](images/large.png){: .inline} 大
サムネイルを一番大きいサイズで表示します。

##### ![images/showlabels.png](images/showlabels.png){: .inline} ラベルを表示
グリッドモードの際にサムネイル名のラベルを表示します。
ラベルはリストモードでは常に表示されます。

##### ![images/showunits.png](images/showunits.png){: .inline} 単位を表示
モデル単位でサイズを表示します。

##### ![images/autoupdatethumbnail.png](images/autoupdatethumbnail.png){: .inline} プレビューを自動更新
設定を変更するとすべてのプレビューを自動的に更新します。

##### ![images/updateallpreviews.png](images/updateallpreviews.png){: .inline} すべてのプレビューを更新
プレビューを自動更新がオフの場合に、プレビューを手動で更新します。

## [ウィンドウ区切り線](#panel_map) ![images/callout_3.svg](images/callout_3.svg){: .inline}
{: #divider}
区切り線をドラッグしてマテリアルリストの長さを変更します。マテリアルリストを長くすると、マテリアルのプロパティセクションが短くなります。

## [マテリアルのプロパティセクション](#panel_map) ![images/callout_4.svg](images/callout_4.svg){: .inline}
{: #properties}

#### [マテリアル名](#panel_map) ![images/callout_5.svg](images/callout_5.svg){: .inline}
{: #name}
マテリアルの名前です。マテリアルをライブラリにエクスポートする際にファイル名としても保存されます。メモ: マテリアルはRhinoのモデルに保存されます。それぞれのマテリアルは異なるRhinoのモデルで同じ名前を持つことができます。

#### [マテリアルパネル](material-editor.html#panel_map) ![images/callout_6.svg](images/callout_6.svg){: .inline}
{: #panels}
マテリアルのプロパティセクションには、多くのマテリアル指示パネルが表示されます。グレーのタイトルバーをクリックすると、マテリアルパネルを折りたたんで内容を隠すことができます。タイトルバーを再度クリックすると、内容が表示されます。

マテリアルパネルは、マテリアルのタイプによって、そして現在のアクティブなマテリアルレベルによって異なります。それぞれのマテリアルパネルの詳細については、[Flamingoのマテリアル](material-type-simple.html)を参照してください。

## ツールメニュー ![images/library_default.png](images/library_default.png){: .inline}
{: #tools-menu}
<!-- This comes from the page http://docs.mcneel.com/rhino/5/help/en-us/popup_moreinformation/materialthumbnail_contextmenu.htm -->
これらの設定は、サムネイルプレビューやサムネイル背景の右クリックコンテクストメニューにも表示されます。

#### ![images/assigntoobjects.png](images/assigntoobjects.png){: .inline} 選択に割り当て
現在のマテリアルを選択されたオブジェクトに割り当てます。

##### マテリアルをオブジェクトに割り当てるには
 1. 選択に割り当てをクリックします。
 1. Rhinoのビューポートで、ターゲットオブジェクトを選択します。

##### オブジェクトを予め選択するには
 1. Rhinoのビューポートで、ターゲットオブジェクトを選択します。
 1. 選択に割り当てをクリックします。
ターゲットオブジェクトは、選択に割り当てをクリックする前でも後にでも選択できます。

##### マテリアルをオブジェクトにドラッグアンドドロップするには
 * マテリアルをサムネイルまたはリストからターゲットオブジェクトにドラッグします。
ドラッグアンドドロップは、一度に1つのオブジェクトに対して行えます。

#### ![images/assigntolayers.png](images/assigntolayers.png){: .inline} レイヤに割り当て
現在のマテリアルをレイヤに割り当てます。

##### マテリアルをレイヤに割り当てるには
 1. レイヤに割り当てをクリックします。
 1. レイヤを選択ダイアログボックスで、マテリアルを割り当てるレイヤのボックスにチェックマークを付けます。

##### レイヤパネルからマテリアルを割り当てるには
 1. [レイヤ](http://docs.mcneel.com/rhino/5/help/ja-jp/index.htm#commands/layer.htm)パネルで、1つまたは複数のレイヤを選択し、[マテリアル](http://docs.mcneel.com/rhino/5/help/ja-jp/commands/layer.htm#Material)カラムをクリックします。
 1. レイヤのマテリアルダイアログボックスで、割り当てるマテリアルを選択します。


##### マテリアルをレイヤにドラッグアンドドロップするには
 * マテリアルをサムネイルまたはリストからターゲットレイヤにドラッグします。
ドラッグアンドドロップは、一度に1つのレイヤに対して行えます。

#### ![images/materials_selectobjects.png](images/materials_selectobjects.png){: .inline} オブジェクトを選択
モデルの中の選択されているマテリアルが割り当てられたオブジェクトを選択します。

#### ![images/toolbarplus.png](images/toolbarplus.png){: .inline} 新規マテリアルを作成
マテリアルのレンダリングコンテクスト[ライブラリ](libraries.html)を開きます。
ライブラリのマテリアルは、モデルのマテリアルを作成するためのテンプレートしての役割をします。

#### ![images/import.png](images/import.png){: .inline} マテリアルをファイルからインポート
保存されているRhinoの.rmtlファイルからマテリアルをインポートします。

#### ![images/savetofile.png](images/savetofile.png){: .inline} ファイルに保存
マテリアルをRhinoの.rmtlファイルに保存します。

#### ![images/changetype.png](images/changetype.png){: .inline} タイプを変更
マテリアルを異なるタイプに変更します。

#### ![images/changetype.png](images/changetype.png){: .inline} タイプを変更 (類似の設定をコピー)
マテリアルを異なるタイプに変更します。
デフォルトの動作は、[レンダリングのオプション](http://docs.mcneel.com/rhino/5/help/ja-jp/popup_moreinformation/materialtoolsmenu.htm) &gt;  [コンテンツのタイプが変更された際に類似の設定をコピー](http://docs.mcneel.com/rhino/5/help/ja-jp/popup_moreinformation/materialtoolsmenu.htm)ボックスの現在の状態に依存します。チェックマークが付いている場合、古いコンテンツから互換性のある設定が新しいコンテンツにコピーされます。

#### ![images/reset.png](images/reset.png){: .inline}  デフォルトにリセット
すべてのマテリアル設定をデフォルトの白、艶なし、反射なし、テクスチャなしのマテリアルに変更します。

#### ![images/copy.png](images/copy.png){: .inline} コピー
選択されたマテリアルをWindowsのクリップボードコピーします。その後、クリップボードの内容をエディタにペーストして新規マテリアルを作成したり、直接フォルダにペーストして[ライブラリ](libraries.html)ファイルを作成することができます。

#### ![images/paste.png](images/paste.png){: .inline} ペースト
クリップボードの内容に基づいて新規マテリアルを作成します。

#### ![images/pasteasinstance.png](images/pasteasinstance.png){: .inline} インスタンスとしてペースト
クリップボードの内容に基づいて、インスタンシングによって元のマテリアルにリンクされている新規マテリアルを作成します。

#### ![images/delete.png](images/delete.png){: .inline} 削除
選択されたマテリアルを削除します。

#### ![images/rename.png](images/rename.png){: .inline} 名前を変更...
選択されたマテリアルの名前を変更します。

#### ![images/duplicate.png](images/duplicate.png){: .inline} 複製
選択されたマテリアルを同じ設定でコピーし、新規マテリアルを作成します。

#### ![images/removeinstancing.png](images/removeinstancing.png){: .inline} インスタンシングを取り除く
[インスタンスされた](http://docs.mcneel.com/rhino/5/help/ja-jp/popup_moreinformation/materialtoolsmenu.htm)マテリアル間の接続を取り除きます。
{% include_relative snippets/snippet-contenteditorpreviewoptions.md %}


#### ![images/contentfilter.png](images/contentfilter.png){: .inline} コンテンツフィルタ
[コンテンツフィルタ](content_filters.html)ダイアログボックスを開きます。

#### ![images/rename.png](images/rename.png){: .inline} プロパティ
[プレビューのプロパティ](http://docs.mcneel.com/rhino/5/help/ja-jp/popup_moreinformation/materialtoolsmenu.htm)ダイアログボックスを開きます。

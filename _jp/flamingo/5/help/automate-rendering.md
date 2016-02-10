---
title: レンダリングの自動化
---

# {{page.title}}


## バッチレンダリング
{: #batch-rendering}
バッチジョブでは、複数のジョブを送信し、自動的にレンダリングできます。特定のビュー、解像度、パスの数の指定が可能です。バッチレンダリングは単一でも[レンダーファーム](render-farm.html)に送信しても開始できます。バッチリストを開き、リストにジョブを追加してください。バッチジョブリストはモデルに保存されます。

##### コマンドの位置

 * メニュー > Flamingo nXt 5.0 > その他のツール > バッチレンダリング

### バッチレンダリングダイアログ
{: #batch-render}
まずジョブを追加し、それからプロパティを編集して、バッチジョブを設定します。

#### 追加
それぞれのバッチジョブは、モデルに保存されたビューに基づいています。「追加」をクリックし、モデルのビューリストからビューを選択します。ジョブが追加され、選択されると、他のメニューアイテムが使用できるようになります。

#### 削除
既存のバッチジョブを選択し、「削除」を使用すると、バッチリストからジョブが削除されます。

#### プロパティ
既存のバッチジョブを選択し、「プロパティ」を使用すると[バッチレンダリングのプロパティ](#batch-render-properties)を設定できるようになります。プロパティでは、それぞれのジョブのファイル名、解像度、そしてパスの数などを設定できます。

#### 上へ移動
リストでビューポート名を1つ上に移動します。

#### 下へ移動
リストでビューポート名を1つ下に移動します。

#### バッチリスト
{: #batch-list}
レンダリングされるビューのリストの情報を表示します。既存のジョブをダブルクリックすると、[バッチレンダリングのプロパティ](#batch-render-properties)を設定または編集できます。

#### レンダリングの進行状況
バッチ処理の進行状況のパス、スキャンライン、経過時間の情報を表示します。

####  レンダリングを停止
バッチ処理を停止します。

#### バッチをローカルでレンダリング
{: #render-batch-locally}
バッチジョブをレンダリングするのに現在のコンピュータのみを使用します。レンダリングイメージは
[バッチレンダリングのプロパティ](#batch-render-properties)で指定された場所に出力されます。

####  バッチをファームへ送信
バッチジョブを[レンダーファーム](render-farm.html)へ送信します。ジョブは使用できるすべてのファームクライアントでレンダリングされます。レンダリングイメージは共有ファームフォルダに出力されます。

### バッチレンダリングのプロパティ
{: #batch-render-properties}

#### レンダリングするビューポート
指定のジョブがレンダリングするビューを表示します。[レンダリングタブ、レンダリングするビューポート](render-tab.html#viewtorender)を参照してください。

#### ファイル名
保存ボタン ![images/saveimageas.png](images/saveimageas.png){: .inline} をクリックし、レンダリングイメージのファイル名を指定します。

#### アルファチャンネル
イメージをアルファチャンネルと一緒に保存します。詳細については、[アルファチャンネル背景を使用する](environment-tab.html#alpha)を参照してください。

#### ドキュメントの設定を使用
{: #rendering-resolution}
デフォルトでは、レンダリングに現在のドキュメントの解像度設定が使用されます。解像度を変更したい場合は、このボックスのチェックマークを外し、解像度を指定してください。詳細については、[レンダリングタブ、解像度](render-tab.html#resolution)のトピックを参照してください。

#### レンダリング停止条件パス
{: #rendering-constraints}
バッチジョブを終了するのに必要なパスの数を設定します。詳細については、[パス](documentproperties-flamingo.html#number-of-passes)のトピックを参照してください。

<!-- TODO: Flamingo nXt 5 runs from the RDK.  The need to Flamingo Automate render is not clear.  What is needed to run animations with nxt right now?
The number of passes and the ability to send a render to the farm are required still.  So the dialog should be smaller.
Alpha channel This needs to be investigated. The rest of this section is commented out.-->

<!-- Commented out until automated render can be determined

## アニメーション
{: #animation}
Rhinoでアニメーションを作成する方法には2通りあります。アニメーションは、[Rhinoのアニメーションツールバー](http://docs.mcneel.com/rhino/5/help/ja-jp/index.htm#commands/animation.htm)または[Bongo](http://bongo.rhino3d.com/)アニメーションプラグインを用いて設定することができます。

##### アニメーションジョブをレンダーファームに送信するには
1. [FlamingoNXtAutomateRender](automate-rendering.html#flamingonxtautomaterender)コマンドを実行します。
1. 自動レンダリングコマンドを設定ダイアログボックスで**ファームへレンダリング**を選択します。
&#160;
ジョブ名を指定し、OKボタンをクリックします。
&#160;
Rhinoのアニメーションセットアップツールバーからアニメーションのタイプを設定します。キャプチャ方法はフルレンダリングを選択します。
&#160;
アニメーションツールバーからアニメーションを記録します。レンダージョブがレンダーファームに送信されます。
&#160;
レンダーファームでジョブが完了したら、FlamingoNXtAutomateRenderコマンドを再度実行し、ダイアログのすべてのジョブを選択します。
&#160;
選択ファイルを指定出力フォルダへコピーボタンをクリックし、すべてのレンダリングイメージをコピーする先のフォルダを選択します。


## FlamingoNXtAutomateRenderコマンド
{: #flamingonxtautomaterender}


## 自動レンダリングコマンドを設定

### オン
デフォルトの**Render**コマンドを**レンダーファーム**を使用させるようにします。

### デフォルトのレンダリングダイアログを使用
**Render**コマンドを（ファームにではなく）直接レンダリングするように設定を戻します。

### レンダリングするレンダリングパスの数
レンダリングパスの数を指定します。

### ファームへレンダリング
**Render**コマンドをファームへレンダリングするようにします。

### ジョブ名
**レンダーファームの** [ジョブ名](automate-rendering.html#job-name)を指定します。

## レンダリング停止条件

### レンダリングするレンダリングパスの数
[パスの数](documentproperties-flamingo.html#number-of-passes)を指定します。

### アルファチャンネルを保存
[アルファチャンネル](render-window.html#save-with-alpha-channel)背景を保存します。
-->

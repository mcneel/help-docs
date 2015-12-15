---
title: Flamingoをはじめるにあたって
---


# ![images/flamingotab.svg](images/flamingotab.svg) Flamingo nXt&#174;をはじめるにあたって
Flamingo nXtは、3Dモデルから高品質でフォトリアリスティックな静止およびアニメーションの画像ファイルをRhinoceros &#174;の中で作成します。Flamingo nXt 5は、Flamingoへのアップデートで、Rhino 5にビルトインレンダリング機能を統合します。これは現在ワーク・イン・プログレス・バージョンです。

Flamingoは、[Flamingo nXt 5 ダウンロード](http://www.rhino3d.com/download/flamingo/5/beta)からダウンロード、インストールしていただけます。

[Flamingo Discourse Forum（フォーラム）](http://discourse.mcneel.com/c/rendering/flamingo)では、テクニカルディスカッションに参加していただけます。

## インストール

* Flamingo 5 ベータには、以前のバージョンのFlamingo nXtがインストールされていることが必要です。
* Flamingo nXt 5を実行するには、Rhino 5 サービスリリース12が必要です。

RHIインストーラをダウンロード、実行後にRhinoを起動してください。

テクニカルサポート、チュートリアル、例、**Flamingo nXt**をはじめるにあたっての情報については、[Flamingo nXtのウェブサイト](http://nxt.flamingo3d.com/)（英語、一部日本語）をご覧ください。

> [チュートリアル](http://nxt.flamingo3d.com/page/tutorials-and-documentation)
> [ギャラリー](http://nxt.flamingo3d.com/photo)
> [テクニカルサポート](http://nxt.flamingo3d.com/forum)

## Flamingo nXtのコントロールパネル
{: #control-panel}
このバージョンのFlamingoはインターフェイスがRhino 5のレンダリングツールと統合されます。Flamingo nXtのコントロールパネルには、レンダリングのためにモデルを設定するためのタブが表示されます:

> [マテリアル](materials-tab.html)
> [照明](lighting-tab.html)
> [環境](environment-tab.html)
> [レンダリング](render-tab.html)

## Flamingoのコントロールパネルを表示するには
* Flamingo nXt 5.0メニューのコントロールパネルをクリックします。

## レンダリングの基礎
{: #rendering-basics}
完成したモデルのレンダリングは次の4つの基本手順で行います。

 1. [マテリアルの設定](material-editor.html)
 1. [照明の設定](lighting-tab.html)
 1. [環境の設定](environment-tab.html)
 1. [レンダリング条件の設定](render-tab.html)

##### レンダリングを開始するには
* レンダリングまたはFlamingo nXtメニューのレンダリングをクリックします。
* または、標準ツールバーのレンダリングボタンをクリックします。

### レンダリングを停止
デフォルトで、レンダリングプロセスはレンダリングを停止ボタンをクリックするまでパス毎にイメージのリファイン（より詳細なレンダリング）を続けます。このボタンを使うと、時間と質のバランスを取ることができます。レンダリングを長く続けるほど、完全に収束した結果に近づきます。レンダリングはいつでも好きな時に中止することができます。

###  レンダリングを再開
レンダリングを停止ボタンをクリックすると、現在処理中のパスが完了した後にレンダリングが停止されます。
レンダリングが停止すると、ボタンの表示はレンダリングを再開に変わります。レンダリング停止条件で設定した時間またはパスの数に達する前にレンダリングを停止した場合、レンダリングを再開ボタンを押すとレンダリングが続行されます。

自動停止条件を設定するには、 [レンダリングウィンドウ](render-window.html)または[ドキュメントのプロパティ Flamingo nXt](documentproperties-flamingo.html)の[パスの数](render-window.html#number-of-passes)または[時間](render-window.html#time)設定を使用します。

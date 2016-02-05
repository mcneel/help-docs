---
title: Flamingo nXt 快速入門
---
<!-- TODO: This page mentions "Work in Progress" and "Flamingo Beta" and has to be updated once Flamingo has been released -->

# ![images/flamingotab.svg](images/flamingotab.svg){: .inline} Flamingo nXt® 快速入門
Flamingo nXt 可在 Rhinoceros® 裡將模型彩現成為高品質而且真實的靜態影像。Flamingo nXt 5 目前還在開發階段，它將 Flamingo 與 Rhino 5 內建彩現功能整合在一起。

請至[這裡](http://www.rhino3d.com/download/flamingo/5/beta)下載、安裝 Flamingo nXt 5。

加入 [Flamingo Discourse 論壇](http://chinese.discourse.mcneel.com/c/flamingo)參與討論。

## 安裝

* Flamingo nXt 5 Beta 需要安裝 Flamingo nXt 才能使用。
* Flamingo nXt 5 Beta 需要 Rhino 5 SR12 才能執行。

下載後請執行 RHI 安裝程式。

**Flamingo nXt** 的技術支援、教學與範例等資訊請至 [Flamingo nXt 網站](http://nxt.flamingo3d.com/)。

* [教學](http://nxt.flamingo3d.com/page/tutorials-and-documentation)
* [作品](http://nxt.flamingo3d.com/photo)
* [技術支援](http://nxt.flamingo3d.com/forum)

## Flamingo nXt 的控制面板
{: #control-panel}
Flamingo nXt 5 整合了 Rhino 5 的彩現工具，Flamingo nXt 的控制面板內有模型彩現需要的設定頁面，包括：

* [材質](materials-tab.html)
* [照明](lighting-tab.html)
* [環境](environment-tab.html)
* [彩現](render-tab.html)

## 開啟 Flamingo 的控制面板
* 從 **Flamingo nXt 5.0** 功能表選擇**控制面板**。

## 基本彩現
{: #rendering-basics}
彩現模型的四個基本步驟：

 1. [設定材質](material-editor.html)
 1. [設定照明](lighting-tab.html)
 1. [設定環境](environment-tab.html)
 1. [設定彩現條件](render-tab.html)

##### 開始彩現
* 從**彩現**或功能表選擇**彩現**。
* 按**標準**工具列上的**彩現**按鈕。

### 停止彩現
Flamingo nXt 5 預設的彩現方式是會持續計算改善彩現影像的品質，直到您按下**停止彩現**按鈕才會停止。此方式讓您可以在時間與品質兩者之間取捨，彩現計算越久得到的效果越好，但您可以在任何時候停止彩現。

###  繼續彩現
按下**停止彩現**按鈕，待目前的彩現處理數完成後彩現計算會暫時停止。
停止彩現後按鈕會變為**繼續彩現**，如果您在處理數或時間限制到達前按下停止彩現，可以按**繼續彩現**繼續彩現計算。

[處理數](render-window.html#number-of-passes)與[時間](render-window.html#time)限制可在[彩現視窗](render-window.html)或[文件內容 > Flamingo nXt 5.0](documentproperties-flamingo.html) 頁面設定。

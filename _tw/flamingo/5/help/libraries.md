---
title: 材質庫面板
---

# ![images/libraries.svg](images/libraries.svg){: .inline} {{page.title}}
**Libraries** 指令可開啟材質庫面板，管理材質、貼圖、環境資料庫。

彩現內容可匯出至檔案再匯入其它模型、從 Rhino 裡拖放至外部的資料夾，或是在兩個 Rhino 視窗之間拖放。

顏色方塊的顏色也可以如此操作。

材質庫面板可顯示您設定的資料夾，材質庫面板裡的項目也可以使用拖放操作。

材質是儲存在硬碟上的檔案，材質庫資料夾也只是一般的 Windows 資料夾。

材質庫面板上方的位址列可瀏覽至電腦上的任何資料夾。

按右上方的板手圖示可快速回到預設的材質庫資料夾。 ![images/library_default.png](images/library_default.png){: .inline}

#### 管理材質庫
{: organizing_libraries}
材質與材質庫資料夾可像在檔案總管裡一樣複製、剪下、貼上，也可以直接在 Windows 檔案總管裡操作，[材質庫設定](#settings)可編輯預設的材質庫資料夾 ![images/library_default.png](images/library_default.png){: .inline}。

## 材質庫
{: #material}
當您將一個材質加入模型後，該材質的複本會儲存在模型檔案裡，編輯儲存在模型檔案裡的材質複本不會影響原來在材質庫資料夾裡的材質。

材質可使用拖放的方式加入模型，材質可：

#### 賦予給圖層
將材質拖放至圖層面板的圖層名稱，物件預設使用它所屬的圖層的材質，要更換圖層的材質時只要將另一個材質再拖放至該圖層即可替換材質。

#### 賦予給物件
將材質拖放至作業視窗裡的物件，物件的材質賦予方式會從**圖層**變為**物件**，物件將使用自己的材質，忽略圖層的材質。

#### 賦予給圖塊
將材質拖放至圖塊引例時，圖塊引例裡**材質賦予方式**設為**父物件**的物件將使用圖塊引例的材質。

## 植物庫
{: #plant}
材質庫資料夾裡有植物庫資料夾的捷徑，您可以將植物從植物庫拖放至作業視窗建立植物的複本。植物的複本會儲存在模型檔案裡，編輯儲存在模型檔案裡的植物複本不會影響原來在植物庫裡的植物。詳細的說明請參考[植物](plants.html)。

## 環境庫
{: #environment}
環境可以儲存在環境庫裡，以便在其它模型使用，詳細說明請參考[環境](environment-tab.html)。

## 材質庫設定
{: #settings}
從 ![images/options.png](images/options.png){: .inline}材質資料庫選項可變更 ![images/library_default.png](images/library_default.png){: .inline} 功能表顯示的資料夾。

##### 可以在哪找到這個指令?
材質資料庫選項可從三個地方開啟。

 1. 材質庫標籤 > 材質庫面板右上角的 ![images/library_default.png](images/library_default.png){: .inline} > 設定...
 1. 功能表 > 工具 > 選項 > 材質庫
 1. 功能表 > 面板 > 材質庫


### 顯示彩現內容
開啟預設的材質庫資料夾。

#### 使用預設的資料夾
預設的[材質庫](libraries.html)資料夾是 **%APPDATA%\McNeel\Rhinoceros\5.0\Localization\zh-TW\Render Content** 資料夾。

#### 自訂
自訂預設的[材質庫](libraries.html)資料夾的位置。

##### 瀏覽按鈕
選擇要使用的資料夾。

#### 顯示"文件"資料夾
在[材質庫面板](libraries.html)的功能表顯示"文件"資料夾。

#### 顯示自訂的資料夾
在[材質庫](libraries.html)面板的功能表顯示其它資料夾。

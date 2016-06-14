---
title: 賦予材質
---

# ![images/paint.svg](images/paint.svg){: .inline} {{page.title}}
場景裡的物件可擁有彩現使用的材質，材質有不同的賦予方式，每種方式都有其優缺點，必需考量後續修改材質的方便性來選擇適當的賦予方式。

材質有三種賦予方式：圖層、父物件、物件，這三者有層級關係，後者可覆蓋前者。

 1. [圖層](#bylayer) - 物件預設使用圖層的材質，除非物件的材質賦予方式是設為父物件或物件。
 2. [父物件](#byparent) - 賦予圖塊引例 (父物件) 材質時，圖塊裡材質賦予方式設為**父物件**的物件會使用圖塊引例的材質。
 3. [物件](#byobject) - 將材質直接賦予給物件，忽略圖層與與圖塊引例的材質。

將物件的材質賦予方式設為**圖層**是建議使用的方法，可方便改變一個圖層上所有物件的材質。如果一個圖層上只有少數幾個物件使用不同的材質，可將這些物件的材質賦予方式設為**物件**。

匯入的物件可能帶有材質，大部分匯入的物件的材質賦予方式是設為**物件**，要全部改成**圖層**可能要花不少時間，但如果後續需要經常對材質做修改，花點時間將材質賦予方式全部改為**圖層**是值得的。 

材質賦予後會儲存在模型檔案裡，編輯一個模型的材質不會影響其它模型裡的材質。

## 將材質賦予給圖層
{: #bylayer}
物件預設使用賦予給圖層的材質，按[圖層面板](http://docs.mcneel.com/rhino/5/help/zh-tw/commands/layer.htm)圖層後方的**材質欄**可改變圖使用的材質。
附註：從[材質編輯器](material-editor.html)刪除物件本身使用的材質會使物件的材質賦予方式變更為**圖層**。

##### 將材質拖放至圖層
{: #drag-dropmaterialtolayer}
1. 開啟 Rhino 的[圖層](http://docs.mcneel.com/rhino/5/help/zh-tw/commands/layer.htm)面板。
1. 從**材質庫**或**材質編輯器**面板的[材質清單](material-editor.html#material_list)，將材質拖放至[圖層面板](http://docs.mcneel.com/rhino/5/help/zh-tw/commands/layer.htm)的圖層上。

##### 賦予材質給圖層
1. 開啟 Rhino 的[圖層](http://docs.mcneel.com/rhino/5/help/zh-tw/commands/layer.htm)面板。
1. 選取一個或數個圖層，按圖層的**材質**欄。
1. 在**圖層材質**對話框選擇一個材質。

##### 移除圖層的材質
{: #detachmaterialfromlayer}
1. 開啟 Rhino 的[圖層](http://docs.mcneel.com/rhino/5/help/zh-tw/commands/layer.htm)面板。
1. 選取一個或數個圖層，按圖層的**材質**欄。
1. 在**圖層材質**對話框選擇**預設材質**。

## 賦予材質給父物件
{: #byparent}
材質賦予方式中的**父物件**較罕用，它讓圖塊引例裡的物件可以使用圖塊引例的材質，或圖塊引例所屬圖層的材質。

以汽車圖塊為例，圖塊裡的輪子與輪框分別屬於兩個圖層，兩個圖層使用不同材質。假使汽車模型的圖塊引例插入模型時車身需要有顏色變化，您可將圖塊裡車身的材質賦予方式設為**父物件**，讓車身使用圖塊引例所在圖層的材質，輪子與輪框的材質不因圖層不同而異。

##### 從物件內容賦予材質
1. 選取物件。
1. 從**編輯**功能表選擇 ![images/properties.png](images/properties.png){: .inline} **物件內容**。
1. 將[內容](properties-object.html)面板**材質**頁面 ![images/materialtab.png](images/materialtab.png){: .inline} 的**材質賦予方式**設為**父物件**。

## 將材質賦予給物件
{: #byobject}
您可將材質庫裡的材質賦予給圖層或物件， Rendering materials are assigned to individual objects and are used by Rhino's built-in renderer.
請參考：[材質編輯器](material-editor.html)

將物件的材質賦予方式設為"圖層"是建議使用的方法，如果一個圖層上只有少數幾個物件使用不同的材質，您又不想為了這些物件建立另一個圖層，這種情形可以將這些物件的材質賦予方式設為"物件"。

##### 從物件內容賦予材質
1. 選取物件。
1. 從**編輯**功能表選擇 ![images/properties.png](images/properties.png){: .inline} **物件內容**。
1. 將[內容](properties-object.html)面板**材質** 頁面 ![images/materialtab.png](images/materialtab.png){: .inline} 的**材質賦予方式**設為**物件**，從材質清單選擇一個材質。

##### 將材質拖放至物件
{: #drag-dropmaterialtoobject}

 * 從材質庫或材質編輯器面板的[材質清單](material-editor.html#material_list)將材質拖放至物件，當滑鼠游標停留在物件上時，物件會以醒目顏色提示將被賦予材質的物件。

##### 將材質賦予給選取的物件
1. 選取物件。
1. 在**材質編輯器**面板的[材質清單](material-editor.html#material_list)的一個材質上按滑鼠右鍵。
1. 在彈出的功能表選擇**賦予給選取的物件**。

##### 以材質選取物件
{: #select-objects-with-material-assignment}
1. 在**材質編輯器**面板的[材質清單](material-editor.html#material_list)的一個材質上按滑鼠右鍵。
1. 在彈出的功能表選擇**選取使用這個材質的物件**。

##### 移除物件的材質
{: #removematerialfromobject}
1. 選取物件。
1. 從**編輯**功能表選擇**物件內容**。
1. 將[內容](properties-object.html)面板**材質**頁面的**材質賦予方式**設為**圖層**。

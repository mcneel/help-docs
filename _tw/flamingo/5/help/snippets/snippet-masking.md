c
### 遮罩
遮罩可使用某個顏色或 Alpha 通道使圖片或物件的某一部分變透明，此功能可用來對圖片做去背處理。

這個例子中的圖片是以印花貼圖貼在一個矩形平面上，並以 Alpha 通道將圖片的背景變透明，一般材質貼圖的遮罩也可以這樣使用。

![images/airplane.png](images/airplane.png)  ![images/masking-004.png](images/masking-004.png)
圖片中灰白相間的棋盤格是圖片透明的部分。

遮罩有三種設定：

* [無](#nomask)
* [Alpha 通道](#alphamask)
* [顏色](#colormask)

#### 無
{: #nomask}
不使用遮罩時，物件的材質完全被貼圖遮蓋。遮罩可用顏色或 Alpha 通道將貼圖的某些部分變透明，讓材質的顏色可以透出貼圖。這個例子的矩形平面是使用紅色的材質。

![images/masking-002.png](images/masking-002.png)
不使用遮罩時 (左) 貼圖涵蓋整個平面，使用遮罩時 (右) 平面的紅色材質可以透出貼圖白色背景的部分。

#### Alpha 通道
{: #alphamask}
圖片本身內含的 [Alpha 通道](environment-tab.html#alpha)也可以拿來做為遮罩使用。

![images/airplane.png](images/airplane.png)  ![images/masking-004.png](images/masking-004.png)
原來的貼圖與使用 Alpha 通道遮罩去背的貼圖，棋盤格背景代表 Alpha 通道的範圍。

Alpha 通道是一個像素儲存的資訊的一部分，用來定義一個像素的透明度，Alpha 通道可用來保護圖片的某部分，使該部分不會受到圖片其它部分的顏色變更、濾鏡或其它效果的影響。圖片的每個像素都儲存了數個通道的資訊，例如 RGB (紅、綠、藍) 通道。Alpha 通道是 8 位元 (256 階) 的灰階色 ，灰階色的深淺代表該像素顏色可見性的強弱。如果一個像素的 Alpha 通道是 100%，代表此像素完全透明，0% 代表完全不透明。

#### 顏色
{: #colormask}
如果使用的圖片沒有 Alpha 通道，可以從圖片上指定一個顏色做為遮罩，寬容度數值可調整指定的顏色允許的色差範圍。當以顏色做為遮罩時，取色滴管、顏色方塊、寬容度與模糊度才可使用。

#### 取色滴管
按取色滴管按鈕，將滴管游標移動至圖片的縮圖上，按滑鼠左鍵指定顏色。當以顏色做為遮罩時，取色滴管按鈕才可使用。

{% include_relative snippets/snippet-material-color-select.md %}

#### 寬容度
設定顏色遮罩的擴散範圍，這個值必需大於 0 顏色遮罩才會有做用。當以顏色做為遮罩時，寬容度數值才可使用。

#### 模糊度
設定顏色遮罩邊界的模糊度，當以顏色做為遮罩時，模糊度數值才可使用。

#### 反轉
對調顏色遮罩作用與不作用的部分。

![images/masking-007.png](images/masking-007.png)  

#### 透明
使物在遮罩作用的部分變透明。

透明選項可以使用遮罩隱藏物件的某些部分，讓視線可以穿過物件看見物件背後的事物，並改變物件投射的陰影的形狀。

![images/masking-003.png](images/masking-003.png)    ![images/masking-004.png](images/masking-004.png)

#### 顯示遮罩顏色
以設定的顏色在預覽圖片上顯示透明遮罩，此顏色可任意改變，它與遮罩使用的顏色無關。

![images/masking-008.png](images/masking-008.png)

---
title: 自動化彩現
---

# {{page.title}}


## 批次彩現
{: #batch-rendering}
批次彩現可設定一個工作清單，自動連續彩現數個場景。批次工作可以設定要彩現的視圖、解析度、處理數。批次工作可在本機彩現，或傳送到[彩現農場](render-farm.html)，批次彩現的工作清單會儲存在模型裡。

##### 可以在哪找到這個指令?

 * 功能表 > Flamingo nXt 5.0 > 更多工具 > 批次彩現

### 批次彩現對話框
{: #batch-render}
從新增工作開始，然後編輯工作的內容完成設定。

#### 新增
每個批次工作代表儲存在模型裡的一個視圖，按**新增**，從視圖清單選取模型裡的一個視圖將它加入工作清單。有工作被選取時其它按鈕才能使用。

#### 刪除
選取一個批次工作，按**刪除**，將此工作從工作列表移除。

#### 內容
選取一個批次工作，按**內容**，開啟[批次彩現內容](#batch-render-properties)，可設定輸出的**檔案名稱**、**解析度**、**處理數**限制。

#### 上移
將選取的作業視窗名稱在清單中上移。

#### 下移
將選取的作業視窗名稱在清單中下移。

#### 批次清單
{: #batch-list}
要彩現的視圖清單，雙擊一個工作可編輯它的[批次彩現內容](#batch-render-properties)。

#### 彩現狀態
顯示批次彩現的進度資訊：處理數、掃描線、已使用時間。

####  停止彩現
中止進行中的批次彩現工作。

#### 本機批次彩現
{: #render-batch-locally}
只使用本機電腦彩現批次工作，彩現影像會輸出至[批次彩現內容](#batch-render-properties)裡設定的位置。

####  傳送批次工作至農場
將批次工作傳送至[彩現農場](render-farm.html)，使用所有可用的農場客戶端電腦合力彩現批次工作，彩現影像會輸出至共用的農場輸出資料夾。

### 批次彩現內容
{: #batch-render-properties}

#### 彩現的作業視窗
顯示批次工作彩現的視圖，進一步的說明請參考：[彩現標籤 > 彩現的作業視窗](render-tab.html#viewtorender)

#### 檔案名稱
按儲存按鈕 ![images/saveimageas.png](images/saveimageas.png) 指定彩現影像儲存的路徑與名稱。

#### Alpha 通道
在彩現影像裡儲存 Alpha 通道，進一步的說明請參考：[使用 Alpha 通道背景](environment-tab.html#alpha)

#### 使用文件設定
{: #rendering-resolution}
預設為使用目前文件的解析度設定彩現，消勾選此核取方塊可自訂彩現解析度，進一步的說明請參考：[彩現標籤 > 解析度](render-tab.html#resolution)

#### 彩現限制處理數
{: #rendering-constraints}
設定一個批次工作用來完成彩現的處理數，進一步的說明請參考：[處理數](documentproperties-flamingo.html#number-of-passes)

<!-- TODO: Flamingo nXt 5 runs from the RDK.  The need to Flamingo Automate render is not clear.  What is needed to run animations with nxt right now? Alpha channel This needs to be investigated. The rest of this section is commented out.-->

<!-- Commented out until automated render can be determined

## Animations
{: #animation}
There are two ways to create animations in Rhino.  Animations can be configured using [Rhino's Animation toolbar](http://docs.mcneel.com/rhino/5/help/en-us/index.htm#commands/animation.htm) or using the [Bongo](http://bongo.rhino3d.com/) animation plugin.

##### To submit an animation job to the render farm
1. Run the [FlamingoNXtAutomateRender](automate-rendering.html#flamingonxtautomaterender) command.
1. In the Configure Automated Render Command dialog, select **Render to farm**.
&#160;
Specify the Job name,and click the OK button.
&#160;
Set a type of animation from Rhino's Animation setup toolbar. Select Render Full as the Capture method.
&#160;
Record the animation from the Animation toolbar. The render jobs will be sent to Render Farm.
&#160;
When the jobs are finished in Render Farm, run the FlamingoNXtAutomateRender command again and select all the jobs in the dialog.
&#160;
Click the Copy selected files to specified output folder button and select a folder where all the render images will be copied to.


## FlamingoNXtAutomateRender command
{: #flamingonxtautomaterender}


## Configure Automated Render Command

### Enabled
Redirects the default **Render** command to use the **Render Farm**.

### Use default render dialog
Resets the **Render** command to render directly instead of to the farm.

### Number of render passes to render
Specifies the number of render passes.

### Render to farm
Redirects the **Render** command to render to the farm.

### Job name
Specifies the **Render Farm**  [Job name](automate-rendering.html#job-name).

## Render constraints

### Number of render passes to render
Specifies the [number of passes](documentproperties-flamingo.html#number-of-passes).

### Save alpha channel
Saves the [alpha channel](render-window.html#save-with-alpha-channel) background.
-->

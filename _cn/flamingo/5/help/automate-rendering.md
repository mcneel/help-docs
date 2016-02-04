---
Title: 自动化渲染
---

# {{page.title}}


## 批量渲染
{: #batch-rendering}
批量渲染让您可以一次性提交多个渲染任务按顺序自动进行渲染，批量渲染可以设置视图、分辨率与队列数。批量渲染可以直接通过本机进行，也可以发送到[渲染农场](render-farm.html)进行渲染，打开批量渲染列表，可以添加渲染任务，批量渲染列表是保存在模型中的。

##### 在哪里可以找到这个指令？

 * 功能表 > Flamingo nXt 5.0 > 更多工具 > 批量渲染

### 批量渲染对话框
{: #batch-render}
先添加渲染任务，然后编辑渲染任务的属性。

#### 新增
每个渲染任务都基于模型中的视图，点击新增按钮并从视图列表中选取一个视图，只有在列表中添加了任务，并且选中一个任务时，其他功能表选项才可以使用。

#### 删除
选取一个现有的任务，然后点击删除可以将其从批量渲染列表中删除。

#### 属性
选取一个现有的任务，然后点击属性可以设置[批量渲染属性](#batch-render-properties)，属性包括文件名、分辨率、每个任务的队列数等。

#### 上移
在列表中上移选中的工作视窗。

#### 下移
在列表中下移选中的工作视窗。

#### 批量渲染列表
{: #batch-list}
显示出需要批量渲染的视窗列表，双击列表中的项目可以设置该任务的[批量渲染属性](#batch-render-properties)。

#### 渲染状态
显示批量渲染的队列数、扫描线、耗时等信息。

####  停止渲染
停止批量渲染。

#### 本地批量渲染
{: #render-batch-locally}
仅使用本机进行批量渲染，渲染后的图片将保存在[批量渲染属性](#batch-render-properties)中设置的文件夹。

####  发送到渲染农场批量渲染
将批量渲染任务发送到[渲染农场](render-farm.html)，将调用所有可用的渲染农场客户端进行渲染，渲染后的图片将保存到渲染农场共享文件夹。

### 批量渲染属性
{: #batch-render-properties}

#### 渲染的工作视窗
显示此任务要渲染的视图，请参考[渲染选项卡，渲染的工作视窗](render-tab.html#viewtorender)。

#### 文件名称
点击保存按钮 ![images/saveimageas.png](images/saveimageas.png) 为渲染图片设置名称。

#### Alpha 通道
保存图片时保存 Alpha 通道，详情请参考[使用 Alpha 通道背景](environment-tab.html#alpha)。

#### 使用文件设置
{: #rendering-resolution}
默认使用当前文件设置中的分辨率进行渲染，如果需要设置其他分辨率，取消勾选“使用文件设置”，然后设置分辨率的值。详情请参考[渲染选项卡，分辨率](render-tab.html#resolution)主题。

#### 渲染约束队列
{: #rendering-constraints}
设置此任务渲染多少此后停止。详情请参考[队列](documentproperties-flamingo.html#number-of-passes)主题。

<!-- TODO: Flamingo nXt 5 runs from the RDK.  The need to Flamingo Automate render is not clear.  What is needed to run animations with nxt right now?
The number of passes and the ability to send a render to the farm are required still.  So the dialog should be smaller.
Alpha channel This needs to be investigated. The rest of this section is commented out.-->

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

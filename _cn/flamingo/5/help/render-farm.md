---
Title: 通过渲染农场渲染
---

# {{page.title}}
Flamingo nXt 的渲染农场可以联合数部计算机的运算能力，合力渲染同一个模型、批次渲染或创建视图动画。渲染农场的客戶端只要安裝渲染农场，不需安裝 Rhino 或 Flamingo nXt。

#### 一个典型的渲染农场配置
{: #render-farm}

![images/renderfarm-002.png](images/renderfarm-002.png){: style="margin-top:25px;"}

>![images/01.png](images/01.png)一部安装 Rhino 与 Flamingo nXt 的计算机。
>![images/02.png](images/02.png)网路主机或共享的农场文件夹。
>![images/03.png](images/03.png)两部渲染农场客户端（nXt 渲染农场包含两个免费的客户端）。
>![images/04.png](images/04.png)加购的渲染农场客户端。

渲染农场包含两个免费的客户端，要使用更多电脑作为客户端，需要再加购 nXt 渲染农场授权，购买地址 [https://www2.mcneel.com/commerce/accurender/buy-farm.asp](https://www2.mcneel.com/commerce/accurender/buy-farm.asp)。

#### 共享的农场文件夹
{: farm-folder}
要使用渲染农场进行渲染，很关键的一个要素是必须要设置一个主机和所有客户端都可以访问的共享文件夹，这是一个很普通的共享文件夹，可以设置在主机上也可以设置在网络上，该共享文件夹不需要在每个客户端都显示为相同的名称，但是每个客户端都必须有完整的读/写/删除权限，共享文件夹至少需要有 20G 可用空间。

#### nXt 渲染农场包含两个应用程序：

##### 渲染农场客户端 (nXtFarmer64.exe)
安装在每一部的渲染农场客户端计算机上等待渲染工作的小程序，这个小程序在渲染工作时不会显示任何信息。网络渲染可以结合多部计算机的运算能力，缩短渲染所需的时间，客户端无法对进行中的渲染工作做变更。

##### 渲染农场监视器 (nXtFarmMonitor64.exe)
可以用来查看渲染工作的进度，含有一些简单的管理功能。
For advanced installations, the nXt Render Farm software lets you work with third-party render managers. The following procedures apply to the Render Farm included with Flamingo nXt. If you are planning to use third-party render farm software, some of these procedures will be different.

#### 渲染农场工作步骤
{: #the-farm-process}
 1. 以 Flamingo nXt 渲染时不使用 Render 指令，改用渲染农场 *(Flamingo nXt 菜单 > 渲染农场)*，这样渲染工作会送出至[农场输出文件夹](options-flamingo.html#farm-output-folder)，所有使用的材质与信息会与这个渲染工作一起送出。
 2. 渲染工作在渲染农场中会被划分为许多个任务，渲染农场的客户端会持续检查农场输出文件夹里是否有新的工作，每一个客户端会取回一个工作的一部分进行渲染。农场监视器 *(Flamingo nXt > 工具 > 农场监视器)* 可以监看渲染工作的进度。
 3. 每一个渲染农场客户端会将渲染的结果储存至农场输出文件夹\<*工作名称*>\Output。
 3. 渲染农场客户端在完成一个渲染工作后会继续搜索、执行其它待完成的工作。
 4. 渲染农场储存的格式为 [nXt 图片格式 (.nXtImage)](image-editor.html)，这个格式可以在 [nXt 图像编辑器](image-editor.html)打开做调整，之后也可以在 [nXt 图像编辑器](image-editor.html)中另存为 TGA、PNG、TIF 与 JPG 各种图片格式。

## 安装与配置渲染农场
{: #install}
The Farmer render client and the Farm monitor are installed with Flamingo on the master Rhino machine.  For other client computers that do not have Rhino and Flamingo nXt, the Farmer client needs to be installed.

##### 安装渲染农场
在没有安装 Rhino 和 Flamingo 的计算机上安装渲染农场客户端：

 1. 下载[渲染农场软件](http://www.rhino3d.com/download/The-Farm/1.0/release)。
 1. 在每个客户端计算机上执行下载安装程序。
 1. 从每个客户端计算机的开始菜单中运行渲染农场。
 1. 渲染农场的图标将会出现在系统托盘里。

##### 配置渲染农场
{: #configure-the-render-farm}
1.  在图标上[点击鼠标右键](mouse-button-right.html)并选择 Restore。
1. 在 nXt 渲染农场视窗，从选项菜单选择路径，将路径设置为渲染农场的共用文件夹。

渲染农场的工作是由 Rhino 与 Flamingo nXt 所在的计算机负责送出，请从 Flamingo nXt 菜单选择选项，设置共用的[农场的输出文件夹](options-flamingo.html#farm-output-folder)的位置。

这样渲染农场的设置就完成了。 

## 使用渲染农场
{: #using-the-render-farm-from-flamingo-nxt}
目前渲染农场可以处理三种渲染工作：单一图片渲染、批次渲染与动画渲染。

##### 确认客户端有响应
所有渲染农场客户端启动之后:

 1. 在任意计算机上的开始菜单中，点击[渲染农场监视器](#render-farm-monitor)。
 1. 客户端计算机将会出现在列表中。
 1. 渲染农场的每个客户端都会显示在机器列表中，状态应该为进行中.

如果出现问题，请回顾[安装](#install)及[配置](#configure-the-render-farm)主题。


##### 送出批量渲染工作至农场
1. 在 Rhino 以一般的方法设置各种渲染设置与调整视图角度。
1. 从 Flamingo nXt 菜单选择启动渲染农场。
1. 将弹出[渲染农场工作](#farm-job)对话框。
1. 确定各项设置，然后点击确定。


##### 监视渲染农场
将渲染任务送出到渲染农场后，使用[渲染农场监视器](#render-farm-monitor)查看渲染状态。

 1. 在主机上，点击[渲染农场监视器](#render-farm-monitor)。
 1. 最近的工作将出现在工作列表中，如果渲染内容较大，可能几分钟后才能看到。
 1. 工作状态将会变更为进行中。
 1. 经过一定的时间，客户端就可以接收到任务。
 1. 进度百分比会随着渲染的完成度而增加。
 1. 等待渲染任务完成。


## 渲染农场工作选项
{: #farm-job}

#### 名称
{: #job-name}
送出的工作会在渲染农场共用文件夹里创建一个子文件夹，并在工作名称之前加上工作送出的日期与时间。
一个工作的渲染结果会储存至该工作文件夹里的 Output 子文件夹。 

#### 开始工作
渲染工作可以立刻开始，也可以在设定的时间后开始。

#### 立刻
立即开始渲染。

#### 以后（手动）
稍后在 nXt [渲染农场监视器](#render-farm-monitor)以手动开始渲染。

#### 预约
设置工作开始的日期与时间。

#### 渲染约束队列
{: #rendering-constraints}
设置此任务渲染多少此后停止。详情请参考[队列](documentproperties-flamingo.html#number-of-passes)主题。


## 渲染农场监视器
{: #render-farm-monitor}
渲染农场监视器是一个独立的小程序，可以用来查看农场客户端计算机的状态与目前农场里的工作，农场监视器可以暂停或继续农场里的客户端或工作。 

从 Rhino 中进入渲染农场监视器，Flamingo nXt 5.0 功能表 > 渲染农场 > 渲染农场监视器。

从 Windows 进入渲染农场，在开始菜单中，点击 **所有应用 > nXt 渲染农场 > 渲染农场监视器**。

#### 选项
在机器或工作清单里的項目上按鼠标右鍵有一些选项可以使用。

#### 刷新
刷新工作列表。

#### 暂停机器
使农场客户端暂停参与渲染计算。

#### 继续机器
使暂停中的农场客户端继续参与渲染计算。

#### 暂停工作
暂停农场里的工作。

#### 继续工作
继续暂停中的农场工作。

#### 移除工作
从列表中删除选取的工作。

## 渲染农场的授权
{: #licensing-the-render-farm-}
免费版的渲染农场可以使用两部客户端计算机完成渲染农场里的工作，如果您需要使用更多的客户端，可以到 [https://www2.mcneel.com/commerce/accurender/buy-farm.asp](https://www2.mcneel.com/commerce/accurender/buy-farm.asp) 购买不限制客户端数量的渲染农场授权。

当您取得渲染农场的授权码后，请使用下列方法加入授权码。

##### 授权客户端
1. 请先等待所有进行中的工作完成后再加入授权码。
1. 将授权码放在一个文字文件里，将该文字文件储存在网络共享的资料夹里，以便使用复制，贴上的方式将授权码输入至每一部客户端计算机。
1. 如果农场客户端正在执行，请在 Windows 任务栏的渲染农夫图标上按鼠标[右鍵](mouse-button-right.html)，选择**关闭**。
1. 从 Windows 的**开始**菜单选择**所有程序**。
在 nXt Render Farm 文件夹下选择 **Authorize Farm**。
1. 在打开的对话框贴上授权码，按**确定**。

##### 启动客户端
1. 从 Windows 的**开始**菜单选择**所有程序**。
在 nXt Render Farm 文件夹下选择 **Render Farmer**。
1. 在任务栏的渲染农夫图标上按[鼠标右键](mouse-button-right.html)，选择**还原**。
1. 从帮助菜单选择**关于**。
如果版本号码显示试用版，代表授权未成功。
1. 将渲染农夫视窗最小化到任务栏。

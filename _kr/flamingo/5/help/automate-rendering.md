---
---


# Automate Rendering
The Flamingo nXt **Render Farm** uses the power of several computers to render single images, batch jobs of multiple images, or view-based animations. Neither Rhino nor Flamingo nXt is required on the computers that are used only as render farm clients.

## A typical Farm layout
{: #render-farm}
![images/renderfarm-002.png](images/renderfarm-002.png)

>![images/01.png](images/01.png)Rhino와 Flamingo nXt가 설치된 컴퓨터.
>![images/02.png](images/02.png)Network server or shared farm folder.
>![images/03.png](images/03.png)Two render farm clients. (The nXt Render Farm comes with two free copies of the client software.
>![images/04.png](images/04.png)Additional purchased render farm clients.

## The Farm Process
{: #the-farm-process}
When rendering using Flamingo nXt, instead of rendering a single image with the **Render** command, use the **Render Farm**  *(Flamingo nXt menu &gt; Render Farm)*. This will submit a render job to the [Farm output folder](options-flamingo.html#farm-output-folder). All materials and support information will automatically be submitted along with the job.
The **Render Farm** clients continuously check the farm output folder for a new job. Each client will pick up a part of the job and start to render. The **Farm Monitor**  *(Flamingo nXt &gt; Utilities &gt; Farm Monitor)* keeps track of the job's progress.
Each farm client deposits the results in the farm folder under &lt;&lt; *job name* &gt;&gt;\Output.
Farm output will be in the [nXt image format (.nXtImage)](image-editor.html). Images in this format can be edited using the [nXt Image Editor](image-editor.html). The results can also be saved as TGA, PNG, TIF, and JPG files from the [nXt Image Editor](image-editor.html).
각각의 클라이언트가 작업을 완료하면, 팜으로 전송되는 새로운 작업을 계속해서 선택합니다.
The Render Farm is free for up to two client computers. To add additional client computers, purchase the **nXt Render Farm** license from [https://www2.mcneel.com/commerce/accurender/buy-farm.asp](https://www2.mcneel.com/commerce/accurender/buy-farm.asp).
The **nXt Render Farm** includes two parts:

>nXtFarmer.exe (nXtFarmer64.exe)

각각의 네트워크 클라이언트에서 실행되는 작은 프로그램으로, 생성되는 작업을 기다립니다. 일반적으로 렌더 팜은 렌더링 진행 상황을 모니터에 표시하지 않고 조용하게 처리합니다. 이 방식으로 렌더링하면, 렌더링이 진행되는 동안 컴퓨터가 이를 간섭하지 않게 하면서 시간이 걸리는 작업에 더 많은 컴퓨터 성능을 활용할 수 있습니다.

>nXtFarmMonitor.exe (nXtFarmMonitor64.exe)

렌더링 작업 상태를 보여주고 간단한 제어 기능을 갖춘 애플릿입니다.
고급 설치의 경우, nXt 렌더 팜 소프트웨어를 타사의 렌더링 관리자와 함께 사용할 수 있습니다. 다음의 절차가 Flaming nXt에 포함된 렌더 팜에 적용됩니다. 타사의 렌더 팜 소프트웨어를 사용할 계획이라면 다음 절차 중 일부가 달라집니다.

##### To configure the Render Farm
{: #configure-the-render-farm}

>Create a folder to store the Render Farm jobs on a common shared location.

이 폴더는 네트워크 서버 컴퓨터 또는 모든 팜 컴퓨터가 액세스할 수 있는 어떤 위치에도 있을 수 있습니다. 모든 팜 클라이언트 컴퓨터는 이 폴더를 읽고 쓸 수 있는 권한이 있어야 합니다. 공유 폴더의 사용 가능한 저장 공간은 최소 20GB가 되어야 합니다.
렌더 팜으로 작업을 전송하는 nXt 워크스테이션을 포함하여, 렌더 팜에서 사용하고자 하는 모든 컴퓨터에서 다음의 네 단계 과정을 실행해야 합니다.
1. Install the **nXt Render Farm** software.
1. From the **Start** menu, run the **Render Farmer** on each machine.
The **Render Farmer** will appear as an icon in the system tray.
1.  [Right-click](mouse-button-right.html) on the icon and select **Restore**.
1. In the **nXt Farmer** window, on the **Options** menu, click **Path** and select the path to the **Render Farm** folder.

>On the computer with Rhino and Flamingo nXt where you will ready the models to render and submit jobs to the farm, in Rhino, from the **Tools** menu, click **Options**, set the common farm location to the [Farm output folder](options-flamingo.html#farm-output-folder).

렌더 팜이 이제 구성되었습니다.

##### To verify that the client workstations are responding

>On any of the client workstations, on the **Windows Start** menu, click **Render Farmer**.

위쪽 목록 상자에 클라이언트 컴퓨터가 나타나야 합니다.

## Using the Render Farm
{: #using-the-render-farm-from-flamingo-nxt}
현재 팜은 여러 대의 컴퓨터에 세 가지 방식으로 렌더링을 처리할 수 있습니다: 단일 렌더링 작업, 일괄 작업, 애니메이션.

## Single Images
{: #single-images}
When rendering single images, each image is split into &quot;slices&quot; and distributed to multiple computers.
The progress of jobs can be viewed with the [Farm Monitor](automate-rendering.html#render-farm-monitor). As soon as the job is sent, another farm job may be submitted. Newly submitted jobs will queue up in the render farm shared folder. By default, the farm will render the jobs in the order they were received.
To reconstruct the output into a single image, use the [nXt Image Editor, Arithmetic](image-editor.html#arithmetic) function.

##### To submit a single image job to the render farm
1. In Rhino, configure your rendering and view as you would for a normal rendering.
1. On the **Flamingo nXt** menu, click **Render Farm**.

## Farm Job Options

### 이름
{: #job-name}
The date and time is automatically pre-pended to the name you choose. A sub-folder for the job is created in the **Render Farm** shared folder. An output folder is also created in the new job folder.
각각의 작업이 완료되면 출력 파일은 작업의 출력 폴더에서 찾을 수 있습니다.

### Start job

#### Now
지금 작업을 시작합니다.

#### Later (Manually)
nXt 렌더링 팜 모니터를 사용하여 작업을 나중에 시작합니다.

#### After
Start the job at a specified date and time.

### Render constraints
{: #render-constraints}

####  [Passes](documentproperties-flamingo.html#number-of-passes) 

## Batch Jobs
{: #batch-jobs}
일괄 작업을 통해 여러 개의 작업을 전송하고 명령 하나로 렌더 팜에서 이를 볼 수 있습니다. 각각의 일괄 렌더링은 하나의 클라이언트 컴퓨터에서 렌더링됩니다.

##### To submit a batch job to the render farm
1. In Rhino, configure your rendering and view as you would for a normal rendering.
1. On the **Flamingo nXt** menu, click **Render Batch**.

## Batch Render Options
{: #batch-render}

### 추가
일괄 목록에 뷰포트를 추가합니다.

### Remove
일괄 목록에서 뷰포트를 삭제합니다.

### Properties
Set the [Batch Render Properties](automate-rendering.html#batch-render-properties).

### Move Up
목록에서 뷰포트 이름을 위로 이동시킵니다.

### Move Down
목록에서 뷰포트 이름을 아래로 이동시킵니다.

## Batch List
{: #batch-list}
렌더링될 뷰 목록에 대한 정보를 표시합니다.

## Rendering

### View
일괄 처리 진행률에 대한 패스, 스캔 라인, 경과 시간 정보를 표시합니다.

###  **Stop Rendering** 
일괄 프로세스를 중지합니다.

###  **Render Batch Locally** 
{: #render-batch-locally}
현재 컴퓨터만을 사용하여 일괄 작업을 렌더링합니다. 렌더링된 이미지는 일괄 작업 속성에 지정된 위치에 출력됩니다.

###  **Send Batch To Farm** 
Sends the batch jobs to the [Render Farm](automate-rendering.html#render-farm). The jobs will be rendered by all available Farm clients. The render images will be output to the shared Farm folder.

## Batch Render Properties
{: #batch-render-properties}

### Viewport to render
See: [Render tab, Viewport to render](render-tab.html#viewtorender).

## Output file

### File name
Click the **Save** button and specify a file name for the rendered image.

### 알파 채널
 [알파 채널 배경을 사용합니다.](environment-tab.html#alpha) 

## Rendering resolution
{: #rendering-resolution}

### 문서 설정 사용
See [Render tab, Resolution](render-tab.html#resolution).

## Rendering constraints
{: #rendering-constraints}

###  [Passes](documentproperties-flamingo.html#number-of-passes) 

## Animation
{: #animation}
Animations in Rhino can be configured using Rhino's **Animation toolbar**.

##### To submit an animation job to the render farm
1. Run the [FlamingoNXtAutomateRender](automate-rendering.html#flamingonxtautomaterender) command.
1. In theConfigure Automated Render Commanddialog, select **Render to farm**.
&#160;
Specify theJob name,and click theOKbutton.
&#160;
Set a type of animation from Rhino'sAnimation setuptoolbar. SelectRenderFullas theCapture method.
&#160;
Record the animation from theAnimationtoolbar. The render jobs will be sent to Render Farm.
&#160;
When the jobs are finished in Render Farm, run theFlamingoNXtAutomateRendercommand again and select all the jobs in the dialog.
&#160;
Click theCopy selected files to specified output folderbutton and select a folder where all the render images will be copied to.

## Render Farm Monitor
{: #render-farm-monitor}
The **Render Farm Monitor** is a standalone program that reports the status of the client workstations and the jobs currently in the Farm. Jobs can be suspended and restarted from the monitor and a client workstation can be excluded from participating in the render farm.

## To access the Farm Monitor from Rhino

>On the **Flamingo nXt** menu click **Utilities** &gt; **Farm Monitor**.

## To access the Farm Monitor from Windows

>On the **Start** menu click **All Programs &gt; nXt Render Farm &gt; Farm Monitor**.

## Options
Right-click a **Machine** or a **Job** to access options.

### Refresh
작업 목록을 새로 고칩니다.

### Suspend Machine
렌더 팜 참여에서 워크스테이션을 제외시킵니다.

### Resume Machine
렌더 팜 작업이 실행될 워크스테이션을 다시 시작합니다.

### Suspend Job
지정된 작업을 잠시 멈춥니다.

### Resume Job
지정된 작업을 다시 시작합니다.

### Remove Job
목록에서 지정된 작업을 삭제합니다.

## Licensing the Render Farm
{: #licensing-the-render-farm-}
The free version of the Render Farm allows two network computers (nodes) to work on jobs simultaneously. If you wish to have more network nodes running simultaneously, you can purchase an unlimited node license from [https://www2.mcneel.com/commerce/accurender/buy-farm.asp](https://www2.mcneel.com/commerce/accurender/buy-farm.asp).
라이선스를 구입하면 제품 키를 가지고 다음 순서로 팜 라이선스를 설정하여 사용하십시오.

##### To authorize the node
1. Wait for any active farm jobs to complete before beginning your licensing.
1. Save your **Product Key** to a text file on a network location so you can easily cut and paste it into each node.
1. If the node is currently active, in the Windows system tray (on the taskbar), **/mouse_button_right.htm');" id="a16" style="position: relative;">right-click** the **Render Farm** icon, and then click **Close**.
1. Click the **Windows Start** button, and then click **All Programs**.
In the **nXt Render Farm** folder, click **Authorize Farm**.
1. In the edit box, paste or type your **Product Key** and click **OK**.

##### To start the node
1. Click the **Windows Start** button, and then click **All Programs**.
In the **nXt Render Farm** folder, click **Render Farmer**.
1.  **p('../mouse_button_right.htm');" id="a17" style="position: relative;">Right-click** the tray icon, and on the menu, click **Restore**.
1. On the **Help** menu, click **About**.
버전 숫자가 평가판인 경우에는 라이선스를 받을 수 없습니다.
1. Minimize the **Render Farmer** window to return it to the tray.

## FlamingoNXtAutomateRender 명령
{: #flamingonxtautomaterender}

## Configure Automated Render Command

### 사용
Redirects the default **Render** command to use the **Render Farm**.

### 기본 렌더링 대화 사용
Resets the **Render** command to render directly instead of to the farm.

### Number of render passes to render
렌더링 패스의 수를 지정합니다.

### Render to farm
Redirects the **Render** command to render to the farm.

### Job name
Specifies the **Render Farm**  [Job name](automate-rendering.html#job-name).

## Render constraints

### Number of render passes to render
Specifies the [number of passes](documentproperties-flamingo.html#number-of-passes).

### Save alpha channel
Saves the [alpha channel](render-window.html#save-with-alpha-channel) background.

## Farm generated output files

### Copy selected files to specified output folder

### Refresh file list

### Check all items

### Uncheck all items
&#160;

---
title: Farm Rendering
---

# {{page.title}}
The Flamingo nXt Render Farm uses the power of several computers to render single images, batch jobs of multiple images or view-based animations. Neither Rhino nor Flamingo nXt is required on the computers used only as render farm clients.

#### A typical Farm layout
{: #render-farm}

![images/renderfarm-002.png](images/renderfarm-002.png){: style="margin-top:25px;"}

>![images/01.png](images/01.png)Rhino와 Flamingo nXt가 설치된 컴퓨터.
>![images/02.png](images/02.png)Network server or shared farm folder.
>![images/03.png](images/03.png)Two render farm clients. (The nXt Render Farm comes with two free copies of the client software.
>![images/04.png](images/04.png)Additional purchased render farm clients.

The Render Farm is free for up to two client computers. To add more client computers, purchase the nXt Render Farm license from [https://www2.mcneel.com/commerce/accurender/buy-farm.asp](https://www2.mcneel.com/commerce/accurender/buy-farm.asp).

#### Shared Farm folder
{: farm-folder}
The key to a functional render farm is a shared folder to which the master machine and all the client computers can access.  This is normally a shared network folder.  It can be a folder on the master machine or on a network.  The folder does not have to be assigned to the same name on each client, but each client does need full read/write/delete access to the folder.  The shared folder should have at least 20GB of available storage.

#### The nXt Render Farm includes two Applications:

##### The Farmer render client (nXtFarmer64.exe)
각각의 네트워크 클라이언트에서 실행되는 작은 프로그램으로, 생성되는 작업을 기다립니다. 일반적으로 렌더 팜은 렌더링 진행 상황을 모니터에 표시하지 않고 조용하게 처리합니다. 이 방식으로 렌더링하면, 렌더링이 진행되는 동안 컴퓨터가 이를 간섭하지 않게 하면서 시간이 걸리는 작업에 더 많은 컴퓨터 성능을 활용할 수 있습니다.

##### The Farm monitor (nXtFarmMonitor64.exe)
렌더링 작업 상태를 보여주고 간단한 제어 기능을 갖춘 애플릿입니다.
For advanced installations, the nXt Render Farm software lets you work with third-party render managers. The following procedures apply to the Render Farm included with Flamingo nXt. If you are planning to use third-party render farm software, some of these procedures will be different.

#### The Farm Process
{: #the-farm-process}
 1. To start a rendering using Flamingo nXt farm, instead of using the standard Render command, use the Render Farm *(Flamingo nXt menu &gt; Render Farm)*. This will submit a render job to the [Farm output folder](options-flamingo.html#farm-output-folder). All materials and support information will automatically be submitted along with the job.
 2. Render jobs are split into many different farm tasks. The Render Farm clients continuously check the farm output folder for new tasks. Each client will pick up a task and start to render. The Farm Monitor  *(Flamingo nXt &gt; Utilities &gt; Farm Monitor)* is a good way to keep track of the job's progress.
 3. Each farm client deposits the results in the farm folder under *job name* \Output.
 3. As each client finishes with a job, it will continue to pick up new jobs as they are submitted to the farm.
 4. Farm output will be in the [nXt image format (.nXtImage)](image-editor.html). Images in this format can be edited using the [nXt Image Editor](image-editor.html). The results can also be saved as TGA, PNG, TIF, and JPG files from the [nXt Image Editor](image-editor.html).

## Install and configure the Farm
{: #install}
The Farmer render client and the Farm monitor are installed with Flamingo on the master Rhino machine.  For other client computers that do not have Rhino and Flamingo nXt, the Farmer client needs to be installed.

##### Installing the Render Farmer
For machines that do not have Rhino and Flamingo installed, install the Farmer client:

 1. Download the current [Render Farmer software](http://www.rhino3d.com/download/The-Farm/1.0/release).
 1. Run the downloaded installer on each of the client computers.
 1. From the Start menu, run the Render Farmer on each machine.
 The Render Farmer will appear as an icon in the system tray.

##### To configure the Render Farm
{: #configure-the-render-farm}
1.  [Right-click](mouse-button-right.html) on the icon and select Restore.
1. In the nXt Farmer window, on the Options menu, click Path and select the path to the Render Farm folder.

On the computer with Rhino and Flamingo nXt set the Zoo folder in Rhino. From the Tools menu, click Options, set the common farm location to the [Farm output folder](options-flamingo.html#farm-output-folder).

렌더 팜이 이제 구성되었습니다.

## Using the Render Farm
{: #using-the-render-farm-from-flamingo-nxt}
현재 팜은 여러 대의 컴퓨터에 세 가지 방식으로 렌더링을 처리할 수 있습니다: 단일 렌더링 작업, 일괄 작업, 애니메이션.

##### To verify that the client workstations are responding
After starting the Render Farmer client on all the client computers:

 1. On any of the computer, in the Windows Start menu, click [Farm Monitor](#render-farm-monitor).
 1. The client machines should appear in the upper list box.
 1. Each Render Farmer client should be listed under the Machine list.  The Status should read Active.

If there is a problem with this, review the [install](#install) and [configuration topics](#configure-the-render-farm).


##### To submit a job to the render farm
1. In Rhino, configure your rendering and view as you would for a normal rendering.
1. On the Flamingo nXt menu, click Start Farm Render.
1. The [Farm Job](#farm-job) dialog should appear.
1. Verify the correct option and hit OK.


##### Monitoring the Farm
After submitting a job to the Render Farm, use the [Farm Monitor](#render-farm-monitor).

 1. On the master computer, in the Windows Start menu, click [Farm Monitor](#render-farm-monitor).
 1. A recent job should show up in the Jobs list. This can take a few minutes for large jobs.
 1. The status of the job will change to active.
 1. After a period of time, the machines above should pick up tasks with the same date.
 1. The Percent complete increases as tasks are completed.
 1. Watch for the job status Completed when the job is finished.


## Farm Job Options
{: #farm-job}

#### 이름
{: #job-name}
The date and time is automatically pre-pended to the name you choose. A sub-folder for the job is created in the Render Farm shared folder. An output folder is also created in the new job folder.
각각의 작업이 완료되면 출력 파일은 작업의 출력 폴더에서 찾을 수 있습니다.

#### 작업 시작
Job may be started immediately after submission, at a later time, or manually through the Farm monitor.

#### Now
지금 작업을 시작합니다.

#### Later (Manually)
Start the job later using the nXt [Farm Monitor](#render-farm-monitor) to start the job.

#### After
Start the job at a specified date and time.

#### Rendering Constraints Passes
{: #rendering-constraints}
Set the number of passes needed to finish the batch job.  See the [Passes](documentproperties-flamingo.html#number-of-passes) topic for more details.


## Render Farm Monitor
{: #render-farm-monitor}
The Render Farm Monitor is a stand-alone program that reports the status of the client workstations and the jobs currently in the Farm. Jobs can be suspended and restarted from the monitor and a client workstation can be excluded from participating in the render farm.

To access the Farm Monitor from Rhino go to the Flamingo nXt 5.0 menu > Render Farm > Farm Monitor.

To access the Farm Monitor from Windows, on the Start menu click **All Programs > nXt Render Farm > Farm Monitor**.

#### 옵션
Right-click a Machine or a Job to access options.

#### Refresh
작업 목록을 새로 고칩니다.

#### Suspend Machine
렌더 팜 참여에서 워크스테이션을 제외시킵니다.

#### Resume Machine
렌더 팜 작업이 실행될 워크스테이션을 다시 시작합니다.

#### Suspend Job
지정된 작업을 잠시 멈춥니다.

#### Resume Job
지정된 작업을 다시 시작합니다.

#### Remove Job
목록에서 지정된 작업을 삭제합니다.

## Licensing the Render Farm
{: #licensing-the-render-farm-}
The free version of the Render Farm allows two network computers (nodes) to work on jobs simultaneously. If you wish to have more network nodes running simultaneously, you can purchase an unlimited node license from [https://www2.mcneel.com/commerce/accurender/buy-farm.asp](https://www2.mcneel.com/commerce/accurender/buy-farm.asp).

라이선스를 구입하면 제품 키를 가지고 다음 순서로 팜 라이선스를 설정하여 사용하십시오.

##### To authorize the node
1. Wait for any active farm jobs to complete before beginning your licensing.
1. Save your Product Key to a text file on a network location so you can easily cut and paste it into each node.
1. If the node is currently active, in the Windows system tray (on the taskbar), /mouse_button_right.htm');" id="a16" style="position: relative;">right-click the Render Farm icon, and then click **Close**.
1. Click the **Windows Start** button, and then click **All Programs**.
In the nXt Render Farm folder, click **Authorize Farm**.
1. In the edit box, paste or type your Product Key and click **OK**.

##### To start the node
1. Click the **Windows Start** button, and then click **All Programs**.
In the nXt Render Farm folder, click **Render Farmer**.
1.  p('../mouse_button_right.htm');" id="a17" style="position: relative;">Right-click the tray icon, and on the menu, click **Restore**.
1. 도움말 메뉴에서 **정보**를 클릭합니다.
버전 숫자가 평가판인 경우에는 라이선스를 받을 수 없습니다.
1. Minimize the Render Farmer window to return it to the tray.

---
title: 자동 렌더링
---

# {{page.title}}


## 일괄 렌더링
{: #batch-rendering}
Batch jobs let you submit multiple jobs to be rendered automatically. A Batch job can specify a specific view, resolution and number of passes. Batch renderings can be started on a single or sent out the [Render Farm](render-farm.html). Open the Batch list and add jobs to the list. The batch jobs list will be saved in the model.

##### 이 명령은 어디에서 찾을 수 있습니까?

 * Menus > Flamingo nXt 5.0 > More Tools > Batch Render

### 일괄 렌더링 대화상자
{: #batch-render}
Start by adding a job, then edit the properties to set up batch jobs.

#### 추가
Each Batch job is based on a view saved in the model.  Click on the Add item to select from a list of views in the model.  All the other menu items will activate once a job is added and selected.

#### 삭제
Select and existing batch job.  Then use Delete to remove the job from the batch list.

#### 속성
Select an existing batch job, then use Properties to set the [Batch Render Properties](#batch-render-properties).  Properties include file name, resolution, and number of passes for each job.

#### 위로 이동
목록에서 뷰포트 이름을 위로 이동시킵니다.

#### 아래로 이동
목록에서 뷰포트 이름을 아래로 이동시킵니다.

#### 일괄 목록
{: #batch-list}
Displays information about the list of views to be rendered. Double-click on an existing job to edit set the [Batch Render Properties](#batch-render-properties).

#### Rendering Status
일괄 처리 진행률에 대한 패스, 스캔 라인, 경과 시간 정보를 표시합니다.

####  Stop Rendering
일괄 프로세스를 중지합니다.

#### Render Batch Locally
{: #render-batch-locally}
Uses only the current computer to render the batch jobs. The rendered images will output to the location specified in the [Batch Render Properties](#batch-render-properties).

####  Send Batch To Farm
Sends the batch jobs to the [Render Farm](render-farm.html). The jobs will be rendered by all available Farm clients. The render images will output to the shared Farm folder.

### Batch Render Properties
{: #batch-render-properties}

#### 렌더링할 뷰포트
Shows the view that this job will render. See [Render tab, Viewport to render](render-tab.html#viewtorender).

#### 파일 이름
Click the Save button ![images/saveimageas.png](images/saveimageas.png) and specify a file name for the rendered image.

#### 알파 채널
Save the image with the Alpha Channel.  See the [Use alpha channel background](environment-tab.html#alpha) for more details.

#### Use document settings
{: #rendering-resolution}
The default is to use the current document resolution settings to render.  If another resolution is needed, then uncheck this box and specify a resolution. See the [Render tab, Resolution](render-tab.html#resolution) topic for more details.

#### Rendering Constraints Passes
{: #rendering-constraints}
Set the number of passes needed to finish the batch job.  See the [Passes](documentproperties-flamingo.html#number-of-passes) topic for more details.

<!-- TODO: Flamingo nXt 5 runs from the RDK.  The need to Flamingo Automate render is not clear.  What is needed to run animations with nxt right now? Alpha channel This needs to be investigated. The rest of this section is commented out.-->

<!-- Commented out until automated render can be determined

## 애니메이션
{: #animation}
There are two ways to create animations in Rhino.  Animations can be configured using [Rhino's Animation toolbar](http://docs.mcneel.com/rhino/5/help/en-us/index.htm#commands/animation.htm) or using the [Bongo](http://bongo.rhino3d.com/) animation plugin.

##### To submit an animation job to the render farm
1. [FlamingoNXtAutomateRender](automate-rendering.html#flamingonxtautomaterender) 명령을 실행합니다.
1. In theConfigure Automated Render Commanddialog, select **Render to farm**.
 
Specify theJob name,and click theOKbutton.
 
Set a type of animation from Rhino'sAnimation setuptoolbar. SelectRenderFullas theCapture method.
 
Record the animation from theAnimationtoolbar. The render jobs will be sent to Render Farm.
 
When the jobs are finished in Render Farm, run theFlamingoNXtAutomateRendercommand again and select all the jobs in the dialog.
 
Click theCopy selected files to specified output folderbutton and select a folder where all the render images will be copied to.


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

### 작업 이름
Specifies the **Render Farm**  [Job name](automate-rendering.html#job-name).

## 렌더링 제한 조건

### Number of render passes to render
Specifies the [number of passes](documentproperties-flamingo.html#number-of-passes).

### 알파 채널 저장
Saves the [alpha channel](render-window.html#save-with-alpha-channel) background.
-->

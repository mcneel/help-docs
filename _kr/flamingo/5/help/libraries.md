---
title: 라이브러리 패널
---

# ![images/libraries.svg](images/libraries.svg) {{page.title}}
Libraries 명령은 재질, 텍스처, 환경 라이브러리를 관리하는 라이브러리 패널을 엽니다.

렌더링 콘텐츠는 모델 간에 공유할 수 있는 외부 라이브러리를 만들어 파일에 저장할 수 있습니다. 콘텐츠는 Rhino 세션 사이 또는 폴더로 끌어올 수 있습니다.

색 견본도 동일한 방식으로 마우스로 끌어 놓을 수 있습니다.

라이브러리에는 사용자가 설정한 콘텐츠 폴더 내용이 표시됩니다. 마우스로 콘텐츠 끌어 놓기 방식을 사용하여, 모델이 아닌 다른 곳에 문서 콘텐츠를 저장할 때 사용하세요.

재질은 사용자의 하드 드라이브에 있는 파일입니다. 라이브러리 폴더는 Windows 폴더입니다. 다른 Windows 파일이나 폴더와 마찬가지로 라이브러리 폴더를 복사하고, 붙여넣고, 이동할 수 있습니다.

Use the address bar at the top of the Libraries tab to navigate to any folder on your computer.

To quickly navigate back to the Default Library locations use the wrench icon at the upper right. ![images/library_default.png](images/library_default.png)

#### Organizing Libraries
{: organizing_libraries}
Libraries are simply files.  You can copy and paste and move around folders. Use Windows Explorer to edit the folders and documents. To edit which folders are the default in the Libraries Tab, use the [Library Settings](#settings) ![images/library_default.png](images/library_default.png).

## 재질 라이브러리
{: #material}
Materials in libraries are files on the hard drive.  Once assigned to the model, the material is then stored and saved in the model.  Any changes to the assigned material will not change the original material on the hard drive.

Drag and drop materials to assign materials to the model. Materials can be assigned to:

#### 레이어 지정
Drag a material directly onto the layer name in the Layers Panel. This is the recommended method as by default any object on the layer will adopt the material assignment. Later changes to the material can be quite quick by simply dropping another material on the layer.

#### 개체 지정
Drag a material directly onto an object in any viewport. This will override the By Layer material to a By Object assignment.

#### 블록 지정
Drag onto a block and any By Parent objects in the block will adopt that material.  Any object within the block that has a By Parent material source will pick up the blocks material.

## 식물 라이브러리
{: #plant}
In the default library folder is a Plants folder.  Go here to place plants in the model.  Once placed in the model, the plant is then stored and saved in the model.  Any changes to the assigned material will not change to original material on the hard drive. Drag and drop plants into a viewport to place plants into the model. For more information see the [Plants Help](plants.html) topic.

## 환경 라이브러리
{: #environment}
Environments can be saved in the library.  This lets Environment settings to be passed from one model to another.  For more details, go to [Environments](environment-tab.html).

## 라이브러리 설정
{: #settings}
Use ![images/options.png](images/options.png)Libraries Options to change the library defaults shown under the ![images/library_default.png](images/library_default.png) menu.

##### 이 명령은 어디에서 찾을 수 있습니까?
There are three places to find the Libraries Options command.

 1. Libraries Tab > ![images/library_default.png](images/library_default.png) in the upper right of the Libraries panel > Settings...
 1. 메뉴 > 도구 메뉴 > 옵션 > 라이브러리.


### 렌더링 콘텐츠 표시
Use this to show or hide the default render content location.

#### Use default library location (My Documents)
By default, the [content libraries](libraries.html) are a subfolder of the *My Documents* folder.

#### 사용자 지정
Sets a custom [library](libraries.html) location.  Changes the default location of [content libraries](libraries.html) for this computer.

##### 찾아보기 단추
파일을 지정하기 위해 파일 브라우저를 엽니다.

#### 문서 폴더 표시
지정된 문서 폴더가 [라이브러리 패널](libraries.html)의 메뉴에 표시됩니다.

#### 사용자 지정 폴더 표시
사용자가 지정한 폴더가 [라이브러리 패널](libraries.html)의 메뉴에 표시됩니다.

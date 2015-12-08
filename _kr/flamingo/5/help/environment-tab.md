---
title: 환경 패널
---

# ![images/environment.svg](images/environment.svg) {{page.title}}
{: #environment-tab}
Environments are not only what can be seen in the background of a rendering, but control an infinite sphere surrounding the model. Objects within the scene will reflect and refract the environment. The environment sphere is not an object that you can select, but a reference surface for background effects.

The Environment affects the visible part of the background and reflections.  For effects that affect lighting the scene, see the [Sky](sun-and-sky.html) help topic.

Flamingo comes with a special environment called *[Default Flamingo Environment](environment.html)*.  This environment will sync to the current [Lighting Preset](lighting-tab.html). By using [Lighting presets](lighting-tab.html), both the Lighting and environment will be set to appropriate scene defaults.

![images/environment-editor-panel.svg](images/environment-editor-panel.svg){:  #panel_map height="600px" style="float: right"}

##### 이 명령은 어디에서 찾을 수 있습니까?
 1. ![images/environments.png](images/environments.png)Environment Tab
 1. ![images/icon-render.png](images/icon-render.png)Render Tools Toolbars > ![images/environments.png](images/environments.png) Environment Editor
 1. ![images/menuicon.png](images/menuicon.png)메뉴 > 렌더링 메뉴 > 환경 편집기
 1. 명령 > EnvironmentEditor

The Environment Editor Panel is split into discrete sections.  Based on the environment type, the advanced panels may vary.

Colors and textures can be dragged from the color swatch and dropped onto any other color swatch or control in the Material Editor, [Texture Palette](texturepalette.html), or [Environment Editor](environmenteditor.html).
환경 패널

 1. [배경 유형](#type)
 1. [설정 막대](#settings)
 1. [Environment List](#environment_list)
 1. [창 구분](#divider)
 1. [환경 속성 섹션](#properties)
 1. [이름](#name)
 1. [환경 속성 패널](#panels)

## [배경 유형](#panel_map) ![images/callout_1.svg](images/callout_1.svg)
{: #type style="clear: both;"}
Select the type of background for the model.  [Environment](#flamingo-environment) is an all inclusive rendering environment and should be the default setting for Flamingo.  The other three settings present a much more simplified set of settings that reflect older ways of defining backgrounds. For more information see the [Rhinoceros Simple Background](http://docs.mcneel.com/rhino/5/help/en-us/commands/environmenteditor.htm#Basic_settings) topic

이 도움말 항목에서 환경 유형에 대해 상세하게 설명합니다.

## [설정 막대](#panel_map) ![images/callout_2.svg](images/callout_2.svg)
{: #settings}
이 막대를 사용하여 환경 목록을 탐색하세요.

#### ![images/met_leftarrow.png](images/met-leftarrow.png) 뒤로 화살표
Walks back through the current environment or the previously selected environments.  For instance an environment with reflective or refractive layers.  Use this arrow to get back to the parent environment from the reflection or refraction details.

####  ![images/met_rightarrow.png](images/met-rightarrow.png) 앞으로 화살표
Walks forward through the previously selected environments.  For instance an environment with reflective or refractive layers.  Use this arrow to get forward to the parent environment from the reflection or refraction details.

#### ![images/material_editor.png](images/material_editor.png)![images/texture-2dchecker.png](images/texture-2dchecker.png) Currently selected environment name
Displays the current environment name and edit level.  For instance, if there is a reflective or refractive level a ">" is shown. A good place to see where the environment is current.

#### ![images/library_default.png](images/library_default.png) 도구 메뉴
Displays the [Tools menu](#tools-menu).  This is an extensive menu of commands, settings and utilities related to environments.

#### ![images/help_topics.png](images/help_topics.png) 도움말

## [환경 목록](#panel_map) ![images/callout_3.svg](images/callout_3.svg)
{: #environment_list}
This lists all the environments contained in the model. One Environment will be selected as the current environment. The current environment is used in the rendering. Yellow corners will show up surrounding the current Environment.

From this list:

* Click on an Environment to make it current. Once selected the environment's properties will show in the panels below. See [Render Materials Properties](#properties) for more information
* Scroll up and down in the list to see all the environments in the model.
* Add a new Environment using the Add New Button ![images/add_material.png](images/add_material.png) at the bottom of the list.
* Right-click a thumbnail to display the Environment context menu
* Right-click the blank area to display the New Environment Context Menu

###  ![images/add_material.png](images/add_material.png) Add new environment
{: #add_environment}
Scroll down to the bottom of the Environment list to see the add icon.

Opens the Render Content [library](libraries.html) of environments.
The environments in the library act as templates for creating environments in the model.

### 환경 상황에 맞는 메뉴
{: environment_context}
This menu is available by right click on a environment listing.  See the [Tools Menu](#tools_menu) for details on the many options in this menu.

### 새로운 환경 상황에 맞는 메뉴
{: new_envrionment_context}
This menu is available by right-clicking on a blank area of the Environment List.

#### ![images/toolbarlus.png](images/toolbarplus.png) 새로운 환경 만들기
새로운 Flamingo 환경을 만듭니다.

#### ![images/import.png](images/import.png) 파일에서 환경 가져오기...
이 명령을 사용하여 이전에 내보낸 환경을 선택합니다.

#### ![images/paste.png](images/paste.png) 붙여넣기
클립보드의 콘텐츠를 바탕으로 새로운 환경을 만듭니다.

#### ![images/pasteasinstance.png](images/pasteasinstance.png) 인스턴스로 붙여넣기
인스턴스 작업을 통해 원래 환경과 연결되어 있는 클립보드의 콘텐츠를 기준으로 새로운 환경을 만듭니다.

#### ![images/grid.png](images/grid.png) 그리드
미리보기를 썸네일 그리드로 표시합니다.

#### ![images/list.png](images/list.png) 목록
미리보기를 썸네일 목록으로 표시합니다.

#### ![images/tree.png](images/tree.png) 나무
미리보기를 중첩된 트리로 표시합니다.

#### ![images/horizontal.png](images/horizontal.png) 가로 레이아웃
제어의 왼쪽으로 미리보기를 표시합니다.

#### ![images/showpreview.png](images/showpreview.png) 미리보기 창 표시
현재 선택된 썸네일의 미리보기 속성을 표시합니다. 미리보기 지오메트리, 크기. 배경, 회전 동작을 설정합니다.

#### ![images/floatthumbnail.png](images/floatthumbnail.png) 플로팅
조정 가능한 창에서 미리보기 이미지를 플로팅(floating)으로 설정합니다.

#### 썸네일

##### ![images/small.png](images/small.png) 작게
썸네일 크기를 가장 작은 크기로 설정합니다.

##### ![images/medium.png](images/medium.png) 중간
썸네일 크기를 중간 크기로 설정합니다.

##### ![images/large.png](images/large.png) 크게
썸네일 크기를 큰 크기로 설정합니다.

##### ![images/showlabels.png](images/showlabels.png) 레이블 표시
썸네일 이름 레이블을 그리드 모드에서 표시합니다.
목록 모드는 항상 레이블을 표시합니다.

##### ![images/showunits.png](images/showunits.png) 단위 표시
크기를 모델 단위로 표시합니다.

##### ![images/autoupdatethumbnail.png](images/autoupdatethumbnail.png) 미리보기 자동 업데이트
설정이 변경되면 그에 따라 자동으로 모든 미리보기를 업데이트합니다.

##### ![images/updateallpreviews.png](images/updateallpreviews.png) 모든 미리보기 업데이트
미리보기 자동 업데이트가 꺼져 있을 때 수동으로 미리보기를 업데이트합니다.

## [창 구분](#panel_map) ![images/callout_4.svg](images/callout_4.svg)
{: #divider}
Drag on this divider to change the length of the Environment List versus the length of the Environment Properties Section.

## [환경 속성 섹션](#panel_map) ![images/callout_5.svg](images/callout_5.svg)
{: #properties}

### [환경 이름](#panel_map) ![images/callout_6.svg](images/callout_6.svg)
{: #name}
This is the name of the environment. The environment name is also saved as the file name when exporting the environment to the library. **Note:** Environments are stored in the Rhino model, unique environments can have the same name in different Rhino models.

### [환경 패널](l#panel_map) ![images/callout_7.svg](images/callout_7.svg)
{: #panels}
The Environment Properties section is filled with a number of direct Environment panels. Clicking on the grey title bar will rollup the environment panel, hiding the contents of that panel.  Click on the title bar again to show contents.

Environment Panels will vary based on the type of environment and the current active environment level. For more information on specific environment panels see [Flamingo Environment](environment.html)

## 도구 메뉴 ![images/library_default.png](images/library_default.png)
{: tools_menu}
이 설정은 썸네일 미리보기와 썸네일 배경을 오른쪽 클릭하여 표시되는 메뉴에서도 선택할 수 있습니다.

#### ![images/currentenvironment.png](images/currentenvironment.png) 현재 환경으로 설정
This sets the target environment current.  The current environment will be used in the next rendering.

#### ![images/toolbarlus.png](images/toolbarplus.png) 새로운 환경 만들기
새로운 Flamingo 환경을 만듭니다.
<!-- This comes from the page http://docs.mcneel.com/rhino/5/help/en-us/popup_moreinformation/materialthumbnail_contextmenu.htm -->
이 설정은 썸네일 미리보기와 썸네일 배경을 오른쪽 클릭하여 표시되는 메뉴에서도 선택할 수 있습니다.

#### ![images/import.png](images/import.png) 파일에서 환경 가져오기
저장된 Rhino .renv 파일에서 환경을 가져옵니다.

#### ![images/savetofile.png](images/savetofile.png) 파일에 저장
환경을 Rhino .renv 파일로 저장합니다.

#### ![images/changetype.png](images/changetype.png) 유형 변경
환경을 다른 유형으로 변경합니다.

#### ![images/changetype.png](images/changetype.png) 유형 변경 (유사한 설정 복사)
환경을 다른 유형으로 변경합니다.
The default behavior depends on the current state of the [Rendering Options](http://docs.mcneel.com/rhino/5/help/en-us/options/rendering.htm) >  [Copy similar settings when content type is changed](http://docs.mcneel.com/rhino/5/help/en-us/options/rendering.htm#Copy_similar_settings_when_content_type_is_changed)  box. If checked, compatible settings from the old content will be copied to the new one.

#### ![images/reset.png](images/reset.png) 기본값으로 다시 설정
Changes all the environment settings to the default Solid color background (Black), reflected background, Sky and Refracted Background visible.

#### ![images/copy.png](images/copy.png) 복사
Copies the selected environment to the Windows Clipboard. The Clipboard can then be pasted into the editor to create a new environment or pasted directly into a folder to create a [library](libraries.html) file.

#### ![images/paste.png](images/paste.png) 붙여넣기
클립보드의 콘텐츠를 바탕으로 새로운 환경을 만듭니다.

#### ![images/pasteasinstance.png](images/pasteasinstance.png) 인스턴스로 붙여넣기
인스턴스 작업을 통해 원래 환경과 연결되어 있는 클립보드의 콘텐츠를 기준으로 새로운 환경을 만듭니다.

#### ![images/delete.png](images/delete.png) 삭제
선택된 환경을 삭제합니다.

#### ![images/rename.png](images/rename.png) 이름 바꾸기...
선택된 환경의 이름을 바꿉니다.

#### ![images/duplicate.png](images/duplicate.png) 복제
선택된 환경을 동일한 설정으로 새 환경에 복사합니다.

#### ![images/removeinstancing.png](images/removeinstancing.png) 인스턴스 제거
Removes the connection between [instanced](#paste-as-instance) environments.

{% include_relative snippets/snippet-contenteditorpreviewoptions.md %}

#### ![images/contentfilter.png](images/contentfilter.png) 콘텐츠 필터
[콘텐츠 필터](content_filters.html) 대화상자를 엽니다.

#### ![images/rename.png](images/rename.png) 속성
[미리보기 속성](previewproperties.html) 대화상자를 엽니다.

---
title: 재질 편집기 패널
---

# ![images/paint.svg](images/paint.svg) {{page.title}}
재질에는 색, 반사, 투명도, 텍스처, 범프 맵, 서피스 마무리 등의 설정이 포함되어 있습니다. 모든 재질에는 기본 설정이 있습니다. 기본 재질은 흰색 무광이며, 반사 또는 투명도가 지정되지 않았습니다. 가장 좋은 결과를 얻으려면 Flamingo 특정 재질을 사용하세요.

Materials can be assigned to layers, objects, and blocks. Assignments can be made by dragging and dropping on to objects or various controls. See [Material Assignments](material_assignment.html) for more information.

Once assigned, materials are stored in the model. The material, textures, and all support files for rendering can be stored within the Rhino model with properly set [Rendering Options](http://docs.mcneel.com/rhino/5/help/en-us/index.htm#options/rendering.htm).

Materials, environments, and textures are stored in the model, but rendering content can also be saved to files that can be shared between models. Content can be dragged between Rhino sessions and into a folder. Color swatches can be dragged and dropped in the same way. The [Libraries Panel](libraries.html) displays the default content folder. Use this to drag and drop content into the model or to drag and drop model content to an external file.

![images/material_editor_panel.svg](images/material_editor_panel.svg){:  #panel_map .float-img-right}

##### 이 명령은 어디에서 찾을 수 있습니까?
There are several options to find the Materials tab.

* ![images/materialtab.png](images/materialtab.png)재질 탭
* ![images/icon-render.png](images/icon-render.png)렌더링 도구 도구모음 > ![images/materialtab.png](images/materialtab.png) 재질 편집기
* 메뉴 > 렌더링 메뉴 > 재질 편집기
* 명령행에 MaterialEditor 를 입력합니다.

재질 편집기 패널은 별개의 섹션으로 나뉘어져 있습니다. 재질 유형에 따라 고급 패널이 달라질 수 있습니다.

You can drag colors and textures from the color swatch and drop onto any other color swatch or control in the Material Editor, [Texture Palette](texturepalette.html), or [Environment Editor](environmenteditor.html).

##### 재질 패널

 1. [설정 막대](#settings)
 1. [재질 목록](#material_list)
 1. [창 구분](#divider)
 1. [재질 속성 섹션](#properties)
 1. [이름](#name)
 1. [재질 속성 패널](#panels)

## [설정 막대](#panel_map) ![images/callout_1.svg](images/callout_1.svg)
{: #settings .clear-img}
Use this bar to navigate the material during its development.

#### ![images/met_leftarrow.png](images/met-leftarrow.png) 뒤로 화살표
Walks back though the current material or the previously selected materials.  For instance, materials with textures have multiple layers.  Use this arrow to return to the parent material from the texture details.

####  ![images/met_rightarrow.png](images/met-rightarrow.png) 앞으로 화살표
Walks back though the current material or the previously selected materials.  For instance materials with textures have multiple layers.  Use this arrow to return to the recently used texture from the parent material.


#### ![images/material_editor.png](images/material_editor.png)![images/texture-2dchecker.png](images/texture-2dchecker.png) 현재 선택된 재질 이름
Displays the current material name and level.  For instance, if there is a texture or a material procedural level the ">" will show. A good place to see where the editor is in a material.

#### ![images/library_default.png](images/library_default.png) 도구 메뉴
Displays the [Tools menu](#tools-menu).  This is an extensive menu of commands, settings and utilities related to materials.


## [재질 목록](#panel_map) ![images/callout_2.svg](images/callout_2.svg)
{: #material_list}
This lists all the materials contained in the model. From this list:

* Scroll up and down in the list to see all the materials in the model.
* Drag and drop a material from this list onto a layer in the [Layer Panel](http://docs.mcneel.com/rhino/5/help/en-us/index.htm#commands/layer.htm) or directly onto an Object to assign it to an Object. See [Material Assignments](material_assignment.html) for more information.
* Add a new Material using the Add New Button ![images/add_material.png](images/add_material.png) at the bottom of the list.


* Click on each material to select it. Once selected the material's properties will show in the panels below. See [Render Materials Properties](#properties) for more information.
* 썸네일을 오른쪽 클릭하면 재질 관련 메뉴가 표시됩니다.
* 공백의 공간을 오른쪽 클릭하면 새로운 재질 관련 메뉴가 표시됩니다.

###  ![images/add_material.png](images/add_material.png) 새 재질 추가
{: #add_material}
Scroll down to the bottom of the Material list to see the add icon.

렌더링 콘텐츠 재질 [라이브러리](libraries.html)를 엽니다.
라이브러리의 재질은 모델에 재질을 만들 때 템플릿처럼 실행됩니다.

### 재질 상황에 맞는 메뉴
{: material_context}
This menu is available by right-clicking on a material listing.  See the [Tools Menu](#tools_menu) for details on the many options in this menu.

### 새로운 재질 상황에 맞는 메뉴
{: new_material_context}
This menu is available by right-clicking on a blank area of the Material List.

#### ![images/toolbarlus.png](images/toolbarplus.png) 새 재질 만들기
새로운 기본 무광택 흰색 재질을 만듭니다.


#### ![images/paste.png](images/paste.png) 붙여넣기
클립보드의 콘텐츠를 기준으로 새로운 재질을 만듭니다.

#### ![images/pasteasinstance.png](images/pasteasinstance.png) 인스턴스로 붙여넣기
인스턴스 작업을 통해 원래 재질과 연결되어 있는 클립보드의 콘텐츠를 기준으로 새로운 재질을 만듭니다.

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

## [창 구분](#panel_map) ![images/callout_3.svg](images/callout_3.svg)
{: #divider}
Drag on this divider to change the length of the Material List. If you lengthen the Material List, the Material Properties Section shortens.

## [재질 속성 섹션](#panel_map) ![images/callout_4.svg](images/callout_4.svg)
{: #properties}

#### [재질 이름](#panel_map) ![images/callout_5.svg](images/callout_5.svg)
{: #name}
This is the name of the material. The material name is also saved as the file name when exporting the material to the library. Note: Materials are stored in the Rhino model. Unique materials can have the same name in different Rhino models.

#### [재질 패널](material-editor.html#panel_map) ![images/callout_6.svg](images/callout_6.svg)
{: #panels}
The Materials Properties section is filled with several direct Material panels. Clicking on the grey title bar will roll up the material panel, hiding the contents of that panel.  Click on the title bar again to show contents.

Material Panels will vary based on the type of material and the current active material level. For more information on specific material panels see [Flamingo Materials](material-type-simple.html).

## 도구 메뉴 ![images/library_default.png](images/library_default.png)
{: #tools-menu}
<!-- This comes from the page http://docs.mcneel.com/rhino/5/help/en-us/popup_moreinformation/materialthumbnail_contextmenu.htm -->
이 설정은 썸네일 미리보기와 썸네일 배경을 오른쪽 클릭하여 표시되는 메뉴에서도 선택할 수 있습니다.

#### ![images/assigntoobjects.png](images/assigntoobjects.png) 선택한 개체에 적용
현재 재질을 선택된 개체에 적용합니다.

##### 재질을 개체에 적용하려면
 1. 메뉴에서 선택한 개체에 적용을 클릭합니다.
 1. Rhino 뷰포트에서 대상 개체를 선택합니다.

##### 개체를 미리 선택하려면
 1. Rhino 뷰포트에서 대상 개체를 선택합니다.
 1. 메뉴에서 선택한 개체에 적용을 클릭합니다.
선택한 개체에 적용을 클릭하기 전,후에 대상 개체를 선택할 수 있습니다.

##### 재질을 개체에 끌어 놓으려면(drag and drop)
 * 썸네일 또는 목록에서 재질을 대상 개체로 끌어옵니다.
끌어 놓기(drag and drop)는 한 번에 하나의 개체에만 실행됩니다.

#### ![images/assigntolayers.png](images/assigntolayers.png) 레이어에 적용
현재 재질을 레이어에 적용합니다.

##### 재질을 레이어에 적용하려면
 1. 레이어에 적용을 클릭합니다.
 1. 레이어 선택 대화상자에서 재질을 적용할 레이어의 확인란을 선택합니다.

##### 레이어 패널에서 재질을 적용하려면
 1. In the  [Layer](http://docs.mcneel.com/rhino/5/help/en-us/index.htm#commands/layer.htm)  panel, select one or more layers and click the  [Material](http://docs.mcneel.com/rhino/5/help/en-us/commands/layer.htm#Material)  column.
 1. In the Layer Material dialog box, select the material to assign.


##### 재질을 개체에 끌어 놓으려면(drag and drop)
 * Drag the material from the thumbnails or list onto the target layer.
끌어 놓기(drag and drop)는 한 번에 하나의 레이어에만 실행됩니다.

#### ![images/materials_selectobjects.png](images/materials_selectobjects.png) 개체 선택
재질을 적용할 개체를 모델에서 선택합니다.

#### ![images/toolbarplus.png](images/toolbarplus.png) 새 재질 만들기
렌더링 콘텐츠 재질 [라이브러리](libraries.html)를 엽니다.
라이브러리의 재질은 모델에 재질을 만들 때 템플릿처럼 실행됩니다.

#### ![images/import.png](images/import.png) 파일에서 재질 가져오기
저장된 Rhino .rmtl 파일에서 재질을 가져옵니다.

#### ![images/savetofile.png](images/savetofile.png) 파일에 저장
재질을 Rhino .rmtl 파일로 저장합니다.

#### ![images/changetype.png](images/changetype.png) 유형 변경
재질을 다른 유형으로 변경합니다.

#### ![images/changetype.png](images/changetype.png) 유형 변경 (유사한 설정 복사)
재질을 다른 유형으로 변경합니다.
기본 동작은 [렌더링 옵션](http://docs.mcneel.com/rhino/5/help/ko-kr/index.htm#popup_moreinformation/materialpanel_toolsmenu.htm) > [콘텐츠 형식이 변경되면 시슷한 설정 복사](http://docs.mcneel.com/rhino/5/help/ko-kr/index.htm#popup_moreinformation/materialpanel_toolsmenu.htm) 상자의 현재 상태에 따라 결정됩니다. 이 확인란을 선택하면 기존 콘텐츠에서 호환되는 설정이 새로운 설정으로 복사됩니다.

#### ![images/reset.png](images/reset.png) 기본값으로 다시 설정
모든 재질 설정을 기본 흰색, 무광택, 반사 없음, 텍스처 없는 재질로 변경합니다.

#### ![images/copy.png](images/copy.png) 복사
선택된 재질을 Windows 클립보드로 복사합니다. 클립보드는 편집기로 붙여넣기 실행되어 새 재질이 되거나, 폴더로 바로 붙여넣기 되어 [라이브러리](libraries.html) 파일이 됩니다.

#### ![images/paste.png](images/paste.png) 붙여넣기
클립보드의 콘텐츠를 기준으로 새로운 재질을 만듭니다.

#### ![images/pasteasinstance.png](images/pasteasinstance.png) 인스턴스로 붙여넣기
인스턴스 작업을 통해 원래 재질과 연결되어 있는 클립보드의 콘텐츠를 기준으로 새로운 재질을 만듭니다.

#### ![images/delete.png](images/delete.png) 삭제
선택된 재질을 삭제합니다.

#### ![images/rename.png](images/rename.png) 이름 바꾸기...
선택된 재질의 이름을 변경합니다.

#### ![images/duplicate.png](images/duplicate.png) 복제
선택된 재질을 동일한 설정으로 새 재질에 복사합니다.

#### ![images/removeinstancing.png](images/removeinstancing.png) 인스턴스 제거
[인스턴스](http://docs.mcneel.com/rhino/5/help/ko-kr/index.htm#popup_moreinformation/materialpanel_toolsmenu.htm) 실행된 재질 간의 연결을 제거합니다.
{% include_relative snippets/snippet-contenteditorpreviewoptions.md %}


#### ![images/contentfilter.png](images/contentfilter.png) 콘텐츠 필터
[콘텐츠 필터](content_filters.html) 대화상자를 엽니다.

#### ![images/rename.png](images/rename.png) 속성
[미리보기 속성](http://docs.mcneel.com/rhino/5/help/ko-kr/index.htm#popup_moreinformation/materialpanel_toolsmenu.htm) 대화상자를 엽니다.

---
title: 재질 편집기 패널
---

# ![images/paint.svg](images/paint.svg) {{page.title}}
재질에는 색, 반사, 투명도, 텍스처, 범프 맵, 서피스 마무리 등의 설정이 포함되어 있습니다. 모든 재질에는 기본 설정이 있습니다. 기본 재질은 흰색 무광이며, 반사 또는 투명도가 지정되지 않았습니다. 가장 좋은 결과를 얻으려면 Flamingo 특정 재질을 사용하세요.

재질은 레이어, 개체, 블록에 적용할 수 있습니다. 재질을 마우스로 끌어 개체에 놓는 방법을 비롯해 다양한 방식으로 적용할 수 있습니다. 자세한 정보는 [재질 적용](material_assignment.html) 항목을 참조하세요.

일단 재질이 적용된 후에는 재질이 모델에 저장됩니다. 재질, 텍스처, 렌더링을 위한 모든 지원 파일은 올바르게 지정된 [렌더링 옵션](http://docs.mcneel.com/rhino/5/help/ko-kr/index.htm#options/rendering.htm) 과 함께 Rhino 모델 안에 저장될 수 있습니다. .

재질, 환경, 텍스처가 모델에 저장되지만, 렌더링 콘텐츠 또한 파일에 저장하고 이를 다른 모델과 공유할 수 있습니다. 콘텐츠는 Rhino 세션 간에 마우스로 끌어 폴더에 놓을 수 있습니다. 색 견본도 동일한 방식으로 마우스로 끌어 놓을 수 있습니다. [라이브러리 패널](libraries.html) 에는 기본 콘텐츠 폴더가 표시됩니다. 이것을 사용하여 마우스로 콘텐츠를 끌어 모델에 놓거나, 모델 콘텐츠를 외부 파일로 끌어 놓을 수 있습니다.

![images/material_editor_panel.svg](images/material_editor_panel.svg){:  #panel_map .float-img-right}

##### 이 명령은 어디에서 찾을 수 있습니까?
재질 탭을 찾는 방법에는 몇 가지가 있습니다.

* ![images/materialtab.png](images/materialtab.png)재질 탭
* ![images/icon-render.png](images/icon-render.png)렌더링 도구 도구모음 > ![images/materialtab.png](images/materialtab.png) 재질 편집기
* 메뉴 > 렌더링 메뉴 > 재질 편집기
* 명령행에 MaterialEditor 를 입력합니다.

재질 편집기 패널은 별개의 섹션으로 나뉘어져 있습니다. 재질 유형에 따라 고급 패널이 달라질 수 있습니다.

색과 텍스처는 색 견본에서 원하는 색을 마우스로 선택하여 재질 편집기, [텍스처 팔레트](texturepalette.html), 또는 [환경 편집기](environmenteditor.html)의 색 견본/제어에 놓을 수 있습니다.

##### 재질 패널

 1. [설정 막대](#settings)
 1. [재질 목록](#material_list)
 1. [창 구분](#divider)
 1. [재질 속성 섹션](#properties)
 1. [이름](#name)
 1. [재질 속성 패널](#panels)

## [설정 막대](#panel_map) ![images/callout_1.svg](images/callout_1.svg)
{: #settings .clear-img}
재질 탐색에 이 설정 막대를 사용합니다.

#### ![images/met_leftarrow.png](images/met-leftarrow.png) 뒤로 화살표
현재 재질 또는 이전에 선택된 재질로 되돌아갑니다. 예를 들어, 텍스처가 있는 재질에는 여러 개의 레이어가 있습니다. 이 화살표를 사용하여 텍스처 디테일에서 부모 재질로 돌아갑니다.

####  ![images/met_rightarrow.png](images/met-rightarrow.png) 앞으로 화살표
현재 재질 또는 이전에 선택된 재질에서 앞으로 갑니다. 예를 들어, 텍스처가 있는 재질에는 여러 개의 레이어가 있습니다. 이 화살표를 사용하여 부모 재질에서 최근에 사용된 텍스처로 돌아갑니다.


#### ![images/material_editor.png](images/material_editor.png)![images/texture-2dchecker.png](images/texture-2dchecker.png) 현재 선택된 재질 이름
현재 재질 이름과 레벨을 표시합니다. 예를 들어 텍스처 또는 재질 절차 레벨이 있으면 ">" 표시가 나타납니다. 재질에서 편집기를 보기에 좋은 위치입니다.

#### ![images/library_default.png](images/library_default.png) 도구 메뉴
[도구 메뉴](#tools-menu)를 표시합니다. 이것은 재질과 관련된 명령, 설정, 유틸리티의 확장된 메뉴입니다.


## [재질 목록](#panel_map) ![images/callout_2.svg](images/callout_2.svg)
{: #material_list}
모델에 포함된 모든 재질 목록입니다. 이 목록으로 다음과 같은 작업이 가능합니다:

* 목록에서 위/아래로 스크롤하여 모델의 모든 재질을 봅니다.
* 이 목록에서 재질을 마우스로 끌어 [레이어 패널](http://docs.mcneel.com/rhino/5/help/ko-kr/index.htm#commands/layer.htm)의 레이어에 놓거나 직접 개체에 놓아 재질을 지정합니다. 자세한 정보는 [재질 적용](material_assignment.html)을 참조하세요.
* 목록의 아래쪽에 있는 새 재질 추가 단추 ![images/add_material.png](images/add_material.png) 를 사용하여 새로운 재질을 추가합니다.


* 각 재질을 클릭하여 선택합니다. 재질을 선택하면 해당 재질의 속성이 아래 패널에 표시됩니다. 자세한 정보는 [렌더링 재질 속성](#properties)을 참조하세요
* 썸네일을 오른쪽 클릭하면 재질 관련 메뉴가 표시됩니다.
* 공백의 공간을 오른쪽 클릭하면 새로운 재질 관련 메뉴가 표시됩니다.

###  ![images/add_material.png](images/add_material.png) 새 재질 추가
{: #add_material}
추가 아이콘을 보려면 재질 목록의 아래로 스크롤합니다.

렌더링 콘텐츠 재질 [라이브러리](libraries.html)를 엽니다.
라이브러리의 재질은 모델에 재질을 만들 때 템플릿처럼 실행됩니다.

### 재질 상황에 맞는 메뉴
{: material_context}
이 메뉴는 재질 목록에서 오른쪽 클릭하여 사용할 수 있습니다. 이 메뉴의 다양한 옵션에 대한 자세한 정보는 [도구 메뉴](#tools_menu)를 참조하세요.

### 새로운 재질 상황에 맞는 메뉴
{: new_material_context}
이 메뉴는 재질 목록에서 비어 있는 공간을 오른쪽 클릭하여 사용할 수 있습니다.

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
이 구분선을 마우스로 끌어 재질 목록의 길이를 변경합니다. 재질 목록을 길게 지정하면 재질 속성 섹션이 짧아집니다.

## [재질 속성 섹션](#panel_map) ![images/callout_4.svg](images/callout_4.svg)
{: #properties}

#### [재질 이름](#panel_map) ![images/callout_5.svg](images/callout_5.svg)
{: #name}
재질의 이름입니다. 재질 이름은 재질을 라이브러리로 내보낼 때 파일 이름으로도 저장됩니다. 안내: 재질은 Rhino 모델에 보관됩니다. 서로 다른 Rhino 모델에서 고유한 재질의 이름은 동일할 수 있습니다.

#### [재질 패널](material-editor.html#panel_map) ![images/callout_6.svg](images/callout_6.svg)
{: #panels}
재질 속성 섹션은 몇 가지 직접적인 재질 패널로 구성되어 있습니다. 회색 제목 표시줄을 클릭하면 재질 패널이 접히고 해당 패널의 콘텐츠가 숨김 상태가 됩니다. 제목 표시줄을 다시 클릭하면 콘텐츠가 다시 표시됩니다.

재질 패널은 재질의 유형과 현재 활성인 재질의 레벨에 따라 달라집니다. 특정 재질 패널에 대한 자세한 정보는 [Flamingo 재질](material-type-simple.html)을 참조하세요.

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
 1. [레이어](http://docs.mcneel.com/rhino/5/help/ko-kr/index.htm#commands/layer.htm) 패널에서 하나 이상의 레이어를 선택하고 [재질](http://docs.mcneel.com/rhino/5/help/ko-kr/commands/layer.htm#Material) 열을 클릭합니다.
 1. 레이어 재질 대화상자에서 적용할 재질을 선택합니다.


##### 재질을 레이어에 끌어 놓으려면(drag and drop)
 * 썸네일 또는 목록에서 재질을 대상 레이어로 끌어옵니다.
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

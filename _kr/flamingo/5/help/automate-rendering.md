---
title: 자동 렌더링
---

# {{page.title}}


## 일괄 렌더링
{: #batch-rendering}
일괄 작업을 통해 자동으로 여러 작업을 렌더링 처리할 수 있습니다. 일괄 작업에서 특정 뷰, 해상도, 패스의 수를 지정할 수 있습니다. 하나의 작업 또는 [렌더 팜](render-farm.html)을 사용하여 일괄 작업을 시작할 수 있습니다. 일괄 작업 목록을 열고 원하는 작업을 목록에 추가합니다. 일괄 작업 목록이 모델에 저장됩니다.

##### 이 명령은 어디에서 찾을 수 있습니까?

 * 메뉴 > Flamingo nXt 5.0 > 기타 도구 > 일괄 렌더링

### 일괄 렌더링 대화상자
{: #batch-render}
작업을 추가하여 시작하고 속성을 편집하여 일괄 작업을 설정합니다.

#### 추가
각각의 일괄 작업은 모델에 저장된 뷰를 기준으로 합니다. 추가를 클릭하여 모델의 뷰 목록에서 추가할 항목을 클릭합니다. 작업이 추가되고 선택되면 다른 모든 메뉴 항목이 활성화됩니다.

#### 삭제
기존 일괄 작업을 선택합니다. 삭제를 사용하여 일괄 작업 목록에서 원하는 작업을 제거합니다.

#### 속성
기존 일괄 작업을 선택하고 속성을 선택하여 [일괄 렌더링 속성](#batch-render-properties)을 설정합니다. 속성에는 파일 이름, 해상도, 각각의 작업에 사용될 패스의 수가 포함됩니다.

#### 위로 이동
목록에서 뷰포트 이름을 위로 이동시킵니다.

#### 아래로 이동
목록에서 뷰포트 이름을 아래로 이동시킵니다.

#### 일괄 목록
{: #batch-list}
렌더링될 뷰의 목록에 대한 정보를 표시합니다. [일괄 렌더링 속성](#batch-render-properties)의 설정을 편집하려면 기존 작업을 두 번 클릭합니다.

#### 렌더링 상태
일괄 처리 진행률에 대한 패스, 스캔 라인, 경과 시간 정보를 표시합니다.

####  렌더링 중지
일괄 프로세스를 중지합니다.

#### 로컬에서 일괄 렌더링
{: #render-batch-locally}
현재 컴퓨터만을 사용하여 일괄 작업을 렌더링합니다. 렌더링된 이미지는 [일괄 렌더링 속성](#batch-render-properties)에 지정된 위치에 출력됩니다.

####  일괄 렌더링을 팜으로 보내기
일괄 작업을 [렌더 팜](render-farm.html)으로 보냅니다. 작업은 모든 사용 가능한 팜 클라이언트에서 렌더링됩니다. 렌더링 이미지는 공유된 팜 폴더에 출력됩니다.

### 일괄 렌더링 속성
{: #batch-render-properties}

#### 렌더링할 뷰포트
이 작업에서 렌더링될 뷰를 표시합니다. [렌더링 탭, 렌더링할 뷰포트](render-tab.html#viewtorender)를 참조하세요.

#### 파일 이름
저장 단추 ![images/saveimageas.png](images/saveimageas.png)를 클릭하고 렌더링된 이미지의 파일 이름을 지정합니다.

#### 알파 채널
알파 채널과 함께 이미지를 저장합니다. 자세한 안내는 [알파 채널 배경 사용](environment-tab.html#alpha)을 참조하세요.

#### 문서 설정 사용
{: #rendering-resolution}
렌더링에 현재 문서 해상도를 사용하는 것이 기본값입니다. 다른 해상도가 필요하다면 이 선택란을 해제하고 원하는 해상도를 지정합니다. [렌더링 탭, 해상도](render-tab.html#resolution) 항목을 참조하세요.

#### 렌더링 제한 조건 패스
{: #rendering-constraints}
일괄 작업을 완료하는 데 필요한 패스의 수를 설정합니다. 자세한 안내는 [패스](documentproperties-flamingo.html#number-of-passes) 항목을 참조하세요.

<!-- TODO: Flamingo nXt 5 runs from the RDK.  The need to Flamingo Automate render is not clear.  What is needed to run animations with nxt right now? Alpha channel This needs to be investigated. The rest of this section is commented out.-->

<!-- Commented out until automated render can be determined

## 애니메이션
{: #animation}
Rhino에서 애니메이션을 생성하는 방법에는 두 가지가 있습니다. [Rhino의 애니메이션 도구모음](http://docs.mcneel.com/rhino/5/help/ko-kr/index.htm#commands/animation.htm)을 설정하거나 [Bongo](http://bongo.rhino3d.com/) 애니메이션 플러그인을 사용하는 것입니다.

##### 렌더 팜에 애니메이션 작업을 전송하려면
1. [FlamingoNXtAutomateRender](automate-rendering.html#flamingonxtautomaterender) 명령을 실행합니다.
1. 자동 렌더링 명령 설정 대화상자에, **팜으로 렌더링**을 선택합니다.
 
작업 이름을 지정하고 확인 단추를 클릭합니다.
 
Rhino의 애니메이션 설정 도구모음에서 애니메이션 종류를 설정합니다. 전체_렌더링을 캡처 방법으로 선택합니다.
 
애니메이션 도구모음에서 애니메이션을 기록합니다. 렌더링 작업이 렌더 팜으로 전송됩니다.
 
렌더 팜에서 작업이 완료되면 FlamingoNXtAutomateRender 명령을 다시 실행하여 대화상자의 모든 작업을 선택합니다.
 
선택 파일을 지정된 출력 폴더로 복사 단추를 클릭하고 모든 렌더링 이미지가 복사될 폴더를 선택합니다.


## FlamingoNXtAutomateRender 명령
{: #flamingonxtautomaterender}


## 자동 렌더링 명령 설정

### 사용
기본 **Render** 명령에서 **렌더 팜**을 사용하도록 리디렉션합니다.

### 기본 렌더링 대화 사용
렌더 팜에서가 아니라 **Render** 명령이 직접 렌더링하도록 다시 설정합니다.

### 렌더링하기 위한 렌더링 패스의 수
렌더링 패스의 수를 지정합니다.

### 팜으로 렌더링
팜으로 렌더링하기 위해 **Render** 명령을 리디렉션합니다.

### 작업 이름
**Render Farm**  [작업 이름](automate-rendering.html#job-name)을 지정합니다.

## 렌더링 제한 조건

### 렌더링하기 위한 렌더링 패스의 수
[패스의 수](documentproperties-flamingo.html#number-of-passes)를 지정합니다.

### 알파 채널 저장
[알파 채널](render-window.html#save-with-alpha-channel) 배경을 저장합니다.
-->

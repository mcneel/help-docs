---
---


# ![images/flamingotab.svg](images/flamingotab.svg){:height="75px" width="75px"} Flamingo nXt® 처음 시작
Flamingo nXt는 Rhinoceros ®안에서 3D 모델을 가지고, 고화질의 마치 사진과도 같은 스틸과 애니메이션 이미지를 만듭니다. Flamingo nXt 5는, Rhino 5에 탑재된 렌더링 기능과 통합되는 Flamingo의 업데이트 버전입니다. 현재 개발 중(WIP: Work in Progress)인 버전입니다.

Flamingo는 [Flamingo nXt 5 다운로드](http://www.rhino3d.com/download/flamingo/5/beta)에서 다운로드하여 설치하실 수 있습니다.

[Flamingo Discourse Forum](http://discourse.mcneel.com/c/rendering/flamingo)에서 기술적인 토론에 참여하실 수 있습니다.

## 설치

* Flamingo 5 Beta를 사용하시려면 이전 버전의 Flamingo nXt가 설치되어 있어야 합니다.
* Flamingo nXt 5를 실행하시려면 Rhino 5 서비스 릴리스(SR) 12가 필요합니다.

RHI 설치 관리자를 다운로드하신 후에 설치하시고, Rhino를 시작합니다.

기술 지원, 튜토리얼, 샘플 파일, **Flamingo nXt** 사용 및 처음 시작에 대한 안내는 [Flamingo nXt 웹사이트](http://nxt.flamingo3d.com/)를 참조하세요.

> [튜토리얼](http://nxt.flamingo3d.com/page/tutorials-and-documentation-kr)
> [갤러리](http://nxt.flamingo3d.com/photo)
> [기술 지원](http://nxt.flamingo3d.com/forum)

## Flamingo nXt 제어 패널
{: #control-panel}
This version of Flamingo features and interface which is integrated with the Rhino 5 rendering tools. The Flamingo nXt Control Panel provides tabs for setting up the model for rendering, including:

> [재질](materials-tab.html)
> [조명](lighting-tab.html)
> [환경](environment-tab.html)
> [렌더링](render-tab.html)

## Flamingo 제어 패널에 액세스하려면
* Flamingo nXt 5.0 메뉴에서 제어 패널을 클릭합니다.

## 렌더링 기초
{: #rendering-basics}
완성된 모델을 렌더링하는 데에는 네 가지 기본적인 과정이 필요합니다.

 1. [재질 설정](material-editor.html)
 1. [조명 설정](lighting-tab.html)
 1. [환경 설정](environment-tab.html)
 1. [렌더링 조건 설정](render-tab.html)

##### 렌더링을 시작하려면
* 렌더링하려면 렌더링 메뉴 또는 Flamingo nXt 메뉴에서 렌더링을 클릭합니다.
* 또는, 표준 도구모음에서 렌더링 단추를 클릭합니다.

### 렌더링 중지
기본적으로, 렌더링 프로세스는 사용자가 렌더링 중지 단추를 클릭할 때까지 패스를 거듭하면서 이미지를 계속해서 구체화시킵니다. 사용자가 원하는 대로 시간과 화질의 균형을 맞출 수 있습니다. 렌더링 시간이 길어지면 보다 집중된 결과물에 더욱 가까워집니다. 언제든지 렌더링을 중지시킬 수 있습니다.

### 렌더링 다시 시작
렌더링 중지 단추를 클릭하면 현재 패스가 완료된 후에 렌더링 프로세스가 일시 중지됩니다.
이 단추는 렌더링 다시 시작 단추로 변경됩니다. 지정된 패스의 수가 완료되기 전이나, 제한된 시간에 이르기 전에 렌더링을 중지한 경우, 렌더링 다시 시작 단추를 클릭하여 렌더링을 계속할 수 있습니다.
[렌더링 창](render-window.html) 또는 [문서 속성 Flamingo nXt](documentproperties-flamingo.html)에서 [패스의 수](render-window.html#number-of-passes) 또는 [시간](render-window.html#time) 설정을 사용하여 자동으로 중지되는 시점을 지정하세요.

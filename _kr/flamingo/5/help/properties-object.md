---
title: 개체 속성
---


#  ![images/properties.svg](images/properties.svg) {{page.title}}
Flamingo nXt 개체 속성은 Flamingo nXt에서 개체를 렌더링하는 방식에만 영향을 미칩니다.

### ![images/materialtab.png](images/materialtab.png) 재질 소스
{: #material-source}
재질은 레이어, 블록, 개체에 적용할 수 있습니다. 재질을 적용하는 방법에 대한 자세한 안내는 [재질 적용](material_assignment.html) 항목을 참조하세요. 재질이 개체_기준으로 설정된 경우, 재질 속성이 이 대화상자에도 표시됩니다. 재질 편집에 대한 자세한 안내는 [재질 속성](material-type-simple.html) 항목을 참조하세요.

### ![images/apply-cylindrical-mapping.png](images/apply-cylindrical-mapping.png) 텍스처 매핑
{: #texture-mapping}
레이어나 개체에 재질이 적용되면, 매핑은 재질이 특정 개체에 어떻게 위치(매핑)하는지를 제어합니다. 눈의 띄는 패턴이 없는 재질은 일반적으로 매핑을 제어할 필요가 없습니다. 재질에 특정한 방향이 있거나 분명한 패턴이 있다면 매핑을 사용합니다. 이 경우에도 기본 매핑으로 충분합니다. 매핑은 개체와 함께 유지되고 개체가 이동/회전/크기 조정되면 그에 맞춰 따라갑니다. 매핑 유형에 대한 자세한 정보는 [텍스처 매핑](http://docs.mcneel.com/rhino/5/help/ko-kr/index.htm#properties/texturemapping.htm) 항목을 참조하세요.

![images/mapping-cube.png](images/mapping-cube.png) ![images/mapping-planar.png](images/mapping-planar.png)
*두 개의 다른 매핑 방향*

### ![images/decalproperties.png](images/decalproperties.png) 데칼
{: #decals}
데칼은 재질을 간접적으로 사용하지 않고, 개체에 직접 적용하는 비(非) 타일 방식의 이미지 맵입니다. 개체 색, 반사도 또는 범프에서 제한된 부분을 수정할 때 데칼을 사용합니다. 데칼의 생성과 배치에 대한 자세한 정보는 [Rhino 데칼](http://docs.mcneel.com/rhino/5/help/ko-kr/index.htm#properties/decal.htm) 항목을 참조하세요.

![images/freshmilk.png](images/freshmilk.png) ![images/decal-planar-001.png](images/decal-planar-001.png)
![images/cylindricaldecal-002.png](images/cylindricaldecal-002.png) ![images/uvmapdecal-00.png](images/uvmapdecal-00.png)
*네 개의 서로 다른 데칼의 예*

### ![images/apply-edge-softening.png](images/apply-edge-softening.png) 사용자 지정 메쉬
{: #custom-meshes}
몇몇 사용자 지정 메쉬 설정은 Rhino에서 렌더링 모델을 더 구체적으로 표현하는 데 사용될 수 있습니다. 이 설정에서 둥근 가장자리, 패널 셧 라인, 커브로 케이블 만들기 등을 설정할 수 있습니다.

관련 정보는 다음 항목을 참조하세요:

>[부드러운 가장자리](http://docs.mcneel.com/rhino/5/help/ko-kr/index.htm#commands/applyedgesoftening.htm)
>[커브 파이프](http://docs.mcneel.com/rhino/5/help/ko-kr/index.htm#commands/applycurvepiping.htm)
>[셧 라인](http://docs.mcneel.com/rhino/5/help/ko-kr/index.htm#commands/applyshutlining.htm)
>[변위](http://docs.mcneel.com/rhino/5/help/ko-kr/index.htm#commands/applydisplacement.htm)

### ![images/object-flamingo.PNG](images/object-flamingo.PNG) Flamingo 속성
{: #flamingo-properties}

#### 알파 채널
{: #alpha-channel}
개체를 안 보이게 만듭니다. 투사되는 그림자와 개체에 보이는 그림자는 렌더링됩니다. 이미지는 다른 이미지와 겹쳐질 수 있으며, 그림자는 합성 이미지에 표시됩니다.

![images/building.png](images/building.png)
위의 예에서, 건물에 드리워지는 나무 그림자가 표시될 수 있도록 이미지와 일치하는 간단한 평면 서피스가 만들어졌습니다. 알파 채널 속성으로 태그된 평면은 렌더링을 실행하면 해당 평면은 보이지 않으나 그림자는 여전히 표시됩니다. 부분적으로 투명한 이미지가 다른 이미지상에 겹쳐졌습니다.

#### 코스틱
{: #caustics}
곡면을 가진 개체 또는 다른 표면에 투영되어, 반사되거나 굴절된 빛의 광선입니다. 코스틱은 매우 특정한 상황에서만 사용되어야 합니다. 코스틱 설정에서는 [경로 추적기](render-tab.html#path-tracer) 엔진 또는 [하이브리드](render-tab.html#hybrid) 렌더링 엔진만으로 렌더링됩니다. 코스틱 계산은 수렴하는 데 많은 패스가 소요됩니다. 자세한 정보는 [Wikipedia 항목: Caustic (optics)](http://en.wikipedia.org/wiki/Caustic_(optics)) 을 참조하세요.

![images/kaustik.png](images/kaustik.png)
* 물이 든 유리잔을 통해 만들어진 코스틱*

![images/caustics-001.png](images/caustics-001.png)
*코스틱이 없는 상태 (왼쪽), 코스틱이 있는 상태 (오른쪽).*

#### 얇음
{: #thin}
닫힌 공간을 가진 투명한 개체는 투명한 굴절에서 보통은 솔리드로 다뤄집니다. 얇음 속성으로 설정하면 각각의 서피스가 2면을 가진 개체로 간주되어 굴절이 실행됩니다. 이 설정은 건축 모델에서 유리와 같은 단일 서피스가 쓰일 때 사용됩니다.

![images/thin.png](images/thin.png) ![images/thinoff.png](images/thinoff.png)
* 기본 Rhino 모델 (왼쪽), 보통 (가운데), 얇은 상태 (오른쪽).*

#### 데이라이트 포털
{: #daylight-portal}
데이라이트 포털(Daylight Portal)은 인테리어 렌더링에서 [태양과 하늘 조명](lighting-tab.html#interior-daylight)이 비춰지는 열린 부분입니다. 데이라이트 포털은 태양, 하늘, 지상의 빛을 자연스러운 방식으로 실내 공간으로 들입니다. 데이라이트 포털은 [태양](sun-and-sky-tabs.html#sun) 설정이 켜져 있는 경우에만 영향을 줍니다. 조명 설정이 [실내 주광](lighting-tab.html#interior-daylight)으로 설정된 경우, 자동으로 모든 투명한 서피스가 데이라이트 포털로 작용합니다. 조명 기본 설정을 스튜디오 또는 실외 주광으로 설정하고도 여전히 바깥의 태양광과 천공광을 실내 공간으로 가져오고 싶을 때에는 사용자가 직접 창을 데이라이트 포털로 태그해야 합니다.

![images/daylightportal-001.png](images/daylightportal-001.png)
* 데이라이트 포털 설정 (왼쪽), 데이라이트 포털 없음 (오른쪽).*

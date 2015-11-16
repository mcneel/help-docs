---
titla: 개체 속성
---


#  ![images/properties.svg](images/properties.svg) {{page.title}}
Flamingo nXt 개체 속성은 Flamingo nXt에서 개체를 렌더링하는 방식에만 영향을 미칩니다.

### ![images/materialtab.png](images/materialtab.png) 재질 소스
{: #material-source}
A material can be assigned to layers, blocks, and objects.  For details on Assigning material see the [Material Assignments](material_assignment.html) topic. If the material is set to ByObject, then the material properties are also displayed in this dialog.  For more details on editing a material, see [Material Properties](material-type-simple.html).

### ![images/apply-cylindrical-mapping.png](images/apply-cylindrical-mapping.png) 텍스처 매핑
{: #texture-mapping}
Mapping controls how a material is located (mapped) on a particular object. The method used to assign a material whether to a layer or object does not effect mapping. For materials that have no noticeable pattern, it is normally not necessary to control the mapping. Use mapping where the material is directional or has an obvious pattern. Even in these cases, the default mapping may be adequate. Mapping remains with the object and follows it if it is moved, rotated, or scaled. For details on the mapping types see the [Texture Mapping](http://docs.mcneel.com/rhino/5/help/en-us/index.htm#properties/texturemapping.htm) topic.

![images/mapping-cube.png](images/mapping-cube.png) ![images/mapping-planar.png](images/mapping-planar.png)
*Two different mapping directions*

### ![images/decalproperties.png](images/decalproperties.png) 데칼
{: #decals}
Decals are non-tiling image maps that apply directly to objects instead of indirectly using a material. Use decals to modify a limited part of an object's color, reflectivity, or bumps. See the [Rhino Decals](http://docs.mcneel.com/rhino/5/help/en-us/index.htm#properties/decal.htm) for details on creating and placing decals.

![images/freshmilk.png](images/freshmilk.png) ![images/decal-planar-001.png](images/decal-planar-001.png)
![images/cylindricaldecal-002.png](images/cylindricaldecal-002.png) ![images/uvmapdecal-00.png](images/uvmapdecal-00.png)
*Four different decal examples*

### ![images/apply-edge-softening.png](images/apply-edge-softening.png) 사용자 지정 메쉬
{: #custom-meshes}
Several custom mesh modifiers can be used in Rhino to detail rendered models. Use these modifiers to round edges, add panel shut lines, and create cables from curves.

For more details go to the topics below:

>[부드러운 가장자리](http://docs.mcneel.com/rhino/5/help/ko-kr/index.htm#commands/applyedgesoftening.htm)
>[커브 파이프](http://docs.mcneel.com/rhino/5/help/ko-kr/index.htm#commands/applycurvepiping.htm)
>[셧 라인](http://docs.mcneel.com/rhino/5/help/ko-kr/index.htm#commands/applyshutlining.htm)
>[변위](http://docs.mcneel.com/rhino/5/help/ko-kr/index.htm#commands/applydisplacement.htm)

### ![images/object-flamingo.png](images/object-flamingo.png) Flamingo 속성
{: #flamingo-properties}

#### 알파 채널
{: #alpha-channel}
개체를 안 보이게 만듭니다. 투사되는 그림자와 개체에 보이는 그림자는 렌더링됩니다. 이미지는 다른 이미지와 겹쳐질 수 있으며, 그림자는 합성 이미지에 표시됩니다.

![images/building.png](images/building.png)
위의 예에서, 건물에 드리워지는 나무 그림자가 표시될 수 있도록 이미지와 일치하는 간단한 평면 서피스가 만들어졌습니다. 알파 채널 속성으로 태그된 평면은 렌더링을 실행하면 해당 평면은 보이지 않으나 그림자는 여전히 표시됩니다. 부분적으로 투명한 이미지가 다른 이미지상에 겹쳐졌습니다.

#### 코스틱
{: #caustics}
The light rays reflected or refracted by a curved object or the projection of those rays on another surface. Caustics should be used in very specific situations. Caustics are only rendered with the [Path Tracer](render-tab.html#path-tracer) engine or the [Hybrid](render-tab.html#hybrid) render engine.  Caustic calculations takes many passes to converge. See [Wikipedia article: Caustic (optics)](http://en.wikipedia.org/wiki/Caustic_(optics)) for more information.

![images/kaustik.png](images/kaustik.png)
*Caustics produced by a glass of water.*

![images/caustics-001.png](images/caustics-001.png)
*Without caustics (left), and with caustics (right).*

#### Thin
{: #thin}
A space-enclosing, transparent object is normally treated as a solid for transparent refraction. Setting the Thin property means that each surface will be treated as a two-sided object for refraction. This is the setting to use if single surfaces as glass are used for architectural models.

![images/thin.png](images/thin.png) ![images/thinoff.png](images/thinoff.png)
*Base Rhino model (left), Normal (middle) and Thin (right).*

#### 데이라이트 포털
{: #daylight-portal}
A daylight portal is an opening for [Sun and Sky lighting](lighting-tab.html#interior-daylight) for an interior rendering. A Daylight portal pulls sun, sky, and ground light into an interior space in a natural way. Daylight portals only have an effect when the [Sun](sun-and-sky-tabs.html#sun) is turned on. When the lighting scheme is set to [Interior daylight](lighting-tab.html#interior-daylight), all transparent surfaces act as daylight portals automatically. It is only when the lighting scheme is set to Studio or Exterior daylight and you still want to bring outside sun and sky light into an interior space that you must manually tag the windows as daylight portals.

![images/daylightportal-001.png](images/daylightportal-001.png)
*With daylight portal (left), without daylight portal (right).*

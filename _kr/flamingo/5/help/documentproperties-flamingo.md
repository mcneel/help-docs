---
---


# Document Properties: Flamingo nXt
이러한 설정은 현재 모델에만 적용됩니다. 렌더링을 완료하는 데 필요한 시간이 길어질수록 원하는 화질로 렌더링이 완성됩니다.

##### To change settings

>On the **Flamingo nXt** menu, click **Document Properties**.

## 재질
{: #materials}

### Use materials
{: #use-materials}
Flamingo nXt 와 Rhino 재질을 사용하여 렌더링합니다. 재질이 적용되지 않은 개체는 하얗게 렌더링됩니다.

### Use object color
{: #use-object-color}
Rhino 개체 또는 레이어 색에서 지정된 색을 사용하여 렌더링합니다.
 **Note** : Both **Use materials** and **Use object color** can be checked. In this case, objects that have materials assigned will use those materials. Other objects will render using their object or layer color.

## Bounces
{: #bounces}

### Reflective
{: #reflective-bounces}
얼마나 많은 수준의 반사가 허용되는지를 결정합니다. 즉, 광선이 개체를 몇 번이나 비추는가가 지정됩니다. 0으로 설정하면 반사를 사용하지 않는 것으로 설정됩니다. 값이 높을수록 렌더링 시간이 길어집니다.

### Refractive
{: #refractive-bounces}
얼마나 많은 수준의 굴절이 허용되는지를 결정합니다. 즉, 광선이 개체를 몇 번이나 굴절시키는지가 지정됩니다. 0으로 설정하면 굴절을 사용하지 않게 됩니다. 값이 높을수록 렌더링 시간이 길어집니다.

### Indirect
{: #indirect-bounces}
얼마나 많은 수준의 간접 조명이 허용되는지를 결정합니다. 즉, 간접 조명 광선이 개체를 몇 번이나 바운스시키는지가 지정됩니다. 0으로 설정하면 반사를 사용하지 않는 것으로 설정됩니다. 값이 높을수록 렌더링 시간이 길어집니다.

## Display in rendered viewports
 **Note** : These settings only affect viewports using Rhino's Rendered display mode. To see these objects in a rendered image, use [Post Effects](render-window.html#postprocessingwireframe).

### Curves
{: #rendercurves}
렌더링된 뷰포트에 커브가 표시됩니다.

### Dimensions and text
{: #renderdimensions}
렌더링된 뷰포트에서 치수와 텍스트 표시.

### Isocurves
{: #renderisocurves}
렌더링된 뷰포트에서 아이소커브 표시.

### Mesh edges
{: #rendermeshedges}
렌더링된 뷰포트의 메쉬 가장자리 표시.

## Miscellaneous

### 꺼진 레이어의 조명 사용
{: #uselightsonlayersthatareoff}
꺼져 있는 레이어에 있는 조명과 숨겨진 조명을 사용합니다.

## Render constraints
{: #number-of-passes}
{: #time}
{: #render-constraints}
{% include_relative snippets/snippet-renderconstraints.md %}
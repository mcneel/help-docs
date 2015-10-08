---
---


# Advanced Material Properties: Transparency
The Transparency settings control&#160;properties associated with light passing through a material.
![images/transparentmaterials.png](images/transparentmaterials.png)

### Transparency
불투명한 재질을 투명한 재질로 변경합니다. 투명한 재질은 렌더링 시간을 증가시킵니다.
![images/transparency.png](images/transparency.png)

### Index of Refraction
{: #index-of-refraction}
재질을 통해 그 너머에 있는 개체를 볼 때 굴절이 얼마나 발생하는지를 결정합니다.
![images/transparencyior.png](images/transparencyior.png)
다음 표는 굴절률의 일부 예를 나타냅니다.

### 재질

### IOR
진공
1. Air
1. Ice
1. Water
1. Glass
1. Emerald
1. Ruby/Sapphire
1. Diamond
1. 
### Translucency
{: #translucency}
확산의 정도입니다. 높은 반투명도는 더 많은 빛이 재질을 통과하면서 불규칙하게 산란되므로, “샌드블라스트(sandblasted)” 효과를 만들어냅니다.
![images/transparencytl.png](images/transparencytl.png)

### Scattering
{: #scattering}
단위 길이당 입자와 빛이 만나는 확률을 제어합니다.
 **Note** : The&#160; [Path Tracer](render-tab.html#path-tracer) &#160;is required for this effect.
표면하 확산(Subsurface scattering)은 빛이 개체의 표면을 관통하고 어떤 방향으로든 확산되는 것을 가능하게 합니다. 많은 반투명 재질들은 이 효과를 사용하여 모델링될 수 있습니다. 빛이 짧은 거리를 통과하도록 설정하면, 돌이나 피부같은 특정한 표면을 현실성 있게 “부드럽게 처리”할 수 있습니다.
재질이 어느 정도 반투명해야 표면하 확산이 발생할 수 있습니다. 이것은 체적을 나타내는 효과(volumetric effect)입니다. 이 효과가 올바르게 실행되려면 이 재질이 적용되는 개체가 솔리드 또는 "폐쇄된 공간"이어야 합니다.
![images/scattering.png](images/scattering.png)

### Attenuation
{: #attenuation}
Determines how much light is absorbed as it passes through the object— greater values produce a more cloudy appearance. Use **Attenuation** to model liquids. Clear liquids have low **Attenuation** ; murky liquids have higher **Attenuation** values.
![images/attenuation.png](images/attenuation.png)

### Dispersion
{: #dispersion}
빛이 얼마나 많이 구성 요소 파장으로 분할되는지를 제어합니다.
![images/dispersion.png](images/dispersion.png)

### Saturation
{: #saturation}
굴절 분산의 양을 결정합니다.
![images/saturation.png](images/saturation.png)

### Blurry Transparency
{: #blurry-transparency}
재질이 부분적으로 투명할 때 재질이 더욱 자연스럽게 보이도록 적은 양의 노이즈가 투명도에 더해집니다.

#### Blurriness
노이즈가 추가되는 정도를 제어합니다.
![images/blurrytransparency.png](images/blurrytransparency.png)

### Glow
{: #glow}
마치 빛이 비추고 있는 것과 같은 착각을 불러일으킵니다.
![images/glow.png](images/glow.png)

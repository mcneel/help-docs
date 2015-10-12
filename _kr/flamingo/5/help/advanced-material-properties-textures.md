---
---


# Advanced Material Properties: Textures
이미지 맵과 범프 맵, 이렇게 두 가지 유형의 맵을 재질에 추가할 수 있습니다. 이미지 맵은 비트맵 이미지를 사용하여 재질에 디테일을 더합니다. 이미지는 색상, 입체처럼 표현하는 서피스 (범프) 등, 서피스 재질의 많은 특성을 바꿀 수 있습니다. 범프는 표면에 불규칙적으로 거칠거나 울퉁불퉁한 느낌을 부여합니다.
![images/textures.png](images/textures.png)
이미지 맵은 래스터 기반 페인트 프로그램이나 스캔한 사진, 또는 다른 재질을 가지고 만든 2차원 패턴입니다. 이미지 맵은 다양한 방식으로 사용할 수 있습니다. 실제 재질의 사진을 재질 색으로 사용하는 것이 일반적인 방식입니다.

## Textures
{: #textures}
지정된 이미지 파일의 미리보기를 나타내는 단추입니다.

>Click a button with an image to edit its [texture properties](texture-properties-main.html). Click a blank image button to apply a new image.

텍스처는 여러 개의 이미지로 구성할 수 있습니다. 때때로 하나의 이미지는 색을 제어하고, 다른 이미지로 텍스처의 범프 속성을 제어합니다.

## Bump Patterns
{: #bump-patterns}
범프는 변위 맵을 사용하거나 또 다른 맵을 사용하지 않아도 표면의 질감을 특정하게 표현합니다. 범프 맵 중 하나를 체크하면 다른 제어를 사용할 수 있습니다. 범프는 수학적인 규칙을 사용하여 마치 표면이 울퉁불퉁한 것처럼 보이도록 재질을 표현합니다. 하나보다 많은 범프 패턴을 하나의 재질에 추가할 수 있습니다.
Materials like stucco, concrete, and clay have a fine texture. It is probably not worth scanning a piece of the material to make a bitmap for it unless it will be viewed at close range. Using a **Sandpaper** procedural bump on a ** [Base Color](advanced-material-properties-main.html#color) ** emulates this kind of fine pattern. Create a ** [Base Color](advanced-material-properties-main.html#color) ** that is the color of the material. Then add a procedural bump to the material. Use **Sandpaper** for a fine texture and **Rubble** for a coarser texture.

### Sandpaper
{: #sandpaper}
랜덤하고 세밀하게 텍스처 처리된 모습으로 표현됩니다.
![images/sandpaper.png](images/sandpaper.png)

### Rubble
{: #rubble}
Gives the appearance of a lumpy, pitted surface. It can be scaled up and used for water, dirt, and smudges on surfaces. **Rubble** bump has a larger size range than **Sandpaper**.
![images/rubble.png](images/rubble.png)

### Pyramid
{: #pyramid}
널링(knurling) 패턴처럼, 작은 피라미드 형태의 돌기를 표현합니다.
![images/pyramid.png](images/pyramid.png)

### Wrinkled
{: #wrinkled}
주름과 같은 모습으로 표현됩니다.
![images/wrinkled.png](images/wrinkled.png)

### Marbled
{: #marbled}
대리석과 같은 모습으로 표현됩니다.
![images/marbled.png](images/marbled.png)

## Scale
{: #scale}
비율은 범프의 비례적 크기를 제어합니다.

#### X/Y/Z
각 방향에서의 비율을 별도로 지정합니다.
![images/texturescalexy.png](images/texturescalexy.png)

#### Lock
종횡비를 유지합니다.

## Properties

#### Strength
{: #strength}
깊이 표시를 제어합니다.
![images/texturestrength.png](images/texturestrength.png)

#### Rotation
{: #rotation}
패턴의 회전 각도를 설정합니다.
절차적 맵에 분명한 패턴이 있거나, 범프맵이 방향성 패턴을 만들기 위해 서로 다른 X, Y, Z 구성 요소를 기준으로 크기 조정된 경우에만 방향을 바꾸는 것이 분명하게 보입니다.
![images/texturerotated.png](images/texturerotated.png)

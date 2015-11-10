---
---

#  ![images/paint.svg](images/paint.svg){:height="75px" width="75px"} Procedural Materials
The Procedures tree combines one or more materials using a set of rules for how the materials interact. The tree displays the components used to create the material and lets you add components. For simple materials, there will be only one component in the list: Base.
<!-- TODO: We need an diagram describing the Proceedure Hirarchyarchy. -->

Each procedure combines two &quot;child&quot; materials using a specific method. Each of these child materials can in turn consist of a procedure, combining two children of its own. In this way, extremely elaborate materials can be built from simpler constituents. Procedures for combining materials include:

> [Base](#base)
> [Angular Blend](#angular-blend)
> [Blend](#blend)
> [Marble](#marble)
> [Granite](#granite)
> [Tile](#tile)
> [Wood](#wood)

##### To add a procedure
1. Right-click anywhere in the Procedures window.
1. On the menu, click a procedure type.

##### To remove a procedure
 1. In the Procedures window, right-click the procedure name.
 2. On the menu, click Remove.

## Base
{: #base}
This is the basic simple material with no layers. This is the default procedure.

## Angular Blend
{: #angular-blend}
Many materials change color, reflection, or transparency based on the angle the material is viewed. The Angular Blend procedure blends between two materials based on the angle of view to the surface of the object.

![images/angularblendmaterials.png](images/angularblendmaterials.png)
The Angular Blend procedure blends between two different materials to create special effects. The two layers in the procedure are the Inner and the Outer Layer.

#### Inner
From 0 degrees from the viewpoint to the Start angle, the Inner component will show completely. Think of this as a base material.

#### Outer
From the Stop angle to 90 degrees from the view, the Outer component will be the only material showing. Think of this as a coating.

#### Start angle
The angle from the viewpoint at which the Outer component material starts.

#### Stop angle
The angle from the viewpoint at which the Outer component material stops.
Between the Start Angle and the Stop angle, the Inner and the Outer components blend.

In the illustration below, the Start angle![images/01.png](images/01.png) is 30 degrees (which in rendering translates to the the green circle on the right) and the Stop angle![images/01.png](images/01.png) is 60 degrees (in the rendering that translates to the red circle).
The image at the left shows the the Inner material as white, and the Outer material as black.

![images/angularblend-003.png](images/angularblend-003.png) ![images/angularblend-001.png](images/angularblend-001.png)

* Between 0 and 30 degrees from the viewpoint, you see white.
* Between 30 and 60 degrees from the viewpoint, you see a gradient from white to black.
* Between 60 and 90 degrees from the viewpoint, you see black.

## Blend
{: #blend}
The Blend procedure combines two base components and controls the proportions of each. All of the standard library wood materials use a Blend procedure to change the finish of the wood from clear matte to dark shiny.
![images/blend-001.png](images/blend-001.png)
기본 패턴 재질에 전체적인 색을 추가하여 전체 재질 정의를 바꿀 때 블렌드가 잘 실행됩니다.

#### 블렌드
Varies the percentage of each component material used in the final material.  For instance, the material below shows a blend between the striped material and solid green color. The left image shows the slider to the left, showing a strong stripe material and weak green.  The middle image show the slider in the middle and 50% striped and 50% green color blended.  The image to the right shows a weak striped material with a strong green material, so the slider is at the right of the Blend slider.
![images/blendpercent.png](images/blendpercent.png)

#### Use image
Bitmap images usually consisting of grayscale patterns define where two component materials will show. The materials are blended by the value of the gray pixels in the image. Use a grayscale image map to mediate between the first and second components. The First component will be placed where there is black in the bitmap pattern, and the Second component will be placed where there is white in the bitmap pattern.
<!--TODO: The first sentence needs work. -->

그림에서 처음과 두 번째 구성 요소에 모두 동일한 재질이 사용되었으나, 블렌드는 세 개의 다른 비트맵으로 제어됩니다.
![images/blendmask.png](images/blendmask.png)
The resolution of the mask bitmap affects the material quality. Higher resolution bitmaps allow a viewpoint closer to the material with fewer quality issues, but they also use more memory.

#### Use Alpha channel
색이 블렌드되는 곳을 결정할 때 이미지에 알파 채널이 있으면 비트맵 회색조 대신 알파 채널이 사용될 수 있습니다.

#### Reverse
The First component will be placed where there is white in the bitmap pattern, and the Second component will be placed where there is black in the bitmap pattern.

#### Tiles
The scale of the material is independent of the resolution of the bitmap used to define it. In order to scale the material correctly, decide how large an area in real units one copy of the bitmap represents. If the bitmap represents the height of six 4-unit tiles and the length represents twelve 4-unit tiles, the scale would be 48 units in the x-direction and 24 units in the y-direction. This stretches the bitmap to the proper size for the pattern.

#### Width
이미지의 단일 인스턴스 너비 (픽셀 단위).

#### Height
이미지의 단일 인스턴스 높이 (픽셀 단위).

## Granite
{: #granite}
Creates a 3-D material with solid pockets of a second material embedded in the Base component. The Granite procedure combines a randomly distributed Spot component in a Base component. The Granite procedure defines how the Base and Spot components combine. Granite procedures can be used for a variety of different materials including rust, sparkly plastic, and other randomly spotted materials.
![images/granitematerials.png](images/granitematerials.png)

#### Base/Spot
The Base and Spot components are two materials. Their properties are specified in the same way as any material.
![images/granitescale.png](images/granitescale.png)
{% include_relative snippets/snippet-materialscaleandlock.md %}

#### Density
전체 패턴의 일부. 이 설정값을 높이면 반점의 상대적 크기도 커집니다.
![images/granitedensity.png](images/granitedensity.png)
{% include_relative snippets/snippet-materialblend.md %}
![images/graniteblend.png](images/graniteblend.png)

## Marble
{: #marble}
Creates alternating slabs of Base and Vein components. The Marble procedure defines how the Base and Vein components combine. The slabs are infinitely large, and the orientation of the object affects the way the slabs are oriented with respect to the object.

![images/marbled.png](images/marbled.png)

Texture [mapping](properties-object.html#mapping) for the objects controls the orientation of the material on the object.
![images/materialunmapped.png](images/materialunmapped.png)
텍스처 매핑 없음 (왼쪽). 텍스처 매핑 적용 상태 (오른쪽).

#### Base/Vein
The Base and Vein components are two materials. Their properties are specified in the same way as any material.
{% include_relative snippets/snippet-materialscaleandlock.md %}![images/marblescale.png](images/marblescale.png)

#### Vein Width
Alters the relative size of the slabs to each other. Vein Width is a fraction of the distance from one Base stripe to the next. Values range from 0 (zero) for no Vein component to 1 for no Base component.
![images/marbleveinwidth.png](images/marbleveinwidth.png)
{% include_relative snippets/snippet-materialblend.md %}![images/marbleblending.png](images/marbleblending.png)
{% include_relative snippets/snippet-materialturbulence.md %}![images/marbleturbulence.png](images/marbleturbulence.png)
{% include_relative snippets/snippet-materialveneer.md %}![images/marbleveneer.png](images/marbleveneer.png)
베니어 (왼쪽), 일반 (오른쪽).

## Tile
{: #tile}
Tile is a 2-D material. Texture [mapping](properties-object.html#mapping) for the objects controls the orientation of the material on the object. The Tile material combines a Base component and a Joint component. Each of these materials can also include any other material.
![images/tile materials.png](images/tile materials.png)
특수 효과를 주려면 타일 크기를 각 방향마다 다르게 설정합니다. 예를 들어, 한쪽에는 극도로 긴 타일 재질을 사용하여 사이딩 재질로 만듭니다.

#### Tile
전체 타일 크기를 설정합니다. 너비와 높이는 독립적으로 설정할 수 있습니다.
![images/tilescale.png](images/tilescale.png)

#### Width/Height
타일의 너비와 높이를 지정합니다.
{% include_relative snippets/snippet-lock-widthheight.md %}

#### Joint
이음 재질의 크기를 지정합니다.
![images/tilejointsize.png](images/tilejointsize.png)

#### Horizontal joint/Vertical joint
이음 재질의 너비와 높이를 지정합니다.

#### 잠금
Maintains the ratio between the Horizontal and Vertical joint sizes.

#### Offset
Provides a relative horizontal offset per vertical tile. For example, use a setting of .5 to produce a standard running bond. This allows modeling of material such as marble tile, without the effect of having the entire floor hewn from the same block of marble.
![images/tileoffset.png](images/tileoffset.png)

#### Vary Tiles
각각의 타일에 임의의 색상을 가진 재질 색을 더합니다. 불규칙한 벽돌과 같은 재질을 모델링할 수 있습니다.

#### R/G/B
Modifies the red, green, and blue color components.  This will slightly vary the base material of each tile randomly.
![images/tilevarycolor.png](images/tilevarycolor.png)

#### X/Y/Z
Offsets the material from the world origin for each tile randomly. Do this if a seam that marks the beginning of the material appears an in inappropriate place.
![images/tilevaryxyz.png](images/tilevaryxyz.png)

## Wood
{: #wood}
Wood consists of concentric cylinders of alternating Base and Ring components. The Wood settings define how the Base and Ring components combine.

Use this method to create wood materials if objects are not closely viewed. If detailed wood is needed, use a [Texture material](material-type-simple.html#textured) to do wood.  If the viewpoint is not close to the wood, a solid color can be used to take the place of wood without sacrificing image quality. This allows faster rendering. An additional advantage of using a wood material is that when rendering different sides of an object, the wood grain will look correct. End grain will show on the ends and parallel grain will show on the sides of an object.
![images/woodmaterials.png](images/woodmaterials.png)

#### Base/Ring
The Base and Ring components are two materials. Their properties are specified in the same way as any material.
{% include_relative snippets/snippet-materialscaleandlock.md %}![images/woodscale.png](images/woodscale.png)

#### Ring Width
A fraction of the distance between one Base stripe and the next. Values range from 0 (zero) for no Ring component to 1 for no Base component.
![images/woodringwidth.png](images/woodringwidth.png)
{% include_relative snippets/snippet-materialblend.md %}![images/woodblend.png](images/woodblend.png)
{% include_relative snippets/snippet-materialturbulence.md %}![images/woodturbulence.png](images/woodturbulence.png)
{% include_relative snippets/snippet-materialveneer.md %}![images/woodveneer.png](images/woodveneer.png)
베니어 (왼쪽), 일반 (오른쪽).

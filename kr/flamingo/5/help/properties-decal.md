---
---


# Decals
데칼은 재질을 간접적으로 사용하지 않고, 개체에 직접 적용하는 비(非) 타일 방식의 이미지 맵입니다. 개체 색, 반사도 또는 범프에서 제한된 부분을 수정할 때 데칼을 사용합니다.
Decals consist of a single instance of the image, rather than being tiled as they are when used in a [material definition](materials-tab.html).
데칼의 용도:

>Hanging artwork on interior walls.
>Placing labels or logos on products.
>Adding signs to the model.
>Creating stained glass windows.

![images/freshmilk.png](images/freshmilk.png)
 **Note:** Decal previews will only display in wireframe views if OpenGL is enabled for wireframe mode.&#160;The **Pipeline** setting must be **OpenGL** in **Options** &#160;&gt; **Appearance** &#160;&gt; **Advanced Settings** &#160;&gt; **Wireframe** &#160;&gt; **Other Settings** &#160;&gt; **Pipeline and Conduits**.

## Decal Placement
{: #decal-list}
{: #decal-placement}

###  **추가** 
{: #add-decal}
1. Select one or more objects.
1. On the **Edit** menu, click **Object Properties**.
1. On the **Properties** list, click **Flamingo nXt Decals**.
1. Click the **Add** button.
1. In the **Open Bitmap** dialog box, select a bitmap name, and click **Open**.
{% include_relative snippets/snippet-clearbitmapcache.md %}1. In the **Decal Properties** dialog box, select options, and click **Place**.
1. At the prompts for points, pick points on the model to locate the decal.
The precise sequence depends on the type of decal selected: [Planar](#decal-planarmapping), [Cylindrical](#decal-cylindricalmapping), or [UVMap](#decal-uvmapping).

###  **Edit Placement** 
{: #decal-edit-placement}
1. Click the **Edit Placement** button.
1. At the **Select control point** prompt, use the graphical editor to change the placement of the decal.
1. Press **Enter** when finished.

###  **속성** 
{: #decal-properties}
1. Click the **Properties** button.
1. In the **Decal Properties** dialog box, use the controls to change the decal's properties.

###  **Delete** 
{: #decal-delete}

>Click the **Delete** button.

###  **Move up** / **Move down** 
{: #decal-movedown}
{: #decal-moveup}
하나의 개체에 여러 개의 데칼이 겹쳐지는 경우, 적용되는 순서가 매우 중요합니다. 데칼은 목록에 표시되는 순서대로 적용됩니다. 목록의 마지막 데칼이 제일 위(표면)에 표시됩니다.

>Click **Move Up** or **Move Down** to change a decal's position in the list.

##### To place a planar decal
1. At the prompts, pick locations for the decal's **Width**, and **Height direction**.
1. At the **Select control point...** prompt, select a control point to adjust the image size, rotation, or location.
Or press **Enter** to complete the decal placement.

### Options

#### Move
데칼을 움직입니다. "이동의 기준점 새 위치" 프롬프트에서 Rhino Move 명령에서와 마찬가지로 원하는 위치를 입력합니다.

#### UseImageAspectRatio
스트레치된 데칼을 원래 비트맵의 종횡비에 맞춰 원래대로 되돌립니다.

##### To place a cylindrical decal
1. At the prompt, pick a location for the **Center point** of the cylinder.
1. At the **Select control point...** prompt, select a control point to adjust the image size, rotation, or location.
Or press **Enter** to complete the decal placement.

## Set or edit the decal placement using the control widget
안내: 평면형 매핑을 곡면에 사용할 때 전체 비트맵은 개체 서피스의 뒤에 있어야 합니다. 비트맵 일부가 개체 앞에 있다면 그 부분은 보이지 않습니다.

#### To resize the decal width and height at the same time

>Drag the control points at the corners of the control widget.

#### To change the decal height

>Drag the center control point on the top and bottom edges of the control widget.

#### To change the decal width

>Drag the center control point on the left and right edges of the control widget.

#### To move the decal

>Drag the control point in the center of the control widget.

#### To rotate the decal

>Drag the x-, y-, or z-axis control point on the widget axis icon.

## Decal Properties
{: #dialogbox-editdecal}
비트맵의 정보는 개체의 색을 데칼의 색으로 바꾸거나, 두 가지를 블렌드합니다. 이것이 데칼의 가장 일반적인 사용법입니다.

## Projection
{: #projection}
매핑 스타일은 데칼이 개체에 투영되는 방식을 결정합니다. 장면에 보조선을 그려 정확하게 데칼을 배치하는 것이 좋습니다. 서피스 바로 뒤에 그린 직사각형은 표준 데칼을 위한 가이드로 도움이 됩니다. 개체 스냅을 사용하여 정확하게 데칼을 배치합니다.

### Cylindrical
{: #decal-cylindricalmapping}

### &#160;
원통형 매핑 유형은 와인 병의 레이블처럼 한 방향으로 곡면이 있는 개체에 데칼을 배치할 때 유용합니다.
원통형 투영은 비트맵의 세로축을 원통형의 축에 맞추고 가로축은 원통을 둘러싸이게 하여 비트맵을 원통에 매핑합니다.
![images/cylindricaldecal-002.png](images/cylindricaldecal-002.png)
### Planar
{: #decal-planarmapping}

### &#160;
평면형 매핑은 가장 일반적인 매핑 스타일입니다. 평평하거나 약간 곡면이 있는 개체에 매핑할 때 적합합니다.
모서리는 비트맵의 위치와 범위를 정의합니다. 직사각형의 비율이 비트맵과 동일하지 않다면 비트맵이 스트레치되거나 압축되어 직사각형에 맞춰집니다.
평면형 매핑을 곡면에 사용할 때 전체 비트맵 투영은 개체 서피스의 뒤에 있어야 합니다. 비트맵 일부가 개체 앞에 있다면 그 부분은 보이지 않습니다.
![images/decal-planar-001.png](images/decal-planar-001.png)
### UV 맵
{: #decal-uvmapping}

### &#160;
머리카락이나 나무껍질처럼 서피스에 맞춰 데칼이 흐르고 늘어나야 하는 개체에 UV 매핑을 사용하는 데칼이 유용합니다.
데칼이 개체 전체를 커버합니다. 데칼의 배치를 제어할 수 없습니다.
UV 매핑은 이미지를 구부리고 늘리기 위해 서피스의 U 방향과 V 방향을 매개변수화하여 사용하므로, 사용자가 직접 배치할 필요가 없습니다.
![images/uvmapdecal-00.png](images/uvmapdecal-00.png)
### Browse
{: #file-browse}
이미피 파일을 바꿉니다.
{% include_relative snippets/snippet-clearbitmapcache.md %}
## Strength
{: #decalmappingstrength}

### Color
{: #decal-color}
Varies the relative strength of the image color with respect to the underlying material. See also, [Material Texture Properties, Color Strength](texture-properties-main.html#color).

### Bump
{: #decalmappingbump}
Bump maps create simulated shadows and highlights on the surface. See also, [Material Texture Properties, Bump Strength](texture-properties-main.html#bump).

## Reflective finish
{: #reflective-finish-and-highlight}
재질 정의에서 제어되는 것과 동일한 속성을 제어합니다. 이 속성을 데칼의 영향을 받는 개체의 특정한 영역에 적용합니다. 기본적으로 데칼은 무광 마무리로 처리됩니다.

### 강도
Adjusts the strength of the highlight. Larger values increase the size and strength of the highlight. See [Advanced Material Properties, Intensity](advanced-material-properties-main.html#intensity).

### Sharpness
Sets the size of the highlight. Lower numbers specify a broader highlight; higher numbers focus the highlight in a smaller area. See [Advanced Material Properties, Sharpness](advanced-material-properties-main.html#sharpness).

### Metallic
Sets the highlight color to match the base color. See [Advanced Material Properties: Metallic](advanced-material-properties-main.html#metallic).
{% include_relative snippets/snippet-linking.md %}
{% include_relative snippets/snippet-masking.md %}
## Advanced
{: #advanced}

### Double Sided
{: #double}
데칼이 서피스의 앞면과 뒷면에 모두 나타나게 합니다.

### Mirror
{: #mirror}
데칼 이미지를 반전시켜 미러(거울) 실행합니다.

## Projection direction
{: #projection-direction}

### Backward
데칼 이미지의 뒤로부터 멀리 데칼을 투영합니다.
![images/projectionbackward1.png](images/projectionbackward1.png)Front (left), back (right).

### Forward
데칼 이미지의 앞으로부터 멀리 데칼을 투영합니다.
![images/projectionforward1.png](images/projectionforward1.png)Front (left), back (right).

### Forward &amp; Backward
데칼을 데칼 이미지의 앞과 뒤로 모두 투영시킵니다.
![images/projectionforwardandback.png](images/projectionforwardandback.png)Front (left), back (right).

### Transparency
Sets the transparency for the decal. See [Transparency](advanced-material-properties-transparency.html).
IOR
Sets the index of refraction for the transparent decal. See [Index of Refraction](advanced-material-properties-transparency.html#index-of-refraction) 

---
title: 印花
---
<--TODO: This page should be updated. There are at least, 3 points to improve, more likely some more: 1. Compare instructions to add decal with actual process in the program. 2. There is another decal type, "spherical", that's not mentioned in the text. 3. Clicking on "Properties" doesn't open a dialog but returns an error message. -->

# {{page.title}}
印花是直接在物件上贴图的方法，这种贴图方法不需要依靠材质，可以在物件的局部贴图。使用印花可以修改物件局部的颜色、反射或凹凸。
一个印花只能使用一张图片，而且该图片不像[材质](materials-tab.html)里的图片可以重复拼贴。
印花的使用方法：

>墙上的图案。
>物件上的标签或商标。
>模型上的标志。
>彩绘玻璃。

![images/freshmilk.png](images/freshmilk.png)
 **附注:** 只有在启用 OpenGL 且显示模式为线框模式时才能预览印花。  **选项**  &gt; **视图**  &gt; **显示模式**  &gt; **线框模式**  &gt; **其他设置**  &gt; **使用显示管线**中的**显示管线** 必须设置为 **OpenGL**。

## 放置印花
{: #decal-list}
{: #decal-placement}

### **加入**
{: #add-decal}
1. 选取一个或以上的物件。
1. 从**编辑**菜单选择**物件属性**。
1. 在**属性**对话框切换到 **Flamingo nXt 印花**页面。
1. 按**新增**按钮。
1. 在**打开位图**对话框中，选择一张位图，并点击**打开**。
{% include_relative snippets/snippet-clearbitmapcache.md %}1. 在**印花属性**对话框设置选项，点击**放置**。
1. 依照指令提示在模型里指定数个点决定印花的位置。
不同投影方式 ([平面](#decal-planarmapping)、[圆柱体](#decal-cylindricalmapping)、[UV](#decal-uvmapping)) 的印花放置的方式各不相同。

### **编辑位置**
{: #decal-edit-placement}
1. 按**编辑位置**按钮。
1. 在**选取控制点**提示下， 移动印花贴图轴上的控制点可以改变印花的位置。
1. 按 **Enter** 完成。

### **属性**
{: #decal-properties}
1. 按**属性**按钮。
1. **印花属性**对话框有許多印花的设置可以修改。

### **删除**
{: #decal-delete}

>点击**删除**按钮。

### **上移** / **下移**
{: #decal-movedown}
{: #decal-moveup}
当一个物件上有数个印花重叠时，会需要设置印花显示的前后顺序，清单里最上面的印花在物件上会显示在最前面。

>按**上移**或**下移**按钮可以将选取的印花在清单中上、下移动。

##### 放置平面印花
1. 依照提示指定印花的位置、**宽度**与**高度**方向。
1. 在**选取控制点...** 提示下，移动控制点调整印花贴图的位置、大小与旋转角度。
或按 **Enter** 放置印花。

### 选项

#### 移动
移动印花的位置，就像 Rhino 的 Move 指令一样指定移动的起点与移动的终点。

#### 使用图片的宽高比
使用图片的宽高比例设置印花，避免贴图变形。

##### 放置圆柱印花
1. 依照提示指定圆柱的**中心点**位置。
1. 在**选取控制点...** 提示下，移动控制点调整印花贴图的位置、大小与旋转角度。
或按 **Enter** 放置印花。

## 设置或编辑印花的位置
附注：在有弧度的曲面上使用平面印花贴图时，必需将整个贴图轴置于曲面后方，因为贴图轴突出于曲面前方的部分无法将贴图投影至曲面上。

#### 同时调整印花的宽度与高度

>移动印花贴图轴的角控制点。

#### 调整印花的高度

>移动印花贴图轴上、下边的控制点。

#### 调整印花的宽度

>移动印花贴图轴左、右边的控制点。

#### 移动印花

>移动印花贴图轴中心的控制点。

#### 旋转印花

>移动印花贴图轴 X、Y、Z 三个轴向箭头尖端的控制点。

## 印花属性
{: #dialogbox-editdecal}
以印花贴图取代物件上某一部分材质的颜色是印花常用的方法。

## 投影方式
{: #projection}
决定如何将印花贴图投影至物件上，在放置印花贴图轴时可以事先创建一些建构线辅助，再配合物件锁点精确放置印花贴图。

### 圆柱体
{: #decal-cylindricalmapping}
圆柱体印花贴图轴适用于在瓶罐类似的物件上贴上标签。
圆柱体印花贴图轴的一个方向是直的，另一个方向环绕物件。
![images/cylindricaldecal-002.png](images/cylindricaldecal-002.png)

### 平面
{: #decal-planarmapping}
平面印花贴图轴是最常用的方式，适用于在平面或是弧度不大的曲面上贴上图案。
平面印花贴图轴的宽度与高度可以任意改变，但它的宽度与高度的比例与使用的图片不一致时，图片会延展或挤压变形。
在有弧度的曲面上使用平面印花贴图时，必需将整个贴图轴置于曲面后方，因为贴图轴突出于曲面前方的部分无法将贴图投影至曲面上。
![images/decal-planar-001.png](images/decal-planar-001.png)

### UV
{: #decal-uvmapping}
UV 印花贴图轴适用于类似头发或树干这种沿曲面延伸的贴图。
它会将贴图布满整个曲面，无法控制贴图位置。
UV 印花贴图是以曲面 U、V 两个方向的参数坐标做贴图的对应，这种方式的贴图可能会有在曲面上的一部分挤压变形，但在另一部分的延展变形不平均的情形。
![images/uvmapdecal-00.png](images/uvmapdecal-00.png)

### 浏览
{: #file-browse}
变更图片文件。

{% include_relative snippets/snippet-clearbitmapcache.md %}

## 强度
{: #decalmappingstrength}

### 颜色
{: #decal-color}
调整印花贴图的透明度，可以让物件材质的颜色透出印花。请参考[材质贴图属性 > 颜色强度](texture-properties-main.html#color)。

### 凹凸
{: #decalmappingbump}
以印花贴图像素的灰阶值在物件上产生视觉上的凹凸效果。请参考：[材质贴图属性 > 凹凸强度](texture-properties-main.html#bump)。

## 反射度
{: #reflective-finish-and-highlight}
控制印花贴图的反射度，可以用来让印花与物件本身的材质有所区别，例如塑料瓶上的铝箔标签，默认值是完全没有反射。

### 强度
调整反光的强度，加大这个数值会加大反光的大小与亮度。请参考：[高级材质属性 > 强度](advanced-material-properties-main.html#intensity)。

### 锐利度
设置物件表面的反光大小，数字越小，反光越大、越模糊。数值越大，反光越小、越锐利。請參考：[高级材质属性 > 锐利度](advanced-material-properties-main.html#sharpness)。

### 金属
将材质的反光颜色设置为与材质颜色相同。请参考：[高级材质属性 > 金属](advanced-material-properties-main.html#metallic)。
{% include_relative snippets/snippet-linking.md %}
{% include_relative snippets/snippet-masking.md %}
## 高级
{: #advanced}

### 双面
{: #double}
让印花贴图同时出现在曲面的正面与背面。

### 镜像
{: #mirror}
镜像印花贴图。

## 投影方向
{: #projection-direction}

### 向后
从印花贴图轴的背面投影至物件上。
![images/projectionbackward1.png](images/projectionbackward1.png)前 (左)、后 (右)。

### 向前
从印花贴图轴的正面投影至物件上。
![images/projectionforward1.png](images/projectionforward1.png)前 (左)、后 (右)。

### 双向
从印花贴图轴的正面与背面投影至物件上。
![images/projectionforwardandback.png](images/projectionforwardandback.png)前 (左)、后 (右)。

### 透明度
设置印花贴图的透明度。请参考：[透明度](advanced-material-properties-transparency.html)。
折射率
设置透明的印花贴图的折射率。请参考：[折射率](advanced-material-properties-transparency.html#index-of-refraction)。

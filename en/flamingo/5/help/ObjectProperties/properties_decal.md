---
layout: toc-page
---


# Decals
{: toc-title }

Decals are non-tiling image maps that apply directly to objects instead of indirectly using a material. Use decals to modify a limited part of an object's color, reflectivity, or bumps.

Decals consist of a single instance of the image, rather than being tiled as they are when used in a [material definition](../Materials/Materials_Tab.html).

Some uses for decals include:

 * Hanging artwork on interior walls.
 * Placing labels or logos on products.
 * Adding signs to the model.
 * Creating stained glass windows.
<img src="FreshMilk.png"/>

 **Note:** Decal previews will only display in wireframe views if OpenGL is enabled for wireframe mode.&#160;The **Pipeline** setting must be **OpenGL** in **Options** &#160;&gt; **Appearance** &#160;&gt; **Advanced Settings** &#160;&gt; **Wireframe** &#160;&gt; **Other Settings** &#160;&gt; **Pipeline and Conduits**.


## Decal Placement
{: .toc-header }


###  <kbd>Add</kbd> 
{: .toc-header }

1.

Select one or more objects.

2.

On the **Edit** menu, click **Object Properties**.

3.

On the **Properties** list, click **Flamingo nXt Decals**.

4.

Click the **Add** button.

5.

In the **Open Bitmap** dialog box, select a bitmap name, and click **Open**.

6.

In the **Decal Properties** dialog box, select options, and click **Place**.

7.

At the prompts for points, pick points on the model to locate the decal.

The precise sequence depends on the type of decal selected: [Planar](#Decal_PlanarMapping), [Cylindrical](#Decal_CylindricalMapping), or [UVMap](#Decal_UVMapping).


###  <kbd>Edit Placement</kbd> 
{: .toc-header }

1.

Click the **Edit Placement** button.

2.

At the **Select control point** prompt, use the graphical editor to change the placement of the decal.

3.

Press **Enter** when finished.


###  <kbd>Properties</kbd> 
{: .toc-header }

1.

Click the **Properties** button.

2.

In the **Decal Properties** dialog box, use the controls to change the decal's properties.


###  <kbd>Delete</kbd> 
{: .toc-header }

 * Click the **Delete** button.

###  <kbd>Move up</kbd> / <kbd>Move down</kbd> 
{: .toc-header }

When multiple overlapping decals are applied on a single object, the order in which they are applied may be significant. Decals are applied in the order they appear in the list. The last decal in the list appears to be on top.

 * Click **Move Up** or **Move Down** to change a decal's position in the list.

#### To place a planar decal

1.

At the prompts, pick locations for the decal's **Width**, and **Height direction**.

2.

At the **Select control point...** prompt, select a control point to adjust the image size, rotation, or location.

Or press **Enter** to complete the decal placement.


### Options


#### Move

Moves the decal. At the Point to move from and the Point to move to prompts, enter any locations as for the Rhino Move command.


#### UseImageAspectRatio

Restores a stretched decal to the aspect ratio of the original bitmap.


#### To place a cylindrical decal

1.

At the prompt, pick a location for the **Center point** of the cylinder.

2.

At the **Select control point...** prompt, select a control point to adjust the image size, rotation, or location.

Or press **Enter** to complete the decal placement.


## Set or edit the decal placement using the control widget
{: .toc-header }

Note: When using the planar mapping on a curved object, the entire bitmap must lie behind the surface of the object. Portions of the bitmap that lie in front of the surface will not be visible.


#### To resize the decal width and height at the same time

 * Drag the control points at the corners of the control widget.

#### To change the decal height

 * Drag the center control point on the top and bottom edges of the control widget.

#### To change the decal width

 * Drag the center control point on the left and right edges of the control widget.

#### To move the decal

 * Drag the control point in the center of the control widget.

#### To rotate the decal

 * Drag the x-, y-, or z-axis control point on the widget axis icon.

## Decal Properties
{: .toc-header }

The information from the bitmap replaces or blends the object's color with the decal's color. This is the most common use of decals.


## Projection
{: .toc-header }

The mapping style determines how to project the decal onto the object. It is a good idea to draw construction lines in the scene to help accurately place decals. A rectangle drawn just behind a surface can act as a guide for a standard decal. Use object snaps for accurate placement.


### Cylindrical
{: .toc-header }


### &#160;
{: .toc-header }

The cylindrical mapping type is useful for placing decals onto objects that curve in one direction, such as labels on wine bottles.

The cylindrical projection maps the bitmap onto the cylinder with the bitmap's vertical axis along the cylinder's axis, and the horizontal axis around the cylinder.

<img src="CylindricalDecal-002.png"/>
### Planar
{: .toc-header }


### &#160;
{: .toc-header }

Planar mapping is the most common mapping style. It is appropriate when mapping to flat or gently curved objects.

The corners define the bitmap's location and extents. If the rectangle does not have the same proportions as the bitmap, the bitmap will be stretched or compressed to fit.

When using planar mapping on a curved object, the entire bitmap projection must lie behind the surface of the object. Portions of the bitmap that lie in front of the surface will not be visible.

<img src="Decal-Planar-001.png"/>
### UV Map
{: .toc-header }


### &#160;
{: .toc-header }

Decals using UV mapping are useful for objects like hair and tree bark where the decal flows and stretches to fit the surface.

The decal covers the entire object; there is no control over the decal placement.

UV mapping uses the u- and v-parameterization of the surface to bend and stretch the image; therefore, no manual placement is necessary.

<img src="UVMapDecal-00.png"/>
### <img src="browsebutton.png"/>Browse
{: .toc-header }

Change the image file.


## Strength
{: .toc-header }


### Color
{: .toc-header }

Varies the relative strength of the image color with respect to the underlying material. See also, [Material Texture Properties, Color Strength](../Materials/Texture_Properties_Main.html#Color).


### Bump
{: .toc-header }

Bump maps create simulated shadows and highlights on the surface. See also, [Material Texture Properties, Bump Strength](../Materials/Texture_Properties_Main.html#Bump).


## Reflective finish
{: .toc-header }

Controls the same properties that are controlled by a material definition. Apply these properties to the specific areas of the object that are affected by the decal. By default, decals have a matte finish.


### Intensity
{: .toc-header }

Adjusts the strength of the highlight. Larger values increase the size and strength of the highlight. See [Advanced Material Properties, Intensity](../Materials/Advanced_Material_Properties_Main.html#Intensity).


### Sharpness
{: .toc-header }

Sets the size of the highlight. Lower numbers specify a broader highlight; higher numbers focus the highlight in a smaller area. See [Advanced Material Properties, Sharpness](../Materials/Advanced_Material_Properties_Main.html#Sharpness).


### Metallic
{: .toc-header }

Sets the highlight color to match the base color. See [Advanced Material Properties: Metallic](../Materials/Advanced_Material_Properties_Main.html#Metallic).




## Advanced
{: .toc-header }


### Double Sided
{: .toc-header }

Causes the decal to appear on the back face of the surface on which it is placed as well as the front face.


### Mirror
{: .toc-header }

Mirrors the decal image.


## Projection direction
{: .toc-header }


### Backward
{: .toc-header }

Projects the decal away from the back of the decal image.

<img src="../image/ProjectionBackward1.png"/>Front (left), back (right).


### Forward
{: .toc-header }

Projects the decal away from the front of the decal image.

<img src="../image/ProjectionForward1.png"/>Front (left), back (right).


### Forward &amp; Backward
{: .toc-header }

Projects the decal away from both the front and the back of the decal image.

<img src="../image/ProjectionForwardandBack.png"/>Front (left), back (right).


### Transparency
{: .toc-header }

Sets the transparency for the decal. See [Transparency](../Materials/Advanced_Material_Properties_Transparency.html).

IOR

Sets the index of refraction for the transparent decal. See [Index of Refraction](../Materials/Advanced_Material_Properties_Transparency.html#Index_Of_Refraction) 


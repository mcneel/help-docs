---
layout: toc-page
---


# Simple Material Properties
 

The Simple Material Properties dialog box give easy access to the properties you will usually want to change to make a material look different without changing the material style from, say Solid Color to Glass. For most materials, changing the color is all that is necessary to get a different look. You can change the advanced properties. These are pre-set by the material template to help you quickly achieve the appearance you want.

All materials share three basic properties: name, color, and preview.


### Name
 

The material name.


### Color
 

Controls the local color for the material. All materials have a base color. [More about color...](general\select-color.html) 


#### Color swatch selector

Click the color swatch to select colors from the [Select Color](general\select-color.html) dialog box.


### Preview
 

The preview image shows the material as it will appear on objects in the model. The style and size of the preview are part of the material definition.

 **Note** : Set the default size for the preview object in [Options: Flamingo nXt](general\options-flamingo.html).

<img src="materials/previewer.png"/>

 * Right-click the material preview pane to specify options that control the preview's appearance:

#### Sphere

Sets the preview object to a sphere.


#### Box

Sets the preview object to a box with a width equaling the sphere radius.


#### Plane

Sets the preview object to a plane with a width equaling the sphere radius.


#### Sphere radius

Sets the preview sphere radius and box and plane width. Set the size to approximate the size of the objects to which the material will be assigned to help visualize the material.


## Solid Color
 

Solid Color materials have only a [name](advanced-material-properties-main.html#name) and a [color](advanced-material-properties-main.html#color).


### 
 

Properties available from the **Simple Material Properties** dialog box:

 *  [Name](advanced-material-properties-main.html#name) 
 *  [Color](advanced-material-properties-main.html#color) 
All other properties are set to a default (usually off or zero).


###  <kbd>Advanced</kbd> 
 

Opens the [Advanced Material Properties](advanced-material-properties-main.html) dialog box.


## Metal
 

Metal materials have a highlight whose color matches the [color](advanced-material-properties-main.html#color). You can control the [Sharpness](advanced-material-properties-main.html#sharpness) of this highlight from the **Simple Material Properties** control.


### 
 

Properties available from the **Simple Material Properties** dialog box:

 *  [Name](advanced-material-properties-main.html#name) 
 *  [Color](advanced-material-properties-main.html#color) 
 *  [Sharpness](advanced-material-properties-main.html#sharpness) 
Properties pre-set by the template:

 *  [Highlight color](advanced-material-properties-main.html#highlight-color) : The Highlight color matches the base color.
 *  [Intensity](advanced-material-properties-main.html#intensity) 
 *  [Fresnel](advanced-material-properties-main.html#fresnel) 
 *  [Type](advanced-material-properties-main.html#type) 

###  <kbd>Advanced</kbd> 
 

Opens the [Advanced Material Properties](advanced-material-properties-main.html) dialog box.


## Glass
 

Glass materials have an [Index of Refraction](advanced-material-properties-transparency.html#index-of-refraction) (IOR) that you can adjust.


### 
 

Properties available from the **Simple Material Properties** dialog box:

 *  [Name](advanced-material-properties-main.html#name) 
 *  [Color](advanced-material-properties-main.html#color) 
 *  [Index of Refraction](advanced-material-properties-transparency.html#index-of-refraction) 
Properties pre-set by the template:

 *  [Highlight color](advanced-material-properties-main.html#highlight-color) 
 *  [Intensity](advanced-material-properties-main.html#intensity) 
 *  [Fresnel](advanced-material-properties-main.html#fresnel) 
 *  [Sharpness](advanced-material-properties-main.html#sharpness) 
 *  [Transparency](advanced-material-properties-transparency.html) 

###  <kbd>Advanced</kbd> 
 

Opens the [Advanced Material Properties](advanced-material-properties-main.html) dialog box.


## Plastic
 

Plastic materials have a white [highlight](advanced-material-properties-main.html#highlight-color) set by the template.


### 
 

Properties available from the **Simple Material Properties** dialog box:

 *  [Name](advanced-material-properties-main.html#name) 
 *  [Color](advanced-material-properties-main.html#color) 
Properties pre-set by the template:

 *  [Highlight color](advanced-material-properties-main.html#highlight-color) 
 *  [Intensity](advanced-material-properties-main.html#intensity) 
 *  [Fresnel](advanced-material-properties-main.html#fresnel) 
 *  [Sharpness](advanced-material-properties-main.html#sharpness) 

###  <kbd>Advanced</kbd> 
 

Opens the [Advanced Material Properties](advanced-material-properties-main.html) dialog box.


## ClearFinish
 

The ClearFinish material simulates car paint, porcelain, ceramics, varnished woods, or any material with a plastic or clear-coat layer. ClearFinish uses the [Fresnel](advanced-material-properties-main.html#fresnel) setting to change the material color based on angle to the view. These materials tend to be a deep color when looked at straight on, but as the surface curves away from the view, they become more and more reflective. Car paints with a clear-coat or clear lacquer finishes are good examples.


### 
 

Properties available from the **Simple Material Properties** dialog box:

 *  [Name](advanced-material-properties-main.html#name) 
 *  [Color](advanced-material-properties-main.html#color) 
Properties pre-set by the template:

 *  [Highlight color](advanced-material-properties-main.html#highlight-color) 
 *  [Intensity](advanced-material-properties-main.html#intensity) 
 *  [Fresnel](advanced-material-properties-main.html#fresnel) 
 *  [Sharpness](advanced-material-properties-main.html#sharpness) 

###  <kbd>Advanced</kbd> 
 

Opens the [Advanced Material Properties](advanced-material-properties-main.html) dialog box.


## Glossy
 

Glossy materials have a highlight with low Highlight [Intensity](advanced-material-properties-main.html#intensity) and [Sharpness](advanced-material-properties-main.html#sharpness) settings that you can control from **Simple Material Properties**.


### 
 

Properties available from the **Simple Material Properties** dialog box:

 *  [Name](advanced-material-properties-main.html#name) 
 *  [Color](advanced-material-properties-main.html#color) 
 *  [Intensity](advanced-material-properties-main.html#intensity) 
 *  [Highlight sharpness](advanced-material-properties-main.html#sharpness) 
Properties pre-set by the template:

 *  [Fresnel](advanced-material-properties-main.html#fresnel) 
 *  [Type](advanced-material-properties-main.html#type) 

###  <kbd>Advanced</kbd> 
 

Opens the [Advanced Material Properties](advanced-material-properties-main.html) dialog box.


## Textured
 

Textured materials use images to create colored and patterned materials. The image name, resolution, tile size, and highlight intensity and sharpness are controlled from the **Simple Materials Properties** dialog box.


### 
 

Properties available from the **Simple Material Properties** dialog box:

 *  [Name](advanced-material-properties-main.html#name) 
 *  [Color](advanced-material-properties-main.html#color) 
 *  [Tiles](texture-properties-main.html#tiles) : [Width/Height](texture-properties-main.html#width-height) and [Mirror tiles](texture-properties-main.html#mirror-tiles) 
 *  [Linked status](texture-properties-main.html#linking) 
 *  [Intensity](advanced-material-properties-main.html#intensity) 
 *  [Sharpness](advanced-material-properties-main.html#sharpness) 

###  <kbd>Advanced</kbd> 
 

Opens the [Advanced Material Properties](advanced-material-properties-main.html) dialog box.


## Texture Set
 

 [Texture set materials](texture-set-materials.html) support&#160;third-party texture maps that contain information such as displacement, normal, or bump maps. Displacement maps cause the material to have depth. The image names, tile size, and map properties are controlled from the **Simple Materials Properties** dialog box.


### 
 

Properties available from the **Simple Material Properties** dialog:

 *  [Name](advanced-material-properties-main.html#name) 
 *  [Color](advanced-material-properties-main.html#color) 
 *  [Tiles](texture-properties-main.html#tiles) : [Width/Height](texture-properties-main.html#width-height) 
 *  [Map Properties](texture-properties-main.html) 

###  <kbd>Advanced</kbd> 
 

Opens the [Advanced Material Properties](advanced-material-properties-main.html) dialog box.

&#160;


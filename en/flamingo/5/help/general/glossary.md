---
layout: toc-page
---


# Glossary
 


## Masking
 

Obscures portions of the image based on either a color value or an alpha channel stored in the image.

In this example, an image with an alpha-channel background is placed as a decal on a rectangular surface. Masking for materials works the same.

The material assigned to a planar surface in this example has a red base color.


 *<img src="objectproperties/airplane.png"/>Original decal image. The gray checkered area represents the image alpha channel.* 

 *<img src="materials/masking-004.png"/>Final rendered image.* 

### None
 

With no masking, the decal image obscures the underlying material. The rectangular planar surface casts a rectangular shadow on the ground plane. Masking allows the material to show through the image where the alpha channel or color masking takes place, but the shadow on the ground plane is rectangular, and the background behind the surface is blocked by the surface.


 *<img src="materials/masking-002.png"/>Without masking (left) the image covers the surface, with masking (right), the red material shows through.* 

### Alpha Channel
 

Uses the image's [alpha channel](environment/environment-tab.html#alpha) to define the masked area if one exists.

The alpha channel is a portion of each pixel's data that is reserved for transparency information. Alpha channels create and store masks that let you isolate and protect parts of an image while you apply color changes, filters, or other effects to the rest of the image.&#160;

Each pixel in an image is described as channels of data that define the mixture of the red, green, and blue (RGB) colors. The alpha channel is an 8-bit (256-level) grayscale representation of the image that masks the color of the underlying pixel. The value of the alpha mask determines the intensity of the pixel color.

If a mask is fully transparent, a red pixel would have full intensity (be fully visible bright red) and if the mask is completely opaque, this red pixel will appear completely transparent.


### Color
 

All image pixels within the sensitivity&#160;range of the selected color will be masked.

Specify a color that will be masked and let the background show through.


#### Color Dropper

Click to select the color from the bitmap.


#### Color swatch

Click to select a color from the
### Popup('General/select_color.htm');" ehlpsource="robohelp classic" class="hcp1" id="a168" style="position: relative;">Select Color
 

dialog box.


### Sensitivity *(Color only)* 
 

The value indicates the size of the area around the color that is also masked. Must be greater than 0.0 for color masking to occur.


### Blur *(Color only)* 
 

Partially masks pixels. The value determines the magnitude of partial masking around the masked color


### Reverse
 

Inverts the mask—pixels that would have been masked are now included, and vice versa.

<img src="materials/masking-007.png"/>


### Transparent
 

Makes the masked area of the underlying object transparent so other objects or the background behind the object can be seen through the object. Normally, the material of the object shows through in that area.

Transparent masking allows a more natural shadow and allows the background objects to show. The underlying material could simply be transparent, but sometimes it is useful to make the surface behind the decal transparent while keeping other areas of the surface opaque.

<img src="materials/masking-003.png"/>

&#160;


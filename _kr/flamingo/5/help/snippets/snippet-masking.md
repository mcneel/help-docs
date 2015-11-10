
### Masking
Obscures portions of the image based on either a color value or an alpha channel stored in the image. This allows textures to have complex shaped boundaries and create complex effects such as holes in a surface.

다음 예에서는 알파 채널 배경을 가진 이미지가 직사각형 서피스에 데칼로 배치되었습니다. 재질을 마스크 처리할 때도 동일합니다.

![images/airplane.png](images/airplane.png)  ![images/masking-004.png](images/masking-004.png)
*Original decal image. The gray checkered area represents the image alpha channel.*

Masking information can come from three sources in the bitmap:

> [None](#nomask)
> [Alpha Channel](#alphamask)
> [Color](#colormask)

#### None
{: #nomask}
With no masking, the image obscures the underlying material. Masking allows the material to show through the image where the alpha channel or masking color exists. The material assigned to a planar surface in this example has a red base color.

![images/masking-002.png](images/masking-002.png)
*Without masking (left) the image covers the surface, with masking (right), the red material shows through.*

#### Alpha Channel
{: #alphamask}
Uses the image's [alpha channel](environment-tab.html#alpha) to define the masked area if one exists.

![images/airplane.png](images/airplane.png)  ![images/masking-004.png](images/masking-004.png)
*Original on the left. The gray checkered area represents the image alpha channel. On the right is the image over a water surface.*

The alpha channel is a portion of each pixel's data that is reserved for transparency information. Alpha channels create and store masks that let you isolate and protect parts of an image while you apply color changes, filters, or other effects to the rest of the image. Each pixel in an image is described as channels of data that define the mixture of the red, green, and blue (RGB) colors. The alpha channel is an 8-bit (256-level) grayscale representation of the image that masks the color of the underlying pixel. The value of the alpha mask determines the intensity of the pixel color. If the Alpha channel is 100%, the images pixel will be complete transparent.  At other alpha strengths, the image pixels will blend with transparency.

#### 색
{: #colormask}
If alpha channel does not exist in an image, a color in the image can be specified as a mask. There is also a sensitivity number to make the mask more or less sensitive to a single specific color as a masked color. Selecting the Color option will activate the Color Dropper, Color Selector, and Sensitivity controls.

#### Color Dropper
Click to select the mask color from the bitmap. Click on the Color Dropper, then on the bitmap to pick the color. This control is only available when the Color option is selected.

{% include_relative snippets/snippet-material-color-select.md %}

#### Sensitivity
The value indicates the size of the area around the color that is also masked. Must be greater than 0.0 for color masking to occur. This control is only available when the Color option is selected.

#### Blur
Partially masks pixels. The value determines the magnitude of partial masking around the masked color. This control is only available when the Color option is selected.

#### Reverse
마스크를 반전시킵니다. 마스크 처리된 픽셀이 지금은 포함되거나, 그 반대의 경우로 처리됩니다.
<!-- TODO: Does this make sense? -->

![images/masking-007.png](images/masking-007.png)  

#### Transparent
아래에 있는 개체의 마스크 처리된 부분을 투명하게 만들어 다른 개체 또는 개체 뒤에 있는 배경이 개체를 통해 보일 수 있습니다. 일반적으로 해당 부분에서 개체의 재질이 그대로 보입니다.

Transparent masking allows a more natural shadow and lets the background objects to show. The underlying material could simply be transparent, but sometimes it is useful to make the surface behind the decal transparent while keeping other areas of the surface opaque.

![images/masking-003.png](images/masking-003.png)    ![images/masking-004.png](images/masking-004.png)

#### Show masked colors
Graphically displays the effects of masking as the parameters change. Use the [Color Selector](select-color.html) ![images/colorswatch-001.png](images/colorswatch-001.png) provided to select the display color of the masked pixels. Changing this color or the setting of the checkbox does not change the masked color. This is simply a graphical tool for editing the mask.

![images/masking-008.png](images/masking-008.png)

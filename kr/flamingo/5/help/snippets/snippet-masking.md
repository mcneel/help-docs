
## Masking
색상값 또는 이미지에 저장된 알파 채널을 기준으로 이미지의 일부를 잘 보이지 않게 합니다.
다음 예에서는 알파 채널 배경을 가진 이미지가 직사각형 서피스에 데칼로 배치되었습니다. 재질을 마스크 처리할 때도 동일합니다.
이 예에서 평면형 서피스에 적용된 재질의 기본색이 빨강입니다.
*![images/airplane.png](images/airplane.png)Original decal image. The gray checkered area represents the image alpha channel.*
*![images/masking-004.png](images/masking-004.png)Final rendered image.*

### None
마스크 처리가 없으면, 데칼 이미지는 아래에 있는 재질을 잘 보이지 않게 가립니다. 직사각형의 평면 서피스는 지반면에 직사각형 그림자를 드리웁니다. 마스크 처리는 이미지에 알파 채널이 있는 부분 또는 컬러 마스크 처리된 부분을 통과하여 재질이 보이도록 설정하지만, 지반면 상의 그림자는 직사각형이며, 서피스 뒤에 있는 배경은 서피스로 인해 가려집니다.
*![images/masking-002.png](images/masking-002.png)Without masking (left) the image covers the surface, with masking (right), the red material shows through.*

### Alpha Channel
Uses the image's [alpha channel](environment-tab.html#alpha) to define the masked area if one exists.
The alpha channel is a portion of each pixel's data that is reserved for transparency information. Alpha channels create and store masks that let you isolate and protect parts of an image while you apply color changes, filters, or other effects to the rest of the image.&#160;
이미지의 각 픽셀은 빨강, 초록, 파랑 (RGB) 의 혼합을 정의하는 데이터 채널로 표현됩니다. 알파 채널은 기저에 있는 픽셀의 색을 마스크 처리한 이미지의 8 비트 (256 단계) 회색조 표현입니다. 알파 채널 값은 픽셀의 채도를 결정합니다.
마스크가 완전 투명하면 빨간색 픽셀은 완전한 채도 (밝은 빨간색으로 완전히 표시됨)를 갖게 되며, 마스크가 완전 불투명하면 이 빨간색이 완전한 투명으로 표시됩니다.

### Color
All image pixels within the sensitivity&#160;range of the selected color will be masked.
배경이 보이도록 마스크 처리할 색을 지정합니다.

#### Color Dropper
클릭하여 비트맵에서 색을 선택합니다.

#### Color swatch
Click to select a color from the [ehlpsource="robohelp classic" class="hcp1" id="a168" style="position: relative;">Select Color]() dialog box.

### Sensitivity *(Color only)* 
마스크 처리되는 색을 중심으로 하는 영역 크기를 나타내는 값입니다. 컬러 마스크 처리가 실행되려면 값이 0.0 보다 커야 합니다.

### Blur *(Color only)* 
픽셀을 부분적으로 마스크 처리합니다. 이 값은 마스크 처리된 색 주변의 부분적 마스크 처리의 규모를 결정합니다.

### Reverse
마스크를 반전시킵니다. 마스크 처리된 픽셀이 지금은 포함되거나, 그 반대의 경우로 처리됩니다.
![images/masking-007.png](images/masking-007.png)

### Transparent
아래에 있는 개체의 마스크 처리된 부분을 투명하게 만들어 다른 개체 또는 개체 뒤에 있는 배경이 개체를 통해 보일 수 있습니다. 일반적으로 해당 부분에서 개체의 재질이 그대로 보입니다.
투명 마스크 처리로 그림자가 더욱 자연스러워지고, 배경 개체도 보이게 됩니다. 아래에 있는 재질을 단순히 투명하게 할 수 있으나, 때때로 데칼 뒤에 있는 서피스를 투명하게 하고 서피스의 다른 부분은 불투명하게 유지하는 방법이 때때로 유용합니다.
![images/masking-003.png](images/masking-003.png)

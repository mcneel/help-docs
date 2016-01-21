
### Máscara
Oscurece partes de la imagen basándose en un valor de color o un canal alfa almacenado en la imagen. Este permite texturas en tienen complejo en forma contornos y crear complejo efectos bitmap agujeros en una superficie.

En este ejemplo, se ha colocado como calcomanía una imagen con un fondo de canal alfa en una superficie rectangular. Las máscara para los materiales funciona del mismo modo.

![images/airplane.png](images/airplane.png)  ![images/masking-004.png](images/masking-004.png)
*Imagen original de calcomanía. El área gris de cuadros representa el canal alfa de la imagen.*

La información de la máscara puede venir de estas tres fuentes en el bitmap:

> [Ninguna](#nomask)
> [Canal alfa](#alphamask)
> [Color](#colormask)

#### Ninguna
{: #nomask}
Sin máscara, la imagen oscurece el material subyacente. La máscara permite mostrar el material a través de la imagen donde existe el canal alfa o el color de máscara. El material asignado a una superficie plana en este ejemplo tiene un color de base rojo.

![images/masking-002.png](images/masking-002.png)
*Sin máscara (izquierda), la imagen cubre la superficie; con máscara (derecha), el material rojo es transparente.*

#### Canal alfa
{: #alphamask}
Utiliza el canal alfa de la imagen [alpha channel](environment-tab.html#alpha) para definir el área de máscara si existe.

![images/airplane.png](images/airplane.png)  ![images/masking-004.png](images/masking-004.png)
*Original a la izquierda. El área gris de cuadros representa el canal alfa de la imagen. A la derecha está la imagen sobre una superficie de agua.*

El canal alfa es una parte de los datos de cada píxel que está reservada para la información de transparencia. Los canales alfa crean y almacenan máscaras que permiten aislar y proteger partes de una imagen mientras se aplican cambios de color, filtros u otros efectos al resto de la imagen. Cada píxel de una imagen se describe como los canales de datos que definen la mezcla de los colores rojo, verde y azul (RGB). El canal alfa es una representación en escala de grises de 8 bits (256 niveles) de la imagen que enmascara el color del píxel subyacente. El valor de la máscara alfa determina la intensidad del color del píxel. Si el canal alfa está en 100%, los píxeles de las imágenes serán completamente transparentes.  En otras intensidades alfa, los píxeles de imagen se mezclan con la transparencia.

#### Color
{: #colormask}
Si una imagen no tiene canal alfa, se puede especificar como máscara un color de la imagen. También hay un número puntoara la sensibilidad que permite hacer la máscara más o menos sensible a un solo color específico como color enmascarado. Si se selecciona la opción Color, se activarán los controles Cuentagotas de color, Selector de color y Sensibilidad.

#### Cuentagotas de color
Haga clic para seleccionar el color de máscara del bitmap. Haga clic en el Cuentagotas de color y luego en el bitmap para designar el color. Este control solo está disponible cuando está seleccionada la opción Color.

{% include_relative snippets/snippet-material-color-select.md %}

#### Sensibilidad
Este valor indica que el tamaño de la zona alrededor del color también tiene máscara. Tiene que ser superior a 0.0 para que se produzca la máscara de color. Este control solo está disponible cuando está seleccionada la opción Color.

#### Difuminado
Enmascara los píxeles parcialmente. Este valor determina la magnitud de la máscara parcial alrededor del color enmascarado. Este control solo está disponible cuando está seleccionada la opción Color.

#### Invertir
Invierte la máscara. Los que píxeles tendrían que tener máscara ahora se incluyen, y viceversa. 
<!-- TODO: Does this make sense? -->

![images/masking-007.png](images/masking-007.png)  

#### Transparente
Hace transparente el área enmascarada del objeto subyacente para que otros objetos o el fondo detrás del objeto se puedan ver a través del objeto. Normalmente, el material del objeto se transparenta en esa área.

La máscara transparente permite que las sombras sean más naturales y se puedan ver los objetos de fondo. El material subyacente podría simplemente ser transparente, pero a veces es conveniente hacer transparente la superficie de atrás de la calcomanía mientras que las otras áreas de la superficie se mantengan opacas.

![images/masking-003.png](images/masking-003.png)    ![images/masking-004.png](images/masking-004.png)

#### Mostrar colores con máscara
Muestra gráficamente los efectos de la máscara al cambiar los parámetros. Utilice el [selector de color](select-color.html) ![images/colorswatch-001.png](images/colorswatch-001.png) para seleccionar el color de visualización de los píxeles con máscara. Cambiar este color o la configuración de la casilla no modifica el color de la máscara. Se trata simplemente de una herramienta gráfica para editar la máscara.

![images/masking-008.png](images/masking-008.png)

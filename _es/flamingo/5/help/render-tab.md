---
---

# ![images/flamingotab.svg](images/flamingotab.svg){:height="75px" width="75px"} Opciones de renderizado
La ficha renderizado controla las propiedades principales del renderizado final.  Utilice esta ficha para controlar la calidad y la duración que puede tardar un renderizado.  La resolución de la imagen final es lo que más influye en el tiempo de renderizado total.

Nota: Una buena práctica es usar una resolución de renderizado baja durante los renderizados de prueba. Utilice renderizados de alta resolución solo en los renderizados finales.

#### ¿Dónde se encuentra el control de iluminación de Flamingo?

 1. ![images/options.png](images/options.png)Barras de herramientas >![images/flamingo-icon.png](images/flamingo-icon.png)Barra de herramientas de Flamingo nXt > Ficha Opciones de renderizado
 1. ![images/menuicon.png](images/menuicon.png)Menús > Flamingo  5.0 > Mostrar panel de control > Flamingo nXt > Ficha Opciones de renderizado


## Ventana a renderizar
{: #viewtorender}
  Defina la vista que renderizará Flamingo nXt 5.  Se trata de una opción muy útil cuando se trabaja en el modelo y el renderizado, pero hay una vista específica que siempre se renderiza.  Por ejemplo, la vista Perspectiva es muchas veces la vista de interés.  Al definir esta opción en la lista desplegable, no es necesario asegurarse que la vista es activa antes de empezar el renderizado.

#### Vista activa
Utilice esta opción para renderizar la vista activa actual.  Es la opción predeterminada.

#### Lista de vistas disponibles
  Esta lista incluye todas las vistas guardadas en el modelo.  Seleccione el nombre de la vista que siempre debe renderizarse.

## Resolución de renderizado
{: #resolution}
La resolución de renderizado es una de las opciones de renderizado más importantes.  Este control ajusta el tamaño y la resolución de la imagen que se guarda en el archivo de Rhino.  Si se aumenta la resolución, aumentará exponencialmente el tiempo de renderizado.  De modo que es importante manejar esta opción con cautela.

#### Píxeles totales
{: #resolutionimagepixels}
Define el número de píxeles totales en el renderizado final, utilizando la vista actual para los índices de altura y anchura.  Es una buena opción para usar cuando se trabaja con renderizados.  Es el mejor ajuste para igualar la vista actual con el renderizado. Es simple aumentar o disminuir la resolución de la imagen simplemente cambiando el número total de píxeles.

### Resolución de vista
Utiliza el tamaño de la vista en píxeles para determinar el tamaño de la imagen renderizada.  Esto crea una recreación de 1 a 1 de la relación de aspecto y la resolución de la vista.  Este modo resulta útil, pero puede ser más lento cuando se renderiza una vista de pantalla completa que cuando se renderiza una vista en la la configuración de vista estándar de Rhino 4.

### Tamaño de imagen
{: #resolutionprintedsize}
El tamaño de la imagen definirá la resolución final en función de diferentes variables.  Es la mejor manera de igualar un tamaño exacto y la resolución de una imagen final. Si la altura y la anchura del renderizado final no coincide con la misma relación de aspecto de la vista que está renderizando, puede que la vista se recorte por la parte superior, inferior o lateral de la vista. Nota: Estos controles también pueden generar renderizado de resolución muy alta que pueden tardar mucho tiempo en completarse.  Utilice estos controles para renderizados finales con alta resolución.

Hay cuatro tipos de unidades que pueden utilizarse:

>Píxeles
>Pulgadas
>Milímetros
>Centímetros

#### Píxeles
Define la imagen de renderizado en píxeles.  Utilice este ajuste para definir la anchura y altura final del renderizado final mediante el número de píxeles.

#### Pulgadas
Define las unidades de página en pulgadas. Las pulgadas se utilizan en combinación con los ajustes de resolución para determinar la resolución final de la imagen renderizada.  Para determinar la resolución final, multiplique el número de pulgadas en anchura y altura por el valor PPP de la resolución.

#### Milímetros
Define las unidades de página en milímetros. Utilice milímetros en combinación con los ajustes de resolución para determinar la resolución final de la imagen renderizada. Para determinar la resolución final, multiplique el número de milímetros en anchura y altura por el valor de puntos de resolución por milímetro.

#### Centímetros
Define las unidades de página en centímetros. Utilice centímetros en combinación con los ajustes de resolución para determinar la resolución final de la imagen renderizada.  Para determinar la resolución final, multiplique el número de centímetros en anchura y altura por el valor de puntos de resolución por centímetro.

#### Aplicar relación de aspecto de vista
Utilice este ajuste para mantener el ajuste de anchura y altura en la misma relación de aspecto que la vista actual.  Esto asegurará que la vista completa se renderiza en la imagen final.

#### Anchura
Anchura de la imagen impresa en el tamaño de la unidad actual.  Multiplique este valor por el ajuste de resolución para lograr el tamaño de imagen final en número total de píxeles.

#### Altura
Altura de la imagen impresa en unidades del tamaño actual.  Multiplique este valor por el ajuste de resolución para lograr el tamaño de imagen final en número total de píxeles.

### Resolución
{: #printsizepixelsperunit}
{: #printsizedpi}
{: #printsizeresolution}

#### Visualización
La imagen se renderiza utilizando la resolución en PPP de la vista. Se trata de la densidad de píxeles en un dispositivo. Normalmente expresa los [puntos por pulgada (PPP)](https://es.wikipedia.org/wiki/Puntos_por_pulgada)

#### Personalizada
La imagen se renderiza utilizando la resolución personalizada. Introduzca la resolución de anchura y altura personalizadas en **Píxeles por: control**.

#### Impresora, calidad de borrador
Establece la resolución a 100 píxeles por pulgada o 4 píxeles por mm.

#### Impresora, calidad normal
Establece la resolución a 150 píxeles por pulgada o 6 píxeles por mm.

#### Impresora, calidad alta
Establece la resolución a 300 píxeles por pulgada o 12 píxeles por mm. Es una resolución bastante alta para un renderizado.  Funciona bien para renderizados más pequeños, pero para renderizados de gran tamaño o pósters, la resolución general puede ser muy alta con este ajuste. Las resoluciones altas pueden necesitar largos tiempos de renderizado.

#### Píxeles por
Cuando el control de Resolución está definido en Personalizado, utilícelo para ajustar la resolución por unidad seleccionada. Cuando se selecciona una resolución preseleccionada, este control muestra la resolución actual.

## Profundidad de campo
{: #depthoffieldoption}
Este efecto crea un desenfoque de profundidad de campo similar al de un objetivo fotográfico. Un objetivo sólo puede enfocar con precisión a una distancia, pero la disminución de la nitidez es gradual alrededor de la distancia focal.

#### Activado
Activa el efecto de profundidad de campo.

#### Intensidad
Controla el tamaño del área focal. Si la Intensidad se ajusta a cero, toda la imagen será nítida. Al aumentar la Intensidad, las áreas fuera de la distancia focal se verán más borrosas y el área focal será más pequeña.

#### Distancia focal
{: #focaldistance}
Define la distancia para la profundidad de campo. Es la distancia alrededor del punto de profundidad de campo en el que los objetos estarán enfocados. Si la Distancia focal es de diez unidades, los objetos alrededor de siete unidades detrás del punto de profundidad de campo y tres unidades delante del punto de profundidad de campo estarán enfocados.

#### Designar >>
Designa un punto en el modelo para la distancia focal.

## Motor de renderizado
{: #render-engine}
Hay tres motores de renderizado diferentes en Flamingo.  Cada motor de render producirá resultados algo diferentes en condiciones normales de renderizado.

Flamingo utiliza técnicas de renderizado progresivas de varios pasos para crear renderizados.  Con pasos progresivos, como los que hace Flamingo, no puede haber artefactos inacabados en cada paso del renderizado. Los artefactos son efectos de renderizado que generan resultados incompletos en un renderizado.  Técnicamente los tres motores de renderizado generarán el mismo renderizado, con el tiempo suficiente.  Pero siendo realistas, el tiempo siempre es un factor limitante. Por tanto, el truco consiste en seleccionar el motor de renderizado que mejor renderice la escena actual en el menor número de pasos.

Es muy fácil seleccionar un motor de renderizado diferente y luego renderizar para ver los resultados.

### Predeterminada
El algoritmo predeterminado produce una simulación de gran calidad. El motor predeterminado es un buen motor de renderizado para una amplia variedad de escenas.  Mientras que los otros dos motores tienen grandes ventajas, también tienen grandes debilidades.  El motor predeterminado es un buen punto de inicio.

El motor de renderizado predeterminado tiene un artefacto muy notable en los primeros pases de los renderizados.  El artefacto se superpone a las sombras.  A medida que los pases avanzan, estas sombras se suavizan.  El motor predeterminado genera un resultado rápidamente, pero puede tardar más pasos para suavizar las sombras.

La diferencia de calidad entre el método predeterminado puede ser muy sutil, sobre todo si se activa la iluminación indirecta. La diferencia de calidad no puede que no compense el tiempo de procesamiento adicional.

### Path Tracer
{: #path-tracer}
El Path Tracer comienza mostrando una imagen granulada que poco a poco se va refinando y suavizando. Este proceso se denomina *convergencia*. El Path Tracer puede ofrecer una mejor calidad de producto acabado en muchos modelos (con una configuración más sencilla), pero a expensas de un cálculo más complejo y lento. **Nota:** El uso del Path Tracer puede crear puntos luminosos o artefactos durante el proceso de renderizado. Estos artefactos son normales con el Path Tracer y desaparecerán con el tiempo.

Algunos efectos avanzados, como la cáustica o la transmisión de desenfoque, pueden calcularse con mayor precisión utilizando el Path Tracer. Las imágenes renderizadas con referencias, plantas y mapas de desplazamiento pueden converger más rápidamente. El Path Tracer normalmente es más fácil de configurar que el método Predeterminado. Las opciones avanzadas, como los sombreadores de reflexión, las entradas de luz diurna y la iluminación ambiente, no se utilizan cuando está seleccionado el motor Path Tracer.

Las imágenes renderizadas con el Path Tracer normalmente tardan más en converger que las imágenes renderizadas con el método predeterminado. Las simulaciones de luz diurna interior, concretamente las escenas donde las ventanas son pequeñas, tardan mucho más en terminar.

### Híbrido
El motor Híbrido es un intento de sacar lo mejor del motor Predeterminado y del motor Path Tracer.  Utiliza efectos de ambos.  El motor Híbrido siempre calculará la luz indirecta.  El artefacto del motor Híbrido es un extenso patrón de puntos que reducirá múltiples pases. En algunas situaciones, puede aplicar muchos pases para quitar ese patrón de puntos. Para muchos renderizados, puede que sea el mejor motor para utilizar.

###  **Avanzado**
Abre el cuadro de diálogo Propiedades de documento en la página de [Flamingo nXt](documentproperties-flamingo.html). Hay varias propiedades avanzadas de renderizado que se pueden configurar para personalizar aún más la calidad del renderizado final.
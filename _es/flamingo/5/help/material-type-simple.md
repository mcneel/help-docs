---
---
# ![images/paint.svg](images/paint.svg){:height="75px" width="75px"} Material Properties
Los materiales de Flamingo se definen mediante una serie de grupos de propiedades. Se trata de tipos de materiales simples de materiales de uso común.  Estos materiales presentan un grupo de controles sencillo. Estos controles facilitan el acceso a las propiedades que hay que cambiar para que un material tenga un aspecto diferente sin la complejidad de los controles avanzados. En la mayoría de materiales simples, cambiar el color es lo único necesario para obtener un aspecto diferente.

#### Tipos de materiales simples:

> ![images/newsolidcolormaterial.png](images/newsolidcolormaterial.png)[Color sólido](#solid-color)
> ![images/newplasticmaterial.png](images/newplasticmaterial.png)[Plástico](#plastic)
> ![images/newmetalmaterial.png](images/newmetalmaterial.png)[Metal](#metal)
> ![images/newglassmaterial.png](images/newglassmaterial.png)[Vidrio](#glass)
> ![images/newglossymaterial.png](images/newglossymaterial.png)[Brillante](#glossy)
> ![images/newclearfinishmaterial.png](images/newclearfinishmaterial.png)[ClearFinish](#clearfinish)
> ![images/newtexturedmaterial.png](images/newtexturedmaterial.png)[Texturizado](#flamingo-textured)
> ![images/newtexturesetmaterial.png](images/newtexturesetmaterial.png)[Conjunto de texturas](#texture-set)

Cualquier material se puede convertir en un material avanzado.  Los materiales avanzados disponen de todos los controles posibles para editar un material en Flamingo nXt.  Para tener el máximo control de un material, utilice los Materiales avanzados o convierta el material existente en un material avanzado.

#### Los materiales avanzados incluyen los siguientes grupos de propiedades:

> [Nombre](material-type-advanced.html#name)
> [Composiciones de material](material-type-advanced.html#procedures)
> [Propiedades de material avanzadas](material-type-advanced.html#advanced-materials-properties)
> [Acabado reflectante](material-type-advanced.html#reflective-finish-and-highlight)
> [Propiedades de transparencia](material-type-advanced.html#transparency)
> [Texturas algorítmicas](material-type-advanced.html#bump-patterns)
> [Texturas bitmap](material-type-advanced.html#textures)
> [Notas](material-type-advanced.html#notes)

Los materiales se guardan en el modelo de Rhino. Los materiales únicos pueden tener el mismo nombre en diferentes modelos de Rhino.

## Color sólido
{: #solid-color}
Los materiales de color sólido solo tienen un [nombre](material-type-advanced.html#name) y un [color](material-type-advanced.html#color).

![images/solidcolors.png](images/3-solidcolor.png)

{% include_relative snippets/snippet-material-name.md %}
{% include_relative snippets/snippet-material-color-select.md %}
{% include_relative snippets/snippet-material-advanced-editor.md %}

## Plástico
{: #plastic}
Los materiales de plástico son ligeramente reflectantes con un [brillo](material-type-advanced.html#highlight-color) de color blanco.

![images/solidcolors.png](images/3-plastic.png)

{% include_relative snippets/snippet-material-name.md %}
{% include_relative snippets/snippet-material-color-select.md %}
{% include_relative snippets/snippet-material-advanced-editor.md %} Utilice el Editor avanzado para reemplazar los preajustes de [Color de brillo](material-type-advanced.html#highlight-color), [Intensidad](material-type-advanced.html#intensity), [Fresnel](material-type-advanced.html#fresnel) y [Definición](material-type-advanced.html#sharpness).

## Metal
{: #metal}
Los materiales de metal tienen un brillo del mismo color que el [color](material-type-advanced.html#color). También puede controlar la [Definición](material-type-advanced.html#sharpness) del reflejo.

![images/solidcolors.png](images/3-metal.png)

{% include_relative snippets/snippet-material-name.md %}
{% include_relative snippets/snippet-material-color-select.md %}
#### Definición
Controla la definición del brillo. Consulte el tema [Definición](material-type-advanced.html#sharpness) en las propiedades de material avanzadas para obtener más información.

{% include_relative snippets/snippet-material-advanced-editor.md %} Utilice el Editor avanzado para reemplazar los preajustes de [Color de brillo](material-type-advanced.html#highlight-color), [Intensidad](material-type-advanced.html#intensity), [Fresnel](material-type-advanced.html#fresnel) y [Tipo](material-type-advanced.html#type). 

## Vidrio
{: #glass}
Los materiales de vidrio tienen un [Color](material-type-advanced.html#color) y un [Índice de refracción](advanced-material-properties-main.html#index-of-refraction) (IOR).

![images/solidcolors.png](images/3-glass.png)

{% include_relative snippets/snippet-material-name.md %}
{% include_relative snippets/snippet-material-color-select.md %}
#### Índice de refracción
Controla la cantidad de luz que se refracta en el material. Consulte el tema [Índice de Refracción](advanced-material-properties-main.html#index-of-refraction) en las propiedades de material avanzadas para obtener más información.

{% include_relative snippets/snippet-material-advanced-editor.md %} Utilice el Editor avanzado para reemplazar los preajustes de [Color de brillo](material-type-advanced.html#highlight-color), [Intensidad](material-type-advanced.html#intensity), [Fresnel](material-type-advanced.html#fresnel), [Definición](material-type-advanced.html#sharpness) y [Transparencia](material-type-advanced.html#transparency).

## Brillante
{: #glossy}
Los materiales brillantes normalmente tienen una [Intensidad](material-type-advanced.html#intensity) de brillo y [Definición](material-type-advanced.html#sharpness) bajas.

![images/solidcolors.png](images/3-glossy.png)

{% include_relative snippets/snippet-material-name.md %}
{% include_relative snippets/snippet-material-color-select.md %}
#### Intensidad
Controla la intensidad del brillo de las luces en la superficie. Consulte el tema [Intensidad](material-type-advanced.html#intensity) en las propiedades de material avanzadas para obtener más información.

#### Definición del brillo
Controla la definición del brillo de las luces en la superficie. Consulte el tema [Definición del brillo](material-type-advanced.html#sharpness) en las propiedades de material avanzadas para obtener más información.

{% include_relative snippets/snippet-material-advanced-editor.md %} Utilice el Editor avanzado para reemplazar los preajustes de [Fresnel](material-type-advanced.html#fresnel) y [Tipo](material-type-advanced.html#type).

## ClearFinish
{: #clearfinish}
El componente ClearFinish es un procedimiento en capas que simula la pintura de coche, porcelana, cerámica, madera barnizada o cualquier otro material que contenga una capa de pintura o de plástico. ClearFinish utiliza la opción [Fresnel](material-type-advanced.html#fresnel) para cambiar el color del material según el ángulo respecto a la vista. Estos materiales suelen ser de color oscuro cuando se mira directamente a la superficie, pero a medida que la superficie se encorva alejándose de la vista, los materiales se vuelven muy brillantes. Un buen ejemplo es la pintura de coches con acabados satinados o laqueados.

![images/solidcolors.png](images/3-clearfinish.png)

{% include_relative snippets/snippet-material-name.md %}
{% include_relative snippets/snippet-material-color-select.md %}
{% include_relative snippets/snippet-material-advanced-editor.md %} Utilice el Editor avanzado para reemplazar los preajustes de [Color de brillo](material-type-advanced.html#highlight-color), [Intensidad](material-type-advanced.html#intensity), [Fresnel](material-type-advanced.html#fresnel) y [Definición](material-type-advanced.html#sharpness).

## Texturizado de Flamingo
{: #flamingo-textured}
Los materiales texturizados utilizan imágenes para crear colores y patrones. El nombre de la imagen, la resolución, el tamaño de loseta y la intensidad y definición del brillo se controlan desde este material simple.

![images/solidcolors.png](images/3-texture.png)

{% include_relative snippets/snippet-material-name.md %}
{% include_relative snippets/snippet-material-color-select.md %}
#### Intensidad
Controla la intensidad del reflejo de espejo de la superficie. Consulte el tema [Intensidad](material-type-advanced.html#intensity) en las propiedades de material avanzadas para obtener más información.

#### Definición
Controla la definición del brillo. Consulte el tema [Definición](material-type-advanced.html#sharpness) en las propiedades de material avanzadas para obtener más información.

#### Imagen
Define el mapa de imagen y las propiedades del material. Aquí hay muchas opciones. Consulte el tema [Imágenes](material-type-advanced.html#texture) de las propiedades de material avanzadas para obtener más información.

{% include_relative snippets/snippet-material-image-add-edit.md %}
{% include_relative snippets/snippet-material-advanced-editor.md %} Utilice el Editor avanzado para reemplazar los preajustes de este material.

## Conjunto de texturas
{: #texture-set}
[Los materiales de conjunto de texturas](texture-set-materials.html) son compatibles con mapas de texturas de terceros que contienen información de mapas de desplazamiento, de normal o de relieve. Los mapas de desplazamiento hacen que el material tenga profundidad. La combinación de estos mapas de textura en conjunto puede crear materiales muy realistas. [PixPlant](http://www.pixplant.com/) es un programa de software que puede usar un bitmap estándar y crear este conjunto de texturas.
<!-- TODO: This dialog Needs a page.-->
![images/solidcolors.png](images/textureset.png)

{% include_relative snippets/snippet-material-name.md %}
#### Anchura y altura
  Controla el tamaño de todas las texturas del conjunto.  Utilice este control para que todos los bitmaps tengan el mismo tamaño y estén alineados.

#### Intensidad
Controla la intensidad del reflejo de espejo de la superficie. Consulte el tema [Intensidad](material-type-advanced.html#intensity) en las propiedades de material avanzadas para obtener más información.

#### Definición
Controla la definición del brillo. Consulte el tema [Definición](material-type-advanced.html#sharpness) en las propiedades de material avanzadas para obtener más información.

#### Tipos
Controla el tipo de reflexión en la superficie.  Consulte el tema [Tipo](material-type-advanced.html#type) en las propiedades de material avanzadas para obtener más información.

{% include_relative snippets/snippet-material-advanced-editor.md %} Utilice el Editor avanzado para reemplazar los preajustes de este material. Nota: Este es un material complejo que utiliza muchas texturas superpuestas definidas con varios valores predeterminados.  El uso del editor avanzado no mantendrá todas las propiedades sincronizadas.

## Material avanzado
El material [Avanzado de Flamingo](material-type-advanced) contiene un conjunto completo de propiedades de un material de Flamingo. Si ninguno de estos materiales simples funciona, utilice el material [Avanzado de Flamingo](material-type-advanced) para crear un material y tener la máxima flexibilidad en la creación de materiales.
---
title: Panel del Editor de materiales
---

# ![images/paint.svg](images/paint.svg){: .inline} {{page.title}}
Los materiales contienen la especificación por color, reflectividad, transparencia, texturas y mapas de relieve de un acabado de superficie. Todos los materiales tienen las opciones básicas. El material predeterminado es blanco y mate, sin reflectividad ni transparencia. Para obtener los mejores resultados, utilice los materiales específicos de Flamingo.

Los materiales se pueden asignar a capas, objetos y bloques. Las asignaciones se pueden realizar arrastrando y colocando en objetos o mediante diferentes controles. Consulte [Asignaciones de materiales](material_assignment.html) para obtener más información.

Una vez asignados, los materiales se guardan en el modelo. El material, las texturas y todos los archivos de soporte para el renderizado se pueden guardar en el modelo de Rhino con las [Opciones de renderizado](http://docs.mcneel.com/rhino/5/help/es-es/index.htm#options/rendering.htm) bien definidas.

Los materiales, entornos y texturas se guardan en el modelo, pero el contenido de renderizado también se puede guardar en los archivos que pueden compartirse entre los modelos. El contenido puede arrastrarse entre sesiones de Rhino y a una carpeta. Las muestras de color se pueden arrastrar y soltar del mismo modo. El [panel Librerías](libraries.html) muestra la carpeta de contenido predeterminada. Utilícela para arrastrar y colocar contenido en el modelo o para arrastrar y colocar contenido del modelo en un archivo externo.

![images/material_editor_panel.svg](images/material_editor_panel.svg){:  #panel_map .float-img-right}

##### ¿Dónde puedo encontrar este comando?
Hay varias opciones para encontrar la ficha Materiales.

* ![images/materialtab.png](images/materialtab.png){: .inline} Ficha Materiales
* ![images/icon-render.png](images/icon-render.png){: .inline} Barra de herramientas Herramientas de renderizado > ![images/materialtab.png](images/materialtab.png){: .inline} Editor de materiales
* Menús > Renderizado > Editor de materiales
* En la línea de comandos, escriba EditorDeMateriales

El panel Editor de materiales se divide en secciones.  Según el tipo de material, los paneles avanzados pueden variar.

Los colores y las texturas pueden arrastrarse desde el selector de color y colocarse en cualquier otro selector de color o control del Editor de materiales, la [Paleta de texturas](texturepalette.html) o el [Editor de entorno](environmenteditor.html).

##### Panel de materiales

 1. [Barra de configuración](#settings)
 1. [Lista de materiales](#material_list)
 1. [Divisor de ventanas](#divider)
 1. [Sección de Propiedades de material](#properties)
 1. [Nombre](#name)
 1. [Paneles de Propiedades de material](#panels)

## [Settings Bar](#panel_map) ![images/callout_1.svg](images/callout_1.svg){: .inline}
{: #settings .clear-img}
Utilice esta barra para navegar por el material durante su desarrollo.

#### ![images/met_leftarrow.png](images/met-leftarrow.png){: .inline} Flecha atrás
Retrocede al material actual o los materiales previamente seleccionados.  Por ejemplo, los materiales con texturas tienen múltiples capas.  Utilice esta flecha para volver al material principal desde los detalles de textura.

####  ![images/met_rightarrow.png](images/met-rightarrow.png){: .inline} Flecha adelante
Retrocede al material actual o los materiales previamente seleccionados.  Por ejemplo, los materiales con texturas tienen múltiples capas.  Utilice esta flecha para volver a la textura usada recientemente desde el material principal.


#### ![images/material_editor.png](images/material_editor.png){: .inline} ![images/texture-2dchecker.png](images/texture-2dchecker.png){: .inline} Nombre de material actualmente seleccionado
Muestra el nombre del material actual y el nivel.  Por ejemplo, si hay una textura o un nivel de material algorítmico, aparecerá  ">". Aquí se puede ver dónde se encuentra el editor en un material.

#### ![images/library_default.png](images/library_default.png){: .inline} Menú Herramientas
Muestra el [menú Herramientas](#tools-menu).  Este amplio menú contiene los comandos, las opciones y las utilidades relacionadas con los materiales.


## [Lista de materiales](#panel_map) ![images/callout_2.svg](images/callout_2.svg){: .inline}
{: #material_list}
Muestra una lista de todos los materiales que contiene el modelo. De esta lista:

* Desplácese hacia arriba y hacia abajo en la lista para ver todos los materiales del modelo.
* Arrastre y coloque un material de esta lista en una capa en el [Panel de capas](http://docs.mcneel.com/rhino/5/help/es-es/index.htm#commands/layer.htm) bien directamente sobre un objeto para asignárselo. Consulte [Asignaciones de materiales](material_assignment.html) para obtener más información.
* Añada un nuevo Material utilizando el botón Añadir nuevo ![images/add_material.png](images/add_material.png){: .inline} que aparece en la parte inferior de la lista.


* Haga clic en cada material para seleccionarlo. Una vez seleccionado, las propiedades del material se mostrarán en los paneles. Consulte [Propiedades de materiales de renderizado](#properties) para obtener más información.
* Haga clic con el botón derecho en una miniatura par ver el menú contextual del material.
* Haga clic con el botón derecho en el área en blanco para ver el menú contextual del nuevo material.

###  ![images/add_material.png](images/add_material.png){: .inline} Añadir nuevo material
{: #add_material}
Desplácese hasta la parte inferior de la lista de materiales para ver el icono de agregar.

Abre la [librería](libraries.html) de materiales de Contenido de renderizado.
Los materiales de la librería pueden utilizarse como plantillas para crear materiales en el modelo.

### Menú contextual del material
{: material_context}
Este menú está disponible haciendo clic con el botón derecho en una lista de materiales.  Consulte el [menú Herramientas](#tools_menu) para obtener más información sobre las distintas opciones del menú.

### Menú contextual de nuevo material
{: new_material_context}
Este menú está disponible haciendo clic con el botón derecho en el area en blanco de la lista de materiales.

#### ![images/toolbarlus.png](images/toolbarplus.png){: .inline} Crear nuevo material
Crea un nuevo material básico blanco mate.


#### ![images/paste.png](images/paste.png){: .inline} Pegar
Crea un nuevo material basado en el contenido del portapapeles.

#### ![images/pasteasinstance.png](images/pasteasinstance.png){: .inline} Pegar como instancia
Crea un nuevo material basado en el contenido del portapapeles vinculado al original a través de instancias.

#### ![images/grid.png](images/grid.png){: .inline} Cuadrícula
Muestra las vistas previas como rejilla de miniaturas.

#### ![images/list.png](images/list.png){: .inline} Lista
Muestra las vistas previas como lista de miniaturas.

#### ![images/tree.png](images/tree.png){: .inline} Árbol
Muestra las vistas previas en forma de árbol anidado.

#### ![images/horizontal.png](images/horizontal.png){: .inline} Disposición horizontal
Muestra las vistas previas a la izquierda de los controles.

#### ![images/showpreview.png](images/showpreview.png){: .inline} Panel de vista previa
Muestra las propiedades de vista previa de la miniatura seleccionada. Define la geometría, el tamaño, el fondo y el comportamiento de rotación de la vista previa.

#### ![images/floatthumbnail.png](images/floatthumbnail.png){: .inline} Flotante
Pone flotante la imagen de vista previa en una ventana de tamaño ajustable.

#### Miniaturas

##### ![images/small.png](images/small.png){: .inline} Pequeño
Define el tamaño de las miniaturas al tamaño más pequeño.

##### ![images/medium.png](images/medium.png){: .inline} Mediano
Define el tamaño de las miniaturas al tamaño mediano.

##### ![images/large.png](images/large.png){: .inline} Grande
Define el tamaño de las miniaturas al tamaño grande.

##### ![images/showlabels.png](images/showlabels.png){: .inline} Mostrar etiquetas
Muestra las etiquetas de los nombres de las miniaturas en el modo Rejilla.
El modo Lista siempre muestra las etiquetas.

##### ![images/showunits.png](images/showunits.png){: .inline} Mostrar unidades
Muestra el tamaño en unidades del modelo.

##### ![images/autoupdatethumbnail.png](images/autoupdatethumbnail.png){: .inline} Actualización automática de vista previa
Actualiza automáticamente todas las vistas previas cuando cambia la configuración.

##### ![images/updateallpreviews.png](images/updateallpreviews.png){: .inline} Actualizar todas las vistas previas
Actualiza las vistas previas manualmente cuando la Actualización automática de vista previa está desactivada.

## [Divisor de ventanas](#panel_map) ![images/callout_3.svg](images/callout_3.svg){: .inline}
{: #divider}
Arrastre este divisor para cambiar la longitud de la Lista de materiales. Si amplía la Lista de materiales, la sección Propiedades de material se reduce.

## [Sección Propiedades de material](#panel_map) ![images/callout_4.svg](images/callout_4.svg){: .inline}
{: #properties}

#### [Nombre de material](#panel_map) ![images/callout_5.svg](images/callout_5.svg){: .inline}
{: #name}
Es el nombre del material. El nombre de material también se guarda como nombre de archivo al exportar el material a la biblioteca. Nota: Los materiales se guardan en el modelo de Rhino. Los materiales únicos pueden tener el mismo nombre en diferentes modelos de Rhino.

#### [Paneles de materiales](material-editor.html#panel_map) ![images/callout_6.svg](images/callout_6.svg){: .inline}
{: #panels}
La sección Propiedades de materiales contiene varios paneles de Materiales. Al hacer clic en la barra de título gris se repliega el panel de materiales y se oculta el contenido de ese panel.  Vuelva a hacer clic en el título de la barra para mostrar el contenido.

Los paneles de material varían en función del tipo de material y el nivel del material actualmente activo. Para obtener más información sobre paneles de materiales específicos, consulte [Materiales de Flamingo](material-type-simple.html).

## Menú Herramientas ![images/library_default.png](images/library_default.png){: .inline}
{: #tools-menu}
<!-- This comes from the page http://docs.mcneel.com/rhino/5/help/en-us/popup_moreinformation/materialthumbnail_contextmenu.htm -->
Estas opciones también aparecen al hacer clic con el botón derecho en los menús contextuales de las previsualizaciones de miniaturas y el fondos de miniatura.

#### ![images/assigntoobjects.png](images/assigntoobjects.png){: .inline} Asignar a la selección
Asigna el material actual a los objetos seleccionados.

##### Para asignar un material a objetos
 1. Haga clic para Asignar a la selección.
 1. En la vista Rhino, seleccione los objetos de destino.

##### Para preseleccionar objetos
 1. En la vista Rhino, seleccione los objetos de destino.
 1. Haga clic para Asignar a la selección.
Los objetos de destino pueden seleccionarse antes o después de hacer clic en Asignar a la selección.

##### Para arrastrar y colocar materiales en objetos
 * Arrastre el material desde las miniaturas o la lista a los objetos de destino.
Arrastrar y colocar funciona solo con un objeto a la vez.

#### ![images/assigntolayers.png](images/assigntolayers.png){: .inline} Asignar a capas
Asigna el material actual a las capas.

##### Para asignar un material a las capas
 1. Haga clic en Asignar a capas.
 1. En el cuadro de diálogo Seleccionar capas, marque las casillas de asignación de material.

##### Para asignar materiales desde el panel Capas
 1. En el panel [Capa](http://docs.mcneel.com/rhino/5/help/es-es/index.htm#commands/layer.htm), seleccione una o más capas y haga clic en la columna [Material](http://docs.mcneel.com/rhino/5/help/en-us/commands/layer.htm#Material).
 1. En el cuadro de diálogo Material de capa, seleccione el material que quiera asignar.


##### Para arrastrar un material a una capa
 * Arrastre el material desde las miniaturas o la lista a la capa de destino.
Arrastrar y colocar funciona solo con una capa a la vez.

#### ![images/materials_selectobjects.png](images/materials_selectobjects.png){: .inline} Seleccionar objetos
Seleccione los objetos del modelo para la asignación de material.

#### ![images/toolbarplus.png](images/toolbarplus.png){: .inline} Crear nuevo material
Abre la [librería](libraries.html) de materiales de Contenido de renderizado.
Los materiales de la librería pueden utilizarse como plantillas para crear materiales en el modelo.

#### ![images/import.png](images/import.png){: .inline} Importar material desde archivo
Importa materiales desde un archivo .rmtl de Rhino guardado.

#### ![images/savetofile.png](images/savetofile.png){: .inline} Guardar en archivo
Guarda un material a un archivo .rmtl de Rhino.

#### ![images/changetype.png](images/changetype.png){: .inline} Cambiar tipo
Cambia el tipo de material.

#### ![images/changetype.png](images/changetype.png){: .inline} Cambiar tipo (Copiar opciones similares)
Cambia el tipo de material.
El comportamiento predeterminado depende del estado actual de la casilla [Opciones: Renderizado](http://docs.mcneel.com/rhino/5/help/es-es/index.htm#popup_moreinformation/materialpanel_toolsmenu.htm) >  [Copiar configuración similar cuando se modifica el tipo de contenido](http://docs.mcneel.com/rhino/5/help/es-es/index.htm#popup_moreinformation/materialpanel_toolsmenu.htm). Si esta opción está activada, la configuración compatible del contenido antiguo se copiará a la nueva.

#### ![images/reset.png](images/reset.png){: .inline} Restaurar valores predeterminados
Cambia la configuración del material al material predeterminado blanco, mate y no reflectante.

#### ![images/copy.png](images/copy.png){: .inline} Copiar
Copia el material seleccionado al portapapeles de Windows. El portapapeles puede pegarse en el editor para crear un nuevo material o directamente en una carpeta para crear un  archivo de [librería](libraries.html).

#### ![images/paste.png](images/paste.png){: .inline} Pegar
Crea un nuevo material basado en el contenido del portapapeles.

#### ![images/pasteasinstance.png](images/pasteasinstance.png){: .inline} Pegar como instancia
Crea un nuevo material basado en el contenido del portapapeles vinculado al original a través de instancias.

#### ![images/delete.png](images/delete.png){: .inline} Eliminar
Elimina el material seleccionado.

#### ![images/rename.png](images/rename.png){: .inline} Cambiar nombre...
Cambia el nombre del material seleccionado.

#### ![images/duplicate.png](images/duplicate.png){: .inline} Duplicar
Copia el material seleccionado a un nuevo material con la misma configuración.

#### ![images/removeinstancing.png](images/removeinstancing.png){: .inline} Quitar referencias
Elimina la la conexión entre los materiales [referenciados](http://docs.mcneel.com/rhino/5/help/en-us/index.htm#popup_moreinformation/materialpanel_toolsmenu.htm).
{% include_relative snippets/snippet-contenteditorpreviewoptions.md %}


#### ![images/contentfilter.png](images/contentfilter.png){: .inline} Filtro de contenido
Abre el  cuadro de diálogo [Filtros de contenido](content_filters.html).

#### ![images/rename.png](images/rename.png){: .inline} Propiedades
Abre el cuadro de diálogo [Propiedades de vista previa](http://docs.mcneel.com/rhino/5/help/en-us/index.htm#popup_moreinformation/materialpanel_toolsmenu.htm).
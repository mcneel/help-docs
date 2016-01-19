---
---

# ![images/paint.svg](images/paint.svg){:height="75px" width="75px"} Asignaciones de material
Los objetos de la escena tienen una fuente de material. Aquí es donde adoptan su material de renderizado.  Los materiales se pueden asignar de varias maneras. El método utilizado para asignar materiales tiene un gran efecto en la facilidad que tendrá para modificarse y mantenerse en el futuro.

Los materiales se pueden asignar de tres maneras. Los tres forman una jerarquía, de modo que una asignación inferior en la lista sobrescribirá una asignación superior. Los tres modos son:

 1. [Capas](#bylayer) - Todos los objetos de la capa adoptarán este material, a menos que estén en un bloque o tengan una asignación de objeto específica.
 2. [Por capa principal](#byparent) - Se utiliza para los objetos dentro de bloques.  Los objetos con una asignación Por objeto principal buscarán el material en la inserción de bloque.
 3. [Objetos individuales](#byobject) - Los materiales se pueden asignar directamente a un objeto, sobrescribiendo cualquier otra asignación de material.

La asignación de materiales por capa es el método recomendado. La opción Por capa facilita modificar el material de todos los objetos de una capa. Utilice la asignación  Por objeto únicamente si tiene algunos objetos que no quiere tener en capas separadas.

Los archivos importados pueden tener cualquiera de estas tres asignaciones. Muchos archivos importados tendrán asignaciones Por objeto.  Puede suponer mucho trabajo convertir el modelo a asignaciones Por capa, pero puede ser provechoso si se prevé mucha edición de los materiales de renderizado.

Una vez que se asignan los materiales, el material se guardará en el modelo actual.  La edición de material no afectará a ese material en otros modelos.

## Asignar materiales a capas
{: #bylayer}
La asignación de materiales por capa permite asignar un material a todos los objetos de un capa. Este es el método predeterminado de asignación. Para cambiar la asignación de material de la capa, utilice el  cuadro de diálogo [Capas](http://docs.mcneel.com/rhino/5/help/es-es/commands/layer.htm).
Nota: Si se elimina un material del [Editor de materiales](material-editor.html), todos los objetos que tenían asignado el material eliminado pasarán a tener asignación por capa.

##### Arrastrar un material a una capa
{: #drag-dropmaterialtolayer}
1. En Rhino 5, abra el cuadro de diálogo [Capas](http://docs.mcneel.com/rhino/5/help/es-es/commands/layer.htm).
1. En la [Lista de materiales](material-editor.html#material_list), en la ficha Librería o Editor de materiales, arrastre un material sobre el nombre de capa en el diálogo [Capas](http://docs.mcneel.com/rhino/5/help/es-es/commands/layer.htm).

##### Para asignar un material a una capa
1. En Rhino 5, abra el cuadro de diálogo [Capas](http://docs.mcneel.com/rhino/5/help/es-es/commands/layer.htm).
1. Seleccione uno o más nombres de capa y haga clic en la columna Material.
1. En el cuadro de diálogo Material de capa, seleccione un material de la lista desplegable de materiales.

##### Quitar un material de una capa
{: #detachmaterialfromlayer}
1. En Rhino 5, abra el cuadro de diálogo [Capas](http://docs.mcneel.com/rhino/5/help/es-es/commands/layer.htm).
1. Seleccione uno o más nombres de capa y haga clic en la columna Material.
1. En el cuadro de diálogo Material de capa, seleccione el material predeterminado de la lista desplegable de materiales.

## Asignar material por objeto principal
{: #byparent}
La opción Por objeto principal se utiliza poco, pero es una asignación muy útil. Los objetos de una referencia de bloque mantienen las asignaciones Por capa o Por objeto.  Los objetos que utilizan la asignación Por objeto principal adoptarán el material de la inserción de bloque.  De este modo, los objetos que están dentro de una instancia de bloque pueden adoptar el material del bloque principal.

Como ejemplo, un modelo de coche puede tener llantas en la capa llantas y ruedas en la capa ruedas. Pero para el renderizado, la carrocería del coche puede variar entre las referencias de bloque individuales. Asigne por objeto principal en la carrocería del coche.  A continuación, se puede asignar un material a la inserción de bloque y solo adoptará ese material la carrocería.

##### Para asignar un material a través de las propiedades del objeto
1. Seleccione objetos.
1. En el menú Edición, haga clic en Propiedades de objeto ![images/properties.png](images/properties.png) para editar el objeto.
1. En el cuadro de diálogo [Propiedades](properties-object.html), en la página Material ![images/materialtab.png](images/materialtab.png), debajo de Asignar por, seleccione Por objeto principal.

## Asignar materiales a objetos
{: #byobject}
Puede asignar materiales de las librerías de materiales a una capa o a un objeto. Los materiales de renderizado se asignan a objetos individuales y son utilizados por el renderizador integrado en Rhino.
Consulte [Editor de materiales](material-editor.html) .

La asignación de materiales por capa es el método recomendado. Asigne materiales por objeto únicamente si tiene algunos objetos que no quiere tener en capas separadas.

##### Asignar un material a través de las propiedades del objeto
1. Seleccione objetos.
1. En el menú Edición, haga clic en [Propiedades de objeto ![images/properties.png](images/properties.png) para editar el objeto.
1. En el cuadro de diálogo [Propiedades](properties-object.html), en la página Materiales ![images/materialtab.png](images/materialtab.png), debajo de Asignar por, seleccione Por objeto principal y luego haga clic en el material de la lista.

##### Arrastrar un material sobre un objeto
{: #drag-dropmaterialtoobject}

 * En la [Lista de materiales](material-editor.html#material_list), en la ficha Librería o Editor de materiales, arrastre un material sobre un objeto. El objeto quedará resaltado cuando el cursor esté situado en el lugar correcto para soltar el material.

##### Asignar un material a los objetos seleccionados
1. Seleccione objetos.
1. En la [Lista de materiales](material-editor.html#material_list), en la ficha Librería o Editor de materiales, haga clic con el botón derecho en un material desde la paleta Materiales del modelo.
1. En el menú, haga clic en Asignar a objetos seleccionados.

##### Seleccionar objetos con asignación de material
{: #select-objects-with-material-assignment}
1. En la [Lista de materiales](material-editor.html#material_list), en la ficha Librería o Editor de materiales, haga clic con el botón derecho en un material desde la paleta Materiales del modelo.
1. En el menú, haga clic en Seleccionar objetos con este material.

##### Quitar una asignación de material por objeto
{: #removematerialfromobject}
1. Seleccione objetos.
1. En el menú Edición, haga clic en Propiedades de objeto.
1. En el cuadro de diálogo [Propiedades](properties-object.html), en la página Material, debajo de Asignar por, seleccione Capa.
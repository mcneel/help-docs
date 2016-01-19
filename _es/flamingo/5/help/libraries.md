---
---

# ![images/libraries.svg](images/libraries.svg){:height="75px" width="75px"} Libraries Panel
El comando Librerías abre el panel Librerías para administrar las librerías de materiales, texturas y entornos.

El contenido de renderizado se puede guardar en los archivos para crear librerías externas que pueden compartirse entre los modelos. El contenido también puede arrastrarse entre sesiones de Rhino y a una carpeta.

Las muestras de color se pueden arrastrar y soltar del mismo modo.

El panel Librerías muestra una vista en las carpetas de contenido que ha configurado. Utilice esta opción para arrastrar y colocar contenido al modelo o para almacenar contenido del documento en una ubicación fuera del modelo.

Los materiales son archivos que se encuentran en el disco duro.  Las carpetas de librerías son carpetas de Windows.  Puede copiar, pegar y mover carpetas como con cualquier archivo o carpeta de Windows.

Utilice la barra de direcciones en la parte superior de la ficha Librerías para navegar a cualquier carpeta de su ordenador.

Para navegar rápidamente a las ubicaciones de la Librería predeterminada, utilice el icono de llave en la parte superior derecha. ![images/library_default.png](images/library_default.png)

#### Organización de las librerías
{: organizing_libraries}
Las librerías son simplemente archivos.  Puede copiar, pegar y mover los archivos en las carpetas. Utilice el Explorador de Windows para editar las carpetas y los documentos. Para editar qué carpetas son las predeterminadas en la ficha Librerías, utilice la [Configuración de librería](#settings) ![images/library_default.png](images/library_default.png).

## Librería de materiales
{: #material}
Los materiales son archivos que se encuentran en el disco duro.  Una vez asignado al modelo, el material se almacena y se guarda en el modelo.  Cualquier cambio realizado en el material asignado no cambiará el material original del disco duro.

Arrastre y suelte los materiales para asignarlos al modelo. Los materiales se pueden asignar a:

#### Asignación por capa
Arrastre un material directamente en el nombre de la capa en el Panel de capas. Este es el método recomendado ya que por defecto cualquier objeto en la capa adoptará la asignación del material. Los cambios posteriores en el material pueden ser rápidos simplemente soltando otro material en la capa.

#### Asignación por objeto
Arrastre un material directamente sobre un objeto en cualquier vista. La opción Por objeto reemplaza a la asignación del material Por capa.

#### Asignación por bloque
Arrastre un material sobre un bloque y cualquier objeto que tenga un material asignado Por objeto principal adoptará ese material.  Cualquier objeto dentro del bloque que tenga un material Por objeto principal adoptará el material de los bloques.

## Librería de plantas
{: #plant}
En la carpeta de la librería predeterminada se encuentra la carpeta Plantas.  Vaya a esa carpeta para colocar plantas en el modelo.  Una vez insertada, la planta se almacena y se guarda en el modelo.  Cualquier cambio realizado en el material asignado no cambiará el material original del disco duro. Arrastre y coloque plantas en una vista para insertarlas en el modelo. Para obtener más información, consulte el tema [Plantas](plants.html) de la Ayuda.

## Librería de entornos
{: #environment}
Los entornos se pueden guardar en la librería.  Esto permite pasar las opciones de Entorno de un modelo a otro.  Para obtener más información, consulte [Entornos](environment-tab.html).

## Configuración de librerías
{: #settings}
Utilice las ![images/options.png](images/options.png)Opciones de librerías para cambiar los valores predeterminados de las librerías que aparecen en el menú ![images/library_default.png](images/library_default.png).

##### Dónde puedo encontrar este comando?
El comando Opciones de librerías puede ejecutar de tres formas:

 1. Ficha Librerías > ![images/library_default.png](images/library_default.png) en la parte superior derecha del panel Librerías > Configuración...
 1. Menús > Herramientas > Opciones > Librerías.
 

### Mostrar contenido de renderizado
Utilice esta opción para mostrar u ocultar la ubicación del contenido de renderizado predeterminado.

#### Utilizar ubicación de librería predeterminada (Mis documentos)
De manera predeterminada, las [librerías de contenido](libraries.html) son una subcarpeta de la carpeta *Mis documentos*.

#### Personalizada
Define una ubicación de [librería](libraries.html) personalizada.  Cambia la ubicación predeterminada de las [librerías de contenido](libraries.html) de este equipo.

##### Botón Examinar
Abre el navegador de archivos para especificar un archivo.

#### Mostrar carpeta Documentos
En el panel [Librerías](libraries.html), la carpeta Documentos designada se mostrará en el menú.

#### Mostrar carpetas personalizadas
En el panel [Librerías](libraries.html), las carpetas personalizadas designadas se mostrarán en el menú.
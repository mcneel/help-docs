---
---


# ![images/flamingotab.svg](images/flamingotab.svg){:height="75px" width="75px"} Getting Started with Flamingo nXtÂ®
Flamingo nXt crea imágenes fotorrealistas, panoramas y animaciones de alta calidad desde modelos 3D en Rhinoceros®. Flamingo nXt 5 es una actualización de Flamingo que se integra con las funciones de renderizado de Rhino 5. La versión actual es una versión en progreso.

Flamingo se puede descargar e instalar desde [Descargar Flamingo nXt 5](http://www.rhino3d.com/download/flamingo/5/beta).

Puede participar en las discusiones técnicas del [Foro de Flamingo en Discourse](http://discourse.mcneel.com/c/rendering/flamingo)

## Instalación

* La beta de Flamingo 5 requiere tener instalada una versión anterior de Flamingo nXt.
* Es necesario tener Rhino 5 Service Release 12 para poder ejecutar Flamingo nXt 5.

Después de descargar y ejecutar el instalador RHI, inicie Rhino.

Para obtener soporte técnico, tutoriales, ejemplos e información sobre cómo empezar a utilizar **Flamingo nXt**, visite el [sitio web de Flamingo nXt](http://nxt.flamingo3d.com/).

> [Tutoriales](http://nxt.flamingo3d.com/page/tutoriales-y-documentacion)
> [Galería](http://nxt.flamingo3d.com/photo)
> [Soporte técnico](http://nxt.flamingo3d.com/forum)

## Panel de control de Flamingo nXt
{: #control-panel}
Esta versión de Flamingo ofrece una interfaz integrada en las herramientas de renderizado de Rhino 5. El panel de control de Flamingo nXt contiene fichas para configurar el modelo para el renderizado:

> [Materiales](materials-tab.html)
> [Iluminación](lighting-tab.html)
> [Entorno](environment-tab.html)
> [Renderizado](render-tab.html)

## Para acceder al Panel de control de Flamingo
* En el menú Flamingo nXt 5, haga clic en Panel de control.

## Conceptos básicos sobre renderizado
{: #rendering-basics}
El renderizado de un modelo acabado comprende cuatro pasos básicos:

 1. [Configurar los materiales](material-editor.html)
 1. [Configurar la iluminación](lighting-tab.html)
 1. [Configurar un entorno](environment-tab.html)
 1. [Configurar las condiciones de renderizado](render-tab.html)

##### Para iniciar un renderizado
* En el menú Renderizado o Flamingo, haga clic en Renderizar.
* En la barra de herramientas Estándar, haga clic en el botón Renderizar.

### Detener renderizado
De manera predeterminada, el proceso de renderizado continuará refinando la imagen, pase tras pase, hasta que haga clic en el botón Detener renderizado. Esta opción permite controlar la relación tiempo-calidad. Cuanto más tiempo continúe el renderizado, más se parecerá al  resultado "correcto" del renderizado completo. El digitalizador se puede recalibrar en cualquier momento.

###  Reanudar renderizado
Al hacer clic en el botón Detener renderizado, se suspende el proceso de renderizado después de completarse el pase en curso.
A continuación, el botón cambia a Reanudar renderizado. Si ha detenido el renderizado antes del número de pases o si se han alcanzado las restricciones de tiempo, puede hacer clic en el botón Reanudar renderizado para continuar.
Utilice las opciones de [Número de pases](render-window.html#number-of-passes) o [Tiempo](render-window.html#time) en la [Ventana de renderizado](render-window.html) o en [Propiedades de documento > Flamingo nXt](documentproperties-flamingo.html) para definir un punto de detención automática.
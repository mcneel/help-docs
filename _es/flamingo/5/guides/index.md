---
layout: fullwidth-page
---

# Introducción a Flamingo nXt 5®
 
## Instalación

La beta de Flamingo 5 requiere tener instalada una versión anterior de Flamingo nXt.
Es necesario tener Rhino 5 Service Release 12 para poder ejecutar Flamingo nXt 5.
Después de descargar y ejecutar el instalador RHI, inicie Rhino.
Notas iniciales

Esta versión de Flamingo ofrece una interfaz integrada en las herramientas de renderizado de Rhino 5. Por este motivo, se han realizado varios cambios necesarios en la interfaz de renderizado. Es importante encontrar la interfaz Flamingo al iniciar Flamingo por primera vez:

El panel de control de Flamingo se encuentra en el desplegable Renderizado > Flamingo nXt 5 > Mostrar panel de control
La ficha Flamingo nXt contiene controles específicos de Flamingo:
Cielo
Administrador de iluminación
Controles de iluminación personalizados
Opciones de renderizado
Una vez en panel de control, haga clic con el botón derecho en el área de la ficha y seleccione los paneles:
Librerías
Entorno
Plano de suelo
Etc.
 
## Para acceder al Panel de control de Flamingo
  * En el menú **Flamingo nXt**, haga clic en **Panel de control**.

  ## Panel de control de Flamingo nXt
El panel de control de **Flamingo nXt** contiene fichas para configurar el modelo para el renderizado:

 *  [Materiales](..\materials\materials-tab.html) 
 *  [Iluminación](../lighting/lighting-tab.html) 
 *  [Entorno](../environment/environment-tab.html) 
 *  [Renderizado](../render/render-tab.html) 

## Conceptos básicos sobre renderizado
 
El renderizado de un modelo acabado comprende cuatro pasos básicos:

 *  [Configurar los materiales](..\materials\materials-tab.html) 
 *  [Configurar la iluminación](../lighting/lighting-tab.html) 
 *  [Configurar un entorno](../environment/environment-tab.html) 
 *  [Configurar las condiciones de renderizado](../render/render-tab.html) 

#### Para iniciar un renderizado

 * En el menú **Renderizado** o **Flamingo nXt**, haga clic en **Renderizar**.
- O bien -

 * En la barra de herramientas **Estándar**, haga clic en el botón **Renderizar**.

### Detener renderizado
 

De manera predeterminada, el proceso de renderizado continuará refinando la imagen, pase tras pase, hasta que haga clic en el botón Detener renderizado. Esta opción permite controlar la relación tiempo-calidad. Cuanto más tiempo continúe el renderizado, más se parecerá al  resultado "correcto" del renderizado completo. El digitalizador se puede recalibrar en cualquier momento.


###  <kbd>Reanudar renderizado</kbd> 
 

Al hacer clic en el botón **Detener renderizado**, se suspende el proceso de renderizado después de completarse el pase en curso.

A continuación, el botón cambia a **Reanudar renderizado**. Si ha detenido el renderizado antes del número de pases o si se han alcanzado las restricciones de tiempo, puede hacer clic en el botón **Reanudar renderizado** para continuar.

Utilice las opciones de [Número de pases](..\render\render-window.html#number-of-passes) o [Tiempo](..\render\render-window.html#time) en la [Ventana de renderizado](..\render\render-window.html) o en [Propiedades de documento > Flamingo nXt](..\render\documentproperties-flamingo.html) para definir un punto de detención automática.

&#160;

Revisión: 22-Dic-2015 14:45


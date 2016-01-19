---
---

# Render Farm
El Render Farm de Flamingo nXt utiliza la potencia de varios equipos para renderizar imágenes individuales, trabajos por lotes de varias imágenes o animaciones basadas en vistas. No es necesario que Rhino ni Flamingo nXt estén instalados en los equipos que se utilizarán como clientes de Render Farm.

#### Esquema típico de Render Farm
{: #render-farm}

![images/renderfarm-002.png](images/renderfarm-002.png){: style="margin-top:25px;"}

>![images/01.png](images/01.png)Equipo con Rhino y Flamingo nXt.
>![images/02.png](images/02.png)Servidor de red o carpeta de Render Farm compartida.
>![images/03.png](images/03.png)Dos clientes de Render Farm. (Render Farm de nXt incluye dos copias gratuitas del software cliente.)
>![images/04.png](images/04.png)Clientes de Render Farm adicionales adquiridos.

El Render Farm es gratuito para dos equipos cliente. Para añadir más equipos cliente, puede comprar la licencia de Render Farm de nXt desde [https://www2.mcneel.com/commerce/accurender/buy-farm.asp](https://www2.mcneel.com/commerce/accurender/buy-farm.asp).

#### Carpeta de Farm compartida
{: farm-folder}
La clave para tener un Render Farm funcional es una carpeta compartida a la que puedan acceder la máquina principal y todos los equipos cliente.  Normalmente es una carpeta de red compartida.  Puede ser una carpeta en la máquina principal o en una red.  La carpeta no tiene que estar asignada al mismo nombre en cada cliente, pero cada cliente necesita acceso completo de lectura/escritura/eliminación a la carpeta.  La carpeta compartida debe tener al menos 20GB de almacenamiento disponible.

#### Render Farm de nXt tiene dos aplicaciones:

##### Cliente de Render Farm (nXtFarmer64.exe) 
Se trata de un pequeño programa que se ejecuta en cada cliente de renderizado en red y espera que se generen trabajos. Normalmente, las Render Farm trabajan en segundo plano sin mostrar el progreso de los renderizados en un monitor. El renderizado de este modo permite el uso de más potencia de los equipos para tareas largas, pero no permite la interacción con el renderizado a medida que avanza.

##### Farm Monitor (nXtFarmMonitor64.exe)
Miniaplicación que muestra el estado de los trabajos de renderizado y proporciona herramientas de control simples.
En instalaciones avanzadas, el software Render Farm de nXt permite trabajar con administradores de renderizado de terceros. Los siguientes procedimientos se aplican al Render Farm que se incluye en Flamingo nXt. Si planea utilizar un software de Render Farm de terceros, algunos de estos procedimientos serán diferentes.

#### El proceso de Render Farm
{: #the-farm-process}
 1. Para iniciar un renderizado con Flamingo nXt, en lugar de utilizar el comando Renderizar estándar, utilice el Render Farm *(Flamingo nXt > Render Farm)*. El trabajo de renderizado se enviará a la [carpeta de salida de Render Farm](options-flamingo.html#farm-output-folder). Todos los materiales y la información de soporte se enviará automáticamente junto con el trabajo.
 2. Los trabajos de renderizado se dividen en diferentes tareas. Los clientes de Render Farm comprueban continuamente si hay algún trabajo nuevo en la carpeta de salida de Render Farm. Cada cliente asumirá un trabajo y empezará a renderizar. El Farm Monitor *(Flamingo nXt > Utilidades > Farm Monitor)* permite hacer el seguimiento de los trabajos en curso.
 3. Cada cliente de Render Farm deposita los resultados en la carpeta de Render Farm *nombre del trabajo* \Output.
 3. Cuando un cliente termine con un trabajo, continuará asumiendo nuevos trabajos a medida que se vayan enviando al Render Farm.
 4. La salida de Farm será en el [formato de imagen de nXt (.nXtImage)](image-editor.html).  Las imágenes en este formato pueden editarse con el [Editor de imágenes de nXt](image-editor.html). Los resultados también pueden guardarse como archivo TGA, PNG, TIF y JPG desde el [Editor de imágenes de nXt](image-editor.html).

## Instalar y configurar The Farm
{: #install}
El cliente de Farm Render y el Farm Monitor se instalan con Flamingo en la máquina principal con Rhino.  En otros equipos cliente que no tienen Rhino y Flamingo nXt, tiene que estar instalado el cliente del Farm.

##### Instalación del Render Farm
En equipos cliente que no tienen instalado Rhino y Flamingo nXt, instale el cliente del Farm:

 1. Descargue el [software del Render Farm](http://www.rhino3d.com/download/The-Farm/1.0/release) actual.
 1. Ejecute el instalador descargado en cada uno de los equipos cliente.
 1. En el menú Inicio, ejecute el programa Render Farmer en cada equipo.
 El icono del programa Render Farm aparecerá en la bandeja del sistema.

##### Para configurar el Render Farm
{: #configure-the-render-farm}
1.  [Haga clic con el botón derecho](mouse-button-right.html) en el icono y seleccione Restaurar.
1. En la ventana nXt Farmer, en el menú Opciones, haga clic en Ruta y seleccione la ruta a la carpeta Render Farm.

En el equipo con Rhino y Flamingo nXt, defina la carpeta del Zoo en Rhino. En el Menú Herramientas, haga clic en Opciones, defina la ubicación del Farm en la [carpeta de salida de Render Farm](options-flamingo.html#farm-output-folder).

El Render Farm ya está configurado.

## Utilizar el Render Farm
{: #using-the-render-farm-from-flamingo-nxt}
Actualmente, el Farm se puede utilizar de tres maneras para procesar los renderizados en varios equipos: trabajos de renderizado individuales, trabajos por lotes y animaciones.

##### Para comprobar que las estaciones de trabajo cliente responden
Después de iniciar el cliente de Render Farm en todos los equipos cliente:

 1. En cualquiera de los equipos, en el menú Inicio de Windows, haga clic en [Farm Monitor](#render-farm-monitor). 
 1. Los equipos cliente deben aparecer en el cuadro de lista superior.
 1. Cada cliente de Render Farm debe estar incluido en la lista de máquinas.  Su estado tiene que ser activo.

Si hay algún problema, revise la [instalación](#install) y los [temas de configuración](#configure-the-render-farm).


##### Para enviar un trabajo al Render Farm
1. En Rhino, configure el renderizado y la vista como lo haría para un renderizando normal.
1. En el menú Flamingo nXt, haga clic en Iniciar Farm Render.
1. Aparecerá el diálogo [Trabajo de Render Farm](#farm-job).
1. Verifique la opción correcta y pulse Aceptar.


##### Supervisión del Farm
Después de enviar un trabajo al Render Farm, utilice el [Farm Monitor](#render-farm-monitor).

 1. En el equipo principal, en el menú Inicio de Windows, haga clic en [Farm Monitor](#render-farm-monitor).
 1. Un trabajo reciente aparecerá en la lista de trabajos. En el caso de trabajos de gran tamaño, esto puede tardar unos minutos.
 1. El estado del trabajo cambiará a activo.
 1. Después de un periodo de tiempo, los equipos deberían ocuparse de las tareas con la misma fecha.
 1. El porcentaje de compleción aumenta a medida que se completan las tareas.
 1. Compruebe que el estado del trabajo es Completado cuando este ha finalizado.


## Opciones de Trabajo de Render Farm
{: #farm-job}

#### Nombre
{: #job-name}
La fecha y la hora se añaden como prefijo al nombre elegido. En la carpeta compartida de Render Farm se creará una subcarpeta para el trabajo. También se creará una carpeta de salida en la nueva carpeta del trabajo.
Después de completarse cada trabajo, el resultado puede encontrarse en la carpeta de salida del trabajo.

#### Iniciar trabajo
El trabajo puede iniciarse inmediatamente después de enviarse, más tarde o bien manualmente a través de Farm Monitor.

#### Ahora
Inicia el trabajo ahora.

#### Más adelante (Manualmente)
Inicia el trabajo más adelante utilizando el [Farm Monitor](#render-farm-monitor).

#### Después de
Inicia el trabajo en la fecha y hora especificada.

#### Renderizado de pases de restricciones
{: #rendering-constraints}
Define el número de pases necesarios para terminar el trabajo de procesamiento por lotes.  Consulte el tema [Pases](documentproperties-flamingo.html#number-of-passes) para obtener más información.


## Render Farm Monitor
{: #render-farm-monitor}
El Render Farm Monitor es un programa independiente que informa sobre el estado de las estaciones de trabajo cliente y los trabajos en curso del Farm. Los trabajos pueden suspenderse y reiniciarse desde el Farm Monitor y una estación de trabajo cliente puede ser excluida del Render Farm.

Para acceder al Farm Monitor desde Rhino, vaya al menú Flamingo nXt 5.0 > Render Farm > Farm Monitor.

Para acceder al Farm Monitor desde Windows, en el menú Inicio, haga clic en **Todos los programas > nXt Render Farm > Farm Monitor**.

#### Opciones
Clic con el botón derecho en una Máquina o un Trabajo para acceder a las opciones.

#### Actualizar
Actualiza la lista de trabajos.

#### Suspender máquina
Excluye la estación de trabajo del Render Farm.

#### Reanudar máquina
Reanuda la estación para que participe en el Render Farm.

#### Suspender trabajo
Pausa el trabajo especificado.

#### Reanudar trabajo
Reanuda el trabajo especificado.

#### Eliminar trabajo
Elimina el trabajo especificado de la lista.

## Licencias de Render Farm
{: #licensing-the-render-farm-}
La versión gratuita de Render Farm permite que dos equipos de la red (nodos) trabajen simultáneamente. Si desea que más nodos de red se ejecuten simultáneamente, puede comprar una licencia de nodos ilimitados desde  [https://www2.mcneel.com/commerce/accurender/buy-farm.asp](https://www2.mcneel.com/commerce/accurender/buy-farm.asp).

Una vez comprada la licencia y recibido el código del producto, utilice los siguientes procedimientos para validar su licencia del Farm.

##### Para autorizar el nodo
1. Espere que los trabajos activos del Farm terminen antes de iniciar el proceso de validación de la licencia.
1. Guarde el código del producto en un archivo de texto de la ubicación de red para poder cortarlo y pegarlo fácilmente a cada nodo.
1. Si el nodo está activo, en la bandeja del sistema de Windows (en la barra de tareas),  /mouse_button_right.htm');" id="a16" style="position: relative;">haga clic con el botón derecho en el icono Render Farm y luego en **Cerrar**. 
1. Haga clic en el botón Inicio en Windows y luego en Todos los programas**.
En la carpeta nXt Render Farm, haga clic en Autorizar Farm**.
1. En el cuadro de edición, pegue o escriba el código del producto y haga clic en Aceptar**.

##### Para iniciar el nodo
1. Haga clic en el botón Inicio en Windows y luego en Todos los programas**.
En la carpeta nXt Render Farm, haga clic en Render Farmer**.
1.  p('../mouse_button_right.htm');" id="a17" style="position: relative;">Haga clic con el botón derecho en el icono de la bandeja y, en el menú, seleccione **Restaurar**.
1. El el menú Ayuda, haga clic en Acerca de**.
Si el número de versión indica una versión de evaluación, la validación de la licencia no será correcta.
1. Minimice la ventana Render Farmer para devolverla a la bandeja.
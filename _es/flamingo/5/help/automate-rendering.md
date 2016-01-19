---
---

# Renderizado automatizado


## Renderizado por lotes
{: #batch-rendering}
Los trabajos por lotes permiten enviar varios trabajos para renderizar automáticamente. Un trabajo de procesamiento por lotes puede especificar una vista, resolución y número de pases determinados. Los renderizados por lotes pueden iniciarse de manera individual o enviarse al [Render Farm](render-farm.html). Abra la lista de procesamiento por lotes y añada los trabajos. La lista de trabajos por lotes se guardará en el modelo.

##### ¿Dónde puedo encontrar este comando?

 * Menús > Flamingo nXt 5.0 > Más herramientas > Renderizado por lotes

### Diálogo de renderizado por lotes
{: #batch-render}
Empiece añadiendo un trabajo y, a continuación, edite las propiedades para configurar los trabajos por lotes.

#### Añadir
Cada trabajo por lotes se basa en una vista guardada en el modelo.  Haga clic en en Añadir elemento para seleccionar una vista en la lista de vistas del modelo.  Todos los demás elementos del menú se activarán cuando se añada y seleccione un trabajo.

#### Eliminar
Seleccione un trabajo por lotes existente.  A continuación, haga clic en Eliminar para quitar el trabajo de la lista por lotes.

#### Propiedades
Seleccione un trabajo por lotes existente y, a continuación, utilice las Propiedades para definir las [Propiedades del renderizado por lotes](#batch-render-properties). Las Propiedades incluyen el nombre de archivo, la resolución y el número de pases para cada trabajo.

#### Subir
Sube el nombre de la vista un nivel en la lista.

#### Bajar
Baja el nombre de la vista un nivel en la lista.

#### Lista por lotes
{: #batch-list}
Muestra información sobre la lista de vistas a renderizar. Haga doble clic en un trabajo existente para editar las [Propiedades del renderizado por lotes](#batch-render-properties).

#### Estado del renderizado
Muestra información de pases, línea de escaneado y tiempo transcurrido sobre el progreso del procesamiento por lotes.

####  Detener renderizado
Detiene el procesamiento por lotes.

#### Renderizar por lotes localmente
{: #render-batch-locally}
Utiliza solo el equipo actual para renderizar los trabajos por lotes. Las imágenes renderizadas se guardarán en la ubicación especificada en las [Propiedades de renderizado por lotes](#batch-render-properties).

####  Enviar lotes a Render Farm
Envía los trabajos por lotes al [Render Farm](render-farm.html). Los trabajos serán renderizados por todos los clientes del Farm disponibles. Las imágenes renderizadas se guardarán en la carpeta compartida del Farm.

### Propiedades del renderizado por lotes
{: #batch-render-properties}

#### Ventana a renderizar
Muestra la ventana que se renderizará. Consulte [Ficha Renderizao, Ventana a renderizar](render-tab.html#viewtorender).

#### Nombre de archivo
Haga clic en el botón Guardar ![images/saveimageas.png](images/saveimageas.png) y especifique un nombre de archivo para la imagen renderizada.

#### Canal alfa
Guarda la imagen con el canal alfa.  Consulte la opción [Usar fondo de canal alfa](environment-tab.html#alpha) para obtener más información.

#### Usar configuración de documento
{: #rendering-resolution}
La opción predeterminada es utilizar la configuración de resolución del documento actual para renderizar. Si necesita indicar otra resolución, desactive esta casilla y especifique una resolución. Consulte el tema [ficha Renderizado, Resolución](render-tab.html#resolution) para obtener más información.

#### Pases de restricciones de renderizado
{: #rendering-constraints}
Define el número de pases necesarios para terminar el trabajo de procesamiento por lotes.  Consulte el tema [Pases](documentproperties-flamingo.html#number-of-passes) para obtener más información.

<!-- TODO: Flamingo nXt 5 runs from the RDK.  The need to Flamingo Automate render is not clear.  What is needed to run animations with nxt right now? Alpha channel This needs to be investigated. The rest of this section is commented out.-->

<!-- Commented out until automated render can be determined

## Animations
{: #animation}
There are two ways to create animations in Rhino.  Animations can be configured using [Rhino's Animation toolbar](http://docs.mcneel.com/rhino/5/help/en-us/index.htm#commands/animation.htm) or using the [Bongo](http://bongo.rhino3d.com/) animation plugin.

##### To submit an animation job to the render farm
1. Run the [FlamingoNXtAutomateRender](automate-rendering.html#flamingonxtautomaterender) command.
1. In theConfigure Automated Render Commanddialog, select **Render to farm**.
&#160;
Specify theJob name,and click theOKbutton.
&#160;
Set a type of animation from Rhino'sAnimation setuptoolbar. Select RenderFull as the Capture method.
&#160;
Record the animation from theAnimationtoolbar. The render jobs will be sent to Render Farm.
&#160;
When the jobs are finished in Render Farm, run theFlamingoNXtAutomateRendercommand again and select all the jobs in the dialog.
&#160;
Click theCopy selected files to specified output folderbutton and select a folder where all the render images will be copied to.


## FlamingoNXtAutomateRender command
{: #flamingonxtautomaterender}


## Configure Automated Render Command

### Enabled
Redirects the default **Render** command to use the **Render Farm**.

### Use default render dialog
Resets the **Render** command to render directly instead of to the farm.

### Number of render passes to render
Specifies the number of render passes.

### Render to farm
Redirects the **Render** command to render to the farm.

### Job name
Specifies the **Render Farm**  [Job name](automate-rendering.html#job-name).

## Render constraints

### Number of render passes to render
Specifies the [number of passes](documentproperties-flamingo.html#number-of-passes).

### Save alpha channel
Saves the [alpha channel](render-window.html#save-with-alpha-channel) background.
-->
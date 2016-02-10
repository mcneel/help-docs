---
title: Opciones de Flamingo nXt
---


# ![images/options.svg](images/options.svg){: .inline} {{page.title}}
Esta configuración se aplica a la aplicación de Flamingo.  Los cambios realizados aquí repercutirán en el funcionamiento general de Flamingo.

{: #default-decal-link-state}
{% include_relative snippets/snippet-linking.md %}

#### Carpeta compartida de Render Farm
{: #farm-output-folder}
Carpeta compartida de los trabajos de Render Farm. Esta es la ubicación donde se guardan los resultados del Farm. Utilice el icono de la carpeta ![images/folderopen32x32.png](images/folderopen32x32.png){: .inline} para seleccionar una nueva ubicación.

#### Mostrar luces etiquetadas
Utilice esta propiedad para mostrar la dirección de una luz etiquetada.  Esta opción funciona en distribuciones de luz focal y difusa.

#### Vista previa rápida en OpenGL
Cambia las miniaturas del material para que aparezca una miniatura OpenGL antes de devolver el material renderizado.  La respuesta de los materiales puede ser más rápida, pero es posible que la imagen OpenGL no se parezca al material.

#### Guardar archivos de historial nativos cuando se completa el renderizado
De manera predeterminada, Flamingo guardará en la caché la última imagen renderizada por si es necesario recurrir a ella en algún momento.
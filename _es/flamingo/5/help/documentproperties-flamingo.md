---
---


# ![images/options.svg](images/options.svg){:height="75px" width="75px"} Document Properties: Flamingo nXt
Esta configuración se aplica únicamente al modelo actual. Existe una interrelación entre el tiempo necesario para completar el renderizado y la calidad deseada.

#### ¿Dónde puedo encontrar este comando?
<!-- These locations are not correct.  They need to be updated. -->

 1. ![images/icon-render.png](images/icon-render.png)Barras de herramientas de Herramientas de renderizado > ![images/environments.png](images/environments.png) Editor de materiales
 1. ![images/menuicon.png](images/menuicon.png)Menús > Renderizado > Editor de entornos
 1. Comando > EditorDeEntorno

## Materiales
{: #materials}
Utilice estos controles para cambiar rápidamente el modo en que Flamingo renderiza las superficies en un renderizado.  Estos ajustes no cambiarán las asignaciones de materiales en los objetos y las capas, sino que cambiarán el modo en Flamingo produce el color de cada superficie.

#### Utilizar materiales
{: #use-materials}
Renderiza utilizando materiales creados en Flamingo nXt y Rhino. Los objetos que no tienen asignación de material se renderizan en blanco. Si no está activada ninguna de las opciones de Usar materiales o Usar colores de objeto, todos los objetos se renderizarán de color blanco.

#### Usar color de objeto
{: #use-object-color}
Renderiza utilizando los colores asignados a través del objeto de Rhino o el color de capa. Nota : Pueden activarse ambas opciones Usr materiales y Usar color de objeto. En este caso, los objetos que tienen materiales asignados utilizaran esos materiales. Los demás objetos se renderizarán utilizando el color del objeto o de la capa.

#### Canal de brillo
{: #channel}
Los materiales que tengan cualquier nivel de brillo se iluminarán, pero no los demás objetos. (Etiquete el objeto como luz para iluminar los otros objetos.)  Ajusta el brillo en un canal, permitiendo ajustar la luminosidad después del renderizado sin renderizar.

## Rebotes
{: #bounces}
Cuando un rayo entra en una escena, rebotará varias veces antes de ser eliminado.  Si se limita el número de rebotes, el renderizado es mucho más rápido. Pero si los límites son demasiado bajos, los efectos pueden desaparecer o verse de color negro. Estos valores predeterminados sirven para la mayoría de renderizados, pero en ciertos casos puede ser necesario modificarlos. 

#### Reflectante
{: #reflective-bounces}
Determina el número de niveles de reflejos que se permiten. En otras palabras, el número de veces que un rayo de luz se reflejará en los objetos. Un valor de 0 desactiva los reflejos. Los valores altos aumentan el tiempo de renderizado. Aumente este número si hay una vista que mira hacia una superficie reflectante que rebota en un reflejo adyacente y los reflejos empiezan a ser de color negro.

#### Refractivo
{: #refractive-bounces}
Determina el número de niveles de refracciones que se permiten. En otras palabras, el número de veces que un rayo de luz se refractará en los objetos. Un valor de 0 desactiva las refracciones. Los valores altos aumentan el tiempo de renderizado. Aumente este número si hay una vista que muestra muchas capas y se ve de color negro en luegar de transparente.

#### Indirecta
{: #indirect-bounces}
Determina el número de niveles de luz indirecta que se permiten. En otras palabras, el número de veces que un rayo de luz rebotará en los objetos. Un valor de 0 desactiva los reflejos. Los valores altos aumentan el tiempo de renderizado.

## Iluminación indirecta
{: #indirect-settings}
La configuración de iluminación indirecta solo afecta a los rayos que rebotan en una superficie e iliminan a otra superficie.

#### Degradado de color
{: #color-bleed}
El degradado de color controla la cantidad de color transferida en un rebote indirecto de luz de una superficie a otra.  De manera predeterminada, la opción está definida en el valor máximo para aumentar la dinámica en el renderizado.  

#### Reflejos Monte Carlo
{: #monte-carlo}
Los reflejos Monte Carlo en la iluminación indirecta controlan el modo en que Flamingo muestrea la luz indirecta. Cuando la opción está activada, la luz indirecta es muy ruidosa en los primeros pases.  Pero a medida que avanzan los pases, el efecto global de los reflejos Monte Carlo será un efecto indirecto más sutil y potencialmente más detallado. Escenas que dependen en gran medida de la luz indirecta pueden beneficiarse de los reflejos indirectos Monte Carlo.

## Miscelánea

#### Utilizar luces en capas desactivadas
{: #uselightsonlayersthatareoff}
Utiliza luces en capas que están desactivadas y que tienen luces ocultas.

### Restricciones de renderizado
{: #number-of-passes}
{: #time}
{: #render-constraints}
{% include_relative snippets/snippet-renderconstraints.md %}
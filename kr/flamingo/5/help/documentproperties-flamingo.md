---
---


# Document Properties: Flamingo nXt
These settings apply to the current model only. There is a trade-off between the time required to complete a rendering, and the quality desired.

##### To change settings

>On the **Flamingo nXt** menu, click **Document Properties**.

## Materials

### Use materials
Renders using materials created in Flamingo nXt and Rhino materials. Objects that have no material assignment render white.

### Use object color
Renders using the colors assigned through Rhino object or layer color.
 **Note** : Both **Use materials** and **Use object color** can be checked. In this case, objects that have materials assigned will use those materials. Other objects will render using their object or layer color.

## Bounces

### Reflective
Determines how many levels of reflections are permitted; in other words, how many times a light ray will reflect off objects. A setting of 0 disables reflections. Higher values cause longer rendering times.

### Refractive
Determines how many levels of refractions are permitted; in other words, how many times a light ray will refract off objects. A setting of 0 disables refractions. Higher values cause longer rendering times.

### Indirect
Determines how many levels of indirect light are permitted; in other words, how many times an indirect light ray will bounce off objects. A setting of 0 disables reflections. Higher values cause longer rendering times.

## Display in rendered viewports
 **Note** : These settings only affect viewports using Rhino's Rendered display mode. To see these objects in a rendered image, use [Post Effects](render-window.html#postprocessingwireframe).

### Curves
Curves display in rendered viewports.

### Dimensions and text
Dimensions and text display in rendered viewports.

### Isocurves
Isocurves display in rendered viewports.

### Mesh edges
Mesh edges display in rendered viewports.

## Miscellaneous

### Use lights on layers that are off
Uses lights on layers that are turned off and hidden lights.

## Render constraints
{% include_relative snippets/snippet-renderconstraints.md %}

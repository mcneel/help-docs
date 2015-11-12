---
title: Document Properties Flamingo nXt
---


# ![images/options.svg](images/options.svg) {{page.title}}
These settings apply to the current model only. There is a trade-off between the time required to complete a rendering, and the quality desired.

#### Where can I find this command?
<!-- These locations are not correct.  They need to be updated. -->

 1. ![images/icon-render.png](images/icon-render.png)Render Tools Toolbars > ![images/environments.png](images/environments.png) Material Editor
 1. ![images/menuicon.png](images/menuicon.png)Menus > Render Pulldown > Environments Editor
 1. Command > EnvironmentEditor

## Materials
{: #materials}
Use these controls to quickly change how Flamingo renders the surfaces in a rendering.  These settings will not change the material assignments on the objects and layers, but will change how Flamingo produces the color of each surface.

#### Use materials
{: #use-materials}
Renders using materials created in Flamingo nXt and Rhino materials. Objects that have no material assignment render white. If neither the Use materials or the Use Object colors is checked, then all the objects will render white.

#### Use object color
{: #use-object-color}
Renders using the colors assigned through Rhino object or layer color. Note : Both Use materials and Use object color can be checked. In this case, objects that have materials assigned will use those materials. Other objects will render using their object or layer color.

#### Glow Channel
{: #channel}
Materials that contain any level of glow will light up, but will not illuminate other objects. (Tag the object as a light to illuminate other objects.)  Set the Glow on a Channel, allowing the brightness of the glow to be adjusted after rendering without re-rendering.

## Bounces
{: #bounces}
When a ray enters a scene it will bounce a few times before being eliminated.  Limiting the number of bounces allows the render to render much faster. But if the limits are two low, then effects can be missing or go black.  The defaults here are very good for the majority of renderings, but in certain cases may need to be changed.

#### Reflective
{: #reflective-bounces}
Determines how many levels of reflections are permitted; in other words, how many times a light ray will reflect off objects. A setting of 0 disables reflections. Higher values cause longer rendering times. Increase this number of there is a view that is looking at a reflective surface that bounces off an adjacent reflective and the reflections start to go completely black.

#### Refractive
{: #refractive-bounces}
Determines how many levels of refractions are permitted; in other words, how many times a light ray will refract off objects. A setting of 0 disables refractions. Higher values cause longer rendering times. Increase this number of there is a view that looks through many layers and ultimately looks black and not look transparent.

#### Indirect
{: #indirect-bounces}
Determines how many levels of indirect light are permitted; in other words, how many times an indirect light ray will bounce off objects. A setting of 0 disables reflections. Higher values cause longer rendering times.

## Indirect lighting
{: #indirect-settings}
The indirect lighting settings only effect the rays that bounce off one surface an carry light to another surface.

#### Color Bleed
{: #color-bleed}
Color bleed controls the amount of color transferred in a indirect bounce of light from one surface to another.  By default this is set to the maximum value to increase dynamics in the rendering.  

#### Monte Carlo Reflections
{: #monte-carlo}
Monte Carlo in indirect lighting controls how Flamingo samples indirect light. When activated, the indirect light will become very noisy in the early passes.  But over all, as the passes progress, the overall effect of Monte Carlo indirect will be a more subtle and potentially more detail indirect effect. Scenes that rely heavily on indirect light may benefit from Mote Carlo indirection reflections.

## Miscellaneous

#### Use lights on layers that are off
{: #uselightsonlayersthatareoff}
Uses lights on layers that are turned off and hidden lights.

### Render constraints
{: #number-of-passes}
{: #time}
{: #render-constraints}
{% include_relative snippets/snippet-renderconstraints.md %}

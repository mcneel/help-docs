---
title: Object Properties
---

#  ![images/properties.svg](images/properties.svg){: .inline} {{page.title}}
Flamingo nXt object properties only affect the way objects are rendered in Flamingo nXt.

### ![images/materialtab.png](images/materialtab.png){: .inline} Material Source
{: #material-source}
A material can be assigned to layers, blocks, and objects.  For details on Assigning material see the [Material Assignments](material_assignment.html) topic. If the material is set to ByObject, then the material properties are also displayed in this dialog.  For more details on editing a material, see [Material Properties](material-type-simple.html).

### ![images/apply-cylindrical-mapping.png](images/apply-cylindrical-mapping.png){: .inline} Texture mapping
{: #texture-mapping}
Mapping controls how a material is located (mapped) on a particular object. The method used to assign a material whether to a layer or object does not affect mapping. For materials that have no noticeable pattern, it is normally not necessary to control the mapping. Use mapping where the material is directional or has an obvious pattern. Even in these cases, the default mapping may be adequate. Mapping remains with the object and follows it if it is moved, rotated, or scaled. For details on the mapping types see the [Texture Mapping](http://docs.mcneel.com/rhino/5/help/en-us/index.htm#properties/texturemapping.htm) topic.

![images/mapping-cube.png](images/mapping-cube.png) ![images/mapping-planar.png](images/mapping-planar.png)
*Two different mapping directions*

### ![images/decalproperties.png](images/decalproperties.png){: .inline} Decals
{: #decals}
Decals are non-tiling image maps that apply directly to objects instead of indirectly using a material. Use decals to modify a limited part of an object's color, reflectivity, or bumps. See the [Rhino Decals](http://docs.mcneel.com/rhino/5/help/en-us/index.htm#properties/decal.htm) for details on creating and placing decals.

![images/freshmilk.png](images/freshmilk.png) ![images/decal-planar-001.png](images/decal-planar-001.png)
![images/cylindricaldecal-002.png](images/cylindricaldecal-002.png) ![images/uvmapdecal-00.png](images/uvmapdecal-00.png)
*Four different decal examples*

### ![images/apply-edge-softening.png](images/apply-edge-softening.png){: .inline} Custom Meshes
{: #custom-meshes}
Several custom mesh modifiers can be used in Rhino to detail rendered models. Use these modifiers to round edges, add panel shut lines, and create cables from curves.

For more details go to the topics below:

* [Edge softening](http://docs.mcneel.com/rhino/5/help/en-us/index.htm#commands/applyedgesoftening.htm)
* [Curve piping](http://docs.mcneel.com/rhino/5/help/en-us/index.htm#commands/applycurvepiping.htm)
* [Shut Lining](http://docs.mcneel.com/rhino/5/help/en-us/index.htm#commands/applyshutlining.htm)
* [Displacement](http://docs.mcneel.com/rhino/5/help/en-us/index.htm#commands/applydisplacement.htm)

### ![images/object-flamingo.PNG](images/object-flamingo.PNG){: .inline} Flamingo Properties
{: #flamingo-properties}

#### Alpha channel
{: #alpha-channel}
Makes the object invisible. Shadows cast by and on the object are rendered. The image can then be overlaid on another image and the shadows will show in the composite image.

![images/building.png](images/building.png)
In the example above, a few simple planar surfaces that match the image were created to catch shadows cast on the building by the trees. The planes were tagged with the Alpha channel property so when they were rendered, they were invisible, but still displayed the shadows. This partially transparent image was then overlaid onto the image.

#### Caustics
{: #caustics}
The light rays reflected or refracted by a curved object or the projection of those rays on another surface. Caustics should be used in very specific situations. Caustics are only rendered with the [Path Tracer](render-tab.html#path-tracer) engine or the [Hybrid](render-tab.html#hybrid) render engine.  Caustic calculations take many passes to converge. See [Wikipedia article: Caustic (optics)](http://en.wikipedia.org/wiki/Caustic_(optics)) for more information.

![images/kaustik.png](images/kaustik.png)
*Caustics produced by a glass of water.*

![images/caustics-001.png](images/caustics-001.png)
*Without caustics (left), and with caustics (right).*

#### Thin
{: #thin}
A space-enclosing, transparent object is normally treated as a solid for transparent refraction. Setting the Thin property means that each surface will be treated as a two-sided object for refraction. This is the setting to use if single surfaces such as glass are used for architectural models.

![images/thin.png](images/thin.png) ![images/thinoff.png](images/thinoff.png)
*Base Rhino model (left), Normal (middle) and Thin (right).*

#### Daylight portal
{: #daylight-portal}
A daylight portal is an opening for [Sun and Sky lighting](lighting-tab.html#interior-daylight) for an interior rendering. A Daylight portal pulls sun, sky, and ground light into an interior space in a natural way. Daylight portals only have an effect when the [Sun](sun-and-sky-tabs.html#sun) is turned on. When the lighting scheme is set to [Interior daylight](lighting-tab.html#interior-daylight), all transparent surfaces act as daylight portals automatically. It is only when the lighting scheme is set to Studio or Exterior daylight and you still want to bring outside sun and sky light into an interior space that you must manually tag the windows as daylight portals.

![images/daylightportal-001.png](images/daylightportal-001.png)
*With daylight portal (left), without daylight portal (right).*

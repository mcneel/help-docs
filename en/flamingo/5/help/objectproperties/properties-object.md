---
layout: toc-page
---


# <img src="../image/properties.png"/>Object Properties
{: .toc-title }

Flamingo nXt object properties only affect the way objects are rendered in Flamingo nXt.


## Alpha channel
{: .toc-header }

Makes the object invisible. Shadows cast by and on the object are rendered. The image can then be overlaid on another image and the shadows will show in the composite image.

<img src="building.png"/>

A few simple planar surfaces that match the image were created in order to catch shadows cast on the building by the &quot;trees.&quot; The planes were tagged with the Alpha channel property so when they were rendered, they were invisible, but still displayed the shadows. This partially transparent image was then overlaid onto the image.


## Caustics
{: .toc-header }

The light rays reflected or refracted by a curved object or the projection of those rays on another surface. See [Wikipedia article: Caustic (optics)](http://en.wikipedia.org/wiki/Caustic_(optics)) for more information.

<img src="kaustik.png"/>


 *Caustics produced by a glass of water.* 
<img src="caustics-001.png"/>


 *Without caustics (left), and with caustics (right).* 

## Thin
{: .toc-header }

A space-enclosing, transparent object is normally treated as a solid for transparent refraction. Setting the **Thin** property means that each surface will be treated as a two-sided object for refraction.

<img src="thin.png"/>


 *Box and torus.* 
<img src="thinoff.png"/>Normal (left) and Thin (right).


## Daylight portal
{: .toc-header }

A daylight portal is an opening for [Sun and Sky lighting](../lighting/lighting-tab.html#interior-daylight) for an interior rendering.

A Daylight portal pulls sun, sky, and ground light into an interior space in a natural way. Daylight portals only have an effect when the [Sun](..\lighting\sun-and-sky-tabs.html#sun) is turned on.

When the lighting scheme is set to [Interior daylight](../lighting/lighting-tab.html#interior-daylight), all transparent surfaces act as daylight portals automatically. It is only when the lighting scheme is set to Studio or Exterior daylight and you still want to bring outside sun and sky light into an interior space that you must manually tag the windows as daylight portals.

<img src="daylightportal-001.png"/>


 *With daylight portal (left), without daylight portal (right).* 

## Mapping
{: .toc-header }

Whether materials are assigned to a layer or object, mapping controls how that material is located (mapped) on a particular object. For materials that have no noticeable pattern, it is normally not necessary to control the mapping. Use mapping where the material is directional or has an obvious pattern. Even in these cases, the default mapping may be adequate. Mapping remains with the object and follows it if it is moved, rotated, or scaled.

One common example is a Wood material on objects arranged in a circular pattern like spokes. The Wood may not be oriented correctly on some of the spokes. In this case, manually position and orient the material on the object. Changing the mapping does not alter the definition of a material, only the direction it is applied.

<img src="mapping-001.png"/>Default mapping (left) and mapping orientation set per object (right).

Five mapping types position a material on an object: [Planar](#planar), [Cube](#cube), [Cylindrical](#cylindrical), and [Spherical](#spherical), and [Surface](properties-object.html#surface-mapping). The [Default](#defaultmapping) setting maps materials the same as cube, but the origin and orientation are not adjustable.

Once a specific mapping type has been set, the object can be rotated, moved, and otherwise edited, and the orientation of the material will follow the object. When specifying points on an object, it is important to use object snaps or set the construction plane to the object before mapping the material.


### Place/Edit Placement
{: .toc-subheader }

Sets the origin point and rotation direction of the material mapping for the object. This controls where the bitmap image starts.

A different control icon activates for each mapping type. For cylindrical and spherical mapping, it is usually important to set the origin at the center of the shape.


### Default
{: .toc-subheader }

Maps patterns orthographically to the world axes. The pattern begins at world 0,0,0. the origin or orientation cannot be changed. This means that the pattern may begin or end somewhere outside the boundaries of the object.

<img src="mapping-cube.png"/>


### Planar
{: .toc-subheader }

Mapping will not change orientation as the sides of the object change. If&#160;the object has faces that are perpendicular to the mapping plane, the material appears to be &quot;extruded&quot; or &quot;projected.&quot; In some cases, the **Planar** mapping can result in the pattern switching orientation suddenly in areas of high curvature.

<img src="mapping-planar.png"/>


### Cube
{: .toc-subheader }

Maps patterns orthographically to the object. The origin and orientation of the material mapping can be changed.

<img src="mapping-cube.png"/>


### Cylindrical
{: .toc-subheader }

Maps patterns as if they were applied to a cylinder centered at the specified origin. The center, rotation, and axis of the mapping can be changed.

Use the material size or override the material size and specify the number of tiles in the u-direction (the circular direction) and a height.

<img src="mapping-cylindrical.png"/>


### Spherical
{: .toc-subheader }

Maps patterns as if they were applied to a sphere centered at the specified origin.

<img src="mapping-spherical.png"/>


### Surface
{: .toc-subheader }

The material does not tile, but only one instance of the material is placed on each surface regardless of the material size.

<img src="mapping-surface.png"/>


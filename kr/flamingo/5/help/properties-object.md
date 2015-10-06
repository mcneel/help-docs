---
---


# Object Properties
Flamingo nXt object properties only affect the way objects are rendered in Flamingo nXt.

## Alpha channel
Makes the object invisible. Shadows cast by and on the object are rendered. The image can then be overlaid on another image and the shadows will show in the composite image.
![images/building.png](images/building.png)
A few simple planar surfaces that match the image were created in order to catch shadows cast on the building by the &quot;trees.&quot; The planes were tagged with the Alpha channel property so when they were rendered, they were invisible, but still displayed the shadows. This partially transparent image was then overlaid onto the image.

## Caustics
The light rays reflected or refracted by a curved object or the projection of those rays on another surface. See [Wikipedia article: Caustic (optics)](http://en.wikipedia.org/wiki/Caustic_(optics)) for more information.
![images/kaustik.png](images/kaustik.png)
*Caustics produced by a glass of water.*
![images/caustics-001.png](images/caustics-001.png)
*Without caustics (left), and with caustics (right).*

## Thin
A space-enclosing, transparent object is normally treated as a solid for transparent refraction. Setting the **Thin** property means that each surface will be treated as a two-sided object for refraction.
![images/thin.png](images/thin.png)
*Box and torus.*
![images/thinoff.png](images/thinoff.png)Normal (left) and Thin (right).

## Daylight portal
A daylight portal is an opening for [Sun and Sky lighting](lighting-tab.html#interior-daylight) for an interior rendering.
A Daylight portal pulls sun, sky, and ground light into an interior space in a natural way. Daylight portals only have an effect when the [Sun](sun-and-sky-tabs.html#sun) is turned on.
When the lighting scheme is set to [Interior daylight](lighting-tab.html#interior-daylight), all transparent surfaces act as daylight portals automatically. It is only when the lighting scheme is set to Studio or Exterior daylight and you still want to bring outside sun and sky light into an interior space that you must manually tag the windows as daylight portals.
![images/daylightportal-001.png](images/daylightportal-001.png)
*With daylight portal (left), without daylight portal (right).*

## Mapping
Whether materials are assigned to a layer or object, mapping controls how that material is located (mapped) on a particular object. For materials that have no noticeable pattern, it is normally not necessary to control the mapping. Use mapping where the material is directional or has an obvious pattern. Even in these cases, the default mapping may be adequate. Mapping remains with the object and follows it if it is moved, rotated, or scaled.
One common example is a Wood material on objects arranged in a circular pattern like spokes. The Wood may not be oriented correctly on some of the spokes. In this case, manually position and orient the material on the object. Changing the mapping does not alter the definition of a material, only the direction it is applied.
![images/mapping-001.png](images/mapping-001.png)Default mapping (left) and mapping orientation set per object (right).
Five mapping types position a material on an object: [Planar](#planar), [Cube](#cube), [Cylindrical](#cylindrical), and [Spherical](#spherical), and [Surface](properties-object.html#surface-mapping). The [Default](#defaultmapping) setting maps materials the same as cube, but the origin and orientation are not adjustable.
Once a specific mapping type has been set, the object can be rotated, moved, and otherwise edited, and the orientation of the material will follow the object. When specifying points on an object, it is important to use object snaps or set the construction plane to the object before mapping the material.

### Place/Edit Placement
Sets the origin point and rotation direction of the material mapping for the object. This controls where the bitmap image starts.
A different control icon activates for each mapping type. For cylindrical and spherical mapping, it is usually important to set the origin at the center of the shape.

### Default
Maps patterns orthographically to the world axes. The pattern begins at world 0,0,0. the origin or orientation cannot be changed. This means that the pattern may begin or end somewhere outside the boundaries of the object.
![images/mapping-cube.png](images/mapping-cube.png)

### Planar
Mapping will not change orientation as the sides of the object change. If&#160;the object has faces that are perpendicular to the mapping plane, the material appears to be &quot;extruded&quot; or &quot;projected.&quot; In some cases, the **Planar** mapping can result in the pattern switching orientation suddenly in areas of high curvature.
![images/mapping-planar.png](images/mapping-planar.png)

### Cube
Maps patterns orthographically to the object. The origin and orientation of the material mapping can be changed.
![images/mapping-cube.png](images/mapping-cube.png)

### Cylindrical
Maps patterns as if they were applied to a cylinder centered at the specified origin. The center, rotation, and axis of the mapping can be changed.
Use the material size or override the material size and specify the number of tiles in the u-direction (the circular direction) and a height.
![images/mapping-cylindrical.png](images/mapping-cylindrical.png)

### Spherical
Maps patterns as if they were applied to a sphere centered at the specified origin.
![images/mapping-spherical.png](images/mapping-spherical.png)

### Surface
The material does not tile, but only one instance of the material is placed on each surface regardless of the material size.
![images/mapping-surface.png](images/mapping-surface.png)


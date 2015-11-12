---
title: Options Flamingo nXt
---


# ![images/options.svg](images/options.svg) {{page.title}}
These settings apply to the Flamingo application.  Making changes here will change how Flamingo runs all the time.

{: #default-decal-link-state}
{% include_relative snippets/snippet-linking.md %}

#### Farm shared folder
{: #farm-output-folder}
The shared folder for render farm jobs. This is also the location that the farm will output its results. Use the Folder icon ![images/folderopen32x32.png](images/folderopen32x32.png) to select a new location

#### Display Tagged Lights
Use this property to Display the direction of a tagged light.  This works on spot and diffuse light distributions.

#### Quick preview in OpenGL
This will change the material thumbnails to start with an OpenGL thumbnail before the rendered material is returned.  This can lead to faster responses on material, but the OpenGL image may not be close to the actual material.

#### Save native history files when rendering is complete
By default Flamingo will cache the last image rendered in there is a need to return to it in the future.

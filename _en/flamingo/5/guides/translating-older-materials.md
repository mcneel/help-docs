---
title: Working with older NXT Materials
---

# {{page.title}}
Flamingo nXt 5 uses the built in Rhino RDK material (.rmat) format.  The previous Flamingo nXt used an earlier .armaterial format.  Flamingo nXt 5 translates and manages older Flamingo materials in very specific ways.  Understanding how the materials interact can be helpful when working with old models and materials.

The new Flamingo nXt 5 uses the built in Rhino RDK materials.  These RDK material have a file extension of (.rmat).  The previous Flamingo nXt used it's own material format with the file extension of (.armaterial).  These are two different material definitions and it is important to understand Flamingo nXt 5 materials and Flamingo nXt do not share the material definition.  So, if you change a material in Flamingo nXt 5, the change will not be reflected in Flamingo nXt.  It is also true that changes in nXt will not be reflected in nXt 5.  There is limited but useful interaction between the two versions.  Understanding this interaction is important when managing older files.

There are three common cases older materials are used.

1. Opening an old model with previous materials
1. Trying to use the old version of Flamingo with the new version, interactively.
1. Assigning old materials to newer models


## Opening old models
{: #opening-old}
Flamingo nXt 5 will translate older materials to newer material only one time within a model.  This will be the first time Flamingo nXt 5 sees the model. After that point, Flamingo nXt 5 and the Flamingo nXt will maintain separate material definitions.

### Layer assignments of materials
Rhino layers contain only one layer name.

## Switching between Flamingo nXt and Nxt 5 interactively
{: #switch-versions}
![images/getting_started001.png](images/getting_started001.png){: .float-img-right} For your first rendering of the model, click on the render button. Your image should look like the one on the right. nXt works differently than previous versions of Flamingo. A new model will include a default HDRI light set-up.  New models will use a white default material for all objects. Also, you may notice that shadows start out very sharp and linear. With each pass, the shadows will get softer as they blend together. There are many other effects that will also improve with each render pass.

## Assigning old materials to new models
{: #using-materials}

---
layout: toc-page
---


# Options: Flamingo nXt
 


## Library folders
 

Additional folder locations to scan when creating the list of available material and plant libraries. By default, this list is empty.


## File search paths
 

The folders are not searched for libraries, but rather for support files, such as bitmaps, plant textures, in addition to the **Library folders**. The folders are searched in order they appear in the list. The current folder containing the .3DM file is searched first.


#### Add a new folder

1.

Under **Library folders**, click the **New** icon.

2.

In the **Browse for Folder** dialog box, select a folder.


#### Delete a folder

 * Select a folder name from the list, and click the Delete icon.

#### To move a folder up in the list

 * Select a folder name from the list, and click the Move Up icon.

#### To move a folder down in the list

 * Select a folder name from the list, and click the Move Down icon.

### Allow modeling while rendering
 

Lets you keep working on the model while rendering is underway.


### Insert plants as point clouds
 

Uses a point cloud to represent a plant. Using point clouds generally make smaller file sizes.

Otherwise, plants are represented by mesh objects.


 *<img src="treespointcloudormesh.png"/>Trees as point cloud (left) and mesh (right).* 

## Default image link state
 


### Linking options
 

Specifies how the image file will be linked to materials.


#### Linked

Creates a link to the image file. The file must be present on the local disk.


#### Embedded

Embeds the image information in the current file.


#### Linked and embedded

If the bitmap is found on the disk before rendering, the external file is used. If the image cannot be found on the disk, the internal definition will be used.

 **Note:** The images are cached for the life of the document.


#### To see changes in linked or linked and embedded files

 * On the **Flamingo nXt** menu, click **Utilities** and then click **Clear bitmap cache**.

### Decal drag transparency
 

Specifies how transparent a decal is while it is being dragged during placement.


### Default material preview size
 

Specifies the default size of the material preview sphere in the [Material Editor](../materials/advanced-material-properties-main.html#preview).


### Farm output folder
 

The output folder for render farm jobs.


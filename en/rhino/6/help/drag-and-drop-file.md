---
---

{: #kanchor2501}{: #kanchor2502}{: #kanchor2503}{: #kanchor2504}{: #kanchor2505}{: #kanchor2506}{: #kanchor2507}{: #kanchor2508}{: #kanchor2509}
# Drag and drop a file into Rhino
Model files
Drag any supported geometry [file format](-index-of-import-export-file-types.html) from Windows Explorer, Rhino will:
 [Open](open.html) the file. [Import](import.html) the file into the current model. [Insert](insert.html) the file as a block, group, or geometry.Attach the file to the current [worksession](worksession.html) .You can also start Rhino by dragging a text file with the .txt extension over a Rhino shortcut.This starts Rhino and runs the text file using theReadCommandFilecommand.Image files
Drag any supported image file type that makes textures (bmp, png, jpeg, hdr, exr).Drag and drop on an object
If the object has a material assignment, the material diffuse texture is changed to the dragged texture.Of the object has no material assignment, a new material is created with the image as the texture in the diffuse slot.Drag and drop to a free space
A dialog box offers options.Image Options
Picture
Runs the [Picture](picture.html) command with the image as the option.
Wallpaper
Runs [-ViewportProperties, Wallpaper, Set](viewport.html#wallpaper) with the image as the option.
Material
Creates a new material using the image as a texture for the color. The name of the image is used as the material name.
Environment
Either sets the current environment's texture to the dropped texture or creates a new basic environment with that texture and sets it current.
Texture Palette
Creates a new texture using the image.
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](drag-and-drop-file.html) 


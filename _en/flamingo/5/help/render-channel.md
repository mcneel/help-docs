---
---


# Channel
{: #channel}
Specifies one of eight channels for the light.
This controls the number of channels for multi-channel rendering.
This feature lets you adjust the lighting in your rendered image in real time, after the rendering has been produced. Each light source in the drawing, including the sun and sky, can be assigned to a channel. Once this image is rendered, each channel can be individually scaled either in the Render Window before saving or it can be saved to an .nXtImage file for later editing. Using this capability, you can produce day and night interiors with a single rendering.
Click to play video clip.
The following conditions are necessary to produce and manipulate a multi-channel image:

>All participating lights must be on.
>Each light source must be assigned a channel. By default, Sun and Sky are set to channel 0.
>The only saved format that preserves this channel information is the .nXtImage format. Lighting can be adjusted there and then the image saved to a bitmap format.

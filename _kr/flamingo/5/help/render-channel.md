---
title: 채널
---

# ![images/render.svg](images/render.svg) {{page.title}}
{: #channel}
A very useful feature in Flamingo nXt 5 is the ability to set lights on one of eight channels. Each light source in the drawing, including the sun and sky, can be assigned to a channel. At render time, the light from each channel is put on its own layer.  Then after the rendering is finished, the channels can be adjusted in strength.  The change is real time without the need to re-render.  

채널이 매우 효과적인 경우:

* Trying to balance an HDRI Environment and the Sunlight.  Not all HDRI environments are calibrated.  It is useful to set the HDRi Sky on one channel and the Sun on another.  Then adjust the relative strength of the Sky light vs the sun after rendering.
* Studio renderings that use a key, fill, and backlight setup. Set each light on a different channel, then adjust their strength real-time in the rendering using channels.
* When using different banks of lights in an exterior or interior rendering.  Each bank of lights can be set on a channel and effectively have their own dimmer to control their strength.
* Rendering with all the lights on, then turning off and on certain lights. No need to render an interior to create a night shot and a daytime rendering.

Once this image is rendered, each channel can be individually scaled either in the Render Window before saving or it can be saved to an .nXtImage file for later editing.

Use channels to adjust the strength of lights relative to each other, not to brighten the whole image.  If you need to brighten the whole image at once, use the Adjust Image controls.

<video id="channelsvideo" src="images/flamingo-lights-onoff.mp4" poster="images/flamingo-lights-onoff.jpg" controls preload></video>
*Click to play video clip.*

다중 채널 이미지를 만들고 조작하려면 다음의 조건들이 필요합니다.

 1. 참여하고 있는 모든 조명은 켜져 있어야 합니다.
 2. Each light source must be assigned to a channel. By default, Sun and Sky are set to channel 0, artificial lights are set to 1.
 3. Immediately after rendering, use the Channel controls in the render window.
 3. The only saved format that preserves this channel information is the .nXtImage format. Lighting can be adjusted there and then the image is saved to a bitmap format.

## 채널 설정
{: setting}
The first step in setting up a muti-channel rendering is to set each light to channel. The channel number is usually set in each light property.  For information on setting specific lights to a channel see:

>[태양 채널](sun-and-sky-tabs.html#sun-channel)
>[하늘 채널](sun-and-sky-tabs.html#sky-channel)
>[인공 조명 채널](lights-tab.html#channel)
>[Material Glow](documentproperties-flamingo.html#channel)

Any number of lights can be grouped onto the same light channel.  The channel adjustment is a multiplier. Lights on the same channel will keep their relative strengths to each other while being adjusted.

## 채널 조정
{: adjusting}
Lighting channels can be adjusted immediately after rendering, or in the Flamingo image editor if the rendering is saved as an nXtImage file.  Channels can be adjusted while Flamingo continues to render, but we recommend that you stop the rendering before making major adjustments.

#### Flamingo 조명 제어는 어디에 있습니까?
The channel controls are found on the Flamingo nXt tab in the [render window](render-window.html) under Channels.

There are eight channel controls 0-7. Only the channels that have lights on them will activate.

![images/channel-slider.png](images/channel-slider.png)
Each channel has a slider and a spinner value.  The spinner value represents the maximum value of the slider. If the slider is all the way to right, then the full value of the spinner is used to multiply the lighting amounts on that channel.  It follows that the slider at 50% will multiply all the lighting on that channel layer by half the spinner amount.  A slider slid all the way to the left will turn off all the lighting on that channel.

The value of the spinner can be very important.  Because Sun and Sky can be many times brighter then artificial lights, the spinner value on artificial lights  might need to be increased to 20 or 50 to see any difference.

After adjusting the channels correctly, then save the image as a JPG or PNG file as the final rendering.

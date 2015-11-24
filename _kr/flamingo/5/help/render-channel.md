---
title: 채널
---

# ![images/render.svg](images/render.svg) {{page.title}}
{: #channel}
8개의 채널 중 하나의 채널에서 조명을 설정할 수 있는 능력은 Flamingo nXt 5의 매우 유용한 기능입니다. 도면에서 태양과 하늘을 비롯한 각각의 광원은 하나의 채널에 지정할 수 있습니다. 렌더링할 때 각 채널의 빛은 그 자체의 레이어에 있게 됩니다. 렌더링을 마친 후에 해당 채널의 세기를 조정할 수 있습니다. 다시 렌더링할 필요 없이, 실시간으로 변경됩니다.  

채널이 매우 효과적인 경우:

* Trying to balance an HDRI Environment and the Sunlight.  Not all HDRI environments are calibrated.  It is useful to set the HDRi Sky on one channel and the Sun on another.  Then adjust the relative strength of the Sky light vs the sun after rendering.
* Studio renderings that use a key, fill, and backlight setup. Set each light on a different channel, then adjust their strength real-time in the rendering using channels.
* When using different banks of lights in an exterior or interior rendering.  Each bank of lights can be set on a channel and effectively have their own dimmer to control their strength.
* Rendering with all the lights on, then turning off and on certain lights. No need to render an interior to create a night shot and a daytime rendering.

Once this image is rendered, each channel can be individually scaled either in the Render Window before saving or it can be saved to an .nXtImage file for later editing.

Use channels to adjust the strength of lights relative to each other, not to brighten the whole image.  If you need to brighten the whole image at once, use the Adjust Image controls.

<video id="channelsvideo" src="images/flamingo-lights-onoff.mp4" poster="images/flamingo-lights-onoff.jpg" controls preload></video>
*동영상을 재생하려면 클릭합니다.*

다중 채널 이미지를 만들고 조작하려면 다음의 조건들이 필요합니다.

 1. 참여하고 있는 모든 조명은 켜져 있어야 합니다.
 2. 각각의 광원이 채널에 지정되어 있어야 합니다. 기본적으로 태양과 하늘은 채널 0에, 인공적인 조명은 채널 1에 설정됩니다.
 3. 렌더링 직후에 렌더링 창의 채널 제어를 사용합니다.
 3. nXtImage 형식에서만 채널 정보가 저장됩니다. 이 파일 형식에서 조명을 조정하고 이미지를 비트맵 형식으로 저장할 수 있습니다.

## 채널 설정
{: setting}
첫 번째 단계는 각각의 조명을 채널에 지정하기 위해 다중 채널 렌더링을 설정하는 것입니다. 채널 번호는 일반적으로 각 조명 속성에 지정됩니다. 특정 조명을 채널에 설정하는 방법에 대한 안내는 다음 링크를 참조하세요:

>[태양 채널](sun-and-sky-tabs.html#sun-channel)
>[하늘 채널](sun-and-sky-tabs.html#sky-channel)
>[인공 조명 채널](lights-tab.html#channel)
>[재질 글로우](documentproperties-flamingo.html#channel)

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

---
---

{: #kanchor2621}{: #kanchor2622}{: #kanchor2623}{: #kanchor2624}{: #kanchor2625}{: #kanchor2626}{: #kanchor2627}
# Annotation
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/documentproperties.png](images/documentproperties.png) [File](file-toolbar.html)  [Properties](properties-toolbar.html)  [Standard](standard-toolbar.html) 
Menus
File
Properties
Annotation properties manage settings for text, dimensions, and leaders for the current model.
Annotation Scaling
Enable scaling of text, dimensions and leaders
When theEnable scalingoption is checked, [text](text.html), [dimension text](dimensions-style.html#text-height), and [leader text](dimensions-style.html#text-height) in a [layout detail](layout.html) get their scale factor from the Detail display scale.
When theEnable scalingoption is NOT checked, [text](text.html), [dimension text](dimensions-style.html#text-height), and [leader text](dimensions-style.html#text-height) in a [layout detail](layout.html) AND in model space, get their scale factor from the named dimension style they belong to.
When theEnable scalingoption disabled, text height is multiplied by the [scale](detail.html#detail-scale) of the detail.
Model space text scale
The model space text scale number is used only for scaling Text objects in model space. This allows text to be scaled for printing, but still be legible in model space.
Model space dimension scale is controlled in each dimension style.
There is no separate annotation scale control for dimensions. Set the scale in [Dimension Style Document Properties](dimensions-style.html).
Enable hatch scaling
When viewed in a [layout detail](layout.html), a hatch pattern in model space uses its [pattern scale](hatch.html#pattern-scale) regardless of the [scale](detail.html#detail-scale) of the detail.
When disabled, the [pattern scale](hatch.html#pattern-scale) is multiplied by the [scale](detail.html#detail-scale) of the detail.
Model space hatch scale
A multiplier used to scale the hatch pattern when in model space. This allows hatch to be scaled for printing, but still be legible in model space.
Model space linetype scale
Controls the scale used to display linetypes in the viewports. TheScalesetting does not affect printing. If you have a dashed pattern (for example) defined as 1/2" line followed by 1/2" break, repeated; that is how it will appear on paper, when printed, without regard to print scale.
See also
 [Use drafting tools](sak-drafting.html) 
 [Manage document properties](sak-documentproperties.html) 
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](annotation.html) 


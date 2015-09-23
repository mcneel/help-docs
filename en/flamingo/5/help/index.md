---
layout: toc-page
---


# All Flamingo Topics
 


## [Environment](environment/environment-tab.html)
 

 [Environmenttest](environment/environment-tab.html) 


## Lighting
 

### LinearLight
 

[Lighting: Advanced](lighting/lighting-advanced-tab.html)
  

 [Lighting](lighting/lighting-tab.html) 

 [Lights](lighting\lights-tab.html) 

 [Sky](lighting/sun-and-sky-tabs.html) 

 [Studio Lighting Basics](lighting/studio-lighting-basics.html) 

 [Sun and Sky](lighting/sun-and-sky-tabs.html) 


## Materials
 

 [Advanced Material Properties: Main](materials/advanced-material-properties-main.html) 

 [Advanced Material Properties: Textures](materials/advanced-material-properties-textures.html) 

 [Advanced Material Properties: Transparency](materials/advanced-material-properties-transparency.html) 

 [Assign Materials](materials\materials-tab.html) 

 [Materials: Textured](materials/texture-properties-main.html) 

 [Simple Material Properties](materials\simple-material-properties.html) 

 [Texture Properties: Main](materials/texture-properties-main.html) 

 [Texture Set Materials](materials/texture-set-materials.html) 


## Object Properties
 

 [Decal Properties](objectproperties\properties-decal.html) 

 [Object properties](objectproperties\properties-object.html) 


## Plants
 

 [Plants](plants/plants.html) 


## Render
 

 [Automate Rendering](render/automate-rendering.html) 

 [Document Properties: Flamingo nXt](render/documentproperties-flamingo.html) 

 [Image Editor](render\image-editor.html) 

 [Render tab](render/render-tab.html) 

 [Render Window](render\render-window.html) 

## Commands
 

 [Flamingo Command List](general\flamingo-command-list.html) 

## Misc
 

 [Enter CD Key](general/enter-cd-key.html) 

 [Options: Flamingo nXt](general\options-flamingo.html) 

 [Progress Form](general/progress-form.html) 

 [Select color](general\select-color.html) 

 [Welcome](general\welcome.html) 

## TODO List
 

#### Commands
 

<div class="trigger">
  <ul>
  {% for page in site.pages %}
    {% if page.TODO == 1 %}
	    {% if page.COMMAND == 1 %}
	       <li>
    	     <a class="page-link" href="{{ page.url | prepend: site.baseurl }}">{{ page.title }}</a>
           </li>
        {% endif %}
    {% endif %}
  {% endfor %}
  </ul>
</div>

&#160;

&#160;

&#160;


---
layout: fullwidth-page
---

# Getting Started with Flamingo nXt 5®
 
## Installation

Flamingo 5 B�ta ne peut �tre install� que si une version pr�c�dente de Flamingo nXt est d�j� install�e.
Rhino 5 Version r�vis�e 12 doit �tre install� pour utiliser Flamingo nXt 5.
Apr�s avoir t�l�charg� et lanc� le fichier RHI, lancez Rhino.
Notes pour le d�marrage

This version of Flamingo features an interface which is integrated with the Rhino 5 rendering tools. This made several necessary changes to the rendering interface. At this time it is important to find the Flamingo interface when first starting up Flamingo:

Le panneau de contr�le de Flamingo peut �tre ouvert � partir du menu Rendu > Flamingo nXt 5 > Afficher le panneau de configuration
The Flamingo nXt tab contains Flamingo specific controls:
Ciel
Lumi�res
�clairage personnalis�
Options du rendu
Once in the control panel, Right-click in the tab area and select the panels:
Biblioth�ques
Environnement
Plan au sol
Etc…
 
## To access the Flamingo control panel
  * Dans le menu **Flamingo nXt**, cliquez sur **Panneau de configuration**.

  ## The Flamingo nXt Control Panel
The **Flamingo nXt**  **Control Panel** provides tabs for setting up the model for rendering, including:

 *  [Materials](..\materials\materials-tab.html) 
 *  [Lighting](../lighting/lighting-tab.html) 
 *  [Environment](../environment/environment-tab.html) 
 *  [Render](../render/render-tab.html) 

## Rendering Basics
 
Rendering your finished model comprises four basic steps:

 *  [Set up materials](..\materials\materials-tab.html) 
 *  [Set up lighting](../lighting/lighting-tab.html) 
 *  [Set up an environment](../environment/environment-tab.html) 
 *  [Set up rendering conditions](../render/render-tab.html) 

#### To start a rendering

 * Dans le menu **Rendu** ou **Flamingo nXt**, cliquez sur  **Rendu**.
- Ou -

 * Dans la barre d'outils **Standard**, cliquez sur le bouton **Rendu**.

### Stop Rendering
 

By default, the rendering process will continue refining the image, pass by pass, until you click the **Stop Rendering** button. This allows you to manage the trade-off between time and quality. Plus vous laisserez le rendu continuer pendant longtemps, plus il se rapprochera du r�sultat enti�rement calcul�. Vous pouvez arr�ter un rendu � tout moment.


###  <kbd>Resume Rendering</kbd> 
 

Le bouton **Arr�ter le rendu** permet d'interrompre le rendu apr�s la fin de la passe en cours.

Le texte affich� sur le bouton indique ensuite **Reprendre le rendu**. Si vous avez interrompu le rendu avant que les contraintes du nombre de passes ou de temps n'aient �t� atteintes, vous pouvez cliquer sur le bouton **Reprendre le rendu** pour continuer.

Use the [Number of passes](..\render\render-window.html#number-of-passes) or [Time](..\render\render-window.html#time) settings on the [Render Window](..\render\render-window.html) or in [Document Properties &gt; Flamingo nXt](..\render\documentproperties-flamingo.html) to set an automatic stopping point.

&#160;

Revised: 22-Dec-2011 14:45



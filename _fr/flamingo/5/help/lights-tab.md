---
title: Lumi�res
---

# ![images/lights-tab.png](images/lights-tab.png) {{page.title}}
Les sources de lumi�re artificielles utilisent les lumi�res standards de Flamingo en ajoutant des propri�t�s pour contr�ler la distribution de la lumi�re. Lorsque vous utilisez des sources de lumi�re, choisissez le type qui repr�sente le mieux la lampe r�elle que vous mod�lisez.


## Onglet Lumi�res
{: #light-tab}
L'onglet Lumi�res�affiche toutes les lumi�res artificielles de la sc�ne. La rubrique couvre l'onglet Lumi�res de Flamingo. Il existe �galement un [onglet Lumi�res de Rhino](http://docs.mcneel.com/rhino/5/help/fr-fr/index.htm#commands/lights.htm).  Flamingo et Rhino synchronisent les param�tres d'�clairage des deux onglets. L'onglet Lumi�res de Flamingo est un peu plus flexible gr�ce � des [propri�t�s de lumi�re](#light-properties) suppl�mentaires.

L'onglet Lumi�res doit �tre activ� � travers les [pr�r�glages d'�clairage](lighting-tab.html#lighting-presets) ou les [param�tres d'�clairage personnalis�](lighting-tab.html#sun).

<!-- #### Is this supposed to be a code? It's showing up as ####. To fix this, there needs to be a new line above the headline for the markdown to work.-->

#### O� puis-je trouver les contr�les d'�clairage de Flamingo ?
Si l'onglet Lumi�res est activ� � travers les [pr�r�glages d'�clairage](lighting-tab.html#lighting-presets) ou les [param�tres d'�clairage personnalis�](lighting-tab.html#sun), l'onglet des lumi�res se trouve ici�:

 1. ![images/options.png](images/options.png)Barres d'outils >![images/flamingo-icon.png](images/flamingo-icon.png)Barre d'outils de Flamingo nXt
 1. ![images/menuicon.png](images/menuicon.png)Menus > Flamingo nXt 5.0 > Montrer le panneau de configuration > Onglet Flamingo > Lumi�res

Vous pouvez ins�rer des lumi�res, les activer et les d�sactiver, et changer l'intensit� et le canal de chaque lumi�re dans l'onglet Lumi�res. 

Flamingo permet d'ins�rer diff�rents types de lumi�res�:

> [Marquer des objets en tant que lumi�res](#tag-objects-as-lights)
> [Projecteur](#spotlight)
> [Lumi�re ponctuelle)](#pointlight)
> [Lumi�re rectangulaire](#rectangularlight)
> [Lumi�re lin�aire](#linearlight)

**Remarque�:** Les lumi�res directionnelles de Rhino ![images/directionallightbutton.png](images/directionallightbutton.png) ne sont pas prises en charge. Elles n'apparaissent pas dans la liste des lumi�res et elles ne peuvent pas poss�der de propri�t�s de Flamingo nXt.

Certaines propri�t�s de lumi�res sont affich�es dans le tableau de l'onglet Lumi�res afin de pouvoir les modifier rapidement.

Propri�t�s contenues dans le tableau�:

 >[Activer/D�sactiver](#on)
 >[Nom](#name)
 >[Distribution](#light-distribution)
 >[Objectif](#aim-light)
 >[Watts](#watts)
 >[Canal](#channel)

Un clic droit sur l'onglet Lumi�res permet d'ouvrir le menu des [options suppl�mentaires](#additional-options).

Acc�dez aux [propri�t�s des lumi�res](#light-properties) en cliquant sur la lumi�re puis sur l'ic�ne Propri�t�s de la lumi�re ![images/spotlightbutton.png](images/spotlightbutton.png) dans le [panneau des propri�t�s objet](http://docs.mcneel.com/rhino/5/help/en-us/commands/properties.htm).

## Types de lumi�res
{: #light-types}
Les lumi�res peuvent �tre ins�r�es � partir de la barres d'outils de Rhino ou de l'onglet Lumi�res de Flamingo. Les objets peuvent �tre marqu�s en tant que lumi�res avec Flamingo. 

#### ![images/tagobjectsaslights.png](images/tagobjectsaslights.png) Marquer des objets en tant que lumi�res
{: #tag-objects-as-lights}
Tout objet pouvant �tre rendu (surface, solide, etc.) peut �tre marqu� en tant que source de lumi�re et peut recevoir des propri�t�s de lumi�re. D'autres propri�t�s, telles que la [distribution](#light-distribution), la [direction](#aim-light), et l'[intensit�](#watts) peuvent �tre d�finies. Les objets marqu�s en tant lumi�res affichent une application d'aper�u indiquant la direction et la position du centre de la lumi�re.

![images/tag-object-as-light-r85.png](images/tag-object-as-light-r85.png)
*Phares LED marqu�s en tant que sources de lumi�re*

#### ![images/spotlight-01.png](images/spotlight-01.png) Projecteur
{: #spotlight}
Un projecteur est une lumi�re avec une distribution conique dans une direction donn�e. Les propri�t�s de la lumi�re comprennent un [rayon de la source](#radius), un [angle de faisceau](#beam-angle), un rayon d'att�nuation et une direction. Plus le rayon de la source est grand, plus les ombres de la lumi�re seront douces. Un disque est visible par d�faut � l'emplacement de la lumi�re. Vous trouverez des informations sur la modification de la position, de la direction et de l'angle du faisceau � l'�cran � l'aide de poign�es dans la rubrique [Projecteur](http://docs.mcneel.com/rhino/5/help/fr-fr/commands/spotlight.htm) de l'aide de Rhino.

![images/spotlight.png](images/spotlight.png)
*Un projecteur dirig� sur la bo�te rouge*

#### ![images/pointlight-01.png](images/pointlight-01.png) Lumi�re ponctuelle
{: #pointlight}
Les lumi�res ponctuelles sont de petites sph�res qui distribuent une lumi�re uniforme dans toutes les directions. Il est possible de d�finir le [rayon de la source](#radius) de ces lumi�res. Plus le rayon est grand, plus les ombres projet�es par la lumi�re sont douces. Une sph�re de lumi�re est visible par d�faut � l'emplacement de la lumi�re lors du rendu. Des effets insolites peuvent se produire si la lumi�re ponctuelle est partiellement masqu�e par un objet qui coupe la lumi�re. 

![images/pointlight.png](images/pointlight.png)
*Une petite lumi�re ponctuelle pr�s du mur blanc*

#### ![images/rectangularlight-01.png](images/rectangularlight-01.png) Lumi�reRectangulaire
{: #rectangularlight}
Imite un spot encastr� �quip� d'un diffuseur ou de d�flecteurs. La lumi�re est distribu�e de fa�on diffuse en fonction de l'orientation du rectangle. Une fl�che de direction est dessin�e au centre de la lumi�re. L'intensit� maximale est diffus�e en face du rectangle. La lumi�re diminue ensuite lorsqu'elle s'�loigne du centre du rectangle. Un rectangle blanc est visible par d�faut lors du rendu. Ces rectangles ne doivent pas �tre ins�r�s � la m�me hauteur que le plan du plafond. Pour des r�sultats plus r�guliers, les lumi�res doivent �tre plac�es l�g�rement en-dessous du plafond. Vous trouverez des informations sur la modification de la position, de la direction et de l'angle du faisceau � l'�cran � l'aide de poign�es dans la rubrique [Lumi�re rectangulaire](http://docs.mcneel.com/rhino/5/help/fr-fr/commands/spotlight.htm) de l'aide de Rhino.

![images/rectangular light.png](images/rectangular light.png)
*Une lumi�re rectangulaire juste en dessous du plafond*

#### ![images/linearlight-01.png](images/linearlight-01.png) Lumi�reLin�aire
{: #linearlight}
Distribue la lumi�re sur un mod�le cylindrique qui imite un n�on. Il est possible de d�finir le [rayon de la source](#radius) et la longueur de ces lumi�res. Plus le rayon est grand, plus les ombres projet�es par la lumi�re sont douces. Un cylindre de lumi�re est visible par d�faut � l'emplacement de la lumi�re lors du rendu. Des effets insolites peuvent se produire si la lumi�re cylindrique est partiellement masqu�e par un objet qui coupe la lumi�re. Utilisez les points de contr�le de Rhino pour activer les poign�es des lumi�res afin de les modifier � l'�cran. 

![images/linearlight.png](images/linearlight.png)

## Propri�t�s de la lumi�re
{: #light-properties}
Lorsque Flamingo est le moteur de rendu actif dans Rhino, des propri�t�s suppl�mentaires peuvent �tre assign�es aux lumi�res. Seules certaines propri�t�s sont communes � toutes  lumi�res.

#### Nom
{: #name}
Le nom de l'objet lumineux. Il permet de facilement diff�rencier les lumi�res de m�me type dans le mod�le. 

#### ![images/lightbulbon.png](images/lightbulbon.png) Activer/D�sactiver
{: #on}
Active et d�sactive la lumi�re. Dans le tableau des lumi�res, si l'ic�ne de l'ampoule est en jaune, la lumi�re est allum�e. Si l'ampoule est grise, la lumi�re sera d�sactiv�e dans le rendu. Double cliquez sur l'ic�ne pour activer ou d�sactiver la lumi�re. La bo�te de dialogue des propri�t�s poss�de une case Activ�e/D�sactiv�e. 

#### Visible
{: #visible}
Par d�faut, les lumi�res sont affich�es sous forme de sources de lumi�re brillantes dans le rendu. En d�sactivant la propri�t� Visible, l'objet de la lumi�re sera invisible dans le rendu. Mais la lumi�re sera toujours projet�e dans la sc�ne. 

#### Distribution de la lumi�re *([Objets marqu�s uniquement](#tag-objects-as-lights))*
{: #light-distribution}
Lorsqu'un objet est marqu� en tant que lumi�re, utilisez ce param�tre pour d�finir le mode utilis� pour projeter la lumi�re dans la sc�ne. Dans le panneau Lumi�re, double cliquez sur la cellule Distribution pour voir le menu d�roulant avec les options. Il existe diff�rents types de distribution�: [Toutes les directions](#pointlight), [Spot](#spotlight) et [Diffuse](#rectangularlight). Pour les options Spot et Diffuse, une [direction](#aim-light) doit �tre indiqu�e.

#### Diriger la lumi�re *([Objets marqu�s uniquement](#tag-objects-as-lights))*
{: #aim-light}
Pour les lumi�res marqu�es ayant une distribution Spot ou Diffuse, indiquez une direction.   Double-cliquez sur l'ic�ne "Objectif >>" et suivez les invites de la ligne de commandes.

#### Watts
{: #watts}
D�finit la puissance �lectrique de la lumi�re. Nous recommandons de commencer avec des valeurs r�alistes pour la sc�ne. Double cliquez sur la cellule dans le tableau pour changer la valeur. 

#### Angle du faisceau *([Projecteurs uniquement](lights-tab.html#spotlight))*
{: #beam-angle}
L'angle en degr�s qui contr�le la largeur de la lumi�re �manant de la source. Cette valeur peut �galement �tre modifi�e en utilisant les poign�es � l'�cran.  Vous trouverez des informations sur la modification � l'aide de poign�es dans la rubrique [Projecteur](http://docs.mcneel.com/rhino/5/help/fr-fr/commands/spotlight.htm) de l'aide de Rhino.

#### Rayon
{: #radius}
Taille de la source de lumi�re visble. Les lumi�res plus petites projettent des ombres plus pr�cises.

#### Couleur
{: #color}
La couleur de la lumi�re � partir de laquelle la source �mane.

#### Utiliser la couleur du mat�riau *([Objets marqu�s uniquement](#tag-objects-as-lights))*
Utilise la couleur du mat�riau assign� � l'objet lumineux pour d�finir la lumi�re qu'il produit.

#### Canal
{: #channel}
Les lumi�res peuvent �tre li�es � un des huit canaux disponibles. Les canaux permettent d'ajuster l'�clairage directement dans l'image rendue. Cette fonction est tr�s utile pour travailler sur l'�quilibrage de plusieurs sources de lumi�re dans un rendu. Pour plus d'informations, voir la rubrique [Canaux de rendu](render-channel.html).

#### Fichier IES
{: #iesfile}
Les fichiers IES (Illuminating Engineering Society) sont des fichiers de photom�trie qui d�finissent la distribution de la lumi�re � partir d'une source de lumi�re. Les fabricants de luminaires fournissent souvent ces fichiers. En utilisant un fichier IES pour d�finir votre distribution, vous pouvez d�crir plus pr�cis�ment votre source de lumi�re. La g�om�trie de l'objet de lumi�re marqu� n'a pas de relation avec la distribution de la lumi�re. La d�finition de la distribution de la lumi�re provient uniquement du fichier de photom�trie.

Remarques�:

* Flamingo nXt est compatible avec les fichiers goniom�triques de Type C, dont font partie la plupart des fichiers IES. Les fichiers de Type A, parfois utilis�s pour l'industrie automobile pour d�finir des phares et ceux de Type B, parfois utilis�s pour d�finir des projecteurs ne sont pas pris en charge.
* Les distributions IES comprennent les effets des �l�ments composant le luminaire, tels que les d�flecteurs, les r�flecteurs et les diffuseurs.
* Les distributions IES sont souvent asym�triques, il est donc n�cessaire de d�finir non seulement une cible mais �galement un angle de rotation pour diriger la source de lumi�re.

#### Luminosit� � partir d'un fichier
Utiliser l'intensit� enregistr�e dans le fichier IES. Si cette option n'est pas coch�e, le param�tre [Watts](lights-tab.html#watts) est utilis�.


## Menu des options suppl�mentaires
{: #additional-options}
Acc�dez � d'autres options pour les lumi�res en cliquant avec le bouton de droite dans le tableau. 

####  Activ�e
[Active et d�sactive](#on) la lumi�re.

#### Supprimer
Supprime la lumi�re s�lectionn�e.

#### Supprimer la marque de lumi�re
Supprime la [marque](#tag-objects-as-lights) qui transforme un objet en lumi�re.

#### Propri�t�s
Permet d'acc�der aux [propri�t�s](#light-properties) de cette lumi�re. 

#### S�lectionner des objets et les �l�ments correspondants
S�lectionne la lumi�re dans la fen�tre.
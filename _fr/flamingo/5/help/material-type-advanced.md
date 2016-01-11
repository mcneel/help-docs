---
title: Propri�t�s avanc�es du mat�riau
---

# ![images/paint.svg](images/paint.svg) {{page.title}}

![images/bunchofmaterials.png](images/bunchofmaterials.png)

Flamingo poss�de des [mat�riaux simples](material-type-simple.html) et des mat�riaux plus complexes. Les mat�riaux complexes comprennent tous les groupes de propri�t�s disponibles pour un mat�riau. Utilisez les mat�riaux complexes pour avoir un maximum de flexibilit� et de contr�le sur un mat�riau. 

Les propri�t�s des mat�riaux complexes sont divis�es en plusieurs groupes�:

> [Nom](#name)
> [Algorithmes du mat�riau](#procedures)
> [Propri�t�s avanc�es du mat�riau](#advanced-materials-properties)
> [Finition r�fl�chissante ](#reflective-finish-and-highlight)
> [Propri�t�s de transparence](#transparency)
> [Textures algorithmiques](#bump-patterns)
> [Textures bitmap](#textures)
> [Notes](#notes)

## Nom du mat�riau
{: #name}
Cette section indique le nom du mat�riau dans le mod�le de Rhino.  Les mat�riaux sont enregistr�s dans le mod�le de Rhino. Ce qui signifie qu'un mat�riau portant le m�me nom dans la biblioth�que ou un autre mod�le ne sera pas affect� par les modifications r�alis�es sur le mat�riau de ce mod�le. Pour utiliser un mat�riau dans un autre mod�le il doit toit d'abord �tre export� vers la [biblioth�que](libraries.html). Le nom du mat�riau servira �galement � d�finir le nom du fichier export�.

## Algorithmes du mat�riau
{: #procedures}
L'arbre des algorithmes combine un ou plusieurs mat�riaux en utilisant des r�gles pour d�finir l'interaction entre eux. L'arbre affiche les composants utilis�s pour cr�er ce mat�riau et vous permet d'ajouter des composants. Pour des mat�riaux standards, il n'y aura qu'un seul composant dans la liste : Base.

Chaque algorithme combine deux sous-mat�riaux en utilisant une m�thode d�termin�e. Chaque sous-mat�riau peut � son tour �tre constitu� d'un algorithme, en combinant deux sous-mat�riaux. De cette fa�on, des mat�riaux extr�mement �labor�s peuvent �tre cr��s � partir de composants simples. Algorithmes permettant de combiner des mat�riaux�: [M�lange angulaire](procedural-materials.html#angular-blend), [M�lange](procedural-materials.html#blend), [Marbre](procedural-materials.html#marble), [Granit](procedural-materials.html#granite), [Mosa�que](procedural-materials.html#tile) et [Bois](procedural-materials.html#wood).

Par exemple, le [Marbre](procedural-materials.html#marble) combine un mat�riau de base et un mat�riau de veine en utilisant un motif en tourbillon. 


##### Pour ajouter un algorithme
1. Cliquez avec le bouton de droite sur Base dans la fen�tre Algorithmes.
1. Dans le menu, cliquez sur un type d'algorithme.
  * [Base](procedural-materials.html#base)
  * [M�lange angulaire](procedural-materials.html#angular-blend)
  * [M�lange](procedural-materials.html#blend)
  * [Granit](procedural-materials.html#granite)
  * [Marbre](procedural-materials.html#marble)
  * [Mosa�que](procedural-materials.html#tile)
  * [Bois](procedural-materials.html#wood)

##### Pour supprimer un algorithme
 1. Dans la fen�tre Algorithmes, cliquez avec le bouton droit sur le nom de l'algorithme.
 2. Dans le menu, cliquez sur Supprimer.

## Propri�t�s avanc�es du mat�riau
{: #advanced-materials-properties}

{% include_relative snippets/snippet-material-color-select.md %}

#### Reflet et finition r�fl�chissante
{: #reflective-finish-and-highlight}
Ces param�tres font varier la fa�on dont un mat�riau r�fl�chit la lumi�re et les objets. L'effet de reflet est normalement associ� avec les zones des mat�riaux brillants o� la lumi�re rencontre l'objet. L'effet r�fl�chissant est normalement d�fini avec des r�flexions telles un miroir refl�tant les objets dans le reste de la sc�ne. Il est important de savoir que le chrome et les autres mat�riaux r�fl�chissants ne sont pas rendus correctement s'ils ne peuvent pas refl�ter quelque chose. Lorsque vous travaillez avec des mat�riaux r�fl�chissants, pensez �galement � un environnement int�ressant et d'autres objets que les mat�riaux pourront r�fl�chir. 
 Remarque�: Pour activer ces param�tres, la valeur d'intensit� doit �tre sup�rieure � z�ro.

#### Couleur du reflet
{: #highlight-color}
La couleur du reflet est la couleur ajout�e par le mat�riau aux r�flexions. Trois param�tres sont possibles pour ce contr�le�: Blanc, M�tallique et Personnalis�. 

#### Blanc
Les mat�riaux avec un reflet blanc n'ajouteront aucune couleur aux r�flexions. Les mat�riaux avec un reflet blanc sont courants et tendent � ressembler aux peintures standard, aux plastiques ou � une finition de miroir.

![images/3-plastic.png](images/3-plastic.png)

#### M�tallique
{: #metallic}
D�finit la m�me couleur pour le reflet que pour la couleur de base de l'objet. De nombreuses finitions de m�taux utilisent normalement la couleur de base comme couleur r�fl�chissante. Cette option utilise la couleur de base du mat�riau comme couleur r�fl�chissante. 

![images/highlightcolormetallic.png](images/highlightcolormetallic.png)

#### Personnaliser
Pour certaines finitions tr�s sp�ciales, la r�flexion de l'objet sera d'une couleur diff�rente de celle du mat�riau.  Il s'agit normalement de mat�riaux compos�s de plusieurs couches. Utilisez l'option Personnalis� pour d�finir la couleur du reflet. Utilisez le [s�lecteur de couleur](select-color.html) ![images/colorswatch-001.png](images/colorswatch-001.png) pour choisir la couleur de la r�flexion. 

![images/highlightcolorcustom.png](images/highlightcolorcustom.png)

#### Intensit�
{: #intensity}
Ajuste l'intensit� du reflet. Des valeurs plus petites tendent � cr�er des objets brillants qui r�fl�chissent la lumi�re mais pas les objets autour. Des valeurs �lev�es augmentent la taille et l'intensit� du reflet et des r�flexions.  Les valeurs les plus �lev�es cr�eront un mat�riau tel un miroir, r�fl�chissant les autres objets et l'environnement de la sc�ne. 

![images/highlightintensity.png](images/highlightintensity.png)

#### Fresnel
{: #fresnel}
Prononc� [fr�-nel]. Contr�le la r�flectivit� des mat�riaux opaques, un ph�nom�ne connu sous le nom de [R�flexion de Fresnel](https://fr.wikipedia.org/wiki/Coefficients_de_Fresnel).  Le param�tre�de Fresnel reproduit la tendance de nombreux mat�riaux � devenir plus r�fl�chissants (proche d'un miroir) lorsqu'ils sont regard�s en oblique et � devenir plus mats lorsqu'ils sont regard�s � la perpendiculaire.

R�duisez la valeur pour les mat�riaux tr�s fonc�s afin d'�viter une r�flexion trop importante. Augmentez la valeur pour les mat�riaux tels que le bois vernis, pour lesquels la r�flexion de Fresnel est plus prononc�e.

![images/highlightfresnel.png](images/highlightfresnel.png)

#### Nettet�
{: #sharpness}
D�finit la taille du reflet. De petites valeurs donnent un reflet plus ample ; de grandes valeurs concentrent le reflet sur une plus petite zone.  Lorsque cette option est appliqu�e � une r�flectivit� d'intensit� plus �lev�e, les r�flexions sont floues ou nettes. 

![images/highlightsharpness.png](images/highlightsharpness.png)

#### Type
{: #type}
Change comment les r�flexions sont calcul�es lorsque des sources de lumi�re artificielles sont r�fl�chies. Les r�flexions sont calcul�es selon deux m�thodes : *raycasting* et *reflet*. Ces deux m�thodes produiront finalement des r�sultats identiques�; cependant, dans certains cas, vous verrez qu'une des m�thodes donne un bon r�sultat plus rapidement. Par exemple, les objets peuvent voir un mauvaise aspect car une r�flexion de source de lumi�re cache l'apparence du mat�riau.

Dans l'illustration suivante concernant le type �quilibr�, l'objet � gauche pr�sente une r�flexion blanche tr�s claire qui masque l'apparence du mat�riau.

Les rendus d'int�rieur avec de petites sources de lumi�re peuvent parfois pr�senter un aspect tachet� sur les surfaces.  Les surfaces pr�sentant cet aspect ont normalement des r�flexions floues. La modification du type de r�flexion, pour utiliser une r�flexion [brillante](advanced-material-properties-main.html#glossy), [aucune r�flexion de la source de lumi�re](advanced-material-properties-main.html#no-light-source-reflection) ou une r�flexion de [Monte Carlo](advanced-material-properties-main.html#monte-carlo), peut aider � r�soudre ce probl�me. 

#### �quilibr�
{: #balanced}
�quilibre automatiquement le raycasting et le reflet en fonction du param�tre de Nettet�. La r�flexion r�elle de la source de lumi�re ainsi que le reflet artificiel sont tous deux calcul�s.

![images/highlightbalanced.png](images/highlightbalanced.png)

#### Brillant
{: #glossy}
Augmente l'aspect flou du reflet et emp�che le raycasting. Aucune r�flexion n'est calcul�e, aussi bien pour les objets que pour les lumi�res, La performance est donc meilleure et les d�fauts sur les mat�riaux pr�sentant des r�flexions tr�s floues sont �vit�s. On peut cependant perdre un peu de subtilit� au niveau des r�flexions.

![images/highlightglossy.png](images/highlightglossy.png)

#### Monte Carlo
{: #monte-carlo}
Seul le raycasting est utilis� pour calculer les r�flexions des sources de lumi�re. Le raycasting pr�sente initialement un bruit assez important pour converger ensuite vers une solution correcte. Il est plus utile lorsque le reflet n'est pas flou.

![images/highlightmontecarlo.png](images/highlightmontecarlo.png)

#### Aucun reflet
{: #no-highlight}
Seul le raycasting est utilis� pour calculer les r�flexions des sources de lumi�re. Cette option est utile lorsque les sources de lumi�re sont large et le mat�riau n'est pas brillant ; dans ce cas, le calcul du reflet peut prendre beaucoup de temps. Les r�flexions de la source de lumi�re convergent petit � petit.

![images/highlightnohighlight.png](images/highlightnohighlight.png)

#### Aucune r�flexion ni reflet de la source de lumi�re
{: #no-light-source-reflection-and-no-highlight}
Exclue toutes les r�flexions des sources de lumi�re artificielles et tous les effets de reflet artificiels. Les r�flexions des objets sont toujours calcul�es.

![images/highlightnohighlightreflection.png](images/highlightnohighlightreflection.png)

#### Aucune r�flexion de la source de lumi�re
{: #no-light-source-reflection}
Exclue les r�flexions raycast des sources de lumi�re. Seul le reflet est utilis�. Cette option est utile parfois pour �viter des artefacts mouchet�s si le mat�riau est flou et si la sc�ne contient des sources de lumi�re petites et brillantes.

![images/highlightnoreflection.png](images/highlightnoreflection.png)

## Transparence
{: #transparency}
Les param�tres de transparence contr�lent les propri�t�s li�es au passage de la lumi�re � travers un mat�riau.

![images/transparentmaterials.png](images/transparentmaterials.png)

#### Intensit� de la transparence
Fait varier le mat�riau entre opaque et transparent. Les mat�riaux transparents augmentent les temps de rendu.

![images/transparency.png](images/transparency.png)

#### Indice de r�fraction
{: #index-of-refraction}
D�termine la quantit� de r�fraction produite lorsque l'on regarde des objets au travers de ce mat�riau.

![images/transparencyior.png](images/transparencyior.png)

Le tableau suivant montre des exemples d'indices de r�fraction :

 | Mat�riau      |     | Indice de r�fraction         |
 |:--------------|:---:|:------------|
 | Vide        |     | 1         |
 | Air           |     | 1,0029      |
 | Glace           |     | 1,309       |
 | Eau         |     | 1,33        |
 | Verre         |     | entre 1,52 et 1,8 |
 | �meraude        |     | 1,57        |
 | Rubis/Saphir        |     | 1,77        |
 | Diamant       |     | 2,417       |
{: .grided-table}

#### Translucidit�
{: #translucency}
Une mesure de la diffusion. Une translucidit� �lev�e produit un effet "sabl�", car une plus grande quantit� de lumi�re est dispers�e al�atoirement � travers le mat�riau. Il s'agit d'un effet tr�s sensible. De petits r�glages peuvent faire une grande diff�rence. 

![images/transparencytl.png](images/transparencytl.png)

#### Diffusion
{: #scattering}
Contr�le la probabilit� que la lumi�re rencontre une particule par unit� de longueur. Le [Path Tracer](render-tab.html#path-tracer)�doit �tre activ� pour pouvoir utiliser cet effet.

La dispersion en sous-surface permet � la lumi�re de p�n�trer la surface de l'objet et de se disperser dans une direction. Beaucoup de mat�riaux translucides peuvent �tre mod�lis�s avec cet effet. Certaines surfaces, telles que la pierre ou la peau peuvent �tre "adoucies" de fa�on r�aliste en permettant � la lumi�re de p�n�trer sur une courte distance.

Le mat�riau doit avoir une certaine transparence pour que la dispersion en sous-surface puisse avoir lieu. Il s'agit d'un effet de volume. Les objets avec ce type de mat�riau doivent �tre solides ou "enfermer un espace" pour que l'effet fonctionne correctement.

![images/scattering.png](images/scattering.png)

#### Att�nuation
{: #attenuation}
D�termine la quantit� de lumi�re absorb�e lorsqu'elle passe � travers l'objet. Plus les valeurs sont �lev�es plus l'apparence est trouble. Utilisez l'att�nuation pour mod�liser des liquides. Les liquides limpides ont une att�nuation faible. Les liquides troubles ont une att�nuation �lev�e. 

![images/attenuation.png](images/attenuation.png)

#### Dispersion
{: #dispersion}
Contr�le la quantit� de lumi�re divis�e suivant les longueurs d'onde de ses composants.

![images/dispersion.png](images/dispersion.png)

#### Saturation
{: #saturation}
D�termine la quantit� de dispersion.

![images/saturation.png](images/saturation.png)

#### Transparence floue
{: #blurry-transparency}
Lorsqu'un mat�riau est partiellement transparent, un petit bruit est introduit dans la transparence, afin que le r�sultat soit plus naturel.

#### Flou
Contr�le la quantit� de bruit ajout�.

![images/blurrytransparency.png](images/blurrytransparency.png)

#### Incandescence
{: #glow}
Cr�e l'illusion d'une illumination.

![images/glow.png](images/glow.png)

## Textures
{: #textures}
Deux types de textures peuvent �tre ajout�es � un mat�riau : Textures d'image et motifs de relief Les textures d'image sont bas�es sur des bitmaps, des photographies ou des images scann�es. Les motifs de relief sont des motifs al�atoires ou r�p�t�s g�n�r�s par Flamingo. 

![images/textures.png](images/textures.png)

### Images
{: #images}
Il est possible d'utiliser jusqu'� quatre images pour ajouter des d�tails � un mat�riau. Les placages d'images peuvent �tre utilis�s de plusieurs fa�ons : pour modifier la couleur de la surface ou la qualit� tridimensionnelle de la surface. Les placages d'image sont des motifs en deux dimensions cr��s avec des programmes de dessin � base de trames ou en scannant des photographies ou d'autres mat�riaux. Une des m�thodes les plus courantes est d'utiliser l'image d'un mat�riau r�el pour d�finir la couleur. Les images peuvent �tre constitu�es de quatre images maximum. Il se peut parfois qu'une image contr�le la couleur et une autre le relief de la texture. Pour choisir comment une image joue sur un mat�riau, ouvrez la bo�te de dialogue [Propri�t�s de l'image](material-image-properties.html).

![images/solidcolors.png](images/3-texture.png)

{% include_relative snippets/snippet-material-image-add-edit.md %}

### Motifs de relief
{: #bump-patterns}
Les motifs de relief cr�ent l'apparence d'un certain type de surface sans utiliser de placage de d�placement ni de placages suppl�mentaires. Les reliefs utilisent des r�gles math�matiques pour donner l'illusion d'asp�rit�s et de creux sur la surface d'un mat�riau. Motifs disponibles :

> [Papier de verre](#sandpaper)
> [Cr�pi](#rubble)
> [Pyramide](#pyramid)
> [Pliss�](#wrinkled)
> [Marbr�](#marbled)

Les mat�riaux tels que le stuc, le b�ton et l'argile ont une texture fine. Il n'est probablement pas n�cessaire de scanner une pi�ce du mat�riau pour cr�er une image sauf s'il doit �tre vu de tr�s pr�s. L'utilisation d'un placage algorithmique de type papier de verre sur une [couleur de base](advanced-material-properties-main.html#color) simule ce type de motif fin. Cr�ez une [couleur de base](advanced-material-properties-main.html#color) qui sera la couleur du mat�riau. Ajoutez ensuite un relief algorithmique au mat�riau. Utilisez Papier de verre pour obtenir une texture fine et Cr�pi pour une texture grossi�re.

Lorsqu'un placage de relief est s�lectionn�, d'autres options deviennent disponibles. Il est possible d'ajouter plusieurs motifs de relief � un seul mat�riau.

#### Papier de verre
{: #sandpaper}
Le papier de verre donne une apparence fine et al�atoire. Changez l'[�chelle](#scale), l'[intensit�](#strength) et la [rotation](#rotation) pour modifier le papier de verre. 

![images/sandpaper.png](images/sandpaper.png)
*Papier de verre dont l'[�chelle](#scale) et l'[intensit�](#strength) passent de faibles � �lev�es.*

#### Cr�pi
{: #rubble}
Donne l'apparence d'une surface grumeleuse, piquet�e. Son �chelle peut �tre modifi�e et il peut �tre utilis� pour repr�senter de l'eau, une surface sale et des taches. Des t�ches peuvent �tre cr��es en utilisant un cr�pi avec une grande [�chelle](#scale) et une tr�s faible [intensit�](#strength). Le placage de type cr�pi offre un �ventail de taille plus grand que le papier de verre.

![images/rubble.png](images/rubble.png)
*Cr�pi dont l'[�chelle](#scale) et l'[intensit�](#strength) passent de faibles � �lev�es.*

#### Pyramide
{: #pyramid}
Donne l'apparence de petites protub�rances formant un motif pyramidal.  L'[�chelle](#scale) contr�lera uniquement la taille X et Y de la base de la pyramide. L'[intensit�](#strength) jouera sur l'effet de hauteur de la pyramide. 

![images/pyramid.png](images/pyramid.png)
*Pyramide avec une [�chelle](#scale) plus �lev�e.*

#### Pliss�
{: #wrinkled}
Donne une apparence pliss�e. Changez l'[�chelle](#scale), l'[intensit�](#strength) et la [rotation](#rotation) pour modifier le pliss�.

![images/wrinkled.png](images/wrinkled.png)
*Pliss� avec une [�chelle](#scale) plus �lev�e. L'[intensit�](#strength) reste constante.*

#### Marbr�
{: #marbled}
Donne une apparence marbr�e.  Il s'agit d'un motif en tourbillon. Changez l'[�chelle](#scale), l'[intensit�](#strength) et la [rotation](#rotation) pour modifier le marbr�.

![images/marbled.png](images/marbled.png)
*Marbr� avec une [�chelle](#scale) plus �lev�e. L'[intensit�](#strength) reste constante.*

### �chelle
{: #scale}
Contr�le la taille proportionnelle des reliefs.

#### X/Y/Z
D�finit l'�chelle dans chaque direction s�par�ment.
![images/texturescalexy.png](images/texturescalexy.png)

#### Verrouiller
Conserve les proportions de l'image.

### Intensit�
{: #strength}
Contr�le l'apparence de profondeur.
![images/texturestrength.png](images/texturestrength.png)

### Rotation
{: #rotation}
D�finit l'angle de rotation du motif. Les changements r�alis�s sur l'orientation ne sont normalement apparents que si le placage algorithmique a un motif �vident ou si le relief a �t� modifi� avec diff�rentes valeurs pour les directions x, y et z afin de produire un motif directionnel.
![images/texturerotated.png](images/texturerotated.png)
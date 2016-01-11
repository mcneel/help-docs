---
title: Propri�t�s de l'image du mat�riau
---


# ![images/images.svg](images/images.svg) {{page.title}}

![images/3-texture.png](images/3-texture.png)
![images/textures.png](images/textures.png)
![images/solidcolors.png](images/textureset.png)

Les mat�riaux peuvent �tre cr��s � partir d'images. Scannez des photos ou des objets tels que de la  de la moquette, cr�ez des motifs dans un programme de dessin ou utilisez des images provenant d'autres sources.

Imaginez que le mat�riau se prolonge infiniment dans toutes les directions de l'espace. Le mat�riau�ne devient visible que lorsqu'un objet passe � travers. Les motifs se r�p�tent infiniment (mosa�que) dans les quatre directions avec une �chelle d�termin�e.

Les petites images, qui peuvent �tre accol�es sans que la jointure ne soit visible donnent de meilleurs r�sultats. Si la mosa�que ne se cr�e pas correctement, utilisez l'option Mirror tiles pour copier l'image par sym�trie. Cette m�thode permet de s'assurer que les bords co�ncident.

**Remarque�:** Pour qu'une image ne couvre qu'une seule partie d'un objet (�tiquette sur une bouteille de vin ou logo sur un produit) utilisez plut�t la fonction [d�calcomanie](properties-decal.html).

Les placages d'images peuvent �tre utilis�s de plusieurs fa�ons. Une des m�thodes les plus courantes est d'utiliser l'image d'un mat�riau r�el pour d�finir la couleur.

## Nom
Les textures d'images peuvent �tre nomm�es. Ce nom est utilis� par la biblioth�que de textures du RDK et n'a pas d'impact r�el sur Flamingo. 

## Image de Flamingo

### Aper�u de l'image
{: #image-preview}
Affiche un aper�u du fichier image s�lectionn�. Laissez le curseur sur l'image pour voir le nom du fichier image. Cliquez sur l'image pour choisir une autre image. 

#### R�solution de l'image
{: #image-resolution}
Affiche la r�solution en pixels du fichier image actuel.

### Mosa�que
{: #tiles}
Les placages d'image utilis�s dans les d�finitions de mat�riau sont toujours r�p�t�s (mosa�que). Ces param�tres d�finissent la taille de chaque carr� dans les unit�s du mod�le.

#### Largeur/Hauteur
{: #width-height}
D�finit la taille de la mosa�que en unit�s du mod�le.  
{% include_relative snippets/snippet-lock-widthheight.md %}

{% include_relative snippets/snippet-masking.md %}

### Type de placage
{: #mapping-type}
Les images sont normalement appliqu�es au canal de couleur. Mais il existe d'autres fa�ons d'utiliser les images. Les images peuvent �tre d�finies en tant que�:

> [Standard](#standard)
> [Normale](#normal)
> [D�placement](#displacement)

### Standard
{: standard}
L'image apporte de la couleur et un relief apparent au mat�riau. Utilisez les valeurs d'intensit� et de relief pour contr�ler comment l'image joue sur le mat�riau. 

#### Intensit� de la couleur
{: #color}
D�termine l'influence de l'image sur l'apparence du mat�riau. Dans l'exemple ci-dessous, le mat�riau de base est color� en magenta. L'intensit� de la couleur diminue jusqu'� ce que la couleur de base soit enti�rement masqu�e par la texture en noir et blanc.

![images/brik-b14.png](images/brik-b14.png)![images/strength.png](images/strength.png)
*Intensit� de la couleur 0.2, 0.5, 1.0.*

#### Intensit� du relief
{: #bump}
Simule des reliefs et des plis sur la surface d'un objet en perturbant les normales de surface de l'objet. L'objet lui-m�me n'est pas modifi�. Dans l'image, le mat�riau de gauche utilise un placage de d�placement alors que celui de droite utilise un placage de relief d�fini sur sa valeur la plus �lev�e. Un relief avec une valeur n�gative inversera l'effet. Le bord et l'ombre sont lisses pour le mat�riau avec le placage de relief. Voir : [Article de Wikipedia : Placage de relief](https://fr.wikipedia.org/wiki/Placage_de_relief).

![images/bumpvsdisplacement.png](images/bumpvsdisplacement.png)
*Intensit� du relief : 0,5 (gauche) et 1 (droite).*

### Normal
{: #normal}
Imite l'�clairage des parties saillantes et des creux sans utiliser de polygones suppl�mentaires pour le maillage de rendu. Voir : [Article de Wikipedia : Normal mapping](http://en.wikipedia.org/wiki/Normal_mapping).

Les placages normaux fonctionnent comme les placages de relief �tant donn� qu'ils modifient la normale de la surface. L'effet est fondamentalement similaire au relief ; mais les placages normaux permettent un meilleur contr�le sur la normale qu'un relief. Un placage de relief utilise la moyenne grise des valeurs RVB d'une image. Le RVB d'un placage normal correspond � la modification des valeurs XYZ de la normale. Le canal bleu de l'image contr�lant la direction Z de la normale, les placages normaux ont une couleur bleu importante. 

### D�placement
{: #displacement}
Le placage d'image d�place le maillage de rendu de la surface � partir des valeurs de couleur de l'image. L'effet produit est un changement de position g�om�trique de la surface. Le d�placement se fait souvent le long de la normale de la surface. Voir : [Article de Wikipedia : Displacement mapping](https://fr.wikipedia.org/wiki/Displacement_mapping).

 ** Remarque�:** utilisez le placage de d�placement avec parcimonie pour les petits objets. Le d�placement augmente consid�rablement le temps de rendu.

![images/displacement.png](images/displacement.png)

#### Hauteur
{: #height}
La hauteur du point le plus haut du d�placement.

![images/displacementheight.png](images/displacementheight.png)

#### D�calage
{: #offset}
D�finit le point de d�part du d�placement par rapport � la normale de la surface. Le d�placement peut se produire enti�rement en dehors, � l'int�rieur et de part et d'autre de la pi�ce.  

![images/displacementz-001.png](images/displacementz-001.png)
*D�calage Z = -1.0*

![images/displacementz-002.png](images/displacementz-002.png)
*D�calage Z = -0.5*

![images/displacementz-003.png](images/displacementz-003.png)
*D�calage Z = -0.0*

#### Taille d'une facette
{: #facet-size}
La taille des facettes du maillage de d�placement. Le d�placement sera plus d�taill� mais la taille du rendu et la m�moire utilis�e seront �galement plus importantes. 

![images/facetsize.png](images/facetsize.png)

## Image avanc�e de Flamingo
{: #advanced}
Une image de Flamingo sera normalement appliqu�e au canal principal de couleur d'un mat�riau. La bo�te de dialogue des options avanc�es de Flamingo permet de d�finir d'autres canaux affect�s par l'image. Ces canaux sont utilis�s pour obtenir des effets tr�s particuliers. 

####  Couleur de base
Il s'agit du param�tre par d�faut.  Une image affectera la [couleur](advanced-material-properties-main.html#color) d'un mat�riau. 

####  Couleur sp�culaire
Dans ce cas, c'est la couleur du [canal de r�flexion](advanced-material-properties-main.html#highlight-color) d�finie � partir de la couleur de l'image en ce point, qui est affect�e. 

####  Intensit� sp�culaire
Cette option modifiera la [quantit� de r�flexion](advanced-material-properties-main.html#intensity) calcul�e � partir de l'�chelle de gris de l'image en ce point. Elle est souvent utilis�e dans les ensembles de texture en tant que placage sp�culaire. 

####  Nettet� du reflet
Cette option modifiera la nettet� par rapport au flou du [reflet](advanced-material-properties-main.html#intensity) calcul�e � partir de l'�chelle de gris du placage en ce point. 

#### Forme du reflet
{: #advanced-highlight-shape}
Joue sur la forme du reflet.

####  Transparence
Cette option modifiera la quantit� de [transparence](advanced-material-properties-transparency.html) du mat�riau calcul�e � partir de l'�chelle de gris de l'image.

####  Translucidit�
Cette option modifiera la quantit� de [translucidit�](advanced-material-properties-transparency.html#translucency) du mat�riau calcul�e � partir de l'�chelle de gris de l'image.

####  Att�nuation
Cette option modifiera la quantit� d'[att�nuation](advanced-material-properties-transparency.html#attenuation) du mat�riau calcul�e � partir de l'�chelle de gris de l'image.

#### D�calage X/Y
{: #advanced-x-y-offset}
D�cale le mat�riau � partir des axes X et Y.

#### Rotation
Une rotation sera appliqu�e au placage d'image. Utilisez pour faire pivoter l'image de 90 ou 180 degr�s si n�cessaire afin de la r�orienter. 
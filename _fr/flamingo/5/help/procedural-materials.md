---
title: Mat�riaux algorithmiques
---

#  ![images/paint.svg](images/paint.svg) {{page.title}}
L'arbre des algorithmes combine un ou plusieurs mat�riaux en utilisant des r�gles pour d�finir l'interaction entre eux. L'arbre affiche les composants utilis�s pour cr�er ce mat�riau et vous permet d'ajouter des composants. Pour des mat�riaux simples, il n'y aura qu'un seul composant dans la liste : Base.

Chaque algorithme combine deux sous-mat�riaux en utilisant une m�thode d�termin�e. Chaque sous-mat�riau peut � son tour �tre constitu� d'un algorithme, en combinant deux sous-mat�riaux. De cette fa�on, des mat�riaux extr�mement �labor�s peuvent �tre cr��s � partir de composants simples. Algorithmes de combinaison de mat�riaux :

> [Base](#base)
> [M�lange angulaire](#angular-blend)
> [M�lange](#blend)
> [Marbre](#marble)
> [Granit](#granite)
> [Mosa�que](#tile)
> [Bois](#wood)

##### Pour ajouter un algorithme
1. Cliquez avec le bouton de droite dans la fen�tre des Algorithmes.
1. Dans le menu, cliquez sur un type d'algorithme.

##### Pour supprimer un algorithme
 1. Dans la fen�tre Algorithmes, cliquez avec le bouton droit sur le nom de l'algorithme.
 2. Dans le menu, cliquez sur Supprimer.

## Base
{: #base}
Ce mat�riau est le mat�riau simple de base sans couche. Il s'agit de l'algorithme par d�faut. 

## M�lange angulaire
{: #angular-blend}
De nombreux mat�riaux changent de couleur, de r�flexion ou de transparence en fonction de l'angle selon lequel le mat�riau est regard�. L'algorithme de m�lange angulaire m�lange deux mat�riaux en fonction de l'angle de vue sur la surface de l'objet.

![images/angularblendmaterials.png](images/angularblendmaterials.png)
L'algorithme M�lange angulaire m�lange deux composants diff�rents pour cr�er des effets sp�ciaux. Les deux couches utilis�es par l'algorithme sont la couche int�rieure et ext�rieure.

#### Int�rieur
De 0 degr� � partir du point de vue jusqu'� l'angle de d�part, le composant int�rieur se verra enti�rement. Vous pouvez consid�rer cet �l�ment comme le mat�riau de base.

#### Ext�rieur
� partir de l'angle final jusqu'� 90 degr�s, le mat�riau ext�rieur sera le seul visible. Vous pouvez consid�rer cet �l�ment comme le rev�tement.

#### Angle de d�part
L'angle avec le point de vue � partir duquel le composant ext�rieur commence.

#### Angle final
L'angle avec le point de vue � partir duquel le composant ext�rieur s'arr�te.
Entre l'angle de d�part et l'angle final, les composants int�rieur et ext�rieur se m�langent.

Dans l'illustration ci-dessous, l'angle de d�part![images/01.png](images/01.png) est �gal � 30 degr�s (ce qui, dans le rendu, se traduit par le cercle vert � droite) et l'angle final![images/02.png](images/02.png) est �gal � 60 degr�s (ce qui, dans le rendu, se traduit par le cercle rouge).

L'image de droite montre un mat�riau int�rieur blanc et un mat�riau ext�rieur noir.

![images/angularblend-003.png](images/angularblend-003.png) ![images/angularblend-001.png](images/angularblend-001.png)

* Entre 0 et 30 degr�s � partir du point de vue, vous voyez le blanc.
* Entre 30 et 60 degr�s � partir du point de vue, vous voyez un d�grad� passant du blanc au noir.
* Entre 60 et 90 degr�s � partir du point de vue, vous voyez noir.

## M�lange
{: #blend}
L'algorithme de m�lange combine deux composants de base et permet de d�finir les proportions de chacun. Tous les bois inclus dans la biblioth�que de Flamingo utilisent un algorithme de m�lange pour donner une finition brillante et fonc�e au bois.
![images/blend-001.png](images/blend-001.png)
Les m�langes permettent de changer enti�rement la d�finition d'un mat�riau en ajoutant une couleur � un motif de base.

#### M�lange
Permet de changer le pourcentage de chaque mat�riau utilis� pour le mat�riau final.  Par exemple, le mat�riau ci-dessous montre un m�lange entre un mat�riau ray� et une couleur verte unie. Pour l'image de gauche, le glisseur est situ� vers la gauche, ce qui donne plus d'importance au mat�riau ray� et r�duit la force du mat�riau vert.  Pour l'image du milieu, le glisseur est situ� au milieu et les deux mat�riaux sont m�lang�s � parts �gales.  Pour l'image de droite, le glisseur est situ� vers la droite, ce qui donne moins d'importance au mat�riau ray� et renforce le mat�riau vert.
![images/blendpercent.png](images/blendpercent.png)

#### Utiliser une image
Une image peut �tre utilis�e pour contr�ler l'interaction entre les deux mat�riaux. Lorsqu'une image est utilis�e, les valeurs d'�chelle de gris des pixels d�finissent le m�lange entre les deux composants. Utilisez une image en �chelle de gris pour cr�er des nuances interm�diaires entre le premier et le deuxi�me composant. Le premier composant sera plac� sur les parties noires de l'image et le deuxi�me composant sera plac� sur les parties blanches.

Dans l'image, les m�mes mat�riaux sont utilis�s pour le premier et le deuxi�me composants, mais le m�lange est contr�l� par trois images diff�rentes.
![images/blendmask.png](images/blendmask.png)
La r�solution de l'image du masque joue sur la qualit� du mat�riau. Des images de haute r�solution vous permettront de regarder le mat�riau de plus pr�s sans perdre de qualit� mais elles utiliseront plus de m�moire.

#### Utiliser le canal alpha
Si l'image poss�de un canal alpha, il peut �tre utilis� au lieu de l'�chelle de gris de l'image pour d�terminer le m�lange des couleurs.

#### Inverser
Le premier composant sera plac� sur les parties blanches de l'image et le deuxi�me sur les parties noires.

#### Mosa�que
L'�chelle du mat�riau lors du rendu ne d�pend pas de la r�solution de l'image. Afin de d�finir correctement l'�chelle du mat�riau, vous devez d�finir la taille, en unit�s r�elles, de la zone repr�sent�e par une copie de l'image. Si la hauteur de l'image repr�sente six carreaux de 4 unit�s et la longueur repr�sente douze carreaux de 4 unit�s, l'�chelle est de 48 unit�s dans la direction des x et de 24 unit�s dans la direction des y. L'image est alors ajust�e � la taille appropri�e pour le motif.

#### Largeur
La largeur en pixels d'une seule copie de l'image.

#### Hauteur
La hauteur en pixels d'une seule copie de l'image.

## Granit
{: #granite}
Cr�e un mat�riau 3D dont le composant de base est incrust� de t�ches d'un deuxi�me mat�riau. L'algorithme de granit combine un composant de point (spot) r�parti de fa�on al�atoire dans un composant de base. L'algorithme du granit d�finit comment les composants de base et de point se combinent. Les algorithmes de granit peuvent �tre utilis�s pour une grande vari�t� de mat�riaux tels que la rouille, le plastique brillant et autres mat�riaux mouchet�s de fa�on al�atoire.
![images/granitematerials.png](images/granitematerials.png)

#### Base/Point
Les composants de Base et de Point sont deux mat�riaux. Leurs propri�t�s sont d�finies comme pour tout autre mat�riau.
![images/granitescale.png](images/granitescale.png)
{% include_relative snippets/snippet-materialscaleandlock.md %}

#### Densit�
Une fraction du motif dans son ensemble. La taille relative des points est proportionnelle � cette valeur.
![images/granitedensity.png](images/granitedensity.png)
{% include_relative snippets/snippet-materialblend.md %}
![images/graniteblend.png](images/graniteblend.png)

## Marbre
{: #marble}
Cr�e des tranches alternant les composants de base et de nervure. L'algorithme du marbre d�finit comment les composants de base et de veine se combinent. Les  dalles sont infiniment larges et l'orientation de l'objet joue sur la fa�on dont les dalles sont orient�es par rapport � l'objet.

![images/marbled.png](images/marbled.png)

Le [placage de texture](properties-object.html#mapping) des objets contr�le l'orientation�du mat�riau sur l'objet.
![images/materialunmapped.png](images/materialunmapped.png)
*Pas de placage de texture (gauche). Avec placage de texture (droite).*

#### Base/Veine
Les composants de Base et de Veine sont deux mat�riaux. Leurs propri�t�s sont d�finies comme pour tout autre mat�riau.
{% include_relative snippets/snippet-materialscaleandlock.md %}![images/marblescale.png](images/marblescale.png)

#### Largeur de la veine
Permet de changer la taille relative des tranches les unes par rapport aux autres. La valeur donn�e � la largeur de veine est une fraction de la distance entre une rayure de la base et la suivante. Les valeurs peuvent aller de 0 (z�ro) pour indiquer qu'il n'y a pas de composant de veine � 1 pour aucun composant de base.
![images/marbleveinwidth.png](images/marbleveinwidth.png)
{% include_relative snippets/snippet-materialblend.md %}![images/marbleblending.png](images/marbleblending.png)
{% include_relative snippets/snippet-materialturbulence.md %}![images/marbleturbulence.png](images/marbleturbulence.png)
{% include_relative snippets/snippet-materialveneer.md %}![images/marbleveneer.png](images/marbleveneer.png)
*Rev�tement (gauche) ; normal (droite).*

## Mosa�que
{: #tile}
La mosa�que est un mat�riau 2D. Le [placage de texture](properties-object.html#mapping) des objets contr�le l'orientation�du mat�riau sur l'objet. L'algorithme de mosa�que est constitu� d'un composant de base et d'un composant de jointure. Chacun des composants peut inclure d'autres mat�riaux.
![images/tile materials.png](images/tile materials.png)
Utilisez une taille diff�rente dans chaque direction afin de cr�er des effets sp�ciaux. Par exemple, utilisez une mosa�que tr�s longue dans une direction pour cr�er des mat�riaux de pavement.

#### Mosa�que
D�finit la taille g�n�rale de la mosa�que. La largeur et la hauteur peuvent �tre d�finies ind�pendamment l'une de l'autre.
![images/tilescale.png](images/tilescale.png)

#### Largeur/Hauteur
D�finit la largeur�et la hauteur des carreaux.
{% include_relative snippets/snippet-lock-widthheight.md %}

#### Joint
Change la taille de la jointure.
![images/tilejointsize.png](images/tilejointsize.png)

#### Jointure horizontale / Jointure verticale
D�finit la largeur et la hauteur de la jointure.

#### Verrouiller
Conserve le rapport entre la taille des jointures horizontale et verticale.

#### D�calage
Permet d'obtenir un d�calage horizontal relatif. Par exemple, utilisez un d�calage de .5 pour cr�er une structure standard de panneresse. Ceci permet de mod�liser des mat�riaux tels que des mosa�ques de marbre, sans avoir l'impression que tout le sol a �t� taill� dans un seul bloc de marbre.
![images/tileoffset.png](images/tileoffset.png)

#### Variation des carreaux
Ajoute un effet al�atoire � la couleur du mat�riau pour chaque carreau. Cette option permet de mod�liser des mat�riaux tels que des briques non uniformes.

#### R/V/B
Modifie les composantes rouge, verte et bleue de la couleur.  Le mat�riau de base de chaque carreau variera alors l�g�rement de fa�on al�atoire.
![images/tilevarycolor.png](images/tilevarycolor.png)

#### X/Y/Z
D�cale le mat�riau par rapport � l'origine du rep�re g�n�ral pour chaque carreau de fa�on al�atoire. Le d�calage peut �tre int�ressant si une jointure qui marque le d�but du mat�riau est mal plac�e.
![images/tilevaryxyz.png](images/tilevaryxyz.png)

## Bois
{: #wood}
Le bois est constitu� de cylindres concentriques avec une alternance des composants de base et d'anneau. L'algorithme du bois d�finit comment les composants de base et d'anneau se combinent.

Utiliser cette m�thode pour cr�er des mat�riaux imitant le bois si les objets ne sont pas vus de pr�s. Si vous avez besoin d'un bois plus d�taill�, utilisez un [mat�riau avec texture](material-type-simple.html#textured) pour le d�finir. Si votre point de vue n'est pas trop proche du bois, une couleur unie peut �tre utilis�e pour remplacer le bois sans que l'image ne perde de qualit�. Le rendu sera alors plus rapide. Un autre avantage du bois est que le grain est correctement dessin�, quel que soit l'angle sous lequel il est vu. L'extr�mit� du grain se verra sur les extr�mit�s et le grain parall�le sur les c�t�s de l'objet.
![images/woodmaterials.png](images/woodmaterials.png)

#### Base/Anneau
Les composants de Base et d'Anneau sont deux mat�riaux. Leurs propri�t�s sont d�finies comme pour tout autre mat�riau.
{% include_relative snippets/snippet-materialscaleandlock.md %}![images/woodscale.png](images/woodscale.png)

#### Largeur des anneaux
Une fraction de la distance entre une rayure de la base et la suivante. Les valeurs peuvent aller de 0 (z�ro) pour indiquer qu'il n'y a pas de composant d'anneau � 1 pour aucun composant de base.
![images/woodringwidth.png](images/woodringwidth.png)
{% include_relative snippets/snippet-materialblend.md %}![images/woodblend.png](images/woodblend.png)
{% include_relative snippets/snippet-materialturbulence.md %}![images/woodturbulence.png](images/woodturbulence.png)
{% include_relative snippets/snippet-materialveneer.md %}![images/woodveneer.png](images/woodveneer.png)
Rev�tement (gauche) ; normal (droite)
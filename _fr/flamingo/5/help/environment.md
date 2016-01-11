---
title: Environnement de Flamingo
---

# ![images/environment.svg](images/environment.svg) {{page.title}}
Rhino poss�de de nombreux [types d'environnements](http://docs.mcneel.com/rhino/5/help/fr-fr/commands/environmenteditor.htm). Cette rubrique traite de l'environnement de Flamingo.

L'environnement agit sur la partie visible de l'arri�re-plan et des r�flexions.  Pour des effets agissant sur l'�clairage de la sc�ne, consultez la rubrique de l'aide sur le [Ciel](sun-and-sky-tabs.html).

Flamingo poss�de un environnement sp�cial appel� **Environnement par d�faut de Flamingo**.  Cet environnement est synchronis� avec les [Pr�r�glages d'�clairage](lighting-tab.html). En utilisant les [Pr�r�glages d'�clairage](lighting-tab.html), l'�clairage et l'environnement seront d�finis avec les valeurs par d�faut adapt�es � la sc�ne.

Les propri�t�s de l'environnement de Flamingo sont divis�es en plusieurs groupes�:

> [Nom](#name)
> [Environnement de Flamingo](#environment)
> [Couleur de l'arri�re-plan](#color-backgrounds)
> [Arri�re-plan avanc�](#advanced-background-reflected-sky)


## Nom de l'environnement
{: #name}
Cette section indique le nom de l'environnement dans le mod�le de Rhino. Les environnements sont enregistr�s dans le mod�le de Rhino. Ce qui signifie qu'un environnement portant le m�me nom dans la biblioth�que ou un autre mod�le ne sera pas affect� par les modifications r�alis�es sur l'environnement de ce mod�le. Pour utiliser un environnement dans un autre mod�le il doit toit d'abord �tre export� vers la [biblioth�que](libraries.html). Le nom de l'environnement servira �galement � d�finir le nom du fichier export�. 

## Environnement de Flamingo
{: #environment}
L'environnement a trois fonctions dans un rendu�:

>Arri�re-plan visible
>[Arri�re-plan r�fl�chissant](#advanced-background-reflected-sky)
>[Arri�re-plan r�fringent](#advanced-background-reflected-sky)

L'arri�re-plan visible est la couleur de base dans l'arri�re-plan de la sc�ne. Il est d�fini dans le panneaux des propri�t�s g�n�rales. Les arri�re-plans [r�fl�chissant](#advanced-background-reflected-sky) et [r�fringent](#advanced-background-refracted-sky) peuvent diff�rer et sont disponibles dans la section Arri�re-plan avanc�.

#### Intensit�
{: #background-intensity}
Modifie la clart� relative de l'arri�re-plan. La valeur de l'intensit� est utilis�e pour multiplier les couleurs de l'arri�re-plan afin d'obtenir une valeur d'�clairage.  Les couleurs peuvent aller de 0 � 255 par canal. L'intensit� multipliera ces valeurs.  Ce param�tre devient important si l'arri�re-plan est tr�s sombre par rapport au mod�le rendu. 

#### Type d'arri�re-plan
{: #background-type}
D�finit le sch�ma de couleur qui remplira l'arri�re-plan de l'image rendue. Il existe diff�rents types d'arri�re-plans :

> [Ciel](#environment-sky)
> [Uni et d�grad� de couleurs](#color-backgrounds)
> [Image](#environment-image)
> [Images HDR et HDR planes](#hdr-background)

## Ciel en arri�re-plan
{: #environment-sky}
L'environnement Ciel utilise les param�tres du soleil et du ciel d�finis dans l'onglet [�clairage(lighting-tab.html) .  Il s'agit du param�tre par d�faut pour les rendus utilisant le ciel. 

![images/background-sky-001.png](images/background-sky-001.png)
*Automatique (gauche) et image HDR et soleil (droite).*

## Couleur en arri�re-plan
{: #color-backgrounds}
Les param�tres de couleur pour l'arri�re-plan sont toujours pr�sents. Une couleur est toujours d�finie pour l'arri�re-plan m�me si elle est enti�rement masqu�e par une image, une image HDR ou le ciel.

### Couleur unie
{: #solid-color}
Un arri�re-plan de couleur unie est compos� d'une seule couleur qui remplit tout l'arri�re-plan.

![images/background-color-001.png](images/background-color-001.png)
*Arri�re-plan de couleur unie.*
Voir [Contr�le de couleur](#enviroment-sky-color-controls) ci-dessous pour plus d'informations sur la modification de la couleur unie.

#### D�grad� de deux couleurs
{: #two-color-gradient}
Les arri�re-plans avec un d�grad� de deux ou trois couleurs ne sont appliqu�s que dans les vues en perspective. Les arri�re-plans avec un d�grad� de deux couleurs interpolent la couleur de l'arri�re-plan entre deux couleurs s�lectionn�es.

![images/background-color-002.png](images/background-color-002.png)
*Arri�re-plan avec un d�grad� de deux couleurs : bleu et jaune.*
Voir [Contr�les de couleur](#enviroment-sky-color-controls) ci-dessous pour plus d'informations sur la modification d'un d�grad� de deux couleurs.

#### D�grad� de trois couleurs
{: #three-color-gradient}
Les arri�re-plans avec un d�grad� de trois couleurs interpolent la couleur de l'arri�re-plan entre trois couleurs s�lectionn�es.
![images/background-color-003.png](images/background-color-003.png)
*Arri�re-plan avec un d�grad� de trois couleurs : bleu, blanc et jaune.*
Voir [Contr�les de couleur](#enviroment-sky-color-controls) ci-dessous pour plus d'informations sur la modification d'un d�grad� de trois couleurs.

### Contr�les de couleur
{: #enviroment-sky-color-controls}
Le nombre de contr�les disponibles peut varier en fonction du type d'arri�re-plan actuellement s�lectionn�. Les arri�re-plans avec un d�grad� auront jusqu'� trois s�lecteurs de couleur qui peuvent comprendre une couleur sup�rieure, m�diane et inf�rieure.

{% include_relative snippets/snippet-material-color-select.md %}

#### Inverser les couleurs
Utilisez ce bouton pour inverser la couleur du d�grad� entre le haut et le bas.

#### Contr�le de placage du d�grad�
{: #gradient-mapping}
Les couleurs d'un arri�re-plan avec d�grad� de couleurs doivent �tre plaqu�es sur la sph�re de l'environnement. Utilisez un syst�me de placage de d�grad� pour ce faire.  Les contr�le de placage du d�grad� ne seront activ�s que lorsqu'un d�grad� de deux ou trois couleurs est s�lectionn�. Les d�grad�s ne peuvent �tre plaqu�s que dans les vues en perspective.

#### Angles � partir d'une vue
{: #angle-from-views}
Si l'option Angles � partir d'une vue est coch�e, le d�grad� de couleurs actuel sera synchronis� avec la vue en perspective actuelle.  La couleur sup�rieure sera plaqu�e en haut de la vue et la couleur inf�rieure en bas.  Toutes les autres couleurs seront r�parties entre ces extr�mit�s. 

#### Ic�ne de visualisation de l'altitude
{: #colorrange}
Si la fen�tre active est une projection en perspective, vous pouvez contr�ler les couleurs sup�rieure et inf�rieure et l'�tendue du d�grad� par rapport � votre vue.

![images/background-color-004.png](images/background-color-004.png){: style="float: left; padding-right: 25px;padding-bottom: 15px;padding-top:15px;"}

* Le contr�le affiche l'environnement dans une vue de section. La marqueur 90 degr�s correspond � la coordonn�e Z vers le haut. La coordonn�e 0 repr�sente le plan au sol horizontal. La marqueur -90 degr�s correspond � la coordonn�e Z vers le bas.
* Le c�ne de vision gris affiche la derni�re coordonn�e de la vue en perspective actuelle. 
* La fl�che rouge repr�sente la position de la couleur sup�rieure. La couleur sup�rieure sera affich�e � cet angle et au-dessus. 
* La double fl�che verte repr�sente le milieu du m�lange entre les couleurs sup�rieure et inf�rieure. S'il s'agit d'un d�grad� de trois couleurs il s'agit �galement de la position de la couleur du milieu. 
* La fl�che rouge repr�sente la position de la couleur inf�rieure. En-dessous de cet angle, seule la couleur inf�rieure appara�tra. 

####  Obtenir les angles � partir du bouton de la vue
Utilisez ce bouton pour effacer les contr�les de placage du d�grad� et utiliser les coordonn�es de la vue en perspective actuelle. 

#### Angles sup�rieur/milieu/inf�rieur
Ces valeurs correspondent aux couleurs sup�rieure, m�diane et inf�rieure du d�grad� actuel. Ils correspondent � la position des fl�ches rouge, verte et bleu dans l'ic�ne de visualisation de l'altitude. 

## Image en arri�re-plan
{: #environment-image}

Une image est projet�e sur l'arri�re-plan. Cette fonctions est souvent utilis�e pour placer un mod�le dans un contexte existant ou pour d�finir une vue derri�re des fen�tres. Une photographie, une illustration scann�e ou une image cr��e avec un programme de dessin peuvent �tre utilis�es comme image. Pour obtenir de meilleurs r�sultats, utilisez des images de haute r�solution pour les arri�re-plans. Vous pouvez aussi rendre les images plus floues ou plus claires pour simuler une mise au point naturelle ou une perspective a�rienne. L'image en l'arri�re-plan peut �tre plaqu�e dans la sc�ne en utilisant une projection plane, cylindrique ou sph�rique. 

![images/background-image-001.png](images/background-image-001.png)
*Une image plane d�finie comme arri�re-plan.*

### Fichier image
{: #image-properties}
D�finissez l'image en arri�re-plan en cliquant sur le bouton *(vide - cliquer pour assigner)*, puis s�lectionnez une image.  Pour assigner une autre image, cliquez sur l'image en miniature. 

### Projection
{: #backgroud-image-projection}
S�lectionnez une des trois projections d'image dans le menu d�roulant�:

>[Plane](#planar)
>[Cylindrique](#cylindrical)
>[Sph�rique](#spherical)

Chaque m�thode de projection poss�de ses propres options pour positionner l'image.

### Projection plane
{: #planar}
L'image est projet�e sur un arri�re plan plat dans la vue actuelle. Les coordonn�es de la projection plane sont toujours relatives � la vue actuelle. 

![images/projectiontypesplanar.png](images/projectiontypesplanar.png)

#### Angle � partir d'une vue
La case angle � partir de vue permettra de synchroniser l'image avec la vue actuelle. L'image sera alors �tir�e pour l'adapter � la vue actuelle.

#### Contr�le de positionnement de l'image
Utilisez le contr�le de positionnement de l'image pour la placer l'image par rapport � la vue actuelle. La forme de la fen�tre appara�t sous forme de rectangle gris fonc�. Faites glisser le rectangle rose ou utilisez les options num�riques pour d�placer ou changer l'�chelle de l'image en arri�re-plan par rapport � la vue. 

![images/background-image-003.png](images/background-image-003.png)
*Zone de la fen�tre active (1), taille et forme de l'image (2).*

#### �chelle X / �chelle Y
D�finit la taille de l'image en arri�re-plan en appliquant une �chelle de 0 � 1 � la largeur et la hauteur de la fen�tre. Par exemple, une valeur de 1.0 repr�sente 100�% de la taille de la vue, une valeur de 0.5 repr�sente 50�% de la largeur de la vue, etc. 

#### D�calage X / D�calage Y
D�finit le d�calage de l'image en arri�re-plan � partir du coin inf�rieur gauche de la fen�tre en appliquant une �chelle de 0 � 1 � la largeur et la hauteur de la vue.  Par exemple, une valeur de 0.25 repr�sente 25�% de la taille de la vue, une valeur de 0.5 repr�sente 50�% de la largeur de la vue, etc.

#### Contr�le de positionnement de l'image
Utilisez le contr�le de positionnement de l'image pour la placer l'image par rapport � la vue actuelle. La forme de la fen�tre appara�t sous forme de rectangle gris fonc�. Faites glisser le rectangle rose ou utilisez les options num�riques pour d�placer ou changer l'�chelle de l'image en arri�re-plan par rapport � la vue. 

![images/background-image-003.png](images/background-image-003.png)
*Zone de la fen�tre active (1), taille et forme de l'image (2).*

#### �chelle X / �chelle Y
D�finit la taille de l'image en arri�re-plan en appliquant une �chelle de 0 � 1 � la largeur et la hauteur de la fen�tre. Par exemple, une valeur de 1.0 repr�sente 100�% de la taille de la vue, une valeur de 0.5 repr�sente 50�% de la largeur de la vue, etc. 

#### D�calage X / D�calage Y
D�finit le d�calage de l'image en arri�re-plan � partir du coin inf�rieur gauche de la fen�tre en appliquant une �chelle de 0 � 1 � la largeur et la hauteur de la vue.  Par exemple, une valeur de 0.25 repr�sente 25�% de la taille de la vue, une valeur de 0.5 repr�sente 50�% de la largeur de la vue, etc.

### Projection cylindrique
{: #cylindrical}
La projection cylindrique plaque l'image sur un cylindre imaginaire entourant le mod�le. M�me si cette projection donne les meilleurs r�sultats avec des images cylindriques, elle peut aussi �tre utilis�e avec des panoramas standards cr��s � partir de photographies.

![images/projectiontypescylindrical.png](images/projectiontypescylindrical.png)
Sp�cifiez la taille et la position du placage selon l'angle de hauteur et l'angle de largeur. Utilisez les outils graphiques et la souris pour positionner et redimensionner l'image. Le c�ne de vision est affich� dans le graphique sous forme de zone gris clair.

#### Angle � partir d'une vue
La case angle � partir de vue permettra de synchroniser l'image avec la vue actuelle. L'image sera alors �tir�e pour l'adapter � la vue actuelle.

#### Contr�le du plan
D�termine la largeur angulaire du placage de l'image. Indiquez un angle ou faites glisser les drapeaux dans l'application de contr�le pour d�finir la largeur. La zone bleue indique les dimensions de la largeur angulaire.

![images/cylindricalcontrol-001.png](images/cylindricalcontrol-001.png){: .float-img-left}

* Le contr�le affiche l'environnement dans une vue en plan. 
* Le c�ne de vision gris fonc� affiche les derni�res coordonn�es dans la vue en perspective actuelle.
* Le c�ne bleu affiche l'intervalle d'angles o� l'image sera visible. 
* La fl�che bleue repr�sente la coordonn�e gauche du placage de l'image. 
* Le point rouge repr�sente le centre de l'image en arri�re-plan.
* La fl�che violette repr�sente la coordonn�e droite du placage de l'image.

#### Contr�le vertical
{: .clear-img}
D�finit les dimensions verticales de la projection cylindrique. Indiquez un angle ou faites glisser les drapeaux dans l'application de contr�le pour d�finir les angles sup�rieur et inf�rieur. La projection cylindrique est limit�e � 45 degr�s au-dessus et en dessous de l'horizon.

![images/background-cylinder-001.png](images/background-cylinder-001.png){: .float-img-left}

* Le contr�le affiche le cylindre dans une vue de section.
* Le c�ne de vision gris affiche les derni�res coordonn�es dans la vue en perspective actuelle.
* La fl�che bleue repr�sente la bordure inf�rieure du placage de l'image.
* La fl�che rouge repr�sente la bordure sup�rieure du placage de l'image.

#### Rotation
{: .clear-img}
D�finit la rotation de l'image. Le point rouge indique le centre de l'image.

#### Largeur
D�finit la largeur de l'image en degr�s par rapport � la vue en plan. 

#### Haut/Bas
D�finit les angles verticaux de l'image en fonction de la direction du plan au sol horizontal dans le mod�le.

####  Obtenir les angles � partir de la vue
D�finit l'angle de rotation en fonction de la  fen�tre perspective actuelle.  Cette option permet par exemple de red�finir les valeur de la projection.

### Projection sph�rique
{: #spherical}
La projection sph�rique plaque l'image sur une sph�re compl�te. Cette m�thode produit g�n�ralement de bons r�sultats si une image cylindrique �quidistante est utilis�e.  Le rapport de forme d'une image cylindrique �quidistante est un rectangle de 2:1.

#### Angle � partir d'une vue
La case angle � partir de vue permettra de synchroniser l'image avec la vue actuelle. L'image sera alors �tir�e pour l'adapter � la vue actuelle.

#### Contr�le sph�rique
D�termine la direction du placage de l'image. Indiquez un angle ou faites glisser l'indicateur dans l'application de contr�le pour d�finir la largeur. Le point rouge repr�sente le centre de l'image en arri�re-plan.

#### Rotation
{: .clear-img}
D�finit la rotation de l'image. Le point rouge indique le centre de l'image.

####  Obtenir les angles � partir de la vue
D�finit l'angle de rotation en fonction de la  fen�tre perspective actuelle.  Cette option permet par exemple de red�finir les valeur de la projection.

## Arri�re-plan HDR
{: #hdr-background}
L'utilisation d'une image HDR comme environnement permet de mieux contr�ler la relation entre la lumi�re de l'arri�re plan et les autres lumi�res de l'image. Cette option est particuli�rement utile pour repr�senter un espace int�rieur avec un espace clair ext�rieur passant par une fen�tre. Une image d'environnement HDR dispose d'une plage de lumi�res plus grande qu'une image bitmap normale et elle peut poss�der un canal ; ainsi, le contraste peut �tre g�r� dans un  rendu [multicanal](lights-tab.html#channel) .

#### Fichier image
{: #hdri-image}
D�finissez l'image HDR en arri�re-plan en cliquant sur le bouton *(vide - cliquer pour assigner)*, puis s�lectionnez une image.  Pour assigner une autre image, cliquez sur l'image en miniature.

{% include_relative snippets/snippet-rotatehdrimage.md %}
{% include_relative snippets/snippet-mirrorimage.md %}
{% include_relative snippets/snippet-sunchannel.md %}
{% include_relative snippets/snippet-skychannel.md %}

## Options d'image HDR plane
{: #planar-hdr-options}

Les images � grande plage dynamique planes sont rarement utilis�es mais peuvent �tre tr�s utiles.  Une image HDR offre une large gamme de possibilit�s de couleurs. Les fichiers HDR peuvent �tre tr�s utiles pour les fen�tre ext�rieures de rendus architecturaux o� l'arri�re-plan est trop clair ou trop fonc�.  Un placage plan est toujours utilis� pour les fichiers HDR.


![images/planarimagebeach.png](images/planarimagebeach.png)
*Une image en arri�re plan (gauche) et une image HDR plane (droite) pr�sentent des diff�rences d'�clairage subtiles en arri�re-plan.*

#### Fichier image
{: #hdri-planar-image}
D�finissez l'image HDR en arri�re-plan en cliquant sur le bouton *(vide - cliquer pour assigner)*, puis s�lectionnez une image.  Pour assigner une autre image, cliquez sur l'image en miniature.
{% include_relative snippets/snippet-sunchannel.md %}
{% include_relative snippets/snippet-skychannel.md %}

## Arri�re-plan avanc�
{: #advanced-background}
Les param�tres de l'arri�re-plan avanc� contr�lent les environnements qui ne sont pas visibles dans les rendus, mais qui se voient dans les r�flexions et r�fractions sur les objets. Il est ainsi possible d'avoir un environnement visible diff�rent de celui utilis� pour les r�fractions et r�fractions sur les objets. Par exemple, dans l'illustration ci-dessous, l'arri�re-plan est noir mais l'environnement de r�flexion est une image HDR d'un int�rieur.

![images/reflectedbackground-002.png](images/reflectedbackground-002.png)
*Environnement normal (gauche) et environnement de r�flexion avec un ciel HDR (droite).*

### R�fl�chi
{: #advanced-background-reflected-sky}
Un environnement de r�flexion n'est pas visible dans l'image rendue mais il se refl�te dans les objets brillants.

#### Ciel
Les objets refl�tent le ciel tel qu'il est d�fini dans les param�tres [�clairage : Soleil et ciel](sun-and-sky-tabs.html).

#### Personnalis�
Les objets refl�tent un arri�re-plan constitu� [d'une couleur unie, d'un d�grad� de couleurs](#color-backgrounds), d'une [image](#environment-image) ou d'une image � grande plage dynamique [(HDR)](#hdr-image).

#### Arri�re-plan visible
Les objets refl�tent l'arri�re-plan visible tel qu'il est d�fini dans les  param�tres [Environnementt](environment-tab.html).

### R�fract�
{: #advanced-background-refracted-sky}

#### Ciel
Les objets r�fractent le ciel tel qu'il est d�fini dans les param�tres [�clairage : Soleil et ciel](sun-and-sky-tabs.html).

#### Personnaliser
Les objets r�fractent un arri�re-plan constitu� [d'une couleur unie, d'un d�grad� de couleurs](#color-and-gradient-backgrounds), d'une [image](#image) ou d'une image � grande plage dynamique [(HDR)](#hdr-image).

#### Arri�re-plan visible
Les objets r�fractent l'arri�re-plan visible tel qu'il est d�fini dans les  param�tres [Environnementt](environment-tab.html).

#### Objets alpha non transparents
{: #no-transparent-alpha-objects}
Le canal alpha ne sera pas visible � travers les objets transparents et le compositing du canal alpha ne sera pas possible � travers les objets transparents.
Si des images doivent �tre coll�es dans le canal alpha, d�sactivez ce param�tre.
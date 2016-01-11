---
title: D�calcomanies
---
1<!-- This is an old page, I am not sure it needs to be updated or translated,  The new Flamingo products used Rhino decals documented in Rhino help. -->

# {{page.title}}
Les d�calcomanies sont des placages d'image sans mosa�que appliqu�s directement sur les objets au lieu d'utiliser un mat�riau. Utilisez les d�calcomanies pour modifier une partie d�termin�e de la couleur, de la r�flectivit� ou du reliefs d'un objet.
Les d�calcomanies sont compos�es d'une seule image et ne sont pas dispos�es en mosa�que comme dans une [d�finition de mat�riaux](materials-tab.html).
Les d�calcomanies peuvent �tre utilis�es pour :

>Accrocher des illustrations sur des murs int�rieurs.
>Placer des �tiquettes ou des logos sur un produit.
>Ajouter des marques au mod�le.
>Cr�er des vitraux.

![images/freshmilk.png](images/freshmilk.png)
 **Remarque�:** Les aper�us des d�calcomanies ne sont visibles dans les vues filaires que si OpenGL est activ� pour le mode filaire. Le param�tre **Canal d'affichage** doit �tre d�fini sur **OpenGL** dans **Options**  &gt; **Vue**  &gt; **Modes d'affichage**  &gt; **Filaire**  &gt; **Autres param�tres**  &gt; **Canal d'affichage**.

## Positionnement de la d�calcomanie
{: #decal-list}
{: #decal-placement}

###  **Ajouter**
{: #add-decal}
1. S�lectionnez un ou plusieurs objets.
1. Dans le menu **�dition**, cliquez sur **Propri�t�s de l'objet**.
1. Dans la liste des **Propri�t�s**, cliquez sur **D�calcomanies de Flamingo nXt**.
1. Cliquer sur le bouton **Ajouter**.
1. Dans la bo�te de dialogue Ouvrir une image, choisissez un fichier image et cliquez sur Ouvrir**.
{% include_relative snippets/snippet-clearbitmapcache.md %}1. Dans la bo�te de dialogue Propri�t�s de la d�calcomanie, s�lectionnez les options et cliquez sur Positionner**.
1. Aux invites demandant les points, choisissez des points dans le mod�le pour positionner la d�calcomanie.
La s�quence pr�cise d�pend du type de d�calcomanie s�lectionn� : [Plane](#decal-planarmapping), [Cylindrique](#decal-cylindricalmapping) ou [Placage UV](#decal-uvmapping).

###  **Changer de position**
{: #decal-edit-placement}
1. Cliquez sur le bouton **Changer de position**.
1. � l'invite S�lectionner un point de contr�le, utilisez l'�diteur graphique pour changer la position de la d�calcomanie.
1. Appuyez sur **Entr�e** une fois termin�.

###  **Propri�t�s**
{: #decal-properties}
1. Cliquez sur le bouton **Propri�t�s**.
1. Dans la bo�te de dialogue Propri�t�s de la d�calcomanie, utilisez les diff�rentes options pour changer les caract�ristiques de la d�calcomanie.

###  **Supprimer**
{: #decal-delete}

>Cliquez sur le bouton **Supprimer**.

###  **D�placer vers le haut** / **D�placer vers le bas**
{: #decal-movedown}
{: #decal-moveup}
Quand plusieurs d�calcomanies sont superpos�es sur un seul objet, l'ordre dans lequel elles sont appliqu�es peut �tre important. Les d�calcomanies sont appliqu�es dans l'ordre dans lequel elles apparaissent dans la liste. La derni�re d�calcomanie de la liste est au-dessus des autres.

>Cliquez sur Vers le haut ou Vers le bas pour changer la position de la d�calcomanie dans la liste.

##### Pour placer une d�calcomanie plane
1. Aux diff�rentes invites, choisissez les points d�finissant la Largeur et la Direction de la hauteur**.
1. � l'invite S�lectionner un point de contr�le..., s�lectionnez un point de contr�le pour ajuster la taille, la rotation et la position de l'image.
Ou appuyez sur Entr�e pour terminer le placement de la d�calcomanie.

### Options

#### D�placer
D�place la d�calcomanie. Aux invites Point de d�part et Point final, entrez des points tout comme pour la commande D�placer de Rhino.

#### UtiliserRapportImage
La d�calcomanie est �tir�e en fonction du rapport de l'image originale.

##### Pour placer une d�calcomanie cylindrique
1. � l'invite, choisissez la position du centre du cylindre.
1. � l'invite S�lectionner un point de contr�le..., s�lectionnez un point de contr�le pour ajuster la taille, la rotation et la position de l'image.
Ou appuyez sur Entr�e pour terminer le placement de la d�calcomanie.

## D�finissez ou modifiez le placement de la d�calcomanie en utilisant l'application de contr�le
Note : Si vous utilisez un placage plan sur un objet courb�, toute l'image doit se trouver derri�re la surface de l'objet. Les portions de l'image qui se trouvent devant la surface ne seront pas visibles.

#### Pour modifier la largeur et la hauteur de la d�calcomanie en m�me temps

>Faites glisser les points de contr�le situ�s au sommet de l'application.

#### Pour changer la hauteur d'une d�calcomanie

>Faites glisser le point de contr�le situ� au milieu des bords sup�rieur et inf�rieur de l'application.

#### Pour changer la largeur�d'une d�calcomanie

>Faites glisser le point de contr�le situ� au milieu des bords gauche et droite de l'application.

#### Pour d�placer la d�calcomanie

>Faites glisser le point de contr�le situ� au centre de l'application.

#### Pour faire tourner la d�calcomanie

>Faites glisser le point de contr�le de l'axe x, y ou z sur l'ic�ne de l'application.

## Propri�t�s de la d�calcomanie
{: #dialogbox-editdecal}
La couleur de l'objet est remplac�e par la couleur de la d�calcomanie ou les deux couleurs sont m�lang�es. Ce r�sultat est celui le plus souvent recherch� lors de l'utilisation des d�calcomanies.

## Projection
{: #projection}
Le style de placage indique comment projeter la d�calcomanie sur l'objet. Vous pouvez dessiner des lignes de construction dans votre sc�ne pour vous aider � placer la d�calcomanie avec pr�cision. Un rectangle dessin� juste derri�re une surface peut servir de guide au moment de placer une d�calcomanie normale. Utilisez les accrochages aux objets pour un positionnement pr�cis.

### Cylindrique
{: #decal-cylindricalmapping}
Le placage cylindrique est utile pour placer des d�calcomanies sur des objets qui sont courb�s dans une seule direction, tels que les �tiquettes sur des bouteilles de vin.
Lorsque l'image est plaqu�e sur le cylindre, son axe vertical est plac� le long de l'axe du cylindre et son axe horizontal autour de celui-ci.
![images/cylindricaldecal-002.png](images/cylindricaldecal-002.png)

### Plan
{: #decal-planarmapping}
Ce style de placage est le plus commun. Il est utilis� pour effectuer un placage sur des objets plats ou pr�sentant une l�g�re une courbure.
Les sommets d�finissent la position de l'image et ses dimensions. Si le rectangle n'a pas les m�mes proportions que la texture, cette derni�re sera �tir�e ou comprim�e en cons�quence.
Lors d'un placage plan sur un objet courb�, toute la projection de l'image doit se trouver derri�re la surface de l'objet. Les portions de l'image qui se trouvent devant la surface ne seront pas visibles.
![images/decal-planar-001.png](images/decal-planar-001.png)

### Placage UV
{: #decal-uvmapping}
Les d�calcomanies utilisant un placage UV sont utiles pour les objets tels que les cheveux, les �corces d'arbres o� la d�calcomanie doit glisser et s'�tirer pour s'adapter � la surface.
La d�calcomanie couvre tout l'objet, il n'est pas possible de contr�ler le placement.
Le placage UV utilise la param�trisation u et v de la surface pour courber et �tirer l'image ; aucun positionnement manuel n'est donc n�cessaire.
![images/uvmapdecal-00.png](images/uvmapdecal-00.png)

### Parcourir
{: #file-browse}
Change le fichier image.

{% include_relative snippets/snippet-clearbitmapcache.md %}

## Intensit�
{: #decalmappingstrength}

### Couleur
{: #decal-color}
Fait varier l'intensit� relative de la couleur de l'image par rapport au mat�riau sous-jacent. Voir aussi, [Propri�t�s de la texture d'un mat�riau, Intensit� de la couleur](texture-properties-main.html#color).

### Relief
{: #decalmappingbump}
Les placages de relief cr�ent des ombres et des reflets simul�s sur la surface. Voir aussi, [Propri�t�s de la texture d'un mat�riau, Intensit� du relief](texture-properties-main.html#bump).

## Finition r�fl�chissante
{: #reflective-finish-and-highlight}
Les options de finition de la d�calcomanie sont les m�mes que celles de d�finition d'un mat�riau. Appliquez ces propri�t�s aux zones sp�cifiques de l'objet o� se trouve la d�calcomanie. Par d�faut, la finition des d�calcomanies est mate.

### Intensit�
D�finit l'intensit� du reflet. Des valeurs �lev�es augmentent la taille et l'intensit� du reflet. Voir [Propri�t�s avanc�es du mat�riau, Intensit�](advanced-material-properties-main.html#intensity).

### Nettet�
D�finit la taille du reflet. De petites valeurs donnent un reflet plus ample ; de grandes valeurs concentrent le reflet sur une plus petite zone. Voir [Propri�t�s avanc�es du mat�riau, Nettet�](advanced-material-properties-main.html#sharpness).

### M�tallique
D�finit la m�me couleur pour le reflet que pour la couleur de base de l'objet. Voir [Propri�t�s avanc�es du mat�riau : M�tallique](advanced-material-properties-main.html#metallic).
{% include_relative snippets/snippet-linking.md %}
{% include_relative snippets/snippet-masking.md %}
## Param�tres avanc�s
{: #advanced}

### Double face
{: #double}
La d�calcomanie appara�t sur la face arri�re de la surface sur laquelle elle est plac�e, ainsi que sur la face avant.

### Miroir
{: #mirror}
Copie sym�triquement l'image de la d�calcomanie.

## Direction de projection
{: #projection-direction}

### Arri�re
Projette la d�calcomanie � partir de la face arri�re de l'image de la d�calcomanie.
![images/projectionbackward1.png](images/projectionbackward1.png)Avant (gauche), arri�re (droite)

### Avant
Projette la d�calcomanie � partir de la face avant de l'image de la d�calcomanie.
![images/projectionforward1.png](images/projectionforward1.png)Avant (gauche), arri�re (droite)

### Avant et Arri�re
Projette la d�calcomanie � partir des deux faces (avant et la face arri�re) de l'image de la d�calcomanie.
![images/projectionforwardandback.png](images/projectionforwardandback.png)Avant (gauche), arri�re (droite)

### Transparence
D�finit la transparence de la d�calcomanie. Voir [Transparence](advanced-material-properties-transparency.html).
Indice de r�fraction
D�finit l'indice de r�fraction de la d�calcomanie transparente. Voir [Indice de r�fraction](advanced-material-properties-transparency.html#index-of-refraction)
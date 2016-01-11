---
title: Propri�t�s de base du mat�riau
---
# ![images/paint.svg](images/paint.svg) {{page.title}}
Les mat�riaux de Flamingo sont d�finis par un ensemble de groupes de propri�t�s. Il s'agit de mat�riaux simples commun�ment utilis�s. Ces mat�riaux pr�sentent un ensemble tr�s simple de contr�les. Cela permet d'acc�der rapidement aux propri�t�s que vous pouvez modifier pour qu'un mat�riau paraisse diff�rent sans la complexit� des options suppl�mentaires. Pour la plupart des mat�riaux simples, seule la couleur a besoin d'�tre modifi�e pour obtenir un aspect diff�rent.

#### Types de mat�riaux simples�:

> ![images/newsolidcolormaterial.png](images/newsolidcolormaterial.png)[Couleur unie](#solid-color)
> ![images/newplasticmaterial.png](images/newplasticmaterial.png)[Plastique](#plastic)
> ![images/newmetalmaterial.png](images/newmetalmaterial.png)[M�tal](#metal)
> ![images/newglassmaterial.png](images/newglassmaterial.png)[Verre](#glass)
> ![images/newglossymaterial.png](images/newglossymaterial.png)[Brillant](#glossy)
> ![images/newclearfinishmaterial.png](images/newclearfinishmaterial.png)[ClearFinish](#clearfinish)
> ![images/newtexturedmaterial.png](images/newtexturedmaterial.png)[Textur� de Flamingo](#flamingo-textured)
> ![images/newtexturesetmaterial.png](images/newtexturesetmaterial.png)[Ensemble de textures](#texture-set)

Tous les mat�riaux peuvent �tre convertis en mat�riaux complexes. Les mat�riaux complexes pr�sentent tous les contr�les possibles afin de modifier un mat�riau dans Flamingo nXt. Pour avoir un contr�le maximum sur un mat�riau, utilisez les mat�riaux complexes ou convertissez votre mat�riau en mat�riau complexe. 

#### Les mat�riaux complexes sont divis�s en plusieurs groupes de propri�t�s�:

> [Nom](material-type-advanced.html#name)
> [Algorithme](material-type-advanced.html#procedures)
> [Propri�t�s avanc�es des mat�riaux](material-type-advanced.html#advanced-materials-properties)
> [Finition r�fl�chissante ](material-type-advanced.html#reflective-finish-and-highlight)
> [Propri�t�s de la transparence](material-type-advanced.html#transparency)
> [Textures algorithmiques](material-type-advanced.html#bump-patterns)
> [Textures d'image](material-type-advanced.html#textures)
> [Notes](material-type-advanced.html#notes)

Les mat�riaux sont enregistr�s dans le mod�le de Rhino. Des mat�riaux uniques peuvent avoir le m�me nom dans diff�rents mod�les de Rhino.

## Couleur unie
{: #solid-color}
Les mat�riaux avec couleur unie ont uniquement un [nom](material-type-advanced.html#name) et une [couleur](material-type-advanced.html#color).

![images/solidcolors.png](images/3-solidcolor.png)

{% include_relative snippets/snippet-material-name.md %}
{% include_relative snippets/snippet-material-color-select.md %}
{% include_relative snippets/snippet-material-advanced-editor.md %}

## Plastique
{: #plastic}
Les mat�riaux plastiques sont l�g�rement r�fl�chissants avec un [reflet](material-type-advanced.html#highlight-color) blanc.

![images/solidcolors.png](images/3-plastic.png)

{% include_relative snippets/snippet-material-name.md %}
{% include_relative snippets/snippet-material-color-select.md %}
{% include_relative snippets/snippet-material-advanced-editor.md %} Utilisez l'�diteur avanc� pour remplacer les r�glages de la [couleur du reflet](material-type-advanced.html#highlight-color), de l'[intensit�](material-type-advanced.html#intensity), de [Fresnel](material-type-advanced.html#fresnel) et de [nettet�](material-type-advanced.html#sharpness).

## M�tal
{: #metal}
Pour les mat�riaux m�talliques, la couleur du reflet est la m�me que la [couleur](material-type-advanced.html#color). Vous pouvez �galement contr�ler la [nettet�](material-type-advanced.html#sharpness) de la r�flexion. 

![images/solidcolors.png](images/3-metal.png)

{% include_relative snippets/snippet-material-name.md %}
{% include_relative snippets/snippet-material-color-select.md %}
#### Nettet�
Contr�le la nettet� ou le flou de la r�flexion. Voir la rubrique sur la [nettet�](material-type-advanced.html#sharpness) pour plus d'informations. 

{% include_relative snippets/snippet-material-advanced-editor.md %} Utilisez l'�diteur avanc� pour remplacer les r�glages de la [couleur du reflet](material-type-advanced.html#highlight-color), de l'[intensit�](material-type-advanced.html#intensity), de [Fresnel](material-type-advanced.html#fresnel) et de [type](material-type-advanced.html#type).

## Verre
{: #glass}
Les mat�riaux en verre ont une [couleur](material-type-advanced.html#color) et un [indice de r�fraction](advanced-material-properties-main.html#index-of-refraction).

![images/solidcolors.png](images/3-glass.png)

{% include_relative snippets/snippet-material-name.md %}
{% include_relative snippets/snippet-material-color-select.md %}
#### Indice de r�fraction
Contr�le l'inclinaison de la lumi�re lorsqu'elle passe � travers le mat�riau. Voir la rubrique [indice de r�fraction](advanced-material-properties-main.html#index-of-refraction) pour plus d'informations.

{% include_relative snippets/snippet-material-advanced-editor.md %} Utilisez l'�diteur avanc� pour remplacer les r�glages de la [couleur du reflet](material-type-advanced.html#highlight-color), de l'[intensit�](material-type-advanced.html#intensity), de [Fresnel](material-type-advanced.html#fresnel), de [nettet�](material-type-advanced.html#sharpness) et de  [transparence](material-type-advanced.html#transparency).

## Brillant
{: #glossy}
Les mat�riaux brillants pr�sentent une [intensit�](material-type-advanced.html#intensity) et [nettet�](material-type-advanced.html#sharpness) du reflet de faible valeur. 

![images/solidcolors.png](images/3-glossy.png)

{% include_relative snippets/snippet-material-name.md %}
{% include_relative snippets/snippet-material-color-select.md %}
#### Intensit�
Contr�le l'intensit� du reflet des lumi�res sur la surface. Voir la rubrique d�taill�e sur l'[intenst�](material-type-advanced.html#intensity) pour plus d'informations. 

#### Nettet� du reflet
Contr�le la nettet� (par rapport au flou) du point nettet� lumi�res sur la surface. Voir la rubrique d�taill�e sur la [nettet� du reflet](material-type-advanced.html#sharpness) pour plus d'informations.

{% include_relative snippets/snippet-material-advanced-editor.md %} Utilisez l'�diteur avanc� pour remplacer les r�glages de [Fresnel](material-type-advanced.html#fresnel) et de [type](material-type-advanced.html#type).

## ClearFinish
{: #clearfinish}
Le mat�riau ClearFinish simule la peinture des voitures, la porcelaine, la c�ramique, les  bois vernis ou tout autre mat�riau avec une couche en plastique ou un enduit lustr�. Le ClearFinish utilise le param�tre [Fresnel](material-type-advanced.html#fresnel) pour modifier la couleur du mat�riau en fonction de l'angle de vue. Ces mat�riaux pr�sentent une couleur profonde lorsque vous regardez directement la surface mais lorsque celle-ci s'�loignent de la vue en se courbant, ils deviennent de plus en plus r�fl�chissants. Les peintures de voiture, laqu�es ou satin�es, sont de bons exemples de ClearFinish.

![images/solidcolors.png](images/3-clearfinish.png)

{% include_relative snippets/snippet-material-name.md %}
{% include_relative snippets/snippet-material-color-select.md %}
{% include_relative snippets/snippet-material-advanced-editor.md %} Utilisez l'�diteur avanc� pour remplacer les r�glages de la [couleur du reflet](material-type-advanced.html#highlight-color), de l'[intensit�](material-type-advanced.html#intensity), de [Fresnel](material-type-advanced.html#fresnel) et de [nettet�](material-type-advanced.html#sharpness).

## Textur� de Flamingo 
{: #flamingo-textured}
Les mat�riaux textur�s utilisent des images pour d�finir des motifs et des couleurs. Le nom et la r�solution de l'image, la taille de la mosa�que ainsi que l'intensit� et la nettet� du reflet sont contr�lables. 

![images/solidcolors.png](images/3-texture.png)

{% include_relative snippets/snippet-material-name.md %}
{% include_relative snippets/snippet-material-color-select.md %}
#### Intensit�
Contr�le l'intensit� de la r�flexion en miroir de la surface. Voir la rubrique d�taill�e sur l'[intenst�](material-type-advanced.html#intensity) pour plus d'informations.

#### Nettet�
Contr�le la nettet� ou le flou de la r�flexion. Voir la rubrique sur la [nettet�](material-type-advanced.html#sharpness) pour plus d'informations.

#### Image
D�finit le placage d'image et les propri�t�s du mat�riau. Cette rubrique contient de nombreuses options. Voir la rubrique d�taill�e sur les [images](material-type-advanced.html#texture) pour plus d'informations. 

{% include_relative snippets/snippet-material-image-add-edit.md %}
{% include_relative snippets/snippet-material-advanced-editor.md %} Utilisez l'�diteur avanc� pour remplacer les r�glages de ce mat�riau. 

## Ensemble de textures
{: #texture-set}
Les [mat�riaux avec ensemble de textures](material-type-texture-set.html) sont un ensemble de coordonn�es de textures qui d�finissent un mat�riau.  Ces ensembles de coordonn�es peuvent �tre cr��s � partir de placages de textures externes qui contiennent des informations telles que les placages de d�placement, normaux ou de relief. Les placages de d�placement permettent de donner une profondeur au mat�riau. En combinant ces placages de texture dans un ensemble, il est possible de cr�er des mat�riaux tr�s r�alistes. Le [logiciel PixPlant](http://www.pixplant.com/) peut cr�er des ensembles de textures � partir d'une image standard.

![images/solidcolors.png](images/textureset.png)

{% include_relative snippets/snippet-material-name.md %}
#### Largeur et Hauteur
Contr�le la taille de toutes les textures de l'ensemble. Utilisez ce contr�le pour conserver une coh�rence au niveau de la taille et de l'alignement de toutes les images.

#### Intensit�
Contr�le l'intensit� de la r�flexion en miroir de la surface. Voir la rubrique d�taill�e sur l'[intenst�](material-type-advanced.html#intensity) pour plus d'informations.

#### Nettet�
Contr�le la nettet� ou le flou de la r�flexion. Voir la rubrique sur la [nettet�](material-type-advanced.html#sharpness) pour plus d'informations.

#### Types
Contr�le le type de r�flexion sur la surface. Voir la rubrique d�taill�e sur le [type](material-type-advanced.html#type) pour plus d'informations.

### Placages de texture
Le tableau des placages de texture affiche la liste des textures faisant partie de l'ensemble. Cliquez avec le bouton droit dans le tableau pour ajouter, supprimer ou modifier les textures de l'ensemble. 

#### Ajouter des placages...
Utilisez cette commande du menu contextuel pour ajouter de nouvelles textures dans la liste. Plusieurs textures peuvent �tre ajout�es en m�me temps. Si les noms des textures incluent des suffixes pour un des types de placage, celui-ci est automatiquement ajout�. Par exemple, si une texture comprend *-normal* dans son nom, elle sera automatiquement marqu�e comme un placage normal. 

#### Supprimer un placage
Cette commande du menu contextuel supprimera un placage de texture dans le tableau. 

#### Couleur
Ce type de placage contribue � la couleur visible de la texture. Pour plus d'informations, voir [Type de placage standard](material-image-properties.html#standard)

#### Relief
Le placage de relief utilisera l'�chelle de gris de la texture pour simuler une modification de la hauteur ou u relief sur le mat�riau. Pour plus d'informations, voir [Placage de relief avanc�](material-image-properties.html#bump)

#### Normal
Les placages normaux sont des placages de relief sp�ciaux qui utilisent le canal rouge, vert et bleu de l'image pour ajuster la direction de relief au niveau de chaque pixel. Le canal bleu repr�sentant la direction Z du relief, les images tendent � prendre une teinte bleue. Pour plus d'informations, voir [Placage normal avanc�](material-image-properties.html#normal)

#### Sp�culaire
Un placage sp�culaire utilise les couleurs de l'�chelle de gris du mat�riau pour contr�ler la quantit� de r�flexion dans l'image en ce point. Pour plus d'informations, voir [Placage de transparence avanc�](material-image-properties.html#transparency)

#### Opacit�
Un placage d'opacit� contr�le la transparence d'un mat�riau au niveau de chaque pixel � partir de l'�chelle de gris de l'image. Pour plus d'informations, voir [Placage normal avanc�](material-image-properties.html#normal)

#### D�placement
Un placage de d�placement d�placera le maillage de rendu en fonction de l'�chelle de gris du placage. Pour plus d'informations, voir [Placage de d�placement avanc�](material-image-properties.html#displacement)

### Mat�riau complexe
Le mat�riau [avanc� de Flamingo](material-type-advanced) contient un ensemble complet de propri�t�s.  Si aucun de ces mat�riaux simples ne fonctionne, utilisez le mat�riau [avanc� de Flamingo](material-type-advanced) pour disposer d'une flexibilit� maximale.
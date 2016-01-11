---
title: Options du rendu
---

# ![images/flamingotab.svg](images/flamingotab.svg) {{page.title}}
L'onglet Rendu contr�le les principales propri�t�s du rendu final. Utilisez cet onglet pour contr�ler la qualit� et la dur�e d'un rendu. La r�solution de l'image finale est un des param�tres qui a le plus d'influence sur le temps de rendu global.

Note : Nous vous conseillons de garder une r�solution de rendu faible pour les rendus d'essai. Utilisez les r�solutions �lev�es uniquement pour les rendus finaux.

#### O� puis-je trouver les contr�les d'�clairage de Flamingo ?

 1. ![images/options.png](images/options.png)Barres d'outils >![images/flamingo-icon.png](images/flamingo-icon.png)Barre d'outils de Flamingo nXt > Onglet Options du rendu
 1. ![images/menuicon.png](images/menuicon.png)Menus > Flamingo nXt 5.0 > Montrer le panneau de configuration > Flamingo nXt > onglet Options du rendu


## Fen�tre � rendre
{: #viewtorender}
D�finit la vue que Flamingo nXt 5 utilisera pour le rendu.  Ce param�tre est  utile lorsque vous travaillez sur le mod�le et le rendu et qu'une vue en particulier doit toujours �tre utilis�e pour le rendu.  La vue en perspective est souvent la vue int�ressante par exemple.  En d�finissant cette option, vous n'�tes plus oblig� de v�rifier que la vue est active avant de lancer le rendu.

#### Vue active
Utilisez cette option pour utiliser la vue active lors du rendu.  Il s'agit du param�tre par d�faut.

#### Liste des fen�tres disponibles
Cette liste affiche toutes les vues nomm�es du mod�le. S�lectionnez la vue nomm�e qui devrait toujours �tre utilis�e pour le rendu. 

## R�solution de rendu
{: #resolution}
La r�solution de rendu est un des param�tres les plus importants.  Cette option d�finit la taille et la r�solution de l'image � enregistrer dans le fichier de Rhino.  Le temps de rendu est exponentiellement proportionnelle � la r�solution. Il est donc important de manipuler ce param�tre avec pr�caution. 

#### Pixels totaux
{: #resolutionimagepixels}
D�finit le nombre total de pixels dans le rendu final, en utilisant la vue actuelle pour d�terminer la proportion hauteur/largeur.  Ce param�tre est tr�s int�ressant � utiliser pour les rendus. C'est la meilleure option pour que le rendu concorde avec la vue actuelle. Il est tr�s facile d'augmenter ou de diminuer la r�solution de l'image en changeant simplement le nombre total de pixels. 

### R�solution de la fen�tre
Utilise la taille de la fen�tre en pixels pour d�terminer la taille de l'image rendue.  Ceci permet de cr�er une reproduction � l'�chelle des proportions et de la r�solution de la fen�tre.  Ce mode est utile mais peut ralentir consid�rablement le rendu d'une fen�tre plein �cran par rapport � une fen�tre occupant un quart d'�cran comme dans la configuration standard.

### Taille de l'image
{: #resolutionprintedsize}
La taille de l'image d�finira la r�solution finale � partir de plusieurs variables.  C'est la meilleure option pour obtenir une taille et une r�solution exactes. Si la hauteur et la largeur du rendu final ne correspondent pas aux proportions de la vue rendue, la vue peut �tre tronqu�e verticalement ou horizontalement. Note : Ces options peuvent donner des rendus de tr�s haute r�solution pouvant prendre tr�s longtemps.  Utilise ces contr�les pour des rendus finaux haute r�solution.

Quatre types d'unit�s peuvent �tre utilis�s�:

>Pixels
>Pouces
>Millim�tres
>Centim�tres

#### Pixels
D�finit les pixels comme unit�s de l'image rendue. Utilisez ce param�tre pour d�finir simplement la largeur et la hauteur du rendu final en utilisant le nombre de pixels. 

#### Pouces
D�finit les pouces comme unit�s de mise en page. Les pouces sont utilis�s en combinaison avec les param�tres de r�solution pour d�terminer la r�solution finale de l'image rendue.  Pour d�terminer la r�solution finale, multipliez le nombre de pouces sur la largeur�et la hauteur par la valeur de r�solution en PPP.

#### Millim�tres
D�finit les millim�tres comme unit�s de mise en page. Les millim�tres sont utilis�s en combinaison avec les param�tres de r�solution pour d�terminer la r�solution finale de l'image rendue.  Pour d�terminer la r�solution finale, multipliez le nombre de millim�tres sur la largeur�et la hauteur par la valeur de r�solution en points par millim�tre.

#### Centim�tres
D�finit les centim�tres comme unit�s de mise en page. Les centim�tres sont utilis�s en combinaison avec les param�tres de r�solution pour d�terminer la r�solution finale de l'image rendue.  Pour d�terminer la r�solution finale, multipliez le nombre de centim�tres sur la largeur�et la hauteur par la valeur de r�solution en points par centim�tre.

#### Appliquer les proportions de la vue
Utilisez ce param�tre pour conserver les proportions entre la largeur et la hauteur de la vue actuelle. Vous vous assurez ainsi que toute la vue est rendue dans l'image finale.

#### Largeur
Largeur de l'image imprim�e dans les unit�s actuelles.  Multipliez ce param�tre par le param�tre de r�solution pour obtenir la taille de l'image finale en nombre de pixels.

#### Hauteur
Hauteur de l'image imprim�e en unit�s actuelle.  Multipliez ce param�tre par le param�tre de r�solution pour obtenir la taille de l'image finale en nombre de pixels.

### R�solution
{: #printsizepixelsperunit}
{: #printsizedpi}
{: #printsizeresolution}

#### Affichage
L'image est rendue en utilisant la r�solution de la fen�tre en PPP. Il s'agit de la densit� de pixels sur un appareil. Cette valeur est normalement exprim�e en [points par pouce (PPP)](https://fr.wikipedia.org/wiki/Point_par_pouce).

#### Personnaliser
L'image est rendue avec une r�solution personnalis�e. Tapez la r�solution personnalis�e pour la largeur et la hauteur dans la case **Pixels par: **.

#### Imprimante, qualit� brouillon
D�finit la r�solution sur 100 pixels par pouce ou 4 pixels par mm.

#### Imprimante, qualit� normale
D�finit la r�solution sur 150 pixels par pouce ou 6 pixels par mm.

#### Imprimante, haute qualit�
D�finit la r�solution sur 300 pixels par pouce ou 12 pixels par mm. Il s'agit d'une r�solution assez �lev�e pour le rendu. Elle fonctionne pour les petits rendus mais pour un grand poster ou des rendus de la taille d'un mur, la r�solution globale peut finir tr�s �lev�e avec ce param�tre. Les r�solutions �lev�es donnent des temps de rendu tr�s longs. 

#### Pixels par
Lorsque le contr�le de la r�solution est sur Personnaliser, utilisez cette case pour d�finir la r�solution par unit� s�lectionn�e. Lorsque vous s�lectionnez une r�solution pr�d�finie, cette valeur indique la r�solution actuelle.

## Profondeur de champ
{: #depthoffieldoption}
Cet effet cr�e un flou de profondeur de champ qui imite un objectif d'appareil-photo. Un objectif ne peut effectuer sa mise au point qu'� une distance pr�cise mais la baisse de nettet� se fait progressivement autour de la distance focale.

#### Activ�
Active l'effet de profondeur de champ.

#### Intensit�
Contr�le la taille de la zone de mise au point. Une intensit� nulle permet d'avoir une image enti�rement nette. L'augmentation de l'intensit� rend les zones en dehors de la distance focale plus flou et diminue la taille de la zone nette.

#### Distance focale
{: #focaldistance}
D�finit la distance pour la profondeur de champ. La distance autour du point du champ de profondeur � laquelle les objets seront nets. Si la Distance focale est d�finie � 10 unit�s, les objets se trouvant � 7 unit�s derri�re le point du champ de profondeur et � 3 unit�s devant seront nets.

#### S�lectionner >>
Choisissez un point dans le mod�le pour la distance focale.

## Moteur de rendu
{: #render-engine}
Flamingo poss�de trois moteurs de rendu diff�rents.  Chaque moteur de rendu produira des r�sultats l�g�rement diff�rents dans des conditions de rendu normales. 

Flamingo utilise des techniques de rendu progressif � plusieurs �tapes pour cr�er les images. Les �tapes progressives peuvent donner des d�fauts dans le rendu. Ces d�fauts sont des effets produits avant la fin du rendu. Techniquement, les trois moteurs de rendu produiront le m�me rendu apr�s un temps suffisant. Mais dans la r�alit� le temps est toujours un facteur de contrainte. Il convient donc de choisir le moteur de rendu qui donnera le meilleur rendu de la sc�ne apr�s le plus petit nombre d'�tapes.

Il est facile de simplement s�lectionner un moteur de rendu diff�rent puis de lancer le rendu afin de voir le r�sultat.

### D�faut
L'algorithme par d�faut produit une simulation de tr�s haute qualit�. Le moteur par d�faut est un bon moteur de rendu pour une grande vari�t� de sc�nes.  Les deux autres moteurs de rendu pr�sentent des atouts importants mais �galement de grandes faiblesses. Le moteur par d�faut est un bon point de d�part. 

Il pr�sente un d�faut tr�s voyant dans les premi�res passes. Il s'agit d'ombres durs se superposant. Ces ombres seront adoucies au fur et � mesure de l'avancement du rendu. Le moteur par d�faut permet ainsi de donner un r�sultat plus rapidement mais peut prendre plus de passes pour adoucir r�ellement toutes les ombres.

La diff�rence au niveau de la qualit� entre la m�thode par d�faut et le Path tracer peut �tre  subtile, en particulier si l'�clairage indirect est activ�. La diff�rence de qualit� n'est peut-�tre pas assez importante compar�e au temps de traitement en plus.

### Path tracer
{: #path-tracer}
Le Path Tracer commence par afficher une image avec des grains qui est am�lior�e � chaque passe pour devenir de plus en plus nette. Ce processus est appel� la convergence*. Le Path Tracer peut apporter une meilleure finition pour beaucoup de mod�les (avec une configuration simple) mais le calcul est plus complexe et prend donc plus de temps. **Remarque�:** Ce moteur peut entra�ner l'apparition de points brillants et d'un effet mouchet� pendant le processus de rendu. Ces artefacts sont normaux et dispara�tront apr�s quelques passes.

Vous pouvez calculer certains effets complexes, tels que les caustiques ou la transparence flou  avec plus de pr�cision en utilisant le Path tracer. Les images rendues avec des instances, des plantes et des placages de d�placement peuvent converger plus vite. Le Path Tracer est presque toujours plus facile � configurer que la m�thode par d�faut. Les param�tres avanc�s tels que les r�flexions, les entr�es de lumi�re du jour et l'�clairage ambiant ne sont pas utilis�s lorsque le moteur Path tracer est s�lectionn�.

Les images rendues avec le Path tracer prendront normalement plus de temps � converger que les images rendues avec la m�thode par d�faut. Les simulations de l'�clairage naturel d'un int�rieur, en particulier les sc�nes dont les fen�tres sont assez petites, prennent beaucoup plus de temps.

### Hybride
Le moteur hybride essaie d'utiliser le meilleur des deux moteurs, D�faut et Path tracer, en utilisant des effets provenant de ces derniers. Il calcule toujours la lumi�re indirecte.  Le d�faut du moteur hybride est un important motif de points qui r�duira apr�s plusieurs passes. Dans certains cas il faudra un grand nombre de passes pour supprimer ce motif de points. Il peut s'agir du meilleur moteur pour de nombreux rendus.

###  **Param�tres avanc�s**
Ouvre la bo�te de dialogue Propri�t�s du document, section [Flamingo nXt](documentproperties-flamingo.html). Plusieurs propri�t�s avanc�es de rendu peuvent �tre d�finies ici pour jouer sur la qualit� finale du rendu. 
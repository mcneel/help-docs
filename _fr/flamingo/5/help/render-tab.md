---
title: Options du rendu
---

# ![images/flamingotab.svg](images/flamingotab.svg){: .inline} {{page.title}}
L'onglet Rendu contrôle les principales propriétés du rendu final.  Utilisez cet onglet pour contrôler la qualité et la durée d'un rendu. La résolution de l'image finale est un des paramètres qui a le plus d'influence sur le temps de rendu global.

Note : Nous vous conseillons de garder une résolution de rendu faible pour les rendus d'essai. Utilisez les résolutions élevées uniquement pour les rendus finaux.

#### Où puis-je trouver les contrôles d'éclairage de Flamingo ?

 1. ![images/options.png](images/options.png){: .inline} Barres d'outils >![images/flamingo-icon.png](images/flamingo-icon.png){: .inline} Barre d'outils de Flamingo nXt > Onglet Options du rendu
 1. ![images/menuicon.png](images/menuicon.png){: .inline} Menus > Flamingo nXt 5.0 > Montrer le panneau de configuration > Flamingo nXt > onglet Options du rendu


## Fenêtre à rendre
{: #viewtorender}
Définit la vue que Flamingo nXt 5 utilisera pour le rendu.  Ce paramètre est  utile lorsque vous travaillez sur le modèle et le rendu et qu'une vue en particulier doit toujours être utilisée pour le rendu.  La vue en perspective est souvent la vue intéressante par exemple.  En définissant cette option, vous n'êtes plus obligé de vérifier que la vue est active avant de lancer le rendu.

#### Vue active
Utilisez cette option pour utiliser la vue active lors du rendu.  Il s'agit du paramètre par défaut.

#### Liste des fenêtres disponibles
Cette liste affiche toutes les vues nommées du modèle. Sélectionnez la vue nommée qui devrait toujours être utilisée pour le rendu. 

## Résolution de rendu
{: #resolution}
La résolution de rendu est un des paramètres les plus importants.  Cette option définit la taille et la résolution de l'image à enregistrer dans le fichier de Rhino.  Le temps de rendu est exponentiellement proportionnel à la résolution. Il est donc important de manipuler ce paramètre avec précaution. 

#### Pixels totaux
{: #resolutionimagepixels}
Définit le nombre total de pixels dans le rendu final, en utilisant la vue actuelle pour déterminer la proportion hauteur/largeur.  Ce paramètre est très intéressant à utiliser pour les rendus. C'est la meilleure option pour que le rendu concorde avec la vue actuelle. Il est très facile d'augmenter ou de diminuer la résolution de l'image en changeant simplement le nombre total de pixels. 

### Résolution de la fenêtre
Utilise la taille de la fenêtre en pixels pour déterminer la taille de l'image rendue.  Ceci permet de créer une reproduction à l'échelle des proportions et de la résolution de la fenêtre.  Ce mode est utile mais peut ralentir considérablement le rendu d'une fenêtre plein écran par rapport à une fenêtre occupant un quart d'écran comme dans la configuration standard.

### Taille de l'image
{: #resolutionprintedsize}
La taille de l'image définira la résolution finale à partir de plusieurs variables.  C'est la meilleure option pour obtenir une taille et une résolution exactes. Si la hauteur et la largeur du rendu final ne correspondent pas aux proportions de la vue rendue, la vue peut être tronquée verticalement ou horizontalement. Note : Ces options peuvent donner des rendus de très haute résolution pouvant prendre très longtemps.  Utilisez ces contrôles pour des rendus finaux haute résolution.

Quatre types d'unités peuvent être utilisés :

* Pixels
* Pouces
* Millimètres
* Centimètres

#### Pixels
Définit les pixels comme unités de l'image rendue. Utilisez ce paramètre pour définir simplement la largeur et la hauteur du rendu final en utilisant le nombre de pixels. 

#### Pouces
Définit les pouces comme unités de mise en page. Les pouces sont utilisés en combinaison avec les paramètres de résolution pour déterminer la résolution finale de l'image rendue.  Pour déterminer la résolution finale, multipliez le nombre de pouces sur la largeur et la hauteur par la valeur de résolution en PPP.

#### Millimètres
Définit les millimètres comme unités de mise en page. Les millimètres sont utilisés en combinaison avec les paramètres de résolution pour déterminer la résolution finale de l'image rendue.  Pour déterminer la résolution finale, multipliez le nombre de millimètres sur la largeur et la hauteur par la valeur de résolution en points par millimètre.

#### Centimètres
Définit les centimètres comme unités de mise en page. Les centimètres sont utilisés en combinaison avec les paramètres de résolution pour déterminer la résolution finale de l'image rendue.  Pour déterminer la résolution finale, multipliez le nombre de centimètres sur la largeur et la hauteur par la valeur de résolution en points par centimètre.

#### Appliquer les proportions de la vue
Utilisez ce paramètre pour conserver les proportions entre la largeur et la hauteur de la vue actuelle. Vous vous assurez ainsi que toute la vue est rendue dans l'image finale.

#### Largeur
Largeur de l'image imprimée dans les unités actuelles.  Multipliez ce paramètre par le paramètre de résolution pour obtenir la taille de l'image finale en nombre de pixels.

#### Hauteur
Hauteur de l'image imprimée en unités actuelle.  Multipliez ce paramètre par le paramètre de résolution pour obtenir la taille de l'image finale en nombre de pixels.

### Résolution
{: #printsizepixelsperunit}
{: #printsizedpi}
{: #printsizeresolution}

#### Affichage
L'image est rendue en utilisant la résolution de la fenêtre en PPP. Il s'agit de la densité de pixels sur un appareil. Cette valeur est normalement exprimée en [points par pouce (PPP)](https://fr.wikipedia.org/wiki/Point_par_pouce).

#### Personnalisée
L'image est rendue avec une résolution personnalisée. Tapez la résolution personnalisée pour la largeur et la hauteur dans la case **Pixels par: **.

#### Imprimante, qualité brouillon
Définit la résolution sur 100 pixels par pouce ou 4 pixels par mm.

#### Imprimante, qualité normale
Définit la résolution sur 150 pixels par pouce ou 6 pixels par mm.

#### Imprimante, qualité élevée
Définit la résolution sur 300 pixels par pouce ou 12 pixels par mm. Il s'agit d'une résolution assez élevée pour le rendu. Elle fonctionne pour les petits rendus mais pour un grand poster ou des rendus de la taille d'un mur, la résolution globale peut finir très élevée avec ce paramètre. Les résolutions élevées donnent des temps de rendu très longs. 

#### Pixels par
Lorsque le contrôle de la résolution est sur Personnalisée, utilisez cette case pour définir la résolution par unité sélectionnée. Lorsque vous sélectionnez une résolution prédéfinie, cette valeur indique la résolution actuelle.

## Profondeur de champ
{: #depthoffieldoption}
Cet effet crée un flou de profondeur de champ qui imite un objectif d'appareil-photo. Un objectif ne peut effectuer sa mise au point qu'à une distance précise mais la baisse de netteté se fait progressivement autour de la distance focale.

#### Activé
Active l'effet de profondeur de champ.

#### Intensité
Contrôle la taille de la zone de mise au point. Une intensité nulle permet d'avoir une image entièrement nette. L'augmentation de l'intensité rend les zones en dehors de la distance focale plus flou et diminue la taille de la zone nette.

#### Distance focale
{: #focaldistance}
Définit la distance pour la profondeur de champ. La distance autour du point du champ de profondeur à laquelle les objets seront nets. Si la Distance focale est définie à 10 unités, les objets se trouvant à 7 unités derrière le point du champ de profondeur et à 3 unités devant seront nets.

#### Sélectionner
Choisissez un point dans le modèle pour la distance focale.

## Moteur de rendu
{: #render-engine}
Flamingo possède trois moteurs de rendu différents.  Chaque moteur de rendu produira des résultats légèrement différents dans des conditions de rendu normales. 

Flamingo utilise des techniques de rendu progressif à plusieurs étapes pour créer les images. Les étapes progressives peuvent donner des défauts dans le rendu. Ces défauts sont des effets produits avant la fin du rendu. Techniquement, les trois moteurs de rendu produiront le même rendu après un temps suffisant. Mais dans la réalité le temps est toujours un facteur de contrainte. Il convient donc de choisir le moteur de rendu qui donnera le meilleur rendu de la scène après le plus petit nombre d'étapes.

Il est facile de simplement sélectionner un moteur de rendu différent puis de lancer le rendu afin de voir le résultat.

### Défaut
L'algorithme par défaut produit une simulation de très haute qualité. Le moteur par défaut est un bon moteur de rendu pour une grande variété de scènes.  Les deux autres moteurs de rendu présentent des atouts importants mais également de grandes faiblesses. Le moteur par défaut est un bon point de départ. 

Il présente un défaut très voyant dans les premières passes. Il s'agit d'ombres dures se superposant. Ces ombres seront adoucies au fur et à mesure de l'avancement du rendu. Le moteur par défaut permet ainsi de donner un résultat plus rapidement mais peut prendre plus de passes pour adoucir réellement toutes les ombres.

La différence au niveau de la qualité entre la méthode par défaut et le Path tracer peut être  subtile, en particulier si l'éclairage indirect est activé. La différence de qualité n'est peut-être pas assez importante comparée au temps de traitement en plus.

### Path tracer
{: #path-tracer}
Le Path Tracer commence par afficher une image avec des grains qui est améliorée à chaque passe pour devenir de plus en plus nette. Ce processus est appelé la *convergence*. Le Path Tracer peut apporter une meilleure finition pour beaucoup de modèles (avec une configuration simple) mais le calcul est plus complexe et prend donc plus de temps. **Remarque :** Ce moteur peut entraîner l'apparition de points brillants et d'un effet moucheté pendant le processus de rendu. Ces défauts sont normaux et disparaîtront après quelques passes.

Vous pouvez calculer certains effets complexes, tels que les caustiques ou la transparence floue  avec plus de précision en utilisant le Path tracer. Les images rendues avec des instances, des plantes et des placages de déplacement peuvent converger plus vite. Le Path Tracer est presque toujours plus facile à configurer que la méthode par défaut. Les paramètres avancés tels que les réflexions, les entrées de lumière du jour et l'éclairage ambiant ne sont pas utilisés lorsque le moteur Path tracer est sélectionné.

Les images rendues avec le Path tracer prendront normalement plus de temps à converger que les images rendues avec la méthode par défaut. Les simulations de l'éclairage naturel d'un intérieur, en particulier les scènes dont les fenêtres sont assez petites, prennent beaucoup plus de temps.

### Hybride
Le moteur hybride essaie d'utiliser le meilleur des deux moteurs, Défaut et Path tracer, en utilisant des effets provenant de ces derniers. Il calcule toujours la lumière indirecte.  Le défaut du moteur hybride est un important motif de points qui réduira après plusieurs passes. Dans certains cas il faudra un grand nombre de passes pour supprimer ce motif de points. Il peut s'agir du meilleur moteur pour de nombreux rendus.

###  **Paramètres avancés**
Ouvre la boîte de dialogue Propriétés du document, section [Flamingo nXt](documentproperties-flamingo.html). Plusieurs propriétés avancées de rendu peuvent être définies ici pour jouer sur la qualité finale du rendu. 
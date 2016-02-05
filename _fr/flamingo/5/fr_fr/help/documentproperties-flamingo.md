---
title: Propriétés du document
---


# ![images/options.svg](images/options.svg){: .inline} {{page.title}}
Ces paramètres concernent uniquement le modèle actuel. Le temps nécessaire au calcul du rendu et la qualité désirée sont proportionnels.

#### Où puis-je trouver cette commande ?
<!-- These locations are not correct.  They need to be updated. -->

 1. ![images/icon-render.png](images/icon-render.png){: .inline} Barres d'outils Outils  pour le rendu > ![images/environments.png](images/environments.png){: .inline} Éditeur de matériaux
 1. ![images/menuicon.png](images/menuicon.png){: .inline} Menus > Rendu > Éditeur d'environnement
 1. Commande > ÉditeurEnvironnement

## Matériaux
{: #materials}
Utilisez ces contrôles pour changer rapidement la façon dont Flamingo calcule le rendu des surfaces.  Ces paramètres ne changeront pas les matériaux assignés aux objets et aux calques mais ils changeront la façon dont Flamingo produit la couleur sur chaque surface. 

#### Utiliser des matériaux
{: #use-materials}
Le rendu est réalisé en utilisant les matériaux créés dans Flamingo nXt et Rhino. Les objets sans matériau sont rendus en blanc. Si aucune des options, Utiliser des matériaux ni Utiliser les couleurs de l'objet, n'est cochée, tous les objets seront rendus en blanc. 

#### Utiliser la couleur de l'objet
{: #use-object-color}
Le rendu est réalisé en utilisant les couleurs assignées à l'objet dans ses propriétés ou dans son calque. Remarque : Les deux cases, Utiliser des matériaux et Utiliser la couleur de l'objet peuvent être cochées en même temps. Dans ce cas, si un matériau est assigné à l'objet, il est utilisé pour le rendu ; sinon, la couleur de l'objet ou du calque est utilisée.

#### Canal d'incandescence
{: #channel}
Les matériaux comprenant un niveau d'incandescence s'allumeront mais n'éclaireront pas les autres objets. (Marquez l'objet comme lumière pour éclairer les autres objets.)  Définissez l'incandescence avec un canal afin de permettre d'ajuster la luminosité après le rendu sans avoir à recalculer toute la scène. 

## Rebonds
{: #bounces}
Lorsqu'un rayon entre dans une scène, il rebondit plusieurs fois avant d'être éliminé.  En limitant le nombre de rebonds, il est possible d'accélérer le rendu de façon considérable. Mais si la limite est trop faible, certains effets peuvent manquer ou apparaître en noir.  Les valeurs par défaut conviennent parfaitement pour la plupart des rendus mais elles doivent être modifiées dans certains cas.

#### Réflectif
{: #reflective-bounces}
Détermine combien de niveaux de réflexions sont permis ; en d'autres termes, combien de fois un rayon de lumière se réfléchira dans les objets. Si vous entrez 0, il n'y aura pas de réflexions. De plus grandes valeurs entraînent des temps de rendu plus élevés. Augmentez cette valeur si une vue regarde une surface réfléchissante qui rebondit sur une vue réfléchissante adjacente et que les réflexions commencent à devenir complètement noires. 

#### Réfringent
{: #refractive-bounces}
Détermine combien de niveaux de réfractions sont permis ; en d'autres termes, combien de fois un rayon de lumière sera réfracté dans les objets. Une valeur nulle désactive les réfractions. De plus grandes valeurs entraînent des temps de rendu plus élevés. Augmentez cette valeur si une vue regarde à travers de nombreuses couches et apparaît finalement noire et non transparente. 

#### Indirecte
{: #indirect-bounces}
Détermine combien de niveaux de lumière indirecte sont permis ; en d'autres termes, combien de fois un rayon de lumière indirecte rebondira sur les objets. Si vous entrez 0, il n'y aura pas de réflexions. De plus grandes valeurs entraînent des temps de rendu plus élevés.

## Éclairage indirect
{: #indirect-settings}
Les paramètres d'éclairage indirect affectent uniquement les rayons qui rebondissent d'une surface et transportent la lumière vers une autre surface.

#### Étalement de la couleur
{: #color-bleed}
L'étalement de la couleur contrôle la quantité de couleur transférée dans un rebond de lumière indirect d'une surface vers une autre.  Par défaut, la valeur maximale est définie afin d'augmenter la dynamique du rendu. 

#### Réflexions de Monte Carlo
{: #monte-carlo}
Le paramètre de Monte Carlo dans l'éclairage indirect contrôle comment Flamingo échantillonne la lumière indirecte. Lorsqu'il est activé, la lumière indirecte devient très floue au cours des premières passes. Mais ensuite, au fur et à mesure des passes, l'effet général de Monte Carlo indirect sera un effet indirect plus subtil et potentiellement plus détaillé. Les scènes qui reposent fortement sur l'éclairage indirect peuvent tirer profit des réflexions indirectes de Monte Carlo. 

## Divers

#### Utiliser les lumières des calques désactivés
{: #uselightsonlayersthatareoff}
Permet d'utiliser les lumières qui se trouvent sur des calques désactivés ou qui sont cachées.

### Contraintes de rendu
{: #number-of-passes}
{: #time}
{: #render-constraints}
{% include_relative snippets/snippet-renderconstraints.md %}
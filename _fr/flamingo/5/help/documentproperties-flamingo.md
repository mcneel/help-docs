---
title: Propri�t�s du document de Flamingo nXt
---


# ![images/options.svg](images/options.svg) {{page.title}}
Ces param�tres concernent uniquement le mod�le actuel. Le temps n�cessaire au calcul du rendu et la qualit� d�sir�e sont proportionnels.

#### O� puis-je trouver cette commande ?
<!-- These locations are not correct.  They need to be updated. -->

 1. ![images/icon-render.png](images/icon-render.png)Barres d'outils Outils  pour le rendu > ![images/environments.png](images/environments.png) �diteur de mat�riaux
 1. ![images/menuicon.png](images/menuicon.png)Menus > Rendu > �diteur d'environnement
 1. Commande > �diteurEnvironnement

## Mat�riaux
{: #materials}
Utilisez ces contr�les pour changer rapidement la fa�on dont Flamingo calcule le rendu des surfaces.  Ces param�tres ne changeront pas les mat�riaux assign�s aux objets et aux calques mais ils changeront la fa�on dont Flamingo produit la couleur sur chaque surface. 

#### Utiliser des mat�riaux
{: #use-materials}
Le rendu est r�alis� en utilisant les mat�riaux cr��s dans Flamingo nXt et Rhino. Les objets sans mat�riau sont rendus en blanc. Si aucune des options, Utiliser des mat�riaux ni Utiliser les couleurs de l'objet, n'est coch�e, tous les objets seront rendus en blanc. 

#### Utiliser la couleur de l'objet
{: #use-object-color}
Le rendu est r�alis� en utilisant les couleurs assign�es � l'objet dans ses propri�t�s ou dans son calque. Remarque : Les deux cases, Utiliser des mat�riaux et Utiliser la couleur de l'objet peuvent �tre coch�es en m�me temps. Dans ce cas, si un mat�riau est assign� � l'objet, il est utilis� pour le rendu ; sinon, la couleur de l'objet ou du calque est utilis�e.

#### Canal d'incandescence
{: #channel}
Les mat�riaux comprenant un niveau d'incandescence s'allumeront mais n'�claireront pas les autres objets. (Marquez l'objet comme lumi�re pour �clairer les autres objets.)  D�finissez l'incandescence avec un canal afin de permettre d'ajuster la luminosit� apr�s le rendu sans avoir � recalculer toute la sc�ne. 

## Rebonds
{: #bounces}
Lorsqu'un rayon entre dans une sc�ne, il rebondit plusieurs fois avant d'�tre �limin�.  En limitant le nombre de rebonds, il est possible d'acc�l�rer le rendu de fa�on consid�rable. Mais si la limite est trop faible, certains effets peuvent manquer ou appara�tre en noir.  Les valeurs par d�faut conviennent parfaitement pour la plupart des rendus mais elles doivent �tre modifi�es dans certains cas.

#### R�flectif
{: #reflective-bounces}
D�termine combien de niveaux de r�flexions sont permis ; en d'autres termes, combien de fois un rayon de lumi�re se r�fl�chira dans les objets. Si vous entrez 0, il n'y aura pas de r�flexions. De plus grandes valeurs entra�nent des temps de rendu plus �lev�s. Augmentez cette valeur si une vue regarde une surface r�fl�chissante qui rebondit sur une vue r�fl�chissante adjacente et que les r�flexions commencent � devenir compl�tement noires. 

#### R�fringent
{: #refractive-bounces}
D�termine combien de niveaux de r�fractions sont permis ; en d'autres termes, combien de fois un rayon de lumi�re sera r�fract� dans les objets. Une valeur nulle d�sactive les r�fractions. De plus grandes valeurs entra�nent des temps de rendu plus �lev�s. Augmentez cette valeur si une vue regarde � travers de nombreuses couches et appara�t finalement noire et non transparente. 

#### Indirecte
{: #indirect-bounces}
D�termine combien de niveaux de lumi�re indirecte sont permis ; en d'autres termes, combien de fois un rayon de lumi�re indirecte rebondira sur les objets. Si vous entrez 0, il n'y aura pas de r�flexions. De plus grandes valeurs entra�nent des temps de rendu plus �lev�s.

## �clairage indirect
{: #indirect-settings}
Les param�tres d'�clairage indirect affectent uniquement les rayons qui rebondissent d'une surface et transportent la lumi�re vers une autre surface.

#### �talement de la couleur
{: #color-bleed}
L'�talement de la couleur contr�le la quantit� de couleur transf�r�e dans un rebond de lumi�re indirect d'une surface vers une autre.  Par d�faut, la valeur maximale est d�finie afin d'augmenter la dynamique du rendu. 

#### R�flexions de Monte Carlo
{: #monte-carlo}
Le param�tre de Monte Carlo dans l'�clairage indirect contr�le comment Flamingo �chantillonne la lumi�re indirecte. Lorsqu'il est activ�, la lumi�re indirecte devient tr�s floue au cours des premi�res passes. Mais ensuite, au fur et � mesure des passes, l'effet g�n�ral de Monte Carlo indirect sera un effet indirect plus subtil et potentiellement plus d�taill�. Les sc�nes qui reposent fortement sur l'�clairage indirect peuvent tirer profit des r�flexions indirectes de Monte Carlo. 

## Divers

#### Utiliser les lumi�res des calques d�sactiv�s
{: #uselightsonlayersthatareoff}
Permet d'utiliser les lumi�res qui se trouvent sur des calques d�sactiv�s ou qui sont cach�es.

### Contraintes de rendu
{: #number-of-passes}
{: #time}
{: #render-constraints}
{% include_relative snippets/snippet-renderconstraints.md %}
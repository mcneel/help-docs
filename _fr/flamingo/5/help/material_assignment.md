---
title: Assignations de matériaux
---

# ![images/paint.svg](images/paint.svg) {{page.title}}
Les objets de la scène possèdent une source de matériau, c'est-à-dire l'endroit où ils adoptent leur matériau de rendu. Les matériaux peuvent être assignés de différentes façons. La méthode utilisée pour assigner les matériaux a un rôle important sur la facilité de modification ultérieure du modèle.

Les matériaux peuvent être assignés de trois façons. Ces méthodes ont une relation de hiérarchie, ainsi une méthode en bas de liste remplacera une assignation plus haute dans la liste. 

 1. [Calques](#bylayer) - Tous les objets se trouvant sur le calque adopteront ce matériau, sauf s'ils sont inclus dans un bloc ou si un matériau leur est assigné spécifiquement. 
 2. [Parent](#byparent) - Cette assignation est utilisée pour les objets dans des blocs. Le matériau des objets dont l'assignation est définie par parent sera déterminé par l'insertion du bloc. 
 3. [Objets individuels](#byobject) - Les matériaux peuvent être assignés directement un objet, ce qui remplace toute autre assignation de matériau.

Nous recommandons d'assigner les matériaux par calque. L'assignation par calque permet de changer facilement le matériau de tous les objets se trouvant sur un calque. Utiliser l'assignation par objet si vous avez uniquement quelques objets que vous ne voulez pas placer sur des calques séparés.

Les fichiers importés peuvent utiliser ces trois assignations indifféremment. La plupart des fichiers importés utilisent l'assignation par objet.  La conversion du modèle en assignation par calque peut représenter beaucoup de travail mais elle peut être très utile si les matériaux de rendu doivent être modifiés.

Lorsque les matériaux sont assignés, ils sont enregistrés dans le modèle actuel.  La modification d'un matériau n'affectera pas ce matériau dans d'autres modèles.

## Assigner des matériaux aux calques
{: #bylayer}
Lorsque vous assignez un matériau par calque, celui-ci est assigné à tous les objets se trouvant sur ce calque. Il s'agit de la méthode d'assignation par défaut. Pour changer le matériau assigné à un calque, utilisez la boîte de dialogue [Calques](http://docs.mcneel.com/rhino/5/help/fr-fr/commands/layer.htm).
Note : Lorsqu'un matériau est supprimé dans l'[éditeur de matériaux](material-editor.html), tous les objets qui possédaient ce matériau retrouvent une assignation par calque.

##### Faire glisser un matériau sur un calque
{: #drag-dropmaterialtolayer}
1. Dans Rhino, ouvrez la boîte de dialogue [Calques](http://docs.mcneel.com/rhino/5/help/fr-fr/commands/layer.htm).
1. Dans la [liste des matériaux ](material-editor.html#material_list), dans l'onglet Bibliothèque ou l'onglet Éditeur de matériaux, déplacez un matériau sur le nom d'un calque dans la boîte de dialogue des [calques](http://docs.mcneel.com/rhino/5/help/fr-fr/commands/layer.htm).

##### Pour assigner un matériau à un calque
1. Dans Rhino, ouvrez la boîte de dialogue [Calques](http://docs.mcneel.com/rhino/5/help/fr-fr/commands/layer.htm).
1. Sélectionnez un ou plusieurs calques et cliquez dans la colonne Matériau.
1. Dans la boîte de dialogue Matériau du calque, sélectionnez un matériau dans la liste déroulante des matériaux.

##### Supprimer un matériau assigné à un calque
{: #detachmaterialfromlayer}
1. Dans Rhino, ouvrez la boîte de dialogue [Calques](http://docs.mcneel.com/rhino/5/help/fr-fr/commands/layer.htm).
1. Sélectionnez un ou plusieurs calques et cliquez dans la colonne Matériau.
1. Dans la boîte de dialogue Matériau du calque, sélectionnez le matériau par défaut dans la liste déroulante.

## Assigner un matériau par parent
{: #byparent}
Cette assignation est rarement utilisée mais très utile. Les objets faisant parti d'une occurrence de bloc conservent leur assignation par calque ou par objet.  Cependant, les objets qui utilisent l'assignation par parents adoptent le matériau de l'insertion de bloc.  Ainsi, les objets contenus dans une occurrence de bloc peuvent adopter le matériau du bloc parent. 

Par exemple, un modèle de voiture peut avoir des pneus sur le calque Pneus et des roues sur le calque Roues. Mais pour le rendu, la carrosserie de la voiture peut varier en fonction des occurrences de bloc individuelles.  Vous pouvez définir le matériau de la carrosserie de la voiture par parent,  puis assigner un matériau à l'insertion de bloc afin que seule la carrosserie adopte ce matériau.

##### Pour assigner un matériau par les propriétés objet
1. Sélectionnez des objets.
1. Dans le menu Édition, cliquez sur Propriétés de l'objet ![images/properties.png](images/properties.png) pour modifier l'objet. 
1. Dans la boîte de dialogue [Propriétés](properties-object.html), dans la section Matériau ![images/materialtab.png] (images/materialtab.png), sous Assigner par, cliquez sur Par parent. 

## Assigner un matériau à des objets
{: #byobject}
Vous pouvez assigner des matériaux des bibliothèques de matériaux à un calque ou un objet. Les matériaux de rendu sont assignés aux objets et sont utilisés par le système de rendu intégré dans Rhino.
Voir [Éditeur de matériaux](material-editor.html).

Nous recommandons d'assigner les matériaux par calque. N'assignez les matériaux par objet que si vous avez quelques objets que vous ne voulez pas placer sur des calques séparés.

##### Assigner un matériau par les propriétés objet
1. Sélectionnez des objets.
1. Dans le menu Édition, cliquez sur [Propriétés de l'objet![images/properties.png](images/properties.png) pour modifier l'objet.
1. Dans la boîte de dialogue [Propriétés](properties-object.html), dans la section Matériaux ![images/materialtab.png](images/materialtab.png) sous Assigner par, cliquez sur Par objet puis cliquez sur le matériau dans la liste.

##### Faire glisser un matériau sur un objet
{: #drag-dropmaterialtoobject}

 * Dans la [liste des matériaux ](material-editor.html#material_list), dans l'onglet Bibliothèque ou l'onglet Éditeur de matériaux, déplacez un matériau sur un objet. L'objet est affiché en surbrillance lorsque le curseur est au bon endroit pour déposer le matériau.

##### Assigner un matériau aux objets sélectionnés
1. Sélectionnez des objets.
1. Dans la [liste des matériaux ](material-editor.html#material_list), dans l'onglet Bibliothèque ou l'onglet Éditeur de matériaux, cliquez avec le bouton de droit sur un matériau dans la palette Matériaux du modèle. 
1. Dans le menu, cliquez sur Assigner aux objets sélectionnés.

##### Sélectionner des objets en fonction de leur matériau
{: #select-objects-with-material-assignment}
1. Dans la [liste des matériaux ](material-editor.html#material_list), dans l'onglet Bibliothèque ou l'onglet Éditeur de matériaux, cliquez avec le bouton de droit sur un Matériaux dans la palette Matériaux du modèle.
1. Dans le menu, cliquez sur Sélectionner les objets possédant ce matériau.

##### Supprimer un matériau assigné à un objet
{: #removematerialfromobject}
1. Sélectionnez des objets.
1. Dans le menu Édition, cliquez sur Propriétés de l'objet.
1. Dans la boîte de dialogue [Propriétés](properties-object.html), dans la section Matériau, sous Assigner par, sélectionnez Calque.
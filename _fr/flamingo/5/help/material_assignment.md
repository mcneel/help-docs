---
title: Assignations de mat�riaux
---

# ![images/paint.svg](images/paint.svg) {{page.title}}
Les objets de la sc�ne poss�dent une source de mat�riau, c'est-�-dire l'endroit o� ils adoptent leur mat�riau de rendu. Les mat�riaux peuvent �tre assign�s de diff�rentes fa�ons. La m�thode utilis�e pour assigner les mat�riaux a un r�le important sur la facilit� de modification ult�rieure du mod�le.

Les mat�riaux peuvent �tre assign�s de trois fa�ons. Ces m�thodes ont une relation de hi�rarchie, ainsi une m�thode en bas de liste remplacera une assignation plus haute dans la liste. 

 1. [Calques](#bylayer) - Tous les objets se trouvant sur le calque adopteront ce mat�riau, sauf s'ils sont inclus dans un bloc ou si un mat�riau leur est assign� sp�cifiquement. 
 2. [Parent](#byparent) - Cette assignation est utilis�e pour les objets dans des blocs. Le mat�riau des objets dont l'assignation est d�finie par parent sera d�termin� par l'insertion du bloc. 
 3. [Objets individuels](#byobject) - Les mat�riaux peuvent �tre assign�s directement un objet, ce qui remplace toute autre assignation de mat�riau.

Nous recommandons d'assigner les mat�riaux par calque. L'assignation par calque permet de changer facilement le mat�riau de tous les objets se trouvant sur un calque. Utiliser l'assignation par objet si vous avez uniquement quelques objets que vous ne voulez pas placer sur des calques s�par�s.

Les fichiers import�s peuvent utiliser ces trois assignations indiff�remment. La plupart des fichiers import�s utilisent l'assignation par objet.  La conversion du mod�le en assignation par calque peut repr�senter beaucoup de travail mais elle peut �tre tr�s utile si les mat�riaux de rendu doivent �tre modifi�s.

Lorsque les mat�riaux sont assign�s, ils sont enregistr�s dans le mod�le actuel.  La modification d'un mat�riau n'affectera pas ce mat�riau dans d'autres mod�les.

## Assigner des mat�riaux aux calques
{: #bylayer}
Lorsque vous assignez un mat�riau par calque, celui-ci est assign� � tous les objets se trouvant sur ce calque. Il s'agit de la m�thode d'assignation par d�faut. Pour changer le mat�riau assign� � un calque, utilisez la bo�te de dialogue [Calques](http://docs.mcneel.com/rhino/5/help/fr-fr/commands/layer.htm).
Note : Lorsqu'un mat�riau est supprim� dans l'[�diteur de mat�riaux](material-editor.html), tous les objets qui poss�daient ce mat�riau retrouvent une assignation par calque.

##### Faire glisser un mat�riau sur un calque
{: #drag-dropmaterialtolayer}
1. Dans Rhino, ouvrez la bo�te de dialogue [Calques](http://docs.mcneel.com/rhino/5/help/fr-fr/commands/layer.htm).
1. Dans la [liste des mat�riaux ](material-editor.html#material_list), dans l'onglet Biblioth�que ou l'onglet �diteur de mat�riaux, d�placez un mat�riau sur le nom d'un calque dans la bo�te de dialogue des [calques](http://docs.mcneel.com/rhino/5/help/fr-fr/commands/layer.htm).

##### Pour assigner un mat�riau � un calque
1. Dans Rhino, ouvrez la bo�te de dialogue [Calques](http://docs.mcneel.com/rhino/5/help/fr-fr/commands/layer.htm).
1. S�lectionnez un ou plusieurs calques et cliquez dans la colonne�Mat�riau.
1. Dans la bo�te de dialogue Mat�riau du calque, s�lectionnez un mat�riau dans la liste d�roulante des mat�riaux.

##### Supprimer un mat�riau assign� � un calque
{: #detachmaterialfromlayer}
1. Dans Rhino, ouvrez la bo�te de dialogue [Calques](http://docs.mcneel.com/rhino/5/help/fr-fr/commands/layer.htm).
1. S�lectionnez un ou plusieurs calques et cliquez dans la colonne�Mat�riau.
1. Dans la bo�te de dialogue Mat�riau du calque, s�lectionnez le mat�riau par d�faut dans la liste d�roulante.

## Assigner un mat�riau par parent
{: #byparent}
Cette assignation est rarement utilis�e mais tr�s utile. Les objets faisant parti d'une occurrence de bloc conservent leur assignation par calque ou par objet.  Cependant, les objets qui utilisent l'assignation par parents adoptent le mat�riau de l'insertion de bloc.  Ainsi, les objets contenus dans une occurrence de bloc peuvent adopter le mat�riau du bloc parent. 

Par exemple, un mod�le de voiture peut avoir des pneus sur le calque Pneus et des roues sur le calque Roues. Mais pour le rendu, la carrosserie de la voiture peut varier en fonction des occurrences de bloc individuelles.  Vous pouvez d�finir le mat�riau de la carrosserie de la voiture par parent,  puis assigner un mat�riau � l'insertion de bloc afin que seule la carrosserie adopte ce mat�riau.

##### Pour assigner un mat�riau par les propri�t�s objet
1. S�lectionnez des objets.
1. Dans le menu �dition, cliquez sur Propri�t�s de l'objet ![images/properties.png](images/properties.png) pour modifier l'objet. 
1. Dans la bo�te de dialogue [Propri�t�s](properties-object.html), dans la section Mat�riau ![images/materialtab.png] (images/materialtab.png), sous Assigner par, cliquez sur Par parent. 

## Assigner un mat�riau � des objets
{: #byobject}
Vous pouvez assigner des mat�riaux des biblioth�ques de mat�riaux � un calque ou un objet. Les mat�riaux de rendu sont assign�s aux objets et sont utilis�s par le syst�me de rendu int�gr� dans Rhino.
Voir [�diteur de mat�riaux](material-editor.html).

Nous recommandons d'assigner les mat�riaux par calque. N'assignez les mat�riaux par objet que si vous avez quelques objets que vous ne voulez pas placer sur des calques s�par�s.

##### Assigner un mat�riau par les propri�t�s objet
1. S�lectionnez des objets.
1. Dans le menu �dition, cliquez sur [Propri�t�s de l'objet![images/properties.png](images/properties.png) pour modifier l'objet.
1. Dans la bo�te de dialogue [Propri�t�s](properties-object.html), dans la section Mat�riaux ![images/materialtab.png](images/materialtab.png) sous Assigner par, cliquez sur Par objet puis cliquez sur le mat�riau dans la liste.

##### Faire glisser un mat�riau sur un objet
{: #drag-dropmaterialtoobject}

 * Dans la [liste des mat�riaux ](material-editor.html#material_list), dans l'onglet Biblioth�que ou l'onglet �diteur de mat�riaux, d�placez un mat�riau sur un objet. L'objet est affich� en surbrillance lorsque le curseur est au bon endroit pour d�poser le mat�riau.

##### Assigner un mat�riau aux objets s�lectionn�s
1. S�lectionnez des objets.
1. Dans la [liste des mat�riaux ](material-editor.html#material_list), dans l'onglet Biblioth�que ou l'onglet �diteur de mat�riaux, cliquez avec le bouton de droit sur un mat�riau dans la palette Mat�riaux du mod�le. 
1. Dans le menu, cliquez sur Assigner aux objets s�lectionn�s.

##### S�lectionner des objets en fonction de leur mat�riau
{: #select-objects-with-material-assignment}
1. Dans la [liste des mat�riaux ](material-editor.html#material_list), dans l'onglet Biblioth�que ou l'onglet �diteur de mat�riaux, cliquez avec le bouton de droit sur un Mat�riaux dans la palette Mat�riaux du mod�le.
1. Dans le menu, cliquez sur S�lectionner les objets poss�dant ce mat�riau.

##### Supprimer un mat�riau assign� � un objet
{: #removematerialfromobject}
1. S�lectionnez des objets.
1. Dans le menu �dition, cliquez sur Propri�t�s de l'objet.
1. Dans la bo�te de dialogue [Propri�t�s](properties-object.html), dans la section Mat�riau, sous Assigner par, s�lectionnez Calque.
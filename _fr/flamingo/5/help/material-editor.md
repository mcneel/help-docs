---
title: Panneau �diteur de mat�riaux
---

# ![images/paint.svg](images/paint.svg) {{page.title}}
Les mat�riaux contiennent les d�finitions de couleur, de r�flectivit�, de transparence, de textures et de relief de la finition d'une surface. Tous les mat�riaux ont des param�tres de base. Le mat�riau par d�faut est blanc mat, sans r�flexion ni transparence. Pour de meilleurs r�sultats, utilisez des mat�riaux sp�cifiques de Flamingo. 

Les mat�riaux peuvent �tre assign�s aux calques, aux objets et aux blocs. Pour assigner un mat�riau, il est possible de le d�poser directement sur un objet ou d'utiliser diff�rents contr�les. Voir [Assignations de mat�riaux](material_assignment.html) pour plus d'informations. 

Une fois assign�s, les mat�riaux sont enregistr�s dans le mod�le. Les mat�riaux, les textures et tous les fichiers de ressources pour le rendu peuvent �tre enregistr�s dans le mod�le en d�finissant correctement les [options de rendu](http://docs.mcneel.com/rhino/5/help/en-us/index.htm#options/rendering.htm).

Les mat�riaux, les environnements et les textures sont enregistr�s dans le mod�le, mais le contenu de rendu peut �galement �tre enregistr� dans des fichiers qui peuvent �tre partag�s entre les mod�les. Le contenu peut �tre d�plac� entre diff�rentes sessions de Rhino ou dans un dossier. Les palettes de couleur peuvent �galement �tre d�plac�es de la m�me fa�on. Le panneau [Biblioth�ques](libraries.html) affiche le dossier de contenu par d�faut. Utilisez cette fonction pour d�poser un contenu dans le mod�le ou le contenu d'un mod�le dans un fichier externe.

![images/material_editor_panel.svg](images/material_editor_panel.svg){:  #panel_map .float-img-right}

##### O� puis-je trouver cette commande ?
Vous disposez de plusieurs options pour trouver l'onglet Mat�riaux.

* ![images/materialtab.png](images/materialtab.png)Onglet Mat�riaux
* ![images/icon-render.png](images/icon-render.png)Barre d'outils Outils pour le rendu > ![images/materialtab.png](images/materialtab.png) �diteur de mat�riaux
* Menus > Rendu > �diteur de mat�riaux
* Dans la ligne de commandes, tapez �diteurMat�riaux

Le panneau de l'�diteur de mat�riaux est divis� en plusieurs sections.  En fonction du type de mat�riau, les panneaux avanc�s peuvent varier.

Il est possible de faire glisser les couleurs et les textures � partir de la palette et de les d�poser sur une autre palette ou sur une option de l'�diteur de mat�riaux, de la [palette de textures](texturepalette.html) ou de [l'�diteur d'environnement](environmenteditor.html).

##### Panneau des mat�riaux

 1. [Barre de param�tres](#settings)
 1. [Liste de mat�riaux](#material_list)
 1. [Diviseur de fen�tre](#divider)
 1. [Section des propri�t�s de mat�riau](#properties)
 1. [Nom](#name)
 1. [Panneau des propri�t�s du mat�riau](#panels)

## [Barre de param�tres](#panel_map) ![images/callout_1.svg](images/callout_1.svg)
{: #settings .clear-img}
Utilisez cette barre pour vous d�placer dans le mat�riau pendant sa cr�ation.

#### ![images/met_leftarrow.png](images/met-leftarrow.png) Fl�che de retour arri�re
S�lectionne le mat�riau pr�c�dent.  Par exemple, les mat�riaux avec des textures ont plusieurs couches. Utilisez cette fl�che pour revenir au mat�riau parent depuis les d�tails de texture.

####  ![images/met_rightarrow.png](images/met-rightarrow.png) Fl�che pour avancer
S�lectionne le mat�riau suivant.  Par exemple, les mat�riaux avec des textures ont plusieurs couches.  Utilisez cette fl�che pour revenir � la derni�re texture utilis�e dans le mat�riau parent. 


#### ![images/material_editor.png](images/material_editor.png)![images/texture-2dchecker.png](images/texture-2dchecker.png) Nom du mat�riau actuellement s�lectionn�
Affiche le nom du mat�riau actuel et le niveau.  Par exemple, si une texture est d�finie ou s'il existe un niveau de mat�riau algorithmique, le signe > est affich�. Vous pouvez voir ici o� se trouve l'�diteur dans un mat�riau.

#### ![images/library_default.png](images/library_default.png) Menu Outils
Affiche le [menu Outils](#tools-menu).  Ce menu contient de nombreuses commandes, param�tres et outils concernant les mat�riaux.


## [Liste des mat�riaux](#panel_map) ![images/callout_2.svg](images/callout_2.svg)
{: #material_list}
Affiche une liste de tous les mat�riaux disponibles dans le mod�le. � partir de cette liste :

* Naviguez dans la liste pour voir tous les mat�riaux du mod�le.
* D�placez un mat�riau de cette liste sur un calque dans le [panneau des calques](http://docs.mcneel.com/rhino/5/help/fr-fr/index.htm#commands/layer.htm) ou directement sur un objet pour l'assigner � celui-ci. Voir [Assignations de mat�riaux](material_assignment.html) pour plus d'informations.
* Ajoutez un nouveau mat�riau, en utilisant le bouton Ajouter ![images/add_material.png](images/add_material.png) en bas de la liste.


* Cliquez sur chaque mat�riau pour le s�lectionner. Une fois s�lectionn�, les propri�t�s du mat�riau seront affich�es dans les panneaux inf�rieurs. Voir [Propri�t�s des mat�riaux de rendu](#properties) pour plus d'informations.
* Cliquez avec le bouton de droite sur une miniature pour afficher le menu contextuel du mat�riau.
* Cliquez avec le  bouton de droite dans la zone vide pour afficher le menu contextuel de cr�ation d'un nouveau mat�riau.

###  ![images/add_material.png](images/add_material.png) Ajouter un nouveau mat�riau
{: #add_material}
L'ic�ne ajouter se trouve en bas de la liste des mat�riaux.

Il ouvre la [biblioth�que](libraries.html) de contenu de rendu des mat�riaux.
Les mat�riaux de la biblioth�que agissent comme des mod�les pour cr�er d'autres mat�riaux.

### Menu contextuel des mat�riaux
{: material_context}
Ce menu est disponible en cliquant avec le bouton droit sur un mat�riau de la liste.  Consultez le [menu Outils](#tools_menu) pour plus d'informations sur les options de ce menu.

### Menu contextuel de cr�ation d'un nouvel mat�riau
{: new_material_context}
Ce menu est disponible en cliquant avec le bouton droit dans une zone vide de la liste de mat�riaux.

#### ![images/toolbarlus.png](images/toolbarplus.png) Cr�er un nouveau mat�riau
Cr�e un nouveau mat�riau blanc mat de base.


#### ![images/paste.png](images/paste.png) Coller
Cr�e un nouveau mat�riau � partir du contenu du presse-papiers.

#### ![images/pasteasinstance.png](images/pasteasinstance.png) Coller comme occurrence
Cr�e un nouveau mat�riau � partir du contenu du presse-papiers et qui est li� � l'original par instanciation.

#### ![images/grid.png](images/grid.png) Grille
Affiche les aper�us sous forme de grille de miniatures.

#### ![images/list.png](images/list.png) Liste
Affiche les aper�us sous forme de liste de miniatures.

#### ![images/tree.png](images/tree.png) Arbre
Affiche les aper�us sous forme d'arbre affichant les diff�rentes branches.

#### ![images/horizontal.png](images/horizontal.png) Mise en page horizontale
Affiche les aper�us � gauche des contr�les.

#### ![images/showpreview.png](images/showpreview.png) Afficher le panneau d'aper�u
Affiche les propri�t�s d'aper�u pour la miniature s�lectionn�e. Vous pouvez d�finir la g�om�trie de l'aper�u, sa taille, l'arri�re-plan utilis� et la m�thode de rotation.

#### ![images/floatthumbnail.png](images/floatthumbnail.png) Aper�u flottant
Affiche l'image d'aper�u dans une fen�tre flottante dont la taille peut �tre modifi�e.

#### Miniatures

##### ![images/small.png](images/small.png) Petit
D�finit la plus petite taille de miniature.

##### ![images/medium.png](images/medium.png) Moyen
D�finit la taille moyenne de miniature.

##### ![images/large.png](images/large.png) Grand
D�finit la plus grande taille de miniature.

##### ![images/showlabels.png](images/showlabels.png) Afficher les �tiquettes
Affiche les �tiquettes du nom de la miniature en mode Grille.
Le mode Liste affiche toujours les �tiquettes.

##### ![images/showunits.png](images/showunits.png) Afficher les unit�s
Affiche la taille dans les unit�s du mod�le.

##### ![images/autoupdatethumbnail.png](images/autoupdatethumbnail.png) Actualisation automatique de l'aper�u
Actualise automatiquement tous les aper�us lorsque les param�tres sont modifi�s.

##### ![images/updateallpreviews.png](images/updateallpreviews.png) Actualiser tous les aper�us
Actualise les aper�us manuellement lorsque l'option Actualisation automatique de l'aper�u est d�sactiv�e.

## [Diviseur de fen�tre](#panel_map) ![images/callout_3.svg](images/callout_3.svg)
{: #divider}
D�placez le diviseur pour modifier la longueur de la liste des mat�riaux. Si vous agrandissez la liste, la section des propri�t�s des mat�riaux diminue. 

## [Section des propri�t�s de mat�riau](#panel_map) ![images/callout_4.svg](images/callout_4.svg)
{: #properties}

#### [Nom du mat�riau](#panel_map) ![images/callout_5.svg](images/callout_5.svg)
{: #name}
Cette section indique le nom du mat�riau. Le nom du mat�riau est �galement enregistr� comme nom du fichier lors de l'exportation du mat�riau vers la biblioth�que. Note : Les mat�riaux sont enregistr�s dans le mod�le de Rhino. Des mat�riaux uniques peuvent avoir le m�me nom dans diff�rents mod�les de Rhino.

#### [Panneau Mat�riau#panel_map) ![images/callout_6.svg](images/callout_6.svg)
{: #panels}
La section des propri�t�s de mat�riaux comprend plusieurs panneaux. Chaque panneau peut �tre ouvert ou ferm� en cliquant sur la barre de titre en gris.  Cliquez sur la barre de titre pour afficher le contenu.

Les panneaux du mat�riau varieront en fonction du type de mat�riau et du niveau actif du mat�riau actuel. Pour plus d'informations sur chaque panneau, consultez la section [mat�riaux de Flamingo](material-type-simple.html).

## Menu Outils ![images/library_default.png](images/library_default.png)
{: #tools-menu}
<!-- Cette partie vient de la page http://docs.mcneel.com/rhino/5/help/en-us/popup_moreinformation/materialthumbnail_contextmenu.htm -->
Ces param�tres apparaissent �galement dans les menus contextuels du bouton de droite de la souris pour les aper�us et arri�re-plans miniatures.

#### ![images/assigntoobjects.png](images/assigntoobjects.png) Assigner � la s�lection
Assigne le mat�riau actuel aux objets s�lectionn�s.

##### Pour assigner un mat�riau � des objets
 1. Cliquez sur Assigner � la s�lection.
 1. Dans la fen�tre de Rhino, s�lectionnez les objets cibles.

##### Pour s�lectionner des objets avant
 1. Dans la fen�tre de Rhino, s�lectionnez les objets cibles.
 1. Cliquez sur Assigner � la s�lection.
Les objets cibles peuvent �tre s�lectionn�s avant ou apr�s avoir cliqu� sur Assigner � la s�lection

##### Pour d�poser des mat�riaux sur des objets
 * Faites glisser le mat�riau � partir d'une miniature ou de la liste sur les objets cibles.
Le d�p�t de mat�riau fonctionne uniquement pour un seul objet � la fois.

#### ![images/assigntolayers.png](images/assigntolayers.png) Assigner � des calques
Assigne le mat�riau actuel � des calques.

##### Pour assigner un mat�riau � des calques
 1. Cliquez sur Assigner � des calques.
 1. Dans la bo�te de dialogue S�lectionner des calques, cochez les cases correspondantes.

##### Pour assigner des mat�riaux � partir du panneau Calques
 1. Dans le panneau [Calques](http://docs.mcneel.com/rhino/5/help/fr-fr/index.htm#commands/layer.htm), s�lectionnez un ou plusieurs calques puis cliquez sur la colonne [Mat�riau](http://docs.mcneel.com/rhino/5/help/fr-fr/commands/layer.htm#Material).
 1. Dans la bo�te de dialogue Mat�riau du calque, s�lectionnez le mat�riau � assigner.


#####  Pour d�poser un mat�riau sur un calque
 * Faites glisser le mat�riau � partir d'une miniature ou de la liste sur le calque cible.
Le d�p�t de mat�riau fonctionne uniquement pour un seul calque � la fois.

#### ![images/materials_selectobjects.png](images/materials_selectobjects.png) S�lectionner des objets
S�lectionnez des objets dans le mod�le pour leur assigner un mat�riau.

#### ![images/toolbarplus.png](images/toolbarplus.png) Cr�er un nouveau mat�riau
Il ouvre la [biblioth�que](libraries.html) de contenu de rendu des mat�riaux.
Les mat�riaux de la biblioth�que agissent comme des mod�les pour cr�er d'autres mat�riaux.

#### ![images/import.png](images/import.png) Importer un mat�riau � partir d'un fichier�
Importe des mat�riaux � partir d'un fichier .rmtl de Rhino.

#### ![images/savetofile.png](images/savetofile.png) Enregistrer dans un fichier
Enregistre un mat�riau dans un fichier .rmtl de Rhino.

#### ![images/changetype.png](images/changetype.png) Modifier le type
Change le type d'un mat�riau.

#### ![images/changetype.png](images/changetype.png) Modifier le type (Copier les param�tres)
Change le type d'un mat�riau.
Le comportement par d�faut d�pend du statut actuel de la case [Options de rendu](http://docs.mcneel.com/rhino/5/help/fr-fr/index.htm#popup_moreinformation/materialpanel_toolsmenu.htm)  >  [Copier les param�tres similaires lorsque le type de contenu est modifi�](http://docs.mcneel.com/rhino/5/help/fr-fr/index.htm#popup_moreinformation/materialpanel_toolsmenu.htm). Si cette case est coch�e, les param�tres compatibles de l'ancien contenu seront copi�s dans le nouveau.

#### ![images/reset.png](images/reset.png) Valeurs par d�faut
D�finit tous les param�tres par d�faut du mat�riau (blanc, mate, non r�fl�chissant, non textur�).

#### ![images/copy.png](images/copy.png) Copier
Copie la mat�riau s�lectionn� dans le presse-papiers de Windows. Le presse-papiers peut ensuite �tre coll� dans l'�diteur afin de cr�er un nouveau mat�riau ou coll� directement dans un dossier pour cr�er un  fichier de [biblioth�que](libraries.html) file.

#### ![images/paste.png](images/paste.png) Coller
Cr�e un nouveau mat�riau � partir du contenu du presse-papiers.

#### ![images/pasteasinstance.png](images/pasteasinstance.png) Coller comme occurrence
Cr�e un nouveau mat�riau � partir du contenu du presse-papiers et qui est li� � l'original par instanciation.

#### ![images/delete.png](images/delete.png) Supprimer
Supprime le mat�riau s�lectionn�.

#### ![images/rename.png](images/rename.png) Renommer...
Renomme le mat�riau s�lectionn�.

#### ![images/duplicate.png](images/duplicate.png) Dupliquer
Copie le mat�riau s�lectionn� sur un nouveau mat�riau avec les m�mes param�tres.

#### ![images/removeinstancing.png](images/removeinstancing.png) Supprimer l'instanciation
Supprime le lien entre les mat�riaux copi�s par [instance](http://docs.mcneel.com/rhino/5/help/fr-fr/index.htm#popup_moreinformation/materialpanel_toolsmenu.htm).
{% include_relative snippets/snippet-contenteditorpreviewoptions.md %}


#### ![images/contentfilter.png](images/contentfilter.png) Filtre de contenu
Ouvre la bo�te de dialogue [Filtres de contenu](content_filters.html) .

#### ![images/rename.png](images/rename.png) Propri�t�s
Ouvre la bo�te de dialogue [Propri�t�s de l'aper�u](http://docs.mcneel.com/rhino/5/help/fr-fr/index.htm#popup_moreinformation/materialpanel_toolsmenu.htm).
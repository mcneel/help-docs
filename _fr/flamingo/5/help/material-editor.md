---
title: Panneau Éditeur de matériaux
---

# ![images/paint.svg](images/paint.svg) {{page.title}}
Les matériaux contiennent les définitions de couleur, de réflectivité, de transparence, de textures et de relief de la finition d'une surface. Tous les matériaux ont des paramètres de base. Le matériau par défaut est blanc mat, sans réflexion ni transparence. Pour de meilleurs résultats, utilisez des matériaux spécifiques de Flamingo. 

Les matériaux peuvent être assignés aux calques, aux objets et aux blocs. Pour assigner un matériau, il est possible de le déposer directement sur un objet ou d'utiliser différents contrôles. Voir [Assignations de matériaux](material_assignment.html) pour plus d'informations. 

Une fois assignés, les matériaux sont enregistrés dans le modèle. Les matériaux, les textures et tous les fichiers de ressources pour le rendu peuvent être enregistrés dans le modèle en définissant correctement les [options de rendu](http://docs.mcneel.com/rhino/5/help/en-us/index.htm#options/rendering.htm).

Les matériaux, les environnements et les textures sont enregistrés dans le modèle, mais le contenu de rendu peut également être enregistré dans des fichiers qui peuvent être partagés entre les modèles. Le contenu peut être déplacé entre différentes sessions de Rhino ou dans un dossier. Les palettes de couleur peuvent également être déplacées de la même façon. Le panneau [Bibliothèques](libraries.html) affiche le dossier de contenu par défaut. Utilisez cette fonction pour déposer un contenu dans le modèle ou le contenu d'un modèle dans un fichier externe.

![images/material_editor_panel.svg](images/material_editor_panel.svg){:  #panel_map .float-img-right}

##### Où puis-je trouver cette commande ?
Vous disposez de plusieurs options pour trouver l'onglet Matériaux.

* ![images/materialtab.png](images/materialtab.png)Onglet Matériaux
* ![images/icon-render.png](images/icon-render.png)Barre d'outils Outils pour le rendu > ![images/materialtab.png](images/materialtab.png) Éditeur de matériaux
* Menus > Rendu > Éditeur de matériaux
* Dans la ligne de commandes, tapez ÉditeurMatériaux

Le panneau de l'éditeur de matériaux est divisé en plusieurs sections.  En fonction du type de matériau, les panneaux avancés peuvent varier.

Il est possible de faire glisser les couleurs et les textures à partir de la palette et de les déposer sur une autre palette ou sur une option de l'éditeur de matériaux, de la [palette de textures](texturepalette.html) ou de [l'éditeur d'environnement](environmenteditor.html).

##### Panneau des matériaux

 1. [Barre de paramètres](#settings)
 1. [Liste de matériaux](#material_list)
 1. [Diviseur de fenêtre](#divider)
 1. [Section des propriétés de matériau](#properties)
 1. [Nom](#name)
 1. [Panneau des propriétés du matériau](#panels)

## [Barre de paramètres](#panel_map) ![images/callout_1.svg](images/callout_1.svg)
{: #settings .clear-img}
Utilisez cette barre pour vous déplacer dans le matériau pendant sa création.

#### ![images/met_leftarrow.png](images/met-leftarrow.png) Flèche de retour arrière
Sélectionne le matériau précédent.  Par exemple, les matériaux avec des textures ont plusieurs couches. Utilisez cette flèche pour revenir au matériau parent depuis les détails de texture.

####  ![images/met_rightarrow.png](images/met-rightarrow.png) Flèche pour avancer
Sélectionne le matériau suivant.  Par exemple, les matériaux avec des textures ont plusieurs couches.  Utilisez cette flèche pour revenir à la dernière texture utilisée dans le matériau parent. 


#### ![images/material_editor.png](images/material_editor.png)![images/texture-2dchecker.png](images/texture-2dchecker.png) Nom du matériau actuellement sélectionné
Affiche le nom du matériau actuel et le niveau.  Par exemple, si une texture est définie ou s'il existe un niveau de matériau algorithmique, le signe > est affiché. Vous pouvez voir ici où se trouve l'éditeur dans un matériau.

#### ![images/library_default.png](images/library_default.png) Menu Outils
Affiche le [menu Outils](#tools-menu).  Ce menu contient de nombreuses commandes, paramètres et outils concernant les matériaux.


## [Liste des matériaux](#panel_map) ![images/callout_2.svg](images/callout_2.svg)
{: #material_list}
Affiche une liste de tous les matériaux disponibles dans le modèle. À partir de cette liste :

* Naviguez dans la liste pour voir tous les matériaux du modèle.
* Déplacez un matériau de cette liste sur un calque dans le [panneau des calques](http://docs.mcneel.com/rhino/5/help/fr-fr/index.htm#commands/layer.htm) ou directement sur un objet pour l'assigner à celui-ci. Voir [Assignations de matériaux](material_assignment.html) pour plus d'informations.
* Ajoutez un nouveau matériau, en utilisant le bouton Ajouter ![images/add_material.png](images/add_material.png) en bas de la liste.


* Cliquez sur chaque matériau pour le sélectionner. Une fois sélectionné, les propriétés du matériau seront affichées dans les panneaux inférieurs. Voir [Propriétés des matériaux de rendu](#properties) pour plus d'informations.
* Cliquez avec le bouton de droite sur une miniature pour afficher le menu contextuel du matériau.
* Cliquez avec le  bouton de droite dans la zone vide pour afficher le menu contextuel de création d'un nouveau matériau.

###  ![images/add_material.png](images/add_material.png) Ajouter un nouveau matériau
{: #add_material}
L'icône ajouter se trouve en bas de la liste des matériaux.

Il ouvre la [bibliothèque](libraries.html) de contenu de rendu des matériaux.
Les matériaux de la bibliothèque agissent comme des modèles pour créer d'autres matériaux.

### Menu contextuel des matériaux
{: material_context}
Ce menu est disponible en cliquant avec le bouton droit sur un matériau de la liste.  Consultez le [menu Outils](#tools_menu) pour plus d'informations sur les options de ce menu.

### Menu contextuel de création d'un nouvel matériau
{: new_material_context}
Ce menu est disponible en cliquant avec le bouton droit dans une zone vide de la liste de matériaux.

#### ![images/toolbarlus.png](images/toolbarplus.png) Créer un nouveau matériau
Crée un nouveau matériau blanc mat de base.


#### ![images/paste.png](images/paste.png) Coller
Crée un nouveau matériau à partir du contenu du presse-papiers.

#### ![images/pasteasinstance.png](images/pasteasinstance.png) Coller comme occurrence
Crée un nouveau matériau à partir du contenu du presse-papiers et qui est lié à l'original par instanciation.

#### ![images/grid.png](images/grid.png) Grille
Affiche les aperçus sous forme de grille de miniatures.

#### ![images/list.png](images/list.png) Liste
Affiche les aperçus sous forme de liste de miniatures.

#### ![images/tree.png](images/tree.png) Arbre
Affiche les aperçus sous forme d'arbre affichant les différentes branches.

#### ![images/horizontal.png](images/horizontal.png) Mise en page horizontale
Affiche les aperçus à gauche des contrôles.

#### ![images/showpreview.png](images/showpreview.png) Afficher le panneau d'aperçu
Affiche les propriétés d'aperçu pour la miniature sélectionnée. Vous pouvez définir la géométrie de l'aperçu, sa taille, l'arrière-plan utilisé et la méthode de rotation.

#### ![images/floatthumbnail.png](images/floatthumbnail.png) Aperçu flottant
Affiche l'image d'aperçu dans une fenêtre flottante dont la taille peut être modifiée.

#### Miniatures

##### ![images/small.png](images/small.png) Petit
Définit la plus petite taille de miniature.

##### ![images/medium.png](images/medium.png) Moyen
Définit la taille moyenne de miniature.

##### ![images/large.png](images/large.png) Grand
Définit la plus grande taille de miniature.

##### ![images/showlabels.png](images/showlabels.png) Afficher les étiquettes
Affiche les étiquettes du nom de la miniature en mode Grille.
Le mode Liste affiche toujours les étiquettes.

##### ![images/showunits.png](images/showunits.png) Afficher les unités
Affiche la taille dans les unités du modèle.

##### ![images/autoupdatethumbnail.png](images/autoupdatethumbnail.png) Actualisation automatique de l'aperçu
Actualise automatiquement tous les aperçus lorsque les paramètres sont modifiés.

##### ![images/updateallpreviews.png](images/updateallpreviews.png) Actualiser tous les aperçus
Actualise les aperçus manuellement lorsque l'option Actualisation automatique de l'aperçu est désactivée.

## [Diviseur de fenêtre](#panel_map) ![images/callout_3.svg](images/callout_3.svg)
{: #divider}
Déplacez le diviseur pour modifier la longueur de la liste des matériaux. Si vous agrandissez la liste, la section des propriétés des matériaux diminue. 

## [Section des propriétés de matériau](#panel_map) ![images/callout_4.svg](images/callout_4.svg)
{: #properties}

#### [Nom du matériau](#panel_map) ![images/callout_5.svg](images/callout_5.svg)
{: #name}
Cette section indique le nom du matériau. Le nom du matériau est également enregistré comme nom du fichier lors de l'exportation du matériau vers la bibliothèque. Note : Les matériaux sont enregistrés dans le modèle de Rhino. Des matériaux uniques peuvent avoir le même nom dans différents modèles de Rhino.

#### [Panneau Matériau#panel_map) ![images/callout_6.svg](images/callout_6.svg)
{: #panels}
La section des propriétés de matériaux comprend plusieurs panneaux. Chaque panneau peut être ouvert ou fermé en cliquant sur la barre de titre en gris.  Cliquez sur la barre de titre pour afficher le contenu.

Les panneaux du matériau varieront en fonction du type de matériau et du niveau actif du matériau actuel. Pour plus d'informations sur chaque panneau, consultez la section [matériaux de Flamingo](material-type-simple.html).

## Menu Outils ![images/library_default.png](images/library_default.png)
{: #tools-menu}
<!-- Cette partie vient de la page http://docs.mcneel.com/rhino/5/help/en-us/popup_moreinformation/materialthumbnail_contextmenu.htm -->
Ces paramètres apparaissent également dans les menus contextuels du bouton de droite de la souris pour les aperçus et arrière-plans miniatures.

#### ![images/assigntoobjects.png](images/assigntoobjects.png) Assigner à la sélection
Assigne le matériau actuel aux objets sélectionnés.

##### Pour assigner un matériau à des objets
 1. Cliquez sur Assigner à la sélection.
 1. Dans la fenêtre de Rhino, sélectionnez les objets cibles.

##### Pour sélectionner des objets avant
 1. Dans la fenêtre de Rhino, sélectionnez les objets cibles.
 1. Cliquez sur Assigner à la sélection.
Les objets cibles peuvent être sélectionnés avant ou après avoir cliqué sur Assigner à la sélection

##### Pour déposer des matériaux sur des objets
 * Faites glisser le matériau à partir d'une miniature ou de la liste sur les objets cibles.
Le dépôt de matériau fonctionne uniquement pour un seul objet à la fois.

#### ![images/assigntolayers.png](images/assigntolayers.png) Assigner à des calques
Assigne le matériau actuel à des calques.

##### Pour assigner un matériau à des calques
 1. Cliquez sur Assigner à des calques.
 1. Dans la boîte de dialogue Sélectionner des calques, cochez les cases correspondantes.

##### Pour assigner des matériaux à partir du panneau Calques
 1. Dans le panneau [Calques](http://docs.mcneel.com/rhino/5/help/fr-fr/index.htm#commands/layer.htm), sélectionnez un ou plusieurs calques puis cliquez sur la colonne [Matériau](http://docs.mcneel.com/rhino/5/help/fr-fr/commands/layer.htm#Material).
 1. Dans la boîte de dialogue Matériau du calque, sélectionnez le matériau à assigner.


#####  Pour déposer un matériau sur un calque
 * Faites glisser le matériau à partir d'une miniature ou de la liste sur le calque cible.
Le dépôt de matériau fonctionne uniquement pour un seul calque à la fois.

#### ![images/materials_selectobjects.png](images/materials_selectobjects.png) Sélectionner des objets
Sélectionnez des objets dans le modèle pour leur assigner un matériau.

#### ![images/toolbarplus.png](images/toolbarplus.png) Créer un nouveau matériau
Il ouvre la [bibliothèque](libraries.html) de contenu de rendu des matériaux.
Les matériaux de la bibliothèque agissent comme des modèles pour créer d'autres matériaux.

#### ![images/import.png](images/import.png) Importer un matériau à partir d'un fichier 
Importe des matériaux à partir d'un fichier .rmtl de Rhino.

#### ![images/savetofile.png](images/savetofile.png) Enregistrer dans un fichier
Enregistre un matériau dans un fichier .rmtl de Rhino.

#### ![images/changetype.png](images/changetype.png) Modifier le type
Change le type d'un matériau.

#### ![images/changetype.png](images/changetype.png) Modifier le type (Copier les paramètres)
Change le type d'un matériau.
Le comportement par défaut dépend du statut actuel de la case [Options de rendu](http://docs.mcneel.com/rhino/5/help/fr-fr/index.htm#popup_moreinformation/materialpanel_toolsmenu.htm)  >  [Copier les paramètres similaires lorsque le type de contenu est modifié](http://docs.mcneel.com/rhino/5/help/fr-fr/index.htm#popup_moreinformation/materialpanel_toolsmenu.htm). Si cette case est cochée, les paramètres compatibles de l'ancien contenu seront copiés dans le nouveau.

#### ![images/reset.png](images/reset.png) Valeurs par défaut
Définit tous les paramètres par défaut du matériau (blanc, mate, non réfléchissant, non texturé).

#### ![images/copy.png](images/copy.png) Copier
Copie la matériau sélectionné dans le presse-papiers de Windows. Le presse-papiers peut ensuite être collé dans l'éditeur afin de créer un nouveau matériau ou collé directement dans un dossier pour créer un  fichier de [bibliothèque](libraries.html) file.

#### ![images/paste.png](images/paste.png) Coller
Crée un nouveau matériau à partir du contenu du presse-papiers.

#### ![images/pasteasinstance.png](images/pasteasinstance.png) Coller comme occurrence
Crée un nouveau matériau à partir du contenu du presse-papiers et qui est lié à l'original par instanciation.

#### ![images/delete.png](images/delete.png) Supprimer
Supprime le matériau sélectionné.

#### ![images/rename.png](images/rename.png) Renommer...
Renomme le matériau sélectionné.

#### ![images/duplicate.png](images/duplicate.png) Dupliquer
Copie le matériau sélectionné sur un nouveau matériau avec les mêmes paramètres.

#### ![images/removeinstancing.png](images/removeinstancing.png) Supprimer l'instanciation
Supprime le lien entre les matériaux copiés par [instance](http://docs.mcneel.com/rhino/5/help/fr-fr/index.htm#popup_moreinformation/materialpanel_toolsmenu.htm).
{% include_relative snippets/snippet-contenteditorpreviewoptions.md %}


#### ![images/contentfilter.png](images/contentfilter.png) Filtre de contenu
Ouvre la boîte de dialogue [Filtres de contenu](content_filters.html) .

#### ![images/rename.png](images/rename.png) Propriétés
Ouvre la boîte de dialogue [Propriétés de l'aperçu](http://docs.mcneel.com/rhino/5/help/fr-fr/index.htm#popup_moreinformation/materialpanel_toolsmenu.htm).
---
title: Panneau Environnement
---

# ![images/environment.svg](images/environment.svg) {{page.title}}
{: #environment-tab}
Les environnements ne sont pas uniquement ce qui peut �tre vu � l'arri�re-plan d'un rendu, mais ils contr�lent �galement une sph�re infinie enveloppant le mod�le. Les objets dans la sc�ne r�fl�chiront et r�fracteront l'environnement. La sph�re de l'environnement n'est pas un objet qui peut �tre s�lectionn� mais une surface de r�f�rence pour les effets d'arri�re-plan.

L'environnement agit sur la partie visible de l'arri�re-plan et des r�flexions.  Pour des effets agissant sur l'�clairage de la sc�ne, consultez la rubrique de l'aide sur le [Ciel](sun-and-sky.html).

Flamingo poss�de un environnement sp�cial appel� *[Environnement par d�faut de Flamingo](environment.html)*.  Cet environnement est synchronis� avec les [Pr�r�glages d'�clairage](lighting-tab.html). En utilisant les [Pr�r�glages d'�clairage](lighting-tab.html), l'�clairage et l'environnement seront d�finis avec les valeurs par d�faut adapt�es � la sc�ne.

![images/environment-editor-panel.svg](images/environment-editor-panel.svg){:  #panel_map height="600px" style="float: right"}

##### O� puis-je trouver cette commande ?
 1. ![images/environments.png](images/environments.png)Onglet Environnement
 1. ![images/icon-render.png](images/icon-render.png)Barres d'outils Outils  pour le rendu > ![images/environments.png](images/environments.png) �diteur d'environnement
 1. ![images/menuicon.png](images/menuicon.png)Menus > Rendu > �diteur d'environnement
 1. Commande > �diteurEnvironnement

Le panneau de l'�diteur d'environnement est divis� en plusieurs sections.  En fonction du type de environnement, les panneaux avanc�s peuvent varier.

Il est possible de faire glisser les couleurs et les textures � partir de la palette et de les d�poser sur une autre palette ou sur une option de l'�diteur de mat�riaux, de la [palette textures](texturepalette.html) ou de [l'�diteur d'environnement](environmenteditor.html).
Panneau Environnement

 1. [Type d'arri�re-plan](#type)
 1. [Barre de param�tres](#settings)
 1. [Liste d'environnements](#environment_list)
 1. [Diviseur de fen�tre](#divider)
 1. [Section des propri�t�s de l'environnement](#properties)
 1. [Nom](#name)
 1. [Panneaux des propri�t�s de l'environnement](#panels)

## [Type d'arri�re-plan](#panel_map) ![images/callout_1.svg](images/callout_1.svg)
{: #type style="clear: both;"}
S�lectionnez le type d'arri�re-plan pour le mod�le.  L'[environnement](#flamingo-environment) est un environnement de rendu tout compris et devrait �tre le param�tre par d�faut pour Flamingo.  Les trois aux param�tres pr�sentent un ensemble de param�tres beaucoup plus simple qui correspond � l'ancien mode de d�finition des arri�re-plans. Pour plus d'informations, consultez la rubrique [arri�re-plan simple de Rhinoceros](http://docs.mcneel.com/rhino/5/help/en-us/commands/environmenteditor.htm#Basic_settings).

Le reste de cette rubrique couvre le type d'environnement.

## [Barre de param�tres](#panel_map) ![images/callout_2.svg](images/callout_2.svg)
{: #settings}
Utilisez cette barre pour mieux naviguer dans la liste des environnements.

#### ![images/met_leftarrow.png](images/met-leftarrow.png) Fl�che de retour arri�re
S�lectionne l'environnement pr�c�dent.  Par exemple un environnement avec des couches r�fl�chissantes ou r�fringentes.  Utilisez cette fl�che pour revenir � l'environnement parent depuis les d�tails de r�flexion ou r�fraction.

####  ![images/met_rightarrow.png](images/met-rightarrow.png) Fl�che pour avancer
S�lectionne l'environnement suivant.  Par exemple un environnement avec des couches r�fl�chissantes ou r�fringentes.  Utilisez cette fl�che pour passer � l'environnement parent suivant depuis les d�tails de r�flexion ou r�fraction.

#### ![images/material_editor.png](images/material_editor.png)![images/texture-2dchecker.png](images/texture-2dchecker.png) Nom de l'environnement actuellement s�lectionn�
Affiche le nom de l'environnement actuel et le niveau d'�dition.  Par exemple, si un niveau R�fl�chi ou R�fract� existe, le signe > est affich�. Vous pouvez voir ici l'environnement actuel. 

#### ![images/library_default.png](images/library_default.png) Menu Outils
Affiche le [menu Outils](#tools-menu).    Ce menu contient de nombreuses commandes, param�tres et outils concernant les environnements. 

#### ![images/help_topics.png](images/help_topics.png) Aide

## [Liste des environnements](#panel_map) ![images/callout_3.svg](images/callout_3.svg)
{: #environment_list}
Affiche une liste de tous environnements disponibles dans le mod�le. Un environnement sera s�lectionn� comme environnement actuel. L'environnement actuel est utilis� pour le rendu. Des petits signes jaunes sont affich�s dans les coins de l'environnement actuel. 

� partir de cette liste :

* Cliquez sur un environnement pour le d�finir comme environnement actuel. Une fois s�lectionn�, les propri�t�s de l'environnement seront affich�es dans les panneaux inf�rieurs. Voir [Propri�t�s des mat�riaux de rendu](#properties) pour plus d'informations.
* Naviguez dans la liste pour voir tous les environnements du mod�le.
* Ajoutez un nouvel environnement, en utilisant le bouton Ajouter ![images/add_material.png](images/add_material.png) en bas de la liste. 
* Cliquez avec le bouton de droite sur une miniature pour afficher le menu contextuel de l'environnement
* Cliquez avec le  bouton de droite dans la zone vide pour afficher le menu contextuel de cr�ation d'un nouvel environnement

###  ![images/add_material.png](images/add_material.png) Ajouter un nouvel environnement
{: #add_environment}
L'ic�ne ajouter se trouve en bas de la liste des environnements. 

Il ouvre le [biblioth�que](libraries.html) d'environnements du contenu de rendu.
Les environnements de la biblioth�que agissent comme des mod�les pour cr�er d'autres environnements dans le document.

### Menu contextuel de l'environnement
{: environment_context}
Le menu est disponible en cliquant avec le bouton droit sur un �l�ment de la liste d'environnements. Consultez le [menu Outils](#tools_menu) pour plus d'informations sur les options de ce menu. 

### Menu contextuel de cr�ation d'un nouvel environnement
{: new_envrionment_context}
Ce menu est disponible en cliquant avec le bouton droit dans une zone vide de la liste d'environnements.

#### ![images/toolbarlus.png](images/toolbarplus.png) Cr�er un nouvel environnement
Cr�e un nouvel environnement de Flamingo.

#### ![images/import.png](images/import.png) Importer un environnement � partir d'un fichier...
Utilisez cette commande pour s�lectionner un environnement pr�c�demment export�. 

#### ![images/paste.png](images/paste.png) Coller
Cr�e un nouvel environnement � partir du contenu du presse-papiers.

#### ![images/pasteasinstance.png](images/pasteasinstance.png) Coller comme occurrence
Cr�e un nouvel environnement � partir du contenu du presse-papiers qui est li� � l'original par instanciation.

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

## [Diviseur de fen�tre](#panel_map) ![images/callout_4.svg](images/callout_4.svg)
{: #divider}
D�placez le diviseur pour modifier la longueur de la liste des environnements par rapport � la longueur de la section des propri�t�s de l'environnement.

## [Section des propri�t�s de l'environnement](#panel_map) ![images/callout_5.svg](images/callout_5.svg)
{: #properties}

### [Nom de l'environnement](#panel_map) ![images/callout_6.svg](images/callout_6.svg)
{: #name}
Cette section indique le nom de l'environnement. Le nom de l'environnement est �galement enregistr� comme nom du fichier lors de l'exportation de l'environnement vers la biblioth�que. **Remarque�:** Les environnements sont sauvegard�s dans le mod�le de Rhino, des environnements uniques peuvent avoir le m�me nom dans diff�rents mod�les de Rhino.

### [Panneaux Environnement](l#panel_map) ![images/callout_7.svg](images/callout_7.svg)
{: #panels}
La section des propri�t�s de l'environnement comprend plusieurs panneaux. Chaque panneau peut �tre ouvert ou ferm� en cliquant sur la barre de titre en gris. Cliquez sur la barre de titre pour afficher le contenu.

Les panneaux de l'environnement varieront en fonction du type d'environnement et du niveau actif de l'environnement actuel. Pour plus d'informations sur chaque panneau, consultez la section [Environnement de Flamingo](environment.html).

## Menu Outils ![images/library_default.png](images/library_default.png)
{: tools_menu}
Ces param�tres apparaissent �galement dans les menus contextuels du bouton de droite de la souris pour les aper�us et arri�re-plan miniatures.

#### ![images/currentenvironment.png](images/currentenvironment.png) D�finir comme environnement actuel
L'environnement cible est d�fini comme environnement actuel.  L'environnement actuel sera utilis� lors du prochain rendu.

#### ![images/toolbarlus.png](images/toolbarplus.png) Cr�er un nouvel environnement
Cr�e un nouvel environnement de Flamingo.
<!-- Cette partie vient de la page http://docs.mcneel.com/rhino/5/help/en-us/popup_moreinformation/materialthumbnail_contextmenu.htm -->
Ces param�tres apparaissent �galement dans les menus contextuels du bouton de droite de la souris pour les aper�us et arri�re-plan miniatures.

#### ![images/import.png](images/import.png) Importer un environnement � partir d'un fichier
Importe un environnement � partir d'un fichier .renv de Rhino.

#### ![images/savetofile.png](images/savetofile.png) Enregistrer dans un fichier
Enregistre un fichier environnement .renv de Rhino.

#### ![images/changetype.png](images/changetype.png) Modifier le type
Change le type d'un environnement.

#### ![images/changetype.png](images/changetype.png) Modifier le type (Copier les param�tres)
Change le type d'un environnement.
Le comportement par d�faut d�pend du statut actuel de la case [Options de rendu](http://docs.mcneel.com/rhino/5/help/en-us/options/rendering.htm) >  [Copier les param�tres similaires lorsque le type de contenu est modifi�](http://docs.mcneel.com/rhino/5/help/en-us/options/rendering.htm#Copy_similar_settings_when_content_type_is_changed). Si cette case est coch�e, les param�tres compatibles de l'ancien contenu seront copi�s dans le nouveau.

#### ![images/reset.png](images/reset.png) Valeurs par d�faut
Red�finit tous les param�tres par d�faut de l'environnement (arri�re-plan uni noir, arri�re-plan r�fl�chi, ciel et arri�re-plan r�fract� visible).

#### ![images/copy.png](images/copy.png) Copier
Copie l'environnement s�lectionn� dans le presse-papiers de Windows. Le presse-papiers peut ensuite �tre coll� dans l'�diteur afin de cr�er un nouvel environnement ou coll� directement dans un dossier pour cr�er un  fichier de [biblioth�que](libraries.html) file.

#### ![images/paste.png](images/paste.png) Coller
Cr�e un nouvel environnement � partir du contenu du presse-papiers.

#### ![images/pasteasinstance.png](images/pasteasinstance.png) Coller comme occurrence
Cr�e un nouvel environnement � partir du contenu du presse-papiers qui est li� � l'original par instanciation.

#### ![images/delete.png](images/delete.png) Supprimer
Supprime l'environnement s�lectionn�.

#### ![images/rename.png](images/rename.png) Renommer...
Renomme l'environnement s�lectionn�.

#### ![images/duplicate.png](images/duplicate.png) Dupliquer
Copie l'environnement s�lectionn� sur un nouvel environnement avec les m�mes param�tres.

#### ![images/removeinstancing.png](images/removeinstancing.png) Supprimer l'instanciation
Supprime la connexion entre les environnements [copi�s par instance](#paste-as-instance) .

{% include_relative snippets/snippet-contenteditorpreviewoptions.md %}

#### ![images/contentfilter.png](images/contentfilter.png) Filtre de contenu
Ouvre la bo�te de dialogue [Filtres de contenu](content_filters.html) .

#### ![images/rename.png](images/rename.png) Propri�t�s
Ouvre la  bo�te de dialogue [Propri�t�s de l'aper�u](previewproperties.html).
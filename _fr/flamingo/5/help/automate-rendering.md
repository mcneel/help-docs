---
title: Rendu automatis�
---

# {{page.title}}


## Rendu par lots
{: #batch-rendering}
Les travaux par lots vous permettent d'envoyer plusieurs travaux pour calculer automatiquement le rendu. Un travail par lot peut d�finir une vue, une r�solution et un nombre de passes. Les rendus par lot peuvent �tre lanc�s seuls ou envoy�s � la [ferme de rendu](render-farm.html). Ouvrez la liste de lots et ajoutez les travaux dans cette liste. La liste des travaux par lots sera enregistr�e dans le mod�le.

##### O� puis-je trouver cette commande ?

 * Menus > Flamingo nXt 5.0 > Plus d'outils > Rendu par lot

### Bo�te de dialogue du rendu par lots
{: #batch-render}
Commencez par ajouter un travail, puis modifiez les propri�t�s pour d�finir des travaux par lots.

#### Ajouter
Chaque travail par lots est bas� sur une vue enregistr�e dans le mod�le. Cliquez sur l'�l�ment Ajouter pour s�lectionner dans une liste de vues dans le mod�le.  Tous les autres �l�ments du menu sont activ�s lorsqu'un travail est ajout� et s�lectionn�.

#### Supprimer
S�lectionnez un travail par lots existant.  Puis utilisez Supprimer pour retirer le travail de la liste.

#### Propri�t�s
S�lectionnez un travail par lots existant, puis utilisez Propri�t�s pour d�finir les [propri�t�s de rendu par lots](#batch-render-properties).  Les propri�t�s comprennent le nom du fichier, la r�solution et le nombre de passes pour chaque travail.

#### Vers le haut
D�placer le nom de la vue vers le haut dans la liste.

#### Vers le bas
D�placer le nom de la vue vers le bas dans la liste.

#### Liste du lot
{: #batch-list}
Affiche des informations sur la liste des vues � rendre. Double cliquez sur un travail existant, pour modifier les [propri�t�s de rendu par lots](#batch-render-properties).

#### Statut du rendu
Affiche les informations concernant les passes, les lignes de balayage et le temps �coul� du traitement par lots.

####  Arr�ter le rendu
Arr�te le traitement par lots.

#### Rendre le lot localement
{: #render-batch-locally}
Utilise uniquement l'ordinateur actuel pour calculer le rendu des travaux par lot. Les images rendues seront plac�es dans le dossier indiqu� dans les [propri�t�s du travail par lots](#batch-render-properties).

####  Envoyer le lot vers la ferme
Envoie le travail de rendu par lots vers la [ferme de rendu](render-farm.html). Les travaux seront rendus par tous les clients disponibles de la ferme. Les images rendues seront plac�es dans le dossier partag� de la ferme.

### Propri�t�s du rendu par lot
{: #batch-render-properties}

#### Fen�tre � rendre
Affiche la vue qui sera rendue lors de ce travail. Voir [Onglet Rendu, Fen�tre � rendre](render-tab.html#viewtorender).

#### Nom du fichier
Cliquez sur le bouton Enregistrer ![images/saveimageas.png](images/saveimageas.png) et indiquez le nom que vous voulez donner au fichier de l'image rendue.

#### Canal Alpha
Enregistrer l�image avec le canal alpha.  Voir la section [Utiliser un arri�re-plan avec canal alpha](environment-tab.html#alpha) pour plus d'informations. 

#### Utiliser les param�tres du document
{: #rendering-resolution}
Les param�tres de r�solution du document actif sont utilis�s par d�faut pour le rendu. Si une autre r�solution est n�cessaire, d�sactivez cette case et indiquez la r�solution. Voir la rubrique [Onglet Rendu, R�solution](render-tab.html#resolution) pour plus d'informations.

#### Passes de contraintes de rendu
{: #rendering-constraints}
D�finir le nombre de passes n�cessaires pour terminer le travail de rendu. Voir la rubrique [Passes](documentproperties-flamingo.html#number-of-passes) pour plus d'informations.

<!-- TODO: Flamingo nXt 5 runs from the RDK.  The need to Flamingo Automate render is not clear.  What is needed to run animations with nxt right now?
The number of passes and the ability to send a render to the farm are required still.  So the dialog should be smaller.
Alpha channel This needs to be investigated. The rest of this section is commented out.-->

<!-- Commented out until automated render can be determined

## Animations
{: #animation}
Deux options sont disponibles pour cr�er des animations dans Rhino.  Les animations peuvent �tre configur�es en utilisant la [barre d'outils Animation de Rhino](http://docs.mcneel.com/rhino/5/help/en-us/index.htm#commands/animation.htm) ou en utilisant le module d'animation [Bongo](http://bongo.rhino3d.com/).

##### Pour envoyer un travail d'animation vers la ferme de rendu
1. Lancez la commande [FlamingoNXtRenduAutomatique](automate-rendering.html#flamingonxtautomaterender).
1. Dans la bo�te de dialogue Configurer le rendu automatique, s�lectionnez **Rendu vers la ferme**.
&#160;
Indiquez le nom d'un travail et cliquez sur le bouton Accepter.
&#160;
D�finissez un type d'animation dans la barre d'outils Configuration de l'animation de Rhino. S�lectionnez rendu entier comme m�thode de capture.
&#160;
Enregistrez l'animation � partir de la barre d'outils Animation. Les travaux de rendu seront envoy�s vers la ferme de rendu.
&#160;
Lorsque les travaux sont termin�s, lancez � nouveau la commande FlamingoNXtRenduAutomatique et s�lectionnez tous les travaux de la bo�te de dialogue.
&#160;
Cliquez sur le bouton Copier les fichiers s�lectionn�s vers le dossier de destination indiqu� et s�lectionnez un dossier o� copier toutes les images rendues.


## Commande FlamingoNXtRenduAutomatique
{: #flamingonxtautomaterender}


## Configurer la commande de rendu automatique

### Activ�
La commande **Rendu** par d�faut utilise maintenant automatiquement la **ferme de rendu**.

### Utiliser la fen�tre de rendu par d�faut
La commande **Rendu** effectuera le rendu directement au lieu de l'envoyer vers la ferme.

### Nombre de passes de rendu
Indique le nombre de passes de rendu.

### Rendu vers la ferme
La commande **Rendu** enverra directement le rendu vers la ferme.

### Nom du travail
D�finit le [nom du travail](automate-rendering.html#job-name) dans la **ferme de rendu**.

## Contraintes de rendu

### Nombre de passes de rendu
D�finit le [nombres de passes](documentproperties-flamingo.html#number-of-passes).

### Enregistrer le canal alpha
Enregistre l'arri�re-plan avec [canal alpha](render-window.html#save-with-alpha-channel).
-->